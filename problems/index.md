---
layout: default
title: Problems
---

<h1 data-lang="en">Problems &amp; Pain Points</h1>
<h1 data-lang="zh" style="display: none;">问题与痛点</h1>

<p data-lang="en">Ongoing list of challenges I've encountered. Some solved, some not.</p>
<p data-lang="zh" style="display: none;">持续更新的挑战清单。有些解决了，有些没有。</p>

<hr>

<h2 data-lang="en">Status Legend</h2>
<h2 data-lang="zh" style="display: none;">状态说明</h2>

<div data-lang="en">
<ul>
  <li>🟡 <strong>Pending</strong> — Not started</li>
  <li>🔵 <strong>In Progress</strong> — Working on it</li>
  <li>🟢 <strong>Solved</strong> — Has solution</li>
  <li>🔴 <strong>Paused</strong> — Deprioritized</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li>🟡 <strong>待解决</strong> — 还没开始</li>
  <li>🔵 <strong>进行中</strong> — 正在处理</li>
  <li>🟢 <strong>已解决</strong> — 有解决方案</li>
  <li>🔴 <strong>暂停</strong> — 优先级降低</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Architecture &amp; Design</h2>
<h2 data-lang="zh" style="display: none;">架构与设计</h2>

<h3>P001: <span data-lang="en">Self-Reference Problem</span><span data-lang="zh" style="display: none;">自指问题</span></h3>

<div data-lang="en">
<p><strong>Status</strong>: 🟡 Pending</p>
<p><strong>Context</strong>: When developing PCP (a protocol layer), I sometimes accidentally use the architecture I'm building while I'm building it.</p>
<p><strong>Impact</strong>: Creates circular dependencies, hard to test, confusing.</p>
<p><strong>Attempts</strong>: None yet.</p>
<p><strong>Related</strong>: PCP project</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>: 🟡 待解决</p>
<p><strong>背景</strong>: 开发 PCP（协议层）时，有时会不小心在自己构建的架构中使用自己正在构建的架构。</p>
<p><strong>影响</strong>: 造成循环依赖，难以测试，令人困惑。</p>
<p><strong>尝试</strong>: 暂无。</p>
<p><strong>相关</strong>: PCP 项目</p>
</div>

<hr>

<h3>P002: <span data-lang="en">Project Complexity Spiral</span><span data-lang="zh" style="display: none;">项目复杂度失控</span></h3>

<div data-lang="en">
<p><strong>Status</strong>: 🔵 In Progress</p>
<p><strong>Context</strong>: Every complex project I work on becomes messy over time. The more I build, the harder it is to plan. I can't see the structure anymore.</p>
<p><strong>Symptoms</strong>:</p>
<ul>
  <li>Features coupling — change one thing, break another</li>
  <li>Afraid to refactor — don't know what will break</li>
  <li>Can't estimate work — everything feels interconnected</li>
  <li>New features add complexity exponentially</li>
</ul>
<p><strong>Root cause</strong>: No clear boundaries between modules. Code grows organically without interface definitions.</p>
<p><strong>My solution — Decompose to interfaces</strong>:</p>
<ol>
  <li><strong>Define <code>_dict</code> interface</strong> — simplest possible contract: function + input + output</li>
  <li><strong>Extract from chaos</strong> — find working code, define its interface, isolate it</li>
  <li><strong>Core first, extras later</strong> — split core functionality before peripheral features</li>
  <li><strong>Verify with baseline</strong> — ensure same output before and after refactoring</li>
</ol>
<p><strong>Current workflow</strong>:</p>
<ul>
  <li>AI decomposes and explains to me</li>
  <li>Future: AI decomposes, I customize the interface</li>
</ul>
<p><strong>Related</strong>: All projects (PCP, aibrain, Expense Tracker)</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>: 🔵 进行中</p>
<p><strong>背景</strong>: 每个复杂项目做着做着就乱了。越做越没法规划。看不到结构。</p>
<p><strong>症状</strong>：</p>
<ul>
  <li>功能耦合 — 改一处，坏多处</li>
  <li>不敢重构 — 不知道会破坏什么</li>
  <li>无法估时 — 感觉什么都连在一起</li>
  <li>新功能让复杂度指数级增长</li>
