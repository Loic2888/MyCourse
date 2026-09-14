# >_ The Terminal & CLIs — Explained Simply

A short, standalone course on the command line, written for absolute beginners. The stated goal: after reading it, a five-year-old could explain what a terminal is.

Open [`index.html`](./index.html) in Chrome or Firefox — no server, no build, no dependencies.

> Course content is in **French**, like every course in this repository.

---

## What makes this one different

Fourth entry in the *Explained Simply* series, and the **bridge between the non-technical half and the technical half**. Courses 1–3 need no terminal; courses 5–9 assume one. This is the step in between.

It is not a generic "learn the shell" course. It is built around one claim, stated in Lesson 3 and carried through every other lesson:

> **An AI cannot click a button. But it can write a command — and that is exactly how it acts on the real world.**

A button only exists for eyes and a mouse. A command is text: a model can write it, a machine can run it, and the reply comes back as text the model can read. That is why an agent's tools are largely commands, why a local MCP server is launched by one, and why Claude Code is a CLI rather than a windowed app.

Every lesson follows the series' two-card pattern:

- `>_` **Version 5 ans** — the idea told as a story (the remote control vs. speaking, the room you're standing in, the black box)
- 🔧 **Version grande personne** — the same idea in real technical terms, right underneath

It adds its own visual device, used eight times: a **command decomposition** — the same line shown with each part coloured and labelled (program · action · arguments · options).

---

## Contents

| Module | Lessons |
|--------|---------|
| **1 — What is it?** | Speaking instead of clicking (terminal vs. shell vs. CLI) · The grammar every command shares, and `--help` · **Why AI uses it** — the pivot of the course, plus the realistic safety reflex · The vocabulary in 6 words |
| **2 — How it works** | Where you are: paths, and why an agent locates itself before acting · What the machine replies — and why error messages are what the agent reads to decide the next step · Chaining commands with pipes · What changes when it runs without you |
| **3 — In practice** | 8 commands that actually matter (four that only look, four that modify) and the three words to slow down for · When clicking is the better answer |
| **4 — Two stories** | Jade's photos (one command → a script → an agent that runs it, with French comments throughout) · Elias's black box (an automation that worked for eight months, broke over a renamed folder, and could not be repaired) |

---

## The spine of the course

**The CLI is the surface through which an AI acts.** Everything follows from that: a task that lives in clicks can only ever be done by you, by hand, one more time; the same task written as commands can be delegated, repeated a thousand times, and scheduled for 3 a.m. Lesson 10's closing quiz makes the point explicitly — you don't need to be able to *write* commands, you need to know that this door exists.

**The failure mode is not the destructive command.** That was a deliberate choice. Teaching a non-technical reader to audit shell commands is wishful thinking — they won't do it, and a course built on that premise would be dishonest. The realistic risk is quieter and far more common: *an automation built by an AI, that works, that nobody understands.* Elias loses eleven days and then six months not to a catastrophe but to an abandonment, over a renamed folder and a one-word fix he had no way to find.

What the course asks instead is achievable without reading a single command: ask the AI to write **French comments beside each line**, keep **the prompt you used to generate it**, and make sure **silence is visible** — a log and an alert. Jade does all three; Elias does none.

The safety advice is kept proportionate and honest: paste the command into *another* AI and ask what it does — while stating plainly that the second AI doesn't know your context either, so the real safeguards are a backup and suspicion of anything that deletes, moves or overwrites.

---

## Design

| | |
|---|---|
| Palette | Terminal `#12211C` · Prompt green `#3FCB8E` · Argument amber `#EFB93B` · Flag blue `#6FA8F0` |
| Typography | Archivo (headings) · Figtree (body) |
| Signature | The paired "5-year-old / grown-up" cards, the colour-coded command decomposition, and progress pips drawn as terminal cursors |

Progress is tracked in `localStorage`: lessons check themselves off as you scroll past them.
