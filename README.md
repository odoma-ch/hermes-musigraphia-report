# HERMES Data Challenge 2026 — Team MusiGraphia

Quagga Agent is an LLM-powered conversational agent that enables researchers to explore musicological knowledge in the Culture Knowledge Graph (CKG) and beyond — without requiring any SPARQL expertise. Built on a LangGraph multi-agent architecture for backend and OpenWebUI interface, it accepts natural-language research questions, autonomously identifies the relevant knowledge graph, retrieves and understands its schema through a systematic exploration phase, generates and executes SPARQL queries, and returns verified, structured results. The agent uses a two-phase SPARQL subagent pipeline: an exploration phase that discovers entity types, properties, and relationship patterns to produce a cached structural report of the KG, and an answer phase that uses this context — along with iterative query validation and self-correction — to ground SPARQL generation in the actual ontology rather than LLM hallucination. A tiered LLM stack with automatic health-based failover ensures operational resilience.

A key design principle of Quagga Agent is scientific transparency. Rather than abstracting away the underlying technical machinery, the agent surfaces the SPARQL query used to answer the user question, allowing users to inspect, verify, and learn from it. Corresponding tool calls are also visible in the OpenWebUI interface, and conversations can be exported for sharing or reproducibility. This reflects a broader philosophy: the goal is not to replace SPARQL, but to lower the barrier to entry while fostering a gradual understanding of how knowledge graphs are queried. Trust in AI-generated answers is built not through opacity but through legibility and provenance.

Current limitations point to directions for ongoing work. The agent often inserts "helpful" information not contained in the graph; these statements appear correct in most cases checked, but their reliability is difficult to predict. Some graphs contain only flat metadata, and underlying datasets include errors that propagate into answers. Retrieval failures remain a concern: queries sometimes time out or fail silently — for instance, when searching across multiple subgraphs in LinkedMusic, timeouts in MusicBrainz or Wikidata can make it appear as though those sources contain no relevant information. Additional limitations include single-KG query scope, result size caps, and language bias. Addressing these shortcomings — through automatic cross-KG federation, other KGs integrated, and improved retrieval robustness — will drive the next phase of development.

## Team Explorations

Each team member (Harshdeep Singh, Polina Proutskova, Olga Velichkina, Matteo Romanello) have shared some of their explorations with links to their conversations with the agent. These can be explored in detail by reading the README in each team member's folder and following the links to the agent conversations mentioned there.

The conversation links require a registered account on the agent. To sign up and access them:

1. Go to [quagga.graphia-ssh.eu/agent](https://quagga.graphia-ssh.eu/agent)
2. Log in with GitHub, ORCID, or OPERAS
3. Once signed in, you can try accessing the links to the chats mentioned in each folder
4. If you run into problems accessing the agent or a link, reach out to `harshdeep.singh@odoma.ch`

## hermes-musigraphia-report

Technical report and case studies for the **HERMES Data Challenge 2026** — Team **MusiGraphia**.

### Published site

Once GitHub Pages is enabled, the report is available at:

**https://odoma-ch.github.io/hermes-musigraphia-report/**

### Local development

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) to preview the site.

### Project structure

```
docs/                  MkDocs source (published content)
├── index.md           Landing page
├── technical-report/  System architecture and approach
├── explorations/      Musicological case studies
├── benchmarks.md      Challenge benchmark trials
└── assets/            PDFs and CSV data files
mkdocs.yml             Site configuration
requirements.txt       Python dependencies
```

Legacy source files (`TECHNICAL_REPORT.md`, `Harshdeep/`, `Polina/`, `Matteo/`, `data/`) remain in the repo root for reference; the canonical published content lives under `docs/`.

### GitHub Pages setup

After pushing to `main`:

1. Go to **Settings → Pages** in the GitHub repository
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**
3. Select branch **`gh-pages`**, folder **`/ (root)`**
4. The GitHub Action (`.github/workflows/docs.yml`) deploys automatically on every push to `main`

## Team

Harshdeep Singh · Polina Proutskova · Olga Velichkina · Matteo Romanello
