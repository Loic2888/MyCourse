# MyCourse

A personal repository of complete, self-contained courses on topics I find worth studying deeply — built with a custom Claude Code skill and designed to run entirely in the browser.

> **Note:** All course content is written in **French**. READMEs are in English.

---

## How it works

Each course is a **single standalone HTML file** — no server, no dependencies, no setup.

To open a course:
1. Navigate into any course folder
2. Open `index.html` directly in **Chrome** or Firefox
3. That's it — everything runs in your browser

Every course includes:
- Sidebar navigation with modules and lessons
- Progress tracking saved in your browser (`localStorage`)
- Syntax-highlighted code examples
- Pitfall callouts, defense/attack badges, and exercises
- Mobile-friendly layout

---

## Course Themes

### 🤖 Agentic AI Development — [`dev-agentique/`](./dev-agentique/)

The first theme in this repository. Four courses covering the full stack of building and securing AI agents in production.

| Course | Description | Modules | Lessons |
|--------|-------------|---------|---------|
| [Agent Orchestration Frameworks](./dev-agentique/frameworks-orchestration-agents/) | LangGraph, LangChain, AutoGen — agent loops, multi-agent architectures, production patterns | 7 | 32 |
| [Tools, Function Calling & MCP](./dev-agentique/outils-function-calling-mcp/) | LLM tool use from first principles, building MCP servers (Python & TypeScript) | 8 | 26 |
| [RAG & Agent Memory](./dev-agentique/rag-memoire-agents/) | Vector stores, ChromaDB, hybrid retrieval, agentic RAG, persistent memory | 8 | 30 |
| [Agentic AI Security & Guardrails](./dev-agentique/securite-guardrails-agents/) | Prompt injection, LlamaGuard, NeMo, red-teaming, EU AI Act, defense in depth | 10 | 35 |

→ See [`dev-agentique/README.md`](./dev-agentique/README.md) for the recommended learning path and full details.

---

### 📊 Data for AI — [`data-for-ai/`](./data-for-ai/)

A 25-course curriculum on preparing data for AI systems, organized into 7 progressive blocks — from foundational SQL/Python/statistics, through classic data cleaning, RAG data prep, unstructured data, agent-ready data, fine-tuning datasets, up to production-grade data tooling.

| Block | Theme |
|-------|-------|
| 1 | Data Foundations (prerequisites) |
| 2 | Classic Data Cleaning |
| 3 | Data Preparation for RAG |
| 4 | Unstructured Data |
| 5 | Data Preparation for AI Agents |
| 6 | Data Preparation for Fine-Tuning |
| 7 | Tooling and Industrialization |

→ See [`data-for-ai/README.md`](./data-for-ai/README.md) for the full list of all 25 courses.

---

### 🧩 Explained Simply — [`LesBases/`](./LesBases/)

Nine deliberately light, one-sitting courses, each explaining a single concept from zero with the stated goal that a five-year-old could explain it afterwards. Every lesson pairs a plain-language story with its technical equivalent, and ends on two fully worked fictional case studies — one that goes well, one that goes wrong. Folder numbers are reading order.

| # | Course | Description | Lessons |
|---|--------|-------------|---------|
| 1 | [AI](./LesBases/1.AI/) | How a language model actually works: next-word prediction, lossy compression, why it invents with confidence, what it can't know about itself | 12 |
| 2 | [Tokens & Context](./LesBases/2.Tokens/) | What the model actually reads and what it costs: tokenization, the context window, lost-in-the-middle, prompt caching | 12 |
| 3 | [Talking to AI](./LesBases/3.Prompt/) | Writing good prompts: the four ingredients, why magic formulas don't work, and when rewriting won't help | 12 |
| 4 | [Terminal & CLIs](./LesBases/4.CLI/) | An AI can't click a button but can write a command — how that one fact turns a task into something delegable, repeatable and schedulable | 12 |
| 5 | [Webhooks](./LesBases/5.Webhooks/) | What a webhook is, how it works step by step, what it's for, and why duplicates are the hard part | 12 |
| 6 | [MCP](./LesBases/6.MCP/) | The Model Context Protocol as a universal plug: hosts and servers, tools/resources/prompts, transports, and the security rules that matter | 12 |
| 7 | [RAG](./LesBases/7.RAG/) | Retrieval-Augmented Generation as a librarian: chunking, embeddings, hybrid search, and why refusing to answer must be built | 12 |
| 8 | [AI Agents](./LesBases/8.Agents/) | The recipe vs. the cook: the loop, tools, memory, the five brakes, and when a workflow is the better answer | 12 |
| 9 | [Authentication](./LesBases/9.Auth/) | Who you are vs. what you may do: passwords, sessions, tokens, OAuth, API keys, passkeys, and how people actually get compromised | 12 |

