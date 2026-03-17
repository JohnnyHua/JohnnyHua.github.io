---
layout: post
title: aibrain
date: 2026-03-17
tags: [python, discord, ai, personal-tool]
status: paused
github: https://github.com/JohnnyHua/aibrain
---

## Goal

Personal AI memory assistant - collects data from my daily activities and helps me remember and retrieve information.

## Tech Stack

- **Backend**: Python, FastAPI, SQLAlchemy, SQLite
- **Frontend**: React, TypeScript, Vite
- **Bot**: Discord.py
- **AI**: OpenAI API, Claude API
- **Infrastructure**: Docker, Docker Compose

## Progress

- [x] Discord Bot with slash commands
- [x] Multi-source collectors (Git, Terminal, Claude, OpenCode, Codex)
- [x] Reminder scheduler with DM notifications
- [x] Dashboard backend API
- [ ] Dashboard frontend (in progress)
- [ ] AI-powered memory retrieval
- [ ] Natural language queries

## Why Paused

- Time constraints
- Pivoted to other projects
- Core functionality works for personal use

## Architecture

```
Collectors → SQLite → Dashboard
                ↓
           Discord Bot
                ↓
           Scheduler (Reminders)
```

## Key Decisions

### Why Discord Bot?
I'm already on Discord. Lower friction than a separate app.

### Why SQLite?
Simpler for personal tool. Can migrate to PostgreSQL if needed.

### Why Multiple Collectors?
Different sources have different formats. Separate collectors allow independent parsing logic.

## Lessons Learned

1. **Start with one collector** - I built multiple collectors too early, should have validated with one first
2. **Discord Bot is great for personal tools** - Instant notifications, already integrated in daily life
3. **SQLite is enough** - Don't over-engineer for scale you don't need

## Related Problems

- P001: NLP intent parsing for reminders
- P002: Deduplication of collected events

## Future

Would continue if:
- I need more sophisticated memory retrieval
- I want to share with others (would need multi-tenancy)