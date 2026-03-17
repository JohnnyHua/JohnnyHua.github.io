---
layout: post
title: aibrain
date: 2026-03-17
tags: [python, discord, ai, personal-tool]
status: paused
github: https://github.com/JohnnyHua/aibrain
---

## 目标

个人AI记忆助手 - 收集日常活动数据，帮助记忆和检索信息。

## 技术栈

- **后端**: Python, FastAPI, SQLAlchemy, SQLite
- **前端**: React, TypeScript, Vite
- **机器人**: Discord.py
- **AI**: OpenAI API, Claude API
- **基础设施**: Docker, Docker Compose

## 进度

- [x] Discord Bot（带斜杠命令）
- [x] 多数据源收集器（Git、Terminal、Claude、OpenCode、Codex）
- [x] 提醒调度器（DM通知）
- [x] Dashboard 后端 API
- [ ] Dashboard 前端（进行中）
- [ ] AI 驱动的记忆检索
- [ ] 自然语言查询

## 为什么暂停

- 时间限制
- 转向其他项目
- 核心功能已满足个人使用需求

## 架构

```
收集器 → SQLite → Dashboard
              ↓
         Discord Bot
              ↓
         调度器（提醒）
```

## 关键决策

### 为什么选 Discord Bot？
我本来就常用 Discord。比单独的 App 更方便。

### 为什么选 SQLite？
个人工具用这个够简单。需要时可以迁移到 PostgreSQL。

### 为什么多个收集器？
不同数据源格式不同。分离收集器让解析逻辑独立。

## 经验教训

1. **先从一个收集器开始** - 我太早做了多个，应该先用一个验证
2. **Discord Bot 适合个人工具** - 即时通知，已融入日常生活
3. **SQLite 够用** - 不要为你不需要的规模过度设计

## 相关问题

- P001: 提醒的 NLP 意图解析
- P002: 收集事件的去重

## 未来计划

以下情况会继续：
- 需要更复杂的记忆检索
- 想分享给他人使用（需要多租户支持）