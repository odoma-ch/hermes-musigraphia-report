# Technical Report: Quagga Agent — An AI-Driven Exploration Tool for Musicological Data in the Culture Knowledge Graph

**Submitted to:** HERMES Data Challenge 2026 — "From Notes to Nodes"
**Team:** [Team Name]
**Members:** Harshdeep Singh, Matteo Romanello, Polina Proutskova, Olga Velichkina

---

## 1. Introduction

This report describes **Quagga Agent**, an LLM-powered conversational agent that enables researchers to explore musicological knowledge in the Culture Knowledge Graph (CKG) and beyond—without requiring any SPARQL expertise. The agent accepts natural-language research questions, autonomously identifies the relevant knowledge graph, retrieves and understands its schema, generates and executes SPARQL queries, and returns verified, structured results with full scientific transparency.

Quagga Agent was originally developed within the EU-funded GRAPHIA project (grant 101188018) as a general-purpose SPARQL agent for multiple knowledge graphs in the social sciences and humanities. For this challenge, we have adapted and deployed it specifically for musicological exploration of the CKG, leveraging its rich RISM, musiconn.performance, APSearch, and Detmolder Hoftheater datasets.

---

## 2. Problem Statement

The HERMES Data Challenge asks:

> *How can musicologists easily interact with a knowledge graph and retrieve relevant information without being SPARQL experts?*

This is a significant barrier. The CKG contains approximately 106 million RDF triples spanning musical works, sources, persons, performances, places, and historical contexts—described using the NFDI4Culture Ontology (CTO), NFDIcore, Schema.org, CIDOC-CRM, the Music Ontology, and FaBiO. Writing correct SPARQL queries against this heterogeneous schema requires:

1. **Ontological knowledge** — understanding which CTO/NFDI classes and properties encode performances, incipits, manifestations, etc.
2. **Query language proficiency** — constructing syntactically valid SPARQL with proper prefix declarations, join patterns, aggregation, and filtering.
3. **Endpoint-specific awareness** — knowing the Virtuoso triple store's quirks, named graph structure, and performance characteristics (e.g., avoiding full table scans on 106M triples).

Quagga Agent eliminates all three barriers by acting as an intelligent intermediary.

---

## 3. System Architecture

### 3.1 High-Level Overview

Quagga Agent follows a **multi-agent architecture** built on LangGraph state machines, with a main routing agent that delegates to a specialised SPARQL subagent. The system comprises four layers:

```
┌─────────────────────────────────────────────────┐
│              User Interface Layer                │
│        OpenWebUI  /  OpenAI-compatible API       │
├─────────────────────────────────────────────────┤
│           Main Agent (LangGraph StateGraph)      │
│  scope_checker → sparql_chat_agent → tools →     │
│  run_sparql_subagent → force_validate → END      │
├─────────────────────────────────────────────────┤
│         SPARQL Subagent (Two-Phase Pipeline)     │
│  Phase 1: explore_kg (schema discovery)          │
│  Phase 2: answer_question (query generation)     │
├─────────────────────────────────────────────────┤
│           Infrastructure Layer                    │
│  API to get KG metadata | SPARQL Endpoints  │
│  PostgreSQL (checkpointing) | LLM Providers       │
└─────────────────────────────────────────────────┘
```

### 3.2 Main Agent Graph

The main agent is implemented as a LangGraph `StateGraph` with the following nodes and edges:

| Node | Role |
|------|------|
| `sparql_chat_agent` | LLM node: receives messages, decides tool calls based on system prompts |
| `tools` | `ToolNode`: executes LangChain tools and returns results |
| Validate SPARQL query | Graph-enforced validation: automatically call a tool to validate query after the SPARQL subagent completes |

**Control flow:**
1. User message enters `sparql_chat_agent`
2. The LLM calls `scope_checker_tool` to identify the relevant KG
3. The LLM calls `run_sparql_subagent_tool` to delegate question answering
4. The graph automatically routes to `force_validate` which extracts and formats the final SPARQL query and results
5. The validated response is returned to the user

