---
title: Home
---

# Quagga Agent — From Notes to Nodes

**HERMES Data Challenge 2026** · Team **MusiGraphia**

| | |
|---|---|
| **Challenge** | [HERMES Data Challenge 2026 — "From Notes to Nodes"](https://hermes.nfdi4culture.de/) |
| **Team** | MusiGraphia |
| **Members** | Harshdeep Singh, Polina Proutskova, Olga Velichkina, Matteo Romanello |
| **System** | [Quagga Agent](https://quagga-agent.graphia-ssh.eu/) — LLM-powered exploration of the [Culture Knowledge Graph (CKG)](https://nfdi4culture.de/) |

## Overview

**Quagga Agent** is a conversational AI that lets musicologists query the Culture Knowledge Graph — and other music-related knowledge graphs — in plain language, without writing SPARQL. Given a research question, the agent identifies the relevant graph, discovers its schema, generates and executes SPARQL queries, validates the results, and returns a structured answer alongside the query used to produce it.

The agent was developed within the EU-funded [GRAPHIA](https://graphia-ssh.eu/) project (grant 101188018) and adapted for this challenge to cover CKG datasets including RISM, musiconn.performance, APSearch, and the Detmolder Hoftheater.

## Contents

- **[Technical note](technical-report/index.md)** — in-depth technical documentation of the agent: architecture, SPARQL pipeline, musicological adequacy, UX, and known limitations
- **[Explorations](explorations/index.md)** — case studies on Bach sources, German venues, Russian operas, Irish traditional music, court theatre repertoire, and more. Team members bring complementary backgrounds spanning AI, musicology, and ethnomusicology; the explorations reflect this diversity, with research questions ranging from technical system probes to substantive musicological inquiries
- **[Team](team.md)** — MusiGraphia team members

## Try the agent

The live system is at **[quagga-agent.graphia-ssh.eu](https://quagga-agent.graphia-ssh.eu/)**. Every answer includes the SPARQL query used; conversations can be shared via link or exported as PDF/JSON.
