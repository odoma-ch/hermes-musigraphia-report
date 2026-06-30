# Technical Approach

## KG Exploration and Caching

The SPARQL subagent's exploration phase generates a **structured report** describing the KG's entity types, properties, relationship patterns, and sample entities. For the CKG, this report contains:

- **120+ entity types** including `CTO_0001005` (Cultural Event/Performance, 2.4M instances), `CTO_0001024` (Music Incipit, 2.2M instances), `mo:MusicalManifestation` (1.6M instances), `schema:MusicEvent` (65K), `schema:MusicComposition` (41K)
- **120+ properties** with their usage counts
- **149 relationship patterns** (two-hop property chains) revealing how entities connect
- **Sample entity profiles** with actual RDF descriptions

This report is usually cached in a database and injected into the subagent's context for every subsequent question, providing the LLM with deep structural understanding of the CKG without requiring any SPARQL queries.

## LLM Stack and Health Routing

Quagga Agent uses a **tiered LLM architecture** with automatic health-based failover:

| Tier | Model | Role |
|------|-------|------|
| Main agent | GLM-5.1 (open weight model) | Tool selection, routing, user interaction |
| SPARQL subagent | GLM-5.1 (open weight model) | SPARQL generation, complex reasoning |
| Tool model | Smaller structured-output model | KG relevance scoring, SPARQL extraction |

The **provider router** (`agent_utils/provider_router.py`) performs health checks every 120 seconds and automatically fails over to backup providers (another open source model) when the primary LLM becomes unavailable. This ensures the system remains operational even during infrastructure instability.

## SPARQL Best Practices Enforcement

The SPARQL subagent is instructed with extensive rules to generate efficient queries against the CKG's Virtuoso endpoint:

- **No full table scans**: Always bind at least one term in triple patterns (critical for 106M triples)
- **Incremental join validation**: Validate each hop independently before combining
- **Limit-first approach**: Use small LIMITs during exploration, paginate with OFFSET
- **Prefix safety**: All namespaces must be declared in PREFIX statements
- **Entity resolution**: Resolve named entities to URIs before querying, never use string filters as URI substitutes
- **Timeout recovery**: On timeout, reduce join width and add constraints incrementally

## Federated and External Data

While the CKG is the core data source, Quagga Agent's architecture supports:

- **MCP-based tool integration**: The GoTriple MCP client (`agent_utils/mcp_client.py`) provides access to scholarly publications, authors, and projects via the Model Context Protocol at `https://gotriple.mcp.netseven.work/mcp`
- **Multiple KG support**: The agent currently supports 7 knowledge graphs (CKG, GESIS KG, EHRI-KG, PHAROS, LinkedMusic, DNB KB, Wikidata) and can be extended to include CORAGO and MIMO
- **SPARQL queries**: The `RunSPARQLTool` can execute queries across different endpoints and improves by itself in case its attempts fail. In short, it is a very simple self-improving harness based on its own mistakes.

### GoTriple MCP Integration

The GoTriple MCP client provides access to scholarly publications and authors via the Model Context Protocol at `https://gotriple.mcp.netseven.work/mcp`. With a single natural-language query, the tool can look up either authors or publications — but not both in a single call. For example, "Find author X" and "Find publication Y" are processed as separate lookup types within the same tool.
