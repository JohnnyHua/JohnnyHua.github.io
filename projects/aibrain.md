---
layout: post
title: aibrain
date: 2026-03-17
tags: [python, discord, ai, personal-tool]
status: paused
github: https://github.com/JohnnyHua/aibrain
---

## <span data-lang="en">Goal</span><span data-lang="zh" style="display: none;">目标</span>

<div data-lang="en">Personal AI memory assistant - collects data from my daily activities and helps me remember and retrieve information.</div>
<div data-lang="zh" style="display: none;">个人AI记忆助手 - 收集日常活动数据，帮助记忆和检索信息。</div>

## <span data-lang="en">Tech Stack</span><span data-lang="zh" style="display: none;">技术栈</span>

<div data-lang="en">
- **Backend**: Python, FastAPI, SQLAlchemy, SQLite
- **Frontend**: React, TypeScript, Vite
- **Bot**: Discord.py
- **AI**: OpenAI API, Claude API
- **Infrastructure**: Docker, Docker Compose
</div>
<div data-lang="zh" style="display: none;">
- **后端**: Python, FastAPI, SQLAlchemy, SQLite
- **前端**: React, TypeScript, Vite
- **机器人**: Discord.py
- **AI**: OpenAI API, Claude API
- **基础设施**: Docker, Docker Compose
</div>

## <span data-lang="en">Progress</span><span data-lang="zh" style="display: none;">进度</span>

<div data-lang="en">
- [x] Discord Bot with slash commands
- [x] Multi-source collectors (Git, Terminal, Claude, OpenCode, Codex)
- [x] Reminder scheduler with DM notifications
- [x] Dashboard backend API
- [ ] Dashboard frontend (in progress)
- [ ] AI-powered memory retrieval
- [ ] Natural language queries
</div>
<div data-lang="zh" style="display: none;">
- [x] Discord Bot（带斜杠命令）
- [x] 多数据源收集器（Git、Terminal、Claude、OpenCode、Codex）
- [x] 提醒调度器（DM通知）
- [x] Dashboard 后端 API
- [ ] Dashboard 前端（进行中）
- [ ] AI 驱动的记忆检索
- [ ] 自然语言查询
</div>

## <span data-lang="en">Why Paused</span><span data-lang="zh" style="display: none;">为什么暂停</span>

<div data-lang="en">
- Time constraints
- Pivoted to other projects
- Core functionality works for personal use
</div>
<div data-lang="zh" style="display: none;">
- 时间限制
- 转向其他项目
- 核心功能已满足个人使用需求
</div>

## <span data-lang="en">Architecture</span><span data-lang="zh" style="display: none;">架构</span>

```
<span data-lang="en">Collectors → SQLite → Dashboard</span><span data-lang="zh" style="display: none;">收集器 → SQLite → Dashboard</span>
                 ↓
            Discord Bot
                 ↓
            <span data-lang="en">Scheduler (Reminders)</span><span data-lang="zh" style="display: none;">调度器（提醒）</span>
```

## <span data-lang="en">Key Decisions</span><span data-lang="zh" style="display: none;">关键决策</span>

### <span data-lang="en">Why Discord Bot?</span><span data-lang="zh" style="display: none;">为什么选 Discord Bot？</span>

<div data-lang="en">I'm already on Discord. Lower friction than a separate app.</div>
<div data-lang="zh" style="display: none;">我本来就常用 Discord。比单独的 App 更方便。</div>

### <span data-lang="en">Why SQLite?</span><span data-lang="zh" style="display: none;">为什么选 SQLite？</span>

<div data-lang="en">Simpler for personal tool. Can migrate to PostgreSQL if needed.</div>
<div data-lang="zh" style="display: none;">个人工具用这个够简单。需要时可以迁移到 PostgreSQL。</div>

### <span data-lang="en">Why Multiple Collectors?</span><span data-lang="zh" style="display: none;">为什么多个收集器？</span>

<div data-lang="en">Different sources have different formats. Separate collectors allow independent parsing logic.</div>
<div data-lang="zh" style="display: none;">不同数据源格式不同。分离收集器让解析逻辑独立。</div>

## <span data-lang="en">Lessons Learned</span><span data-lang="zh" style="display: none;">经验教训</span>

<div data-lang="en">
1. **Start with one collector** - I built multiple collectors too early, should have validated with one first
2. **Discord Bot is great for personal tools** - Instant notifications, already integrated in daily life
3. **SQLite is enough** - Don't over-engineer for scale you don't need
</div>
<div data-lang="zh" style="display: none;">
1. **先从一个收集器开始** - 我太早做了多个，应该先用一个验证
2. **Discord Bot 适合个人工具** - 即时通知，已融入日常生活
3. **SQLite 够用** - 不要为你不需要的规模过度设计
</div>

## <span data-lang="en">Related Problems</span><span data-lang="zh" style="display: none;">相关问题</span>

- P001: <span data-lang="en">NLP intent parsing for reminders</span><span data-lang="zh" style="display: none;">提醒的 NLP 意图解析</span>
- P002: <span data-lang="en">Deduplication of collected events</span><span data-lang="zh" style="display: none;">收集事件的去重</span>

## <span data-lang="en">Future</span><span data-lang="zh" style="display: none;">未来计划</span>

<div data-lang="en">
Would continue if:
- I need more sophisticated memory retrieval
- I want to share with others (would need multi-tenancy)
</div>
<div data-lang="zh" style="display: none;">
以下情况会继续：
- 需要更复杂的记忆检索
- 想分享给他人使用（需要多租户支持）
</div>