---
title: Matteo Romanello
---

# Exploring the Detmolder Hoftheater Repertoire (1825–1875) — Matteo Romanello

This exploration focuses on the [repertoire of the Detmolder Hoftheater 1825–1875](https://nfdi4culture.de/id/E5305) as a case study for what CKG makes accessible.


| Resource | Link |
|----------|------|
| Archived conversation (part 1) | [PDF export](../assets/chat-archive/Matteo_chat-Detmolder-hoftheater.pdf) / [Markdown export](../assets/chat-archive/Matteo_chat-Detmolder-hoftheater.md) | 
| Archived conversation (part 2) | [PDF export](../assets/chat-archive/Matteo_chat-Detmolder-hoftheater_part2.md) / [Markdown export](../assets/chat-archive/Matteo_chat-Detmolder-hoftheater_part2.pdf) | 

## Querying the collection

The query below counts works by associated person within this collection. The CKG "data index" for each collection links works to persons via external authority identifiers (GND, VIAF, etc.):

```sparql
PREFIX cto: <https://nfdi4culture.de/ontology/>
PREFIX nfdi: <https://nfdi.fiz-karlsruhe.de/ontology/>

SELECT ?extId (COUNT(*) AS ?workCount) WHERE {
  ?work cto:CTO_0001006 <https://nfdi4culture.de/id/E5305> .
  ?work cto:CTO_0001009 ?obj .
  ?obj nfdi:NFDI_0001006 ?extId .
} GROUP BY ?extId
ORDER BY DESC(?workCount)
```

The results ([CSV download](../assets/data/table-a29d4668-0cf6-4622-b95d-b6a326b4f16f-b556021c-dc19-486e-9c30-f02c7054b047-9.csv)) follow a long-tail distribution: a handful of highly represented individuals and a long tail of those appearing only once or twice. Persons appearing more than 10 times provide a reasonable first overview of the collection's character.

## A note on CKG's data index approach

This query also reveals a structural limitation worth keeping in mind. The CKG publishes what might be called *indexes of data*: each collection is described in terms of the entities — persons, places, institutions — that appear within it, linked via authority records. This is a deliberate design choice aimed at maximising discoverability across heterogeneous collections. The cost is a flattening of the underlying semantic richness: the *nature* of the relation between a person and a work is lost in the process. The query above tells us "how many works in this collection are associated with person X", but it cannot tell us in what capacity — composer, librettist, translator, performer, dedicatee? That distinction, which would be essential for any deeper musicological analysis, is not surfaced.

Despite this limitation, even a flattened view of this kind already constitutes a meaningful *fingerprint* of the collection, as the case of August von Kotzebue illustrates below.

## August von Kotzebue: a collection fingerprint

The top-ranked person in this collection is August von Kotzebue (105 associated works), followed by figures such as Ernst Raupach (46) and Ludwig Robert (73). Even without knowing the role these individuals played in relation to each work, the ranking itself is historically meaningful: Kotzebue was the dominant playwright on German-language stages in the very era the Detmold theatre was founded, and his posthumous prominence in the collection data is entirely consistent with what we know about 19th-century repertoire practice.

[GoTriple](https://gotriple.eu/) surfaces a substantial body of scholarship on Kotzebue, illustrating the kind of research context that can be brought to bear on this collection:

### Blog Posts & Scholarly Blog Entries

| Title | Author | Date | Topics |
|-------|--------|------|--------|
| Kotzebue, der Kosmopolitismus und die Weimarer Klassik – eine Polemik | Gastautor*in | 2021 | hist, litt |
| Unbekannter Brief August von Kotzebues an Baron Peter von Braun in Wien (1797) | Rolf Haaser | 2021 | litt, art |
| August von Kotzebue and Russia's Lived Enlightenment | Gastautor*in | 2021 | phil, hist |
| Kotzebue durch Nietzsches Augen | Rolf Haaser | 2025 | art, litt |
| August von Kotzebue vs. Gall, oder: Erlaubt ist was gefällt? | Frieder Sondermann | 2023 | art, musiq |
| August Wilhelm Schlegel trifft auf August von Kotzebue in St. Petersburg (1812) | Anna Ananieva | 2021 | litt, anthro-se |
| Unbekannter Zeitzeugenbericht von der Ermordung August von Kotzebues (1819) | Rolf Haaser | 2021 | — |

### Books by Kotzebue

| Title | Date | Language | Access |
|-------|------|----------|--------|
| Die Geschichte meines Vaters (Roman) | 1790 | de | open-access |
| Erinnerungen aus Paris im Jahre 1804 | 1804 | de | open-access |
| Er und Sie: Vier romantische Gedichte | 1781 | de | open-access |
| Menschenhaß und Reue (Schauspiel) | 1790/1791 | de | open-access |
| Unpartheyische Untersuchung über die Folgen der französischen Revolution | 1794 | de | open-access |

### Scholarly Books & Articles

| Title | Author | Date | Topics |
|-------|--------|------|--------|
| Von Kotzebue bis Fleming: Sprach-, Literatur- und Kulturkontakt im Baltikum | Mari Tarvas | 2024 | lang |
| O pewnym zabójstwie na tle politycznym (on the assassination of Kotzebue) | Nina Nowara-Matusik | 2020 | hist, phil |

## Recovering the roles: Kotzebue in LinkedMusic (RISM)

The fingerprint above raises a natural follow-up. If CKG, by design, flattens the *nature* of the person–work relation, what does the same figure look like in a knowledge graph that preserves it? [LinkedMusic](https://virtuoso.simssa.ca/sparql) — a federation of fourteen music-specific databases (MusicBrainz, RISM, DIAMM, CantusDB and others), also accessible through the Quagga Agent — offers a useful complement, both because it covers the period in which the Detmold theatre operated and because, being domain-specific, it retains role-level vocabulary that CKG necessarily drops.

After a discovery turn that lists the available KGs and a schema-introspection turn enumerating the eleven sub-graphs of LinkedMusic, the question *"is there information about August von Kotzebue (Q57242)?"* returns two records: a MusicBrainz artist node (biographical, with no associated works) and a RISM person node (`rism.online/people/34844`). Both are linked to Q57242 via `P2888`, which makes the cross-graph identity resolution explicit.

Inside RISM, **410 sources** are linked to Kotzebue, distributed across four roles, each encoded as a different predicate:

| Role | Predicate | Sources |
|------|-----------|---------|
| Lyricist | `wd:P676` | 399 |
| Librettist | `wd:P87` | 8 |
| Other (Quagga labels as *dedicatee*) | `wd:P655` | 2 |
| Composer | `wd:P86` | 1 |

This is exactly the level of distinction that the CKG fingerprint cannot expose. With roles preserved, the question *"who set Kotzebue's texts to music?"* becomes well-defined, and a single `GROUP BY` produces an answer:

```sparql
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
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

The result is itself long-tailed and historically revealing. Eighty-five distinct composers set Kotzebue's texts in the RISM corpus; **Friedrich Heinrich Himmel** — a today-peripheral Berlin Kapellmeister — dominates with **139 sources**, more than the next six composers combined. He is followed by Bernhard Anselm Weber (27), Carl Maria von Weber (22), an "Anonymus" cluster (21), and Beethoven, in fifth place at 20. Forty-seven of the eighty-five composers (55%) appear only once. The shape of this distribution echoes the Detmold ranking — a small group of high-volume associations and a long tail of singletons — but its semantic content is qualitatively different: here we are reading specifically *musical* reception, not undifferentiated co-occurrence.

### Interactive chart

Quagga Agent generated this horizontal bar chart from the RISM query results above, showing the top ten composers by source count for musical settings of Kotzebue's texts.

<iframe
  src="../../assets/visualizations/artifact-24ec0466-26bd-405f-82bd-1da4c6019f00-0.html"
  title="Composers who set Kotzebue's texts to music"
  width="100%"
  height="640"
  style="border: 1px solid var(--md-default-fg-color--lightest); border-radius: 8px; display: block;"
  loading="lazy">
</iframe>

[Open chart in full screen](../assets/visualizations/artifact-24ec0466-26bd-405f-82bd-1da4c6019f00-0.html){ .md-button .md-button--primary target="_blank" }

The methodological takeaway compounds the complementarity argued in the next section. CKG and a domain graph such as LinkedMusic answer different questions at different scopes: the former trades semantic depth for cross-domain discoverability anchored on collections; the latter retains relation types at the cost of narrower coverage. Used together — CKG to surface Kotzebue as the Detmold fingerprint, LinkedMusic to characterise the musical settings of his texts in RISM — they reconstitute much of what either alone would leave implicit.

## CKG vs. LLMs: access to structured collection data

CKG surfaces structured information about this collection that is effectively invisible to general-purpose LLMs — and, to a large extent, to web search engines as well. This is not merely a quantitative point about the amount of data; it concerns the *type* of knowledge involved. The CKG encodes specific, provenance-rich facts about individual collections — which works they hold, which persons are associated with them, how those works relate to authority records — that are not crawled, indexed, or memorised by current AI systems.

This contrast is well illustrated by an exchange with Claude Opus 4.8, prompted with: "What do you know about August von Kotzebue in relation to the Hoftheater in Detmold?"

> Let me look into the specific connection rather than rely on general impressions, since the Detmold link is fairly niche. The general results turn up a lot about Kotzebue but nothing tying him specifically to Detmold. Let me look more directly at the Detmold court theatre's history. The honest answer here turns on a chronological point that's worth leading with: there's no direct personal connection between Kotzebue and the Detmold court theatre, because he was dead before it opened.
>
> The timeline makes this clear. Kotzebue was murdered in 1819 by Karl Ludwig Sand, a militant member of the Burschenschaften — stabbed at his home in Mannheim on 23 March of that year. The Detmold Hoftheater, by contrast, didn't exist yet: Prince Leopold II of Lippe decided to have a court theatre built in Detmold, the foundation stone was laid on 18 April 1825, and the curtain rose for the first time on 8 November, with Mozart's "Titus der Gütige" (La clemenza di Tito). So the house opened more than six years after Kotzebue's death. He never visited, directed, or wrote for it — unlike his documented stints running the Vienna court theatre and the German theatre in St. Petersburg.
>
> The real relationship is therefore one of **repertoire**, and it's a strong one. Kotzebue was simply the most-played playwright on German-language stages in exactly the era the Detmold theatre was founded. To give a sense of scale: his roughly 230 plays made up about a quarter of the repertoire of all German-language stages between 1795 and 1825, and his works remained a staple well after his death. From the outset the Detmold programme included both music theatre and spoken drama, and the house quickly built up an extensive repertoire and a good reputation well beyond the borders of the principality — and a "spoken drama" repertoire in the 1820s–1840s would almost inevitably have leaned heavily on Kotzebue, alongside figures like Iffland.
>
> So the accurate framing is: when the Detmold court theatre was filling its stage with the standard German repertoire of the period, Kotzebue's comedies and sentimental dramas (*Menschenhass und Reue*, *Die deutschen Kleinstädter*, and so on) were part of that stock — a posthumous, repertoire-level presence rather than any biographical tie.
>
> One caveat worth flagging for your purposes: I haven't been able to confirm *specific* documented Kotzebue performances at Detmold with dates from these searches. The digitization project covering the Detmold Hoftheater (1825–1875) — the TEI/MEI source-cataloguing effort run through the Lippische Landesbibliothek — would be the place where individual *Theaterzettel* (playbills) and performance materials are indexed. If you want, I can dig into that project's catalogue or spielplan data to see whether specific Kotzebue stagings are recorded. Would that be useful?

The response is instructive on two counts. First, it confirms that the model has no direct access to the collection-level facts that CKG encodes: it cannot verify Kotzebue's actual presence in the Detmold repertoire and is reduced to historical inference and a request to "dig into" a digitisation project that CKG already indexes. Second, the response itself demonstrates what a well-informed LLM *can* contribute when CKG provides the structured anchor: contextualisation, interpretation, and the identification of meaningful patterns in data that the graph alone can hardly explain.

This complementarity is arguably the most productive framing for CKG–LLM integration: the graph supplies the collection fingerprint; the model supplies the interpretive layer.