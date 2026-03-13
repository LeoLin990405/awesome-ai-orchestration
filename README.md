# Awesome AI Orchestration [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, tools, protocols, and resources for orchestrating AI agents — from multi-agent coding to enterprise workflow automation.

The AI agent landscape has exploded in 2025-2026. The bottleneck has shifted from "how do I build an agent?" to **"how do I run multiple agents in parallel without chaos?"** This list covers everything you need.

---

## Contents

- [Protocols & Standards](#protocols--standards)
- [Multi-Agent Frameworks](#multi-agent-frameworks)
- [Coding Agent Orchestrators](#coding-agent-orchestrators)
- [Low-Code / Visual Platforms](#low-code--visual-platforms)
- [Observability & Evaluation](#observability--evaluation)
- [Agent Infrastructure](#agent-infrastructure)
- [Personal AI Assistants](#personal-ai-assistants)
- [Autonomous Loop Runners](#autonomous-loop-runners)
- [Multi-Agent Swarms](#multi-agent-swarms)
- [Learning Resources](#learning-resources)

---

## Protocols & Standards

*Open protocols that enable agent interoperability.*

| Protocol | By | Purpose | Stars |
|----------|-----|---------|-------|
| [MCP (Model Context Protocol)](https://github.com/modelcontextprotocol/specification) | Anthropic → Linux Foundation | Agent-to-tool communication standard. 97M+ monthly SDK downloads, 10K+ servers. | ![GitHub stars](https://img.shields.io/github/stars/modelcontextprotocol/specification) |
| [A2A (Agent2Agent)](https://github.com/a2aproject/A2A) | Google → Linux Foundation | Agent-to-agent interoperability via JSON-RPC & SSE. 100+ partner companies. | ![GitHub stars](https://img.shields.io/github/stars/a2aproject/A2A) |
| [ACP (Agent Communication Protocol)](https://github.com/i-am-bee/beeai-platform) | IBM / BeeAI → Linux Foundation | Standardized agent messaging and discovery. | ![GitHub stars](https://img.shields.io/github/stars/i-am-bee/beeai-platform) |

### MCP vs A2A vs ACP

- **MCP** — How agents talk to **tools** (databases, APIs, file systems)
- **A2A** — How agents talk to **other agents** (cross-vendor interop)
- **ACP** — How agents **discover and communicate** in enterprise environments

They are complementary, not competing.

---

## Multi-Agent Frameworks

*Frameworks for building and orchestrating multi-agent systems.*

### Production-Grade

| Framework | Language | Approach | Stars | Highlights |
|-----------|----------|----------|-------|------------|
| [LangGraph](https://github.com/langchain-ai/langgraph) | Python / JS | Graph-based workflows | ![GitHub stars](https://img.shields.io/github/stars/langchain-ai/langgraph) | Stateful, cyclic graphs. Most popular by downloads (47M+ PyPI). Best for complex enterprise workflows. |
| [CrewAI](https://github.com/crewAIInc/crewAI) | Python | Role-based crews | ![GitHub stars](https://img.shields.io/github/stars/crewAIInc/crewAI) | Think of agents as team members with roles. Fastest-growing multi-agent framework. |
| [AutoGen](https://github.com/microsoft/autogen) | Python / TS | Conversational agents | ![GitHub stars](https://img.shields.io/github/stars/microsoft/autogen) | Microsoft's v0.4 rewrite with distributed agents and Azure integration. |
| [AG2](https://github.com/ag2ai/ag2) | Python | Conversational agents | ![GitHub stars](https://img.shields.io/github/stars/ag2ai/ag2) | Community fork of AutoGen 0.2 by original creators. Keeps familiar API. |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Python | Lightweight multi-agent | ![GitHub stars](https://img.shields.io/github/stars/openai/openai-agents-python) | Lowest barrier to entry. Tracing, guardrails, 100+ LLM support. |
| [Claude Agent SDK](https://github.com/anthropics/claude-code-sdk-python) | Python / TS | Subagent orchestration | ![GitHub stars](https://img.shields.io/github/stars/anthropics/claude-code-sdk-python) | Programmatic access to Claude Code as an agent. |
| [Google ADK](https://github.com/google/adk-python) | Python | Agent Development Kit | ![GitHub stars](https://img.shields.io/github/stars/google/adk-python) | Native A2A + MCP support. Tight Gemini integration. |

### Emerging & Specialized

| Framework | Language | Focus | Stars |
|-----------|----------|-------|-------|
| [Mastra](https://github.com/mastra-ai/mastra) | TypeScript | TS-native agent framework (by Gatsby team) | ![GitHub stars](https://img.shields.io/github/stars/mastra-ai/mastra) |
| [PydanticAI](https://github.com/pydantic/pydantic-ai) | Python | Type-safe agents with structured I/O | ![GitHub stars](https://img.shields.io/github/stars/pydantic/pydantic-ai) |
| [Swarm](https://github.com/openai/swarm) | Python | Educational multi-agent patterns | ![GitHub stars](https://img.shields.io/github/stars/openai/swarm) |
| [MetaGPT](https://github.com/geekan/MetaGPT) | Python | Software company simulation | ![GitHub stars](https://img.shields.io/github/stars/geekan/MetaGPT) |
| [LlamaIndex Workflows](https://github.com/run-llama/llama_index) | Python | Data-aware agent workflows | ![GitHub stars](https://img.shields.io/github/stars/run-llama/llama_index) |
| [Haystack](https://github.com/deepset-ai/haystack) | Python | Composable AI pipelines | ![GitHub stars](https://img.shields.io/github/stars/deepset-ai/haystack) |
| [Semantic Kernel](https://github.com/microsoft/semantic-kernel) | C# / Python / Java | Enterprise AI orchestration | ![GitHub stars](https://img.shields.io/github/stars/microsoft/semantic-kernel) |
| [Smolagents](https://github.com/huggingface/smolagents) | Python | Lightweight HuggingFace agents | ![GitHub stars](https://img.shields.io/github/stars/huggingface/smolagents) |
| [FastAgency](https://github.com/agentuniverse-ai/fastagency) | Python | Notebook → production pipeline | ![GitHub stars](https://img.shields.io/github/stars/agentuniverse-ai/fastagency) |
| [Agno](https://github.com/agno-agi/agno) | Python | Lightweight multi-modal agents | ![GitHub stars](https://img.shields.io/github/stars/agno-agi/agno) |
| [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) | Python | Modular agent building blocks | ![GitHub stars](https://img.shields.io/github/stars/BrainBlend-AI/atomic-agents) |

### Choosing a Framework

```
Need max control + enterprise?     → LangGraph
Want fast role-based prototyping?  → CrewAI
TypeScript team?                   → Mastra
OpenAI ecosystem?                  → OpenAI Agents SDK
Type-safe structured output?       → PydanticAI
Google/Gemini ecosystem?           → Google ADK
Microsoft/.NET ecosystem?          → Semantic Kernel / AutoGen
```

---

## Coding Agent Orchestrators

*Tools for running multiple AI coding agents in parallel.*

### Parallel Agent Runners

| Tool | Description | Stars |
|------|-------------|-------|
| [claude-squad](https://github.com/smtg-ai/claude-squad) | Manage multiple AI terminal agents in background with tmux | ![GitHub stars](https://img.shields.io/github/stars/smtg-ai/claude-squad) |
| [MCO](https://github.com/mco-org/mco) | Neutral orchestration layer for Claude Code, Codex CLI, Gemini CLI, OpenCode, Qwen Code | ![GitHub stars](https://img.shields.io/github/stars/mco-org/mco) |
| [agent-orchestrator](https://github.com/ComposioHQ/agent-orchestrator) | Plan tasks, spawn agents, handle CI fixes and merge conflicts | ![GitHub stars](https://img.shields.io/github/stars/ComposioHQ/agent-orchestrator) |
| [crystal](https://github.com/stravu/crystal) | Run multiple Codex and Claude Code sessions in parallel git worktrees | ![GitHub stars](https://img.shields.io/github/stars/stravu/crystal) |
| [dmux](https://github.com/standardagents/dmux) | Parallel agents with tmux and worktrees | ![GitHub stars](https://img.shields.io/github/stars/standardagents/dmux) |
| [amux](https://github.com/andyrewlee/amux) | TUI for easily running parallel coding agents | ![GitHub stars](https://img.shields.io/github/stars/andyrewlee/amux) |
| [cmux](https://github.com/manaflow-ai/cmux) | Open-source platform for running multiple coding agents in parallel | ![GitHub stars](https://img.shields.io/github/stars/manaflow-ai/cmux) |
| [mux](https://github.com/coder/mux) | Desktop app for isolated, parallel agentic development | ![GitHub stars](https://img.shields.io/github/stars/coder/mux) |
| [claude_code_bridge](https://github.com/bfly123/claude_code_bridge) | Real-time multi-AI collaboration (tmux/WezTerm split-pane) | ![GitHub stars](https://img.shields.io/github/stars/bfly123/claude_code_bridge) |
| [dorothy](https://github.com/Charlie85270/Dorothy) | Desktop app with automations, Kanban, and MCP servers | ![GitHub stars](https://img.shields.io/github/stars/Charlie85270/Dorothy) |
| [1code](https://github.com/21st-dev/1code) | UI for Claude Code with local and remote agent execution | ![GitHub stars](https://img.shields.io/github/stars/21st-dev/1code) |
| [agent-deck](https://github.com/asheshgoplani/agent-deck) | Terminal session manager for AI coding agents | ![GitHub stars](https://img.shields.io/github/stars/asheshgoplani/agent-deck) |
| [symphony](https://github.com/openai/symphony) | Turns project work into isolated, autonomous implementation runs | ![GitHub stars](https://img.shields.io/github/stars/openai/symphony) |
| [CodexMonitor](https://github.com/Dimillian/CodexMonitor) | Orchestrate multiple Codex agents across local workspaces | ![GitHub stars](https://img.shields.io/github/stars/Dimillian/CodexMonitor) |
| [vibe-kanban](https://github.com/BloopAI/vibe-kanban) | Kanban board for managing AI coding agents | ![GitHub stars](https://img.shields.io/github/stars/BloopAI/vibe-kanban) |
| [vibecraft](https://github.com/rayzhudev/vibecraft) | RTS-style workspace for managing AI coding agents | ![GitHub stars](https://img.shields.io/github/stars/rayzhudev/vibecraft) |
| [constellagent](https://github.com/owengretzinger/constellagent) | macOS app with terminal, editor, and git worktree per agent | ![GitHub stars](https://img.shields.io/github/stars/owengretzinger/constellagent) |
| [aizen](https://github.com/vivy-company/aizen) | macOS workspace for managing git worktrees with integrated agent sessions | ![GitHub stars](https://img.shields.io/github/stars/vivy-company/aizen) |
| [supacode](https://github.com/supabitapp/supacode) | Native macOS coding agent orchestrator | ![GitHub stars](https://img.shields.io/github/stars/supabitapp/supacode) |

### IDE-Integrated Agent Platforms

| Platform | Multi-Agent? | Parallel? | Key Feature |
|----------|:-----:|:---------:|-------------|
| **Claude Code** (Agent Teams) | Yes | Yes | Subagent communication, shared task list, worktree isolation |
| **Cursor** (Background Agents) | Yes | 10-20 agents | Cloud VMs, auto-PR generation |
| **Codex CLI** (Agents SDK) | Yes | Yes | Long-running workflows, sandbox execution |
| **Windsurf** | Yes | 5 agents | Cascading agent flows |
| **Copilot** (Coding Agent) | Yes | Yes | GitHub-native, auto-assigns issues |

---

## Low-Code / Visual Platforms

*Build agent workflows visually without deep coding.*

| Platform | Type | Stars | Highlights |
|----------|------|-------|------------|
| [Dify](https://github.com/langgenius/dify) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/langgenius/dify) | Visual workflow builder, RAG pipelines, BaaS + LLMOps |
| [n8n](https://github.com/n8n-io/n8n) | Source Available | ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n) | 400+ integrations, workflow automation + AI agents |
| [Flowise](https://github.com/FlowiseAI/Flowise) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/FlowiseAI/Flowise) | Drag & drop multi-agent orchestration |
| [LangFlow](https://github.com/langflow-ai/langflow) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/langflow-ai/langflow) | Visual LangChain builder |
| [Coze](https://www.coze.com/) | Commercial | N/A | ByteDance's agent platform with rich plugin ecosystem |
| [Wordware](https://github.com/wordware-ai/twitter) | Commercial | N/A | Natural language programming for AI agents |

---

## Observability & Evaluation

*Monitor, debug, and evaluate agent performance in production.*

| Tool | Type | Stars | Focus |
|------|------|-------|-------|
| [Langfuse](https://github.com/langfuse/langfuse) | Open Source (MIT) | ![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse) | Tracing, prompt management, evaluation. 6M+ SDK installs/month. |
| [Arize Phoenix](https://github.com/Arize-ai/phoenix) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/Arize-ai/phoenix) | Self-hosted observability. Strong eval + tracing. |
| [LangSmith](https://smith.langchain.com/) | Commercial | N/A | Deep LangChain integration. Near-zero overhead. |
| [AgentOps](https://github.com/AgentOps-AI/agentops) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/AgentOps-AI/agentops) | Agent-specific observability with session replay. |
| [Laminar](https://github.com/lmnr-ai/lmnr) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/lmnr-ai/lmnr) | Minimal overhead (5%). Rust-powered. |
| [Helicone](https://github.com/Helicone/helicone) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/Helicone/helicone) | Gateway-based observability. Easy integration. |
| [Braintrust](https://www.braintrust.dev/) | Commercial | N/A | Eval, logging, and prompt playground. |

---

## Agent Infrastructure

*Execution environments, sandboxes, and deployment tools.*

| Tool | Purpose | Stars |
|------|---------|-------|
| [E2B](https://github.com/e2b-dev/e2b) | Cloud sandboxes for AI agents (code execution) | ![GitHub stars](https://img.shields.io/github/stars/e2b-dev/e2b) |
| [Modal](https://modal.com/) | Serverless compute for agent workloads | N/A |
| [Daytona](https://github.com/daytonaio/daytona) | Dev environments for AI agents | ![GitHub stars](https://img.shields.io/github/stars/daytonaio/daytona) |
| [Composio](https://github.com/ComposioHQ/composio) | 250+ tool integrations for AI agents | ![GitHub stars](https://img.shields.io/github/stars/ComposioHQ/composio) |
| [ToolHouse](https://github.com/toolhouseai/toolhouse) | Tool execution infrastructure | ![GitHub stars](https://img.shields.io/github/stars/toolhouseai/toolhouse) |
| [Browserbase](https://github.com/browserbase/stagehand) | Browser automation for agents (Stagehand) | ![GitHub stars](https://img.shields.io/github/stars/browserbase/stagehand) |
| [Firecrawl](https://github.com/mendableai/firecrawl) | Web scraping API optimized for LLMs | ![GitHub stars](https://img.shields.io/github/stars/mendableai/firecrawl) |
| [Crawl4AI](https://github.com/unclecode/crawl4ai) | Open-source LLM-friendly web crawling | ![GitHub stars](https://img.shields.io/github/stars/unclecode/crawl4ai) |

---

## Personal AI Assistants

*Always-on AI assistants with memory and multi-platform presence.*

| Tool | Description | Stars |
|------|-------------|-------|
| [OpenClaw](https://github.com/openclaw/openclaw) | Open-source personal AI assistant | ![GitHub stars](https://img.shields.io/github/stars/openclaw/openclaw) |
| [Leon](https://github.com/leon-ai/leon) | Open-source personal assistant (voice + text) | ![GitHub stars](https://img.shields.io/github/stars/leon-ai/leon) |
| [BabyAGI](https://github.com/yoheinakajima/babyagi3) | Minimal AI agent — configure once, run via natural language | ![GitHub stars](https://img.shields.io/github/stars/yoheinakajima/babyagi3) |
| [Happy](https://github.com/slopus/happy) | Mobile/web client for Claude Code, Codex, Gemini CLI | ![GitHub stars](https://img.shields.io/github/stars/slopus/happy) |

---

## Autonomous Loop Runners

*"Keep running until done" patterns for agent workflows.*

| Tool | Description | Stars |
|------|-------------|-------|
| [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) | Hat-based orchestration that keeps agents in a loop until done | ![GitHub stars](https://img.shields.io/github/stars/mikeyobrien/ralph-orchestrator) |
| [ralph-tui](https://github.com/subsy/ralph-tui) | Orchestrate AI coding agents through task lists autonomously | ![GitHub stars](https://img.shields.io/github/stars/subsy/ralph-tui) |
| [loom](https://github.com/ghuntley/loom) | Infrastructure for evolutionary software where autonomous loops evolve products | ![GitHub stars](https://img.shields.io/github/stars/ghuntley/loom) |
| [lalph](https://github.com/tim-smart/lalph) | LLM agent orchestrator driven by your chosen source of issues | ![GitHub stars](https://img.shields.io/github/stars/tim-smart/lalph) |

---

## Multi-Agent Swarms

*Coordinated swarms of specialized agents.*

| Tool | Description | Stars |
|------|-------------|-------|
| [claude-flow](https://github.com/ruvnet/claude-flow) | Deploy multi-agent swarms with coordinated workflows | ![GitHub stars](https://img.shields.io/github/stars/ruvnet/claude-flow) |
| [ruflo](https://github.com/ruvnet/ruflo) | Enterprise-grade swarm intelligence with RAG integration | ![GitHub stars](https://img.shields.io/github/stars/ruvnet/ruflo) |
| [gastown](https://github.com/steveyegge/gastown) | Multi-agent orchestration with persistent work tracking | ![GitHub stars](https://img.shields.io/github/stars/steveyegge/gastown) |
| [paperclip](https://github.com/paperclipai/paperclip) | Orchestration for fully autonomous agent organizations | ![GitHub stars](https://img.shields.io/github/stars/paperclipai/paperclip) |
| [overstory](https://github.com/jayminwest/overstory) | Pluggable runtime adapters for Claude Code, Pi, and more | ![GitHub stars](https://img.shields.io/github/stars/jayminwest/overstory) |

---

## Learning Resources

### Articles & Guides

- [Conductors to Orchestrators: The Future of Agentic Coding](https://www.oreilly.com/radar/conductors-to-orchestrators-the-future-of-agentic-coding/) — O'Reilly
- [A Developer's Guide to Agentic Frameworks in 2026](https://pub.towardsai.net/a-developers-guide-to-agentic-frameworks-in-2026-3f22a492dc3d) — Towards AI
- [LangGraph vs CrewAI vs AutoGen: Complete Guide](https://dev.to/pockit_tools/langgraph-vs-crewai-vs-autogen-the-complete-multi-agent-ai-orchestration-guide-for-2026-2d63) — DEV Community
- [The State of AI Coding Agents (2026)](https://medium.com/@dave-patten/the-state-of-ai-coding-agents-2026-from-pair-programming-to-autonomous-ai-teams-b11f2b39232a) — Medium
- [MCP & Multi-Agent AI: Building Collaborative Intelligence](https://onereach.ai/blog/mcp-multi-agent-ai-collaborative-intelligence/) — OneReach
- [The 2026 MCP Roadmap](https://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/) — MCP Blog

### Comparison & Benchmarks

- [AI Agent Frameworks Compared](https://langfuse.com/blog/2025-03-19-ai-agent-comparison) — Langfuse
- [AI Coding Agents Comparison 2026](https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/) — Lushbinary
- [The AI Agent Tools Landscape: 120+ Tools Mapped](https://www.stackone.com/blog/ai-agent-tools-landscape-2026/) — StackOne

### Existing Awesome Lists

- [awesome-agents](https://github.com/kyrolabs/awesome-agents) — Comprehensive list of AI agents
- [awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) — List of autonomous AI agents
- [awesome-agent-orchestrators](https://github.com/andyrewlee/awesome-agent-orchestrators) — Coding agent orchestrators
- [awesome-llm-agents](https://github.com/kaushikb11/awesome-llm-agents) — LLM agent frameworks

---

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
