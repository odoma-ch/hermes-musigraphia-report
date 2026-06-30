### USER
What knowledge graphs can I explore?

### ASSISTANT
**Checking available knowledge graphs**


<details>
<summary>Result from Checking available knowledge graphs</summary>

```json
[
  {
    "kg_name": "Culture Knowledge Graph",
    "description": "large-scale semantic infrastructure developed within  NFDI4Culture￼ to interconnect heterogeneous cultural heritage and humanities research data — including musicology, art history, performance, archives, and audiovisual collections. It aggregates metadata from distributed repositories into a shared graph based on ontologies such as NFDIcore and the NFDI4Culture Ontology (CTO), enabling cross-collection discovery, SPARQL querying, interoperability, and AI-driven exploration of cultural data across institutions and domains.",
    "endpoint_url": "https://nfdi4culture.de/sparql"
  },
  {
    "kg_name": "GESIS KG",
    "description": "The GESIS Knowledge Graph (GESIS KG) is an integrated research knowledge graph that captures and interlinks metadata of scientific resources—such as datasets, publications, variables, and survey instruments—along with entities like authors and social science concepts, from GESIS Search.",
    "endpoint_url": "https://data.gesis.org/gesiskg/sparql"
  },
  {
    "kg_name": "EHRI - KG",
    "description": "The EHRI Knowledge Graph (EHRI-KG) is a Linked Open Data (LOD) representation of the EHRI Portal’s metadata about Holocaust-related archival sources. Developed to complement the EHRI Portal, it transforms archival descriptions—such as countries, institutions, collection records, and more—into a semantically enriched, interlinked graph.",
    "endpoint_url": "https://lod.ehri-project-test.eu/sparql"
  },
  {
    "kg_name": "PHAROS",
    "description": "PHAROS (via artresearch.net) is the International Association of Photo Archives — a consortium of leading European and North American art-historical photographic archives that unifies tens of millions of images of art, architecture, and documentary photography with rich scholarly metadata. Founded to advance access, standardization, and digital humanities research, PHAROS maps and links dispersed collections using CIDOC-CRM and ResearchSpace technologies, enabling consolidated searching, image-to-image comparison, and interdisciplinary scholarship. Its Artresearch.net platform launched in 2025, offering free, centralized access to an unprecedented visual and data resource for art history research and teaching.",
    "endpoint_url": "https://artresearch.net/sparql"
  },
  {
    "kg_name": "LinkedMusic",
    "description": "A federated graph of 14 music databases, including The Global Jukebox, Dig That Lick, The Sessions, RISM, MusicBrainz and more",
    "endpoint_url": "https://virtuoso.simssa.ca/sparql"
  }
]
```
</details>

Here are the knowledge graphs you can explore:

1. **Culture Knowledge Graph** — A large-scale semantic infrastructure from NFDI4Culture that interconnects cultural heritage and humanities research data, including musicology, art history, performance, archives, and audiovisual collections. It aggregates metadata from distributed repositories using ontologies like NFDIcore and CTO.
   - 🔗 Endpoint: `https://nfdi4culture.de/sparql`

2. **GESIS KG** — An integrated research knowledge graph capturing and interlinking metadata of scientific resources such as datasets, publications, variables, and survey instruments, along with authors and social science concepts from GESIS Search.
   - 🔗 Endpoint: `https://data.gesis.org/gesiskg/sparql`

3. **EHRI - KG** — A Linked Open Data representation of the EHRI Portal's metadata about Holocaust-related archival sources. It transforms archival descriptions—countries, institutions, collection records—into a semantically enriched, interlinked graph.
   - 🔗 Endpoint: `https://lod.ehri-project-test.eu/sparql`

4. **PHAROS** — The International Association of Photo Archives, unifying tens of millions of images of art, architecture, and documentary photography with rich scholarly metadata. It uses CIDOC-CRM and ResearchSpace technologies for consolidated searching and interdisciplinary scholarship via the Artresearch.net platform.
   - 🔗 Endpoint: `https://artresearch.net/sparql`

5. **LinkedMusic** — A federated graph of 14 music databases, including The Global Jukebox, Dig That Lick, The Sessions, RISM, MusicBrainz, and more.
   - 🔗 Endpoint: `https://virtuoso.simssa.ca/sparql`

Feel free to ask me any question about the data in any of these knowledge graphs, and I'll query it for you!

### USER
What kind of data can I find in LinkedMusic (LM)?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

The LinkedMusic knowledge graph integrates music-related data from 11 source datasets, each stored in its own named graph. Here are the main entity types and their counts:

| Source Graph | Entity Type | Count |
|---|---|---|
| **MusicBrainz** | Artist | 2,649,740 |
| | Recording | 2,198,791 |
| | Release | 1,101,712 |
| | Label | 310,248 |
| | Area | 119,677 |
| | Event | 101,420 |
| | Place | 73,636 |
| | Genre | 2,051 |
| | Instrument | 1,050 |
| **RISM** | Incipit | 2,391,497 |
| | Source | 1,526,463 |
| | Exemplar | 934,538 |
| | Person | 148,172 |
| | Institution | 25,708 |
| | Place | 16,119 |
| | Subject | 646 |
| | ExemplarsSection | 240 |
| **CantusDB** | Chant | 444,171 |
| | Source | 236 |
| **UTSI** | Song | 56,895 |
| | Anthology | 2,622 |
| **DIAMM** | Composition | 60,210 |
| | Source | 4,603 |
| | Person | 4,151 |
| | Organization | 709 |
| | Archive | 681 |
| | City | 608 |
| | Set | 472 |
| | Region | 77 |
| | Country | 34 |
| **CantusIndex** | Chant | 60,426 |
| **The Session** | Tuneset | 88,020 |
| | TuneSetting | 51,350 |
| | Tune | 22,276 |
| | Member | 9,476 |
| | Events | 7,947 |
| | Recording | 7,644 |
| | Session | 2,035 |
| **The Global Jukebox** | Song | 6,040 |
| | Instrument | 1,780 |
| | Culture | 1,302 |
| | Ensemble | 774 |
| | Minutage | 687 |
| | Phonotactics | 338 |
| | Parlametrics | 188 |
| | Source | 138 |
| **Dig That Lick** | Solo | 1,685 |
| | Track | 616 |
| **WJazzD** | Solo | 456 |
| | Track | 344 |
| | Composition | 302 |
| | Record | 184 |
| **SIMSSADB** | File | 2,241 |
| | Section | 125 |
| | Work | 98 |
| | Source | 78 |
| | Person | 29 |
| | GenreAsInType | 8 |

**Summary of data domains:**

- **Popular & mainstream music metadata** (MusicBrainz): Artists, recordings, releases, labels, events, places, genres, instruments
- **Historical musical sources** (RISM): Incipits, sources, exemplars, people, institutions, places
- **Gregorian chant** (CantusDB & CantusIndex): Chants, sources, chant modes, genres
- **Medieval music manuscripts** (DIAMM): Compositions, sources, people, archives, cities
- **Irish traditional music** (The Session): Tunes, tune settings, tune sets, sessions, members
- **Folk & traditional songs** (UTSI): Songs, anthologies, languages
- **World music & ethnomusicology** (The Global Jukebox): Songs, instruments, cultures, ensembles
- **Jazz solo transcription** (Dig That Lick & WJazzD): Solos, tracks, instruments
- **Cantata analysis** (SIMSSADB): Files, sections, works, sources

Common cross-cutting Wikidata properties link these graphs together, including **P86** (composer), **P175** (performer), **P136** (genre), **P361** (part of), **P276** (location), **P2888** (see also), and **P826** (mode).
</details>

**Validating and executing SPARQL query**


The LinkedMusic knowledge graph integrates music-related data from 11 source datasets, each stored in its own named graph. Here are the main entity types and their counts:

| Source Graph | Entity Type | Count |
|---|---|---|
| **MusicBrainz** | Artist | 2,649,740 |
| | Recording | 2,198,791 |
| | Release | 1,101,712 |
| | Label | 310,248 |
| | Area | 119,677 |
| | Event | 101,420 |
| | Place | 73,636 |
| | Genre | 2,051 |
| | Instrument | 1,050 |
| **RISM** | Incipit | 2,391,497 |
| | Source | 1,526,463 |
| | Exemplar | 934,538 |
| | Person | 148,172 |
| | Institution | 25,708 |
| | Place | 16,119 |
| | Subject | 646 |
| | ExemplarsSection | 240 |
| **CantusDB** | Chant | 444,171 |
| | Source | 236 |
| **UTSI** | Song | 56,895 |
| | Anthology | 2,622 |
| **DIAMM** | Composition | 60,210 |
| | Source | 4,603 |
| | Person | 4,151 |
| | Organization | 709 |
| | Archive | 681 |
| | City | 608 |
| | Set | 472 |
| | Region | 77 |
| | Country | 34 |
| **CantusIndex** | Chant | 60,426 |
| **The Session** | Tuneset | 88,020 |
| | TuneSetting | 51,350 |
| | Tune | 22,276 |
| | Member | 9,476 |
| | Events | 7,947 |
| | Recording | 7,644 |
| | Session | 2,035 |
| **The Global Jukebox** | Song | 6,040 |
| | Instrument | 1,780 |
| | Culture | 1,302 |
| | Ensemble | 774 |
| | Minutage | 687 |
| | Phonotactics | 338 |
| | Parlametrics | 188 |
| | Source | 138 |
| **Dig That Lick** | Solo | 1,685 |
| | Track | 616 |
| **WJazzD** | Solo | 456 |
| | Track | 344 |
| | Composition | 302 |
| | Record | 184 |
| **SIMSSADB** | File | 2,241 |
| | Section | 125 |
| | Work | 98 |
| | Source | 78 |
| | Person | 29 |
| | GenreAsInType | 8 |

