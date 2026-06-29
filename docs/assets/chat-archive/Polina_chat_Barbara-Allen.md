### USER
Can you search for song titles from Global Jukebox in other LinkedMusic subgraphs?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

I now have comprehensive results. Let me compile the final answer.

**Yes, Global Jukebox song titles can be found in other LinkedMusic subgraphs — specifically in MusicBrainz.** Here are the findings from the cross-graph search:

## Results

Global Jukebox song titles matching entities in **other LinkedMusic subgraphs** (exact label match):

| GJB Song Title | Matching Subgraph | Matching Entity | 
|---|---|---|
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/7af29525-7aa6-4aa8-a4f1-d57b208d1bbb` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/a3c851af-8b00-4efe-a42d-e97d5a198603` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/e4ddbc0c-fbe9-426d-a1a8-7d73009e58de` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/b93426cd-d6cd-47f5-83bf-6232c7c90549` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/8d6d612d-ec28-4a5e-9f9b-f16a5b899509` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/38e0e381-68d8-4417-bfe6-d5d5718a0fb2` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/eadd9564-e250-4da0-a09c-264de7316d42` |
| **Children's Song** | musicbrainz | `musicbrainz.org/recording/91369158-d44b-4cab-be3b-4c64b4b9f8b4` |
| **How Long** | musicbrainz | `musicbrainz.org/recording/d1fb304a-cbc8-4c8b-929d-152c148f5364` |
| **How Long** | musicbrainz | `musicbrainz.org/recording/996d4faf-62a2-4376-8eb3-ea493b1231dd` |
| **How Long** | musicbrainz | `musicbrainz.org/recording/7d913210-abec-49bc-9262-0c060247fd39` |
| **Shorty George** | musicbrainz | `musicbrainz.org/recording/7ba671c8-ed7f-453d-b932-46d8cf2c986a` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/479c4589-c3e5-4e43-a6be-17c800643838` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/59b8cf8c-5acf-4827-a69d-089f130c4d2f` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/c5a22e6d-97a9-4f46-a640-e6030b5eeb18` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/f2bf8219-077b-4dce-a3af-7205edcda8e2` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/640020bb-1c45-4c5f-96af-fa0ca182a49b` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/65eb05a4-b79e-41ee-8afe-ca80ed1b0db0` |
| **Fandango** | musicbrainz | `musicbrainz.org/recording/e6d60abb-0cd7-4753-a8b1-504568c7658e` |

## Key Observations

1. **Only MusicBrainz yielded matches** — no GJB song titles were found in thesession, utsi, diamm, cantusdb, cantusindex, rism, wjazzd, simssadb, or dig-that-lick graphs.

2. **5 distinct GJB titles matched** in MusicBrainz: *Lullaby*, *Children's Song*, *How Long*, *Shorty George*, *Sweet Home Chicago*, and *Fandango* — totaling 19 recording matches.

3. These are **mostly generic or well-known titles** (e.g., "Lullaby", "How Long", "Sweet Home Chicago"), so the matches are likely **coincidental title overlaps rather than references to the same song**. The Global Jukebox focuses on ethnographic/field recordings of world music, while MusicBrainz catalogs commercial recordings.

4. The vast majority of GJB's ~5,447 distinct song titles (highly specific ethnographic names like "Mosori", "Kembang Mas", "Enrilang", "Pokob E Pokob") have **no matches** in any other LinkedMusic subgraph, reflecting the unique, specialized nature of the Global Jukebox collection.

**SPARQL query used for the final comprehensive result:**

```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>

SELECT DISTINCT ?gjb_title ?matching_entity
WHERE {
  VALUES ?gjb_title { "Fandango" "Lullaby" "Children's Song" "How Long" "Shorty George" "Sweet Home Chicago" ... }
  GRAPH <https://linkedmusic.ca/graphs/musicbrainz/> {
    ?matching_entity rdfs:label ?gjb_title .
  }
}
LIMIT 25
```
</details>

**Validating and executing SPARQL query**


I now have comprehensive results. Let me compile the final answer.

**Yes, Global Jukebox song titles can be found in other LinkedMusic subgraphs — specifically in MusicBrainz.** Here are the findings from the cross-graph search:

## Results

Global Jukebox song titles matching entities in **other LinkedMusic subgraphs** (exact label match):

| GJB Song Title | Matching Subgraph | Matching Entity | 
|---|---|---|
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/7af29525-7aa6-4aa8-a4f1-d57b208d1bbb` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/a3c851af-8b00-4efe-a42d-e97d5a198603` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/e4ddbc0c-fbe9-426d-a1a8-7d73009e58de` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/b93426cd-d6cd-47f5-83bf-6232c7c90549` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/8d6d612d-ec28-4a5e-9f9b-f16a5b899509` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/38e0e381-68d8-4417-bfe6-d5d5718a0fb2` |
| **Lullaby** | musicbrainz | `musicbrainz.org/recording/eadd9564-e250-4da0-a09c-264de7316d42` |
| **Children's Song** | musicbrainz | `musicbrainz.org/recording/91369158-d44b-4cab-be3b-4c64b4b9f8b4` |
| **How Long** | musicbrainz | `musicbrainz.org/recording/d1fb304a-cbc8-4c8b-929d-152c148f5364` |
| **How Long** | musicbrainz | `musicbrainz.org/recording/996d4faf-62a2-4376-8eb3-ea493b1231dd` |
| **How Long** | musicbrainz | `musicbrainz.org/recording/7d913210-abec-49bc-9262-0c060247fd39` |
| **Shorty George** | musicbrainz | `musicbrainz.org/recording/7ba671c8-ed7f-453d-b932-46d8cf2c986a` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/479c4589-c3e5-4e43-a6be-17c800643838` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/59b8cf8c-5acf-4827-a69d-089f130c4d2f` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/c5a22e6d-97a9-4f46-a640-e6030b5eeb18` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/f2bf8219-077b-4dce-a3af-7205edcda8e2` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/640020bb-1c45-4c5f-96af-fa0ca182a49b` |
| **Sweet Home Chicago** | musicbrainz | `musicbrainz.org/recording/65eb05a4-b79e-41ee-8afe-ca80ed1b0db0` |
| **Fandango** | musicbrainz | `musicbrainz.org/recording/e6d60abb-0cd7-4753-a8b1-504568c7658e` |

## Key Observations

1. **Only MusicBrainz yielded matches** — no GJB song titles were found in thesession, utsi, diamm, cantusdb, cantusindex, rism, wjazzd, simssadb, or dig-that-lick graphs.

2. **5 distinct GJB titles matched** in MusicBrainz: *Lullaby*, *Children's Song*, *How Long*, *Shorty George*, *Sweet Home Chicago*, and *Fandango* — totaling 19 recording matches.

3. These are **mostly generic or well-known titles** (e.g., "Lullaby", "How Long", "Sweet Home Chicago"), so the matches are likely **coincidental title overlaps rather than references to the same song**. The Global Jukebox focuses on ethnographic/field recordings of world music, while MusicBrainz catalogs commercial recordings.

4. The vast majority of GJB's ~5,447 distinct song titles (highly specific ethnographic names like "Mosori", "Kembang Mas", "Enrilang", "Pokob E Pokob") have **no matches** in any other LinkedMusic subgraph, reflecting the unique, specialized nature of the Global Jukebox collection.