This graph-enforced validation ensures that **every** SPARQL answer is scientifically transparent—the generated query and reasoning steps are always exposed to the user.

### 3.3 SPARQL Subagent Pipeline

The SPARQL subagent is itself a LangGraph agent with a two-phase pipeline:

**Phase 1: Knowledge Graph Exploration (`explore_kg`)**
- Checks for a cached exploration report for the identified KG
- If no cache exists, runs a systematic multi-step SPARQL exploration:
  1. Discover eligible named graphs
  2. Retrieve entity types and their counts
  3. Retrieve property usage statistics
  4. Describe sample entities of the top types
  5. Discover relationship patterns (two-hop property chains)
  6. Discover entity-value patterns
  7. Compile a structured exploration report
- The report is cached locally for future queries, avoiding redundant exploration

**Phase 2: Question Answering (`answer_question`)**
- Receives the exploration context and the user's question
- Uses a large LLM (DeepSeek-V3.1, 128K context) with the `run_sparql_tool` to iteratively generate and execute SPARQL queries
- Follows a disciplined workflow:
  - Step 0: Check cached KG description for fast capability answers
  - Step 1: Consult the cached KG description for relevant classes/properties
  - Step 2: Run targeted exploration queries
  - Step 3: Validate joins incrementally before complex queries
  - Step 4: Refine queries based on results
  - Step 5: Provide the final answer with SPARQL, metrics, and result table
- Enforces a hard limit of `N` (=80) SPARQL queries per question, with a summary mechanism when the limit is reached

### 3.4 Tool Arsenal

| Tool | File | Purpose |
|------|------|---------|
| `scope_checker_tool` | `tools.py:154` | Classifies user questions against known KGs using a structured-output LLM, fetches KG metadata |
| `run_sparql_subagent_tool` | `tools.py:480` | Delegates to the two-phase SPARQL subagent |
| `validate_sparql_tool` | `tools.py:579` | Extracts SPARQL from subagent response, formats for display |
| `RunSPARQLTool` | `tools.py:504` | Direct SPARQL query execution against the endpoint |
| `describe_knowledge_graphs_tool` | `tools.py:468` | Lists available KGs with descriptions |
| MCP tools (dynamic) | `mcp_client.py:133` | GoTriple scholarly search tools (publications, authors, projects) |

---

## 4. Technical Approach

### 4.1 KG Exploration and Caching

The SPARQL subagent's exploration phase generates a **structured report** describing the KG's entity types, properties, relationship patterns, and sample entities. For the CKG, this report contains:

- **120+ entity types** including `CTO_0001005` (Cultural Event/Performance, 2.4M instances), `CTO_0001024` (Music Incipit, 2.2M instances), `mo:MusicalManifestation` (1.6M instances), `schema:MusicEvent` (65K), `schema:MusicComposition` (41K)
- **120+ properties** with their usage counts
- **149 relationship patterns** (two-hop property chains) revealing how entities connect
- **Sample entity profiles** with actual RDF descriptions

This report is usually cached in a database and injected into the subagent's context for every subsequent question, providing the LLM with deep structural understanding of the CKG without requiring any SPARQL queries.

### 4.2 LLM Stack and Health Routing

Quagga Agent uses a **tiered LLM architecture** with automatic health-based failover:

| Tier | Model | Role |
|------|-------|------|
| Main agent | GLM-5.1 (open weight model) | Tool selection, routing, user interaction |
| SPARQL subagent | GLM-5.1 (open weight model) | SPARQL generation, complex reasoning |
| Tool model | Smaller structured-output model | KG relevance scoring, SPARQL extraction |

The **provider router** (`agent_utils/provider_router.py`) performs health checks every 120 seconds and automatically fails over to backup providers (another open source model) when the primary LLM becomes unavailable. This ensures the system remains operational even during infrastructure instability.