**Summary of data domains:**

- **Popular & mainstream music metadata** (MusicBrainz): Artists, recordings, releases, labels, events, places, genres, instruments
- **Historical musical sources** (RISM): Incipits, sources, exemplars, people, institutions, places
- **Gregorian chant** (CantusDB & CantusIndex): Chants, sources, chant modes, genres
- **Medieval music manuscripts** (DIAMM): Compositions, sources, people, archives, cities
- **Irish traditional music** (The Session): Tunes, tune settings, tune sets, sessions, members
- **Folk & traditional songs** (UTSI): Songs, anthologies, languages
- **World music & ethnomusicology** (The Global Jukebox): Songs, instruments, cultures, ensembles
- **Jazz solo transcription** (Dig That Lick & WJazzD): Solos, tracks, instruments
- **Cantata analysis** (SIMSSADB): Files, sections, works, sources

Common cross-cutting Wikidata properties link these graphs together, including **P86** (composer), **P175** (performer), **P136** (genre), **P361** (part of), **P276** (location), **P2888** (see also), and **P826** (mode).

### USER
Do you have anything here about August von Kotzebue (Q57242)?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: Culture Knowledge Graph
</details>

**Querying knowledge graph**

### USER
Is there are information in LinkedMusic related to August von Kotzebue (Q57242)?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

**Yes**, LinkedMusic contains information related to August von Kotzebue (Q57242). He appears in two source graphs:

### 1. MusicBrainz (`https://linkedmusic.ca/graphs/musicbrainz/`)

**Entity:** `https://musicbrainz.org/artist/014d3c1a-57a4-49cb-bcf9-2c8a61c25c70`

| Property | Value |
|---|---|
| **Label** | August von Kotzebue |
| **Type** | Artist (Q5 = human) |
| **Birth date (P569)** | 1761-05-03 |
| **Death date (P570)** | 1819-03-23 |
| **Sex (P21)** | Q6581097 (male) |
| **Birth place (P19)** | Weimar (MusicBrainz area) |
| **Death place (P20)** | Mannheim (MusicBrainz area) |
| **Nationality (P27)** | Germany (MusicBrainz area) |
| **External links (P2888)** | Wikidata (Q57242), VIAF (14771963), GND (118565796), BnF, IMDb, IMSLP, Discogs, Open Library, WorldCat, SNAC, NLA |

### 2. RISM (`https://linkedmusic.ca/graphs/rism/`)

**Entity:** `https://rism.online/people/34844`

| Property | Value |
|---|---|
| **Label** | Kotzebue, August von (1761-1819) |
| **Type** | Person |
| **External link (P2888)** | Wikidata Q57242 |

Both records are linked to the same Wikidata entity (Q57242), confirming they refer to the same person — the German playwright and author August von Kotzebue (1761–1819).
</details>

**Validating and executing SPARQL query**


Yes, LinkedMusic contains information related to August von Kotzebue (Q57242). He appears in two source graphs:

### 1. MusicBrainz (`https://linkedmusic.ca/graphs/musicbrainz/`)

**Entity:** `https://musicbrainz.org/artist/014d3c1a-57a4-49cb-bcf9-2c8a61c25c70`

| Property | Value |
|---|---|
| **Label** | August von Kotzebue |
| **Type** | Artist (Q5 = human) |
| **Birth date (P569)** | 1761-05-03 |
| **Death date (P570)** | 1819-03-23 |
| **Sex (P21)** | Q6581097 (male) |
| **Birth place (P19)** | Weimar (MusicBrainz area) |
| **Death place (P20)** | Mannheim (MusicBrainz area) |
| **Nationality (P27)** | Germany (MusicBrainz area) |
| **External links (P2888)** | Wikidata (Q57242), VIAF (14771963), GND (118565796), BnF, IMDb, IMSLP, Discogs, Open Library, WorldCat, SNAC, NLA |

### 2. RISM (`https://linkedmusic.ca/graphs/rism/`)

**Entity:** `https://rism.online/people/34844`

| Property | Value |
|---|---|
| **Label** | Kotzebue, August von (1761-1819) |
| **Type** | Person |
| **External link (P2888)** | Wikidata Q57242 |

Both records are linked to the same Wikidata entity (Q57242), confirming they refer to the same person — the German playwright and author August von Kotzebue (1761–1819).

The SPARQL has been executed:
```sparql
yes_linkedmusic_contains_information_related_to_august_von_kotzebue_q57242_he_appears_in_two_source_graphs_1_musicbrainz_httpslinkedmusiccagraphsmusicbrainz_entity_httpsmusicbrainzorgartist014d3c1a-57a4-49cb-bcf9-2c8a61c25c70_property_value_label_august_von_kotzebue_type_artist_q5_human_birth_date_p569_1761-05-03_death_date_p570_1819-03-23_sex_p21_q6581097_male_birth_place_p19_weimar_musicbrainz_area_death_place_p20_mannheim_musicbrainz_area_nationality_p27_germany_musicbrainz_area_external_links_p2888_wikidata_q57242_viaf_14771963_gnd_118565796_bnf_imdb_imslp_discogs_open_library_worldcat_snac_nla_2_rism_httpslinkedmusiccagraphsrism_entity_httpsrismonlinepeople34844_property_value_label_kotzebue_august_von_1761-1819_type_person_external_link_p2888_wikidata_q57242_both_records_are_linked_to_the_same_wikidata_entity_q57242_confirming_they_refer_to_the_same_person_the_german_playwright_and_author_august_von_kotzebue_17611819
```

### USER
How can I search for other historical figures or composers from the same era?

### ASSISTANT
**Selecting knowledge graph(s)**

### USER
Can you show me all records about him from these two sources (RISM and MusicBrainz)?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

Now I have a comprehensive picture. Let me compile the final answer.

---

## All Records about August von Kotzebue (Q57242) in LinkedMusic

Two entity records for August von Kotzebue exist across the RISM and MusicBrainz graphs, both linked to Wikidata Q57242 via `P2888`. Below are all details.

---

### 1. RISM Person Record

**URI:** <https://rism.online/people/34844>  
**Graph:** <https://linkedmusic.ca/graphs/rism/>

| Property | Value |
|----------|-------|
| rdf:type | `https://linkedmusic.ca/graphs/rism/Person` |
| rdfs:label | Kotzebue, August von (1761-1819) |
| P2888 (see also) | <http://www.wikidata.org/entity/Q57242> |

**410 RISM sources** link to this person via four relationships:

| Relationship | Wikidata Property | Count | Meaning |
|---|---|---|---|
| **P676** | lyrics written by | 399 | Sources where Kotzebue wrote the text/lyrics |
| **P87** | libretto by | 8 | Sources where Kotzebue wrote the libretto |
| **P655** | dedicatee | 2 | Sources dedicated to Kotzebue |
| **P86** | composer | 1 | Source where Kotzebue is listed as composer |

Sample sources by role:

**Lyrics written by (P676) — 399 sources**, including:
| Source | Label |
|---|---|
| https://rism.online/sources/1001057350 | Nettchen erscheint mit einer Guitarre auf dem Balkon und singt–E major; Manuscript copy; D-FLa XII Hs 1552 Bd. 5 |
| https://rism.online/sources/1001064639 | Es kann ja nicht immer so bleiben; Manuscript copy; D-Dl Mus.1-B-504 |
| https://rism.online/sources/1001086447 | Das Nachtgespenst–G major; Manuscript copy; D-Mbs Mus.ms. 3200 |
| https://rism.online/sources/1001094222 | Deodata (Excerpts, Arrangement); Manuscript copy; D-Bhm RH 0925 |
| https://rism.online/sources/1001205794 | Gesellschaftslied; Manuscript copy; D-Dl Mus.2-K-520 |
| https://rism.online/sources/1001208383 | Feodora; Manuscript copy; D-Dl Mus.4946-F-1 |
| https://rism.online/sources/1001228275 | Die Ruinen von Athen (Excerpts); Manuscript copy; D-Dl Mus.4193-F-527 |
| https://rism.online/sources/1001222079 | Er hofft laß ihn hoffen–F major (Arrangement); Manuscript copy; D-SPlb Mus Hs 25 |
| https://rism.online/sources/1001222085 | In des Irtisch weiße Fluten–D minor (Arrangement); Manuscript copy; D-SPlb Mus Hs 25 |
| https://rism.online/sources/452518974 | Das Dorf im Gebirge; Manuscript copy; GraW 1a.4; D-B Mus.ms. 22917/3 |