The SPARQL has been executed:
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
SELECT DISTINCT ?gjb_title ?matching_entity 
WHERE {
  VALUES ?gjb_title {
  "Fandango" "Lullaby" "Children's Song" "How Long" "Shorty George" "Sweet Home Chicago" ...
} GRAPH <https://linkedmusic.ca/graphs/musicbrainz/> {
  ?matching_entity rdfs:label ?gjb_title .
  
}
} 
LIMIT 25
```

### USER
Please search for ‘Barbara Allen’ in all LinkedMusic subgraphs

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

I now have comprehensive results across all 11 subgraphs. Here is the complete answer:

---

## "Barbara Allen" found in 4 out of 11 LinkedMusic subgraphs

The search for "Barbara Allen" across all LinkedMusic named graphs returned matches in **4 subgraphs**: **thesession**, **utsi**, **theglobaljukebox**, and **rism**. No matches were found in musicbrainz (exact match returned empty; case-insensitive scan timed out due to scale), diamm, cantusdb, cantusindex, wjazzd, simssadb, or dig-that-lick.

---

### 1. thesession — 1 result

| Entity | Label | Type |
|--------|-------|------|
| https://thesession.org/tunes/9177 | Barbara Allen | Tune |

---

### 2. theglobaljukebox — 2 results

| Entity | Label | Type |
|--------|-------|------|
| https://theglobaljukebox.org/song/9409 | Barbara Allen | Song |
| https://theglobaljukebox.org/song/9410 | Barbara Allen | Song |

---

### 3. rism — 1 result

| Entity | Label | Type |
|--------|-------|------|
| https://rism.online/sources/451010166 | Barbara Allen–D major; Manuscript copy; D-HVs Kestner No. 136 (Nr. 58) | Source |

Additional details for this RISM source: genre = Ballads (voc.), mode = D, composer linked to `rism.online/people/30004985`, held at institution `rism.online/institutions/30000824`.

---

### 4. utsi — 20 results (all songs)

| Entity | Label |
|--------|-------|
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARB'RY%20ELLEN%20(%20BARBARA%20ALLEN%20) | BARB'RY ELLEN ( BARBARA ALLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARB'RY%20ELLEN:%20BARBARA%20ALLEN | BARB'RY ELLEN: BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARB'RY%20ELLEN;%20OR%20BARBARA%20ALLEN | BARB'RY ELLEN; OR BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN | BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20(%20BARB'RA%20ALLEN%20) | BARBARA ALLEN ( BARB'RA ALLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20/%20BARB'RY%20ALLEN | BARBARA ALLEN / BARB'RY ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(%20BONNY%20BARBARA%20ALLEN%20\) | BARBARA ALLEN ( BONNY BARBARA ALLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(CHILD%2084\) | BARBARA ALLEN (CHILD 84) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(CHILD%2084\)%20\(WORDS%20ONLY\) | BARBARA ALLEN (CHILD 84) (WORDS ONLY) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(TEXT%20ONLY\) | BARBARA ALLEN (TEXT ONLY) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN]%20BARB'RA%20ELLEN | BARBARA ALLEN] BARB'RA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN]%20BARBARA%20ELLEN | BARBARA ALLEN] BARBARA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN | BONNY BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20A:%20BARBARA%20ELLEN | BONNY BARBARA ALLEN (CHILD, NO. 84), A: BARBARA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20B:%20BARBARA%20ELLEN | BONNY BARBARA ALLEN (CHILD, NO. 84), B: BARBARA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20C:%20BARBARA%20ALLEN | BONNY BARBARA ALLEN (CHILD, NO. 84), C: BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20E | BONNY BARBARA ALLEN (CHILD, NO. 84), E |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20\(%20BARBARA%20ELLEN%20\) | BONNY BARBARA ALLEN ( BARBARA ELLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20\(%20ENGLISH%20AIR%20\) | BONNY BARBARA ALLEN ( ENGLISH AIR ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20\(I\) | BONNY BARBARA ALLEN (I) |

---

### No results in these subgraphs: musicbrainz, diamm, cantusdb, cantusindex, wjazzd, simssadb, dig-that-lick

---

### Summary

| Subgraph | Match Count | Entity Type(s) |
|----------|-------------|----------------|
| **utsi** | 20 | Song |
| **theglobaljukebox** | 2 | Song |
| **thesession** | 1 | Tune |
| **rism** | 1 | Source |
| **Total** | **24** | |

The UTSI (University of Tennessee Song Index) has the richest representation of "Barbara Allen" with 20 variant entries including alternate spellings ("Barb'ry Ellen", "Barb'ra Ellen"), Child Ballad number references (Child 84), and multiple tune variants. This reflects the song's prominence as one of the most widely collected folk ballads in the English-speaking world (Child Ballad 84).
</details>

**Validating and executing SPARQL query**


I now have comprehensive results across all 11 subgraphs. Here is the complete answer:

---

## "Barbara Allen" found in 4 out of 11 LinkedMusic subgraphs

The search for "Barbara Allen" across all LinkedMusic named graphs returned matches in **4 subgraphs**: **thesession**, **utsi**, **theglobaljukebox**, and **rism**. No matches were found in musicbrainz (exact match returned empty; case-insensitive scan timed out due to scale), diamm, cantusdb, cantusindex, wjazzd, simssadb, or dig-that-lick.

---

### 1. thesession — 1 result

| Entity | Label | Type |
|--------|-------|------|
| https://thesession.org/tunes/9177 | Barbara Allen | Tune |

---

### 2. theglobaljukebox — 2 results

| Entity | Label | Type |
|--------|-------|------|
| https://theglobaljukebox.org/song/9409 | Barbara Allen | Song |
| https://theglobaljukebox.org/song/9410 | Barbara Allen | Song |

---

### 3. rism — 1 result

| Entity | Label | Type |
|--------|-------|------|
| https://rism.online/sources/451010166 | Barbara Allen–D major; Manuscript copy; D-HVs Kestner No. 136 (Nr. 58) | Source |

Additional details for this RISM source: genre = Ballads (voc.), mode = D, composer linked to `rism.online/people/30004985`, held at institution `rism.online/institutions/30000824`.

---

### 4. utsi — 20 results (all songs)

| Entity | Label |
|--------|-------|
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARB'RY%20ELLEN%20(%20BARBARA%20ALLEN%20) | BARB'RY ELLEN ( BARBARA ALLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARB'RY%20ELLEN:%20BARBARA%20ALLEN | BARB'RY ELLEN: BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARB'RY%20ELLEN;%20OR%20BARBARA%20ALLEN | BARB'RY ELLEN; OR BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN | BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20(%20BARB'RA%20ALLEN%20) | BARBARA ALLEN ( BARB'RA ALLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20/%20BARB'RY%20ALLEN | BARBARA ALLEN / BARB'RY ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(%20BONNY%20BARBARA%20ALLEN%20\) | BARBARA ALLEN ( BONNY BARBARA ALLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(CHILD%2084\) | BARBARA ALLEN (CHILD 84) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(CHILD%2084\)%20\(WORDS%20ONLY\) | BARBARA ALLEN (CHILD 84) (WORDS ONLY) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN%20\(TEXT%20ONLY\) | BARBARA ALLEN (TEXT ONLY) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN]%20BARB'RA%20ELLEN | BARBARA ALLEN] BARB'RA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BARBARA%20ALLEN]%20BARBARA%20ELLEN | BARBARA ALLEN] BARBARA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN | BONNY BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20A:%20BARBARA%20ELLEN | BONNY BARBARA ALLEN (CHILD, NO. 84), A: BARBARA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20B:%20BARBARA%20ELLEN | BONNY BARBARA ALLEN (CHILD, NO. 84), B: BARBARA ELLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20C:%20BARBARA%20ALLEN | BONNY BARBARA ALLEN (CHILD, NO. 84), C: BARBARA ALLEN |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20(CHILD,%20NO.%2084),%20E | BONNY BARBARA ALLEN (CHILD, NO. 84), E |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20\(%20BARBARA%20ELLEN%20\) | BONNY BARBARA ALLEN ( BARBARA ELLEN ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20\(%20ENGLISH%20AIR%20\) | BONNY BARBARA ALLEN ( ENGLISH AIR ) |
| https://databases.lib.utk.edu/songdb/songdb.php?word=0&title=BONNY%20BARBARA%20ALLEN%20\(I\) | BONNY BARBARA ALLEN (I) |

---

### No results in these subgraphs: musicbrainz, diamm, cantusdb, cantusindex, wjazzd, simssadb, dig-that-lick

---

### Summary

| Subgraph | Match Count | Entity Type(s) |
|----------|-------------|----------------|
| **utsi** | 20 | Song |
| **theglobaljukebox** | 2 | Song |
| **thesession** | 1 | Tune |
| **rism** | 1 | Source |
| **Total** | **24** | |

The UTSI (University of Tennessee Song Index) has the richest representation of "Barbara Allen" with 20 variant entries including alternate spellings ("Barb'ry Ellen", "Barb'ra Ellen"), Child Ballad number references (Child 84), and multiple tune variants. This reflects the song's prominence as one of the most widely collected folk ballads in the English-speaking world (Child Ballad 84).

### USER
What are these UTSI hits? What do we know about them? Are they related in any way?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

Ask the user which knowledge graph would they want me to query: Culture Knowledge Graph or GESIS KG?
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

Now I have all the data. Let me compile the comprehensive answer.

## UTSI "Barbara Allen" Hits: Full Analysis

There are **20 Song entities** in the UTSI graph matching "Barbara Allen." All are typed as `utsi:Song`. They represent **different collected variants** of the same traditional ballad (Child Ballad 84), as indexed in various published folk song anthologies held by the University of Tennessee library.

---

### Complete Entity Inventory

| # | Label | Key Distinguishing Feature |
|---|-------|---------------------------|
| 1 | BARB'RY ELLEN ( BARBARA ALLEN ) | Irish variant (Lim'rick) |
| 2 | BARB'RY ELLEN: BARBARA ALLEN | Irish variant |
| 3 | BARB'RY ELLEN; OR BARBARA ALLEN | Irish variant |
| 4 | BARBARA ALLEN | **Aggregation entity** — richest (many collections, first lines, composers) |
| 5 | BARBARA ALLEN ( BARB'RA ALLEN ) | North Carolina variant |
| 6 | BARBARA ALLEN / BARB'RY ALLEN | U.S. variant |
| 7 | BARBARA ALLEN ( BONNY BARBARA ALLEN ) | U.S. variant (WV + OH) |
| 8 | BARBARA ALLEN (CHILD 84) | East Tennessee collection |
| 9 | BARBARA ALLEN (CHILD 84) (WORDS ONLY) | Text-only variant |
| 10 | BARBARA ALLEN (TEXT ONLY) | Text-only variant (no composer) |
| 11 | BARBARA ALLEN] BARB'RA ELLEN | U.S. variant (Sing of America / Songs of Man) |
| 12 | BARBARA ALLEN] BARBARA ELLEN | Nova Scotia variant |
| 13 | BONNY BARBARA ALLEN | U.S. + UK variant |
| 14 | BONNY BARBARA ALLEN (CHILD, NO. 84), A: BARBARA ELLEN | Ohio variant A |
| 15 | BONNY BARBARA ALLEN (CHILD, NO. 84), B: BARBARA ELLEN | Ohio variant B |
| 16 | BONNY BARBARA ALLEN (CHILD, NO. 84), C: BARBARA ALLEN | Ohio variant C |
| 17 | BONNY BARBARA ALLEN (CHILD, NO. 84), E | Ohio variant E |
| 18 | BONNY BARBARA ALLEN ( BARBARA ELLEN ) | Ohio variant |
| 19 | BONNY BARBARA ALLEN ( ENGLISH AIR ) | English air variant |
| 20 | BONNY BARBARA ALLEN (I) | U.S. variant (American Anthology) |

---

### Properties Present Across All 20 Entities

| Property | Wikidata ID | Meaning | Present on |
|----------|-------------|---------|------------|
| **rdf:type** | — | utsi:Song | All 20 |
| **rdfs:label** | — | Song title (variant spelling) | All 20 |
| **P136** | Genre | All 20 — always Q43343 (folk song) |
| **P1922** | First line of text | All 20 — varying opening lines |
| **P361** | Part of (anthology/collection) | All 20 — various anthologies |
| **P407** | Language | All 20 — always Q1860 (English) |
| **P676** | Subject/work | 19 of 20 — mostly Q4233718 (Barbara Allen) |
| **P86** | Composer | 19 of 20 — mostly Q86167 (traditional/trad.) |
| **P1071** | Location of formation | 16 of 20 — varying countries/regions |
| **P870** | Instrument | 8 of 20 — always Q52954 (piano) when present |
| **P1433** | Published in | 1 of 20 — the aggregation entity only |

---

### Composer (P86) Values

| Composer URI/Value | Appears on | Meaning |
|--------------------|------------|---------|
| **Q86167** | 18 entities | Traditional / Anonymous |
| **Q56260622** | 2 entities | (Wikidata entity — specific arranger) |
| **Q6520499** | 1 entity | (Wikidata entity) |
| **Q75288932** | 1 entity | (Wikidata entity) |
| **Q5058116** | 1 entity | (Wikidata entity) |
| **Q315723** | 1 entity | (Wikidata entity) |
| **Q2960395** | 1 entity | (Wikidata entity) |
| **FISHER, WILLIAM ARMS, ARR.** | 1 entity | Arranger (string literal) |
| **MOFFAT, ALFRED (ARR.)** | 1 entity | Arranger (string literal) |
| **SIEGMEISTER, ELIE (ARR.)** | 1 entity | Arranger (string literal) |
| **SCOTT, TOM ( ARR)** | 1 entity | Arranger (string literal) |
| **RUFTY, HILTON** | 3 entities | Arranger (string literal) |
| **NONE** | 1 entity | No composer listed (text-only variant) |
| **Q11836324** | 1 entity | (Wikidata entity) |

The vast majority are attributed to **Q86167** (traditional/anonymous), reflecting the ballad's folk origin. Several named arrangers (Fisher, Moffat, Siegmeister, Rufty, Scott) appear for published arranged versions.

---

### Genre (P136) Values

| Value | Appears on | Meaning |
|-------|------------|---------|
| **Q43343** | All 20 | Folk song |
| **Q4797274** | 2 entities | Narrative ballad |
| **Q373342** | 1 entity | Ballad |

All are classified as folk songs; some carry additional genre tags of "narrative ballad" or "ballad."

---

### Subject/Work (P676) Values

| Value | Appears on | Meaning |
|-------|------------|---------|
| **Q4233718** | 17 entities | Barbara Allen (the Wikidata item for the ballad) |
| **Q315723** | 1 entity | (Wikidata entity) |
| **Q11318125** | 1 entity | (Wikidata entity) |
| **Q11836324** | 1 entity | (Wikidata entity) |
| **TRADITIONAL** | 1 entity | String literal |

---

### Location of Formation (P1071) — Geographic Origins

| Country | Wikidata URI | Appears on |
|---------|-------------|------------|
| **United States** (Q30) | Q30 | 8 entities |
| **England** (Q21) | Q21 | 4 entities |
| **Ireland** (Q18389) | Q18389 | 3 entities |
| **Ohio** (Q1397) | Q1397 | 4 entities |
| **Scotland** (Q22) | Q22 | 1 entity |
| **North Carolina** (Q23666) | Q23666 | 2 entities |
| **Florida** (Q812) | Q812 | 1 entity |
| **Canada** (Q16) | Q16 | 1 entity |
| **Virginia** (Q230) | Q230 | 1 entity |
| **Kentucky** (Q1581) | Q1581 | 1 entity |
| **Wales** (Q93332) | Q93332 | 1 entity |

---

### First Lines of Text (P1922) — Demonstrating Variants

Each entity has one or more opening lines, showing how the ballad varies across collections:

| First Line | Appears on |
|-----------|------------|
| IN SCARLET TOWN WHERE I WAS BORN | 6 entities |
| IN SCARLET TOWN WHERE I WAS BORN, THERE WAS A FAIR MAID DWELLIN' | 2 entities |
| IN SCARLET TOWN WHERE I DID DWELL | 1 entity |
| IN LIM'RICK CITY HE WAS BROUGHT UP | 1 entity (Irish) |
| IN LIMRICK CITY HE WAS BROUGHT UP AND DUBLIN WAS HIS STATION | 1 entity (Irish) |
| IN STORYTOWN WHERE I DID LIVE | 2 entities (Ohio) |
| IN READING TOWN THERE I WAS BORN | 1 entity |
| IN SCARBOROUGH TOWN | 1 entity |
| AWAY LOW DOWN IN STONY TOWN | 1 entity |
| IN LONDON TOWN WHERE I ONCE LIVED | 2 entities |
| IN YONDERS TOWN WHERE I WAS BORN | 1 entity |
| 'TWAS IN THE AUTUMN THE MOISTTIME OF THE YEAR | 1 entity |
| 'TWAS IN THE MERRY MONTH OF MAY | 1 entity |
| 'TWAS IN THE SPRINGTIME OF THE YEAR | 1 entity |
| IT WAS UPON A HIGH, HIGH HILL TWO MAIDENS CHOSE THEIR DWELLING | 1 entity |
| THEY GREW UP AND THEY GREW TO THE CHURCH STEEPLE TOP | 1 entity |
| + ~15 more variants on the aggregation entity |

---

### Collections / Anthologies (P361) — Where Each Variant Was Published

The "BARBARA ALLEN" aggregation entity (#4) is part of **~40+ anthologies**, including:

American Favorite Ballads · Americans and Their Songs · An Alabama Songbook · Ancient Ballads Traditionally Sung in New England · Ballads and Songs of Southern Michigan · Beech Mountain Folk-Songs and Ballads · Burl Ives Song Book · English Folk Songs from the Southern Appalachia Mts. · English Melodies · Fake Book of the World's Favorite Songs · Fireside Book of Folk Songs · Folk Songs Abecedary · Folk Songs of Florida · Folk Songs of North America · Folk Visions and Voices (North Georgia) · Folksongs and Chanties · Garland of English Folk-Songs · Heart Songs · Heritage Songster · Joan Baez Song Book · Lomax: Folk Songs of North America · Memory Melodies · My Favorite Folk Songs · One Hundred Songs of England · Ozark Folksongs · Reliquary of English Song · The Oxford Song Book · Traditional American Folk Songs (Warner Collection) · Traditional Tunes · Songs Lincoln Loved · The East Tennessee State University Collection of Folklore: Folksongs · The Guitar Songbook · Singa Hipsey Doodle (West Virginia) · Song Catcher in Southern Mountains · etc.

Other entities are linked to **1–3 anthologies** each, including:
- *Folk Songs of Old New England* (Irish variants)
- *Jerry Silverman's Folk Song Encyclopedia* (variant #1)
- *Sing of America / Songs of Man* (variant #11)
- *Traditional Songs from Nova Scotia* (variant #12)
- *Ballads and Songs from Ohio* (variants #14–18)
- *American Anthology of Old-World Ballads* (variants #7, 19, 20)
- *Ballads and Folk Songs of the Southwest* (variant #13)
- *The Scots Musical Museum* (variant #13)

---

### Instrument (P870)

When present, always **Q52954** (piano), or **Q34379** (guitar, on entity #4 only). This reflects the published arrangement medium, not the original folk instrumentation.

---

### Are They Related?

**Yes, deeply — they are all variants of the same ballad.** The relationships are:

1. **Shared subject (P676 = Q4233718)**: 17 of 20 entities link to the same Wikidata item for "Barbara Allen" the ballad, confirming they are all instances of the same folk work.

2. **Shared genre (P136 = Q43343)**: All 20 are classified as folk songs.

3. **Shared language (P407 = Q1860)**: All are in English.

4. **Shared composer (P86 = Q86167)**: 18 of 20 are attributed to "traditional" (anonymous folk origin).

5. **Shared narrative structure**: The first lines (P1922) all begin variations of the same narrative — "In Scarlet Town where I was born," "In the merry month of May," etc. — all opening the Barbara Allen story.

6. **Title variants encode the relationships**: Labels like "BARB'RY ELLEN; OR BARBARA ALLEN" and "BONNY BARBARA ALLEN (CHILD, NO. 84), A: BARBARA ELLEN" explicitly reference the other names for the same ballad and its Child Ballad number (84).

7. **Geographic spread reflects transmission**: The locations (Ireland → England → Scotland → U.S. regions like Ohio, North Carolina, Virginia, Kentucky, Florida, Appalachia, Nova Scotia) map the ballad's migration across the English-speaking world.

8. **No explicit RDF links between entities**: There are no `skos:relatedMatch`, `owl:sameAs`, or other inter-entity links within UTSI connecting the 20 songs to each other. Their relatedness is **implicit** — inferred from shared P676 (subject), P86 (composer), P136 (genre), and the ballad naming conventions in their labels.

---

**Key SPARQL queries used:**

```sparql
# Entity discovery
SELECT ?entity ?label WHERE {
  GRAPH <https://linkedmusic.ca/graphs/utsi/> {
    ?entity rdfs:label ?label .
    FILTER(CONTAINS(LCASE(STR(?label)), "barbara allen"))
  }
} LIMIT 30

