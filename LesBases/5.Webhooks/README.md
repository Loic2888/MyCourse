# 🔔 Webhooks — Explained Simply

A short, standalone course on webhooks, written for absolute beginners. The stated goal: after reading it, a five-year-old could explain what a webhook is.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Fifth entry in the *Explained Simply* series, and the first of the technical building blocks proper — MCP, RAG and Agents each lean on it later. Deliberately **light** — 12 short lessons, roughly 45 minutes end to end. It trades exhaustiveness for clarity.

Every lesson follows the same two-card pattern, which is the course's visual signature:

- 🧸 **Version 5 ans** — the idea told as a story (the postman, the doorbell, the cake in the oven)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | The doorbell and the postman · The cost of polling · "Just tell me when" · The vocabulary in 6 words |
| **2 — How it works** | The 5 steps end to end · Inside the envelope (JSON & headers) · Saying "got it" (HTTP status codes) · Retries, duplicates, idempotency & HMAC signatures |
| **3 — What it's for** | 8 everyday use cases · Webhook vs API (and WebSocket, SSE, message queues) |
| **4 — Two stories** | Léo's pizzeria (a full evening, minute by minute) · Mia's candy shop (a duplicate-delivery incident, diagnosed and fixed) |

The two final lessons are fully worked fictional case studies: real payloads, real handler code, a real bug with its timeline, diagnosis, and three-part fix.

---

## Takeaways

Ends with a production checklist covering the things that actually break in the wild: verifying the raw-body signature, answering `200` before doing slow work, durable storage before acknowledging, unique-constraint deduplication, idempotent processing, ignoring unknown event types, and nightly reconciliation as a safety net.

---

## Design

| | |
|---|---|
| Palette | Midnight `#151A3A` · Signal orange `#FF6B35` · Turquoise `#17BEBB` · Envelope yellow `#FFC94A` |
| Typography | Baloo 2 (headings) · Nunito (body) |
| Signature | The paired "5-year-old / grown-up" cards, plus ASCII sequence diagrams on midnight cards |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