**Libretto by (P87) — 8 sources:**
| Source | Label |
|---|---|
| https://rism.online/sources/1001209730 | Fanchon das Leyermädchen (Excerpts, Arrangement); Print |
| https://rism.online/sources/1001149624 | Der Eremit auf Formentera; Print |
| https://rism.online/sources/1001209847 | Fanchon das Leyermädchen (Excerpts, Arrangement); Print |
| https://rism.online/sources/1001209852 | Fanchon das Leyermädchen (Excerpts, Arrangement); Print |
| https://rism.online/sources/410003383 | Graf Benjowski (Excerpts, Arrangement); Manuscript copy; CH-BEl SLA-Mus-JL MLHs 132/4/22 |
| https://rism.online/sources/407000033 | Fanchon das Leyermädchen–C major (Excerpts, Arrangement); Manuscript copy; CH-SGv VMs P 174 |
| https://rism.online/sources/410002835 | Fanchon das Leyermädchen (Excerpts, Arrangement); Manuscript copy; CH-BEl SLA-Mus-JL MLHs 132/8/14 |
| https://rism.online/sources/410003268 | Graf Benjowski (Excerpts, Arrangement); Manuscript copy; CH-BEl SLA-Mus-JL MLHs 132/3/3 |

**Dedicatee (P655) — 2 sources:**
| Source | Label |
|---|---|
| https://rism.online/sources/1001011441 | Der Gefangene; Manuscript copy; D-Mbs Mus.ms. 2967 |
| https://rism.online/sources/1001239123 | Fanchon das Leyermädchen (Excerpts); Manuscript copy; D-Mbs Mus.ms. 24856 |

**Composer (P86) — 1 source:**
| Source | Label |
|---|---|
| https://rism.online/sources/300041722 | König Stephan–C minor (Excerpts); Manuscript copy; LvBWV op.117, KinB 117; PL-Wn Mus.1192 |

---

### 2. MusicBrainz Artist Record

**URI:** <https://musicbrainz.org/artist/014d3c1a-57a4-49cb-bcf9-2c8a61c25c70>  
**Graph:** <https://linkedmusic.ca/graphs/musicbrainz/>

| Property | Value |
|----------|-------|
| rdf:type | `https://linkedmusic.ca/graphs/musicbrainz/Artist` |
| rdfs:label | August von Kotzebue |
| P31 (instance of) | Q5 (human) |
| P21 (sex or gender) | Q6581097 (male) |
| P569 (date of birth) | 1761-05-03 |
| P570 (date of death) | 1819-03-23 |
| P27 (country of citizenship) | <https://musicbrainz.org/area/85752fda-13c4-31a3-bee5-0e5cb1f51dad> |
| P19 (place of birth) | <https://musicbrainz.org/area/c7644e45-dec4-43fd-aad6-35036b8e911d> |
| P20 (place of death) | <https://musicbrainz.org/area/b07271ff-75a4-4dbd-96ee-6386cf3c5fab> |
| P2888 (see also) | <http://www.wikidata.org/entity/Q57242> (Wikidata) |
| P2888 (see also) | <http://viaf.org/viaf/14771963> (VIAF) |
| P2888 (see also) | <https://d-nb.info/gnd/118565796> (GND/DNB) |
| P2888 (see also) | <http://id.loc.gov/authorities/names/n50000570> (LC Names) |
| P2888 (see also) | <https://catalogue.bnf.fr/ark:/12148/cb11910016f> (BNF) |
| P2888 (see also) | <https://nla.gov.au/nla.party-895637> (NLA) |
| P2888 (see also) | <https://www.worldcat.org/identities/lccn-n50000570> (WorldCat) |
| P2888 (see also) | <https://openlibrary.org/works/OL4365621A> (Open Library) |
| P2888 (see also) | <https://imslp.org/wiki/Category:Kotzebue,_August_von> (IMSLP) |
| P2888 (see also) | <https://www.discogs.com/artist/2064923> (Discogs) |
| P2888 (see also) | <http://snaccooperative.org/ark:/99166/w6m047b9> (SNAC) |
| P2888 (see also) | <https://www.imdb.com/name/nm2539546/> (IMDb) |

**No recordings, releases, or other entities in MusicBrainz** currently link to this artist record via P175 (performer) or other relationships.

---

### Summary

| Graph | Record URI | Type | Key Facts |
|-------|-----------|------|-----------|
| **RISM** | <https://rism.online/people/34844> | Person | 410 linked sources: 399 as lyricist (P676), 8 as librettist (P87), 2 as dedicatee (P655), 1 as composer (P86) |
| **MusicBrainz** | <https://musicbrainz.org/artist/014d3c1a-57a4-49cb-bcf9-2c8a61c25c70> | Artist | Full biographical record with 12 external authority links; no linked recordings/releases |
</details>

**Validating and executing SPARQL query**


Now I have a comprehensive picture. Let me compile the final answer.

---

## All Records about August von Kotzebue (Q57242) in LinkedMusic

Two entity records for August von Kotzebue exist across the RISM and MusicBrainz graphs, both linked to Wikidata Q57242 via `P2888`. Below are all details.

---

### 1. RISM Person Record

**URI:** <https://rism.online/people/34844>  
**Graph:** <https://linkedmusic.ca/graphs/rism/>

| Property | Value |
|----------|-------|
| rdf:type | `https://linkedmusic.ca/graphs/rism/Person` |
| rdfs:label | Kotzebue, August von (1761-1819) |
| P2888 (see also) | <http://www.wikidata.org/entity/Q57242> |

**410 RISM sources** link to this person via four relationships:

| Relationship | Wikidata Property | Count | Meaning |
|---|---|---|---|
| **P676** | lyrics written by | 399 | Sources where Kotzebue wrote the text/lyrics |
| **P87** | libretto by | 8 | Sources where Kotzebue wrote the libretto |
| **P655** | dedicatee | 2 | Sources dedicated to Kotzebue |
| **P86** | composer | 1 | Source where Kotzebue is listed as composer |

Sample sources by role:

**Lyrics written by (P676) — 399 sources**, including:
| Source | Label |
|---|---|
| https://rism.online/sources/1001057350 | Nettchen erscheint mit einer Guitarre auf dem Balkon und singt–E major; Manuscript copy; D-FLa XII Hs 1552 Bd. 5 |
| https://rism.online/sources/1001064639 | Es kann ja nicht immer so bleiben; Manuscript copy; D-Dl Mus.1-B-504 |
| https://rism.online/sources/1001086447 | Das Nachtgespenst–G major; Manuscript copy; D-Mbs Mus.ms. 3200 |
| https://rism.online/sources/1001094222 | Deodata (Excerpts, Arrangement); Manuscript copy; D-Bhm RH 0925 |
| https://rism.online/sources/1001205794 | Gesellschaftslied; Manuscript copy; D-Dl Mus.2-K-520 |
| https://rism.online/sources/1001208383 | Feodora; Manuscript copy; D-Dl Mus.4946-F-1 |
| https://rism.online/sources/1001228275 | Die Ruinen von Athen (Excerpts); Manuscript copy; D-Dl Mus.4193-F-527 |
| https://rism.online/sources/1001222079 | Er hofft laß ihn hoffen–F major (Arrangement); Manuscript copy; D-SPlb Mus Hs 25 |
| https://rism.online/sources/1001222085 | In des Irtisch weiße Fluten–D minor (Arrangement); Manuscript copy; D-SPlb Mus Hs 25 |
| https://rism.online/sources/452518974 | Das Dorf im Gebirge; Manuscript copy; GraW 1a.4; D-B Mus.ms. 22917/3 |

**Libretto by (P87) — 8 sources:**
| Source | Label |
|---|---|
| https://rism.online/sources/1001209730 | Fanchon das Leyermädchen (Excerpts, Arrangement); Print |
| https://rism.online/sources/1001149624 | Der Eremit auf Formentera; Print |
| https://rism.online/sources/1001209847 | Fanchon das Leyermädchen (Excerpts, Arrangement); Print |
| https://rism.online/sources/1001209852 | Fanchon das Leyermädchen (Excerpts, Arrangement); Print |
| https://rism.online/sources/410003383 | Graf Benjowski (Excerpts, Arrangement); Manuscript copy; CH-BEl SLA-Mus-JL MLHs 132/4/22 |
| https://rism.online/sources/407000033 | Fanchon das Leyermädchen–C major (Excerpts, Arrangement); Manuscript copy; CH-SGv VMs P 174 |
| https://rism.online/sources/410002835 | Fanchon das Leyermädchen (Excerpts, Arrangement); Manuscript copy; CH-BEl SLA-Mus-JL MLHs 132/8/14 |
| https://rism.online/sources/410003268 | Graf Benjowski (Excerpts, Arrangement); Manuscript copy; CH-BEl SLA-Mus-JL MLHs 132/3/3 |

