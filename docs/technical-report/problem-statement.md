# Problem Statement

The HERMES Data Challenge asks:

> *How can musicologists easily interact with a knowledge graph and retrieve relevant information without being SPARQL experts?*

This is a significant barrier. The CKG contains approximately 106 million RDF triples spanning musical works, sources, persons, performances, places, and historical contexts—described using the NFDI4Culture Ontology (CTO), NFDIcore, Schema.org, CIDOC-CRM, the Music Ontology, and FaBiO. Writing correct SPARQL queries against this heterogeneous schema requires:

1. **Ontological knowledge** — understanding which CTO/NFDI classes and properties encode performances, incipits, manifestations, etc.
2. **Query language proficiency** — constructing syntactically valid SPARQL with proper prefix declarations, join patterns, aggregation, and filtering.
3. **Endpoint-specific awareness** — knowing the Virtuoso triple store's quirks, named graph structure, and performance characteristics (e.g., avoiding full table scans on 106M triples).

Quagga Agent eliminates all three barriers by acting as an intelligent intermediary.