# Property retrieval per entity (batched by VALUES and FILTER on label)
SELECT ?entity ?p ?o WHERE {
  GRAPH <https://linkedmusic.ca/graphs/utsi/> {
    ?entity rdfs:label ?label .
    FILTER(?label IN ("BARBARA ALLEN / BARB'RY ALLEN", ...))
    ?entity ?p ?o .
  }
} ORDER BY ?entity ?p
```
</details>

**Validating and executing SPARQL query**


Now I have all the data. Let me compile the comprehensive answer.

## UTSI "Barbara Allen" Hits: Full Analysis

There are **20 Song entities** in the UTSI graph matching "Barbara Allen." All are typed as `utsi:Song`. They represent **different collected variants** of the same traditional ballad (Child Ballad 84), as indexed in various published folk song anthologies held by the University of Tennessee library.

---

### Complete Entity Inventory

| # | Label | Key Distinguishing Feature |
|---|-------|---------------------------|
| 1 | BARB'RY ELLEN ( BARBARA ALLEN ) | Irish variant (Lim'rick) |
| 2 | BARB'RY ELLEN: BARBARA ALLEN | Irish variant |
| 3 | BARB'RY ELLEN; OR BARBARA ALLEN | Irish variant |
| 4 | BARBARA ALLEN | **Aggregation entity** — richest (many collections, first lines, composers) |
| 5 | BARBARA ALLEN ( BARB'RA ALLEN ) | North Carolina variant |
| 6 | BARBARA ALLEN / BARB'RY ALLEN | U.S. variant |
| 7 | BARBARA ALLEN ( BONNY BARBARA ALLEN ) | U.S. variant (WV + OH) |
| 8 | BARBARA ALLEN (CHILD 84) | East Tennessee collection |
| 9 | BARBARA ALLEN (CHILD 84) (WORDS ONLY) | Text-only variant |
| 10 | BARBARA ALLEN (TEXT ONLY) | Text-only variant (no composer) |
| 11 | BARBARA ALLEN] BARB'RA ELLEN | U.S. variant (Sing of America / Songs of Man) |
| 12 | BARBARA ALLEN] BARBARA ELLEN | Nova Scotia variant |
| 13 | BONNY BARBARA ALLEN | U.S. + UK variant |
| 14 | BONNY BARBARA ALLEN (CHILD, NO. 84), A: BARBARA ELLEN | Ohio variant A |
| 15 | BONNY BARBARA ALLEN (CHILD, NO. 84), B: BARBARA ELLEN | Ohio variant B |
| 16 | BONNY BARBARA ALLEN (CHILD, NO. 84), C: BARBARA ALLEN | Ohio variant C |
| 17 | BONNY BARBARA ALLEN (CHILD, NO. 84), E | Ohio variant E |
| 18 | BONNY BARBARA ALLEN ( BARBARA ELLEN ) | Ohio variant |
| 19 | BONNY BARBARA ALLEN ( ENGLISH AIR ) | English air variant |
| 20 | BONNY BARBARA ALLEN (I) | U.S. variant (American Anthology) |

---

### Properties Present Across All 20 Entities

| Property | Wikidata ID | Meaning | Present on |
|----------|-------------|---------|------------|
| **rdf:type** | — | utsi:Song | All 20 |
| **rdfs:label** | — | Song title (variant spelling) | All 20 |
| **P136** | Genre | All 20 — always Q43343 (folk song) |
| **P1922** | First line of text | All 20 — varying opening lines |
| **P361** | Part of (anthology/collection) | All 20 — various anthologies |
| **P407** | Language | All 20 — always Q1860 (English) |
| **P676** | Subject/work | 19 of 20 — mostly Q4233718 (Barbara Allen) |
| **P86** | Composer | 19 of 20 — mostly Q86167 (traditional/trad.) |
| **P1071** | Location of formation | 16 of 20 — varying countries/regions |
| **P870** | Instrument | 8 of 20 — always Q52954 (piano) when present |
| **P1433** | Published in | 1 of 20 — the aggregation entity only |

---

### Composer (P86) Values

| Composer URI/Value | Appears on | Meaning |
|--------------------|------------|--------|
| **Q86167** | 18 entities | Traditional / Anonymous |
| **Q56260622** | 2 entities | (Wikidata entity — specific arranger) |
| **Q6520499** | 1 entity | (Wikidata entity) |
| **Q75288932** | 1 entity | (Wikidata entity) |
| **Q5058116** | 1 entity | (Wikidata entity) |
| **Q315723** | 1 entity | (Wikidata entity) |
| **Q2960395** | 1 entity | (Wikidata entity) |
| **FISHER, WILLIAM ARMS, ARR.** | 1 entity | Arranger (string literal) |
| **MOFFAT, ALFRED (ARR.)** | 1 entity | Arranger (string literal) |
| **SIEGMEISTER, ELIE (ARR.)** | 1 entity | Arranger (string literal) |
| **SCOTT, TOM ( ARR)** | 1 entity | Arranger (string literal) |
| **RUFTY, HILTON** | 3 entities | Arranger (string literal) |
| **NONE** | 1 entity | No composer listed (text-only variant) |
| **Q11836324** | 1 entity | (Wikidata entity) |

The vast majority are attributed to **Q86167** (traditional/anonymous), reflecting the ballad's folk origin. Several named arrangers (Fisher, Moffat, Siegmeister, Rufty, Scott) appear for published arranged versions.

---

### Genre (P136) Values

| Value | Appears on | Meaning |
|-------|------------|--------|
| **Q43343** | All 20 | Folk song |
| **Q4797274** | 2 entities | Narrative ballad |
| **Q373342** | 1 entity | Ballad |

All are classified as folk songs; some carry additional genre tags of "narrative ballad" or "ballad."

---

### Subject/Work (P676) Values

| Value | Appears on | Meaning |
|-------|------------|--------|
| **Q4233718** | 17 entities | Barbara Allen (the Wikidata item for the ballad) |
| **Q315723** | 1 entity | (Wikidata entity) |
| **Q11318125** | 1 entity | (Wikidata entity) |
| **Q11836324** | 1 entity | (Wikidata entity) |
| **TRADITIONAL** | 1 entity | String literal |

---

### Location of Formation (P1071) — Geographic Origins

| Country | Wikidata URI | Appears on |
|---------|-------------|------------|
| **United States** (Q30) | Q30 | 8 entities |
| **England** (Q21) | Q21 | 4 entities |
| **Ireland** (Q18389) | Q18389 | 3 entities |
| **Ohio** (Q1397) | Q1397 | 4 entities |
| **Scotland** (Q22) | Q22 | 1 entity |
| **North Carolina** (Q23666) | Q23666 | 2 entities |
| **Florida** (Q812) | Q812 | 1 entity |
| **Canada** (Q16) | Q16 | 1 entity |
| **Virginia** (Q230) | Q230 | 1 entity |
| **Kentucky** (Q1581) | Q1581 | 1 entity |
| **Wales** (Q93332) | Q93332 | 1 entity |

---

### First Lines of Text (P1922) — Demonstrating Variants

Each entity has one or more opening lines, showing how the ballad varies across collections:

| First Line | Appears on |
|-----------|------------|
| IN SCARLET TOWN WHERE I WAS BORN | 6 entities |
| IN SCARLET TOWN WHERE I WAS BORN, THERE WAS A FAIR MAID DWELLIN' | 2 entities |
| IN SCARLET TOWN WHERE I DID DWELL | 1 entity |
| IN LIM'RICK CITY HE WAS BROUGHT UP | 1 entity (Irish) |
| IN LIMRICK CITY HE WAS BROUGHT UP AND DUBLIN WAS HIS STATION | 1 entity (Irish) |
| IN STORYTOWN WHERE I DID LIVE | 2 entities (Ohio) |
| IN READING TOWN THERE I WAS BORN | 1 entity |
| IN SCARBOROUGH TOWN | 1 entity |
| AWAY LOW DOWN IN STONY TOWN | 1 entity |
| IN LONDON TOWN WHERE I ONCE LIVED | 2 entities |
| IN YONDERS TOWN WHERE I WAS BORN | 1 entity |
| 'TWAS IN THE AUTUMN THE MOISTTIME OF THE YEAR | 1 entity |
| 'TWAS IN THE MERRY MONTH OF MAY | 1 entity |
| 'TWAS IN THE SPRINGTIME OF THE YEAR | 1 entity |
| IT WAS UPON A HIGH, HIGH HILL TWO MAIDENS CHOSE THEIR DWELLING | 1 entity |
| THEY GREW UP AND THEY GREW TO THE CHURCH STEEPLE TOP | 1 entity |
| + ~15 more variants on the aggregation entity |

---

### Collections / Anthologies (P361) — Where Each Variant Was Published

The "BARBARA ALLEN" aggregation entity (#4) is part of **~40+ anthologies**, including:

American Favorite Ballads · Americans and Their Songs · An Alabama Songbook · Ancient Ballads Traditionally Sung in New England · Ballads and Songs of Southern Michigan · Beech Mountain Folk-Songs and Ballads · Burl Ives Song Book · English Folk Songs from the Southern Appalachia Mts. · English Melodies · Fake Book of the World's Favorite Songs · Fireside Book of Folk Songs · Folk Songs Abecedary · Folk Songs of Florida · Folk Songs of North America · Folk Visions and Voices (North Georgia) · Folksongs and Chanties · Garland of English Folk-Songs · Heart Songs · Heritage Songster · Joan Baez Song Book · Lomax: Folk Songs of North America · Memory Melodies · My Favorite Folk Songs · One Hundred Songs of England · Ozark Folksongs · Reliquary of English Song · The Oxford Song Book · Traditional American Folk Songs (Warner Collection) · Traditional Tunes · Songs Lincoln Loved · The East Tennessee State University Collection of Folklore: Folksongs · The Guitar Songbook · Singa Hipsey Doodle (West Virginia) · Song Catcher in Southern Mountains · etc.

Other entities are linked to **1–3 anthologies** each, including:
- *Folk Songs of Old New England* (Irish variants)
- *Jerry Silverman's Folk Song Encyclopedia* (variant #1)
- *Sing of America / Songs of Man* (variant #11)
- *Traditional Songs from Nova Scotia* (variant #12)
- *Ballads and Songs from Ohio* (variants #14–18)
- *American Anthology of Old-World Ballads* (variants #7, 19, 20)
- *Ballads and Folk Songs of the Southwest* (variant #13)
- *The Scots Musical Museum* (variant #13)

---

### Instrument (P870)

When present, always **Q52954** (piano), or **Q34379** (guitar, on entity #4 only). This reflects the published arrangement medium, not the original folk instrumentation.

---

### Are They Related?

**Yes, deeply — they are all variants of the same ballad.** The relationships are:

1. **Shared subject (P676 = Q4233718)**: 17 of 20 entities link to the same Wikidata item for "Barbara Allen" the ballad, confirming they are all instances of the same folk work.

2. **Shared genre (P136 = Q43343)**: All 20 are classified as folk songs.

3. **Shared language (P407 = Q1860)**: All are in English.

4. **Shared composer (P86 = Q86167)**: 18 of 20 are attributed to "traditional" (anonymous folk origin).

5. **Shared narrative structure**: The first lines (P1922) all begin variations of the same narrative — "In Scarlet Town where I was born," "In the merry month of May," etc. — all opening the Barbara Allen story.

6. **Title variants encode the relationships**: Labels like "BARB'RY ELLEN; OR BARBARA ALLEN" and "BONNY BARBARA ALLEN (CHILD, NO. 84), A: BARBARA ELLEN" explicitly reference the other names for the same ballad and its Child Ballad number (84).

7. **Geographic spread reflects transmission**: The locations (Ireland → England → Scotland → U.S. regions like Ohio, North Carolina, Virginia, Kentucky, Florida, Appalachia, Nova Scotia) map the ballad's migration across the English-speaking world.

8. **No explicit RDF links between entities**: There are no `skos:relatedMatch`, `owl:sameAs`, or other inter-entity links within UTSI connecting the 20 songs to each other. Their relatedness is **implicit** — inferred from shared P676 (subject), P86 (composer), P136 (genre), and the ballad naming conventions in their labels.

---

**Key SPARQL queries used:**

The SPARQL has been executed:
```sparql
# Entity discovery 
SELECT ?entity ?label 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/utsi/> {
  ?entity rdfs:label ?label .
   
FILTER(CONTAINS(LCASE(STR(?label)), "barbara allen"))
}
} 
LIMIT 30 # Property retrieval per entity (batched by 
VALUES and 
FILTER on label) 
SELECT ?entity ?p ?o 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/utsi/> {
  ?entity rdfs:label ?label .
   
FILTER(?label IN ("BARBARA ALLEN / BARB'RY ALLEN", ...)) ?entity ?p ?o .
  
}
} 
ORDER BY ?entity ?p
```

### USER
Great, thanks. Can you relate the Session variants you found with specific variants from UTSI?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

Now I have a complete picture. Let me compile the final answer.

## Relating the Session "Barbara Allen" Tune to UTSI Variants

### The thesession Tune's Metadata

The tune `<https://thesession.org/tunes/9177>` ("Barbara Allen") has **3 settings** (tune variants), each with:

| Property | Wikidata ID | Value | Meaning |
|----------|-------------|-------|---------|
| **P136** (genre) | Q23637018 | Present on all 3 settings | Irish traditional music |
| **P3440** (time signature) | Q27955141 | Present on all 3 settings | Specific time signature |
| **P826** (mode) | Q283880 (settings 1,3) / Q283895 (setting 2) | Dorian / Aeolian | Musical mode |

The tune itself (parent entity) carries only: `rdfs:label "Barbara Allen"`, `rdf:type Tune`, and three `P747` (has setting) links.

---

### Direct Shared URI Overlap: **None**

I tested for shared Wikidata URI values across all properties (P136, P826, P3440) between the thesession tune settings and all 20 UTSI "Barbara Allen" entities. **No exact URI matches were found.** The reason:

| Property | Session Value | UTSI Values | Overlap? |
|----------|---------------|-------------|----------|
| **P136** (genre) | Q23637018 (Irish trad) | Q43343 (folk song), Q4797274 (narrative ballad), Q373342 (ballad) | **No** |
| **P826** (mode) | Q283880 (Dorian), Q283895 (Aeolian) | UTSI entities have **no P826 values** | **N/A** |
| **P3440** (time signature) | Q27955141 | UTSI entities have **no P3440 values** | **N/A** |
| **P86** (composer) | Not present on Session tune | Q86167 (traditional) on 18/20 UTSI entries | **N/A** (Session lacks this) |
| **P676** (subject/work) | Not present on Session tune | Q4233718 (Barbara Allen) on 17/20 UTSI entries | **N/A** (Session lacks this) |
| **P1922** (first line) | Not present on Session tune | Varies across UTSI entries | **N/A** (Session lacks this) |

The genre mismatch is notable: thesession classifies this as **Q23637018** (Irish traditional music), while UTSI classifies all its entries as **Q43343** (folk song). These are different — and not hierarchically related — Wikidata concepts.

---

### Indirect Connections: What Links Them Despite No Shared URIs

Despite the absence of direct URI overlap, there are **meaningful indirect connections** between the thesession tune and specific UTSI variants:

#### 1. Irish Geographic Connection → 3 UTSI Variants

The Session tune is typed as **Irish traditional music** (Q23637018). Three UTSI entries carry **P1071 = Q18389 (Ireland)** as their location of formation:

| UTSI Variant | First Line (P1922) | Collection (P361) |
|-------------|---------------------|---------------------|
| **BARB'RY ELLEN: BARBARA ALLEN** | IN LIM'RICK CITY HE WAS BROUGHT UP | Folk Songs of Old New England |
| **BARB'RY ELLEN; OR BARBARA ALLEN** | IN LIMRICK CITY HE WAS BROUGHT UP AND DUBLIN WAS HIS STATION | Folk Songs of Old New England |
| **BARBARA ALLEN** (aggregation entity) | (many first lines) | (many collections) |