</ul>
<p><strong>根本原因</strong>: 模块之间没有清晰的边界。代码有机生长，没有接口定义。</p>
<p><strong>我的解法 — 拆解到接口</strong>：</p>
<ol>
  <li><strong>定义 <code>_dict</code> 接口</strong> — 最简单的契约：功能 + 输入 + 输出</li>
  <li><strong>从混乱中提取</strong> — 找到能用的代码，定义接口，隔离出来</li>
  <li><strong>先核心，后额外</strong> — 先拆核心功能，再拆周边功能</li>
  <li><strong>Baseline 验证</strong> — 确保修改前后输出一致</li>
</ol>
<p><strong>当前工作流</strong>：</p>
<ul>
  <li>AI 拆解，讲给我听</li>
  <li>日后：AI 拆解，我来定制接口</li>
</ul>
<p><strong>相关</strong>: 所有项目（PCP、aibrain、记账）</p>
</div>

<hr>

<h2 data-lang="en">Cost Management</h2>
<h2 data-lang="zh" style="display: none;">成本管理</h2>

<h3>P003: <span data-lang="en">AI Cost Control for Solo Developers</span><span data-lang="zh" style="display: none;">个人开发者的 AI 成本控制</span></h3>

<div data-lang="en">
<p><strong>Status</strong>: 🔵 In Progress</p>
<p><strong>Context</strong>: As a solo developer, keeping costs low is critical. I try to avoid spending money whenever possible.</p>
<p><strong>Pain point</strong>:</p>
<ul>
  <li>Subscription quotas run out</li>
  <li>Need fallback options</li>
  <li>Can't always use the best model</li>
</ul>
<p><strong>Current approach</strong>:</p>
<ul>
  <li>GLM-5 as unlimited fallback</li>
  <li>Switch platforms when quota exhausted</li>
</ul>
<p><strong>Trade-off</strong>: Quality vs cost</p>
<p><strong>Related</strong>: <a href="/workflow/">Workflow</a></p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>: 🔵 进行中</p>
<p><strong>背景</strong>: 作为个人开发者，保持低成本很关键。能不花钱就不花钱。</p>
<p><strong>痛点</strong>：</p>
<ul>
  <li>订阅配额用完</li>
  <li>需要备用方案</li>
  <li>不能总用最好的模型</li>
</ul>
<p><strong>当前方案</strong>：</p>
<ul>
  <li>GLM-5 作为无限量备用</li>
  <li>配额用完切换平台</li>
</ul>
<p><strong>权衡</strong>: 质量 vs 成本</p>
<p><strong>相关</strong>: <a href="/workflow/">开发流程</a></p>
</div>

<hr>

<h2 data-lang="en">Workflow &amp; Process</h2>
<h2 data-lang="zh" style="display: none;">流程与工作流</h2>

<h3>P004: <span data-lang="en">Git Workflow for Solo Developers</span><span data-lang="zh" style="display: none;">个人开发者的 Git 工作流</span></h3>

<div data-lang="en">
<p><strong>Status</strong>: 🟡 Pending</p>
<p><strong>Context</strong>: I don't use Git well. No habits formed. Since I'm the only developer, I don't care much.</p>
<p><strong>Pain point</strong>:</p>
<ul>
  <li>Don't know proper Git workflow</li>
  <li>No branching strategy</li>
  <li>Commit messages are messy</li>
  <li>No code review</li>
</ul>
<p><strong>Impact</strong>: Hard to track changes, hard to revert, hard to collaborate if needed</p>
<p><strong>Attempts</strong>: None yet.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>: 🟡 待解决</p>
<p><strong>背景</strong>: 我 Git 用得不好。没有形成习惯。因为只有我一个人开发，所以不太在意。</p>
<p><strong>痛点</strong>：</p>
<ul>
  <li>不知道正确的 Git 工作流</li>
  <li>没有分支策略</li>
  <li>提交信息混乱</li>
  <li>没有代码审查</li>
</ul>
<p><strong>影响</strong>: 难以追踪变更，难以回滚，需要协作时困难</p>
<p><strong>尝试</strong>: 暂无。</p>
</div>

<h3>P005: <span data-lang="en">Context Handoff Across Platforms</span><span data-lang="zh" style="display: none;">跨平台上下文交接</span></h3>

