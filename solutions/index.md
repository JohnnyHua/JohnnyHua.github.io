---
layout: default
title: Solutions
---

<h1 data-lang="en">Solutions</h1>
<h1 data-lang="zh" style="display: none;">解决方案</h1>

<p data-lang="en">How I solved specific problems.</p>
<p data-lang="zh" style="display: none;">我如何解决特定问题。</p>

<hr>

<h2>S001: <span data-lang="en">Context Handoff Across Platforms</span><span data-lang="zh" style="display: none;">跨平台上下文交接</span></h2>

<div data-lang="en">
<p><strong>Problem</strong>: <a href="/problems/">P004</a> — When AI tool quota runs out, switching platforms loses context.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>问题</strong>: <a href="/problems/">P004</a> — AI 工具配额用完时，切换平台会丢失上下文。</p>
</div>

<h3 data-lang="en">The Problem</h3>
<h3 data-lang="zh" style="display: none;">问题是什么</h3>

<div data-lang="en">
<p>I use multiple AI tools (Codex, Claude Code, OpenCode, GLM-5). When one runs out of quota, I switch to another. But the new platform doesn't know:</p>
<ul>
  <li>What project I'm working on</li>
  <li>What decisions were made</li>
  <li>What's the current state</li>
  <li>What's blocked</li>
</ul>
<p>This means re-explaining everything from scratch.</p>
</div>
<div data-lang="zh" style="display: none;">
<p>我使用多个 AI 工具（Codex、Claude Code、OpenCode、GLM-5）。当一个配额用完，我切换到另一个。但新平台不知道：</p>
<ul>
  <li>我在做什么项目</li>
  <li>做了什么决策</li>
  <li>当前状态是什么</li>
  <li>什么卡住了</li>
</ul>
<p>这意味着要从头重新解释一切。</p>
</div>

<h3 data-lang="en">Solution</h3>
<h3 data-lang="zh" style="display: none;">解决方案</h3>

<div data-lang="en">
<p><strong>Two tools I built</strong>:</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>我构建了两个工具</strong>：</p>
</div>

<h4>1. automem — <span data-lang="en">Memory Storage</span><span data-lang="zh" style="display: none;">记忆存储</span></h4>

<div data-lang="en">
<p>Stores important context across sessions:</p>
<ul>
  <li>Decisions made</li>
  <li>Patterns discovered</li>
  <li>User preferences</li>
  <li>Bug fixes and root causes</li>
</ul>
<pre><code># Example usage
store_memory({
    "content": "Chose SQLite over PostgreSQL for aibrain. Solo project, no scaling needed.",
    "tags": ["architecture", "aibrain"],
    "importance": 0.8
})</code></pre>
</div>
<div data-lang="zh" style="display: none;">
<p>跨会话存储重要上下文：</p>
<ul>
  <li>做过的决策</li>
  <li>发现的模式</li>
  <li>用户偏好</li>
  <li>Bug 修复和根因</li>
</ul>
<pre><code># 示例用法
store_memory({
    "content": "aibrain 选了 SQLite 而不是 PostgreSQL。个人项目，不需要扩展。",
    "tags": ["architecture", "aibrain"],
    "importance": 0.8
})</code></pre>
</div>

<h4>2. handoff — <span data-lang="en">Context Transfer</span><span data-lang="zh" style="display: none;">上下文转移</span></h4>

<div data-lang="en">
<p>Generates a structured handoff document:</p>
<ul>
  <li>Current task status</li>
  <li>Key files</li>
  <li>Decisions made</li>
  <li>Blockers</li>
  <li>Next steps</li>
</ul>
<p>This can be passed to a new AI session.</p>
</div>
<div data-lang="zh" style="display: none;">
<p>生成结构化的交接文档：</p>
<ul>
  <li>当前任务状态</li>
  <li>关键文件</li>
  <li>已做决策</li>
  <li>阻塞问题</li>
  <li>下一步</li>
</ul>
<p>可以传递给新的 AI 会话。</p>
</div>

<h3 data-lang="en">Trade-offs</h3>
<h3 data-lang="zh" style="display: none;">权衡</h3>

