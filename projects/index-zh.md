---
layout: default
title: 项目
---

# 项目

我做过的个人项目。有些完成了，有些暂停了，有些演变成了别的。

---

## 状态说明

- 🔵 **进行中** — 正在开发
- ⏸️ **暂停** — 临时停止
- ❌ **放弃** — 决定不再继续
- 🔄 **演进** — 变成了其他项目

---

## 活跃项目

### PCP (Progress Control Plane)

**状态**: 🔵 进行中

AI Agent 协作的协议层和状态内核。

**解决的问题**：
- AI 会话偏离范围
- 工作中断无法恢复
- 没有证据就声称完成
- 多会话开发缺乏状态

**核心价值**：
- 任务状态的单一数据源
- 证据优先的完成规则
- 工具无关的协议

**位置**: `/clawd/pcp/`

---

### aibrain

**状态**: ⏸️ 暂停（核心功能个人可用）

个人 AI 记忆助手 — todolist、知识库、日常提醒。

**技术**: Python, FastAPI, React, Discord Bot, SQLite

**为什么暂停**: 时间限制，转向其他项目

**[详情 →](aibrain-zh.html)**

---

## 暂停 / 放弃的项目

### MoneyPrinterTurbo

**状态**: ❌ 放弃

AI 视频生成：主题 → 文案 → 素材 → 字幕 → 音乐 → 成片。

**为什么放弃**: 视频生成成本对个人使用来说太高。好项目，但我用不起。

**技术**: Python, Docker, FFmpeg, ImageMagick, 多种 LLM 服务

---

### xhs_posts

**状态**: ⏸️ 暂停

小红书帖子管理和分析。

**子项目**：
- intro
- fenjue (分掘)
- jobbi
- UsingAI

---

### 记账

**状态**: ⏸️ 暂停

个人记账工具。

**技术**: Python

---

### agents-projet

**状态**: 🔄 演进为 PCP

基于 LangChain 的 CLI Agent，通过访谈收集项目需求。

**学到的**: 这成为我对 AI Agent 协作模式思考的一部分。

---

## PCP 演进历史

PCP 不是凭空出现的，它经历了多次迭代：

| 阶段 | 项目 | 发生了什么 |
|------|------|-----------|
| v0.1 | AI_Progress_Control_Plane | 初始设计文档 |
| v0.2 | DevOPS / study_openclaw | 探索 AI 工作空间 |
| v0.3 | PCP_OpenCode_Plugin_Plan | 聚焦 OpenCode 集成 |
| 当前 | PCP | 协议层，工具无关 |

**设计文档**：
- AI_Agent_Cluster_项目说明_对外版本.pdf
- AI_RD_OS_v1_自托管智能体研发组织操作系统_v1.pdf

---

## 为什么要记录暂停的项目？

因为它们仍然有价值：
- 记录学到了什么
- 解释为什么停止
- 帮助未来决策
- 也许别人可以继续