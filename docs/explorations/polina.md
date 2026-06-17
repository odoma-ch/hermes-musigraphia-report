---
title: Polina Proutskova
---

# Case Studies — Polina Proutskova

Three explorations using Quagga Agent across the Global Jukebox, CKG, and LinkedMusic. Each study includes a shareable conversation link and a critical assessment of the querying process.

---

## Exploration 1: A Cappella Dance Songs

This exploration uses the Global Jukebox (GJB) dataset to test an ethnomusicological hypothesis about the rarity of a cappella dance songs worldwide.

| Resource | Link |
|----------|------|
| Live conversation | [quagga-agent.graphia-ssh.eu/s/d1137806…](https://quagga-agent.graphia-ssh.eu/s/d1137806-d47a-4e7b-ba95-0f4abd0bcc08) |

### Hypothesis

In most cultures, people dance to instrumental music; dancing while singing a cappella is rare. The reasoning is twofold: singing and dancing simultaneously is physically demanding, so performers usually do one or the other; and dance music is highly repetitive, which is generally easier for instruments than for singers.

In Eastern Europe, Russia has the *khorovod* genre — circle dances performed with a cappella singing. This genre may be connected to Ivan the Terrible's ban on instrumental music, which interrupted the instrumental tradition and created space for dance songs to develop. Neighbouring countries, despite many musical similarities, do not have comparable genres and tend to dance to instrumental tunes.

### The querying process

The investigation required substantial hand-holding, primarily due to two factors:

1. **Non-human-readable genre labels.** The GJB dataset uses Wikidata genre IDs rather than human-readable labels. The initial search found 19 songs with no Russian songs among them, even though the dataset contains two Russian *khorovods*. After some deliberation, the agent found one of them. We then had to identify what the Wikidata genre IDs referred to and determine which were related to dance. After an extended process, we collected a list of dance-related genre labels and reran the search.

2. **Sorting by country.** Asking for the findings to be sorted or grouped by country required another extended retrieval process to collect country labels for the Wikidata IDs. The agent initially guessed many labels incorrectly. Once the country labels had been retrieved, the sorted table could be constructed.

Querying Wikidata was unstable throughout, and the overall process required substantial human intervention.

### Findings

The initial result was surprising: a cappella dance songs represented **28% of all dance songs worldwide** and **47% in Europe**. However, this number is biased because only cultures in which dance songs were recorded were included. This excluded traditions in which dances were performed only, or mostly, to instrumental tunes and no dance songs were recorded.

The bias follows from the construction of the Lomax dataset, which focused on singing and did not include purely instrumental performances.

Correcting for this bias by looking at cultures rather than songs:

- In Europe, there were 75 dance songs in total, of which 37 (almost half) were a cappella dance songs. However, across **all** European songs in the dataset, a cappella dance songs constituted only **5.6%**.
- Of the 148 European cultures represented in GJB, only **7 (4.7%)** had a cappella group dance songs — closer to the intuitive expectation of under 5%.
- The worldwide percentage of cultures with a cappella dance songs was **6.7%**.

### Cultures with a cappella group dance songs by continent

| Continent | Total Cultures (any songs) | A Cappella Group Dance Cultures | % |
|:----------|---------------------------:|--------------------------------:|:--|
| Africa | 204 | 19 | 9.3% |
| Asia | 190 | 15 | 7.9% |
| Europe | 148 | 7 | 4.7% |
| North America (incl. Caribbean) | 132 | 2 | 1.5% |
| South America | 73 | 7 | 9.6% |
| Oceania | 123 | 8 | 6.5% |
| **Global total** | **870** | **58** | **6.7%** |

### Assessment

It produced new ethnomusicological insights and showed the potential value of this technology. The key methodological lesson is the importance of correcting for dataset bias: raw song counts dramatically overstate the prevalence of a cappella dance songs because the Lomax dataset systematically excludes purely instrumental traditions.

### Possible next steps

- Investigate the specific cultures with a cappella dance songs to identify shared characteristics
- Compare the Russian *khorovod* tradition with a cappella dance traditions in other continents
- Explore whether the dataset bias can be quantified more precisely by cross-referencing with other sources on instrumental dance traditions

---

## Exploration 2: Russian Operas and Ballets

This exploration asked for Russian operas in CKG.

| Resource | Link |
|----------|------|
| Live conversation | [quagga-agent.graphia-ssh.eu/s/2ddbd5fa…](https://quagga-agent.graphia-ssh.eu/s/2ddbd5fa-d8d7-4510-9624-2d6864a9fd0c) |

### The querying process

The CKG graph does not appear to contain a country property. The agent did not state this at first, but instead searched for examples of Russian operas that seemed to be known to the system in advance:

```sparql
SELECT DISTINCT ?work ?label WHERE {
  ?performance cto:CTO_0001019 ?work .
  ?work rdfs:label ?label .
  FILTER(
    CONTAINS(LCASE(STR(?label)), "boris godunov") ||
    CONTAINS(LCASE(STR(?label)), "onegin") ||
    CONTAINS(LCASE(STR(?label)), "pikovaja") ||
    CONTAINS(LCASE(STR(?label)), "zarenbraut") ||
    CONTAINS(LCASE(STR(?label)), "sadko") ||
    CONTAINS(LCASE(STR(?label)), "mlada") ||
    CONTAINS(LCASE(STR(?label)), "leben für den czar")
  )
}
```

This was not sufficient, so I asked for more operas and for ballets. The agent returned more operas, but I do not have the SPARQL query for that step, so the retrieval method is unclear. It may have searched by composer, by Russian institutions, or through Musiconn.

### Hallucinated attribution

When I asked for the most popular ballet, the agent looked for the number of performances in Musiconn and returned *Romeo and Juliet* by Tchaikovsky, which does not exist. There is a *Romeo and Juliet* ballet by Prokofiev. The agent appears to have conflated Tchaikovsky's overture with Prokofiev's ballet. When prompted, it corrected itself.

### Assessment

Two problems emerged: the absence of a country property in CKG forced a workaround based on known work titles rather than structural queries, and the agent hallucinated an attribution by conflating two distinct works sharing the same title.

---

## Exploration 3: Barbara Allen

This exploration searched for the ballad "Barbara Allen" across LinkedMusic datasets.

| Resource | Link |
|----------|------|
| Live conversation | [quagga-agent.graphia-ssh.eu/s/2e3f27f7…](https://quagga-agent.graphia-ssh.eu/s/2e3f27f7-7444-4399-b1b0-c41ef0028d72) |

### Findings across datasets

- **The Session:** one entity found, but the dataset mainly contains instrumental dance tunes and lacks data structures for songs or lyrics. Notation for two variants exists on the website but appears to be a different tune from the ballad despite sharing the title.
- **GJB:** two correct songs with the correct cultures. One item was a compilation of several recordings by several performers from Aberdeen, all singing versions of the same song. It had only one song number, which the agent found, but the agent could not identify that the record represented a compilation.
- **RISM:** one manuscript.
- **UTSI:** 20 variants, including three Irish examples, with lyric incipits. The hope of relating variants across datasets was not realised, since The Session lacks song/lyric data structures.
- **MusicBrainz** (within LinkedMusic): returned nothing, probably because of a timeout. A direct MusicBrainz search returned ~88,000 hits, of which approximately the first 450 were relevant.
- **GoTriple:** the agent found several field recordings, one book chapter, one short film with the song title in the name, and several more publications described as relevant but less convincing. When checked directly, GoTriple found the field recordings and the short film, but not the book chapter. The chapter does exist and is findable through Google Scholar; GoTriple finds the book but not the chapter in it, even though "Barbara Allen" appears in the chapter title.

### Assessment

It found informative UTSI variants and relevant field recordings from GoTriple. Limitations included the inability to cross-link variants across datasets due to underlying graph structure and the agent's failure to recognise a compilation record.
