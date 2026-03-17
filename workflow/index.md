---
layout: default
title: Development Workflow
---

# Development Workflow

How I work with AI tools day-to-day.

---

## My AI Tool Stack

| Tool | Primary Use | Why |
|------|-------------|-----|
| **Cursor** | Company projects | Subscription, integrated IDE |
| **Codex** | Daily projects | Strong code generation, structured |
| **Claude Code** | Daily projects | Good reasoning, complements Codex |
| **OpenCode** | Flexible model selection | More freedom, larger quota |
| **GLM-5** (via Ali Bailian) | High-volume tasks | Premium subscription, cost-effective |
| **ChatGPT** | Pre-development planning | Voice input saves typing time |

---

## Model Selection Logic

**Problem**: Subscription plans have usage limits. As I run 3-4 projects in parallel, I often hit quotas.

**Solution**:

```
Codex/Opus (best quality)
      ↓ quota exhausted?
GLM-5 (close second, unlimited)
      ↓ need specific API?
OpenAI API (for embeddings, specific tasks)
```

GLM-5 is the closest to Codex/Opus in quality. When subscriptions run out, it becomes my daily driver.

---

## Development Flow

### Phase 1: Pre-Development (ChatGPT)

**Before writing any code, I talk to ChatGPT.**

Using voice input (saves typing time), I discuss:
- Project architecture
- Competitor analysis
- Task breakdown
- Development standards
- Process design

This phase clarifies direction before diving into implementation.

### Phase 2: Development (Codex/Claude/GLM)

**AI controls the entire coding process.**

- Continue tasks iteratively
- AI writes code, I review
- Keep context in one session per project
- One directory = one conversation (no parallel mixing)

**When stuck**:
1. Handoff context to ChatGPT
2. Talk through the problem
3. Return to coding session with clarity

### Phase 3: Review

**What I check**:
- Logic correctness (primary focus)
- Sometimes request visual verification
- API testing
- Application-level validation

**When issues found**:
1. Clarify the logic first
2. Ask AI to rewrite (not fix blindly)

---

## Managing Multiple Projects

**Challenge**: 3-4 projects running in parallel.

**How I avoid context mixing**:
- One project directory = one AI session
- Never run multiple projects in the same conversation
- Switch projects = switch context completely

**Managing ideas**:
- Create a folder when an idea emerges
- Start prototyping immediately
- Ideas that stay are the ones worth building

---

## Key Learnings

1. **Voice input is underrated** — ChatGPT voice saves 80% of typing time during planning
2. **Quota management matters** — Having a fallback model (GLM-5) prevents workflow interruption
3. **One session per project** — Prevents AI from confusing contexts
4. **Clarify before rewrite** — Fixing logic > fixing code
5. **AI controls, human reviews** — I don't write code anymore, I review it