### 4.4 SPARQL Best Practices Enforcement

The SPARQL subagent is instructed with extensive rules to generate efficient queries against the CKG's Virtuoso endpoint:

- **No full table scans**: Always bind at least one term in triple patterns (critical for 106M triples)
- **Incremental join validation**: Validate each hop independently before combining
- **Limit-first approach**: Use small LIMITs during exploration, paginate with OFFSET
- **Prefix safety**: All namespaces must be declared in PREFIX statements
- **Entity resolution**: Resolve named entities to URIs before querying, never use string filters as URI substitutes
- **Timeout recovery**: On timeout, reduce join width and add constraints incrementally

### 4.5 Federated and External Data

While the CKG is the core data source, Quagga Agent's architecture supports:

- **MCP-based tool integration**: The GoTriple MCP client (`agent_utils/mcp_client.py`) provides access to scholarly publications, authors, and projects via the Model Context Protocol at `https://gotriple.mcp.netseven.work/mcp`
- **Multiple KG support**: The agent currently supports 7 knowledge graphs (CKG, GESIS KG, EHRI-KG, PHAROS, LinkedMusic, DNB KB, Wikidata) and can be extended to include CORAGO and MIMO
- **SPARQL queries**: The `RunSPARQLTool` can execute queries across different endpoints and improves by itself incase its attempts fail. In short, it is a very simple self improving harness base on its own mistakes.

---

## 5. Musicological Adequacy

Quagga Agent is designed to address authentic musicological research questions. The CKG exploration report reveals that the graph contains rich musicological data:

### 5.1 Supported Musicological Question Types

| Question Type | CKG Data Sources | Key Classes/Properties |
|---------------|-----------------|----------------------|
| Composer works and catalogues | RISM (~28M triples) | `schema:MusicComposition`, `mo:MusicalManifestation`, `CTO_0001024` (incipits) |
| Performance repertoire studies | musiconn.performance (~2M) | `CTO_0001005` (performances), `CTO_0001070` (dates), `CTO_0001011` (venues) |
| Source verification | RISM | `CTO_0001025` (has manifestation), `CTO_0001019` (related work) |
| Incipit-based identification | RISM | `CTO_0001063` (Plaine & Easie), `CTO_0001060` (time signature), `CTO_0001062` (key signature) |
| Historical performance context | Detmolder Hoftheater | `schema:MusicEvent`, `CTO_0001071` |
| Person-institution networks | NFDIcore | `NFDI_0000004` (Person), `NFDI_0000003` (Organisation), `schema:member` |
| Geographic studies | All sources | `NFDI_0000005` (Place), `schema:geo`, `schema:latitude/longitude` |

### 5.2 Example Musicological Queries

The agent can handle questions such as:

- *"Which works by Mozart have incipits in B-flat major stored in RISM?"*
- *"List all performances at the Kulturpalast Dresden between 1980 and 1990."*
- *"What are the most common instruments in Detmolder Hoftheater performances?"*
- *"Which RISM institutions hold sources by J.S. Bach?"*
- *"How many musical sources in the CKG are autographs vs. copies?"*

The CKG exploration report's relationship patterns reveal that `NFDI_0001006` serves as the primary **cross-KG alignment mechanism**—linking CKG entities to Wikidata, ROR, GND, and other authority records. This enables entity resolution across data silos.

---

## 6. User Experience

### 6.1 Conversational Interface

Quagga Agent provides a conversational interface via **OpenWebUI**, a widely-used open-source chat UI. The agent appears as a model named "Graphia SPARQL Agent" in the model selector. Users interact entirely in natural language—no knowledge of SPARQL, the CTO ontology, or the CKG endpoint is required.

### 6.2 Streaming and Progress Indicators

The agent streams responses in real-time using a custom SSE protocol with multiple chunk types:

