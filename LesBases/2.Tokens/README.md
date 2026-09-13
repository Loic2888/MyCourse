# 🪙 Tokens & Context — Explained Simply

A short, standalone course on tokens, context windows, and what they cost. Written for absolute beginners, with the stated goal that a five-year-old could explain it afterwards.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Second entry in the *Explained Simply* series, right after [`../1.AI/`](../1.AI/). Same deliberately **light** format: 12 short lessons, roughly 45 minutes end to end.

This one is a **foundation under the others**. It explains why RAG exists, why an agent's cost grows quadratically and why it goes amnesiac after compaction, and why you don't connect forty MCP tools "just in case." Several pieces of advice given elsewhere in the series as assertions get their justification here.

Every lesson follows the series' two-card pattern:

- 🪙 **Version 5 ans** — the idea told as a story (puzzle pieces, the work table, the bookmark, the clock on the first line)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

It also adds a visual device the other courses don't have: a **context gauge**, used four times to show what actually fills a request — and to show Amine's before/after.

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | The AI reads pieces, not words (and numbers tokenize badly) · What it costs: output is 4–5× input, and JSON costs 3× CSV · The context window as a work table, and why the advertised limit isn't the usable one · The vocabulary in 6 words |
| **2 — How it works** | The model remembers nothing — it *re-reads*, which is why conversation cost grows quadratically · What actually fills your context (measured, not guessed) · Lost in the middle and context rot · Prompt caching, prefix matching, and the silent invalidators |
| **3 — What it costs** | Reading your bill: the levers in order, free wins before tradeoffs · When the table overflows: truncate, compact, split, or retrieve |
| **4 — Two stories** | Amine's assistant (measured, then fixed in four steps: 2 100 € → 310 €, *and* quality up) · Clara's support bot (seven weeks of zero cache hits caused by one line, found in two minutes) |

---

## The spine of the course

Three claims carry it.

**One:** *the model doesn't remember, it re-reads.* Every turn resends the whole history, so a 40-turn conversation bills ~20× the text the user actually wrote. This single fact explains agent costs, caching's value, and why "new conversation" is an optimization button.

**Two:** *the advertised limit is not the usable limit.* Lesson 7 covers lost-in-the-middle and context rot with the real numbers — accuracy falling 30–50% for mid-context information, degrading well before the window fills. This retroactively justifies the RAG course's top-k advice and the agents course's ordering advice.

**Three:** *token optimizations are silent in both directions.* A working cache looks exactly like a broken one. Clara's story is built on that: one `datetime.now()` at the top of a system prompt, zero cache hits for seven weeks, no error, no slowdown, no quality drop — just a bill 6× the estimate. The fix moves the date rather than deleting it.

Written against the state of the field as of September 2026: frontier context windows up to 1M tokens, input pricing spanning ~$0.14–$10 per M tokens across models, prompt caching saving 50–80%, and the published lost-in-the-middle findings.

---

## Design

| | |
|---|---|
| Palette | Walnut `#2B2118` · Token cyan `#3FA7D6` · Limit raspberry `#D64550` · Cache sage `#62A87C` |
| Typography | Bricolage Grotesque (headings) · Work Sans (body) |
| Signature | The paired "5-year-old / grown-up" cards, the reusable context gauge, and progress pips drawn as coins |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
