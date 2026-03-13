# Awesome AI Orchestration [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, tools, protocols, and resources for orchestrating AI agents — from multi-agent coding to enterprise workflow automation.

The AI agent landscape has exploded in 2025-2026. The bottleneck has shifted from "how do I build an agent?" to **"how do I run multiple agents in parallel without chaos?"** This list covers everything you need.

---

## Contents

- [Protocols & Standards](#protocols--standards)
- [Multi-Agent Frameworks](#multi-agent-frameworks)
- [Autonomous Coding Agents](#autonomous-coding-agents)
- [Coding Agent Orchestrators](#coding-agent-orchestrators)
- [Chinese AI Orchestration (中国特色)](#chinese-ai-orchestration-中国特色)
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
| [CrewAI](https://github.com/crewAIInc/crewAI) | Python | Role-based crews | ![GitHub stars](https://img.shields.io/github/stars/crewAIInc/crewAI) | Think of agents as team members with roles. Fastest-growing multi-agent framework. 44K+ stars. |
| [AutoGen](https://github.com/microsoft/autogen) | Python / TS | Conversational agents | ![GitHub stars](https://img.shields.io/github/stars/microsoft/autogen) | Microsoft's v0.4 rewrite with distributed agents and Azure integration. Merging into Microsoft Agent Framework. |
| [AG2](https://github.com/ag2ai/ag2) | Python | Conversational agents | ![GitHub stars](https://img.shields.io/github/stars/ag2ai/ag2) | Community fork of AutoGen 0.2 by original creators. Keeps familiar API. |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Python | Lightweight multi-agent | ![GitHub stars](https://img.shields.io/github/stars/openai/openai-agents-python) | Lowest barrier to entry. Tracing, guardrails, 100+ LLM support. |
| [Claude Agent SDK](https://github.com/anthropics/claude-code-sdk-python) | Python / TS | Subagent orchestration | ![GitHub stars](https://img.shields.io/github/stars/anthropics/claude-code-sdk-python) | Programmatic access to Claude Code as an agent. |
| [Google ADK](https://github.com/google/adk-python) | Python | Agent Development Kit | ![GitHub stars](https://img.shields.io/github/stars/google/adk-python) | Native A2A + MCP support. Tight Gemini integration. |
| [Semantic Kernel](https://github.com/microsoft/semantic-kernel) | C# / Python / Java | Enterprise AI orchestration | ![GitHub stars](https://img.shields.io/github/stars/microsoft/semantic-kernel) | Microsoft's unified agent framework. Multi-language. |

### Emerging & Specialized

| Framework | Language | Focus | Stars |
|-----------|----------|-------|-------|
| [Mastra](https://github.com/mastra-ai/mastra) | TypeScript | TS-native agent framework (by Gatsby team) | ![GitHub stars](https://img.shields.io/github/stars/mastra-ai/mastra) |
| [PydanticAI](https://github.com/pydantic/pydantic-ai) | Python | Type-safe agents with structured I/O | ![GitHub stars](https://img.shields.io/github/stars/pydantic/pydantic-ai) |
| [PraisonAI](https://github.com/MervinPraison/PraisonAI) | Python | Low-code multi-agent with YAML config. Integrates CrewAI + AG2. | ![GitHub stars](https://img.shields.io/github/stars/MervinPraison/PraisonAI) |
| [Swarm](https://github.com/openai/swarm) | Python | Educational multi-agent patterns | ![GitHub stars](https://img.shields.io/github/stars/openai/swarm) |
| [MetaGPT](https://github.com/geekan/MetaGPT) | Python | Software company simulation (PM, Architect, Engineer roles) | ![GitHub stars](https://img.shields.io/github/stars/geekan/MetaGPT) |
| [LlamaIndex Workflows](https://github.com/run-llama/llama_index) | Python | Data-aware agent workflows | ![GitHub stars](https://img.shields.io/github/stars/run-llama/llama_index) |
| [Haystack](https://github.com/deepset-ai/haystack) | Python | Composable AI pipelines | ![GitHub stars](https://img.shields.io/github/stars/deepset-ai/haystack) |
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
Low-code YAML config?              → PraisonAI
Software team simulation?          → MetaGPT
```

---

## Autonomous Coding Agents

*Standalone AI agents that can autonomously write, debug, and ship code.*

| Agent | Type | Stars | Highlights |
|-------|------|-------|------------|
| [OpenHands](https://github.com/OpenHands/OpenHands) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/OpenHands/OpenHands) | Formerly OpenDevin. Autonomous AI software engineer. Model-agnostic, enterprise-ready. Scales to 1000s of agents. |
| [SWE-agent](https://github.com/SWE-agent/SWE-agent) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/SWE-agent/SWE-agent) | Princeton/Stanford. Takes GitHub issues, auto-fixes them. NeurIPS 2024. |
| [Aider](https://github.com/Aider-AI/aider) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/Aider-AI/aider) | Terminal-based AI pair programming. Git-native, 100+ languages. |
| [Roo Code](https://github.com/RooCodeInc/Roo-Code) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/RooCodeInc/Roo-Code) | VS Code extension. Multi-mode (Architect/Developer/Tester). Fork of Cline. 22K+ stars. |
| [Cline](https://github.com/cline/cline) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/cline/cline) | VS Code/JetBrains extension. 5M+ installs. MCP marketplace. Subagents v3.58. |
| [Open SWE](https://github.com/langchain-ai/open-swe) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/langchain-ai/open-swe) | LangChain's async coding agent. Built on LangGraph. |
| [Devin](https://devin.ai/) | Commercial | N/A | Cognition Labs. First "AI software engineer". $10.2B valuation. Cloud sandbox. |
| [OpenClaw](https://github.com/openclaw/openclaw) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/openclaw/openclaw) | Viral AI assistant (210K+ stars). Self-improving, writes own skills. Multi-platform. |
| [Mini SWE-agent](https://github.com/SWE-agent/mini-swe-agent) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/SWE-agent/mini-swe-agent) | 100-line agent scoring 65%+ on SWE-bench verified. |

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
| [CCB (Claude Code Bridge)](https://github.com/bfly123/claude_code_bridge) | Real-time multi-AI collaboration via split-pane terminal. 8 providers (Claude/Codex/Gemini/OpenCode/Droid/Copilot/CodeBuddy/Qwen). Only 50-200 tokens/call vs 5K-20K traditional. | ![GitHub stars](https://img.shields.io/github/stars/bfly123/claude_code_bridge) |
| [dmux](https://github.com/standardagents/dmux) | Parallel agents with tmux and worktrees | ![GitHub stars](https://img.shields.io/github/stars/standardagents/dmux) |
| [amux](https://github.com/andyrewlee/amux) | TUI for easily running parallel coding agents | ![GitHub stars](https://img.shields.io/github/stars/andyrewlee/amux) |
| [cmux](https://github.com/manaflow-ai/cmux) | Open-source platform for running multiple coding agents in parallel | ![GitHub stars](https://img.shields.io/github/stars/manaflow-ai/cmux) |
| [mux](https://github.com/coder/mux) | Desktop app for isolated, parallel agentic development | ![GitHub stars](https://img.shields.io/github/stars/coder/mux) |
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
| [ai-maestro](https://github.com/23blocks-OS/ai-maestro) | Orchestrate Claude, Aider, and Cursor agents across machines | ![GitHub stars](https://img.shields.io/github/stars/23blocks-OS/ai-maestro) |
| [humanlayer](https://github.com/humanlayer/humanlayer) | Get AI coding agents to solve hard problems with human-in-the-loop | ![GitHub stars](https://img.shields.io/github/stars/humanlayer/humanlayer) |
| [emdash](https://github.com/generalaction/emdash) | Run multiple coding agents in parallel | ![GitHub stars](https://img.shields.io/github/stars/generalaction/emdash) |
| [jean](https://github.com/coollabsio/jean) | Manage multiple projects, worktrees, and sessions with Claude CLI | ![GitHub stars](https://img.shields.io/github/stars/coollabsio/jean) |
| [t3code](https://github.com/pingdotgg/t3code) | Minimal web GUI for coding agents | ![GitHub stars](https://img.shields.io/github/stars/pingdotgg/t3code) |
| [vibe-tree](https://github.com/sahithvibudhi/vibe-tree) | Vibe code with Claude in parallel git worktrees | ![GitHub stars](https://img.shields.io/github/stars/sahithvibudhi/vibe-tree) |
| [openkanban](https://github.com/techdufus/openkanban) | TUI kanban board for orchestrating AI coding agents | ![GitHub stars](https://img.shields.io/github/stars/techdufus/openkanban) |
| [subtask](https://github.com/zippoxer/subtask) | Claude Skill for doing tasks with subagents in Git worktrees | ![GitHub stars](https://img.shields.io/github/stars/zippoxer/subtask) |
| [superset](https://github.com/superset-sh/superset) | A terminal built for coding agents | ![GitHub stars](https://img.shields.io/github/stars/superset-sh/superset) |
| [automaker](https://github.com/AutoMaker-Org/automaker) | Autonomous AI development studio | ![GitHub stars](https://img.shields.io/github/stars/AutoMaker-Org/automaker) |
| [ariana](https://github.com/ariana-dot-dev/ariana) | The IDE of the future | ![GitHub stars](https://img.shields.io/github/stars/ariana-dot-dev/ariana) |
| [jat](https://github.com/joewinke/jat) | The World's First Agentic IDE | ![GitHub stars](https://img.shields.io/github/stars/joewinke/jat) |

### IDE-Integrated Agent Platforms

| Platform | Multi-Agent? | Parallel? | Key Feature |
|----------|:-----:|:---------:|-------------|
| **Claude Code** (Agent Teams) | Yes | Yes | Subagent communication, shared task list, worktree isolation |
| **Cursor** (Background Agents) | Yes | 10-20 agents | Cloud VMs, auto-PR generation |
| **Codex CLI** (Agents SDK) | Yes | Yes | Long-running workflows, sandbox execution |
| **Windsurf** | Yes | 5 agents | Cascading agent flows |
| **Copilot** (Coding Agent) | Yes | Yes | GitHub-native, auto-assigns issues |
| **Grok Build** | Yes | 8 agents | xAI integration |

---

## Chinese AI Orchestration (中国特色)

*AI orchestration projects with Chinese cultural themes or from Chinese developers.*

### AI 朝廷 (AI Imperial Court)

| Tool | Description | Stars |
|------|-------------|-------|
| [Edict (三省六部制)](https://github.com/cft0808/edict) | 以唐朝三省六部制为蓝本的 OpenClaw 多 Agent 编排系统。12 个 Agent 角色（太子分拣→中书省规划→门下省审核→尚书省调度→六部执行→奏折回报），内置实时仪表盘、模型配置、审计追踪。30 秒完成从圣旨到执行的全流程。 | ![GitHub stars](https://img.shields.io/github/stars/cft0808/edict) |
| [AI 朝廷教程](https://github.com/wanikua/boluobobo-ai-court-tutorial) | AI 朝廷从零搭建完整教程，手把手教你部署一支 7x24 在线的 AI 朝廷。 | ![GitHub stars](https://img.shields.io/github/stars/wanikua/boluobobo-ai-court-tutorial) |

> **AI 朝廷 vs 传统框架对比:**
> - vs CrewAI: 多了门下省审核层（质量把关），每个 Agent 有明确的朝廷角色
> - vs AutoGen: 多了实时仪表盘（军事指挥中心），可视化全流程
> - vs LangGraph: 更高层抽象，用"圣旨→执行→奏折"替代图节点思维

### CCB (Claude Code Bridge)

| Tool | Description | Stars |
|------|-------------|-------|
| [CCB](https://github.com/bfly123/claude_code_bridge) | 实时多 AI 协作桥梁。支持 8 个 Provider（Claude/Codex/Gemini/OpenCode/Droid/Copilot/CodeBuddy/Qwen），tmux/WezTerm 分屏终端 WYSIWYG 可视化。每次调用仅 50-200 tokens（传统方式 5K-20K），支持持久会话、断点续传。 | ![GitHub stars](https://img.shields.io/github/stars/bfly123/claude_code_bridge) |

> **CCB 的独特之处:**
> - **WYSIWYG**: 不同于 API 调用，CCB 在终端分屏中直接展示每个 AI 的交互
> - **极低 Token 开销**: 50-200 tokens/call，是传统方案的 1/100
> - **8 Provider 统一**: 一套 CLI 统一管理 Claude、Codex、Gemini 等 8 个 AI
> - **协议标记**: CCB_REQ_ID/CCB_DONE 协议标记，daemon-per-provider 架构

### More Chinese-Origin Projects

| Tool | Description | Stars |
|------|-------------|-------|
| [Dify](https://github.com/langgenius/dify) | 国产开源 LLM 应用平台，可视化工作流 + RAG + Agent 编排。129K+ stars。 | ![GitHub stars](https://img.shields.io/github/stars/langgenius/dify) |
| [MetaGPT](https://github.com/geekan/MetaGPT) | 深圳 DeepWisdom 团队。模拟软件公司（产品经理→架构师→工程师），按 SOP 协同开发。 | ![GitHub stars](https://img.shields.io/github/stars/geekan/MetaGPT) |
| [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) | 阿里通义千问官方 Agent 框架，支持 Function Calling、Code Interpreter、RAG。 | ![GitHub stars](https://img.shields.io/github/stars/QwenLM/Qwen-Agent) |
| [Open WebUI](https://github.com/open-webui/open-webui) | 自托管 AI 平台，282M+ 下载，124K+ stars。支持离线运行、多模型管理。 | ![GitHub stars](https://img.shields.io/github/stars/open-webui/open-webui) |
| [RAGFlow](https://github.com/infiniflow/ragflow) | 深度文档理解的 RAG 引擎，支持 Agent 编排和知识库管理。 | ![GitHub stars](https://img.shields.io/github/stars/infiniflow/ragflow) |
| [Coze (扣子)](https://www.coze.com/) | 字节跳动 Agent 平台，丰富插件生态，可视化工作流编排。 | N/A |

---

## Low-Code / Visual Platforms

*Build agent workflows visually without deep coding.*

| Platform | Type | Stars | Highlights |
|----------|------|-------|------------|
| [Dify](https://github.com/langgenius/dify) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/langgenius/dify) | Visual workflow builder, RAG pipelines, BaaS + LLMOps. 129K+ stars. |
| [n8n](https://github.com/n8n-io/n8n) | Source Available | ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n) | 400+ integrations, workflow automation + AI agents |
| [Flowise](https://github.com/FlowiseAI/Flowise) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/FlowiseAI/Flowise) | Drag & drop multi-agent orchestration |
| [LangFlow](https://github.com/langflow-ai/langflow) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/langflow-ai/langflow) | Visual LangChain builder |
| [RAGFlow](https://github.com/infiniflow/ragflow) | Open Source | ![GitHub stars](https://img.shields.io/github/stars/infiniflow/ragflow) | Deep document understanding + agent orchestration |
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
| [OpenClaw](https://github.com/openclaw/openclaw) | Viral open-source AI assistant (210K+ stars). Self-improving, writes own skills. WhatsApp/Discord/Telegram/Slack/iMessage + 20 more platforms. | ![GitHub stars](https://img.shields.io/github/stars/openclaw/openclaw) |
| [Leon](https://github.com/leon-ai/leon) | Open-source personal assistant (voice + text) | ![GitHub stars](https://img.shields.io/github/stars/leon-ai/leon) |
| [BabyAGI](https://github.com/yoheinakajima/babyagi3) | Minimal AI agent — configure once, run via natural language | ![GitHub stars](https://img.shields.io/github/stars/yoheinakajima/babyagi3) |
| [Happy](https://github.com/slopus/happy) | Mobile/web client for Claude Code, Codex, Gemini CLI. E2E encrypted. | ![GitHub stars](https://img.shields.io/github/stars/slopus/happy) |
| [Letta](https://github.com/letta-ai/letta) | AI assistant framework with persistent memory | ![GitHub stars](https://img.shields.io/github/stars/letta-ai/letta) |
| [rho](https://github.com/mikeyobrien/rho) | Agent with persistent memory across sessions and autonomous updates | ![GitHub stars](https://img.shields.io/github/stars/mikeyobrien/rho) |

---

## Autonomous Loop Runners

*"Keep running until done" patterns for agent workflows.*

| Tool | Description | Stars |
|------|-------------|-------|
| [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) | Hat-based orchestration that keeps agents in a loop until done | ![GitHub stars](https://img.shields.io/github/stars/mikeyobrien/ralph-orchestrator) |
| [ralph-tui](https://github.com/subsy/ralph-tui) | Orchestrate AI coding agents through task lists autonomously | ![GitHub stars](https://img.shields.io/github/stars/subsy/ralph-tui) |
| [ralph-claude-code](https://github.com/frankbria/ralph-claude-code) | Autonomous AI development loop for Claude Code with intelligent exit detection | ![GitHub stars](https://img.shields.io/github/stars/frankbria/ralph-claude-code) |
| [ralphy](https://github.com/michaelshimeles/ralphy) | Runs AI agents on tasks until done | ![GitHub stars](https://img.shields.io/github/stars/michaelshimeles/ralphy) |
| [wreckit](https://github.com/mikehostetler/wreckit) | Run Ralph Wiggum Loop over your roadmap | ![GitHub stars](https://img.shields.io/github/stars/mikehostetler/wreckit) |
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
| [antfarm](https://github.com/snarktank/antfarm) | Build your agent team in OpenClaw with one command | ![GitHub stars](https://img.shields.io/github/stars/snarktank/antfarm) |
| [clawe](https://github.com/getclawe/clawe) | Multi-agent coordination — Trello for OpenClaw agents | ![GitHub stars](https://img.shields.io/github/stars/getclawe/clawe) |
| [opengoat](https://github.com/marian2js/opengoat) | Build AI autonomous organizations of OpenClaw agents | ![GitHub stars](https://img.shields.io/github/stars/marian2js/opengoat) |
| [openfang](https://github.com/RightNow-AI/openfang) | Open-source Agent Operating System | ![GitHub stars](https://img.shields.io/github/stars/RightNow-AI/openfang) |

---

## Learning Resources

### Articles & Guides

- [Conductors to Orchestrators: The Future of Agentic Coding](https://www.oreilly.com/radar/conductors-to-orchestrators-the-future-of-agentic-coding/) — O'Reilly
- [A Developer's Guide to Agentic Frameworks in 2026](https://pub.towardsai.net/a-developers-guide-to-agentic-frameworks-in-2026-3f22a492dc3d) — Towards AI
- [LangGraph vs CrewAI vs AutoGen: Complete Guide](https://dev.to/pockit_tools/langgraph-vs-crewai-vs-autogen-the-complete-multi-agent-ai-orchestration-guide-for-2026-2d63) — DEV Community
- [The State of AI Coding Agents (2026)](https://medium.com/@dave-patten/the-state-of-ai-coding-agents-2026-from-pair-programming-to-autonomous-ai-teams-b11f2b39232a) — Medium
- [MCP & Multi-Agent AI: Building Collaborative Intelligence](https://onereach.ai/blog/mcp-multi-agent-ai-collaborative-intelligence/) — OneReach
- [The 2026 MCP Roadmap](https://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/) — MCP Blog
- [Agentic Coding 2026: AI Agent Teams Guide](https://halallens.no/en/blog/agentic-coding-in-2026-the-complete-guide-to-plugins-multi-model-orchestration-and-ai-agent-teams) — Complete guide to multi-model orchestration
- [Open Source AI Agent Comparison](https://www.ilsilfverskiold.com/articles/agentic-aI-comparing-new-open-source-frameworks) — AG2, PydanticAI, BeeAI, Mastra compared

### Comparison & Benchmarks

- [AI Agent Frameworks Compared](https://langfuse.com/blog/2025-03-19-ai-agent-comparison) — Langfuse
- [AI Coding Agents Comparison 2026](https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/) — Lushbinary
- [The AI Agent Tools Landscape: 120+ Tools Mapped](https://www.stackone.com/blog/ai-agent-tools-landscape-2026/) — StackOne
- [Top 18 Open Source AI Agent Projects by Stars](https://www.nocobase.com/en/blog/github-open-source-ai-agent-projects) — NocoBase
- [Best Open Source AI Coding Agents 2026](https://cssauthor.com/best-open-source-ai-coding-agents/) — CSS Author

### Existing Awesome Lists

- [awesome-agents](https://github.com/kyrolabs/awesome-agents) — Comprehensive list of AI agents
- [awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) — List of autonomous AI agents
- [awesome-agent-orchestrators](https://github.com/andyrewlee/awesome-agent-orchestrators) — Coding agent orchestrators
- [awesome-llm-agents](https://github.com/kaushikb11/awesome-llm-agents) — LLM agent frameworks
- [awesome-devins](https://github.com/e2b-dev/awesome-devins) — Devin-inspired AI agents
- [awesome-ai-tools](https://github.com/mahseema/awesome-ai-tools) — General AI tools collection
- [500-AI-Agents-Projects](https://github.com/ashishpatel26/500-AI-Agents-Projects) — 500 AI agent use cases across industries
- [awesome-AI-driven-development](https://github.com/eltociear/awesome-AI-driven-development) — AI-driven development tools

---

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