**Dedicatee (P655) — 2 sources:**
| Source | Label |
|---|---|
| https://rism.online/sources/1001011441 | Der Gefangene; Manuscript copy; D-Mbs Mus.ms. 2967 |
| https://rism.online/sources/1001239123 | Fanchon das Leyermädchen (Excerpts); Manuscript copy; D-Mbs Mus.ms. 24856 |

**Composer (P86) — 1 source:**
| Source | Label |
|---|---|
| https://rism.online/sources/300041722 | König Stephan–C minor (Excerpts); Manuscript copy; LvBWV op.117, KinB 117; PL-Wn Mus.1192 |

---

### 2. MusicBrainz Artist Record

**URI:** <https://musicbrainz.org/artist/014d3c1a-57a4-49cb-bcf9-2c8a61c25c70>  
**Graph:** <https://linkedmusic.ca/graphs/musicbrainz/>

| Property | Value |
|----------|-------|
| rdf:type | `https://linkedmusic.ca/graphs/musicbrainz/Artist` |
| rdfs:label | August von Kotzebue |
| P31 (instance of) | Q5 (human) |
| P21 (sex or gender) | Q6581097 (male) |
| P569 (date of birth) | 1761-05-03 |
| P570 (date of death) | 1819-03-23 |
| P27 (country of citizenship) | <https://musicbrainz.org/area/85752fda-13c4-31a3-bee5-0e5cb1f51dad> |
| P19 (place of birth) | <https://musicbrainz.org/area/c7644e45-dec4-43fd-aad6-35036b8e911d> |
| P20 (place of death) | <https://musicbrainz.org/area/b07271ff-75a4-4dbd-96ee-6386cf3c5fab> |
| P2888 (see also) | <http://www.wikidata.org/entity/Q57242> (Wikidata) |
| P2888 (see also) | <http://viaf.org/viaf/14771963> (VIAF) |
| P2888 (see also) | <https://d-nb.info/gnd/118565796> (GND/DNB) |
| P2888 (see also) | <http://id.loc.gov/authorities/names/n50000570> (LC Names) |
| P2888 (see also) | <https://catalogue.bnf.fr/ark:/12148/cb11910016f> (BNF) |
| P2888 (see also) | <https://nla.gov.au/nla.party-895637> (NLA) |
| P2888 (see also) | <https://www.worldcat.org/identities/lccn-n50000570> (WorldCat) |
| P2888 (see also) | <https://openlibrary.org/works/OL4365621A> (Open Library) |
| P2888 (see also) | <https://imslp.org/wiki/Category:Kotzebue,_August_von> (IMSLP) |
| P2888 (see also) | <https://www.discogs.com/artist/2064923> (Discogs) |
| P2888 (see also) | <http://snaccooperative.org/ark:/99166/w6m047b9> (SNAC) |
| P2888 (see also) | <https://www.imdb.com/name/nm2539546/> (IMDb) |

**No recordings, releases, or other entities in MusicBrainz** currently link to this artist record via P175 (performer) or other relationships.

---

### Summary

| Graph | Record URI | Type | Key Facts |
|-------|-----------|------|----------|
| **RISM** | <https://rism.online/people/34844> | Person | 410 linked sources: 399 as lyricist (P676), 8 as librettist (P87), 2 as dedicatee (P655), 1 as composer (P86) |
| **MusicBrainz** | <https://musicbrainz.org/artist/014d3c1a-57a4-49cb-bcf9-2c8a61c25c70> | Artist | Full biographical record with 12 external authority links; no linked recordings/releases |

### USER
Who are the composers who set Kotzebue's texts to music in those 399 RISM sources?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**

### USER
Who are the composers who set Kotzebue's texts to music in those 399 RISM sources?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

There are **85 distinct composers** who set Kotzebue's texts to music in the RISM sources. Here is the complete list:

---

## Composers Who Set Kotzebue's Texts to Music (RISM)

