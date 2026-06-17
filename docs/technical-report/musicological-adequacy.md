# Musicological Adequacy

Quagga Agent is designed to address authentic musicological research questions. The CKG exploration report reveals that the graph contains rich musicological data:

## Supported Musicological Question Types

| Question Type | CKG Data Sources | Key Classes/Properties |
|---------------|-----------------|----------------------|
| Composer works and catalogues | RISM (~28M triples) | `schema:MusicComposition`, `mo:MusicalManifestation`, `CTO_0001024` (incipits) |
| Performance repertoire studies | musiconn.performance (~2M) | `CTO_0001005` (performances), `CTO_0001070` (dates), `CTO_0001011` (venues) |
| Source verification | RISM | `CTO_0001025` (has manifestation), `CTO_0001019` (related work) |
| Incipit-based identification | RISM | `CTO_0001063` (Plaine & Easie), `CTO_0001060` (time signature), `CTO_0001062` (key signature) |
| Historical performance context | Detmolder Hoftheater | `schema:MusicEvent`, `CTO_0001071` |
| Person-institution networks | NFDIcore | `NFDI_0000004` (Person), `NFDI_0000003` (Organisation), `schema:member` |
| Geographic studies | All sources | `NFDI_0000005` (Place), `schema:geo`, `schema:latitude/longitude` |

## Example User Queries

The agent can handle questions such as:

- *"Retrieve the Plaine & Easie notation strings and tonal centers for all music incipits that feature a C-4 clef and a 3/4 time signature."*
- *"List all performances at the Kulturpalast Dresden between 1980 and 1990."*
- *"What are the most common instruments in Detmolder Hoftheater performances?"*
- *"List persons with profession/role links to musicology in CKG"*
- *"Which RISM institutions are most frequently referenced as holding musical source manifestations in the knowledge graph, ranked by the number of holdings?"*

The CKG exploration report's relationship patterns reveal that `NFDI_0001006` serves as the primary **cross-KG alignment mechanism**—linking CKG entities to Wikidata, ROR, GND, and other authority records. This enables entity resolution across data silos.

See also the [case studies](../explorations/harshdeep.md) for documented examples.
