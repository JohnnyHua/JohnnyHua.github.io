---
layout: default
title: Solutions
---

# Solutions

How I solved specific problems.

---

## S001: Context Handoff Across Platforms

**Problem**: [P004](/problems/) — When AI tool quota runs out, switching platforms loses context.

### The Problem

I use multiple AI tools (Codex, Claude Code, OpenCode, GLM-5). When one runs out of quota, I switch to another. But the new platform doesn't know:
- What project I'm working on
- What decisions were made
- What's the current state
- What's blocked

This means re-explaining everything from scratch.

### Solution

**Two tools I built**:

#### 1. automem — Memory Storage

Stores important context across sessions:
- Decisions made
- Patterns discovered
- User preferences
- Bug fixes and root causes

```python
# Example usage
store_memory({
    "content": "Chose SQLite over PostgreSQL for aibrain. Solo project, no scaling needed.",
    "tags": ["architecture", "aibrain"],
    "importance": 0.8
})
```

#### 2. handoff — Context Transfer

Generates a structured handoff document:
- Current task status
- Key files
- Decisions made
- Blockers
- Next steps

This can be passed to a new AI session.

### Trade-offs

- **Time cost**: Takes 2-5 minutes to create proper handoff
- **Discipline required**: Must do it before quota runs out
- **Format learning**: AI needs to understand the handoff format

### Lessons Learned

1. **Don't wait until quota runs out** — Create handoff when you feel you're at a good stopping point
2. **Keep it minimal** — Only transfer what's essential
3. **Test handoff** — Verify the receiving AI understands the context

---

## S002: AI Cost Control — GLM-5 Fallback

**Problem**: [P002](/problems/) — Subscription quotas run out, can't afford unlimited premium models.

### Solution

**Primary**: Codex / Claude Opus (best quality)
**Fallback**: GLM-5 via Ali Bailian premium subscription

**Why GLM-5**:
- Close to Codex/Opus in quality
- Unlimited usage with premium subscription
- Good enough for most tasks

### Decision Tree

```
Task complexity?
├─ High → Codex/Opus (if quota available)
│         └─ No quota? → GLM-5
└─ Low/Medium → GLM-5 directly
```

### Trade-offs

- GLM-5 slightly worse at complex reasoning
- Sometimes needs more prompts to get same result
- But: unlimited, predictable cost

---

## Template for New Solutions

When adding a new solution:

1. **Problem**: Link to the problem page
2. **What I tried**: List attempts
3. **What worked**: The actual solution
4. **Trade-offs**: What I gave up
5. **Lessons learned**: For future reference