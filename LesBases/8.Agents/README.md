# 🔁 AI Agents — Explained Simply

A short, standalone course on AI agents, written for absolute beginners. The stated goal: after reading it, a five-year-old could explain what an agent is.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Eighth entry in the *Explained Simply* series — the capstone of the technical building blocks — after [`../5.Webhooks/`](../5.Webhooks/), [`../6.MCP/`](../6.MCP/) and [`../7.RAG/`](../7.RAG/). Same deliberately **light** format: 12 short lessons, roughly 45 minutes end to end.

It also closes the series: **the agent is the loop, MCP gives it tools, RAG gives it long-term memory, and webhooks wake it or report what it did.** Each of the other three answers a question this one raises.

For the deep treatment (LangGraph, AutoGen, multi-agent architectures, production patterns), see [`../../dev-agentique/frameworks-orchestration-agents/`](../../dev-agentique/frameworks-orchestration-agents/) instead.

Every lesson follows the series' two-card pattern:

- 🤖 **Version 5 ans** — the idea told as a story (the man with no arms, the recipe versus the cook, the stuck drawer)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | A model can only talk (the harness has the hands) · Recipe vs. cook: who decides the next step · The four ingredients, and which exits you have to write yourself · The vocabulary in 6 words |
| **2 — How it works** | The ReAct loop shown as a real five-turn trace, plus the 20-line harness · Tools: five rules, and why error messages are your main steering wheel · Memory: the context fills up, the three kinds of memory, compaction and what it costs · The five brakes, and the irreversibility test |
| **3 — What it's for** | The three autonomy levels and 8 proven use cases, plus what the working ones have in common · When *not* to build an agent — the unpopular lesson |
| **4 — Two stories** | Sofia's accounting firm (invoice triage that works, including the invoice it correctly refuses) · Karim's agency (an agent that looped 2,300 times overnight, diagnosed and fixed in five changes) |

---

## The spine of the course

Two claims are repeated until they stick.

**One:** *who decides the next step?* That single question separates a workflow from an agent, and Lesson 10 argues — at some length — that most projects framed as "we need an agent" are workflows nobody wanted to write. The cost table there is the honest version: variable spend, non-reproducible runs, and no straightforward way to test in CI.

**Two:** *an agent has no sense that it's going in circles.* No fatigue, no feeling that three hours have passed. Three of the four ways out of the loop — turn cap, budget, human approval — are code you write yourself. Karim's story exists to make that concrete: nothing was broken, every individual turn was reasonable, and the whole incident traces back to one silent error message and four missing brakes.

Written against the state of the field as of September 2026: ReAct loops, the three autonomy levels, plan-execute and evaluator-optimizer patterns, human approval on irreversible actions, and prompt injection through agent-read external content.

---

## Design

| | |
|---|---|
| Palette | Graphite `#23252C` · Loop coral `#FF6B6B` · Brass `#E0A93B` · Approval mint `#3FBF8F` |
| Typography | Space Grotesk (headings) · IBM Plex Sans (body) |
| Signature | The paired "5-year-old / grown-up" cards, coral-tabbed ASCII traces, and progress pips drawn as circular arrows |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
