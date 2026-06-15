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
└── dev-agentique/              ← Theme: Agentic AI Development
    ├── README.md
    ├── frameworks-orchestration-agents/
    │   └── index.html
    ├── outils-function-calling-mcp/
    │   └── index.html
    ├── rag-memoire-agents/
    │   └── index.html
    └── securite-guardrails-agents/
        └── index.html
```

Last updated: **June 2026**
