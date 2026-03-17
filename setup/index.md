---
layout: default
title: Development Setup
---

# Development Setup

My development environment and self-built tools.

---

## Hardware

- MacBook
- iTerm2

---

## Editor & IDE

**Primary**: Cursor

Tried Trae, but one Cursor is enough.

---

## AI Tools

| Tool | Role |
|------|------|
| ChatGPT | Pre-development planning (voice input) |
| Codex | Daily coding |
| Claude Code | Daily coding |
| OpenCode | Flexible model selection |
| GLM-5 (Ali Bailian) | High-volume tasks, fallback |
| Cursor | Company projects |

See [Workflow](/workflow/) for details.

---

## Self-Built Tools

### aibrain

Personal AI memory assistant — todolist, knowledge base, daily reminders.

- [GitHub](https://github.com/JohnnyHua/aibrain)
- See [Projects → aibrain](/projects/aibrain.html)

### PCP (Progress Control Plane)

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

---

## Other Tools

- Git (command line)
- Docker / Docker Compose