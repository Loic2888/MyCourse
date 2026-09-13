# 🦜 AI — Explained Simply

A short, standalone course on how language models actually work. Written for absolute beginners, with the stated goal that a five-year-old could explain it afterwards.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

First entry in the *Explained Simply* series, and its foundation. Everything else is engineering around one limitation: **the model doesn't know that it doesn't know.** [Tokens & context](../2.Tokens/) describe the table you put it all on. [Prompt](../3.Prompt/) turns this course into practice. RAG converts recall into transformation. MCP and tools give access to things that actually compute and verify. An agent is the loop that fetches what it's missing instead of guessing. Auth decides what any of it may reach.

It all comes from one sentence: *the model doesn't know that it doesn't know.*

Every lesson follows the series' two-card pattern:

- 🦜 **Version 5 ans** — the idea told as a story (the parrot that heard everything, the loaded die, the invented reference)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

It also adds its own visual device: a **probability distribution** showing what the model "thinks" before each word — used three times, including once on a question whose answer doesn't exist, to show that nothing in the distribution flags ignorance.

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | The parrot that read everything (and what the analogy gets wrong) · Predicting the next word, and why that turns out to be enough · The three lives of a model: pretraining, post-training, inference — and why it learns nothing from you · The vocabulary in 6 words |
| **2 — How it works** | What it actually kept: lossy compression, not a database (plus mixture-of-experts) · The loaded die: sampling and temperature · Why it invents with total confidence · **What "next-token prediction" doesn't explain** — post-training, implicit plans, reasoning models |
| **3 — What it can and can't do** | Transformation vs. recall: the single best predictor of success, and how to convert one into the other · What it cannot know about itself — and why asking "are you sure?" measures nothing |
| **4 — Two stories** | Hugo's interviews (42 transcripts, mechanically verified citations, zero false quotes in the paper) · Nora's report (six perfectly formatted references: three real, two misattributed, one that never existed) |

---

## The spine of the course

**Transformation vs. recall** is the practical takeaway. Give the model the text and ask it to do something with it, and it excels. Ask it to retrieve something from its parameters, and it reconstructs. Lesson 9 shows that most recall tasks can be *converted* into transformation tasks — which is precisely what RAG, tools and agents do.

**It has no signal for ignorance** is the mechanical core. Lesson 7 shows a probability distribution for a question about a document that doesn't exist: it looks entirely ordinary. Lesson 10 follows through — "are you sure?" tests compliance, not certainty; confidence scores are tokens, not measurements.

Lesson 8 is deliberately a **correction of the course itself**: "next-token predictor" is accurate for pretraining and increasingly incomplete for the model you actually use, since post-training optimizes whole responses rather than single tokens. The honest conclusion offered: keep the parrot as a *risk detector*, not as a *capability measure*.

Nora's story is the whole course in one failure: the *form* of a citation is a heavily repeated pattern and survives compression perfectly; individual citations appear once or twice and don't. So the model fills a perfect form with invented content — and nothing in the text or the tone distinguishes it from a real one.

---

## Design

| | |
|---|---|
| Palette | Petrol `#10303C` · Probability magenta `#E0479E` · Gold `#F0A202` · Verified green `#4C9F70` |
| Typography | Chivo (headings) · Rubik (body) |
| Signature | The paired "5-year-old / grown-up" cards, the probability-distribution component, and progress pips drawn as tiny histograms |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
