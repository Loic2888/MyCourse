# MyCourse

A personal collection of self-learning courses on topics I find interesting — AI, agentic systems, programming, and more.

## How it works

Each course is a **standalone HTML file** generated with a custom Claude Code skill I built myself. No server, no dependencies, no setup required.

To follow a course:
1. Navigate into any course folder
2. Copy or open the `index.html` file directly in **Chrome**
3. That's it — the course runs entirely in your browser

Features included in every course:
- Sidebar navigation with modules and lessons
- Progress tracking saved in your browser (`localStorage`)
- Syntax-highlighted code examples
- Exercises and pitfalls callouts
- Mobile-friendly layout

## How courses are generated

I use a custom skill developed in Claude Code that:
1. Maps the subject into modules and lessons (fundamentals → advanced)
2. Chooses a visual identity tailored to the topic
3. Writes each lesson in depth (concepts, examples, pitfalls, exercises)
4. Assembles everything into a single self-contained HTML file

## Course catalog

| Folder | Topic | Language |
|--------|-------|----------|
| [dev-agentique/frameworks-orchestration-agents/](dev-agentique/frameworks-orchestration-agents/) | Agent Orchestration Frameworks — LangGraph, LangChain, AutoGen | 🇫🇷 French |
| [dev-agentique/rag-memoire-agents/](dev-agentique/rag-memoire-agents/) | RAG and Agent Memory — Vector Stores, ChromaDB | 🇫🇷 French |

## Adding a new course

Run the `create-course` skill in Claude Code and specify the target folder. The generated HTML file can be dropped anywhere and opened directly in Chrome.
