# System Architecture

## High-Level Overview

Quagga Agent follows a **multi-agent architecture** built on LangGraph state machines, with a main routing agent that delegates to a specialised SPARQL subagent. The system comprises four layers:

```
┌─────────────────────────────────────────────────┐
│              User Interface Layer               │
│        OpenWebUI  /  OpenAI-compatible API      │
├─────────────────────────────────────────────────┤
│           Main Agent (LangGraph StateGraph)     │
│  scope_checker → sparql_chat_agent → tools →    │
│  run_sparql_subagent → force_validate → END     │
├─────────────────────────────────────────────────┤
│         SPARQL Subagent (Two-Phase Pipeline)    │
│  Phase 1: explore_kg (schema discovery)         │
│  Phase 2: answer_question (query generation)    │
├─────────────────────────────────────────────────┤
│           Infrastructure Layer                  │
│  API to get KG metadata | SPARQL Endpoints      │
│  PostgreSQL (checkpointing) | LLM Providers     │
└─────────────────────────────────────────────────┘
```

## Main Agent Graph

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

## SPARQL Subagent Pipeline

The SPARQL subagent is itself a LangGraph agent with a two-phase pipeline:

### Phase 1: Knowledge Graph Exploration (`explore_kg`)

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

### Phase 2: Question Answering (`answer_question`)

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

## Tool Arsenal

| Tool | Purpose |
|------|---------|
| `scope_checker_tool` | Classifies user questions against known KGs using a structured-output LLM, fetches KG metadata |
| `run_sparql_subagent_tool` | Delegates to the two-phase SPARQL subagent |
| `validate_sparql_tool` | Extracts SPARQL from subagent response, formats for display |
| `RunSPARQLTool` | Direct SPARQL query execution against the endpoint |
| `describe_knowledge_graphs_tool` | Lists available KGs with descriptions |
| MCP tools (dynamic) | GoTriple scholarly search tools (publications, authors, projects) |