<div data-lang="en">
<ul>
  <li><strong>Time cost</strong>: Takes 2-5 minutes to create proper handoff</li>
  <li><strong>Discipline required</strong>: Must do it before quota runs out</li>
  <li><strong>Format learning</strong>: AI needs to understand the handoff format</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li><strong>时间成本</strong>: 创建合适的交接需要 2-5 分钟</li>
  <li><strong>需要自律</strong>: 必须在配额用完前做</li>
  <li><strong>格式学习</strong>: AI 需要理解交接格式</li>
</ul>
</div>

<h3 data-lang="en">Lessons Learned</h3>
<h3 data-lang="zh" style="display: none;">经验教训</h3>

<div data-lang="en">
<ol>
  <li><strong>Don't wait until quota runs out</strong> — Create handoff when you feel you're at a good stopping point</li>
  <li><strong>Keep it minimal</strong> — Only transfer what's essential</li>
  <li><strong>Test handoff</strong> — Verify the receiving AI understands the context</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<ol>
  <li><strong>不要等到配额用完</strong> — 在一个好的停止点就创建交接</li>
  <li><strong>保持最小</strong> — 只转移必要的</li>
  <li><strong>测试交接</strong> — 验证接收的 AI 理解上下文</li>
</ol>
</div>

<hr>

<h2>S002: <span data-lang="en">AI Cost Control — GLM-5 Fallback</span><span data-lang="zh" style="display: none;">AI 成本控制 — GLM-5 备用</span></h2>

<div data-lang="en">
<p><strong>Problem</strong>: <a href="/problems/">P002</a> — Subscription quotas run out, can't afford unlimited premium models.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>问题</strong>: <a href="/problems/">P002</a> — 订阅配额用完，用不起无限量的高级模型。</p>
</div>

<h3 data-lang="en">Solution</h3>
<h3 data-lang="zh" style="display: none;">解决方案</h3>

<div data-lang="en">
<p><strong>Primary</strong>: Codex / Claude Opus (best quality)<br>
<strong>Fallback</strong>: GLM-5 via Ali Bailian premium subscription</p>
<p><strong>Why GLM-5</strong>:</p>
<ul>
  <li>Close to Codex/Opus in quality</li>
  <li>Unlimited usage with premium subscription</li>
  <li>Good enough for most tasks</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>主力</strong>: Codex / Claude Opus（质量最好）<br>
<strong>备用</strong>: GLM-5（阿里百炼高级订阅）</p>
<p><strong>为什么选 GLM-5</strong>：</p>
<ul>
  <li>质量接近 Codex/Opus</li>
  <li>高级订阅无限量使用</li>
  <li>对大多数任务够用</li>
</ul>
</div>

<h3 data-lang="en">Decision Tree</h3>
<h3 data-lang="zh" style="display: none;">决策树</h3>

<pre><code data-lang="en">Task complexity?
├─ High → Codex/Opus (if quota available)
│         └─ No quota? → GLM-5
└─ Low/Medium → GLM-5 directly</code>
<code data-lang="zh" style="display: none;">任务复杂度？
├─ 高 → Codex/Opus（如果配额够）
│        └─ 没配额？ → GLM-5
└─ 低/中 → 直接用 GLM-5</code></pre>

<h3 data-lang="en">Trade-offs</h3>
<h3 data-lang="zh" style="display: none;">权衡</h3>

<div data-lang="en">
<ul>
  <li>GLM-5 slightly worse at complex reasoning</li>
  <li>Sometimes needs more prompts to get same result</li>
  <li>But: unlimited, predictable cost</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li>GLM-5 复杂推理稍弱</li>
  <li>有时需要更多 prompt 才能得到相同结果</li>
  <li>但：无限量，成本可预测</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Template for New Solutions</h2>
<h2 data-lang="zh" style="display: none;">新方案模板</h2>

<div data-lang="en">
<p>When adding a new solution:</p>
<ol>
  <li><strong>Problem</strong>: Link to the problem page</li>
  <li><strong>What I tried</strong>: List attempts</li>
  <li><strong>What worked</strong>: The actual solution</li>
  <li><strong>Trade-offs</strong>: What I gave up</li>
  <li><strong>Lessons learned</strong>: For future reference</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<p>添加新解决方案时：</p>
<ol>
  <li><strong>问题</strong>: 链接到问题页面</li>
  <li><strong>尝试了什么</strong>: 列出尝试</li>
  <li><strong>什么有效</strong>: 实际解决方案</li>
  <li><strong>权衡</strong>: 放弃了什么</li>
  <li><strong>经验教训</strong>: 供未来参考</li>
</ol>
</div>