**Kotzebue** (RISM person https://rism.online/people/34844) is linked to sources as lyricist (P655), librettist (P87), and lyrics author (P676). On those same sources, **85 distinct composers** are credited via P86 (composer):

| # | Composer | RISM Person URI |
|---|----------|-----------------|
| 1 | Angely, Louis (1788c-1835) | https://rism.online/people/30006780 |
| 2 | Anonymus | https://rism.online/people/30004985 |
| 3 | Beethoven, Ludwig van (1770-1827) | https://rism.online/people/11035 |
| 4 | Bergt, Christian Gottlob August (1771-1837) | https://rism.online/people/13615 |
| 5 | Blumenthal, Casimir von (1787-1849) | https://rism.online/people/30000388 |
| 6 | Boieldieu, Adrien (1775-1834) | https://rism.online/people/23607 |
| 7 | Bornhardt, Johann Heinrich Carl (1774-1843) | https://rism.online/people/30000435 |
| 8 | Danzi, Franz (1763-1826) | https://rism.online/people/2671 |
| 9 | Della Maria, Pierre-Antoine-Dominique (1769-1800) | https://rism.online/people/30000815 |
| 10 | Destouches, Franz Seraph von (1772-1844) | https://rism.online/people/8701 |
| 11 | Dieter, Christian Ludwig (1757-1822) | https://rism.online/people/11252 |
| 12 | Dittersdorf, Carl Ditters von (1739-1799) | https://rism.online/people/14522 |
| 13 | Eberwein, Carl (1786-1868) | https://rism.online/people/33572 |
| 14 | Ehlers, Wilhelm (1774-1845) | https://rism.online/people/38341 |
| 15 | Ett, Caspar (1788-1847) | https://rism.online/people/59061 |
| 16 | Feldmayr, Georg (1756-1834) | https://rism.online/people/30001035 |
| 17 | Fischer, Heinrich Wilhelm (18/19) | https://rism.online/people/30005751 |
| 18 | Gabler, Christoph August (1767-1839) | https://rism.online/people/32961 |
| 19 | Gantzert, Berthold (1801-1874) | https://rism.online/people/41559 |
| 20 | Geissler, Heinrich (18/19) | https://rism.online/people/30015375 |
| 21 | Gerl, Franz Xaver (1764-1827) | https://rism.online/people/30015376 |
| 22 | Geyer, Eduard (19.sc) | https://rism.online/people/41012783 |
| 23 | Gollmick, Carl Friedrich (1774-1852) | https://rism.online/people/3060031 |
| 24 | Graun, Carl Heinrich (1704-1759) | https://rism.online/people/30001351 |
| 25 | Guhr, Karl Wilhelm Ferdinand (1787-1848) | https://rism.online/people/92755 |
| 26 | Gyrowetz, Adalbert (1763-1850) | https://rism.online/people/94547 |
| 27 | Gürrlich, Joseph Augustin (1761-1817) | https://rism.online/people/329683 |
| 28 | Hacker, Benedikt (1769-1829) | https://rism.online/people/35788 |
| 29 | Haering, Joseph | https://rism.online/people/30001420 |
| 30 | Himmel, Friedrich Heinrich (1765-1814) | https://rism.online/people/90050 |
| 31 | Huber, Ferdinand Fürchtegott (1791-1863) | https://rism.online/people/30019145 |
| 32 | Knapp, Friedrich Jonathan (1784-1817) | https://rism.online/people/30100159 |
| 33 | Kocher, Konrad (1786-1872) | https://rism.online/people/27619 |
| 34 | Kranz, Johann Friedrich (1752-1810) | https://rism.online/people/38468 |
| 35 | Kreutzer, Conradin (1780-1849) | https://rism.online/people/53829 |
| 36 | Kreutzer, Rodolphe (1766-1831) | https://rism.online/people/53845 |
| 37 | Krufft, Nikolaus von (1779-1818) | https://rism.online/people/57125 |
| 38 | Kuhlau, Friedrich (1786-1832) | https://rism.online/people/60618 |
| 39 | Kunzen, Friedrich Ludwig Aemilius (1761-1817) | https://rism.online/people/61940 |
| 40 | Langer, Ferdinand (1839-1905) | https://rism.online/people/72574 |
| 41 | Lauer von Münchofen, Adolf (1795-1874) | https://rism.online/people/76010 |
| 42 | Lindpaintner, Peter Josef von (1791-1856) | https://rism.online/people/103799 |
| 43 | Lortzing, Albert (1801-1851) | https://rism.online/people/122656 |
| 44 | Marinelli, Franz (1792-1849) | https://rism.online/people/78738 |
| 45 | Marschner, Heinrich August (1795-1861) | https://rism.online/people/79853 |
| 46 | Mayer, Emilie (1812-1883) | https://rism.online/people/30000776 |
| 47 | Mosel, Ignaz Franz von (1772-1844) | https://rism.online/people/94341 |
| 48 | Möller, Max (1887-1985) | https://rism.online/people/51016128 |
| 49 | Müller, Donat (1804-1879) | https://rism.online/people/158590 |
| 50 | Nisle, Johann Martin Friedrich (1780-1873c) | https://rism.online/people/30075311 |
| 51 | Reichardt, Johann Friedrich (1752-1814) | https://rism.online/people/40133 |
| 52 | Reinicke, Leopold (1774-1820) | https://rism.online/people/43172 |
| 53 | Ritter, Peter (1763-1846) | https://rism.online/people/57840 |
| 54 | Rösler, Johann Joseph (1771-1813) | https://rism.online/people/30012758 |
| 55 | Schacht, Theodor von (1748-1823) | https://rism.online/people/30002852 |
| 56 | Schermer, Anton (1759-1821) | https://rism.online/people/30004890 |
| 57 | Schermer, Lorenz (1762-1838) | https://rism.online/people/30004891 |
| 58 | Schermer, Willibald (1773-1806) | https://rism.online/people/30093146 |
| 59 | Schinn, Johann Georg (1768-1833) | https://rism.online/people/128242 |
| 60 | Schmidt, Johann Philipp Samuel (1779-1853) | https://rism.online/people/152004 |
| 61 | Schubert, Franz (1797-1828) | https://rism.online/people/111603 |
| 62 | Schubert, Louis (1828-1884) | https://rism.online/people/111727 |
| 63 | Schuster, Joseph (1748-1812) | https://rism.online/people/133066 |
| 64 | Schäffer, August (1814-1879) | https://rism.online/people/110743 |
| 65 | Seyfried, Ignaz Ritter von (1776-1841) | https://rism.online/people/146950 |
| 66 | Sixt, Johann Abraham (1757-1797) | https://rism.online/people/30004471 |
| 67 | Spindler, Stanislaus Franz Xaver (1763-1819) | https://rism.online/people/30004079 |
| 68 | Spohr, Louis (1784-1859) | https://rism.online/people/149499 |
| 69 | Stegmann, Carl David (1751-1826) | https://rism.online/people/123796 |
| 70 | Steibelt, Daniel (1765-1823) | https://rism.online/people/331204 |
| 71 | Süßmayr, Franz Xaver (1766-1803) | https://rism.online/people/30003087 |
| 72 | Theuss, Carl Theodor (1785-1847) | https://rism.online/people/30025545 |
| 73 | Uber, Alexander (1783-1824) | https://rism.online/people/30007401 |
| 74 | Veltheim, Baron von (19.sc) | https://rism.online/people/30025444 |
| 75 | Vogler, Georg Joseph (1749-1814) | https://rism.online/people/147606 |
| 76 | Walter, Ignaz (1755-1822) | https://rism.online/people/30003290 |
| 77 | Weber, Bernhard Anselm (1764-1821) | https://rism.online/people/116512 |
| 78 | Weber, Carl Maria von (1786-1826) | https://rism.online/people/117485 |
| 79 | Weigl, Joseph (1766-1846) | https://rism.online/people/125775 |
| 80 | Weigl, Joseph Franz (1740-1820) | https://rism.online/people/30004846 |
| 81 | Weitenkampf, F. G. (18/19) | https://rism.online/people/30010796 |
| 82 | Wineberger, Paul (1758-1821) | https://rism.online/people/30003360 |
| 83 | Winter, Peter von (1754-1825) | https://rism.online/people/141907 |
| 84 | Wranitzky, Paul (1756-1808) | https://rism.online/people/143618 |
| 85 | Zumsteeg, Johann Rudolf (1760-1802) | https://rism.online/people/103020 |

---

**SPARQL query used:**

```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX wd: <http://www.wikidata.org/prop/direct/>

SELECT DISTINCT ?composer ?composerLabel WHERE {
  GRAPH <https://linkedmusic.ca/graphs/rism/> {
    ?source ?p <https://rism.online/people/34844> .
    FILTER(?p IN (wd:P655, wd:P87, wd:P676))
    ?source wd:P86 ?composer .
    ?composer rdfs:label ?composerLabel .
  }
} ORDER BY ?composerLabel
```

**Method:** The query finds RISM sources where Kotzebue (person 34844) is linked via P655 (lyricist), P87 (librettist), or P676 (lyrics written by), then retrieves the P86 (composer) on those same sources. The total count of **85 distinct composers** was confirmed by a separate `COUNT(DISTINCT ?composer)` query.

Notable composers include **Beethoven**, **Schubert**, **Spohr**, **Weber**, **Kreutzer**, **Kuhlau**, **Reichardt**, and **Zumsteeg** — all prominent figures of the late 18th and early 19th centuries, reflecting Kotzebue's enormous influence as a playwright and librettist of his era.
</details>

**Validating and executing SPARQL query**


There are **85 distinct composers** who set Kotzebue's texts to music in the RISM sources. Here is the complete list:

---

## Composers Who Set Kotzebue's Texts to Music (RISM)

**Kotzebue** (RISM person https://rism.online/people/34844) is linked to sources as lyricist (P655), librettist (P87), and lyrics author (P676). On those same sources, **85 distinct composers** are credited via P86 (composer):

| # | Composer | RISM Person URI |
|---|----------|-----------------|
| 1 | Angely, Louis (1788c-1835) | https://rism.online/people/30006780 |
| 2 | Anonymus | https://rism.online/people/30004985 |
| 3 | Beethoven, Ludwig van (1770-1827) | https://rism.online/people/11035 |
| 4 | Bergt, Christian Gottlob August (1771-1837) | https://rism.online/people/13615 |
| 5 | Blumenthal, Casimir von (1787-1849) | https://rism.online/people/30000388 |
| 6 | Boieldieu, Adrien (1775-1834) | https://rism.online/people/23607 |
| 7 | Bornhardt, Johann Heinrich Carl (1774-1843) | https://rism.online/people/30000435 |
| 8 | Danzi, Franz (1763-1826) | https://rism.online/people/2671 |
| 9 | Della Maria, Pierre-Antoine-Dominique (1769-1800) | https://rism.online/people/30000815 |
| 10 | Destouches, Franz Seraph von (1772-1844) | https://rism.online/people/8701 |
| 11 | Dieter, Christian Ludwig (1757-1822) | https://rism.online/people/11252 |
| 12 | Dittersdorf, Carl Ditters von (1739-1799) | https://rism.online/people/14522 |
| 13 | Eberwein, Carl (1786-1868) | https://rism.online/people/33572 |
| 14 | Ehlers, Wilhelm (1774-1845) | https://rism.online/people/38341 |
| 15 | Ett, Caspar (1788-1847) | https://rism.online/people/59061 |
| 16 | Feldmayr, Georg (1756-1834) | https://rism.online/people/30001035 |
| 17 | Fischer, Heinrich Wilhelm (18/19) | https://rism.online/people/30005751 |
| 18 | Gabler, Christoph August (1767-1839) | https://rism.online/people/32961 |
| 19 | Gantzert, Berthold (1801-1874) | https://rism.online/people/41559 |
| 20 | Geissler, Heinrich (18/19) | https://rism.online/people/30015375 |
| 21 | Gerl, Franz Xaver (1764-1827) | https://rism.online/people/30015376 |
| 22 | Geyer, Eduard (19.sc) | https://rism.online/people/41012783 |
| 23 | Gollmick, Carl Friedrich (1774-1852) | https://rism.online/people/3060031 |
| 24 | Graun, Carl Heinrich (1704-1759) | https://rism.online/people/30001351 |
| 25 | Guhr, Karl Wilhelm Ferdinand (1787-1848) | https://rism.online/people/92755 |
| 26 | Gyrowetz, Adalbert (1763-1850) | https://rism.online/people/94547 |
| 27 | Gürrlich, Joseph Augustin (1761-1817) | https://rism.online/people/329683 |
| 28 | Hacker, Benedikt (1769-1829) | https://rism.online/people/35788 |
| 29 | Haering, Joseph | https://rism.online/people/30001420 |
| 30 | Himmel, Friedrich Heinrich (1765-1814) | https://rism.online/people/90050 |
| 31 | Huber, Ferdinand Fürchtegott (1791-1863) | https://rism.online/people/30019145 |
| 32 | Knapp, Friedrich Jonathan (1784-1817) | https://rism.online/people/30100159 |
| 33 | Kocher, Konrad (1786-1872) | https://rism.online/people/27619 |
| 34 | Kranz, Johann Friedrich (1752-1810) | https://rism.online/people/38468 |
| 35 | Kreutzer, Conradin (1780-1849) | https://rism.online/people/53829 |
| 36 | Kreutzer, Rodolphe (1766-1831) | https://rism.online/people/53845 |
| 37 | Krufft, Nikolaus von (1779-1818) | https://rism.online/people/57125 |
| 38 | Kuhlau, Friedrich (1786-1832) | https://rism.online/people/60618 |
| 39 | Kunzen, Friedrich Ludwig Aemilius (1761-1817) | https://rism.online/people/61940 |
| 40 | Langer, Ferdinand (1839-1905) | https://rism.online/people/72574 |
| 41 | Lauer von Münchofen, Adolf (1795-1874) | https://rism.online/people/76010 |
| 42 | Lindpaintner, Peter Josef von (1791-1856) | https://rism.online/people/103799 |
| 43 | Lortzing, Albert (1801-1851) | https://rism.online/people/122656 |
| 44 | Marinelli, Franz (1792-1849) | https://rism.online/people/78738 |
| 45 | Marschner, Heinrich August (1795-1861) | https://rism.online/people/79853 |
| 46 | Mayer, Emilie (1812-1883) | https://rism.online/people/30000776 |
| 47 | Mosel, Ignaz Franz von (1772-1844) | https://rism.online/people/94341 |
| 48 | Möller, Max (1887-1985) | https://rism.online/people/51016128 |
| 49 | Müller, Donat (1804-1879) | https://rism.online/people/158590 |
| 50 | Nisle, Johann Martin Friedrich (1780-1873c) | https://rism.online/people/30075311 |
| 51 | Reichardt, Johann Friedrich (1752-1814) | https://rism.online/people/40133 |
| 52 | Reinicke, Leopold (1774-1820) | https://rism.online/people/43172 |
| 53 | Ritter, Peter (1763-1846) | https://rism.online/people/57840 |
| 54 | Rösler, Johann Joseph (1771-1813) | https://rism.online/people/30012758 |
| 55 | Schacht, Theodor von (1748-1823) | https://rism.online/people/30002852 |
| 56 | Schermer, Anton (1759-1821) | https://rism.online/people/30004890 |
| 57 | Schermer, Lorenz (1762-1838) | https://rism.online/people/30004891 |
| 58 | Schermer, Willibald (1773-1806) | https://rism.online/people/30093146 |
| 59 | Schinn, Johann Georg (1768-1833) | https://rism.online/people/128242 |
| 60 | Schmidt, Johann Philipp Samuel (1779-1853) | https://rism.online/people/152004 |
| 61 | Schubert, Franz (1797-1828) | https://rism.online/people/111603 |
| 62 | Schubert, Louis (1828-1884) | https://rism.online/people/111727 |
| 63 | Schuster, Joseph (1748-1812) | https://rism.online/people/133066 |
| 64 | Schäffer, August (1814-1879) | https://rism.online/people/110743 |
| 65 | Seyfried, Ignaz Ritter von (1776-1841) | https://rism.online/people/146950 |
| 66 | Sixt, Johann Abraham (1757-1797) | https://rism.online/people/30004471 |
| 67 | Spindler, Stanislaus Franz Xaver (1763-1819) | https://rism.online/people/30004079 |
| 68 | Spohr, Louis (1784-1859) | https://rism.online/people/149499 |
| 69 | Stegmann, Carl David (1751-1826) | https://rism.online/people/123796 |
| 70 | Steibelt, Daniel (1765-1823) | https://rism.online/people/331204 |
| 71 | Süßmayr, Franz Xaver (1766-1803) | https://rism.online/people/30003087 |
| 72 | Theuss, Carl Theodor (1785-1847) | https://rism.online/people/30025545 |
| 73 | Uber, Alexander (1783-1824) | https://rism.online/people/30007401 |
| 74 | Veltheim, Baron von (19.sc) | https://rism.online/people/30025444 |
| 75 | Vogler, Georg Joseph (1749-1814) | https://rism.online/people/147606 |
| 76 | Walter, Ignaz (1755-1822) | https://rism.online/people/30003290 |
| 77 | Weber, Bernhard Anselm (1764-1821) | https://rism.online/people/116512 |
| 78 | Weber, Carl Maria von (1786-1826) | https://rism.online/people/117485 |
| 79 | Weigl, Joseph (1766-1846) | https://rism.online/people/125775 |
| 80 | Weigl, Joseph Franz (1740-1820) | https://rism.online/people/30004846 |
| 81 | Weitenkampf, F. G. (18/19) | https://rism.online/people/30010796 |
| 82 | Wineberger, Paul (1758-1821) | https://rism.online/people/30003360 |
| 83 | Winter, Peter von (1754-1825) | https://rism.online/people/141907 |
| 84 | Wranitzky, Paul (1756-1808) | https://rism.online/people/143618 |
| 85 | Zumsteeg, Johann Rudolf (1760-1802) | https://rism.online/people/103020 |

---

**SPARQL query used:**

**Method:** The query finds RISM sources where Kotzebue (person 34844) is linked via P655 (lyricist), P87 (librettist), or P676 (lyrics written by), then retrieves the P86 (composer) on those same sources. The total count of **85 distinct composers** was confirmed by a separate `COUNT(DISTINCT ?composer)` query.

Notable composers include **Beethoven**, **Schubert**, **Spohr**, **Weber**, **Kreutzer**, **Kuhlau**, **Reichardt**, and **Zumsteeg** — all prominent figures of the late 18th and early 19th centuries, reflecting Kotzebue's enormous influence as a playwright and librettist of his era.

The SPARQL has been executed:
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
PREFIX wd: <http://www.wikidata.org/prop/direct/> 
SELECT DISTINCT ?composer ?composerLabel 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/rism/> {
  ?source ?p <https://rism.online/people/34844> .
   
FILTER(?p IN (wd:P655, wd:P87, wd:P676)) ?source wd:P86 ?composer .
   ?composer rdfs:label ?composerLabel .
  
}
} 
ORDER BY ?composerLabel
```

### USER
can you do a group by in this query and give me the list of composers by number of works for which von Kotzebue has written the text?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

Here are the **85 composers** ranked by the number of RISM sources they set Kotzebue's texts to music for, ordered by count descending:

| Rank | Composer | Source Count |
|------|----------|-------------|
| 1 | Himmel, Friedrich Heinrich (1765-1814) | 139 |
| 2 | Weber, Bernhard Anselm (1764-1821) | 27 |
| 3 | Weber, Carl Maria von (1786-1826) | 22 |
| 4 | Anonymus | 21 |
| 5 | Beethoven, Ludwig van (1770-1827) | 20 |
| 6 | Weigl, Joseph (1766-1846) | 14 |
| 7 | Ritter, Peter (1763-1846) | 13 |
| 8 | Kreutzer, Conradin (1780-1849) | 10 |
| 9 | Kuhlau, Friedrich (1786-1832) | 9 |
| 10 | Lindpaintner, Peter Josef von (1791-1856) | 6 |
| 11 | Schmidt, Johann Philipp Samuel (1779-1853) | 5 |
| 12 | Süßmayr, Franz Xaver (1766-1803) | 5 |
| 13 | Bornhardt, Johann Heinrich Carl (1774-1843) | 4 |
| 14 | Reichardt, Johann Friedrich (1752-1814) | 4 |
| 15 | Marschner, Heinrich August (1795-1861) | 4 |
| 16 | Schermer, Willibald (1773-1806) | 4 |
| 17 | Zumsteeg, Johann Rudolf (1760-1802) | 3 |
| 18 | Dieter, Christian Ludwig (1757-1822) | 3 |
| 19 | Lortzing, Albert (1801-1851) | 3 |
| 20 | Wranitzky, Paul (1756-1808) | 3 |
| 21 | Seyfried, Ignaz Ritter von (1776-1841) | 3 |
| 22 | Vogler, Georg Joseph (1749-1814) | 3 |
| 23 | Walter, Ignaz (1755-1822) | 3 |
| 24 | Eberwein, Carl (1786-1868) | 3 |
| 25 | Schinn, Johann Georg (1768-1833) | 2 |
| 26 | Spohr, Louis (1784-1859) | 2 |
| 27 | Steibelt, Daniel (1765-1823) | 2 |
| 28 | Reinicke, Leopold (1774-1820) | 2 |
| 29 | Gyrowetz, Adalbert (1763-1850) | 2 |
| 30 | Weitenkampf, F. G. (18/19) | 2 |
| 31 | Fischer, Heinrich Wilhelm (18/19) | 2 |
| 32 | Rösler, Johann Joseph (1771-1813) | 2 |
| 33 | Knapp, Friedrich Jonathan (1784-1817) | 2 |
| 34 | Gollmick, Carl Friedrich (1774-1852) | 2 |
| 35 | Spindler, Stanislaus Franz Xaver (1763-1819) | 2 |
| 36 | Stegmann, Carl David (1751-1826) | 2 |
| 37 | Bergt, Christian Gottlob August (1771-1837) | 2 |
| 38 | Marinelli, Franz (1792-1849) | 2 |
| 39 | Schäffer, August (1814-1879) | 1 |
| 40 | Schubert, Franz (1797-1828) | 1 |
| 41 | Schuster, Joseph (1748-1812) | 1 |
| 42 | Winter, Peter von (1754-1825) | 1 |
| 43 | Dittersdorf, Carl Ditters von (1739-1799) | 1 |
| 44 | Müller, Donat (1804-1879) | 1 |
| 45 | Boieldieu, Adrien (1775-1834) | 1 |
| 46 | Danzi, Franz (1763-1826) | 1 |
| 47 | Della Maria, Pierre-Antoine-Dominique (1769-1800) | 1 |
| 48 | Feldmayr, Georg (1756-1834) | 1 |
| 49 | Graun, Carl Heinrich (1704-1759) | 1 |
| 50 | Sixt, Johann Abraham (1757-1797) | 1 |
| 51 | Huber, Ferdinand Fürchtegott (1791-1863) | 1 |
| 52 | Nisle, Johann Martin Friedrich (1780-1873c) | 1 |
| 53 | Gürrlich, Joseph Augustin (1761-1817) | 1 |
| 54 | Hacker, Benedikt (1769-1829) | 1 |
| 55 | Ehlers, Wilhelm (1774-1845) | 1 |
| 56 | Kreutzer, Rodolphe (1766-1831) | 1 |
| 57 | Krufft, Nikolaus von (1779-1818) | 1 |
| 58 | Ett, Caspar (1788-1847) | 1 |
| 59 | Schacht, Theodor von (1748-1823) | 1 |
| 60 | Schermer, Anton (1759-1821) | 1 |
| 61 | Guhr, Karl Wilhelm Ferdinand (1787-1848) | 1 |
| 62 | Gantzert, Berthold (1801-1874) | 1 |
| 63 | Angely, Louis (1788c-1835) | 1 |
| 64 | Gabler, Christoph August (1767-1839) | 1 |
| 65 | Kunzen, Friedrich Ludwig Aemilius (1761-1817) | 1 |
| 66 | Lauer von Münchofen, Adolf (1795-1874) | 1 |
| 67 | Möller, Max (1887-1985) | 1 |
| 68 | Blumenthal, Casimir von (1787-1849) | 1 |
| 69 | Haering, Joseph | 1 |
| 70 | Weigl, Joseph Franz (1740-1820) | 1 |
| 71 | Mayer, Emilie (1812-1883) | 1 |
| 72 | Veltheim, Baron von (19.sc) | 1 |
| 73 | Geissler, Heinrich (18/19) | 1 |
| 74 | Kocher, Konrad (1786-1872) | 1 |
| 75 | Wineberger, Paul (1758-1821) | 1 |
| 76 | Uber, Alexander (1783-1824) | 1 |
| 77 | Theuss, Carl Theodor (1785-1847) | 1 |
| 78 | Geyer, Eduard (19.sc) | 1 |
| 79 | Schermer, Lorenz (1762-1838) | 1 |
| 80 | Schubert, Louis (1828-1884) | 1 |
| 81 | Gerl, Franz Xaver (1764-1827) | 1 |
| 82 | Kranz, Johann Friedrich (1752-1810) | 1 |
| 83 | Langer, Ferdinand (1839-1905) | 1 |
| 84 | Mosel, Ignaz Franz von (1772-1844) | 1 |
| 85 | Destouches, Franz Seraph von (1772-1844) | 1 |

**SPARQL query used:**

```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX wd: <http://www.wikidata.org/prop/direct/>

SELECT ?composer ?composerLabel (COUNT(DISTINCT ?source) AS ?sourceCount)
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/rism/> {
    ?source ?p <https://rism.online/people/34844> .
    FILTER(?p IN (wd:P655, wd:P87, wd:P676))
    ?source wd:P86 ?composer .
    ?composer rdfs:label ?composerLabel .
  }
}
GROUP BY ?composer ?composerLabel
ORDER BY DESC(?sourceCount)
```

**Key takeaway:** Friedrich Heinrich Himmel dominates with **139 sources** — more than the next 6 composers combined. Beethoven ranks 5th with 20 sources. The distribution is heavily long-tailed: the top 5 composers account for the majority of sources, while 47 composers (55%) are credited with only a single source each.
</details>

**Validating and executing SPARQL query**


Here are the **85 composers** ranked by the number of RISM sources they set Kotzebue's texts to music for, ordered by count descending:

| Rank | Composer | Source Count |
|------|----------|-------------|
| 1 | Himmel, Friedrich Heinrich (1765-1814) | 139 |
| 2 | Weber, Bernhard Anselm (1764-1821) | 27 |
| 3 | Weber, Carl Maria von (1786-1826) | 22 |
| 4 | Anonymus | 21 |
| 5 | Beethoven, Ludwig van (1770-1827) | 20 |
| 6 | Weigl, Joseph (1766-1846) | 14 |
| 7 | Ritter, Peter (1763-1846) | 13 |
| 8 | Kreutzer, Conradin (1780-1849) | 10 |
| 9 | Kuhlau, Friedrich (1786-1832) | 9 |
| 10 | Lindpaintner, Peter Josef von (1791-1856) | 6 |
| 11 | Schmidt, Johann Philipp Samuel (1779-1853) | 5 |
| 12 | Süßmayr, Franz Xaver (1766-1803) | 5 |
| 13 | Bornhardt, Johann Heinrich Carl (1774-1843) | 4 |
| 14 | Reichardt, Johann Friedrich (1752-1814) | 4 |
| 15 | Marschner, Heinrich August (1795-1861) | 4 |
| 16 | Schermer, Willibald (1773-1806) | 4 |
| 17 | Zumsteeg, Johann Rudolf (1760-1802) | 3 |
| 18 | Dieter, Christian Ludwig (1757-1822) | 3 |
| 19 | Lortzing, Albert (1801-1851) | 3 |
| 20 | Wranitzky, Paul (1756-1808) | 3 |
| 21 | Seyfried, Ignaz Ritter von (1776-1841) | 3 |
| 22 | Vogler, Georg Joseph (1749-1814) | 3 |
| 23 | Walter, Ignaz (1755-1822) | 3 |
| 24 | Eberwein, Carl (1786-1868) | 3 |
| 25 | Schinn, Johann Georg (1768-1833) | 2 |
| 26 | Spohr, Louis (1784-1859) | 2 |
| 27 | Steibelt, Daniel (1765-1823) | 2 |
| 28 | Reinicke, Leopold (1774-1820) | 2 |
| 29 | Gyrowetz, Adalbert (1763-1850) | 2 |
| 30 | Weitenkampf, F. G. (18/19) | 2 |
| 31 | Fischer, Heinrich Wilhelm (18/19) | 2 |
| 32 | Rösler, Johann Joseph (1771-1813) | 2 |
| 33 | Knapp, Friedrich Jonathan (1784-1817) | 2 |
| 34 | Gollmick, Carl Friedrich (1774-1852) | 2 |
| 35 | Spindler, Stanislaus Franz Xaver (1763-1819) | 2 |
| 36 | Stegmann, Carl David (1751-1826) | 2 |
| 37 | Bergt, Christian Gottlob August (1771-1837) | 2 |
| 38 | Marinelli, Franz (1792-1849) | 2 |
| 39 | Schäffer, August (1814-1879) | 1 |
| 40 | Schubert, Franz (1797-1828) | 1 |
| 41 | Schuster, Joseph (1748-1812) | 1 |
| 42 | Winter, Peter von (1754-1825) | 1 |
| 43 | Dittersdorf, Carl Ditters von (1739-1799) | 1 |
| 44 | Müller, Donat (1804-1879) | 1 |
| 45 | Boieldieu, Adrien (1775-1834) | 1 |
| 46 | Danzi, Franz (1763-1826) | 1 |
| 47 | Della Maria, Pierre-Antoine-Dominique (1769-1800) | 1 |
| 48 | Feldmayr, Georg (1756-1834) | 1 |
| 49 | Graun, Carl Heinrich (1704-1759) | 1 |
| 50 | Sixt, Johann Abraham (1757-1797) | 1 |
| 51 | Huber, Ferdinand Fürchtegott (1791-1863) | 1 |
| 52 | Nisle, Johann Martin Friedrich (1780-1873c) | 1 |
| 53 | Gürrlich, Joseph Augustin (1761-1817) | 1 |
| 54 | Hacker, Benedikt (1769-1829) | 1 |
| 55 | Ehlers, Wilhelm (1774-1845) | 1 |
| 56 | Kreutzer, Rodolphe (1766-1831) | 1 |
| 57 | Krufft, Nikolaus von (1779-1818) | 1 |
| 58 | Ett, Caspar (1788-1847) | 1 |
| 59 | Schacht, Theodor von (1748-1823) | 1 |
| 60 | Schermer, Anton (1759-1821) | 1 |
| 61 | Guhr, Karl Wilhelm Ferdinand (1787-1848) | 1 |
| 62 | Gantzert, Berthold (1801-1874) | 1 |
| 63 | Angely, Louis (1788c-1835) | 1 |
| 64 | Gabler, Christoph August (1767-1839) | 1 |
| 65 | Kunzen, Friedrich Ludwig Aemilius (1761-1817) | 1 |
| 66 | Lauer von Münchofen, Adolf (1795-1874) | 1 |
| 67 | Möller, Max (1887-1985) | 1 |
| 68 | Blumenthal, Casimir von (1787-1849) | 1 |
| 69 | Haering, Joseph | 1 |
| 70 | Weigl, Joseph Franz (1740-1820) | 1 |
| 71 | Mayer, Emilie (1812-1883) | 1 |
| 72 | Veltheim, Baron von (19.sc) | 1 |
| 73 | Geissler, Heinrich (18/19) | 1 |
| 74 | Kocher, Konrad (1786-1872) | 1 |
| 75 | Wineberger, Paul (1758-1821) | 1 |
| 76 | Uber, Alexander (1783-1824) | 1 |
| 77 | Theuss, Carl Theodor (1785-1847) | 1 |
| 78 | Geyer, Eduard (19.sc) | 1 |
| 79 | Schermer, Lorenz (1762-1838) | 1 |
| 80 | Schubert, Louis (1828-1884) | 1 |
| 81 | Gerl, Franz Xaver (1764-1827) | 1 |
| 82 | Kranz, Johann Friedrich (1752-1810) | 1 |
| 83 | Langer, Ferdinand (1839-1905) | 1 |
| 84 | Mosel, Ignaz Franz von (1772-1844) | 1 |
| 85 | Destouches, Franz Seraph von (1772-1844) | 1 |

**Key takeaway:** Friedrich Heinrich Himmel dominates with **139 sources** — more than the next 6 composers combined. Beethoven ranks 5th with 20 sources. The distribution is heavily long-tailed: the top 5 composers account for the majority of sources, while 47 composers (55%) are credited with only a single source each.

The SPARQL has been executed:
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
PREFIX wd: <http://www.wikidata.org/prop/direct/> 
SELECT ?composer ?composerLabel (COUNT(DISTINCT ?source) AS ?sourceCount) 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/rism/> {
  ?source ?p <https://rism.online/people/34844> .
   
FILTER(?p IN (wd:P655, wd:P87, wd:P676)) ?source wd:P86 ?composer .
   ?composer rdfs:label ?composerLabel .
  
}
} 
GROUP BY ?composer ?composerLabel 
ORDER BY DESC(?sourceCount)
```

