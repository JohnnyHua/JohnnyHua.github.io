---
layout: default
title: Solutions
---

<h1 data-lang="en">Solutions</h1>
<h1 data-lang="zh" style="display: none;">解决方案</h1>

<div data-lang="en">How I solved specific problems.</div>
<div data-lang="zh" style="display: none;">我如何解决特定问题。</div>

---

## S001: <span data-lang="en">Context Handoff Across Platforms</span><span data-lang="zh" style="display: none;">跨平台上下文交接</span>

<div data-lang="en">
**Problem**: [P004](/problems/) — When AI tool quota runs out, switching platforms loses context.
</div>
<div data-lang="zh" style="display: none;">
**问题**: [P004](/problems/) — AI 工具配额用完时，切换平台会丢失上下文。
</div>

### <span data-lang="en">The Problem</span><span data-lang="zh" style="display: none;">问题是什么</span>

<div data-lang="en">
I use multiple AI tools (Codex, Claude Code, OpenCode, GLM-5). When one runs out of quota, I switch to another. But the new platform doesn't know:
- What project I'm working on
- What decisions were made
- What's the current state
- What's blocked

This means re-explaining everything from scratch.
</div>
<div data-lang="zh" style="display: none;">
我使用多个 AI 工具（Codex、Claude Code、OpenCode、GLM-5）。当一个配额用完，我切换到另一个。但新平台不知道：
- 我在做什么项目
- 做了什么决策
- 当前状态是什么
- 什么卡住了

这意味着要从头重新解释一切。
</div>

### <span data-lang="en">Solution</span><span data-lang="zh" style="display: none;">解决方案</span>

<div data-lang="en">
**Two tools I built**:
</div>
<div data-lang="zh" style="display: none;">
**我构建了两个工具**：
</div>

#### 1. automem — <span data-lang="en">Memory Storage</span><span data-lang="zh" style="display: none;">记忆存储</span>

<div data-lang="en">
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
</div>
<div data-lang="zh" style="display: none;">
跨会话存储重要上下文：
- 做过的决策
- 发现的模式
- 用户偏好
- Bug 修复和根因

```python
# 示例用法
store_memory({
    "content": "aibrain 选了 SQLite 而不是 PostgreSQL。个人项目，不需要扩展。",
    "tags": ["architecture", "aibrain"],
    "importance": 0.8
})
```
</div>

#### 2. handoff — <span data-lang="en">Context Transfer</span><span data-lang="zh" style="display: none;">上下文转移</span>

<div data-lang="en">
Generates a structured handoff document:
- Current task status
- Key files
- Decisions made
- Blockers
- Next steps

This can be passed to a new AI session.
</div>
<div data-lang="zh" style="display: none;">
生成结构化的交接文档：
- 当前任务状态
- 关键文件
- 已做决策
- 阻塞问题
- 下一步

可以传递给新的 AI 会话。
</div>

### <span data-lang="en">Trade-offs</span><span data-lang="zh" style="display: none;">权衡</span>

<div data-lang="en">
- **Time cost**: Takes 2-5 minutes to create proper handoff
- **Discipline required**: Must do it before quota runs out
- **Format learning**: AI needs to understand the handoff format
</div>
<div data-lang="zh" style="display: none;">
- **时间成本**: 创建合适的交接需要 2-5 分钟
- **需要自律**: 必须在配额用完前做
- **格式学习**: AI 需要理解交接格式
</div>

### <span data-lang="en">Lessons Learned</span><span data-lang="zh" style="display: none;">经验教训</span>

<div data-lang="en">
1. **Don't wait until quota runs out** — Create handoff when you feel you're at a good stopping point
2. **Keep it minimal** — Only transfer what's essential
3. **Test handoff** — Verify the receiving AI understands the context
</div>
<div data-lang="zh" style="display: none;">
1. **不要等到配额用完** — 在一个好的停止点就创建交接
2. **保持最小** — 只转移必要的
3. **测试交接** — 验证接收的 AI 理解上下文
</div>

---

## S002: <span data-lang="en">AI Cost Control — GLM-5 Fallback</span><span data-lang="zh" style="display: none;">AI 成本控制 — GLM-5 备用</span>

<div data-lang="en">
**Problem**: [P002](/problems/) — Subscription quotas run out, can't afford unlimited premium models.
</div>
<div data-lang="zh" style="display: none;">
**问题**: [P002](/problems/) — 订阅配额用完，用不起无限量的高级模型。
</div>

### <span data-lang="en">Solution</span><span data-lang="zh" style="display: none;">解决方案</span>

<div data-lang="en">
**Primary**: Codex / Claude Opus (best quality)
**Fallback**: GLM-5 via Ali Bailian premium subscription

**Why GLM-5**:
- Close to Codex/Opus in quality
- Unlimited usage with premium subscription
- Good enough for most tasks
</div>
<div data-lang="zh" style="display: none;">
**主力**: Codex / Claude Opus（质量最好）
**备用**: GLM-5（阿里百炼高级订阅）

**为什么选 GLM-5**：
- 质量接近 Codex/Opus
- 高级订阅无限量使用
- 对大多数任务够用
</div>

### <span data-lang="en">Decision Tree</span><span data-lang="zh" style="display: none;">决策树</span>

```
<span data-lang="en">Task complexity?</span><span data-lang="zh" style="display: none;">任务复杂度？</span>
├─ <span data-lang="en">High → Codex/Opus (if quota available)</span><span data-lang="zh" style="display: none;">高 → Codex/Opus（如果配额够）</span>
│         └─ <span data-lang="en">No quota? → GLM-5</span><span data-lang="zh" style="display: none;">没配额？ → GLM-5</span>
└─ <span data-lang="en">Low/Medium → GLM-5 directly</span><span data-lang="zh" style="display: none;">低/中 → 直接用 GLM-5</span>
```

### <span data-lang="en">Trade-offs</span><span data-lang="zh" style="display: none;">权衡</span>

<div data-lang="en">
- GLM-5 slightly worse at complex reasoning
- Sometimes needs more prompts to get same result
- But: unlimited, predictable cost
</div>
<div data-lang="zh" style="display: none;">
- GLM-5 复杂推理稍弱
- 有时需要更多 prompt 才能得到相同结果
- 但：无限量，成本可预测
</div>

---

## <span data-lang="en">Template for New Solutions</span><span data-lang="zh" style="display: none;">新方案模板</span>

<div data-lang="en">
When adding a new solution:

1. **Problem**: Link to the problem page
2. **What I tried**: List attempts
3. **What worked**: The actual solution
4. **Trade-offs**: What I gave up
5. **Lessons learned**: For future reference
</div>
<div data-lang="zh" style="display: none;">
添加新解决方案时：

1. **问题**: 链接到问题页面
2. **尝试了什么**: 列出尝试
3. **什么有效**: 实际解决方案
4. **权衡**: 放弃了什么
5. **经验教训**: 供未来参考
</div>