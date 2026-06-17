# Limitations and Future Work

## Current Limitations

- **Single-KG queries**: While the architecture supports multiple KGs, each query currently targets one KG at a time. Federated queries across CKG + CORAGO/Wikidata require the user to manually steer the conversation or for advanced users to manually trigger the `SERVICE` clause generation.
- **Exploration cost**: First-time KG exploration (before caching) can require 15–30 SPARQL queries and take 2–5 minutes. Subsequent queries benefit from the cached report.
- **Result size limits**: The `RunSPARQLTool` caps results at 50 rows to avoid endpoint timeouts, which may truncate very large result sets.
- **Language bias**: The CKG's labels are predominantly German and English; the agent's effectiveness depends on the LLM's multilingual capabilities.

## Planned Enhancements

- **CORAGO integration**: Add the CORAGO Italian opera repository as a supplementary KG, enabling queries for libretto references.
- **GND alignment**: Leverage the CKG's existing `NFDI_0001006` links to GND for person/place disambiguation across datasets.
- **Automatic cross-KG federation**:
  - Implement transparent federation across multiple knowledge graphs (CKG, CORAGO, Wikidata, GND, MIMO) without requiring the user to explicitly request or trigger cross-source queries—the agent would autonomously detect when a question spans multiple KGs (e.g., resolving a composer via GND authority links, enriching performance data with CORAGO libretto references, or supplementing RISM source records with Wikidata biographical metadata).
  - Compose SPARQL SERVICE federated queries accordingly, turning the single-KG query flow into a seamless multi-source exploration behind a single conversational interface.
- **Visualization**: Add more relevant tools for result visualization (e.g., performance timelines, geographic maps, network graphs) to the OpenWebUI interface.

An early visualization example — an interactive map of German performance venues enriched with Wikidata coordinates — is documented in the [venues case study](../explorations/harshdeep.md#interactive-map).
