---
layout: default
title: Problems
---

<h1 data-lang="en">Problems & Pain Points</h1>
<h1 data-lang="zh" style="display: none;">问题与痛点</h1>

<div data-lang="en">Ongoing list of challenges I've encountered. Some solved, some not.</div>
<div data-lang="zh" style="display: none;">持续更新的挑战清单。有些解决了，有些没有。</div>

---

## <span data-lang="en">Status Legend</span><span data-lang="zh" style="display: none;">状态说明</span>

<div data-lang="en">
- 🟡 **Pending** — Not started
- 🔵 **In Progress** — Working on it
- 🟢 **Solved** — Has solution
- 🔴 **Paused** — Deprioritized
</div>
<div data-lang="zh" style="display: none;">
- 🟡 **待解决** — 还没开始
- 🔵 **进行中** — 正在处理
- 🟢 **已解决** — 有解决方案
- 🔴 **暂停** — 优先级降低
</div>

---

## <span data-lang="en">Architecture & Design</span><span data-lang="zh" style="display: none;">架构与设计</span>

### P001: <span data-lang="en">Self-Reference Problem</span><span data-lang="zh" style="display: none;">自指问题</span>

<div data-lang="en">
**Status**: 🟡 Pending

**Context**: When developing PCP (a protocol layer), I sometimes accidentally use the architecture I'm building while I'm building it.

**Impact**: Creates circular dependencies, hard to test, confusing.

**Attempts**: None yet.

**Related**: PCP project
</div>
<div data-lang="zh" style="display: none;">
**状态**: 🟡 待解决

**背景**: 开发 PCP（协议层）时，有时会不小心在自己构建的架构中使用自己正在构建的架构。

**影响**: 造成循环依赖，难以测试，令人困惑。

**尝试**: 暂无。

**相关**: PCP 项目
</div>

---

## <span data-lang="en">Cost Management</span><span data-lang="zh" style="display: none;">成本管理</span>

### P002: <span data-lang="en">AI Cost Control for Solo Developers</span><span data-lang="zh" style="display: none;">个人开发者的 AI 成本控制</span>

<div data-lang="en">
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
</div>
<div data-lang="zh" style="display: none;">
**状态**: 🔵 进行中

**背景**: 作为个人开发者，保持低成本很关键。能不花钱就不花钱。

**痛点**：
- 订阅配额用完
- 需要备用方案
- 不能总用最好的模型

**当前方案**：
- GLM-5 作为无限量备用
- 配额用完切换平台

**权衡**: 质量 vs 成本

**相关**: [开发流程](/workflow/)
</div>

---

## <span data-lang="en">Workflow & Process</span><span data-lang="zh" style="display: none;">流程与工作流</span>

### P003: <span data-lang="en">Git Workflow for Solo Developers</span><span data-lang="zh" style="display: none;">个人开发者的 Git 工作流</span>

<div data-lang="en">
**Status**: 🟡 Pending

**Context**: I don't use Git well. No habits formed. Since I'm the only developer, I don't care much.

**Pain point**:
- Don't know proper Git workflow
- No branching strategy
- Commit messages are messy
- No code review

**Impact**: Hard to track changes, hard to revert, hard to collaborate if needed

**Attempts**: None yet.
</div>
<div data-lang="zh" style="display: none;">
**状态**: 🟡 待解决

**背景**: 我 Git 用得不好。没有形成习惯。因为只有我一个人开发，所以不太在意。

**痛点**：
- 不知道正确的 Git 工作流
- 没有分支策略
- 提交信息混乱
- 没有代码审查

**影响**: 难以追踪变更，难以回滚，需要协作时困难

**尝试**: 暂无。
</div>

---

### P004: <span data-lang="en">Context Handoff Across Platforms</span><span data-lang="zh" style="display: none;">跨平台上下文交接</span>

<div data-lang="en">
**Status**: 🟢 Solved

**Context**: When AI tool quota runs out, I need to switch platforms. But the new platform doesn't know my project context.

**Solution**: 
- **automem**: Memory storage across sessions
- **handoff**: Context transfer protocol

**Trade-off**: Takes time to setup handoff

**Related**: aibrain, PCP
</div>
<div data-lang="zh" style="display: none;">
**状态**: 🟢 已解决

**背景**: AI 工具配额用完时，需要切换平台。但新平台不知道我的项目上下文。

**解决方案**：
- **automem**: 跨会话记忆存储
- **handoff**: 上下文转移协议

**权衡**: 设置交接需要时间

**相关**: aibrain, PCP
</div>

---

## <span data-lang="en">Technical Issues</span><span data-lang="zh" style="display: none;">技术问题</span>

### P005: <span data-lang="en">Mermaid Font Rendering</span><span data-lang="zh" style="display: none;">Mermaid 字体渲染</span>

<div data-lang="en">
**Status**: 🔵 In Progress

**Context**: When AI generates Mermaid diagrams and converts to images, the fonts look weird.

**Problem**: Default fonts don't support Chinese well, or look ugly.

**Current approach**: Download fonts manually.

**Not yet automated**.
</div>
<div data-lang="zh" style="display: none;">
**状态**: 🔵 进行中

**背景**: AI 生成 Mermaid 图并转换为图片时，字体看起来很怪。

**问题**: 默认字体对中文支持不好，或者看起来很丑。

**当前方案**: 手动下载字体。

**尚未自动化**。
</div>

---

## <span data-lang="en">Summary</span><span data-lang="zh" style="display: none;">总览</span>

<div data-lang="en">
| # | Problem | Status | Solution |
|---|---------|--------|----------|
| P001 | Self-reference in architecture design | 🟡 Pending | - |
| P002 | AI cost control for solo devs | 🔵 In Progress | GLM-5 fallback |
| P003 | Git workflow for solo devs | 🟡 Pending | - |
| P004 | Context handoff across platforms | 🟢 Solved | automem, handoff |
| P005 | Mermaid font rendering | 🔵 In Progress | Manual fonts |
</div>
<div data-lang="zh" style="display: none;">
| # | 问题 | 状态 | 解决方案 |
|---|------|------|----------|
| P001 | 架构设计的自指问题 | 🟡 待解决 | - |
| P002 | 个人开发者的 AI 成本控制 | 🔵 进行中 | GLM-5 备用 |
| P003 | 个人开发者的 Git 工作流 | 🟡 待解决 | - |
| P004 | 跨平台上下文交接 | 🟢 已解决 | automem, handoff |
| P005 | Mermaid 字体渲染 | 🔵 进行中 | 手动字体 |
</div>

---

> <span data-lang="en">This list is continuously updated as I encounter new problems.</span><span data-lang="zh" style="display: none;">这个列表会随着我遇到新问题持续更新。</span>