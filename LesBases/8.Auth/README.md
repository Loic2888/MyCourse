# 🔑 Authentication — Explained Simply

A short, standalone course on authentication, written for absolute beginners. The stated goal: after reading it, a five-year-old could explain what it is.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Eighth and last entry in the *Explained Simply* series. Same deliberately **light** format: 12 short lessons, roughly 45 minutes end to end.

Where the other seven each explain one system, this one fills the **gap running underneath four of them**: the webhook signature, the MCP server's token and consent screen, the RAG access filter, the agent's least-privilege scope. Each of those was gestured at elsewhere and explained nowhere. This is that lesson — placed last on purpose, as the closing layer over everything before it.

Every lesson follows the series' two-card pattern:

- 🔑 **Version 5 ans** — the idea told as a story (the theme park gate, the festival wristband, the valet key, the note pinned to the front door)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | Who are you ≠ are you allowed (with the IDOR bug that follows from confusing them) · The three factors, and why not all second factors are equal · Passwords: hashing, salting, and what current advice actually says · The vocabulary in 6 words |
| **2 — How it works** | Sessions and cookies: the festival wristband, and the three attributes that matter · Tokens: signed ≠ encrypted, and the revocation problem solved by the two-token pattern · OAuth as the valet key, plus OIDC and the AI-agent tie-in · Machine-to-machine: API keys, the five rules, and where secrets must never live |
| **3 — Where it's going** | Passkeys: how they kill phishing, the real adoption numbers, and the recovery problem nobody has solved · 8 ways people actually get compromised — none of which involve breaking cryptography |
| **4 — Two stories** | Yann's SaaS (a clean design, and the Thursday an employee left) · Inès's startup (a key pushed to a public repo, found in 50 seconds, and the "fix" that fixed nothing) |

---

## The spine of the course

Two claims carry the whole thing.

**One:** *being authenticated is not being authorized.* Lesson 1 opens on it, shows the four-line bug it produces — one of the most common web vulnerabilities there is — and every later lesson re-applies it. Lesson 11 shows both questions being asked, in order, on every request.

**Two:** *a system is only as strong as its weakest path.* An unbreakable passkey with SMS account recovery has the security of SMS. That reasoning drives Lesson 9's honest treatment of passkeys — they genuinely end phishing, and account recovery remains unsolved — and Lesson 10's list of eight real-world compromises, none of which attack the cryptography.

Inès's story exists to teach one counterintuitive fact: **removing a secret from a file does not remove it from Git.** The commit stays. The only valid response to a pushed secret is to revoke and replace it.

Written against the state of the field as of September 2026: 15B+ passkey-enabled accounts, passkey sign-ins at 93% success vs. 63% for passwords, ecosystem fragmentation and account recovery as the two adoption blockers, and OAuth 2.1 emerging as the baseline for authenticating AI agents.

---

## Design

| | |
|---|---|
| Palette | Oxblood `#331222` · Lock crimson `#E8455F` · Badge blue `#4DA8DA` · Granted green `#47B881` |
| Typography | Manrope (headings) · Public Sans (body) |
| Signature | The paired "5-year-old / grown-up" cards, crimson-tabbed ASCII diagrams, and progress pips drawn as padlocks that spring open |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
