# 🔎 RAG — Explained Simply

A short, standalone course on Retrieval-Augmented Generation, written for absolute beginners. The stated goal: after reading it, a five-year-old could explain what RAG is.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Sixth entry in the *Explained Simply* series, after [`../4.Webhooks/`](../4.Webhooks/) and [`../5.MCP/`](../5.MCP/). Same deliberately **light** format: 12 short lessons, roughly 45 minutes end to end.

For the deep treatment (vector stores, ChromaDB, hybrid retrieval implementations, agentic RAG, persistent agent memory), see [`../../dev-agentique/rag-memoire-agents/`](../../dev-agentique/rag-memoire-agents/) instead.

Every lesson follows the series' two-card pattern:

- 🔎 **Version 5 ans** — the idea told as a story (the man who read everything two years ago, the library, the index cards)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | Why the model doesn't know your documents (and invents anyway) · "Search first, answer second" · The two phases: indexing vs. querying · The vocabulary in 6 words |
| **2 — How it works** | Chunking, and why it caps everything downstream · Embeddings as a map of meaning (and the three things they can't do) · Hybrid retrieval, reciprocal-rank fusion, reranking as a funnel · Building the final prompt, citations, and licensing failure |
| **3 — What it's for** | 8 concrete use cases and the three conditions they share · Five failure modes and where each is actually fixed — plus when *not* to build a RAG (long context, fine-tuning, SQL) |
| **4 — Two stories** | Léa's support desk (a full afternoon, with the retrieval code and the threshold guard) · Malik's school (a confident wrong answer that went unnoticed for three weeks, diagnosed and fixed in four steps) |

---

## The spine of the course

One diagnostic reflex is repeated throughout, because it saves days: **when an answer is wrong, first look at the retrieved chunks.** If the right passage wasn't there, the model and the prompt are irrelevant — the bug is in retrieval or indexing. Four of the five documented failure modes have nothing to do with the language model.

The second story exists to make one specific point concrete: a RAG cannot natively say *"there's nothing here."* Retrieval always returns its top-k, and a model always writes something. Refusal has to be built — with a score threshold and an explicit failure sentence.

Written against the state of the field as of September 2026: hybrid retrieval as the default, reranking as the highest-return addition, and agentic / self-corrective RAG mentioned as extensions of these fundamentals rather than replacements for them.

---

## Design

| | |
|---|---|
| Palette | Archive green `#14302E` · Searchlight amber `#F5A623` · Jade `#2E9E8F` · Bookmark red `#D95D5D` |
| Typography | Sora (headings) · Karla (body) |
| Signature | The paired "5-year-old / grown-up" cards, ASCII diagrams as amber-tabbed index cards, and progress pips drawn as book spines |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