These Irish-located UTSI variants share the ballad's **Irish transmission path** with the thesession tune, which is an Irish traditional music setting. The first lines referencing **Limerick and Dublin** place them squarely in the Irish tradition that thesession.org documents.

#### 2. "Barbara Allen" / "Barb'ry Ellen" Naming Convention

The thesession tune uses the title **"Barbara Allen"**. All 20 UTSI variants reference this same ballad by name, with variant spellings including "Barb'ry Ellen" and "Barb'ra Ellen" — all referring to the same folk work (Child Ballad 84). The labels themselves encode the relationship:

- "BARB'RY ELLEN ( BARBARA ALLEN )" — explicitly equates the Irish name with the standard name
- "BARB'RY ELLEN; OR BARBARA ALLEN" — the "OR" makes the synonymy explicit

#### 3. Traditional/Anonymous Attribution

While the thesession tune doesn't carry a P86 (composer) property, thesession.org is a database of **traditional Irish tunes** — implying traditional/anonymous origin. 18 of 20 UTSI entries carry **P86 = Q86167** (traditional), consistent with the same assumption.

#### 4. Shared Subject/Work (Q4233718) — Indirectly

17 of 20 UTSI entries link to **P676 = Q4233718** (the Wikidata item for "Barbara Allen" the ballad). The thesession tune does not carry P676, but the matching title "Barbara Allen" implies the same subject. If this property were added to the thesession tune, it would link directly to these same UTSI entries.

---

### Strongest Candidate Matches

Based on indirect evidence, the **3 most relatable UTSI variants** to the thesession tune are:

| # | UTSI Variant | Reason for Connection |
|---|-------------|----------------------|
| 1 | **BARB'RY ELLEN: BARBARA ALLEN** | Location = Ireland (Q18389); First line = "IN LIM'RICK CITY HE WAS BROUGHT UP"; Composer = traditional (Q86167); Subject = Barbara Allen (Q4233718) |
| 2 | **BARB'RY ELLEN; OR BARBARA ALLEN** | Location = Ireland (Q18389); First line = "IN LIMRICK CITY HE WAS BROUGHT UP AND DUBLIN WAS HIS STATION"; Composer = traditional (Q86167); Subject = Barbara Allen (Q4233718) |
| 3 | **BARB'RY ELLEN ( BARBARA ALLEN )** | Location = United States (Q30), but the title foregrounds the Irish name "Barb'ry Ellen"; First line = "IN SCARLET TOWN WHERE I WAS BORN"; Composer = traditional (Q86167); Subject = Barbara Allen (Q4233718) |

The first two are the strongest matches because their **Irish geographic origin** (P1071 = Q18389) aligns with the thesession tune's classification as **Irish traditional music** (P136 = Q23637018), and their first lines reference **Limerick and Dublin** — Irish cities — placing them in the same Irish ballad tradition.

---

### Why No Direct Links Exist

The two graphs model the same ballad at **different levels of description**:
- **thesession** models the **tune** (melody, mode, time signature) — what you *play*
- **UTSI** models the **song** (lyrics, first line, text, collection source) — what you *sing*

The thesession tune has **no lyrical metadata** (no P1922, no P676, no P86), and the UTSI entries have **no musical metadata** (no P826 mode, no P3440 time signature). The two systems capture complementary but non-overlapping facets of the same folk tradition. A proper cross-link would require either:
- Adding **P676 = Q4233718** (Barbara Allen) to the thesession tune, or
- Adding **P826** (mode) values to UTSI entries, or
- Creating explicit **owl:sameAs / skos:relatedMatch** links between the graphs
</details>

**Validating and executing SPARQL query**


Now I have a complete picture. Let me compile the final answer.

## Relating the Session "Barbara Allen" Tune to UTSI Variants

### The thesession Tune's Metadata

The tune `<https://thesession.org/tunes/9177>` ("Barbara Allen") has **3 settings** (tune variants), each with:

| Property | Wikidata ID | Value | Meaning |
|----------|-------------|-------|---------|
| **P136** (genre) | Q23637018 | Present on all 3 settings | Irish traditional music |
| **P3440** (time signature) | Q27955141 | Present on all 3 settings | Specific time signature |
| **P826** (mode) | Q283880 (settings 1,3) / Q283895 (setting 2) | Dorian / Aeolian | Musical mode |

The tune itself (parent entity) carries only: `rdfs:label "Barbara Allen"`, `rdf:type Tune`, and three `P747` (has setting) links.

---

### Direct Shared URI Overlap: **None**

I tested for shared Wikidata URI values across all properties (P136, P826, P3440) between the thesession tune settings and all 20 UTSI "Barbara Allen" entities. **No exact URI matches were found.** The reason:

| Property | Session Value | UTSI Values | Overlap? |
|----------|---------------|-------------|----------|
| **P136** (genre) | Q23637018 (Irish trad) | Q43343 (folk song), Q4797274 (narrative ballad), Q373342 (ballad) | **No** |
| **P826** (mode) | Q283880 (Dorian), Q283895 (Aeolian) | UTSI entities have **no P826 values** | **N/A** |
| **P3440** (time signature) | Q27955141 | UTSI entities have **no P3440 values** | **N/A** |
| **P86** (composer) | Not present on Session tune | Q86167 (traditional) on 18/20 UTSI entries | **N/A** (Session lacks this) |
| **P676** (subject/work) | Not present on Session tune | Q4233718 (Barbara Allen) on 17/20 UTSI entries | **N/A** (Session lacks this) |
| **P1922** (first line) | Not present on Session tune | Varies across UTSI entries | **N/A** (Session lacks this) |

The genre mismatch is notable: thesession classifies this as **Q23637018** (Irish traditional music), while UTSI classifies all its entries as **Q43343** (folk song). These are different — and not hierarchically related — Wikidata concepts.

---

### Indirect Connections: What Links Them Despite No Shared URIs

Despite the absence of direct URI overlap, there are **meaningful indirect connections** between the thesession tune and specific UTSI variants:

#### 1. Irish Geographic Connection → 3 UTSI Variants

The Session tune is typed as **Irish traditional music** (Q23637018). Three UTSI entries carry **P1071 = Q18389 (Ireland)** as their location of formation:

| UTSI Variant | First Line (P1922) | Collection (P361) |
|-------------|---------------------|---------------------|
| **BARB'RY ELLEN: BARBARA ALLEN** | IN LIM'RICK CITY HE WAS BROUGHT UP | Folk Songs of Old New England |
| **BARB'RY ELLEN; OR BARBARA ALLEN** | IN LIMRICK CITY HE WAS BROUGHT UP AND DUBLIN WAS HIS STATION | Folk Songs of Old New England |
| **BARBARA ALLEN** (aggregation entity) | (many first lines) | (many collections) |

These Irish-located UTSI variants share the ballad's **Irish transmission path** with the thesession tune, which is an Irish traditional music setting. The first lines referencing **Limerick and Dublin** place them squarely in the Irish tradition that thesession.org documents.

#### 2. "Barbara Allen" / "Barb'ry Ellen" Naming Convention

The thesession tune uses the title **"Barbara Allen"**. All 20 UTSI variants reference this same ballad by name, with variant spellings including "Barb'ry Ellen" and "Barb'ra Ellen" — all referring to the same folk work (Child Ballad 84). The labels themselves encode the relationship:

- "BARB'RY ELLEN ( BARBARA ALLEN )" — explicitly equates the Irish name with the standard name
- "BARB'RY ELLEN; OR BARBARA ALLEN" — the "OR" makes the synonymy explicit

#### 3. Traditional/Anonymous Attribution

While the thesession tune doesn't carry a P86 (composer) property, thesession.org is a database of **traditional Irish tunes** — implying traditional/anonymous origin. 18 of 20 UTSI entries carry **P86 = Q86167** (traditional), consistent with the same assumption.

#### 4. Shared Subject/Work (Q4233718) — Indirectly

17 of 20 UTSI entries link to **P676 = Q4233718** (the Wikidata item for "Barbara Allen" the ballad). The thesession tune does not carry P676, but the matching title "Barbara Allen" implies the same subject. If this property were added to the thesession tune, it would link directly to these same UTSI entries.

---

### Strongest Candidate Matches

Based on indirect evidence, the **3 most relatable UTSI variants** to the thesession tune are:

| # | UTSI Variant | Reason for Connection |
|---|-------------|----------------------|
| 1 | **BARB'RY ELLEN: BARBARA ALLEN** | Location = Ireland (Q18389); First line = "IN LIM'RICK CITY HE WAS BROUGHT UP"; Composer = traditional (Q86167); Subject = Barbara Allen (Q4233718) |
| 2 | **BARB'RY ELLEN; OR BARBARA ALLEN** | Location = Ireland (Q18389); First line = "IN LIMRICK CITY HE WAS BROUGHT UP AND DUBLIN WAS HIS STATION"; Composer = traditional (Q86167); Subject = Barbara Allen (Q4233718) |
| 3 | **BARB'RY ELLEN ( BARBARA ALLEN )** | Location = United States (Q30), but the title foregrounds the Irish name "Barb'ry Ellen"; First line = "IN SCARLET TOWN WHERE I WAS BORN"; Composer = traditional (Q86167); Subject = Barbara Allen (Q4233718) |

The first two are the strongest matches because their **Irish geographic origin** (P1071 = Q18389) aligns with the thesession tune's classification as **Irish traditional music** (P136 = Q23637018), and their first lines reference **Limerick and Dublin** — Irish cities — placing them in the same Irish ballad tradition.

---

### Why No Direct Links Exist

The two graphs model the same ballad at **different levels of description**:
- **thesession** models the **tune** (melody, mode, time signature) — what you *play*
- **UTSI** models the **song** (lyrics, first line, text, collection source) — what you *sing*

The thesession tune has **no lyrical metadata** (no P1922, no P676, no P86), and the UTSI entries have **no musical metadata** (no P826 mode, no P3440 time signature). The two systems capture complementary but non-overlapping facets of the same folk tradition. A proper cross-link would require either:
- Adding **P676 = Q4233718** (Barbara Allen) to the thesession tune, or
- Adding **P826** (mode) values to UTSI entries, or
- Creating explicit **owl:sameAs / skos:relatedMatch** links between the graphs

### USER
The Session does not have lyrics or first lines?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

## Answer

**No, the thesession graph contains no lyrics, first lines of text, or any lyrical properties whatsoever — neither for "Barbara Allen" nor for any tune in the entire graph.**

### Evidence

**1. "Barbara Allen" tune (`https://thesession.org/tunes/9177`)** — all properties:

| Property | Value |
|----------|-------|
| rdf:type | Tune |
| rdfs:label | Barbara Allen |
| P747 (has setting) | #setting19940, #setting19941, #setting9177 |

No P1922 or any lyric-related property.

**2. Its 3 settings** — all properties:

| Property | Value(s) | Meaning |
|----------|----------|---------|
| rdf:type | TuneSetting | Type |
| P826 | Q283880 (Dorian), Q283895 (Aeolian) | Mode |
| P136 | Q23637018 | Genre (Irish trad) |
| P3440 | Q27955141 | Time signature |

No P1922 or any lyric-related property on any setting.

**3. Complete property inventory of the entire thesession graph** — all 19 predicates:

| Property | Count | Meaning |
|----------|-------|---------|
| P527 | 221,033 | Has part |
| rdf:type | 188,748 | Type |
| P658 | 132,203 | Tracklist |
| P571 | 88,020 | Inception/date |
| P170 | 88,020 | Creator |
| P747 | 51,350 | Has setting |
| P3440 | 51,350 | Time signature |
| P136 | 49,305 | Genre |
| rdfs:label | 47,343 | Label |
| P826 | 40,872 | Mode |
| skos:altLabel | 28,849 | Alternate label |
| P131 | 11,139 | Located in |
| P625 | 9,982 | Coordinates |
| P276 | 9,499 | Location |
| P17 | 9,488 | Country |
| P580 | 7,947 | Start time |
| P582 | 7,947 | End time |
| P175 | 7,644 | Performer |
| P2888 | 1,423 | See also |

**P1922 (first line of text) does not appear anywhere.** The thesession graph models tunes purely as **melodic entities** — with mode, time signature, genre, and membership in tune sets — and carries no textual/lyrical metadata at all. This contrasts sharply with UTSI, where every song carries P1922 (first line of text), P86 (composer), P676 (subject/work), P407 (language), and P1071 (location of formation).

### SPARQL Queries Used

**Tune properties:**
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
SELECT ?p ?o
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/thesession/> {
    <https://thesession.org/tunes/9177> ?p ?o .
  }
}
```

**Setting properties:**
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
SELECT ?setting ?p ?o
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/thesession/> {
    <https://thesession.org/tunes/9177> <http://www.wikidata.org/prop/direct/P747> ?setting .
    ?setting ?p ?o .
  }
}
```

**Full graph property inventory:**
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
SELECT DISTINCT ?p (COUNT(*) AS ?cnt)
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/thesession/> {
    ?s ?p ?o .
  }
}
GROUP BY ?p
ORDER BY DESC(?cnt)
```
</details>

**Validating and executing SPARQL query**


## Answer

**No, the thesession graph contains no lyrics, first lines of text, or any lyrical properties whatsoever — neither for "Barbara Allen" nor for any tune in the entire graph.**

### Evidence

**1. "Barbara Allen" tune (`https://thesession.org/tunes/9177`)** — all properties:

| Property | Value |
|----------|-------|
| rdf:type | Tune |
| rdfs:label | Barbara Allen |
| P747 (has setting) | #setting19940, #setting19941, #setting9177 |

No P1922 or any lyric-related property.

**2. Its 3 settings** — all properties:

| Property | Value(s) | Meaning |
|----------|----------|---------|
| rdf:type | TuneSetting | Type |
| P826 | Q283880 (Dorian), Q283895 (Aeolian) | Mode |
| P136 | Q23637018 | Genre (Irish trad) |
| P3440 | Q27955141 | Time signature |

No P1922 or any lyric-related property on any setting.

**3. Complete property inventory of the entire thesession graph** — all 19 predicates:

| Property | Count | Meaning |
|----------|-------|---------|
| P527 | 221,033 | Has part |
| rdf:type | 188,748 | Type |
| P658 | 132,203 | Tracklist |
| P571 | 88,020 | Inception/date |
| P170 | 88,020 | Creator |
| P747 | 51,350 | Has setting |
| P3440 | 51,350 | Time signature |
| P136 | 49,305 | Genre |
| rdfs:label | 47,343 | Label |
| P826 | 40,872 | Mode |
| skos:altLabel | 28,849 | Alternate label |
| P131 | 11,139 | Located in |
| P625 | 9,982 | Coordinates |
| P276 | 9,499 | Location |
| P17 | 9,488 | Country |
| P580 | 7,947 | Start time |
| P582 | 7,947 | End time |
| P175 | 7,644 | Performer |
| P2888 | 1,423 | See also |

