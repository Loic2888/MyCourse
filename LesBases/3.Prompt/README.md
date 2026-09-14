# 💬 Talking to AI — Explained Simply

A short, standalone course on writing good prompts. Written for absolute beginners, with the stated goal that a five-year-old could explain it afterwards.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Third entry in the *Explained Simply* series, right after [`../1.AI/`](../1.AI/) and [`../2.Tokens/`](../2.Tokens/) — and the **most immediately useful course of the nine, with no technical prerequisite at all**: no server, no API, no code. It's the practical counterpart to AI: that course explains *why* the model invents and why it's good at transformation and bad at recall; this one turns that into what to actually type.

Every lesson follows the series' two-card pattern:

- 💬 **Version 5 ans** — the idea told as a story (the brilliant intern on day one, the folded napkin, the fourteen rewrites)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

It adds its own visual device, used fifteen times: a **before / after** pair showing the same request written badly and written well, with a line explaining what changed.

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | The intern who just arrived (a prompt is a brief, not a search query) · The four ingredients: context, task, format, examples · **Magic formulas don't work** — the folklore cleared away early · The vocabulary in 6 words |
| **2 — Doing it well** | Give it the material: recall vs. transformation, applied to how you write · Show, don't describe: examples beat adjectives, and the edge-case example matters most · State the format (the highest effort-to-result ratio in the course) · Iterate — including the trick almost nobody uses: make it ask *you* questions first |
| **3 — In practice** | 8 everyday situations with the bad and good version of each · **When the prompt isn't the problem** — four situations where rewriting is pure waste, and a 30-second three-question test |
| **4 — Two stories** | Camille's job postings (a reusable template, built in five versions, with the two accidental discoveries that made it work) · Théo's report (14 rewrites, each more confident and no more true) |

---

## The spine of the course

**A prompt doesn't improve the model — it improves what the model has in front of it.** Lesson 3 uses that as the test for every piece of prompt advice in circulation: does it add information, or is it an incantation? Role-play, tips, threats and politeness fall on the wrong side; giving the document, giving examples, stating the format and letting it think fall on the right one.

**Rewriting only fixes wording problems.** Lesson 10 lists the four situations where no prompt helps — the information isn't there, the task needs real computation, you don't know what you want, or the judgment is yours — and gives a three-question test to tell them apart in thirty seconds.

Théo's story is built on one counterintuitive mechanism: asking for *more precision* from a model that lacks the information doesn't produce more truth, it produces **more detailed inventions, and therefore more credible ones**. Across 14 versions, prompt length, confidence and detail all rose; accuracy never moved. The working version took four minutes — all of it spent finding the PDF.

---

## Design

| | |
|---|---|
| Palette | Indigo `#242A63` · Apricot `#FF9F68` · Periwinkle `#8B7EF8` · Green `#2BB673` |
| Typography | Epilogue (headings) · DM Sans (body) |
| Signature | The paired "5-year-old / grown-up" cards, the before/after comparison blocks, and progress pips drawn as speech bubbles |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
