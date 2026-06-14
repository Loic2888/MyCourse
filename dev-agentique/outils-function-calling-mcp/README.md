# Tools, Function Calling & MCP

> **Note:** This course is written in French.

A complete course on LLM tools, function calling, and the Model Context Protocol (MCP).

## Content

| Module | Topic | Lessons |
|--------|-------|---------|
| M1 | Function Calling Fundamentals | Core concept, request/response cycle, JSON Schema |
| M2 | Claude Tool Use API | Basic syntax, parallel tool use, tool_choice, streaming |
| M3 | Designing Effective Tools | Design principles, validation & security, error handling |
| M4 | Agents & Orchestration | Agentic loop, tool chaining, ReAct / plan-execute |
| M5 | Introduction to MCP | The M×N problem, client/server architecture, JSON-RPC & transports |
| M6 | Building an MCP Server | Python SDK, TypeScript SDK, full Tools implementation, stdio vs HTTP |
| M7 | Advanced MCP Primitives | Resources & Templates, Prompts, LLM Sampling |
| M8 | Production & Security | OAuth 2.1, debugging, Docker + observability |

**26 lessons · 26 hands-on exercises · 54+ code examples**

## Getting Started

Open `index.html` directly in a browser — no local dependencies, fully self-contained.

```bash
# With Live Server (VS Code)
# Right-click index.html → Open with Live Server

# Or directly
xdg-open index.html   # Linux
open index.html        # macOS
```

## Prerequisites

- Python 3.11+ with `pip install anthropic mcp pydantic`
- Node.js 18+ for TypeScript examples and the MCP Inspector
- An Anthropic API key (`ANTHROPIC_API_KEY`)

## Reference

- MCP spec: `2025-11-25` — [modelcontextprotocol.io](https://modelcontextprotocol.io)
- Recommended transport: Streamable HTTP (remote) / stdio (local)
- Python SDK: `mcp` · TypeScript SDK: `@modelcontextprotocol/sdk`