**P1922 (first line of text) does not appear anywhere.** The thesession graph models tunes purely as **melodic entities** — with mode, time signature, genre, and membership in tune sets — and carries no textual/lyrical metadata at all. This contrasts sharply with UTSI, where every song carries P1922 (first line of text), P86 (composer), P676 (subject/work), P407 (language), and P1071 (location of formation).

### SPARQL Queries Used

**Tune properties:**

**Setting properties:**

**Full graph property inventory:**

The SPARQL has been executed:
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
SELECT ?p ?o 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/thesession/> {
  <https://thesession.org/tunes/9177> ?p ?o .
  
}
} 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
SELECT ?setting ?p ?o 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/thesession/> {
  <https://thesession.org/tunes/9177> <http://www.wikidata.org/prop/direct/P747> ?setting .
   ?setting ?p ?o .
  
}
} 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
SELECT DISTINCT ?p (COUNT(*) AS ?cnt) 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/thesession/> {
  ?s ?p ?o .
  
}
} 
GROUP BY ?p 
ORDER BY DESC(?cnt)
```

### USER
PLease search Global Jukebox for Barbara Ellen

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

User messages are aligned with the knowledge graph: LinkedMusic
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

## Results

**No entities with the exact phrase "Barbara Ellen" exist in the Global Jukebox graph.** However, searching for the related spelling "Barbara Allen" returns **2 Song entities**, both carrying the label "Barbara Allen." I also searched for "Barb'ry Ellen" and any label matching `barb.*ell` — both returned zero results. The Global Jukebox uses the "Allen" spelling exclusively.

---

### Entity 1: `https://theglobaljukebox.org/song/9409`

| Property | Wikidata ID | Value | Meaning |
|----------|-------------|-------|---------|
| rdf:type | — | `theglobaljukebox/Song` | Song |
| rdfs:label | — | Barbara Allen | Title |
| P10893 | — | Charles Seeger | Collector |
| P136 | Q1077388 | (ballad genre) | Genre |
| P175 | — | Rebecca Tarwater | Performer |
| P2341 | — | Rockwood | Location/Region |
| P2596 | — | culture/18349 → **Appalachia** | Culture |
| P495 | Q948 | (Tennessee) | Country |
| P585 | — | 1936-01-01 | Recording date |
| P870 | Q54285818 | (vocal) | Instrument |

**Culture details (Appalachia):** altLabel "Country"; P17 = Q30 (United States); P2341 = Q2673740 (Appalachia); languages = Q3802476, Q6144345, "Southern American English"; P361 = "Appalachian White"; P4970 = "Country".

---

### Entity 2: `https://theglobaljukebox.org/song/9410`

| Property | Wikidata ID | Value | Meaning |
|----------|-------------|-------|---------|
| rdf:type | — | `theglobaljukebox/Song` | Song |
| rdfs:label | — | Barbara Allen | Title |
| P10893 | — | Alan Lomax | Collector |
| P10893 | — | Harnish Henderson | Collector |
| P10893 | — | William Montgomerie | Collector |
| P10893 | — | the MacLeans of Raasay | Collector |
| P136 | Q1077388 | (ballad genre) | Genre |
| P136 | Q380233 | (folk song genre) | Genre |
| P175 | — | Jessie Murray | Performer |
| P2341 | — | Buchan | Location/Region |
| P2596 | — | culture/25071 → **Aberdeen** | Culture |
| P495 | Q230791 | (Scotland) | Country |
| P585 | — | 1950s | Recording date |
| P870 | Q54285818 | (vocal) | Instrument |

**Culture details (Aberdeen):** altLabel "Scotland"; P17 = Q230791 (Scotland); P2341 = Q22 (Scotland), Q189912 (Aberdeenshire), "Aberdeenshire", "Aberdeenshire, E Scotland"; P2888 = Q36405; languages = Q14549 (Scots/Doric), "Scots (also known as Doric)"; P361 = Q111955286, "Lowland Scots"; P4970 = "Scotland".

---

### SPARQL Queries Used

**1. Label search for "barbara ellen" (case-insensitive):**
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
SELECT ?entity ?label
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
    ?entity rdfs:label ?label .
    FILTER(CONTAINS(LCASE(STR(?label)), "barbara ellen"))
  }
}
LIMIT 50
```
→ **0 results**

**2. Label search for "barbara allen" (case-insensitive):**
```sparql
SELECT ?entity ?label
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
    ?entity rdfs:label ?label .
    FILTER(CONTAINS(LCASE(STR(?label)), "barbara allen"))
  }
}
LIMIT 50
```
→ **2 results**

**3. Full property retrieval for both entities:**
```sparql
SELECT ?entity ?p ?o
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
    VALUES ?entity { <https://theglobaljukebox.org/song/9409> <https://theglobaljukebox.org/song/9410> }
    ?entity ?p ?o .
  }
}
ORDER BY ?entity ?p
```
→ **24 triples** (11 for song/9409, 13 for song/9410)

**4. Culture entity details:**
```sparql
SELECT ?culture ?p ?o
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
    VALUES ?culture {
      <https://theglobaljukebox.org/culture/18349>
      <https://theglobaljukebox.org/culture/25071>
    }
    ?culture ?p ?o .
  }
}
ORDER BY ?culture ?p
```
→ **26 triples** (11 for Appalachia, 15 for Aberdeen)

---

### Summary

The Global Jukebox contains **no entities with "Barbara Ellen"** in their label. It has **2 entities labeled "Barbara Allen"** — one an **Appalachian** recording from 1936 (performer: Rebecca Tarwater, collector: Charles Seeger, in Rockwood, Tennessee) and one a **Scottish** recording from the 1950s (performer: Jessie Murray, collectors: Alan Lomax, Harnish Henderson, William Montgomerie, and the MacLeans of Raasay, in Buchan/Aberdeenshire, Scotland). Both are vocal ballads (P136 = Q1077388), with the Scottish variant also tagged as a folk song (Q380233).
</details>

**Validating and executing SPARQL query**


## Results

**No entities with the exact phrase "Barbara Ellen" exist in the Global Jukebox graph.** However, searching for the related spelling "Barbara Allen" returns **2 Song entities**, both carrying the label "Barbara Allen." I also searched for "Barb'ry Ellen" and any label matching `barb.*ell` — both returned zero results. The Global Jukebox uses the "Allen" spelling exclusively.

---

### Entity 1: `https://theglobaljukebox.org/song/9409`

| Property | Wikidata ID | Value | Meaning |
|----------|-------------|-------|---------|
| rdf:type | — | `theglobaljukebox/Song` | Song |
| rdfs:label | — | Barbara Allen | Title |
| P10893 | — | Charles Seeger | Collector |
| P136 | Q1077388 | (ballad genre) | Genre |
| P175 | — | Rebecca Tarwater | Performer |
| P2341 | — | Rockwood | Location/Region |
| P2596 | — | culture/18349 → **Appalachia** | Culture |
| P495 | Q948 | (Tennessee) | Country |
| P585 | — | 1936-01-01 | Recording date |
| P870 | Q54285818 | (vocal) | Instrument |

**Culture details (Appalachia):** altLabel "Country"; P17 = Q30 (United States); P2341 = Q2673740 (Appalachia); languages = Q3802476, Q6144345, "Southern American English"; P361 = "Appalachian White"; P4970 = "Country".

---

### Entity 2: `https://theglobaljukebox.org/song/9410`

| Property | Wikidata ID | Value | Meaning |
|----------|-------------|-------|---------|
| rdf:type | — | `theglobaljukebox/Song` | Song |
| rdfs:label | — | Barbara Allen | Title |
| P10893 | — | Alan Lomax | Collector |
| P10893 | — | Harnish Henderson | Collector |
| P10893 | — | William Montgomerie | Collector |
| P10893 | — | the MacLeans of Raasay | Collector |
| P136 | Q1077388 | (ballad genre) | Genre |
| P136 | Q380233 | (folk song genre) | Genre |
| P175 | — | Jessie Murray | Performer |
| P2341 | — | Buchan | Location/Region |
| P2596 | — | culture/25071 → **Aberdeen** | Culture |
| P495 | Q230791 | (Scotland) | Country |
| P585 | — | 1950s | Recording date |
| P870 | Q54285818 | (vocal) | Instrument |

**Culture details (Aberdeen):** altLabel "Scotland"; P17 = Q230791 (Scotland); P2341 = Q22 (Scotland), Q189912 (Aberdeenshire), "Aberdeenshire", "Aberdeenshire, E Scotland"; P2888 = Q36405; languages = Q14549 (Scots/Doric), "Scots (also known as Doric)"; P361 = Q111955286, "Lowland Scots"; P4970 = "Scotland".

---

### SPARQL Queries Used

**1. Label search for "barbara ellen" (case-insensitive):**
→ **0 results**

**2. Label search for "barbara allen" (case-insensitive):**
→ **2 results**

**3. Full property retrieval for both entities:**
→ **24 triples** (11 for song/9409, 13 for song/9410)

**4. Culture entity details:**
→ **26 triples** (11 for Appalachia, 15 for Aberdeen)

---

### Summary

The Global Jukebox contains **no entities with "Barbara Ellen"** in their label. It has **2 entities labeled "Barbara Allen"** — one an **Appalachian** recording from 1936 (performer: Rebecca Tarwater, collector: Charles Seeger, in Rockwood, Tennessee) and one a **Scottish** recording from the 1950s (performer: Jessie Murray, collectors: Alan Lomax, Harnish Henderson, William Montgomerie, and the MacLeans of Raasay, in Buchan/Aberdeenshire, Scotland). Both are vocal ballads (P136 = Q1077388), with the Scottish variant also tagged as a folk song (Q380233).

The SPARQL has been executed:
```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#> 
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> 
SELECT ?entity ?label 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
  ?entity rdfs:label ?label .
   
FILTER(CONTAINS(LCASE(STR(?label)), "barbara ellen"))
}
} 
LIMIT 50 
SELECT ?entity ?label 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
  ?entity rdfs:label ?label .
   
FILTER(CONTAINS(LCASE(STR(?label)), "barbara allen"))
}
} 
LIMIT 50 
SELECT ?entity ?p ?o 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
  VALUES ?entity {
  <https://theglobaljukebox.org/song/9409> <https://theglobaljukebox.org/song/9410>
} ?entity ?p ?o .
  
}
} 
ORDER BY ?entity ?p 
SELECT ?culture ?p ?o 
WHERE {
  GRAPH <https://linkedmusic.ca/graphs/theglobaljukebox/> {
  VALUES ?culture {
  <https://theglobaljukebox.org/culture/18349> <https://theglobaljukebox.org/culture/25071>
} ?culture ?p ?o .
  
}
} 
ORDER BY ?culture ?p
```

### USER
Can you give me the GJB song numbers for the two songs you found?

### ASSISTANT
Based on the results from the previous search, the two Global Jukebox song numbers are:

| Song | GJB Song Number | URI |
|------|----------------|-----|
| Barbara Allen (Appalachian) | **9409** | `https://theglobaljukebox.org/song/9409` |
| Barbara Allen (Scottish) | **9410** | `https://theglobaljukebox.org/song/9410` |

These numbers come directly from the URIs of the two entities found in the Global Jukebox graph.

### USER
9410 seems to have several variants, can you see that?

### ASSISTANT
**Selecting knowledge graph(s)**


<details>
<summary>Result from Selecting knowledge graph(s)</summary>

Ask the user which knowledge graph would they want me to query: EHRI-KG or PHAROS?
</details>

**Querying knowledge graph**


<details>
<summary>Result from Querying knowledge graph</summary>

Now I have a complete picture. Let me compile the final answer.

## Answer

**Global Jukebox song 9410 has no explicit variant, setting, or alternative-version links within the GJB graph.** There are no P747 (has setting), P527 (has part), P2888 (see also), P361 (part of), P144 (based on), or P4340 properties on this entity. No other entity links *to* song 9410 either (zero incoming triples). However, several **implicitly related songs** can be identified through shared properties.

---

### Direct Link Properties on Song 9410

| Property | Value | Meaning |
|----------|-------|---------|
| P10893 | Alan Lomax | Collector |
| P10893 | Harnish Henderson | Collector |
| P10893 | William Montgomerie | Collector |
| P10893 | the MacLeans of Raasay | Collector |
| P136 | Q1077388 | Genre: Ballad |
| P136 | Q380233 | Genre: Folk song |
| P175 | Jessie Murray | Performer |
| P2341 | Buchan | Location |
| P2596 | culture/25071 | Culture: Aberdeen |
| P495 | Q230791 | Country: Scotland |
| P585 | 1950s | Recording date |
| P870 | Q54285818 | Instrument: Vocal |

**No P747, P527, P2888, P361, P144, or P4340 values exist.**

---

### The Closest Relative: Song 9409 (same title)

| Property | Song 9409 | Song 9410 |
|----------|-----------|-----------|
| Label | Barbara Allen | Barbara Allen |
| Culture | **Appalachia** (18349) | **Aberdeen** (25071) |
| Country | Tennessee (Q948) | Scotland (Q230791) |
| Performer | Rebecca Tarwater | Jessie Murray |
| Collector | Charles Seeger | Alan Lomax, Harnish Henderson, William Montgomerie, the MacLeans of Raasay |
| Date | 1936 | 1950s |
| Genre | Q1077388 (ballad) | Q1077388 (ballad) + Q380233 (folk song) |
| Location | Rockwood | Buchan |
| Instrument | Q54285818 (vocal) | Q54285818 (vocal) |

These are the **only two** songs in the entire GJB graph with the label "Barbara Allen." They share genre (Q1077388) and instrument (vocal) but come from **completely different cultural traditions** (Appalachian vs. Scottish). No label variants like "Barb'ry Ellen" or "Barbara Ellen" exist in GJB.

---

### Songs Sharing the Same Culture (Aberdeen / culture/25071)

| Song | Label | Performer | Genre | Date |
|------|-------|-----------|-------|------|
| **song/9332** | Glenlogie | John Strachan | Q1077388 (ballad) | 1951 |
| **song/9474** | The Twa Sisters | John Strachan | Q1077388 (ballad) | 1951 |
| **song/2304** | The Bonny Wee Lassie Who Never Said No | — | — | — |

Songs 9332 and 9474 are particularly close to 9410: same culture, same country, same collectors (all four), same date, same instrument — differing only in performer (John Strachan vs. Jessie Murray) and location (Fyvie vs. Buchan).

---

### Songs Sharing the Same Collectors (Henderson, Montgomerie, MacLeans of Raasay)

