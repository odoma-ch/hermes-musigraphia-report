---
title: Harshdeep Singh
---

# Case Studies — Harshdeep Singh

Three multi-step explorations using Quagga Agent across the CKG, Wikidata, DNB, and DIAMM. Each exploration includes the conversation prompts, a shareable link, and a PDF export.

---

## Exploration 1: Johann Sebastian Bach

| Resource | Link |
|----------|------|
| Archived conversation | [PDF export](../assets/chat-archive/Harshdeep_chat_) / [Markdown export](../assets/chat-archive/Harshdeep_chat_) | |

Biographical data, sources, and works across multiple knowledge graphs.


**Prompts:**

- What sources by Bach in Culture Knowledge graph exist, and what incipits do they contain?
- In Wikidata, what are Bach's life dates, image, occupations, and family relationships?
- What musical entries exist for Bach in DNB, and what are their instrumentation and key designations?
- Build a comprehensive profile of Bach spanning sources, biography, and published editions.

| Resource | Link |
|----------|------|
| Live conversation | [quagga-agent.graphia-ssh.eu/s/edfaddf0…](https://quagga-agent.graphia-ssh.eu/s/edfaddf0-62df-45a3-81c1-8ba4ab20b717) |
| PDF export | [bach-sources-and-incipits.pdf](../assets/pdfs/bach-sources-and-incipits.pdf) |

---

## Exploration 2: German Performance Venues

| Resource | Link |
|----------|------|
| Archived conversation | [PDF export](../assets/chat-archive/Harshdeep_chat_) / [Markdown export](../assets/chat-archive/Harshdeep_chat_) | |

CKG performance venues in Germany, enriched with Wikidata coordinates and visualized on a map.

**Prompts:**

- Could you list all the performance venues in CKG which are in Germany
- For these venues, retrieve their coordinates from Wikidata
- Could you make a visualization with a map of these venues using HTML/CSS/JS?

| Resource | Link |
|----------|------|
| Live conversation | [quagga-agent.graphia-ssh.eu/s/0841ec6f…](https://quagga-agent.graphia-ssh.eu/s/0841ec6f-d5e0-422d-8877-51a1c018cce6) |
| PDF export | [ckg-venues-wikidata.pdf](../assets/pdfs/ckg-venues-wikidata.pdf) |
| Interactive map | [Open full screen](../assets/visualizations/german-venues-map.html){ target="_blank" } |

### Interactive map

Quagga Agent generated this Leaflet map from CKG venue data enriched with Wikidata coordinates. Click legend items or venue names in the sidebar to explore.

<iframe
  src="../../assets/visualizations/german-venues-map.html"
  title="CKG performance venues in Germany"
  width="100%"
  height="640"
  style="border: 1px solid var(--md-default-fg-color--lightest); border-radius: 8px; display: block;"
  loading="lazy">
</iframe>

[Open map in full screen](../assets/visualizations/german-venues-map.html){ .md-button .md-button--primary target="_blank" }

---

## Exploration 3: RISM Composers and DIAMM

Cross-graph analysis linking RISM composer records in CKG with DIAMM composition data.

| Resource | Link |
|----------|------|
| Archived conversation | [PDF export](../assets/chat-archive/Harshdeep_chat_) / [Markdown export](../assets/chat-archive/Harshdeep_chat_) | |

**Prompts:**

- Which RISM persons are recorded in CKG as composers, and what are their source counts?
- In the DIAMM graph, which compositions have composer links matching these same persons?
- Is there a correlation between a composer's RISM source count and their DIAMM composition count for these matched persons?
