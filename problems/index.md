---
layout: default
title: Problems
---

# Problems & Pain Points

Ongoing list of challenges I've encountered. Some solved, some not.

---

## Status Legend

- 🟡 **Pending** — Not started
- 🔵 **In Progress** — Working on it
- 🟢 **Solved** — Has solution
- 🔴 **Paused** — Deprioritized

---

## Architecture & Design

### P001: Self-Reference Problem

**Status**: 🟡 Pending

**Context**: When developing PCP (a protocol layer), I sometimes accidentally use the architecture I'm building while I'm building it.

**Impact**: Creates circular dependencies, hard to test, confusing.

**Attempts**: None yet.

**Related**: PCP project

---

## Cost Management

### P002: AI Cost Control for Solo Developers

**Status**: 🔵 In Progress

**Context**: As a solo developer, keeping costs low is critical. I try to avoid spending money whenever possible.

**Pain point**: 
- Subscription quotas run out
- Need fallback options
- Can't always use the best model

**Current approach**: 
- GLM-5 as unlimited fallback
- Switch platforms when quota exhausted

**Trade-off**: Quality vs cost

**Related**: [Workflow](/workflow/)

---

## Workflow & Process

### P003: Git Workflow for Solo Developers

**Status**: 🟡 Pending

**Context**: I don't use Git well. No habits formed. Since I'm the only developer, I don't care much.

**Pain point**:
- Don't know proper Git workflow
- No branching strategy
- Commit messages are messy
- No code review

**Impact**: Hard to track changes, hard to revert, hard to collaborate if needed

**Attempts**: None yet.

---

### P004: Context Handoff Across Platforms

**Status**: 🟢 Solved

**Context**: When AI tool quota runs out, I need to switch platforms. But the new platform doesn't know my project context.

**Solution**: 
- **automem**: Memory storage across sessions
- **handoff**: Context transfer protocol

**Trade-off**: Takes time to setup handoff

**Related**: aibrain, PCP

---

## Technical Issues

### P005: Mermaid Font Rendering

**Status**: 🔵 In Progress

**Context**: When AI generates Mermaid diagrams and converts to images, the fonts look weird.

**Problem**: Default fonts don't support Chinese well, or look ugly.

**Current approach**: Download fonts manually.

**Not yet automated**.

---

## Summary

| # | Problem | Status | Solution |
|---|---------|--------|----------|
| P001 | Self-reference in architecture design | 🟡 Pending | - |
| P002 | AI cost control for solo devs | 🔵 In Progress | GLM-5 fallback |
| P003 | Git workflow for solo devs | 🟡 Pending | - |
| P004 | Context handoff across platforms | 🟢 Solved | automem, handoff |
| P005 | Mermaid font rendering | 🔵 In Progress | Manual fonts |

---

> This list is continuously updated as I encounter new problems.