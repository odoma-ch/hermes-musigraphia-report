---
title: Olga Velichkina
---

# Case Studies — Olga Velichkina

Three explorations testing Quagga Agent on Irish traditional music topics across The Session, MusicBrainz, GoTriple, and Wikidata. Each study includes a critical assessment of agent reasoning and knowledge-graph coverage.

---

## Exploration 1: Down by the Salley Gardens

| Resource | Link |
|----------|------|
| Archived conversation | [PDF export](../assets/chat-archive/Olga_chat_Salley-Gardens.pdf) / [Markdown export](../assets/chat-archive/Olga_chat_Salley-Gardens.md) | |

The Irish folk song *Down by the Salley Gardens* is known to most
musicians through the version arranged by Benjamin Britten on the poem
by W. B. Yeats (see [this annex](../assets/pdfs/Down-by-the-Salley_TheSession.pdf) for additional information about this song). I wanted to learn more about the origin of this song,
its recorded and notated versions, its sources, and its poetic texts. An
important point is that folk songs frequently exist in many melodic and
textual versions, and their titles do not always match. Britten chose a
version associated with Yeats\'s poem, but the same melody is also known
with another text, *The Maids of the Mourne Shore*/*Moorlough Shore*.

The search process was rather slow, and some important sources were
absent from the knowledge graph (KG), such as the Roud Folk Song Index,
one of the most important sources for song texts. The agent was able to
retrieve information about editions of Britten's arrangement, which
appeared in two anthologies: *Folksong Arrangements, Volume 1: British
Isles* and *Britten: Complete Folksong Arrangements (High)* in the UTSI
graph. It then claimed that TheSession database does not contain this
song (under either title, *The Salley Gardens* or *Moorlough Shore*),
which is entirely incorrect. A simple search on TheSession.org shows
otherwise.

In a second round, the agent acknowledged that the song is present in
TheSession and identified two entries, nos. 1314 and 98, asserting that
they represent the same tune. This is, again, incorrect: a simple
musical analysis reveals that these are two completely different
melodies, coincidentally associated with the same title (although
spelled slightly differently: *Salley* and *Sally*). What is troubling
here is that the agent attempted to justify its conclusion:

> "The key finding is that tune 1314
> (<https://thesession.org/tunes/1314>) carries both 'Down By The Sally
> Gardens' and 'The Maids of the Mourne Shore' as names for the same
> tune --- confirming they are the same air/melody under different
> titles. This is consistent with the well-known tradition that the air
> 'The Maids of the Mourne Shore' was repurposed by W. B. Yeats for the
> poem 'Down by the Salley Gardens.'"
>
> "Tune 1314 has 9 settings (melodic variants, linked via P747), and
> tune 98 has 8 settings. Both are in the The Session graph."

The wording is suspicious. A human would never say "consistent with a
well-known tradition" in this context; one may speak of a fact here, but
not of a tradition. Moreover, the air was not "repurposed" by Yeats, who
had nothing to do with the use of his poem with this melody.

On a subsequent query, the agent offered another false argument:

"There is no direct link between the two tunes, but there is an indirect
relationship: they co-appear in three shared tunesets."

According to the agent, this reflected "their real-world melodic
kinship."

The problem with this argument is that tunesets are compiled by users,
and the logic or motivation behind these compilations is entirely
subjective. No conclusions about relationships between tunes can be
drawn simply from their co-occurrence in user-created sets.

Finally, the agent explained that it could not draw conclusions about
melodic relationships between tunes on the basis of the data available
to it, since it had access only to metadata and not to incipits or
musical notation. This is correct, but it could have been stated much
earlier.

Looking back on this interaction, I realize that my questions were
formulated rather awkwardly, since I myself knew little about the topic
and was merely exploring it. I asked about the origin of the song and
its traditional version, meaning the earlier (pre-Yeats) version
associated with the title *The Mourne Shore*. The agent searched for the
phrase "Irish traditional" and found it in a recent work by the American
composer John Corigliano (*Three Irish Folksong Settings*), who produced
his own arrangement of Britten's song. The designation "Irish
traditional" appeared in the "author" field, which the agent interpreted
as an explicit reference to a traditional version. In fact, however, the
answer was unsatisfactory, since this was simply another arrangement of
the same tune.

In short, the limitations of the original KG (lack of data, such as
musical notation or incipits, and inconsistencies in field completion),
the agent's faulty reasoning, and my own lack of experience in
formulating effective prompts all contributed to the limited results of
this search.

---

## Exploration 2: Music for the Irish (Celtic) Harp

| Resource | Link |
|----------|------|
| Archived conversation | [PDF export](../assets/chat-archive/Olga_chat_Celtic-Harp-Composers.pdf) / [Markdown export](../assets/chat-archive/Olga_chat_Celtic-Harp-Composers.md) | |

The task was to identify as many sources as possible relating to the
historical and modern repertoire of the Irish (Celtic) harp (clarsach).
Initially, I requested a list of composers who used the Irish harp in
their music. QUAGGA compiled a list of 53 composers and performers based
on the MusicBrainz KG. This list included several groups as well as a
number of kora players (or so it appeared). On the other hand, some
well-known composers and performers whom I expected to find, such as
Turlough O'Carolan (an eighteenth-century Irish composer) and Alain
Stivell (a modern Breton interpreter of Celtic harp music), were absent.

O'Carolan: a second query specifically requesting a list of his works
returned a substantial number of entries from the KG. However, because
QUAGGA had not identified him as a composer who wrote specifically for
the Irish harp, he was omitted from the first list. It should also be
noted that searching simply for "Carolan," rather than "Turlough
O'Carolan," produced unrelated results (e.g., The Session tunes nos.
5842 and 78830, and probably many others, which would require manual
verification).

This search was not completed because the system crashed when I asked a
question requiring both GoTriple and Wikidata. The error message was:

"\<Response payload is not completed: \<TransferEncodingError: 400,
message=\'Not enough data to satisfy transfer length header.\'\>"

---

## Exploration 3: Tunes in 7/8 Time

| Resource | Link |
|----------|------|
| Live conversation | [TODO]() |
| PDF export | [](../assets/pdfs/) |

I requested a complete list of pieces in 7/8 time in order to examine
their geographical and historical distribution across different European
musical traditions. The agent identified 170 tunes, all of them from The
Session. This result seemed counterintuitive from the outset, since it
is well known that this meter is highly untypical of Irish traditional
music.

The agent explained that:

"The time signature is encoded via the Wikidata property P3440 (time
signature) pointing to entity Q50353331 (7/8)."

However, checking the listed examples revealed that most of them were
actually in 3/2 rather than 7/8. One exception was the Greek tune
*Kalamatianos*, which indeed uses a 7/8 meter, but it is clearly an
exception within The Session corpus. We went through several rounds of
questioning, but the incorrect answer persisted.

When I eventually asked what entity Q50353331 actually represented in
Wikidata, the agent suddenly arrived at the following conclusion:

> "The entity Q50353331 is labeled '3/2' (three-two time signature) in
> Wikidata --- not '7/8'. This confirms your earlier observation that
> the 170 tunes previously listed under Q50353331 are actually in 3/2
> meter, not 7/8. The Wikidata URI Q50353331 represents the 3/2 time
> signature, meaning the data in The Session graph that links those
> tunes to Q50353331 is consistent with 3/2, not 7/8."

I cannot determine the reason for this persistent error.

Overall, the agent needs to improve both its speed and the reliability
of its answers. Part of the problem appears to stem from deficiencies in
the underlying KG, but some issues are clearly attributable to the
agent's reasoning processes.