<div data-lang="en">
<p><strong>Status</strong>: 🟢 Solved</p>
<p><strong>Context</strong>: When AI tool quota runs out, I need to switch platforms. But the new platform doesn't know my project context.</p>
<p><strong>Solution</strong>:</p>
<ul>
  <li><strong>automem</strong>: Memory storage across sessions</li>
  <li><strong>handoff</strong>: Context transfer protocol</li>
</ul>
<p><strong>Trade-off</strong>: Takes time to setup handoff</p>
<p><strong>Related</strong>: aibrain, PCP</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>: 🟢 已解决</p>
<p><strong>背景</strong>: AI 工具配额用完时，需要切换平台。但新平台不知道我的项目上下文。</p>
<p><strong>解决方案</strong>：</p>
<ul>
  <li><strong>automem</strong>: 跨会话记忆存储</li>
  <li><strong>handoff</strong>: 上下文转移协议</li>
</ul>
<p><strong>权衡</strong>: 设置交接需要时间</p>
<p><strong>相关</strong>: aibrain, PCP</p>
</div>

<hr>

<h2 data-lang="en">Technical Issues</h2>
<h2 data-lang="zh" style="display: none;">技术问题</h2>

<h3>P006: <span data-lang="en">Mermaid Font Rendering</span><span data-lang="zh" style="display: none;">Mermaid 字体渲染</span></h3>

<div data-lang="en">
<p><strong>Status</strong>: 🔵 In Progress</p>
<p><strong>Context</strong>: When AI generates Mermaid diagrams and converts to images, the fonts look weird.</p>
<p><strong>Problem</strong>: Default fonts don't support Chinese well, or look ugly.</p>
<p><strong>Current approach</strong>: Download fonts manually.</p>
<p><strong>Not yet automated</strong>.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>: 🔵 进行中</p>
<p><strong>背景</strong>: AI 生成 Mermaid 图并转换为图片时，字体看起来很怪。</p>
<p><strong>问题</strong>: 默认字体对中文支持不好，或者看起来很丑。</p>
<p><strong>当前方案</strong>: 手动下载字体。</p>
<p><strong>尚未自动化</strong>。</p>
</div>

<hr>

<h2 data-lang="en">Summary</h2>
<h2 data-lang="zh" style="display: none;">总览</h2>

<div data-lang="en">
<table>
  <thead><tr><th>#</th><th>Problem</th><th>Status</th><th>Solution</th></tr></thead>
  <tbody>
    <tr><td>P001</td><td>Self-reference in architecture design</td><td>🟡 Pending</td><td>-</td></tr>
    <tr><td>P002</td><td>Project complexity spiral</td><td>🔵 In Progress</td><td>_dict interface decomposition</td></tr>
    <tr><td>P003</td><td>AI cost control for solo devs</td><td>🔵 In Progress</td><td>GLM-5 fallback</td></tr>
    <tr><td>P004</td><td>Git workflow for solo devs</td><td>🟡 Pending</td><td>-</td></tr>
    <tr><td>P005</td><td>Context handoff across platforms</td><td>🟢 Solved</td><td>automem, handoff</td></tr>
    <tr><td>P006</td><td>Mermaid font rendering</td><td>🔵 In Progress</td><td>Manual fonts</td></tr>
  </tbody>
</table>
</div>
<div data-lang="zh" style="display: none;">
<table>
  <thead><tr><th>#</th><th>问题</th><th>状态</th><th>解决方案</th></tr></thead>
  <tbody>
    <tr><td>P001</td><td>架构设计的自指问题</td><td>🟡 待解决</td><td>-</td></tr>
    <tr><td>P002</td><td>项目复杂度失控</td><td>🔵 进行中</td><td>_dict 接口拆解</td></tr>
    <tr><td>P003</td><td>个人开发者的 AI 成本控制</td><td>🔵 进行中</td><td>GLM-5 备用</td></tr>
    <tr><td>P004</td><td>个人开发者的 Git 工作流</td><td>🟡 待解决</td><td>-</td></tr>
    <tr><td>P005</td><td>跨平台上下文交接</td><td>🟢 已解决</td><td>automem, handoff</td></tr>
    <tr><td>P006</td><td>Mermaid 字体渲染</td><td>🔵 进行中</td><td>手动字体</td></tr>
  </tbody>
</table>
</div>

<hr>

<p data-lang="en"><em>This list is continuously updated as I encounter new problems.</em></p>
<p data-lang="zh" style="display: none;"><em>这个列表会随着我遇到新问题持续更新。</em></p>