All three of these collectors appear on exactly the same set of 4 songs:

| Song | Label | Culture | Performer | Location |
|------|-------|---------|-----------|----------|
| **song/9410** | Barbara Allen | Aberdeen (25071) | Jessie Murray | Buchan |
| **song/9332** | Glenlogie | Aberdeen (25071) | John Strachan | Fyvie |
| **song/9474** | The Twa Sisters | Aberdeen (25071) | John Strachan | Fyvie |
| **song/2305** | Tail Toddle | culture/50244 | Hamish Henderson | Glenshee |

These four songs form a **tight cluster** — all were collected by the same Scottish fieldwork team (Henderson + Montgomerie + MacLeans + Lomax) in the early 1950s in northeastern Scotland.

---

### Scottish Ballads (same genre Q1077388 + country Q230791)

| Song | Label |
|------|-------|
| song/2302 | The Bonnie Lass O' Fyvie |
| song/2304 | The Bonny Wee Lassie Who Never Said No |
| song/2306 | Sleepytoon |
| song/785 | Lord Lovell |
| song/9332 | Glenlogie |
| song/9412 | The Dowie Dens of Yarrow |
| song/9474 | The Twa Sisters |

These 7 songs (plus song 9410 itself = 8 total) share the ballad genre and Scottish origin. Several are well-known Child Ballads alongside "Barbara Allen" (Child 84): "The Twa Sisters" (Child 10), "Lord Lovell" (Child 75), "The Dowie Dens of Yarrow" (Child 214), "Glenlogie" (Child 238).

---

### Performer "Jessie Murray"

Jessie Murray appears as performer on **only one song** in the entire GJB graph: song 9410 itself. No other GJB songs share this performer.

---

### Summary

| Relationship Type | Found? | Details |
|-------------------|--------|---------|
| **P747 (has setting)** | **No** | Not present on song 9410 |
| **P527 (has part)** | **No** | Not present |
| **P2888 (see also)** | **No** | Not present |
| **P361 (part of)** | **No** | Not present |
| **P144 (based on)** | **No** | Not present |
| **Incoming links from other entities** | **No** | Zero triples point to song 9410 |
| **Same-label songs ("Barbara Allen")** | **Yes — 1** | song/9409 (Appalachian variant) |
| **Same-culture songs (Aberdeen)** | **Yes — 3** | Glenlogie, The Twa Sisters, The Bonny Wee Lassie… |
| **Same-collector cluster** | **Yes — 3** | Glenlogie, The Twa Sisters, Tail Toddle |
| **Same genre+country (Scottish ballads)** | **Yes — 7** | See table above |
| **Same performer** | **No** | Jessie Murray is unique to song 9410 |
| **Label variants ("Barb'ry Ellen", etc.)** | **No** | GJB uses only "Barbara Allen" spelling |

**Bottom line:** Song 9410 has **no explicit variant/setting/alternative-version relationships** in the GJB graph. Its closest implicit relatives are the other 3 songs from the same Scottish fieldwork collection (Glenlogie, The Twa Sisters, Tail Toddle), the Appalachian "Barbara Allen" (song/9409), and the broader cluster of Scottish ballads. The absence of P747, P527, P2888, or any inter-entity links means the graph does not encode variant relationships — these must be inferred from shared collectors, culture, genre, and geography.
</details>

**Validating and executing SPARQL query**


## Answer

**Global Jukebox song 9410 has no explicit variant, setting, or alternative-version links within the GJB graph.** There are no P747 (has setting), P527 (has part), P2888 (see also), P361 (part of), P144 (based on), or P4340 properties on this entity. No other entity links *to* song 9410 either (zero incoming triples). However, several **implicitly related songs** can be identified through shared properties.

---

### Direct Link Properties on Song 9410

| Property | Value | Meaning |
|----------|-------|---------|
| P10893 | Alan Lomax | Collector |
| P10893 | Harnish Henderson | Collector |
| P10893 | William Montgomerie | Collector |
| P10893 | the MacLeans of Raasay | Collector |
| P136 | Q1077388 | Genre: Ballad |
| P136 | Q380233 | Genre: Folk song |
| P175 | Jessie Murray | Performer |
| P2341 | Buchan | Location |
| P2596 | culture/25071 | Culture: Aberdeen |
| P495 | Q230791 | Country: Scotland |
| P585 | 1950s | Recording date |
| P870 | Q54285818 | Instrument: Vocal |

**No P747, P527, P2888, P361, P144, or P4340 values exist.**

---

### The Closest Relative: Song 9409 (same title)

| Property | Song 9409 | Song 9410 |
|----------|-----------|----------|
| Label | Barbara Allen | Barbara Allen |
| Culture | **Appalachia** (18349) | **Aberdeen** (25071) |
| Country | Tennessee (Q948) | Scotland (Q230791) |
| Performer | Rebecca Tarwater | Jessie Murray |
| Collector | Charles Seeger | Alan Lomax, Harnish Henderson, William Montgomerie, the MacLeans of Raasay |
| Date | 1936 | 1950s |
| Genre | Q1077388 (ballad) | Q1077388 (ballad) + Q380233 (folk song) |
| Location | Rockwood | Buchan |
| Instrument | Q54285818 (vocal) | Q54285818 (vocal) |

These are the **only two** songs in the entire GJB graph with the label "Barbara Allen." They share genre (Q1077388) and instrument (vocal) but come from **completely different cultural traditions** (Appalachian vs. Scottish). No label variants like "Barb'ry Ellen" or "Barbara Ellen" exist in GJB.

---

### Songs Sharing the Same Culture (Aberdeen / culture/25071)

| Song | Label | Performer | Genre | Date |
|------|-------|-----------|-------|------|
| **song/9332** | Glenlogie | John Strachan | Q1077388 (ballad) | 1951 |
| **song/9474** | The Twa Sisters | John Strachan | Q1077388 (ballad) | 1951 |
| **song/2304** | The Bonny Wee Lassie Who Never Said No | — | — | — |

Songs 9332 and 9474 are particularly close to 9410: same culture, same country, same collectors (all four), same date, same instrument — differing only in performer (John Strachan vs. Jessie Murray) and location (Fyvie vs. Buchan).

---

### Songs Sharing the Same Collectors (Henderson, Montgomerie, MacLeans of Raasay)

All three of these collectors appear on exactly the same set of 4 songs:

| Song | Label | Culture | Performer | Location |
|------|-------|---------|-----------|----------|
| **song/9410** | Barbara Allen | Aberdeen (25071) | Jessie Murray | Buchan |
| **song/9332** | Glenlogie | Aberdeen (25071) | John Strachan | Fyvie |
| **song/9474** | The Twa Sisters | Aberdeen (25071) | John Strachan | Fyvie |
| **song/2305** | Tail Toddle | culture/50244 | Hamish Henderson | Glenshee |

These four songs form a **tight cluster** — all were collected by the same Scottish fieldwork team (Henderson + Montgomerie + MacLeans + Lomax) in the early 1950s in northeastern Scotland.

---

### Scottish Ballads (same genre Q1077388 + country Q230791)

| Song | Label |
|------|-------|
| song/2302 | The Bonnie Lass O' Fyvie |
| song/2304 | The Bonny Wee Lassie Who Never Said No |
| song/2306 | Sleepytoon |
| song/785 | Lord Lovell |
| song/9332 | Glenlogie |
| song/9412 | The Dowie Dens of Yarrow |
| song/9474 | The Twa Sisters |

These 7 songs (plus song 9410 itself = 8 total) share the ballad genre and Scottish origin. Several are well-known Child Ballads alongside "Barbara Allen" (Child 84): "The Twa Sisters" (Child 10), "Lord Lovell" (Child 75), "The Dowie Dens of Yarrow" (Child 214), "Glenlogie" (Child 238).

---

### Performer "Jessie Murray"

Jessie Murray appears as performer on **only one song** in the entire GJB graph: song 9410 itself. No other GJB songs share this performer.

---

### Summary

| Relationship Type | Found? | Details |
|-------------------|--------|--------|
| **P747 (has setting)** | **No** | Not present on song 9410 |
| **P527 (has part)** | **No** | Not present |
| **P2888 (see also)** | **No** | Not present |
| **P361 (part of)** | **No** | Not present |
| **P144 (based on)** | **No** | Not present |
| **Incoming links from other entities** | **No** | Zero triples point to song 9410 |
| **Same-label songs ("Barbara Allen")** | **Yes — 1** | song/9409 (Appalachian variant) |
| **Same-culture songs (Aberdeen)** | **Yes — 3** | Glenlogie, The Twa Sisters, The Bonny Wee Lassie… |
| **Same-collector cluster** | **Yes — 3** | Glenlogie, The Twa Sisters, Tail Toddle |
| **Same genre+country (Scottish ballads)** | **Yes — 7** | See table above |
| **Same performer** | **No** | Jessie Murray is unique to song 9410 |
| **Label variants ("Barb'ry Ellen", etc.)** | **No** | GJB uses only "Barbara Allen" spelling |

**Bottom line:** Song 9410 has **no explicit variant/setting/alternative-version relationships** in the GJB graph. Its closest implicit relatives are the other 3 songs from the same Scottish fieldwork collection (Glenlogie, The Twa Sisters, Tail Toddle), the Appalachian "Barbara Allen" (song/9409), and the broader cluster of Scottish ballads. The absence of P747, P527, P2888, or any inter-entity links means the graph does not encode variant relationships — these must be inferred from shared collectors, culture, genre, and geography.

### USER
Can you search GoTriple for publications on Barbara Allen?

### ASSISTANT
**search_documents**


<details>
<summary>Result from search_documents</summary>

