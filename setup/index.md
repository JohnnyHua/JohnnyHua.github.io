---
layout: default
title: Development Setup
---

<h1 data-lang="en">Development Setup</h1>
<h1 data-lang="zh" style="display: none;">开发环境</h1>

<div data-lang="en">My development environment and self-built tools.</div>
<div data-lang="zh" style="display: none;">我的开发环境和自制工具。</div>

---

## <span data-lang="en">Hardware</span><span data-lang="zh" style="display: none;">硬件</span>

- MacBook
- iTerm2

---

## <span data-lang="en">Editor & IDE</span><span data-lang="zh" style="display: none;">编辑器 & IDE</span>

<div data-lang="en">
**Primary**: Cursor

Tried Trae, but one Cursor is enough.
</div>
<div data-lang="zh" style="display: none;">
**主力**: Cursor

试过 Trae，但一个 Cursor 就够了。
</div>

---

## <span data-lang="en">AI Tools</span><span data-lang="zh" style="display: none;">AI 工具</span>

<div data-lang="en">
| Tool | Role |
|------|------|
| ChatGPT | Pre-development planning (voice input) |
| Codex | Daily coding |
| Claude Code | Daily coding |
| OpenCode | Flexible model selection |
| GLM-5 (Ali Bailian) | High-volume tasks, fallback |
| Cursor | Company projects |

See [Workflow](/workflow/) for details.
</div>
<div data-lang="zh" style="display: none;">
| 工具 | 用途 |
|------|------|
| ChatGPT | 开发前规划（语音输入） |
| Codex | 日常编码 |
| Claude Code | 日常编码 |
| OpenCode | 灵活选模型 |
| GLM-5 (阿里百炼) | 高用量任务，备用 |
| Cursor | 公司项目 |

详见 [开发流程](/workflow/)。
</div>

---

## <span data-lang="en">Self-Built Tools</span><span data-lang="zh" style="display: none;">自制工具</span>

### aibrain

<div data-lang="en">
Personal AI memory assistant — todolist, knowledge base, daily reminders.

- [GitHub](https://github.com/JohnnyHua/aibrain)
- See [Projects → aibrain](/projects/aibrain.html)
</div>
<div data-lang="zh" style="display: none;">
个人 AI 记忆助手 — todolist、知识库、日常提醒。

- [GitHub](https://github.com/JohnnyHua/aibrain)
- 详见 [项目 → aibrain](/projects/aibrain.html)
</div>

### PCP (Progress Control Plane)

<div data-lang="en">
Protocol layer and state kernel for PM-Agent and Dev-Agent collaboration.

**Problem it solves**:
- AI sessions drift from scope
- Work gets interrupted and cannot resume
- Completion claimed without verifiable evidence
- Multi-session development lacks consistent state

**Core value**:
- Single source of truth for task state
- Evidence-first completion rules
- Predictable handoff across sessions/models
- Tool-agnostic protocol

**Status**: In development
</div>
<div data-lang="zh" style="display: none;">
PM-Agent 和 Dev-Agent 协作的协议层和状态内核。

**解决的问题**：
- AI 会话偏离范围
- 工作中断无法恢复
- 没有证据就声称完成
- 多会话开发缺乏一致状态

**核心价值**：
- 任务状态的单一数据源
- 证据优先的完成规则
- 跨会话/模型的可预测交接
- 工具无关的协议

**状态**：开发中
</div>

---

## <span data-lang="en">Other Tools</span><span data-lang="zh" style="display: none;">其他工具</span>

- Git（<span data-lang="en">command line</span><span data-lang="zh" style="display: none;">命令行</span>）
- Docker / Docker Compose