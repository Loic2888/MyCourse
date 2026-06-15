# Agentic AI Development — Course Series

A collection of four self-contained, browser-based courses covering the full stack of agentic AI development in 2026: from orchestration frameworks to security hardening.

> **Language:** All courses are written in **French**. READMEs are in English.

---

## Courses

### 1 — [Agent Orchestration Frameworks](./frameworks-orchestration-agents/)
**LangGraph · LangChain · AutoGen**

Build and orchestrate AI agents using the three most widely adopted frameworks in production. From the agent loop fundamentals to multi-agent supervisor architectures.

| | |
|--|--|
| Modules | 7 |
| Lessons | 32 |
| Key tools | LangGraph 1.0, LangChain 0.3.x, AutoGen 1.0 / AG2 |

---

### 2 — [Tools, Function Calling & MCP](./outils-function-calling-mcp/)
**Tool Use · JSON Schema · Model Context Protocol**

Master LLM tool use from first principles, then build and deploy MCP servers that expose your own tools and resources to any MCP-compatible client.

| | |
|--|--|
| Modules | 8 |
| Lessons | 26 |
| Key tools | Anthropic Tool Use API, MCP Python SDK, MCP TypeScript SDK, MCP Inspector |

---

### 3 — [RAG & Agent Memory](./rag-memoire-agents/)
**Vector Stores · ChromaDB · Agentic RAG**

Design and optimize retrieval-augmented generation pipelines and persistent agent memory systems, from basic embeddings to advanced hybrid retrieval and self-correcting RAG agents.

| | |
|--|--|
| Modules | 8 |
| Lessons | 30 |
| Key tools | ChromaDB 0.5.x, FAISS, Qdrant, sentence-transformers, RAGAS, LangGraph Store |

---

### 4 — [Agentic AI Security & Guardrails](./securite-guardrails-agents/)
**Prompt Injection · Guardrails · Red-teaming · EU AI Act**

Secure agentic systems in production: prevent prompt injection and jailbreaks, implement layered guardrails, build multi-agent trust, run adversarial red-team campaigns, and meet regulatory requirements.

| | |
|--|--|
| Modules | 10 |
| Lessons | 35 |
| Key tools | LlamaGuard 3, Guardrails AI, Presidio, NeMo Guardrails, Garak, PyRIT, OpenTelemetry |

---

## How to open any course

Each course is a single self-contained `index.html` file — open it directly in Chrome or Firefox, no server or dependencies needed.

```
MyCourse/dev-agentique/<course-folder>/index.html
```

Progress (completed lessons) is saved automatically in `localStorage` per browser.

---

## Recommended learning path

```
Orchestration Frameworks
        ↓
Tool Use & MCP         ←  Can be taken in parallel
        ↓
RAG & Agent Memory
        ↓
Security & Guardrails  ←  Best taken last (references concepts from the others)
```

Security & Guardrails is intentionally placed last — it assumes you understand how agents work, what tools are, and what RAG means, so the threat models and defenses are grounded in real architectural context.

---

## Prerequisites (all courses)

- Python 3.11+
- Familiarity with LLM APIs (Anthropic or OpenAI)
- Basic understanding of async Python is helpful

Last updated: **June 2026**