### USER
can you generate a bar plot for the top-10 of composers by number of works for which von Kotzebue has written the text? (html + javascript + css)

### ASSISTANT
Here's a standalone HTML file with a horizontal bar chart for the top-10 composers who set Kotzebue's texts to music:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Composers who set Kotzebue's texts to music — Top 10</title>
<style>
  :root {
    --bar-color: #4a7c91;
    --bar-hover: #6ba3ba;
    --bg: #fafafa;
    --text: #2c2c2c;
    --grid: #e0e0e0;
    --accent: #c0392b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    background: var(--bg);
    color: var(--text);
    padding: 2rem 1rem;
    display: flex;
    justify-content: center;
  }

  .chart-container {
    max-width: 860px;
    width: 100%;
  }

  h1 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 0.25rem;
    line-height: 1.3;
  }

  .subtitle {
    font-size: 0.95rem;
    color: #666;
    margin-bottom: 2rem;
  }

  .bar-row {
    display: flex;
    align-items: center;
    margin-bottom: 0.6rem;
  }

  .bar-label {
    width: 260px;
    min-width: 260px;
    text-align: right;
    padding-right: 14px;
    font-size: 0.88rem;
    line-height: 1.35;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  .bar-track {
    flex: 1;
    position: relative;
    height: 32px;
    background: #f0f0f0;
    border-radius: 4px;
    overflow: hidden;
  }

  .bar-fill {
    height: 100%;
    background: var(--bar-color);
    border-radius: 4px;
    transition: width 1.2s cubic-bezier(0.25, 0.8, 0.25, 1),
                background-color 0.2s ease;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 8px;
    min-width: 0;
    cursor: default;
  }

  .bar-fill:hover {
    background: var(--bar-hover);
  }

  .bar-fill.top-composer {
    background: var(--accent);
  }
  .bar-fill.top-composer:hover {
    background: #e74c3c;
  }

  .bar-value {
    font-size: 0.82rem;
    font-weight: 600;
    color: #fff;
    white-space: nowrap;
    opacity: 0;
    transition: opacity 0.3s ease 0.8s;
  }

  .bar-value.visible {
    opacity: 1;
  }

  .bar-value.outside {
    color: var(--text);
    padding-left: 8px;
    opacity: 0;
    transition: opacity 0.3s ease 0.8s;
  }

  .bar-value.outside.visible {
    opacity: 1;
  }

  .axis-line {
    border-top: 1px solid var(--grid);
    margin-left: 260px;
    margin-top: 0.5rem;
    padding-top: 0.35rem;
    display: flex;
    justify-content: space-between;
    font-size: 0.75rem;
    color: #999;
  }

  .source-note {
    margin-top: 1.5rem;
    font-size: 0.78rem;
    color: #999;
    line-height: 1.5;
  }

  @media (max-width: 600px) {
    .bar-label { width: 140px; min-width: 140px; font-size: 0.78rem; }
    .axis-line { margin-left: 140px; }
    h1 { font-size: 1.2rem; }
  }
</style>
</head>
<body>

<div class="chart-container">
  <h1>Composers who set Kotzebue's texts to music</h1>
  <p class="subtitle">Top 10 by number of RISM sources (Kotzebue as lyricist / librettist)</p>
  <div id="chart"></div>
  <div class="axis-line" id="axis"></div>
  <p class="source-note">
    Data: RISM sources via LinkedMusic Knowledge Graph · Kotzebue linked via P655 (lyricist), P87 (librettist), P676 (lyrics) · Count = distinct sources per composer (P86)
  </p>
</div>

<script>
const data = [
  { composer: "Himmel, Friedrich Heinrich (1765–1814)", count: 139 },
  { composer: "Weber, Bernhard Anselm (1764–1821)",      count: 27  },
  { composer: "Weber, Carl Maria von (1786–1826)",       count: 22  },
  { composer: "Anonymus",                                 count: 21  },
  { composer: "Beethoven, Ludwig van (1770–1827)",       count: 20  },
  { composer: "Weigl, Joseph (1766–1846)",               count: 14  },
  { composer: "Ritter, Peter (1763–1846)",               count: 13  },
  { composer: "Kreutzer, Conradin (1780–1849)",          count: 10  },
  { composer: "Kuhlau, Friedrich (1786–1832)",           count: 9   },
  { composer: "Lindpaintner, Peter Josef von (1791–1856)", count: 6 }
];

const maxCount = Math.max(...data.map(d => d.count));
const chart = document.getElementById("chart");
const axis   = document.getElementById("axis");

// Render bars
data.forEach((d, i) => {
  const pct = (d.count / maxCount) * 100;
  const isTop = i === 0;

  const row = document.createElement("div");
  row.className = "bar-row";

  const label = document.createElement("div");
  label.className = "bar-label";
  label.textContent = d.composer;
  label.title = d.composer;

  const track = document.createElement("div");
  track.className = "bar-track";

  const fill = document.createElement("div");
  fill.className = "bar-fill" + (isTop ? " top-composer" : "");
  fill.style.width = "0%";

  const value = document.createElement("span");
  value.className = "bar-value";
  value.textContent = d.count;

  fill.appendChild(value);
  track.appendChild(fill);
  row.appendChild(label);
  row.appendChild(track);
  chart.appendChild(row);

  // Animate in
  requestAnimationFrame(() => {
    setTimeout(() => {
      fill.style.width = pct + "%";
      value.classList.add("visible");
    }, i * 80);
  });
});

// Axis ticks
const ticks = [0, Math.round(maxCount / 4), Math.round(maxCount / 2), Math.round(3 * maxCount / 4), maxCount];
ticks.forEach(t => {
  const span = document.createElement("span");
  span.textContent = t;
  axis.appendChild(span);
});
</script>

</body>
</html>
```

**What this gives you:**

- **Horizontal bar chart** with animated bars that grow on load, staggered by 80 ms per row for a cascading effect.
- **Friedrich Heinrich Himmel** is highlighted in red (accent color) since he dominates with 139 sources — more than the next 6 composers combined.
- **Responsive layout**: on screens under 600 px the label column shrinks for mobile readability.
- **Hover effect** on each bar for interactivity.
- **Axis ticks** along the bottom for scale reference.
- **Source note** at the bottom crediting RISM / LinkedMusic.

Just save it as an `.html` file and open it in any browser — no external libraries needed!