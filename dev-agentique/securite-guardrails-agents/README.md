# Agentic AI Security & Guardrails

> **Language:** This course is written in **French**.

A comprehensive self-learning course on securing agentic AI systems in production — covering prompt injection, guardrails frameworks, multi-agent trust, red-teaming, and EU AI Act compliance.

## What's covered

| Module | Topics |
|--------|--------|
| 1 — Fundamentals | Why agents change the security equation, attack surface anatomy, threat modeling, CIA triad for AI |
| 2 — Prompt Injection | Direct injection, indirect injection, jailbreaks, RAG poisoning, multi-layer defenses |
| 3 — Tool Security | Least privilege (PoLP), sandboxing & isolation, tool I/O validation, human-in-the-loop |
| 4 — Guardrails | Guardrails architecture, LlamaGuard, Guardrails AI (Python), PII detection with Presidio |
| 5 — NeMo Guardrails | Colang language, dialog & jailbreak rails, tool rails, production deployment |
| 6 — Multi-agent Trust | Trust propagation, agent-to-agent authentication (JWT/HMAC), inter-agent attacks |
| 7 — Observability | Structured logging, behavioral anomaly detection, immutable audit trails, incident response |
| 8 — Red-teaming | Adversarial methodology, Garak & PyRIT tools, CI/CD security regression tests |
| 9 — Compliance | OWASP Top 10 for LLM (2025 edition), EU AI Act risk classification, enterprise AI governance |
| 10 — Advanced Defense | Defense in depth, circuit breakers & fail-safes, 40-point production deployment checklist |

## How to open

Open `index.html` directly in **Chrome** or **Firefox**. No server or installation needed.

```
MyCourse/dev-agentique/securite-guardrails-agents/index.html
```

Progress is saved automatically in your browser's `localStorage`.

## Content snapshot

- **35 lessons** across 10 modules
- **Fundamentals to advanced** — from attack surface anatomy to enterprise AI governance
- **Code-first** — every lesson includes runnable Python examples
- **Production-ready** — patterns used in real deployments (Docker sandboxing, OTel tracing, LangGraph HITL, CI/CD pipelines)

## Key tools and frameworks covered

| Tool | What it does | Lesson |
|------|-------------|--------|
| **LlamaGuard 3** | Meta's safety classifier for LLM I/O | 4.2 |
| **Guardrails AI** | Python framework for validators & on-fail actions | 4.3 |
| **Microsoft Presidio** | PII detection and anonymization | 4.4 |
| **NeMo Guardrails** | NVIDIA's Colang-based dialog safety framework | 5.1–5.3 |
| **Garak** | Automated LLM vulnerability scanner | 8.2 |
| **PyRIT** | Microsoft's red-teaming orchestration tool | 8.2 |
| **E2B** | Cloud sandboxes for secure code execution | 3.2 |
| **OpenTelemetry** | Distributed tracing for agent sessions | 7.1 |

## Prerequisites

- Basic Python (you should be comfortable reading async code)
- Familiarity with LLM APIs (Anthropic, OpenAI, or similar)
- Some exposure to agentic frameworks (LangChain, LangGraph) is helpful but not required

## Related courses in this series

- [frameworks-orchestration-agents](../frameworks-orchestration-agents/) — LangGraph, LangChain, AutoGen
- [outils-function-calling-mcp](../outils-function-calling-mcp/) — Tool calling and MCP
- [rag-memoire-agents](../rag-memoire-agents/) — RAG and agent memory