{'type': 'text', 'text': '**Results: 1/2597 pages (64912 total)**\n### Barbara Allen ; Cruelty of Barbara Allen; Barbaro Ellen; Barb\'ry Allen ; Bonny Barbara Allen; Barbara Ellen\n- **ID:** ftunivarkansasdc:oai:digitalcollections.uark.edu:OzarkFolkSong/1517\n- **DOI:** \n- **Authors:** Smith, Oscar\n- **Date:** 1959-07-22\n- **Type:** other\n- **Languages:** en\n- **Publisher:** University of Arkansas Libraries, Fayetteville\n- **Access:** acr_open-access\n- **Topics:** hist, art\n- **Keywords:** a capella singing, Death, Love, Emotions, Burial, burials, London, Death of a Lover, Grief, Grave\n\nvoice ; Collected by Helen McAllister and Sung by Oscar Smith Sue Holley Westville, Oklahoma For Mary Celestia Parler July 22, 1959 Transcribed by Helen McAllister and Sue Holley Reel 289, Item 6 Barbara Allen In London town where I was born There was a fair maid dwelling Made every youth cry well I\'ll wait For the love of Barbara Allen. He sent his servant to the town Where Barbara was a dwelling master\'s sick and calls for thee If your name be Barbara Allen. And death is painted on his face And o\'er his heart is stealing Then hasten away to comfort him Oh, lovely Barbara Allen. So slowly, slowly she got up And slowly she came nigh him And all she said when she got there Young man I think you\'re dying. Oh yes I\'m sick and very sick And death is on me dwelling No better no better I never shall be If I can\'t have Barbara Allen. Oh yes you\'re sick and very sick And death is on your dwelling No better no better you never will be For you can\'t have Barbara Allen. Oh don\'t you remember in yonder town When you were at the tavern You drank the health of the ladies all around And slighted Barbara Allen. (Cont\'d)Barbara Allen Reel 289, Item 6 Continued Oh yes I remember in yonder town In yonder town a drinking I drank to the health of the ladies all around Gave my heart to Barbara Allen. As she was on her highway home The birds they kept a singing They sang so clear they seem to say Hard-hearted Barbara Allen. As she was walking o\'er the fields She heard the death bells tolling And every stroke did seem to say Hard-hearted Barbara Allen. She looked to the East, she looked to the West She spyed his corpse a coming Lay down, lay down that corpse of clay That I may look upon him. The more she looked the more she mourned Till she fell to the ground a crying Saying take me up and carry me home For I am now a dying. Oh mother, oh mother, go make my bed Go make it long and narrow Sweet William died for pure pure love And I shall die for sorrow. Oh father, oh father, go dig my grave Go dig it long and narrow Sweet William died ...\n---\n### Barbara Allen ; Cruelty of Barbara Allen; Barbaro Ellen; Barb\'ry Allen ; Bonny Barbara Allen; Barbara Ellen; Barbry Allen; Bonny Barbara Allan; Barbry Allen ; In Scarlet town, where I was born\n- **ID:** ftunivarkansasdc:oai:digitalcollections.uark.edu:OzarkFolkSong/3123\n- **DOI:** \n- **Authors:** Crymes, Jim, Mrs.\n- **Date:** 1954-06-15\n- **Type:** other\n- **Languages:** en\n- **Publisher:** University of Arkansas Libraries, Fayetteville\n- **Access:** acr_open-access\n- **Topics:** hisphilso, socio\n- **Keywords:** a capella singing, Death, Love, Rejection (Psychology), Burial, Wisdom, rejection, burials, Death of a Lover, Grave, Warning\n\nvoice ; Coll. by Mary Jo Davis For M. C. Parler Sung by Mrs. Jim Crymes DeValls Bluff, Arkansas June 15, 1954 Reel 193 Item 4 Barbara Allen In Scarlet town, where I was born, There was a fair maid dwelling, And every youth cried well away, Her name was Barbara Allen. All in the merry month of May, When the green buds were swelling, Young Jimmy Graves on his deathbed lay, For the love of Barbara Allen. He sent his men unto them, To the town where she was dwelling, Saying you must to my master come, If your name be Barbara Allen. For death is printed on his face, And o\'er his heart is stealing, Then haste to comfort him, Oh lovely Barbara Allen. Though death be printed on his face, And o\'er his heart is stealing, Yet little better he will be, For bonny Barbara Allen. So slowly, slowly she came up, And slowly she came nigh him, And all she waid when she came there, Young man, I think you\'re dying. He turned his face toward her straight, With deathly sorrow sighing, Oh pity me, come pity me, I\'m on my death bed lying. If on your deathbed you do lie, What need the tales your telling, I cannot keep you from your death, Farewell, said Barbara Allen. He turned his face toward the wall, And death was with him dwelling, Adieu, adieu, my friends adieu, Adieu to Barbara Allen. As she was walking o\'er the fields, She heard the bells a\'tumming, And every stroke did seem to say, Unworthy Barbara Allen. Reel 193, Item 4, cont\'d. Mrs. Jim Crymes singing, Barbara Allen She turned her body \'round and about, And spied the corpse a\'coming, Lie down, lie down, the corpse she said, That I may look upon him. With scornful eyes, she looked down, Her cheeks with laughter swelling, While all her friends cried out amazed, Unworthy, Barbara Allen. When he was dead and in his grave, His (her) heart was wound with sorrow, Oh mother, mother make my bed, For I shall die tomorrow. Hardhearted creature him to slight, Who loved me so, so dearly, Oh that I\'d been more kind to him, When he was alive and near me, And on her deathbed as she lay, ...\n---\n### Barbara Allen ; Cruelty of Barabara Allen; Barbro Ellen; Barb\'ry Allen ; Bonny Barbara Allen; Barbara Ellen; Barbry Allen ; "Sweet Willie\'s sick, and very sick\n- **ID:** ftunivarkansasdc:oai:digitalcollections.uark.edu:OzarkFolkSong/716\n- **DOI:** \n- **Authors:** Minnick, Betty, Briscoe, Mary\n- **Date:** 1951-05-01\n- **Type:** other\n- **Languages:** en\n- **Publisher:** University of Arkansas Libraries, Fayetteville\n- **Access:** acr_open-access\n- **Topics:** hist, art\n- **Keywords:** a capella singing, Death, Emotions, Burial, burials, Death of a lover, Grief, Grave, Easter\n\nvoice ; Reel 115 Mrs. Betty Minnick (And Mrs. Mary Briscoe) High, Arkansas May 1, 1951 Collected by Irene Carlisle Reel 115 Item 1 BARBARA ALLEN "Sweet Willie\'s sick, and very sick, And sent for you, Barbara Allen; Kb better will he ever be If he don\'t get Barbary Ellen" So slowly, slowly she arose, And slowly she went traveling; And all she said when she got there: "Young man, I think you\'re a-dying." "I know I\'m sick, and very sick, And death is on me dwelling; No better will I ever be, If I don\'t get Barbro Allen." "Don\'t you recollect that long summer day, "While we \'as setting at the tavern, You passed the wine to the ladies all around; You slighted Barbry Allen." "Yes, I recollect that long summer day, while we \'as setting at the tavern; I passed the wine to the ladies all around; Give my heart to Barbry Allen." She turned herself all around and about; She came downstairs a-smiling, Baying, "I might \'a\' saved that young man\'s l i f e, If I had been a-trying." He turned his pale face up to the wall, And he bursted out to crying, Saying, "I will die with pure hard love; Barbry Allen shall die with sorrow." She had not got one mile from town Till she heared the death-bell a-ringing; with ever\' stroke it seemed to say, "Hard-hearted Barbry Allen!" She had not got three miles from town Till she spied the corpse a-coming; "Go bring him here and lay him dawn, And let me look upon him." (MORE) Barbara Allen Reel 115 Minnick 2 The more she looked, the harder she looked, And she bursted out to crying; "Sweet William died for me today, And I shall die tomorrow." Oh, Willie died on Saturday night; Barbara Ellen on Easter Sunday; The good old mother for the sake of the both, She died on Easter Monday. They planted a rose at Willie\'s feet, And a briar at Barbro Ellen\'s; They growed t i l l they tied in a true-love\'s knot, The rose and the briar. ; Funding for digitization provided by the Arkansas Humanities Council and the Happy Hollow Foundation.\n---\n### Barbara Allen ; Cruelty of Barbara Allen; Barbaro Ellen; Barb\'ry Allen ; Bonny Barbara Allen; Barbara Ellen; Bonny Barbara Allan ; There were three maids, there were three maids\n- **ID:** ftunivarkansasdc:oai:digitalcollections.uark.edu:OzarkFolkSong/1598\n- **DOI:** \n- **Authors:** Griffin, Hallie\n- **Date:** 1958-07-27\n- **Type:** other\n- **Languages:** en\n- **Publisher:** University of Arkansas Libraries, Fayetteville\n- **Access:** acr_open-access\n- **Topics:** art, relig\n- **Keywords:** a capella singing, Death, Love, Emotions, Death of a Lover, Grief\n\nVoice ; Collected and transcribed by Mary Celestia Parler Sung by Mrs. Hallie Griffin Conway, Arkansas July 27, 1958 Reel 293, Item 6 Barbara Allen There were three maids, there were three maids There were three maids dwelling The ______ one I called my own And that was Barbara Allen. Young man, recollect the other day When you were in town drinking, You drank a toast to the ladies all But you slighted Barbara Allen. He sent a servant to the town, He sent him to her dwelling, Saying, Master’s sick and sends for you If your name be Barbara Allen. Then slowly slowly she rose up And to his bedside going And all she said wherever she stood Was Young man, I fear you\'re dying. Oh, yes, you\'re sick, and very sick, And death is on you dwelling No better, no better, you ever shall be, Cried cruel Barbara Allen. He turned his pale face to the wall And burst out crying Saying, Adieu, adieu to one and all Be kind to Barbara Allen. As she was walking up the streets She heard the bells tolling, And every word they seemed to say Was Cruel Barbara Allen. (Cont\'d)Barbara Allen Reel 298, Item 6 Continued She turned to the east, then looked to the west, And saw those cold corpse coming, Sit down, sit down, this mournful corpse And let me look upon it. Sit down, sit down this mournful corpse And let me look upon it, For I could hare saved this young man\'s life If I had but said that I love him. Sweet William died on a Friday night Miss Barbara died on Saturday The old woman died for love of both She died on Easter Sunday. ; Funding for digitization provided by the Arkansas Humanities Council and the Happy Hollow Foundation.\n---\n### Barbara Allen ; Barbara Ellen; Barbry Allen; Bonny Barbara Allen; Bonny Barbara Allan ; In scarlet twon where I was born\n- **ID:** ftunivarkansasdc:oai:digitalcollections.uark.edu:OzarkFolkSong/2401\n- **DOI:** \n- **Authors:** Sargent, Irene\n- **Date:** 1963-11-22\n- **Type:** other\n- **Languages:** en\n- **Publisher:** University of Arkansas Libraries, Fayetteville\n- **Access:** acr_open-access\n- **Keywords:** a capella singing, Death, Love, Rejection (Psychology), Emotions, Burial, rejection, burials, Death of a Lover, Grief, Grave\n\nvoice ; Collected and transcribed by Don Callaway Irene Sergant Weat Fork, Ark. November 22, 1963 Reel 433, Item 8 BARBARA ALLEN In scarlet twon where I was born There was a fair maid dwelling And every youth cried well away Her name was Barbara Allen. It was in the merry month of May The green buds they were swelling Sweet William came from western state And courted Barbara Allen. It was in the merry month of June When all things they were blooming Sweet William on his death bed lay For the love of Barbara Allan. He sent his servant to the town Where Barbara was a dwelling Saying master is sick and sent for you If your name be Barbara Allen. Slowly, slowly she got up and slowly she came nigh him And first she said whan she got there Young man I think you\'re dying. Ah yes I\'m sick and vary sick And death is nigh me dwelling No better, no better I ever will be If I can\'t have Barbara Allen. Continued Barbara Allen Reel 433, Item 8 Continued Ah don\'t you remember in yonder town When we were at the tavern You drank a health to the ladys all around And slighted Barbara Allen. Oh yes I remember in yonder town When we were at the tavern I gave a health to the ladys all around Gave my heart to Barbara Allen. If you do on your death bed lay What need the tale you\'re telling I can not keep you from your death Adieu said Barbara Allen. As she was on the highway home The birds they kept a singing With every song they seemed to say Hard-hearted Barbara Allen. As she was walking over the fields She heard the death bells knelling With every stroke they seemed to say Hard-hearted Barbara Allen. She looked to the east, she looked to the west She saw the corpse a coming Lay down, lay down that corpse she said That I may look upon him. The more she looked the more she mourned She fell to the ground a crying Saying pick me up and take me home For I am now a dying. Continued Barbara Allen Reel 433, Item 8 Continued Mother, oh Mother go make my bed Go make it long and narrow Sweet William died of pure, pure love And I will die of ...\n---\n### Barbara Allen (Child No. 84) ; Cruelty of Barbara Allen; Barbaro Ellen; Barb\'ry Allen ; Barbara Ellen, Barbry Allen; Bonny Barbara Allan; Bonny Barbara Allen ; In Scarlet Town, where I was born\n- **ID:** ftunivarkansasdc:oai:digitalcollections.uark.edu:OzarkFolkSong/2843\n- **DOI:** \n- **Authors:** Winn, Emmett\n- **Date:** 1958-10-25\n- **Type:** other\n- **Languages:** en\n- **Publisher:** University of Arkansas Libraries, Fayetteville\n- **Access:** acr_open-access\n- **Topics:** hist, hisphilso\n- **Keywords:** a capella singing, Love, Death, Emotions, Burial, burials, Grief, Grave\n\nvoice ; Collected by: Billie Lou Ratliff For: Mary C. Parler Name of singer: Emmett Winn Address: Westville, Oklahoma Date: October 25, 1958 Reel 267 Item 9 BARBARA ALLEN (Child 84) In Scarlet Town, where I was born There was a fair maid dwelling, Made every youth cry ’Well-a-way’ , Her name was Barbara Allen. It was in the month of May The green buds they were swelling; Sweet William came from the western states And courted Barbree Allen. It was in the month of June The roses they were blooming, Sweet William on his deathbed lay For the love of Barbree Allen. He sent his servants to the town Where Barbree was a-dwelling, My master is sick and sent for you Oh, bonnie Barbree Allen. And death is printed on his face And o’er his heart is stealing; Then hasten away to comfort him Oh, lovely Barbree Allen. So slowly, slowly she got up And slowly she came anigh him; And all she said when she was there ’’Young man I think you’re a-dying.” Oh yes, I’m sick and very sick And death is on me dwelling; No better, no better I never will be If I can’t have Barbree Allen. Oh yes, you’re sick and very sick And death is on you dwelling; No better, no better you never will be For you can’t have Barbree Allen.Collected by: Billie Lou Ratliff For: Mary C. Parler Name of singer: Emmett Winn Address: Westville, Oklahoma Date: October 25, 1958 Reel 267 Item 9 (Cont’d) BARBARA ALLEN (Continued) Oh yes, I remember in yonder town In yonder town a-drinking, A drink have to the ladies all around But my heart to you, Barbree Allen. As she was on her highway home The birds the

[Response truncated to prevent overload. Use smaller page sizes or more specific queries.]
</details>

**search_documents**


<details>
<summary>Result from search_documents</summary>

{'type': 'text', 'text': '**Results: 1/410485 pages (6157268 total)**\n### Flowering thorn, The: international ballad studies\n- **ID:** m5yfCWrFODWCrI46HQ24n\n- **Date:** 2007-01-03\n- **Type:** typ_text\n- **Languages:** en\n- **Publisher:** Colorado State University. Libraries, Utah State University Press\n- **Access:** acr_open-access\n- **Topics:** art, litt\n- **Keywords:** Ballads -- History and criticism, Folk literature -- History and criticism\n\nEdited by Thomas A. McKean. ; Includes bibliographical references and index. ; The flowering thorn expresses the dual nature of the ballad: at once a distinctive expression of European tradition, but also somewhat tricky to approach from a scholarly perspective, requiring a range of disciplines to illuminate its rich composition. ; Now she\'s fairly altered her meaning: Interpreting narrative song -- Healing the spider\'s bite: "Ballad therapy" and Tarantismo / Luisa del Giudice -- Music, charm, and seduction in British traditional songs and ballads / Vic Gammon -- "Places she knew very well": the symbolic economy of women\'s travels in traditional Newfoundland ballads / Pauline Greenhill -- A good man is hard to find: positive masculinity in the ballads sung by Scottish women / Lynn Wollstadt -- Jesting with edge tools: the dynamics of a fragmentary ballad tradition / Gerald Porter -- The servant problem in child ballad / Roger deV. Renwick -- May Day and mayhem: portraits of a holiday in eighteenth-century Dublin ballads / Cozette Griffin Kremer -- Malign forces that can punish and pardon: structure and motif -- An oddity of Catalan folk songs and ballad / Simon Furey -- "Barbara Allen" and "The Gypsy Laddie": single-rhyme ballads in the child corpus / William Bernard McCarthy -- The motif of poisoning in Ukrainian ballads / Larysa Vakhnina -- Contexts and interpretations: the walled-up wife ballad and other related texts / Nicolae Constantinescu -- Recapturing the journey: cruxes of context, version, and transmission -- The life and times of Rosie Anderson / Sheila Douglas -- Scholar, Antischolar: Sir Alexander Gray\'s translations of the Danish ballads / Larry Syndergaard -- "George Collins" in Hampshire / David Atkinson -- From France to Brazil via Germany and Portugal: the meandering journey of a traditional ballad / J.J. Dias Marques -- "The White Fisher": an illegitimate child ballad from Aberdeenshire / Julia C. Bishop.\n---\n### Olive Dame Campbell (interview)\n- **ID:** ftutahstateuniv:oai:digital.lib.usu.edu:AFS/329\n- **DOI:** \n- **Authors:** Campbell, Olive D. (Olive Dame), 1882-1954\n- **Date:** 1945-12-28\n- **Type:** other\n- **Languages:** en\n- **Publisher:** Archive of Folk Culture, American Folklife Center, Library of Congress, Washington, D.C.;\n- **Topics:** info, musiq\n- **Keywords:** Wolf, Jim--Correspondence, Folk singers--Appalachian Region, Folk songs, English--Appalachian Region, Ballads, Hymns\n\nThis interview is included in the American Folklore Society Oral History Project held at the Archive of Folk Culture, American Folklife Center, Library of Congress, Washington, D.C. This item is a sound recording of Olive Dame Campbell speaking and singing, dated December 28, 1945 and recorded at an unknown location, talking about her early work as a folksong collector. She remembers the first ballad she heard in 1907 at the Hindman Settlement School in Kentucky. Campbell sings \'\'Barbara Allen\'\' and \'\'Guide me, O thou great Jehovah\'\' on the recording, which is identified as an illustrated lecture by the Library of Congress sound engineer who duplicated the disc. Collection includes two letters from Jim Wolf to Rae Korson of the Archive of Folk Song dated 1957, using the return address of the Council of the Southern Mountains, Berea, Kentucky, and the Campbell Folk School, Brasstown, N.C., describing the original disc recording and discussing its possible duplication by the Library of Congress. Wolf mentions a visit with singer Jean Ritchie and her family in one letter. Manuscripts include photocopies of the labels of the original sound disc and duplicate sound disc. This collection consists of a manuscripts, 1 sound tape reel (21 min.) (analog, 7 1/2 ips, 1 track ; 7 in.).\n---\n### Volkslied und Volksballade\n- **ID:** 6_WO3xznJfqeN1Jt10Rfh\n- **Date:** 2013\n- **Type:** typ_text\n- **Languages:** de, ru\n- **Publisher:** SPbGU, RIO, Filologiceskij fakul\'tet\n- **Topics:** musiq\n- **Keywords:** German and related languages, Music\n---\n### Kramářská píseň jako inspirační zdroj české písně lidové (na základě analýzy textových i melodických variant písně Jaký mám trápení.) ; Broadside ballads as an inspiration for the Czech folk song\n- **ID:** ftczechacademysc:oai:kramerius.lib.cas.cz:uuid:3e9f4e55-9bf5-41cc-b97f-a9c37e9d6598\n- **DOI:** \n- **Authors:** Thořová, Věra\n- **Type:** other\n- **Languages:** undefined\n- **Topics:** musiq, anthro-se\n- **Keywords:** broadside ballad, folk song, variants, oral tradition, transformation of broadside ballad to a folk song\n\nThe oral tradition preserved several dozens of folk songs that arose out of the broadside ballads. In these cases the broadside ballad was shortened, the strophes that included verses and formulations not reflecting the popular experience were omitted and the vulgar words replaced by formulations typical for folk song. The tolkative character of the broadside ballad was substituted by the concise way of folk song. The texts were supplemented by folk melodies. These statements can be proved by the case of the song Such a sorrow I have, cloth trousers… that arose out of the broadside ballad. This folk song existed in many textual and melodic variants and under various incipits on the whole territory of Bohemia and parts of Moravia and Slovakia. Some formulations in the broadside ballad indicate its origin in the period of 1811–1816, while the folk song appeared for the first time in the collection of K. J. Erben from the year 1864. In published and manuscript collections were ascertained in the whole 23 textual and 18 melodic variants. The tunes come out of the traditional melodies and usually imitated some concrete folk song. The songs are mostly dance songs, in triple time, mostly in the rhythm of „sousedská“, ländler or round-and-round („kolečko“). The instrumental recordings of closing parts of some songs as well as the notes of the collectors prove that these songs accompanied the dance at dance evenings or weddings. Their humorous text and dance rhythm probably contributed to their popularity and wide spreading, especially on occasions of high-spirited wedding celebrations. The song had been preserved in oral tradition, in numerous variants, for almost 200 years, and this constitutes one of the main attributes of a folk song.\n---\n### Broadside Ballads Online: RDF metadata\n- **ID:** ftuloxford:oai:ora.ox.ac.uk:uuid:5ab934b5-8229-4f33-82d5-4a18f976c6fb\n- **DOI:** \n- **Authors:** Franklin, A, Bergel, G\n- **Date:** 2020-02-21\n- **Type:** typ_dataset\n- **Languages:** undefined\n- **Publisher:** University of Oxford\n- **Access:** acr_open-access\n- **Topics:** art, info\n- **Keywords:** Broadsides, Ballads, English\n\nBroadside ballads, printed cheaply on one side of a sheet of paper from the earliest days of printing, contain song-lyrics, tunes and woodcut illustrations and bear news, prophecies, histories, moral advice, religious warnings, political arguments, satire, comedy and bawdy tales. Sold in large numbers on street-corners, in town-squares and at fairs by travelling ballad-singers and pinned on the walls of alehouses and other public places, they were sung, read and viewed with pleasure by a wide audience, but have been handed-down to us in only small numbers. The Bodleian Library at the University of Oxford holds nearly 30,000 songs, many of them unique survivals, printed from the 16th to the 20th Centuries. Digital facsimiles and an online database were first made accessible in 1999. The Broadside Ballads Online project (ballads.bodleian.ox.ac.uk) updated that database and included links it to other resources. The English Broadside Ballad Archive based in the Early-Modern Center at the University of California, Santa Barbara specialises in ballads of the 17th century and provided full-text transcriptions, as well as images and catalogue records, of over 4,000 ballads. The Vaughan Williams Memorial Library, based at the English Folk Song and Dance Society headquartered at Cecil Sharp House in London, maintains the Roud Broadside Index of references to songs which appeared on broadsides, chapbooks, songsters, and other cheap print publications, up to about 1920. Linked to the Roud Folk Song index, this provides a survey of the ballad tradition through its publishing history. A representation of the Broadside Ballads Online data as RDF can be downloaded from this dataset.\n---\n### For the Love of Barbie Allen: A Modern Child Ballad\n- **ID:** ftmarshalluniv:oai:mds.marshall.edu:asa_conference-1707\n- **DOI:** \n- **Authors:** Barnett, Phillip A, Curry, Zachary T\n- **Date:** 2015-03-28\n- **Type:** typ_text\n- **Languages:** undefined\n- **Publisher:** Marshall Digital Scholar\n- **Topics:** musiq, art\n- **Keywords:** folklore_folkways, music\n\nThe short film, For the Love of Barbie Allen: A Modern Child Ballad, is the modern retelling of one of the most widespread Child Ballads, Child 84: “Barbara Allen.” Sweet William becomes Will and Barbara Allen becomes Barbie Allen as the two undergo the breakdown of what was once a strong, intimate relationship. In less than ten days, the film was conceived, written, filmed, and edited by University of Kentucky students. Directed and written by Appalachian filmmakers Phillip Barnett and Zachary Curry, For the Love of Barbie Allen examines the human condition and the destructive power of love and jealousy. While parts of the story are altered, the core of the ballad rings true and is clearly still relevant. Though modern American relationships are quite distinct from their Scots-Irish ancestors, one thing will always remain constant: true love has the ability to build a person up and tear them down in the same breath.\n---\n### Woody Guthrie\'s "Tom Joad" ; Woody Guthrie\'s "Tom Joad": Reinventing the American folk ballad\n- **ID:** 0LiD2EEdaadRmS22N_Nnb\n- **Authors:** Arleo, Andy\n- **Date:** 2006\n- **Type:** typ_book-part\n- **Languages:** en\n- **Publisher:** HAL CCSD, CRINI\n- **Access:** acr_open-access\n- **PDF:** https://shs.hal.science/halshs-00623908/file/Tom_Joad_version_1.pdf\n- **Topics:** musiq, anthro-se\n- **Keywords:** ballade populaire, musique populaire, Les Raisins de la colère, Woody Guthie, Tom Joad, folk ballad, folk music, popular music, John Steinbeck, Bruce Springsteen, The Grapes of Wrath, John Ford, [SHS.LANGUE]Humanities and Social Sciences/Linguistics, [SHS.MUSIQ]Humanities and Social Sciences/Musicology and performing arts, [SHS.LITT]Humanities and Social Sciences/Literature\n\nWoody Guthrie\'s ballad "Tom Joad," recorded in 1940, was directly inspired by John Steinbeck\'s 1939 novel The Grapes of Wrath and the successful John Ford film adaptation, released in 1940. The main focus of this article will be on the Guthrie ballad, with passing references to the Steinbeck novel and the John Ford film. We will also look at Tom Joad\'s legacy as reflected in the Springsteen song. In addition to painting a portrait of an American folk ballad, this research aims to shed light on several more general issues. "Tom Joad" provides a fascinating case study on the migration and transformations of a particular poetic form, the ballad, notably within the historical and social context of Depression-era America. It also exemplifies the subtle interplay between oral and written traditions along the folk--popular--highbrow cultural continuum. The tale of the Joad family raises questions regarding shifting national, regional, social, ethnic and linguistic identities as well. The song also illustrates intertextuality within and among three different semiotic systems (music, language and film) and lends itself to a comparative study of narration in these media. Finally, we may view "Tom Joad" as a national folk/literary hero contributing to the forging of an American mythology.\n---\n### Learning Lineage And The Problem Of Authenticity In Ozark Folk Music\n- **ID:** ftunimississippi:oai:egrove.olemiss.edu:etd-2828\n- **DOI:** \n- **Authors:** Tharp, Kevin Lyle\n- **Date:** 2020-01-01\n- **Type:** typ_text\n- **Languages:** undefined\n- **Publisher:** eGrove\n- **Topics:** musiq\n- **Keywords:** Authenticity, British Ballads, Folklore, Informal Learning, Oral Transmission, Ozark Folk Music\n\nABSTRACT Thorough examination of the existing research and the content of ballad and folk song collections reveals a lack of information regarding the methods by which folk musicians learn the music they perform. The centuries-old practice of folk song and ballad performance is well-documented. Many Child ballads and other folk songs have been passed down through the generations. Oral tradition is the principal method of transmission in Ozark folk music. The variants this method produces are considered evidence of authenticity. Although alteration is a distinguishing characteristic of songs passed down in the oral tradition, many ballad variants have persisted in the folk record for great lengths of time without being altered beyond recognition. This fact reveals the existence of a formidable teaching and learning method that deserves extensive investigation. This research represents a deeper understanding of how folk musicians learn the music they perform. It includes information about methods of folk music teaching and learning not previously recorded in the extant research. Informants’ statements about their personal learning experiences can be connected to widely accepted theories of learning. These connections are some of the most important findings reported in this research. In addition, this research provides an exploration of folk musicians’ beliefs about the roles of family lineage, places of birth, and methods of transmission in authentic folk music performance. This work contains evidence of a fundamental change in what folk musicians consider authentic methods of transmission. The exploration of authenticity, the effects of technology on folk music learning, and oral transmission provided here is a step forward in the study of Ozark folk music.\n---\n### Ballads\n- **ID:** 20.500.12657/25518\n- **DOI:** \n- **Authors:** Owens, Richard\n- **Date:** 2015-01-01\n- **Type:** typ_book\n- **Languages:** en\n- **Topics:** hisphilso, musiq\n\nOriginally published by eth co-director David Hadbawnik’s habenicht press in 2012, Ballads uses the lyric form to explore the effects of global Capitalism from a sharp Marxist perspective. Recognizing the congruence between folk song circulation and the circulation o

[Response truncated to prevent overload. Use smaller page sizes or more specific queries.]
</details>

Here's a summary of what GoTriple has on "Barbara Allen":

---

## GoTriple Results for "Barbara Allen"

The search returned two kinds of material: **field recording transcriptions** and **scholarly publications**.

### 🎵 Field Recording Transcriptions (University of Arkansas Ozark Folk Song Collection)

These are individual variant recordings of the ballad, collected in Arkansas and Oklahoma in the 1950s–60s as part of the Mary Celestia Parler collection:

| Singer | Date | Location | Title Variant | First Line |
|--------|------|----------|---------------|------------|
| Oscar Smith | 1959-07-22 | Westville, OK | Barbara Allen | "In London town where I was born" |
| Mrs. Jim Crymes | 1954-06-15 | DeValls Bluff, AR | Barbara Allen | "In Scarlet town, where I was born" |
| Betty Minnick & Mary Briscoe | 1951-05-01 | High, AR | Barbara Allen | "Sweet Willie's sick, and very sick" |
| Hallie Griffin | 1958-07-27 | Conway, AR | Barbara Allen | "There were three maids dwelling" |
| Irene Sargent | 1963-11-22 | West Fork, AR | Barbara Allen | "In scarlet town where I was born" |
| Emmett Winn | 1958-10-25 | Westville, OK | Barbara Allen (Child 84) | "In Scarlet Town, where I was born" |

All are a capella vocal recordings, open access, with full lyric transcriptions. They showcase the same title variants we saw in UTSI ("Barb'ry Allen," "Barbara Ellen," "Bonny Barbara Allen," etc.).

---

### 📚 Scholarly Publications

| Title | Author(s) | Date | Type | Key Relevance |
|-------|-----------|------|------|---------------|
| **"Barbara Allen" and "The Gypsy Laddie": Single-rhyme ballads in the child corpus** | William Bernard McCarthy | 2007 | Book chapter in *The Flowering Thorn: International Ballad Studies* | Directly analyzes Barbara Allen as a single-rhyme ballad in the Child corpus |
| **For the Love of Barbie Allen: A Modern Child Ballad** | Phillip Barnett & Zachary Curry | 2015 | Short film / conference paper | Modern retelling of Child 84 set in Appalachia |
| **Olive Dame Campbell (interview)** | Olive Dame Campbell | 1945 | Sound recording | Campbell sings "Barbara Allen" and discusses her early folk song collecting in Kentucky (1907) |
| **Learning Lineage and the Problem of Authenticity in Ozark Folk Music** | Kevin Lyle Tharp | 2020 | Thesis | Examines oral transmission and authenticity in Ozark ballad performance, including Child ballads |
| **Broadside Ballads Online: RDF metadata** | Franklin & Bergel | 2020 | Dataset | Bodleian Library's broadside ballad collection — includes Barbara Allen broadsides |
| **Kramářská píseň jako inspirační zdroj české písně lidové** | Věra Thořová | 2013 | Article | On broadside-to-folk-song transformation (Czech tradition, parallel to Barbara Allen's broadside origins) |

---

### Key Takeaway

The most directly relevant scholarly work is **William Bernard McCarthy's chapter** in *The Flowering Thorn* (2007), which specifically analyzes **"Barbara Allen" as a single-rhyme ballad** in the Child corpus — exactly the kind of analytical study that connects the variants we've been finding across UTSI, the Session, and Global Jukebox. The Ozark field recordings also complement the UTSI and GJB variants nicely, adding more American Southern/Appalachian versions to the picture.

### USER
What’s broadside?
Do we get the links to the field recordings?

### ASSISTANT
**get_document**

**get_document**

### USER
What is broadside?

### ASSISTANT
A **broadside** (or broadside ballad) is a single sheet of paper printed on one side with the lyrics of a song — often with a suggested tune name, a woodcut illustration, and sometimes a publisher's name. They were essentially the cheap, popular press of their day.

### Key facts:

- **When:** Flourished from the 16th through the 19th centuries, particularly in Britain.
- **How they worked:** A ballad-seller would stand on a street corner or at a fair, sing the song printed on the sheet, and sell copies to passersby. They were also pinned up on walls of alehouses and public places.
- **Content:** News, prophecies, moral advice, political satire, love stories, crime reports, and — crucially — traditional ballads like "Barbara Allen."
- **Price:** Very cheap — a penny or less — making them accessible to a wide audience.
- **Relationship to folk tradition:** Many songs that we now think of as "traditional folk songs" were actually widely circulated *as broadsides first*. "Barbara Allen" is a prime example — it existed in oral tradition but was also printed on hundreds of different broadsides over the centuries, which helped spread it across Britain, Ireland, and North America.
- **Survival:** Because they were cheap and disposable, relatively few have survived. The Bodleian Library at Oxford holds nearly 30,000 (the *Broadside Ballads Online* collection from the GoTriple results), and the English Broadside Ballad Archive at UC Santa Barbara has digitized over 4,000 from the 17th century.

### Why it matters for "Barbara Allen":

The broadside trade is a big part of why "Barbara Allen" became one of the most widely distributed ballads in the English-speaking world. It was printed on broadsides in England, Scotland, and later America, which helped transmit it to singers who then carried it into oral tradition — producing the many regional variants we've been finding across UTSI, the Global Jukebox, and the Ozark field recordings.

### USER
Do we have links to the field recordings?

### ASSISTANT
**get_document**

**get_document**