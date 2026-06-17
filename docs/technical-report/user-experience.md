# User Experience

## Conversational Interface

Quagga Agent provides a conversational interface via **OpenWebUI**, a widely-used open-source chat UI. The agent appears as a model named "Graphia SPARQL Agent" in the model selector. Users interact entirely in natural language—no knowledge of SPARQL, the CTO ontology, or the CKG endpoint is required.

## Streaming and Progress Indicators

The agent streams responses in real-time using a custom SSE protocol with multiple chunk types:

| Chunk Type | Purpose |
|------------|---------|
| `progress` | Status updates ("Selecting knowledge graph(s)", "Retrieving metadata", "Generating SPARQL query") |
| `tool_call` / `tool_result` | Tool execution transparency |
| `llm_text` | Final answer text |
| `reasoning_content` | Renders as "Thinking..." in OpenWebUI for progress steps |

The `QuaggaProgressPipe` OpenWebUI filter (`filters/progress_pipe.py`) translates progress chunks into native OpenWebUI status indicators, giving users real-time feedback during the 10–60 second query generation process.

## Multi-Turn Conversations

The agent maintains conversation state via **PostgreSQL-backed checkpointing** (AsyncPostgresSaver). Follow-up questions inherit context from previous turns—the subagent receives formatted parent context including prior questions, answers, and SPARQL queries. This enables natural research workflows like:

> **User:** Are there any Russian operas in the graph? Which ones?
> **Agent:** *[lists operas]*
> **User:** Romeo and Julia by Tchaikovsky? What's that? 1812 Ouvertuere - from which work is it?
> **Agent:** *[refines query based on previous context]*

A full multi-turn example is available in [this Quagga conversation](https://quagga-agent.graphia-ssh.eu/s/0ce0e13d-1ccf-4698-9c4e-ca97149e1d74); see also [Russian operas and ballets](../explorations/polina.md#exploration-2-russian-operas-and-ballets) for a critical assessment of similar queries.