**Two reading paths, and a bridge.** The first three need no technical background at all. The fourth is the step between the two halves. The next four are the technical building blocks, in the order each leans on the last; the ninth is a closing layer over all of it.

- **No technical background** — read **1 → 2 → 3**: how a model works, what it reads and costs, and how to talk to it. Nothing in that path requires writing code.
- **The bridge** — **4 (Terminal & CLIs)**. Not a dev course: it explains *how an AI actually acts on the world*, since it can write a command but cannot click a button. Read it even if you stop there — it's what turns a task you do by hand into one you can delegate.
- **If you build things** — continue **5 → 6 → 7 → 8 → 9**: Webhooks first (the most self-contained building block), then MCP (tools) and RAG (memory) which both lean on it, then Agents (the loop that combines all three), then Auth as the closing layer underneath everything.

**How they fit.** [AI](./LesBases/1.AI/) is the foundation — everything else is engineering around one limitation: *the model doesn't know that it doesn't know.* [Tokens & context](./LesBases/2.Tokens/) describe the table you put things on. [Talking to AI](./LesBases/3.Prompt/) turns that foundation into practice. [Terminal & CLIs](./LesBases/4.CLI/) is where a model stops explaining and starts *doing*: it can't click a button, but it can write a command. [Webhooks](./LesBases/5.Webhooks/) wake a system up or report what it did. [MCP](./LesBases/6.MCP/) plugs in tools for what the model does badly. [RAG](./LesBases/7.RAG/) converts recall into transformation at scale. [Agents](./LesBases/8.Agents/) are the loop that combines tools, memory and triggers to fetch what's missing instead of guessing — and that loop, at ground level, is the terminal one: write an action, read the result, correct. [Authentication](./LesBases/9.Auth/) decides what any of it may reach — the webhook signature, the MCP token, the RAG access filter, the agent's least-privilege scope are all this one lesson, seen four times before it's finally named.

→ Each course ends on a production checklist — see the per-course READMEs for the outlines.

---

## How courses are generated

Each course is produced by a custom `create-course` skill built in Claude Code that:
1. Maps the subject into modules and lessons (fundamentals → advanced)
2. Chooses a visual identity tailored to the topic
3. Writes each lesson in depth (concepts, real code examples, pitfalls, exercises)
4. Assembles everything into a single self-contained HTML file

To generate a new course, run the `create-course` skill in Claude Code and specify the output path.

---

## Repository structure

```
MyCourse/
├── dev-agentique/              ← Theme: Agentic AI Development
│   ├── README.md
│   ├── frameworks-orchestration-agents/
│   │   └── index.html
│   ├── outils-function-calling-mcp/
│   │   └── index.html
│   ├── rag-memoire-agents/
│   │   └── index.html
│   └── securite-guardrails-agents/
│       └── index.html
├── data-for-ai/                 ← Theme: Data for AI (7 blocks, 25 courses)
│   ├── README.md
│   ├── 1.fondations-data/
│   ├── 2.data-cleaning-classique/
│   ├── 3.prepa-data-pour-RAG/
│   ├── 4.data-non-structurées/
│   ├── 5.prepa-data-for-agent-IA/
│   ├── 6.prepa-data-for-fine-tuning/
│   └── 7.outillage-industrialisation/
└── LesBases/                    ← Theme: Explained Simply (9 short courses, numbered in reading order)
    ├── 1.AI/
    ├── 2.Tokens/
    ├── 3.Prompt/
    ├── 4.CLI/
    ├── 5.Webhooks/
    ├── 6.MCP/
    ├── 7.RAG/
    ├── 8.Agents/
    └── 9.Auth/              (each: README.md + index.html)
```

Last updated: **September 2026**
