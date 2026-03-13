# Awesome AI Orchestration [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, tools, protocols, and resources for orchestrating AI agents — from multi-agent coding to enterprise workflow automation.
>
> 精选的 AI Agent 编排框架、工具、协议和资源列表 — 涵盖多 Agent 编程到企业工作流自动化。

[English](#contents) | [中文](#目录)

The AI agent landscape has exploded in 2025-2026. The bottleneck has shifted from "how do I build an agent?" to **"how do I run multiple agents in parallel without chaos?"** This list covers everything you need.

AI Agent 领域在 2025-2026 年迎来爆发式增长。瓶颈已从"如何构建一个 Agent"转变为**"如何在不混乱的情况下并行运行多个 Agent"**。本列表涵盖你需要的一切。

---

## Contents / 目录

- [Protocols & Standards / 协议与标准](#protocols--standards--协议与标准)
- [Multi-Agent Frameworks / 多 Agent 框架](#multi-agent-frameworks--多-agent-框架)
- [Autonomous Coding Agents / 自主编码 Agent](#autonomous-coding-agents--自主编码-agent)
- [Coding Agent Orchestrators / 编码 Agent 编排器](#coding-agent-orchestrators--编码-agent-编排器)
- [Chinese AI Orchestration / 中国特色 AI 编排](#chinese-ai-orchestration--中国特色-ai-编排)
- [Low-Code / Visual Platforms / 低代码可视化平台](#low-code--visual-platforms--低代码可视化平台)
- [Observability & Evaluation / 可观测性与评估](#observability--evaluation--可观测性与评估)
- [Agent Infrastructure / Agent 基础设施](#agent-infrastructure--agent-基础设施)
- [Personal AI Assistants / 个人 AI 助手](#personal-ai-assistants--个人-ai-助手)
- [Autonomous Loop Runners / 自主循环执行器](#autonomous-loop-runners--自主循环执行器)
- [Multi-Agent Swarms / 多 Agent 蜂群](#multi-agent-swarms--多-agent-蜂群)
- [Benchmarks & Evaluation / 基准测试与评估](#benchmarks--evaluation--基准测试与评估)
- [Academic Papers / 学术论文](#academic-papers--学术论文)
- [Courses & Tutorials / 课程与教程](#courses--tutorials--课程与教程)
- [Learning Resources / 学习资源](#learning-resources--学习资源)

---

## Protocols & Standards / 协议与标准

*Open protocols that enable agent interoperability. / 实现 Agent 互操作性的开放协议。*

| Protocol / 协议 | By / 发起方 | Purpose / 用途 | Stars |
|----------|-----|---------|-------|
| [MCP (Model Context Protocol)](https://github.com/modelcontextprotocol/specification) | Anthropic → Linux Foundation | Agent-to-tool communication standard. 97M+ monthly SDK downloads, 10K+ servers. / Agent 与工具的通信标准。月 SDK 下载 9700 万+，1 万+ 服务器。 | ![GitHub stars](https://img.shields.io/github/stars/modelcontextprotocol/specification) |
| [A2A (Agent2Agent)](https://github.com/a2aproject/A2A) | Google → Linux Foundation | Agent-to-agent interoperability via JSON-RPC & SSE. 100+ partner companies. / 基于 JSON-RPC 和 SSE 的 Agent 间互操作。100+ 合作企业。 | ![GitHub stars](https://img.shields.io/github/stars/a2aproject/A2A) |
| [ACP (Agent Communication Protocol)](https://github.com/i-am-bee/beeai-platform) | IBM / BeeAI → Linux Foundation | Standardized agent messaging and discovery. / 标准化的 Agent 消息传递和发现机制。 | ![GitHub stars](https://img.shields.io/github/stars/i-am-bee/beeai-platform) |
| [ANP (Agent Network Protocol)](https://github.com/agent-network-protocol/anp-spec) | Community / 社区 | Peer discovery and networking for agents. / Agent 的对等发现和网络协议。 | ![GitHub stars](https://img.shields.io/github/stars/agent-network-protocol/anp-spec) |

### MCP vs A2A vs ACP vs ANP / 协议对比

| Protocol / 协议 | EN | 中文 |
|----------|-----|------|
| **MCP** | How agents talk to **tools** (databases, APIs, file systems) | Agent 如何与**工具**通信（数据库、API、文件系统） |
| **A2A** | How agents talk to **other agents** (cross-vendor interop) | Agent 如何与**其他 Agent** 通信（跨厂商互操作） |
| **ACP** | How agents **discover and communicate** in enterprise environments | Agent 如何在企业环境中**发现和通信** |
| **ANP** | How agents **find each other** in decentralized networks | Agent 如何在去中心化网络中**相互发现** |

They are complementary, not competing. See [Survey of Agent Interoperability Protocols](https://arxiv.org/abs/2505.02279) for details.

它们是互补的，而非竞争关系。详见 [Agent 互操作协议综述](https://arxiv.org/abs/2505.02279)。

---

## Multi-Agent Frameworks / 多 Agent 框架

*Frameworks for building and orchestrating multi-agent systems. / 构建和编排多 Agent 系统的框架。*

### Production-Grade / 生产级

| Framework / 框架 | Language / 语言 | Approach / 方法 | Stars | Highlights / 亮点 |
|-----------|----------|----------|-------|------------|
| [LangGraph](https://github.com/langchain-ai/langgraph) | Python / JS | Graph-based workflows / 基于图的工作流 | ![GitHub stars](https://img.shields.io/github/stars/langchain-ai/langgraph) | Stateful, cyclic graphs. Most popular by downloads (47M+ PyPI). v1.0 GA in 2026. / 有状态循环图。下载量最高（PyPI 4700万+）。2026 年 v1.0 正式版。 |
| [CrewAI](https://github.com/crewAIInc/crewAI) | Python | Role-based crews / 基于角色的团队 | ![GitHub stars](https://img.shields.io/github/stars/crewAIInc/crewAI) | Think of agents as team members with roles. 44K+ stars, 5.2M monthly downloads. / 将 Agent 视为有角色的团队成员。44K+ stars，月下载 520 万。 |
| [AutoGen](https://github.com/microsoft/autogen) | Python / TS | Conversational agents / 对话式 Agent | ![GitHub stars](https://img.shields.io/github/stars/microsoft/autogen) | Microsoft's v0.4 rewrite. Merging into Microsoft Agent Framework Q1 2026. / 微软 v0.4 重写。2026 Q1 合并入微软 Agent 框架。 |
| [AG2](https://github.com/ag2ai/ag2) | Python | Conversational agents / 对话式 Agent | ![GitHub stars](https://img.shields.io/github/stars/ag2ai/ag2) | Community fork of AutoGen 0.2 by original creators. / 原作者的 AutoGen 0.2 社区分叉。 |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Python | Lightweight multi-agent / 轻量多 Agent | ![GitHub stars](https://img.shields.io/github/stars/openai/openai-agents-python) | Lowest barrier to entry. Tracing, guardrails, 100+ LLM support. / 最低入门门槛。追踪、护栏、100+ LLM 支持。 |
| [Claude Agent SDK](https://github.com/anthropics/claude-code-sdk-python) | Python / TS | Subagent orchestration / 子 Agent 编排 | ![GitHub stars](https://img.shields.io/github/stars/anthropics/claude-code-sdk-python) | Programmatic access to Claude Code as an agent. / 以编程方式将 Claude Code 作为 Agent 使用。 |
| [Google ADK](https://github.com/google/adk-python) | Python | Agent Development Kit / Agent 开发套件 | ![GitHub stars](https://img.shields.io/github/stars/google/adk-python) | Native A2A + MCP support. Tight Gemini integration. / 原生 A2A + MCP 支持。深度 Gemini 集成。 |
| [Semantic Kernel](https://github.com/microsoft/semantic-kernel) | C# / Python / Java | Enterprise AI orchestration / 企业级 AI 编排 | ![GitHub stars](https://img.shields.io/github/stars/microsoft/semantic-kernel) | Microsoft's unified agent framework. 27K+ stars. Multi-language. / 微软统一 Agent 框架。27K+ stars。多语言。 |
| [CAMEL](https://github.com/camel-ai/camel) | Python | Role-playing agents / 角色扮演 Agent | ![GitHub stars](https://img.shields.io/github/stars/camel-ai/camel) | 1st LLM multi-agent framework. Research on scaling laws of agents. / 首个 LLM 多 Agent 框架。研究 Agent 缩放定律。 |

### Emerging & Specialized / 新兴与专业化

| Framework / 框架 | Language / 语言 | Focus / 方向 | Stars |
|-----------|----------|-------|-------|
| [Mastra](https://github.com/mastra-ai/mastra) | TypeScript | TS-native agent framework (by Gatsby team) / TS 原生 Agent 框架（Gatsby 团队） | ![GitHub stars](https://img.shields.io/github/stars/mastra-ai/mastra) |
| [PydanticAI](https://github.com/pydantic/pydantic-ai) | Python | Type-safe agents with structured I/O / 类型安全的结构化 I/O Agent | ![GitHub stars](https://img.shields.io/github/stars/pydantic/pydantic-ai) |
| [PraisonAI](https://github.com/MervinPraison/PraisonAI) | Python | Low-code multi-agent with YAML config / 低代码 YAML 配置多 Agent | ![GitHub stars](https://img.shields.io/github/stars/MervinPraison/PraisonAI) |
| [Swarm](https://github.com/openai/swarm) | Python | Educational multi-agent patterns / 教育性多 Agent 模式 | ![GitHub stars](https://img.shields.io/github/stars/openai/swarm) |
| [MetaGPT](https://github.com/geekan/MetaGPT) | Python | Software company simulation / 软件公司模拟（产品经理→架构师→工程师） | ![GitHub stars](https://img.shields.io/github/stars/geekan/MetaGPT) |
| [DeerFlow](https://github.com/bytedance/deer-flow) | Python | ByteDance SuperAgent. Sub-agents, memory, sandboxes. / 字节跳动超级 Agent。子 Agent + 记忆 + 沙箱。 | ![GitHub stars](https://img.shields.io/github/stars/bytedance/deer-flow) |
| [Strands Agents](https://github.com/strands-agents/sdk-python) | Python | Hierarchical planning, multi-step reasoning (AWS) / 层级规划，多步推理（AWS） | ![GitHub stars](https://img.shields.io/github/stars/strands-agents/sdk-python) |
| [LlamaIndex Workflows](https://github.com/run-llama/llama_index) | Python | Data-aware agent workflows / 数据感知 Agent 工作流 | ![GitHub stars](https://img.shields.io/github/stars/run-llama/llama_index) |
| [Haystack](https://github.com/deepset-ai/haystack) | Python | Composable AI pipelines / 可组合 AI 管道 | ![GitHub stars](https://img.shields.io/github/stars/deepset-ai/haystack) |
| [Smolagents](https://github.com/huggingface/smolagents) | Python | Lightweight HuggingFace agents / 轻量 HuggingFace Agent | ![GitHub stars](https://img.shields.io/github/stars/huggingface/smolagents) |
| [FastAgency](https://github.com/agentuniverse-ai/fastagency) | Python | Notebook → production pipeline / 从 Notebook 到生产的管道 | ![GitHub stars](https://img.shields.io/github/stars/agentuniverse-ai/fastagency) |
| [Agno](https://github.com/agno-agi/agno) | Python | Lightweight multi-modal agents / 轻量多模态 Agent | ![GitHub stars](https://img.shields.io/github/stars/agno-agi/agno) |
| [Atomic Agents](https://github.com/BrainBlend-AI/atomic-agents) | Python | Modular agent building blocks / 模块化 Agent 构建块 | ![GitHub stars](https://img.shields.io/github/stars/BrainBlend-AI/atomic-agents) |
| [OWL](https://github.com/camel-ai/owl) | Python | CAMEL-based multi-agent (browser + terminal + MCP) / 基于 CAMEL 的多 Agent 协作 | ![GitHub stars](https://img.shields.io/github/stars/camel-ai/owl) |

### Choosing a Framework / 框架选择指南

```
Need / 需求                          → Framework / 推荐框架
─────────────────────────────────────────────────────────
Max control + enterprise             → LangGraph
最大控制力 + 企业级

Fast role-based prototyping          → CrewAI
快速角色化原型

TypeScript team                      → Mastra
TypeScript 团队

OpenAI ecosystem                     → OpenAI Agents SDK
OpenAI 生态

Type-safe structured output          → PydanticAI
类型安全结构化输出

Google/Gemini ecosystem              → Google ADK
Google/Gemini 生态

Microsoft/.NET ecosystem             → Semantic Kernel / AutoGen
微软/.NET 生态

Low-code YAML config                 → PraisonAI
低代码 YAML 配置

Software team simulation             → MetaGPT
软件团队模拟

Research + sub-agents                → DeerFlow
研究 + 子 Agent

Role-playing research                → CAMEL
角色扮演研究
```

---

## Autonomous Coding Agents / 自主编码 Agent

*Standalone AI agents that can autonomously write, debug, and ship code. / 能自主编写、调试和发布代码的独立 AI Agent。*

| Agent | Type / 类型 | Stars | Highlights / 亮点 |
|-------|------|-------|------------|
| [OpenHands](https://github.com/OpenHands/OpenHands) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/OpenHands/OpenHands) | Formerly OpenDevin. Model-agnostic, enterprise-ready. Scales to 1000s. / 前 OpenDevin。模型无关，企业就绪。可扩展至数千 Agent。 |
| [SWE-agent](https://github.com/SWE-agent/SWE-agent) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/SWE-agent/SWE-agent) | Princeton/Stanford. Auto-fixes GitHub issues. NeurIPS 2024. / 普林斯顿/斯坦福。自动修复 GitHub Issue。 |
| [Aider](https://github.com/Aider-AI/aider) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/Aider-AI/aider) | Terminal AI pair programming. Git-native, 100+ languages. / 终端 AI 结对编程。Git 原生，100+ 语言。 |
| [Roo Code](https://github.com/RooCodeInc/Roo-Code) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/RooCodeInc/Roo-Code) | VS Code extension. Multi-mode (Architect/Developer/Tester). / VS Code 扩展。多模式（架构师/开发者/测试者）。 |
| [Cline](https://github.com/cline/cline) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/cline/cline) | VS Code/JetBrains. 5M+ installs. MCP marketplace. / 500 万+ 安装。MCP 市场。 |
| [OpenClaw](https://github.com/openclaw/openclaw) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/openclaw/openclaw) | 210K+ stars. Self-improving, writes own skills. / 21 万+ stars。自我改进，编写自己的技能。 |
| [Open SWE](https://github.com/langchain-ai/open-swe) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/langchain-ai/open-swe) | LangChain's async coding agent on LangGraph. / LangChain 基于 LangGraph 的异步编码 Agent。 |
| [DeerFlow](https://github.com/bytedance/deer-flow) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/bytedance/deer-flow) | ByteDance SuperAgent. Docker sandbox. / 字节跳动超级 Agent。Docker 沙箱。 |
| [Mini SWE-agent](https://github.com/SWE-agent/mini-swe-agent) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/SWE-agent/mini-swe-agent) | 100-line agent, 65%+ on SWE-bench. / 100 行代码，SWE-bench 65%+。 |
| [Devin](https://devin.ai/) | Commercial / 商业 | N/A | Cognition Labs. $10.2B valuation. Cloud sandbox. / $102 亿估值。云沙箱。 |

---

## Coding Agent Orchestrators / 编码 Agent 编排器

*Tools for running multiple AI coding agents in parallel. / 并行运行多个 AI 编码 Agent 的工具。*

### Parallel Agent Runners / 并行 Agent 运行器

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [claude-squad](https://github.com/smtg-ai/claude-squad) | Manage multiple AI terminal agents in background with tmux / 用 tmux 在后台管理多个 AI 终端 Agent | ![GitHub stars](https://img.shields.io/github/stars/smtg-ai/claude-squad) |
| [MCO](https://github.com/mco-org/mco) | Neutral orchestration layer for Claude Code, Codex, Gemini, OpenCode, Qwen / 中立编排层，支持 Claude Code、Codex、Gemini、OpenCode、Qwen | ![GitHub stars](https://img.shields.io/github/stars/mco-org/mco) |
| [agent-orchestrator](https://github.com/ComposioHQ/agent-orchestrator) | Plan tasks, spawn agents, handle CI fixes and merge conflicts / 规划任务、生成 Agent、处理 CI 修复和合并冲突 | ![GitHub stars](https://img.shields.io/github/stars/ComposioHQ/agent-orchestrator) |
| [crystal](https://github.com/stravu/crystal) | Run multiple Codex and Claude Code in parallel git worktrees / 在并行 git worktree 中运行多个 Codex 和 Claude Code | ![GitHub stars](https://img.shields.io/github/stars/stravu/crystal) |
| [CCB (Claude Code Bridge)](https://github.com/bfly123/claude_code_bridge) | Real-time multi-AI collaboration via split-pane terminal. 8 providers. 50-200 tokens/call. / 通过分屏终端实时多 AI 协作。8 个 Provider。每次调用仅 50-200 tokens。 | ![GitHub stars](https://img.shields.io/github/stars/bfly123/claude_code_bridge) |
| [dmux](https://github.com/standardagents/dmux) | Parallel agents with tmux and worktrees / tmux + worktree 并行 Agent | ![GitHub stars](https://img.shields.io/github/stars/standardagents/dmux) |
| [amux](https://github.com/andyrewlee/amux) | TUI for running parallel coding agents / 并行编码 Agent 的 TUI 界面 | ![GitHub stars](https://img.shields.io/github/stars/andyrewlee/amux) |
| [cmux](https://github.com/manaflow-ai/cmux) | Open-source platform for parallel coding agents / 并行编码 Agent 的开源平台 | ![GitHub stars](https://img.shields.io/github/stars/manaflow-ai/cmux) |
| [mux](https://github.com/coder/mux) | Desktop app for isolated, parallel agentic development / 隔离并行 Agent 开发的桌面应用 | ![GitHub stars](https://img.shields.io/github/stars/coder/mux) |
| [dorothy](https://github.com/Charlie85270/Dorothy) | Desktop app with automations, Kanban, and MCP servers / 带自动化、看板和 MCP 服务器的桌面应用 | ![GitHub stars](https://img.shields.io/github/stars/Charlie85270/Dorothy) |
| [1code](https://github.com/21st-dev/1code) | UI for Claude Code with local and remote execution / Claude Code 的本地和远程执行 UI | ![GitHub stars](https://img.shields.io/github/stars/21st-dev/1code) |
| [agent-deck](https://github.com/asheshgoplani/agent-deck) | Terminal session manager for AI coding agents / AI 编码 Agent 的终端会话管理器 | ![GitHub stars](https://img.shields.io/github/stars/asheshgoplani/agent-deck) |
| [symphony](https://github.com/openai/symphony) | Turns project work into isolated, autonomous runs / 将项目工作转化为隔离的自主运行 | ![GitHub stars](https://img.shields.io/github/stars/openai/symphony) |
| [CodexMonitor](https://github.com/Dimillian/CodexMonitor) | Orchestrate multiple Codex agents across workspaces / 跨工作区编排多个 Codex Agent | ![GitHub stars](https://img.shields.io/github/stars/Dimillian/CodexMonitor) |
| [vibe-kanban](https://github.com/BloopAI/vibe-kanban) | Kanban board for managing AI coding agents / 管理 AI 编码 Agent 的看板 | ![GitHub stars](https://img.shields.io/github/stars/BloopAI/vibe-kanban) |
| [vibecraft](https://github.com/rayzhudev/vibecraft) | RTS-style workspace for AI coding agents / RTS 风格的 AI 编码 Agent 工作区 | ![GitHub stars](https://img.shields.io/github/stars/rayzhudev/vibecraft) |
| [constellagent](https://github.com/owengretzinger/constellagent) | macOS app: terminal + editor + git worktree per agent / macOS 应用：每个 Agent 一个终端+编辑器+worktree | ![GitHub stars](https://img.shields.io/github/stars/owengretzinger/constellagent) |
| [aizen](https://github.com/vivy-company/aizen) | macOS workspace for git worktrees with agent sessions / 带 Agent 会话的 git worktree macOS 工作区 | ![GitHub stars](https://img.shields.io/github/stars/vivy-company/aizen) |
| [supacode](https://github.com/supabitapp/supacode) | Native macOS coding agent orchestrator / macOS 原生编码 Agent 编排器 | ![GitHub stars](https://img.shields.io/github/stars/supabitapp/supacode) |
| [ai-maestro](https://github.com/23blocks-OS/ai-maestro) | Orchestrate Claude, Aider, Cursor across machines / 跨机器编排 Claude、Aider、Cursor | ![GitHub stars](https://img.shields.io/github/stars/23blocks-OS/ai-maestro) |
| [humanlayer](https://github.com/humanlayer/humanlayer) | Human-in-the-loop for hard problems / 人在回路解决复杂问题 | ![GitHub stars](https://img.shields.io/github/stars/humanlayer/humanlayer) |
| [emdash](https://github.com/generalaction/emdash) | Run multiple coding agents in parallel / 并行运行多个编码 Agent | ![GitHub stars](https://img.shields.io/github/stars/generalaction/emdash) |
| [jean](https://github.com/coollabsio/jean) | Manage projects, worktrees, sessions with Claude CLI / 用 Claude CLI 管理项目、worktree 和会话 | ![GitHub stars](https://img.shields.io/github/stars/coollabsio/jean) |
| [t3code](https://github.com/pingdotgg/t3code) | Minimal web GUI for coding agents / 极简编码 Agent Web 界面 | ![GitHub stars](https://img.shields.io/github/stars/pingdotgg/t3code) |
| [vibe-tree](https://github.com/sahithvibudhi/vibe-tree) | Claude in parallel git worktrees / 在并行 git worktree 中使用 Claude | ![GitHub stars](https://img.shields.io/github/stars/sahithvibudhi/vibe-tree) |
| [openkanban](https://github.com/techdufus/openkanban) | TUI kanban for orchestrating AI agents / 编排 AI Agent 的 TUI 看板 | ![GitHub stars](https://img.shields.io/github/stars/techdufus/openkanban) |
| [subtask](https://github.com/zippoxer/subtask) | Claude Skill for subagents in Git worktrees / 在 Git worktree 中使用子 Agent 的 Claude Skill | ![GitHub stars](https://img.shields.io/github/stars/zippoxer/subtask) |
| [superset](https://github.com/superset-sh/superset) | A terminal built for coding agents / 为编码 Agent 打造的终端 | ![GitHub stars](https://img.shields.io/github/stars/superset-sh/superset) |
| [automaker](https://github.com/AutoMaker-Org/automaker) | Autonomous AI development studio / 自主 AI 开发工作室 | ![GitHub stars](https://img.shields.io/github/stars/AutoMaker-Org/automaker) |
| [ariana](https://github.com/ariana-dot-dev/ariana) | The IDE of the future / 未来 IDE | ![GitHub stars](https://img.shields.io/github/stars/ariana-dot-dev/ariana) |
| [jat](https://github.com/joewinke/jat) | The World's First Agentic IDE / 世界首个 Agentic IDE | ![GitHub stars](https://img.shields.io/github/stars/joewinke/jat) |

### IDE-Integrated Agent Platforms / IDE 集成 Agent 平台

| Platform / 平台 | Multi-Agent? / 多 Agent? | Parallel? / 并行? | Key Feature / 核心特性 |
|----------|:-----:|:---------:|-------------|
| **Claude Code** (Agent Teams) | Yes / 是 | Yes / 是 | Subagent communication, shared task list, worktree isolation / 子 Agent 通信、共享任务列表、worktree 隔离 |
| **Cursor** (Background Agents) | Yes / 是 | 10-20 agents | Cloud VMs, auto-PR generation / 云 VM、自动 PR 生成 |
| **Codex CLI** (Agents SDK) | Yes / 是 | Yes / 是 | Long-running workflows, sandbox execution / 长时间运行工作流、沙箱执行 |
| **Windsurf** | Yes / 是 | 5 agents | Cascading agent flows / 级联 Agent 流 |
| **Copilot** (Coding Agent) | Yes / 是 | Yes / 是 | GitHub-native, auto-assigns issues / GitHub 原生、自动分配 Issue |
| **Grok Build** | Yes / 是 | 8 agents | xAI integration / xAI 集成 |

---

## Chinese AI Orchestration / 中国特色 AI 编排

*AI orchestration projects with Chinese cultural themes or from Chinese developers. / 具有中国文化特色或来自中国开发者的 AI 编排项目。*

### AI 朝廷 (AI Imperial Court / AI 皇廷系统)

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [Edict (三省六部制)](https://github.com/cft0808/edict) | OpenClaw multi-agent system based on Tang Dynasty's 3-department-6-ministry system. 12 agents (Crown Prince triage → Planning Dept → Review Dept → Dispatch → 6 Ministries → Report). Real-time dashboard, 30s end-to-end. / 以唐朝三省六部制为蓝本的多 Agent 编排系统。12 个 Agent 角色（太子分拣→中书省规划→门下省审核→尚书省调度→六部执行→奏折回报），内置实时仪表盘，30 秒完成全流程。 | ![GitHub stars](https://img.shields.io/github/stars/cft0808/edict) |
| [AI 朝廷教程](https://github.com/wanikua/boluobobo-ai-court-tutorial) | Complete tutorial for building your AI Imperial Court from scratch. / AI 朝廷从零搭建完整教程，手把手教你部署 7x24 在线的 AI 朝廷。 | ![GitHub stars](https://img.shields.io/github/stars/wanikua/boluobobo-ai-court-tutorial) |

> **AI 朝廷 vs Traditional Frameworks / 与传统框架对比:**
> - vs CrewAI: Extra review layer (Chancellery). Each agent has explicit court role. / 多了门下省审核层（质量把关），Agent 有明确朝廷角色
> - vs AutoGen: Built-in real-time dashboard ("war room"). / 多了实时仪表盘（军事指挥中心）
> - vs LangGraph: Higher abstraction: "edict → execution → memorial" replaces graph nodes. / 更高层抽象，"圣旨→执行→奏折"替代图节点思维

### CCB (Claude Code Bridge / Claude 代码桥)

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [CCB](https://github.com/bfly123/claude_code_bridge) | Real-time multi-AI collaboration bridge. 8 providers (Claude/Codex/Gemini/OpenCode/Droid/Copilot/CodeBuddy/Qwen). WYSIWYG split-pane terminal. Only 50-200 tokens/call (vs 5K-20K traditional). Persistent sessions with resume support. / 实时多 AI 协作桥梁。8 个 Provider，tmux/WezTerm 分屏终端 WYSIWYG 可视化，每次调用仅 50-200 tokens（传统方式 5K-20K），支持持久会话和断点续传。 | ![GitHub stars](https://img.shields.io/github/stars/bfly123/claude_code_bridge) |

> **What makes CCB unique / CCB 的独特之处:**
> - **WYSIWYG**: Unlike API calls, CCB shows every AI interaction in split-pane terminal / 不同于 API 调用，在终端分屏中直接展示每个 AI 的交互
> - **Ultra-low tokens / 极低 Token 开销**: 50-200 tokens/call = 1/100 of traditional / 是传统方案的 1/100
> - **8 providers unified / 8 Provider 统一**: One CLI manages Claude, Codex, Gemini + 5 more / 一套 CLI 统一管理 8 个 AI
> - **Protocol markers / 协议标记**: CCB_REQ_ID/CCB_DONE, daemon-per-provider architecture / daemon-per-provider 架构

### More Chinese-Origin Projects / 更多中国开源项目

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [Dify](https://github.com/langgenius/dify) | Open-source LLM app platform. Visual workflows + RAG + agent orchestration. 129K+ stars. / 开源 LLM 应用平台，可视化工作流 + RAG + Agent 编排。 | ![GitHub stars](https://img.shields.io/github/stars/langgenius/dify) |
| [MetaGPT](https://github.com/geekan/MetaGPT) | Shenzhen DeepWisdom. Simulates software company (PM → Architect → Engineer) with SOP. / 深圳 DeepWisdom 团队。模拟软件公司，按 SOP 协同开发。 | ![GitHub stars](https://img.shields.io/github/stars/geekan/MetaGPT) |
| [DeerFlow](https://github.com/bytedance/deer-flow) | ByteDance SuperAgent. Sub-agents + memory + sandboxes. GitHub Trending #1. MIT license. / 字节跳动超级 Agent。子 Agent + 记忆 + 沙箱。GitHub Trending #1。MIT 协议。 | ![GitHub stars](https://img.shields.io/github/stars/bytedance/deer-flow) |
| [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) | Alibaba Qwen official agent framework. Function Calling, Code Interpreter, RAG. / 阿里通义千问官方 Agent 框架，支持 Function Calling、Code Interpreter、RAG。 | ![GitHub stars](https://img.shields.io/github/stars/QwenLM/Qwen-Agent) |
| [Open WebUI](https://github.com/open-webui/open-webui) | Self-hosted AI platform. 282M+ downloads, 124K+ stars. Offline capable. / 自托管 AI 平台，2.82 亿+ 下载，支持离线运行。 | ![GitHub stars](https://img.shields.io/github/stars/open-webui/open-webui) |
| [RAGFlow](https://github.com/infiniflow/ragflow) | Deep document understanding RAG engine with agent orchestration. / 深度文档理解的 RAG 引擎，支持 Agent 编排和知识库管理。 | ![GitHub stars](https://img.shields.io/github/stars/infiniflow/ragflow) |
| [CAMEL](https://github.com/camel-ai/camel) | 1st LLM multi-agent framework. Research on agent scaling laws. / 第一个 LLM 多 Agent 框架，专注 Agent 扩展定律研究。 | ![GitHub stars](https://img.shields.io/github/stars/camel-ai/camel) |
| [Coze (扣子)](https://www.coze.com/) | ByteDance agent platform. Rich plugin ecosystem, visual workflow orchestration. / 字节跳动 Agent 平台，丰富插件生态，可视化工作流编排。 | N/A |

---

## Low-Code / Visual Platforms / 低代码可视化平台

*Build agent workflows visually without deep coding. / 无需深度编码即可可视化构建 Agent 工作流。*

| Platform / 平台 | Type / 类型 | Stars | Highlights / 亮点 |
|----------|------|-------|------------|
| [Dify](https://github.com/langgenius/dify) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/langgenius/dify) | Visual workflow + RAG + LLMOps. 129K+ stars. / 可视化工作流 + RAG + LLMOps。 |
| [n8n](https://github.com/n8n-io/n8n) | Source Available / 源码可用 | ![GitHub stars](https://img.shields.io/github/stars/n8n-io/n8n) | 400+ integrations, workflow automation + AI agents / 400+ 集成，工作流自动化 + AI Agent |
| [Flowise](https://github.com/FlowiseAI/Flowise) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/FlowiseAI/Flowise) | Drag & drop multi-agent orchestration / 拖拽式多 Agent 编排 |
| [LangFlow](https://github.com/langflow-ai/langflow) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/langflow-ai/langflow) | Visual LangChain builder / 可视化 LangChain 构建器 |
| [RAGFlow](https://github.com/infiniflow/ragflow) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/infiniflow/ragflow) | Deep document understanding + agent orchestration / 深度文档理解 + Agent 编排 |
| [Coze](https://www.coze.com/) | Commercial / 商业 | N/A | ByteDance's agent platform / 字节跳动 Agent 平台 |
| [Wordware](https://github.com/wordware-ai/twitter) | Commercial / 商业 | N/A | Natural language programming for AI agents / 自然语言编程 |

---

## Observability & Evaluation / 可观测性与评估

*Monitor, debug, and evaluate agent performance in production. / 在生产环境中监控、调试和评估 Agent 性能。*

| Tool / 工具 | Type / 类型 | Stars | Focus / 方向 |
|------|------|-------|-------|
| [Langfuse](https://github.com/langfuse/langfuse) | Open Source (MIT) / 开源 | ![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse) | Tracing, prompt management, evaluation. 6M+ installs/month. / 追踪、提示词管理、评估。月安装 600 万+。 |
| [Arize Phoenix](https://github.com/Arize-ai/phoenix) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/Arize-ai/phoenix) | Self-hosted observability. Strong eval + tracing. / 自托管可观测性。强评估 + 追踪。 |
| [LangSmith](https://smith.langchain.com/) | Commercial / 商业 | N/A | Deep LangChain integration. Near-zero overhead. / 深度 LangChain 集成。接近零开销。 |
| [AgentOps](https://github.com/AgentOps-AI/agentops) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/AgentOps-AI/agentops) | Agent-specific observability with session replay. / Agent 专属可观测性，带会话回放。 |
| [Laminar](https://github.com/lmnr-ai/lmnr) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/lmnr-ai/lmnr) | Minimal overhead (5%). Rust-powered. / 最低开销（5%）。Rust 驱动。 |
| [Helicone](https://github.com/Helicone/helicone) | Open Source / 开源 | ![GitHub stars](https://img.shields.io/github/stars/Helicone/helicone) | Gateway-based observability. / 基于网关的可观测性。 |
| [Braintrust](https://www.braintrust.dev/) | Commercial / 商业 | N/A | Eval, logging, and prompt playground. / 评估、日志和提示词实验场。 |

---

## Agent Infrastructure / Agent 基础设施

*Execution environments, sandboxes, and deployment tools. / 执行环境、沙箱和部署工具。*

| Tool / 工具 | Purpose / 用途 | Stars |
|------|---------|-------|
| [E2B](https://github.com/e2b-dev/e2b) | Cloud sandboxes for AI agents / AI Agent 的云沙箱 | ![GitHub stars](https://img.shields.io/github/stars/e2b-dev/e2b) |
| [Modal](https://modal.com/) | Serverless compute for agent workloads / Agent 负载的无服务器计算 | N/A |
| [Daytona](https://github.com/daytonaio/daytona) | Dev environments for AI agents / AI Agent 的开发环境 | ![GitHub stars](https://img.shields.io/github/stars/daytonaio/daytona) |
| [Composio](https://github.com/ComposioHQ/composio) | 250+ tool integrations for AI agents / AI Agent 的 250+ 工具集成 | ![GitHub stars](https://img.shields.io/github/stars/ComposioHQ/composio) |
| [ToolHouse](https://github.com/toolhouseai/toolhouse) | Tool execution infrastructure / 工具执行基础设施 | ![GitHub stars](https://img.shields.io/github/stars/toolhouseai/toolhouse) |
| [Browserbase](https://github.com/browserbase/stagehand) | Browser automation for agents (Stagehand) / Agent 浏览器自动化 | ![GitHub stars](https://img.shields.io/github/stars/browserbase/stagehand) |
| [Firecrawl](https://github.com/mendableai/firecrawl) | Web scraping API optimized for LLMs / 为 LLM 优化的网页抓取 API | ![GitHub stars](https://img.shields.io/github/stars/mendableai/firecrawl) |
| [Crawl4AI](https://github.com/unclecode/crawl4ai) | Open-source LLM-friendly web crawling / LLM 友好的开源网页爬取 | ![GitHub stars](https://img.shields.io/github/stars/unclecode/crawl4ai) |

---

## Personal AI Assistants / 个人 AI 助手

*Always-on AI assistants with memory and multi-platform presence. / 具有记忆和多平台存在的全天候 AI 助手。*

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [OpenClaw](https://github.com/openclaw/openclaw) | 210K+ stars. Self-improving, writes own skills. 20+ platforms. / 21 万+ stars。自我改进，编写自己的技能。20+ 平台。 | ![GitHub stars](https://img.shields.io/github/stars/openclaw/openclaw) |
| [Leon](https://github.com/leon-ai/leon) | Open-source personal assistant (voice + text) / 开源个人助手（语音+文字） | ![GitHub stars](https://img.shields.io/github/stars/leon-ai/leon) |
| [BabyAGI](https://github.com/yoheinakajima/babyagi3) | Minimal AI agent — configure once, run via natural language / 极简 AI Agent — 配置一次，自然语言运行 | ![GitHub stars](https://img.shields.io/github/stars/yoheinakajima/babyagi3) |
| [Happy](https://github.com/slopus/happy) | Mobile/web client for Claude Code, Codex, Gemini CLI. E2E encrypted. / AI CLI 的移动/Web 客户端。端到端加密。 | ![GitHub stars](https://img.shields.io/github/stars/slopus/happy) |
| [Letta](https://github.com/letta-ai/letta) | AI assistant framework with persistent memory / 具有持久记忆的 AI 助手框架 | ![GitHub stars](https://img.shields.io/github/stars/letta-ai/letta) |
| [rho](https://github.com/mikeyobrien/rho) | Agent with persistent memory and autonomous updates / 带持久记忆和自主更新的 Agent | ![GitHub stars](https://img.shields.io/github/stars/mikeyobrien/rho) |

---

## Autonomous Loop Runners / 自主循环执行器

*"Keep running until done" patterns for agent workflows. / Agent 工作流的"持续运行直到完成"模式。*

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) | Keeps agents in a loop until done / 让 Agent 循环运行直到完成 | ![GitHub stars](https://img.shields.io/github/stars/mikeyobrien/ralph-orchestrator) |
| [ralph-tui](https://github.com/subsy/ralph-tui) | Orchestrate AI agents through task lists autonomously / 通过任务列表自主编排 AI Agent | ![GitHub stars](https://img.shields.io/github/stars/subsy/ralph-tui) |
| [ralph-claude-code](https://github.com/frankbria/ralph-claude-code) | Autonomous AI dev loop with intelligent exit detection / 带智能退出检测的自主开发循环 | ![GitHub stars](https://img.shields.io/github/stars/frankbria/ralph-claude-code) |
| [ralphy](https://github.com/michaelshimeles/ralphy) | Runs AI agents on tasks until done / 在任务上运行 AI Agent 直到完成 | ![GitHub stars](https://img.shields.io/github/stars/michaelshimeles/ralphy) |
| [wreckit](https://github.com/mikehostetler/wreckit) | Run loop over your roadmap / 在路线图上运行循环 | ![GitHub stars](https://img.shields.io/github/stars/mikehostetler/wreckit) |
| [loom](https://github.com/ghuntley/loom) | Autonomous loops that evolve products / 自主进化产品的循环 | ![GitHub stars](https://img.shields.io/github/stars/ghuntley/loom) |
| [lalph](https://github.com/tim-smart/lalph) | LLM agent orchestrator driven by issue sources / 由 Issue 源驱动的 LLM Agent 编排器 | ![GitHub stars](https://img.shields.io/github/stars/tim-smart/lalph) |

---

## Multi-Agent Swarms / 多 Agent 蜂群

*Coordinated swarms of specialized agents. / 协调的专业化 Agent 蜂群。*

| Tool / 工具 | Description / 描述 | Stars |
|------|-------------|-------|
| [claude-flow](https://github.com/ruvnet/claude-flow) | Multi-agent swarms with coordinated workflows / 具有协调工作流的多 Agent 蜂群 | ![GitHub stars](https://img.shields.io/github/stars/ruvnet/claude-flow) |
| [ruflo](https://github.com/ruvnet/ruflo) | Enterprise-grade swarm intelligence with RAG / 企业级蜂群智能 + RAG | ![GitHub stars](https://img.shields.io/github/stars/ruvnet/ruflo) |
| [gastown](https://github.com/steveyegge/gastown) | Multi-agent with persistent work tracking / 带持久工作追踪的多 Agent | ![GitHub stars](https://img.shields.io/github/stars/steveyegge/gastown) |
| [paperclip](https://github.com/paperclipai/paperclip) | Orchestration for fully autonomous organizations / 全自主组织的编排 | ![GitHub stars](https://img.shields.io/github/stars/paperclipai/paperclip) |
| [overstory](https://github.com/jayminwest/overstory) | Pluggable runtime adapters for Claude Code, Pi, etc. / 可插拔运行时适配器 | ![GitHub stars](https://img.shields.io/github/stars/jayminwest/overstory) |
| [antfarm](https://github.com/snarktank/antfarm) | Build agent team in OpenClaw with one command / 一行命令构建 Agent 团队 | ![GitHub stars](https://img.shields.io/github/stars/snarktank/antfarm) |
| [clawe](https://github.com/getclawe/clawe) | Trello for OpenClaw agents / OpenClaw Agent 的 Trello | ![GitHub stars](https://img.shields.io/github/stars/getclawe/clawe) |
| [opengoat](https://github.com/marian2js/opengoat) | Build AI autonomous organizations / 构建 AI 自治组织 | ![GitHub stars](https://img.shields.io/github/stars/marian2js/opengoat) |
| [openfang](https://github.com/RightNow-AI/openfang) | Open-source Agent Operating System / 开源 Agent 操作系统 | ![GitHub stars](https://img.shields.io/github/stars/RightNow-AI/openfang) |
| [OASIS](https://github.com/camel-ai/oasis) | Social simulations with 1M agents / 百万 Agent 社交模拟 | ![GitHub stars](https://img.shields.io/github/stars/camel-ai/oasis) |

---

## Benchmarks & Evaluation / 基准测试与评估

*Benchmarks for measuring agent and multi-agent system performance. / 衡量 Agent 和多 Agent 系统性能的基准。*

| Benchmark / 基准 | Focus / 方向 | Paper / 论文 |
|-----------|-------|-------|
| [SWE-bench](https://github.com/SWE-bench/SWE-bench) | Real-world GitHub issue resolution / 真实 GitHub Issue 解决 | [arXiv:2310.06770](https://arxiv.org/abs/2310.06770) |
| [SWE-bench Pro](https://www.swebench.com/) | Long-horizon enterprise tasks (1,865 problems) / 长周期企业级任务 | [arXiv:2509.16941](https://arxiv.org/abs/2509.16941) |
| [SWE-bench Live](https://swe-bench-live.github.io/) | Live benchmark with updated issues / 持续更新的实时基准 | — |
| [MultiAgentBench](https://arxiv.org/abs/2503.01935) | Multi-agent collaboration & competition / 多 Agent 协作与竞争评估 | ACL 2025 |
| [MAFBench](https://arxiv.org/abs/2602.03128) | Unified multi-agent framework benchmark / 统一多 Agent 框架基准 | [arXiv:2602.03128](https://arxiv.org/abs/2602.03128) |
| [AgentBench](https://github.com/THUDM/AgentBench) | 8-environment LLM-as-Agent evaluation / 8 环境 LLM-as-Agent 评估 | [arXiv:2308.03688](https://arxiv.org/abs/2308.03688) |
| [WebArena](https://github.com/web-arena-x/webarena) | Realistic web environment for agents / 真实 Web 环境 | [arXiv:2307.13854](https://arxiv.org/abs/2307.13854) |
| [Terminal-Bench](https://terminalbench.com/) | Command-line agent evaluation (Stanford) / 命令行 Agent 评估（斯坦福） | — |
| [DPAI Arena](https://arena.jetbrains.com/) | JetBrains developer productivity benchmark / JetBrains 开发者生产力基准 | — |

---

## Academic Papers / 学术论文

*Key research papers on AI agent orchestration. / AI Agent 编排的关键研究论文。*

### Surveys & Overviews / 综述

| Paper / 论文 | Venue / 发表 | Date / 日期 | Link / 链接 |
|-------|-------------|------|------|
| The Orchestration of Multi-Agent Systems: Architectures, Protocols, and Enterprise Adoption / 多 Agent 系统编排：架构、协议和企业采纳 | — | Jan 2026 | [2601.13671](https://arxiv.org/abs/2601.13671) |
| AI Agent Systems: Architectures, Applications, and Evaluation / AI Agent 系统：架构、应用和评估 | — | Jan 2026 | [2601.01743](https://arxiv.org/abs/2601.01743) |
| Agentic AI: Architectures, Taxonomies, and Evaluation of LLM Agents / Agentic AI：LLM Agent 的架构、分类和评估 | — | Jan 2026 | [2601.12560](https://arxiv.org/abs/2601.12560) |
| A Survey on Agent Workflow — Status and Future / Agent 工作流综述：现状与未来 | — | Aug 2025 | [2508.01186](https://arxiv.org/abs/2508.01186) |
| Evaluation and Benchmarking of LLM Agents: A Survey / LLM Agent 评估与基准测试综述 | ACM SIGKDD 2025 | Jul 2025 | [2507.21504](https://arxiv.org/abs/2507.21504) |
| Agentic AI: A Comprehensive Survey / Agentic AI 综合综述 | Springer AI Review | Oct 2025 | [2510.25445](https://arxiv.org/abs/2510.25445) |
| Large Language Model Agent: A Survey on Methodology / 大语言模型 Agent 方法论综述 | CoLing 2025 | Mar 2025 | [2503.21460](https://arxiv.org/abs/2503.21460) |
| Agentic Large Language Models, a Survey / Agentic 大语言模型综述 | — | Mar 2025 | [2503.23037](https://arxiv.org/abs/2503.23037) |
| A Survey on LLM-based Multi-Agent System / 基于 LLM 的多 Agent 系统综述 | — | Dec 2024 | [2412.17481](https://arxiv.org/abs/2412.17481) |
| LLM-based Multi-Agents: A Survey of Progress / 基于 LLM 的多 Agent：进展综述 | — | Feb 2024 | [2402.01680](https://arxiv.org/abs/2402.01680) |

### Multi-Agent Communication & Collaboration / 多 Agent 通信与协作

| Paper / 论文 | Venue / 发表 | Date / 日期 | Link / 链接 |
|-------|-------------|------|------|
| Beyond Self-Talk: A Communication-Centric Survey of LLM-Based MAS / 超越自言自语：以通信为中心的 LLM 多 Agent 系统综述 | — | Feb 2025 | [2502.14321](https://arxiv.org/abs/2502.14321) |
| Multi-Agent Collaboration Mechanisms: A Survey of LLMs / 多 Agent 协作机制：LLM 综述 | — | Jan 2025 | [2501.06322](https://arxiv.org/abs/2501.06322) |
| LLM-Based Human-Agent Collaboration Systems: A Survey / 基于 LLM 的人机协作系统综述 | — | May 2025 | [2505.00753](https://arxiv.org/abs/2505.00753) |
| Large Language Models Miss the Multi-Agent Mark / 大语言模型未达多 Agent 标准 | — | May 2025 | [2505.21298](https://arxiv.org/abs/2505.21298) |
| Understanding Multi-Agent LLM Frameworks: A Unified Benchmark / 理解多 Agent LLM 框架：统一基准 | — | Feb 2026 | [2602.03128](https://arxiv.org/abs/2602.03128) |
| MultiAgentBench: Evaluating Collaboration and Competition / 多 Agent 基准：评估协作与竞争 | ACL 2025 | Mar 2025 | [2503.01935](https://arxiv.org/abs/2503.01935) |

### Protocols & Interoperability / 协议与互操作性

| Paper / 论文 | Venue / 发表 | Date / 日期 | Link / 链接 |
|-------|-------------|------|------|
| Survey of Agent Interoperability Protocols: MCP, ACP, A2A, ANP / Agent 互操作协议综述 | — | May 2025 | [2505.02279](https://arxiv.org/abs/2505.02279) |
| Security Threat Modeling for AI-Agent Protocols / AI Agent 协议的安全威胁建模 | — | Feb 2026 | [2602.11327](https://arxiv.org/abs/2602.11327) |
| MCP × A2A Framework for Enhancing Interoperability / MCP × A2A 增强互操作性框架 | — | Jun 2025 | [2506.01804](https://arxiv.org/abs/2506.01804) |
| Advancing Multi-Agent Systems Through MCP / 通过 MCP 推进多 Agent 系统 | — | Apr 2025 | [2504.21030](https://arxiv.org/abs/2504.21030) |
| Beyond Context Sharing: Unified ACP / 超越上下文共享：统一 ACP | — | Feb 2026 | [2602.15055](https://arxiv.org/abs/2602.15055) |

### Agent Reasoning & Planning / Agent 推理与规划

| Paper / 论文 | Venue / 发表 | Date / 日期 | Link / 链接 |
|-------|-------------|------|------|
| Agentic Reasoning for Large Language Models / 大语言模型的 Agentic 推理 | — | Jan 2026 | [2601.12538](https://arxiv.org/abs/2601.12538) |
| ReAct: Synergizing Reasoning and Acting in LMs / ReAct：协同推理与行动 | ICLR 2023 | 2022 | [2210.03629](https://arxiv.org/abs/2210.03629) |
| Tree of Thoughts: Deliberate Problem Solving with LLMs / 思维树：LLM 的深思熟虑式问题解决 | NeurIPS 2023 | 2023 | [2305.10601](https://arxiv.org/abs/2305.10601) |
| Language Agent Tree Search Unifies Reasoning, Acting, and Planning / LATS：统一推理、行动和规划 | — | 2023 | [2310.04406](https://arxiv.org/abs/2310.04406) |
| Emerging AI Agent Architectures for Reasoning, Planning, and Tool Calling / 新兴 AI Agent 架构 | — | Apr 2024 | [2404.11584](https://arxiv.org/abs/2404.11584) |
| Towards Autonomous Agents: Adaptive-planning / 走向自主 Agent：自适应规划 | — | Aug 2024 | [2408.06458](https://arxiv.org/abs/2408.06458) |

### Coding Agents & Software Engineering / 编码 Agent 与软件工程

| Paper / 论文 | Venue / 发表 | Date / 日期 | Link / 链接 |
|-------|-------------|------|------|
| SWE-agent: Agent-Computer Interfaces Enable Automated SE / SWE-agent：Agent-计算机接口使软件工程自动化 | NeurIPS 2024 | 2024 | [2405.15793](https://arxiv.org/abs/2405.15793) |
| SWE-bench: Can LMs Resolve Real-world GitHub Issues? / SWE-bench：LM 能解决真实 GitHub Issue 吗？ | ICLR 2024 | 2023 | [2310.06770](https://arxiv.org/abs/2310.06770) |
| SWE-Bench Pro: Can AI Agents Solve Long-Horizon SE Tasks? / AI Agent 能解决长周期软件工程任务吗？ | — | Sep 2025 | [2509.16941](https://arxiv.org/abs/2509.16941) |
| Adaptation of Agentic AI / Agentic AI 的适应 | Stanford/Harvard/Berkeley/Caltech | Dec 2025 | — |

### Paper Collections / 论文集

| Resource / 资源 | Description / 描述 |
|----------|-------------|
| [Awesome-Agent-Papers](https://github.com/luo-junyu/Awesome-Agent-Papers) | Up-to-date paper collection on LLM agents / 持续更新的 LLM Agent 论文集 |
| [LLM-Agent-Survey](https://github.com/xinzhel/LLM-Agent-Survey) | Survey on LLM Agents (CoLing 2025) / LLM Agent 综述（CoLing 2025） |
| [free-ai-agents-resources](https://github.com/avinash201199/free-ai-agents-resources) | Free AI Agents Resources — 2026 Learning Hub / 免费 AI Agent 资源中心 |

---

## Courses & Tutorials / 课程与教程

*Learn to build and orchestrate AI agent systems. / 学习构建和编排 AI Agent 系统。*

### Free Courses / 免费课程

| Course / 课程 | Platform / 平台 | Focus / 方向 |
|--------|----------|-------|
| [Agentic AI](https://learn.deeplearning.ai/courses/agentic-ai/) | DeepLearning.AI | Andrew Ng. Iterative agent workflows. / 吴恩达。迭代式 Agent 工作流。 |
| [Multi AI Agent Systems with CrewAI](https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/) | DeepLearning.AI | Design and prompt teams of AI agents. / 设计和提示 AI Agent 团队。 |
| [AI Agents in LangGraph](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/) | DeepLearning.AI | Build agents from scratch with LangGraph. / 从零用 LangGraph 构建 Agent。 |
| [A2A: The Agent2Agent Protocol](https://www.deeplearning.ai/short-courses/a2a-the-agent2agent-protocol/) | DeepLearning.AI | Build healthcare multi-agent with A2A. / 用 A2A 构建医疗多 Agent 系统。 |
| [Agentic AI with LangGraph, CrewAI, AutoGen and BeeAI](https://www.coursera.org/learn/agentic-ai-with-langgraph-crewai-autogen-and-beeai) | Coursera (IBM) | Compare and build with 4 frameworks. / 对比和构建 4 大框架。 |
| [Agentic AI with LangChain and LangGraph](https://www.coursera.org/learn/agentic-ai-with-langchain-and-langgraph) | Coursera (IBM) | 3 weeks. Agent orchestration, routing, governance. / 3 周。Agent 编排、路由、治理。 |
| [AI Agents with LangChain and LangGraph](https://www.udacity.com/course/ai-agents-with-langchain-and-langgraph--cd13764) | Udacity | Practical LangGraph development. / 实用 LangGraph 开发。 |

### Paid Courses & Specializations / 付费课程与专项

| Course / 课程 | Platform / 平台 | Focus / 方向 |
|--------|----------|-------|
| [Building AI Agents and Agentic Workflows](https://www.coursera.org/specializations/building-ai-agents-and-agentic-workflows) | Coursera (IBM) | Specialization: CrewAI workflows, modular agents. / 专项：CrewAI 工作流，模块化 Agent。 |
| [IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai) | Coursera (IBM) | RAG + LangChain + LangGraph + CrewAI + AG2 + BeeAI + MCP. / 全栈 6 框架 + MCP。 |
| [Build Powerful AI Agents with OpenAI Tools](https://www.coursera.org/professional-certificates/build-ai-agents-with-openai-tools) | Coursera | OpenAI Agents SDK, multi-agent orchestration. / OpenAI Agents SDK，多 Agent 编排。 |
| [Agentic AI Nanodegree](https://www.udacity.com/course/agentic-ai--nd900) | Udacity | Comprehensive: design, deploy, coordinate agents. / 综合：设计、部署、协调 Agent。 |
| [AI Engineer Agentic Track](https://www.udemy.com/course/the-complete-agentic-ai-engineering-course/) | Udemy | 30 days, 8 projects. 5 frameworks + MCP. / 30 天 8 个项目，5 框架 + MCP。 |
| [The Agentic AI Engineering Masterclass 2026](https://www.udemy.com/course/become-an-ai-agent-workflow-automation-engineer/) | Udemy | Memory, tools, collaboration, automation. / 记忆、工具、协作、自动化。 |
| [100 AI Agents in 100 Days](https://www.udemy.com/course/100-ai-agents/) | Udemy | Project-driven. Concepts to production. / 项目驱动。从概念到生产。 |
| [2026 Bootcamp: Build Professional AI Agents](https://www.udemy.com/course/2025-bootcamp-understand-and-build-professional-ai-agents/) | Udemy | 45K+ students from 154 countries. / 来自 154 国的 4.5 万+ 学生。 |
| [AI Agents in Python](https://www.coursera.org/specializations/ai-agents-python) | Coursera | Python-focused multi-agent specialization. / Python 多 Agent 专项。 |

### Free Tutorial Resources / 免费教程资源

| Resource / 资源 | Description / 描述 |
|----------|-------------|
| [free-ai-agents-resources](https://github.com/avinash201199/free-ai-agents-resources) | All-in-one 2026 learning hub / 2026 一站式学习中心 |
| [15 FREE AI Agent Courses](https://www.analyticsvidhya.com/blog/2025/10/free-ai-agent-courses/) | Curated list with certificates / 带证书的精选列表 |
| [CrewAI vs LangGraph vs AutoGen Tutorial](https://www.datacamp.com/tutorial/crewai-vs-langgraph-vs-autogen) | DataCamp hands-on comparison / DataCamp 动手对比 |

---

## Learning Resources / 学习资源

### Articles & Guides / 文章与指南

- [Conductors to Orchestrators: The Future of Agentic Coding](https://www.oreilly.com/radar/conductors-to-orchestrators-the-future-of-agentic-coding/) — O'Reilly / 从指挥到编排：Agentic 编码的未来
- [A Developer's Guide to Agentic Frameworks in 2026](https://pub.towardsai.net/a-developers-guide-to-agentic-frameworks-in-2026-3f22a492dc3d) — Towards AI / 2026 Agentic 框架开发者指南
- [LangGraph vs CrewAI vs AutoGen: Complete Guide](https://dev.to/pockit_tools/langgraph-vs-crewai-vs-autogen-the-complete-multi-agent-ai-orchestration-guide-for-2026-2d63) — DEV Community / 完整对比指南
- [The State of AI Coding Agents (2026)](https://medium.com/@dave-patten/the-state-of-ai-coding-agents-2026-from-pair-programming-to-autonomous-ai-teams-b11f2b39232a) — Medium / 2026 AI 编码 Agent 现状
- [MCP & Multi-Agent AI: Building Collaborative Intelligence](https://onereach.ai/blog/mcp-multi-agent-ai-collaborative-intelligence/) — OneReach / MCP 与多 Agent AI：构建协作智能
- [The 2026 MCP Roadmap](https://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/) — MCP Blog / 2026 MCP 路线图
- [Agentic Coding 2026: AI Agent Teams Guide](https://halallens.no/en/blog/agentic-coding-in-2026-the-complete-guide-to-plugins-multi-model-orchestration-and-ai-agent-teams) — Complete guide / AI Agent 团队完整指南
- [Open Source AI Agent Comparison](https://www.ilsilfverskiold.com/articles/agentic-aI-comparing-new-open-source-frameworks) — AG2, PydanticAI, BeeAI, Mastra / 开源 AI Agent 对比
- [Top 10 Open Source AI Projects on GitHub](https://github.blog/open-source/maintainers/from-mcp-to-multi-agents-the-top-10-open-source-ai-projects-on-github-right-now-and-why-they-matter/) — GitHub Blog / GitHub 上 10 大开源 AI 项目
- [Why Most Agentic AI Falls Apart in Real Use](https://www.marktechpost.com/2025/12/24/this-ai-paper-from-stanford-and-harvard-explains-why-most-agentic-ai-systems-feel-impressive-in-demos-and-then-completely-fall-apart-in-real-use/) — Stanford/Harvard / 为什么大多数 Agentic AI 在实际使用中崩溃

### Comparison & Benchmarks / 对比与基准

- [AI Agent Frameworks Compared](https://langfuse.com/blog/2025-03-19-ai-agent-comparison) — Langfuse / AI Agent 框架对比
- [AI Coding Agents Comparison 2026](https://lushbinary.com/blog/ai-coding-agents-comparison-cursor-windsurf-claude-copilot-kiro-2026/) — Lushbinary / 2026 AI 编码 Agent 对比
- [The AI Agent Tools Landscape: 120+ Tools Mapped](https://www.stackone.com/blog/ai-agent-tools-landscape-2026/) — StackOne / AI Agent 工具全景图
- [Top 18 Open Source AI Agent Projects by Stars](https://www.nocobase.com/en/blog/github-open-source-ai-agent-projects) — NocoBase / 18 大开源 AI Agent 项目
- [Best Open Source AI Coding Agents 2026](https://cssauthor.com/best-open-source-ai-coding-agents/) — CSS Author / 2026 最佳开源 AI 编码 Agent
- [8 Benchmarks Shaping Next-Gen AI Agents](https://ainativedev.io/news/8-benchmarks-shaping-the-next-generation-of-ai-agents) — AI Native Dev / 塑造下一代 AI Agent 的 8 个基准

### Existing Awesome Lists / 相关 Awesome 列表

- [awesome-agents](https://github.com/kyrolabs/awesome-agents) — Comprehensive list of AI agents / AI Agent 综合列表
- [awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) — List of autonomous AI agents / 自主 AI Agent 列表
- [awesome-agent-orchestrators](https://github.com/andyrewlee/awesome-agent-orchestrators) — Coding agent orchestrators / 编码 Agent 编排器
- [awesome-llm-agents](https://github.com/kaushikb11/awesome-llm-agents) — LLM agent frameworks / LLM Agent 框架
- [awesome-devins](https://github.com/e2b-dev/awesome-devins) — Devin-inspired AI agents / Devin 类 AI Agent
- [awesome-ai-tools](https://github.com/mahseema/awesome-ai-tools) — General AI tools collection / AI 工具集合
- [500-AI-Agents-Projects](https://github.com/ashishpatel26/500-AI-Agents-Projects) — 500 AI agent use cases / 500 个 AI Agent 用例
- [awesome-AI-driven-development](https://github.com/eltociear/awesome-AI-driven-development) — AI-driven development tools / AI 驱动的开发工具
- [Awesome-Agent-Papers](https://github.com/luo-junyu/Awesome-Agent-Papers) — LLM agent research papers / LLM Agent 研究论文

---

## Contributing / 参与贡献

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

欢迎贡献！请先阅读[贡献指南](CONTRIBUTING.md)。

## License / 许可证

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
