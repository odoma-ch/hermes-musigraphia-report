# Scientific Transparency

A key requirement of the challenge is scientific transparency. Quagga Agent addresses this at multiple levels:

## SPARQL Query Exposure

Every answer includes the exact SPARQL query used, with all prefixes, formatting, and whitespace preserved. The `validate_sparql_tool` extracts the query from the subagent response and presents it alongside the natural-language answer.

Also since we use OpenWebUI, we can export the conversation using a web link for other users of the Quagga Agent or for wider use using a PDF or JSON file export.

## Tool Call Visibility

The OpenWebUI interface displays all tool calls and their results, making the agent's reasoning process fully inspectable. Users can see:

- Which KG was selected and why (relevance scores)
- What was the query which led to the answer and metadata like: how many SPARQL queries were attempted?
- The final validated answer and its results (presented as markdown)

## Federated Query Potential

The CKG uses `NFDI_0001006` (external identifier) to link entities to Wikidata, ROR, GND, and other authority records—over 11 million such links. This shared authority data enables querying other knowledge graphs (Wikidata/GND) to verify the underlying data or use SPARQL `SERVICE` federated queries across the CKG and external endpoints, which the agent can generate when the user's question requires cross-KG data.

Cross-KG exploration in practice is illustrated in the [Bach case study](../explorations/harshdeep.md#exploration-1-johann-sebastian-bach) and the [Detmolder Hoftheater study](../explorations/detmolder-hoftheater.md#enriching-the-data-from-dnb).
