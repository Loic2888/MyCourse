# 🔌 MCP — Explained Simply

A short, standalone course on the Model Context Protocol, written for absolute beginners. The stated goal: after reading it, a five-year-old could explain what MCP is.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Fifth entry in the *Explained Simply* series, right after [`../4.Webhooks/`](../4.Webhooks/) — same deliberately **light** format: 12 short lessons, roughly 45 minutes end to end. It trades exhaustiveness for clarity.

For the deep treatment (building MCP servers in Python and TypeScript, function calling from first principles), see [`../../dev-agentique/outils-function-calling-mcp/`](../../dev-agentique/outils-function-calling-mcp/) instead.

Every lesson follows the series' two-card pattern:

- 🔌 **Version 5 ans** — the idea told as a story (the universal plug, the appliances, the doorbell)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | The M×N problem (a thousand different plugs) · MCP as the universal plug · Host, client, server · The vocabulary in 6 words |
| **2 — How it works** | A server's three gifts: tools, resources, prompts · The two transports (stdio & Streamable HTTP) · A full conversation in JSON-RPC, plus elicitation |
| **3 — What it's for** | 8 concrete use cases · MCP vs API vs webhook (discovery is the real difference) · The golden rule: you're the one who says yes |
| **4 — Two stories** | Nina's library (a full morning at the desk, with the server's Python source) · Tom's travel agency (a prompt-injection data leak, diagnosed and fixed in five steps) |

---

## Accuracy note

Written against spec revision **2026-07-28**, verified against the published specification rather than from memory. That revision matters: the protocol core became **stateless** (no `initialize` handshake, capabilities travel per-request), and both **Sampling** and **Roots** were deprecated — so this course covers neither, unlike most material written earlier.

Covered as current: JSON-RPC 2.0 messages · server primitives tools / resources / prompts · client-side elicitation · stdio and Streamable HTTP transports · the Tasks, Skills-over-MCP and MCP Apps extensions, mentioned by name only.

---

## Design

| | |
|---|---|
| Palette | Plum `#241634` · Electric violet `#8B5CF6` · Lime `#A3D93B` · Copper `#E8A33D` |
| Typography | Outfit (headings) · Inter (body) |
| Signature | The paired "5-year-old / grown-up" cards, ASCII sequence diagrams on plum cards, and progress pips drawn as two-pin plugs |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