| Chunk Type | Purpose |
|------------|---------|
| `progress` | Status updates ("Selecting knowledge graph(s)", "Retrieving metadata", "Generating SPARQL query") |
| `tool_call` / `tool_result` | Tool execution transparency |
| `llm_text` | Final answer text |
| `reasoning_content` | Renders as "Thinking..." in OpenWebUI for progress steps |

The `QuaggaProgressPipe` OpenWebUI filter (`filters/progress_pipe.py`) translates progress chunks into native OpenWebUI status indicators, giving users real-time feedback during the 10-60 second query generation process.

### 6.3 Multi-Turn Conversations

The agent maintains conversation state via **PostgreSQL-backed checkpointing** (AsyncPostgresSaver). Follow-up questions inherit context from previous turns—the subagent receives formatted parent context including prior questions, answers, and SPARQL queries. This enables natural research workflows like:

> **User:** What performances are in the CKG?
> **Agent:** *[lists performances]*
> **User:** How many of those were in Dresden?
> **Agent:** *[refines query based on previous context]*

---

## 7. Scientific Transparency

A key requirement of the challenge is scientific transparency. Quagga Agent addresses this at multiple levels:

### 7.1 SPARQL Query Exposure

Every answer includes the exact SPARQL query used, with all prefixes, formatting, and whitespace preserved. The `validate_sparql_tool` extracts the query from the subagent response and presents it alongside the natural-language answer.

### 7.2 Tool Call Visibility

The OpenWebUI interface displays all tool calls and their results, making the agent's reasoning process fully inspectable. Users can see:
- Which KG was selected and why (relevance scores)
- What was the query which led to the answer and metadata like: how many SPARQL queries were attempted?
- The final validated answer and its results (presented as markown)

### 7.3 Federated Query Potential

The CKG uses `NFDI_0001006` (external identifier) to link entities to Wikidata, ROR, GND, and other authority records—over 11 million such links. This shared authority data enables to query other knowledge graphs (Wikidata/GND) to verify the underlying data or use SPARQL `SERVICE` federated queries across the CKG and external endpoints, which the agent can generate when the user's question requires cross-KG data.

---

## 12. Limitations and Future Work

### 12.1 Current Limitations

- **Single-KG queries**: While the architecture supports multiple KGs, each query currently targets one KG at a time. Federated queries across CKG + CORAGO/Wikidata require user to manually steer the conversation or for advanced user to manually trigger the `SERVICE` clause generation.
- **Exploration cost**: First-time KG exploration (before caching) can require 15-30 SPARQL queries and take 2-5 minutes. Subsequent queries benefit from the cached report.
- **Result size limits**: The `RunSPARQLTool` caps results at 50 rows to avoid endpoint timeouts, which may truncate very large result sets.
- **Language bias**: The CKG's labels are predominantly German and English; the agent's effectiveness depends on the LLM's multilingual capabilities.

### 12.2 Planned Enhancements

- **CORAGO integration**: Add the CORAGO Italian opera repository as a supplementary KG, enabling queries for libretto references.
- **GND alignment**: Leverage the CKG's existing `NFDI_0001006` links to GND for person/place disambiguation across datasets.
- **Automatic cross-KG federation**: 
  - Implement transparent federation across multiple knowledge graphs (CKG, CORAGO, Wikidata, GND, MIMO) without requiring the user to explicitly request or trigger cross-source queries—the agent would autonomously detect when a question spans multiple KGs (e.g., resolving a composer via GND authority links, enriching performance data with CORAGO libretto references, or supplementing RISM source records with Wikidata biographical metadata).
  - Compose SPARQL SERVICE federated queries accordingly, turning the single-KG query flow into a seamless multi-source exploration behind a single conversational interface.
- **Visualization**: Add more relevant tools for result visualization (e.g., performance timelines, geographic maps, network graphs) to the OpenWebUI interface.
---
