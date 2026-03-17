---
layout: default
title: Development Workflow
---

<h1 data-lang="en">Development Workflow</h1>
<h1 data-lang="zh" style="display: none;">开发流程</h1>

<div data-lang="en">How I work with AI tools day-to-day.</div>
<div data-lang="zh" style="display: none;">我如何日常使用 AI 工具工作。</div>

---

## <span data-lang="en">My AI Tool Stack</span><span data-lang="zh" style="display: none;">AI 工具栈</span>

<div data-lang="en">
| Tool | Primary Use | Why |
|------|-------------|-----|
| **Cursor** | Company projects | Subscription, integrated IDE |
| **Codex** | Daily projects | Strong code generation, structured |
| **Claude Code** | Daily projects | Good reasoning, complements Codex |
| **OpenCode** | Flexible model selection | More freedom, larger quota |
| **GLM-5** (via Ali Bailian) | High-volume tasks | Premium subscription, cost-effective |
| **ChatGPT** | Pre-development planning | Voice input saves typing time |
</div>
<div data-lang="zh" style="display: none;">
| 工具 | 主要用途 | 原因 |
|------|----------|------|
| **Cursor** | 公司项目 | 订阅，集成 IDE |
| **Codex** | 日常项目 | 代码生成强，规范 |
| **Claude Code** | 日常项目 | 推理好，与 Codex 互补 |
| **OpenCode** | 灵活选模型 | 更自由，配额大 |
| **GLM-5** (阿里百炼) | 高用量任务 | 高级订阅，性价比高 |
| **ChatGPT** | 开发前规划 | 语音输入节省打字时间 |
</div>

---

## <span data-lang="en">Model Selection Logic</span><span data-lang="zh" style="display: none;">模型选择逻辑</span>

<div data-lang="en">
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
</div>
<div data-lang="zh" style="display: none;">
**问题**：订阅计划有用量限制。我同时跑 3-4 个项目，经常触达配额。

**解决方案**：

```
Codex/Opus（质量最好）
      ↓ 配额用完？
GLM-5（仅次于前者，无限量）
      ↓ 需要特定 API？
OpenAI API（用于 embedding 等特定任务）
```

GLM-5 是质量上最接近 Codex/Opus 的模型。订阅用完后，它成为我的主力。
</div>

---

## <span data-lang="en">Development Flow</span><span data-lang="zh" style="display: none;">开发流程</span>

### <span data-lang="en">Phase 1: Pre-Development (ChatGPT)</span><span data-lang="zh" style="display: none;">阶段一：开发前（ChatGPT）</span>

<div data-lang="en">
**Before writing any code, I talk to ChatGPT.**

Using voice input (saves typing time), I discuss:
- Project architecture
- Competitor analysis
- Task breakdown
- Development standards
- Process design

This phase clarifies direction before diving into implementation.
</div>
<div data-lang="zh" style="display: none;">
**写代码之前，先和 ChatGPT 聊。**

用语音输入（节省打字时间），讨论：
- 项目架构
- 竞品分析
- 任务拆解
- 开发规范
- 流程设计

这个阶段在动手之前理清方向。
</div>

### <span data-lang="en">Phase 2: Development (Codex/Claude/GLM)</span><span data-lang="zh" style="display: none;">阶段二：开发中（Codex/Claude/GLM）</span>

<div data-lang="en">
**AI controls the entire coding process.**

- Continue tasks iteratively
- AI writes code, I review
- Keep context in one session per project
- One directory = one conversation (no parallel mixing)

**When stuck**:
1. Handoff context to ChatGPT
2. Talk through the problem
3. Return to coding session with clarity
</div>
<div data-lang="zh" style="display: none;">
**AI 全程控制编码过程。**

- 迭代式继续任务
- AI 写代码，我 review
- 每个项目一个会话保持上下文
- 一个目录 = 一个对话（不并行混合）

**卡住时**：
1. 把上下文交给 ChatGPT
2. 聊通问题
3. 带着清晰思路回到编码会话
</div>

### <span data-lang="en">Phase 3: Review</span><span data-lang="zh" style="display: none;">阶段三：Review</span>

<div data-lang="en">
**What I check**:
- Logic correctness (primary focus)
- Sometimes request visual verification
- API testing
- Application-level validation

**When issues found**:
1. Clarify the logic first
2. Ask AI to rewrite (not fix blindly)
</div>
<div data-lang="zh" style="display: none;">
**检查什么**：
- 逻辑正确性（主要关注）
- 有时要求可视化验证
- API 测试
- 应用级别验证

**发现问题**：
1. 先理清逻辑
2. 让 AI 重写（不是盲目修复）
</div>

---

## <span data-lang="en">Managing Multiple Projects</span><span data-lang="zh" style="display: none;">多项目管理</span>

<div data-lang="en">
**Challenge**: 3-4 projects running in parallel.

**How I avoid context mixing**:
- One project directory = one AI session
- Never run multiple projects in the same conversation
- Switch projects = switch context completely

**Managing ideas**:
- Create a folder when an idea emerges
- Start prototyping immediately
- Ideas that stay are the ones worth building
</div>
<div data-lang="zh" style="display: none;">
**挑战**：同时跑 3-4 个项目。

**如何避免上下文混淆**：
- 一个项目目录 = 一个 AI 会话
- 从不在同一个对话里跑多个项目
- 切项目 = 完全切换上下文

**想法管理**：
- 有想法时创建文件夹
- 立即开始原型
- 能留下来的想法才值得做
</div>

---

## <span data-lang="en">Key Learnings</span><span data-lang="zh" style="display: none;">关键经验</span>

<div data-lang="en">
1. **Voice input is underrated** — ChatGPT voice saves 80% of typing time during planning
2. **Quota management matters** — Having a fallback model (GLM-5) prevents workflow interruption
3. **One session per project** — Prevents AI from confusing contexts
4. **Clarify before rewrite** — Fixing logic > fixing code
5. **AI controls, human reviews** — I don't write code anymore, I review it
</div>
<div data-lang="zh" style="display: none;">
1. **语音输入被低估了** — ChatGPT 语音在规划阶段节省 80% 打字时间
2. **配额管理很重要** — 有备用模型（GLM-5）防止工作流中断
3. **一个会话一个项目** — 避免 AI 混淆上下文
4. **先理清再重写** — 修复逻辑 > 修复代码
5. **AI 控制，人审核** — 我不再写代码了，我只审核代码
</div>