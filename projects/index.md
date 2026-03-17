---
layout: default
title: Projects
---

# Projects

Personal projects I've worked on. Some complete, some paused, some evolved into something else.

---

## Status Legend

- 🔵 **In Progress** — Actively developing
- ⏸️ **Paused** — Temporarily stopped
- ❌ **Abandoned** — Decided not to continue
- 🔄 **Evolved** — Became another project

---

## Active Projects

### PCP (Progress Control Plane)

**Status**: 🔵 In Progress

Protocol layer and state kernel for AI agent collaboration.

**Problem it solves**:
- AI sessions drift from scope
- Work interrupted cannot resume
- Completion claimed without evidence
- Multi-session development lacks state

**Core value**:
- Single source of truth for task state
- Evidence-first completion rules
- Tool-agnostic protocol

**Location**: `/clawd/pcp/`

---

### aibrain

**Status**: ⏸️ Paused (core features work for personal use)

Personal AI memory assistant — todolist, knowledge base, daily reminders.

**Tech**: Python, FastAPI, React, Discord Bot, SQLite

**Why paused**: Time constraints, pivoted to other projects

**[Details →](aibrain.html)** | **[中文版 →](aibrain-zh.html)**

---

## Paused / Abandoned Projects

### MoneyPrinterTurbo

**Status**: ❌ Abandoned

AI-powered video generation: topic → script → footage → subtitle → music → final video.

**Why abandoned**: Video generation cost too high for personal use. Great project, but not sustainable for me.

**Tech**: Python, Docker, FFmpeg, ImageMagick, multiple LLM providers

---

### xhs_posts

**Status**: ⏸️ Paused

Xiaohongshu (Little Red Book) post management and analysis.

**Sub-projects**:
- intro
- fenjue (分掘)
- jobbi
- UsingAI

---

### 记账 (Accounting)

**Status**: ⏸️ Paused

Personal accounting tool.

**Tech**: Python

---

### agents-projet

**Status**: 🔄 Evolved into PCP

LangChain-based CLI agent that interviews users to collect project requirements.

**What I learned**: This became part of my thinking about AI agent collaboration patterns.

---

## PCP Evolution History

PCP didn't appear out of nowhere. It evolved through several iterations:

| Phase | Project | What happened |
|-------|---------|---------------|
| v0.1 | AI_Progress_Control_Plane | Initial design documents |
| v0.2 | DevOPS / study_openclaw | Explored AI workspaces |
| v0.3 | PCP_OpenCode_Plugin_Plan | Focused on OpenCode integration |
| Current | PCP | Protocol layer, tool-agnostic |

**Design documents**:
- AI_Agent_Cluster_项目说明_对外版本.pdf
- AI_RD_OS_v1_自托管智能体研发组织操作系统_v1.pdf

---

## Why Track Paused Projects?

Because they still have value:
- Document what was learned
- Explain why it stopped
- Help future decisions
- Maybe someone else can continue