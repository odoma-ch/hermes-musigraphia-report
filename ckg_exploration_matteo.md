Started exploring a bit the musicology content in CKG. Decided to focus on the [repertoire of the Detmolder Hoftheater 1825–1875](https://nfdi4culture.de/id/E5305) – see [this conversation](https://quagga-agent.graphia-ssh.eu/s/a29d4668-0cf6-4622-b95d-b6a326b4f16f) with Quagga agent.


This is the query that gives you the count of works by person (composer?) in this collection (results are [here](./data:/table-a29d4668-0cf6-4622-b95d-b6a326b4f16f-b556021c-dc19-486e-9c30-f02c7054b047-9.csv)):
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

It's a long tail distribution: a handful of very "prominent" people, and a long tail of "less represented" people. It seems fair to focus on people that appear more than 10 times, at least to get an overview of what is this collection about.

Thanks to GraphChat, I was able to get the following query to retrieve information about these individuals from DNB (results [here](./data:/Iwts5i.csv)):

```
PREFIX gndo: <https://d-nb.info/standards/elementset/gnd#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>

SELECT ?gndId ?preferredName ?bio ?dateOfBirth ?dateOfDeath ?placeOfBirth ?placeOfDeath ?professionOrOccupation ?sameAs WHERE {
  VALUES ?gndId {
    <https://d-nb.info/gnd/118565796>
    <https://d-nb.info/gnd/118612425>
    <https://d-nb.info/gnd/100823548>
    <https://d-nb.info/gnd/118706640>
    <https://d-nb.info/gnd/118667424>
    <https://d-nb.info/gnd/116207523>
    <https://d-nb.info/gnd/116836709>
    <https://d-nb.info/gnd/116752505>
    <https://d-nb.info/gnd/116850310>
    <https://d-nb.info/gnd/118610813>
    <https://d-nb.info/gnd/116616261>
    <https://d-nb.info/gnd/116311118>
    <https://d-nb.info/gnd/118633716>
    <https://d-nb.info/gnd/118555324>
    <https://d-nb.info/gnd/100844901>
    <https://d-nb.info/gnd/118658875>
    <https://d-nb.info/gnd/104309040>
    <https://d-nb.info/gnd/116686030>
    <https://d-nb.info/gnd/118607626>
    <https://d-nb.info/gnd/116987367>
    <https://d-nb.info/gnd/118507400>
    <https://d-nb.info/gnd/105607231>
    <https://d-nb.info/gnd/116891025>
    <https://d-nb.info/gnd/118613723>
    <https://d-nb.info/gnd/118737775>
    <https://d-nb.info/gnd/116989114>
    <https://d-nb.info/gnd/116746823>
    <https://d-nb.info/gnd/118785230>
    <https://d-nb.info/gnd/117767360>
    <https://d-nb.info/gnd/118574469>
    <https://d-nb.info/gnd/118713507>
    <https://d-nb.info/gnd/117464406>
    <https://d-nb.info/gnd/103770617X>
    <https://d-nb.info/gnd/118810715>
    <https://d-nb.info/gnd/100844979>
    <https://d-nb.info/gnd/118646192>
    <https://d-nb.info/gnd/118528068>
    <https://d-nb.info/gnd/116452145>
    <https://d-nb.info/gnd/118518399>
    <https://d-nb.info/gnd/118540238>
    <https://d-nb.info/gnd/119106698>
    <https://d-nb.info/gnd/104325011>
    <https://d-nb.info/gnd/118658166>
  }
  
  ?gndId gndo:preferredNameForThePerson ?preferredName .
  OPTIONAL { ?gndId gndo:dateOfBirth ?dateOfBirth . }
  OPTIONAL { ?gndId gndo:dateOfDeath ?dateOfDeath . }
  OPTIONAL { ?gndId gndo:placeOfBirth ?placeOfBirth . }
  OPTIONAL { ?gndId gndo:placeOfDeath ?placeOfDeath . }
  OPTIONAL { ?gndId gndo:professionOrOccupation ?professionOrOccupation . }
  OPTIONAL { ?gndId owl:sameAs ?sameAs . }
  OPTIONAL { ?gndId gndo:biographicalOrHistoricalInformation ?bio .}
}
ORDER BY ?gndId
```

The top person in this collection is August von Kotzebue. 
GoTriple contains quite a few resources about him:

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

There are many more results — the search returned over 25 items on the first page alone. Would you like me to retrieve more details on any specific publication, or search for something more specific?

Claude's (Opus 4.8) answer to my question "What do you know about August von Kotzebue in relation to the Hoftheather in Detmold?" is interesting in itself:

```
Let me look into the specific connection rather than rely on general impressions, since the Detmold link is fairly niche.The general results turn up a lot about Kotzebue but nothing tying him specifically to Detmold. Let me look more directly at the Detmold court theatre's history.The honest answer here turns on a chronological point that's worth leading with: there's no direct personal connection between Kotzebue and the Detmold court theatre, because he was dead before it opened.

The timeline makes this clear. Kotzebue was murdered in 1819 by Karl Ludwig Sand, a militant member of the Burschenschaften — stabbed at his home in Mannheim on 23 March of that year. The Detmold Hoftheater, by contrast, didn't exist yet: Prince Leopold II of Lippe decided to have a court theatre built in Detmold, the foundation stone was laid on 18 April 1825, and the curtain rose for the first time on 8 November, with Mozart's "Titus der Gütige" (La clemenza di Tito). So the house opened more than six years after Kotzebue's death. He never visited, directed, or wrote for it — unlike his documented stints running the Vienna court theatre and the German theatre in St. Petersburg.

The real relationship is therefore one of **repertoire**, and it's a strong one. Kotzebue was simply the most-played playwright on German-language stages in exactly the era the Detmold theatre was founded. To give a sense of scale: his roughly 230 plays made up about a quarter of the repertoire of all German-language stages between 1795 and 1825, and his works remained a staple well after his death. From the outset the Detmold programme included both music theatre and spoken drama, and the house quickly built up an extensive repertoire and a good reputation well beyond the borders of the principality — and a "spoken drama" repertoire in the 1820s–1840s would almost inevitably have leaned heavily on Kotzebue, alongside figures like Iffland.

So the accurate framing is: when the Detmold court theatre was filling its stage with the standard German repertoire of the period, Kotzebue's comedies and sentimental dramas (*Menschenhass und Reue*, *Die deutschen Kleinstädter*, and so on) were part of that stock — a posthumous, repertoire-level presence rather than any biographical tie.

One caveat worth flagging for your purposes: I haven't been able to confirm *specific* documented Kotzebue performances at Detmold with dates from these searches. The digitization project covering the Detmold Hoftheater (1825–1875) — the TEI/MEI source-cataloguing effort run through the Lippische Landesbibliothek — would be the place where individual *Theaterzettel* (playbills) and performance materials are indexed. If you want, I can dig into that project's catalogue or spielplan data to see whether specific Kotzebue stagings are recorded. Would that be useful?
```

CKG surfaces information about the Detmolder Hoftheater collection that is not accessible to Claude (even despite Web search). 