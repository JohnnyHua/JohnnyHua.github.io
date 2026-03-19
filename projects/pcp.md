---
layout: post
title: PCP (Progress Control Plane)
date: 2026-03-18
tags: [typescript, opencode, workflow, ai]
status: in-progress
github: https://github.com/JohnnyHua/pcp-skills
started: 2026-02-21
---

<h2 data-lang="en">Origin</h2>
<h2 data-lang="zh" style="display: none;">起源</h2>

<div data-lang="en">
<p>PCP started from a bigger idea: an AI development team.</p>
<p>The vision was a chain of agents:</p>
<ul>
  <li><strong>Sales Agent</strong> — talks to users, collects requirements via chat</li>
  <li><strong>CTO Agent</strong> — defines technical roadmap</li>
  <li><strong>PM Agent</strong> — one per project, breaks down work</li>
  <li><strong>Dev Agent</strong> — writes code</li>
  <li><strong>Test Agent</strong> — validates, reports back to PM</li>
</ul>
<p>Each agent would be driven by prompts. Simple enough?</p>
<p><strong>Problem</strong>: Each agent's job is a huge project by itself. The communication between agents is even harder.</p>
<p><strong>Simplification</strong>: Reduce to one problem — how does PM control Dev?</p>
<p>That became PCP: a protocol layer between PM and Dev that defines a stable, verifiable workflow.</p>
</div>
<div data-lang="zh" style="display: none;">
<p>PCP 源于一个更大的想法：AI 开发团队。</p>
<p>愿景是一条 Agent 链：</p>
<ul>
  <li><strong>销售 Agent</strong> — 和用户聊天，收集需求</li>
  <li><strong>CTO Agent</strong> — 制定技术路线</li>
  <li><strong>PM Agent</strong> — 每个项目一个，拆解工作</li>
  <li><strong>Dev Agent</strong> — 写代码</li>
  <li><strong>测试 Agent</strong> — 验证，汇报回 PM</li>
</ul>
<p>每个 Agent 用提示词驱动。听起来很简单？</p>
<p><strong>问题</strong>：每个 Agent 的工作本身就是一个大项目。Agent 之间的沟通更难。</p>
<p><strong>简化</strong>：缩小到一个问题 — PM 怎么控制 Dev？</p>
<p>这就变成了 PCP：PM 和 Dev 之间的协议层，定义一套稳定、可验证的工作流。</p>
</div>

<hr>

<h2 data-lang="en">What PCP Is</h2>
<h2 data-lang="zh" style="display: none;">PCP 是什么</h2>

<div data-lang="en">
<p><strong>PCP is a protocol layer and state kernel for PM-Agent and Dev-Agent collaboration.</strong></p>
<p>It does not execute product code. It does not make autonomous product decisions.</p>
<p>Think of PCP like HTTP for AI collaboration: it standardizes interaction and verification.</p>
<p><strong>Current use</strong>: PCP now controls my own development — keeping me on track, not drifting.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>PCP 是 PM-Agent 和 Dev-Agent 协作的协议层和状态内核。</strong></p>
<p>它不执行产品代码，不做自主产品决策。</p>
<p>把 PCP 想象成 AI 协作的 HTTP：标准化交互和验证。</p>
<p><strong>当前用途</strong>：PCP 现在用来控制我自己的开发 — 保持聚焦，不跑偏。</p>
</div>

<hr>

<h2 data-lang="en">What Works Today</h2>
<h2 data-lang="zh" style="display: none;">当前能用什么</h2>

<div data-lang="en">
<p><strong>Host</strong>: OpenCode (plugin installed via <code>npx skills add JohnnyHua/pcp-skills</code>)</p>
<p><strong>Scenario</strong>: Single developer, single project directory</p>
<p><strong>Available workflow</strong>:</p>
<ul>
  <li><code>pcp_init</code> — scan project, establish baseline</li>
  <li><code>pcp_plan</code> — compile approved tasks into queue</li>
  <li><code>pcp_status</code> — show current task, queue, backlog</li>
  <li><code>pcp_done</code> — submit completion (gated approval)</li>
  <li><code>pcp_review</code> / <code>pcp_review_apply</code> — unified review flow</li>
  <li><code>pcp_handoff</code> — generate handoff for another AI tool</li>
  <li><code>pcp_intake</code> — resume from handoff or onboard new project</li>
  <li>Proposal / Blueprint / Concern / Backlog management</li>
</ul>
<p><strong>Not yet</strong>: Multi-host adapters (Claude Code, Cursor), semantic intent layer</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>宿主</strong>: OpenCode（通过 <code>npx skills add JohnnyHua/pcp-skills</code> 安装插件）</p>
<p><strong>场景</strong>: 单人、单项目目录</p>
<p><strong>可用工作流</strong>：</p>
<ul>
  <li><code>pcp_init</code> — 扫描项目，建立基线</li>
  <li><code>pcp_plan</code> — 编译已批准的任务到队列</li>
  <li><code>pcp_status</code> — 显示当前任务、队列、backlog</li>
  <li><code>pcp_done</code> — 提交完成（需审批）</li>
  <li><code>pcp_review</code> / <code>pcp_review_apply</code> — 统一审核流程</li>
  <li><code>pcp_handoff</code> — 生成交接文档给其他 AI 工具</li>
  <li><code>pcp_intake</code> — 从交接恢复或接入新项目</li>
  <li>Proposal / Blueprint / Concern / Backlog 管理</li>
</ul>
<p><strong>暂不支持</strong>：多宿主适配器（Claude Code、Cursor）、语义意图层</p>
</div>

<hr>

<h2 data-lang="en">Problems PCP Solves</h2>
<h2 data-lang="zh" style="display: none;">解决的问题</h2>

<div data-lang="en">
<ol>
  <li><strong>Session drift</strong> — AI wanders off, forgets the main task</li>
  <li><strong>Interrupted work</strong> — Cannot resume cleanly after interruption</li>
  <li><strong>Hallucinated completion</strong> — Claims done without evidence</li>
  <li><strong>Inconsistent state</strong> — Multi-session development lacks shared context</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<ol>
  <li><strong>会话漂移</strong> — AI 跑偏，忘记主任务</li>
  <li><strong>中断无法恢复</strong> — 工作被打断后无法干净地继续</li>
  <li><strong>虚假完成</strong> — 没有证据就声称完成</li>
  <li><strong>状态不一致</strong> — 多会话开发缺乏共享上下文</li>
</ol>
</div>

<hr>

<h2 data-lang="en">Architecture</h2>
<h2 data-lang="zh" style="display: none;">架构</h2>

<div data-lang="en">
<p>All state lives in <code>.opencode/pcp/</code> inside your project:</p>
<table>
  <thead><tr><th>File</th><th>Purpose</th></tr></thead>
  <tbody>
    <tr><td><code>stack.json</code></td><td>Runtime state — current task, queue, IDs (SSOT)</td></tr>
    <tr><td><code>events.jsonl</code></td><td>Append-only event log — full history</td></tr>
    <tr><td><code>taskcards/</code></td><td>TaskCard files — one JSON per task</td></tr>
    <tr><td><code>plans/</code></td><td>Plan records — compiled from pcp_plan</td></tr>
    <tr><td><code>blueprints/</code></td><td>Blueprints — step-by-step execution guides</td></tr>
    <tr><td><code>PROJECT.md</code></td><td>Project baseline — purpose, status, constraints</td></tr>
    <tr><td><code>WORKLOG.md</code></td><td>Work log — chronological notes</td></tr>
    <tr><td><code>HANDOFF.md</code></td><td>Handoff document — generated on demand</td></tr>
  </tbody>
</table>
<p><strong>Key rule</strong>: <code>stack.json</code> is the single source of truth for runtime state.</p>
</div>
<div data-lang="zh" style="display: none;">
<p>所有状态存储在项目内的 <code>.opencode/pcp/</code> 目录：</p>
<table>
  <thead><tr><th>文件</th><th>用途</th></tr></thead>
  <tbody>
    <tr><td><code>stack.json</code></td><td>运行时状态 — 当前任务、队列、ID（SSOT）</td></tr>
    <tr><td><code>events.jsonl</code></td><td>追加式事件日志 — 完整历史</td></tr>
    <tr><td><code>taskcards/</code></td><td>任务卡片 — 每个任务一个 JSON</td></tr>
    <tr><td><code>plans/</code></td><td>计划记录 — 由 pcp_plan 编译</td></tr>
    <tr><td><code>blueprints/</code></td><td>蓝图 — 分步执行指南</td></tr>
    <tr><td><code>PROJECT.md</code></td><td>项目基线 — 目的、状态、约束</td></tr>
    <tr><td><code>WORKLOG.md</code></td><td>工作日志 — 按时间记录</td></tr>
    <tr><td><code>HANDOFF.md</code></td><td>交接文档 — 按需生成</td></tr>
  </tbody>
</table>
<p><strong>核心规则</strong>：<code>stack.json</code> 是运行时状态的单一数据源。</p>
</div>

<hr>

<h2 data-lang="en">Protocol Principles</h2>
<h2 data-lang="zh" style="display: none;">协议原则</h2>

<div data-lang="en">
<ol>
  <li><strong>No UI</strong> — Keep Markdown/JSON interface, faster iteration, easier audit</li>
  <li><strong>SSOT is stack.json</strong> — Prevents state divergence across views</li>
  <li><strong>Evidence is mandatory</strong> — Task completion requires verifiable proof</li>
  <li><strong>Planning stays in PM layer</strong> — Protocol doesn't do autonomous planning</li>
  <li><strong>Approval-first</strong> — Tasks and subtasks require explicit approval before execution</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<ol>
  <li><strong>没有 UI</strong> — 保持 Markdown/JSON 接口，迭代更快，审计更易</li>
  <li><strong>SSOT 是 stack.json</strong> — 防止跨视图状态分歧</li>
  <li><strong>证据是强制的</strong> — 任务完成需要可验证的证据</li>
  <li><strong>规划留在 PM 层</strong> — 协议层不做自主规划</li>
  <li><strong>审批优先</strong> — 任务和子任务需要明确审批后才能执行</li>
</ol>
</div>

<hr>

<h2 data-lang="en">Tech Stack</h2>
<h2 data-lang="zh" style="display: none;">技术栈</h2>

<div data-lang="en">
<ul>
  <li><strong>Runtime</strong>: OpenCode plugin (TypeScript)</li>
  <li><strong>State</strong>: JSON + Markdown files (local only)</li>
  <li><strong>Skills</strong>: pcp-intake, pcp-setup, pcp-sprint-review</li>
  <li><strong>Tools</strong>: 20+ PCP commands</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li><strong>运行时</strong>: OpenCode 插件 (TypeScript)</li>
  <li><strong>状态</strong>: JSON + Markdown 文件（仅本地）</li>
  <li><strong>技能</strong>: pcp-intake, pcp-setup, pcp-sprint-review</li>
  <li><strong>工具</strong>: 20+ PCP 命令</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Progress</h2>
<h2 data-lang="zh" style="display: none;">进度</h2>

<div data-lang="en">
<p><strong>Version</strong>: v0 complete, starting v0.1</p>
<ul>
  <li><input type="checkbox" checked disabled> TaskCard / Queue / stack.json</li>
  <li><input type="checkbox" checked disabled> pcp_init / pcp_plan / pcp_done / pcp_status</li>
  <li><input type="checkbox" checked disabled> Proposal / Subtask approval flow</li>
  <li><input type="checkbox" checked disabled> Blueprint for complex tasks</li>
  <li><input type="checkbox" checked disabled> Handoff / Intake</li>
  <li><input type="checkbox" checked disabled> Backlog / Concern Log</li>
  <li><input type="checkbox" checked disabled> pcp_review / pcp_review_apply</li>
  <li><input type="checkbox" disabled> v0.1 UX polish (in progress)</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>版本</strong>: v0 完成，开始 v0.1</p>
<ul>
  <li><input type="checkbox" checked disabled> TaskCard / Queue / stack.json</li>
  <li><input type="checkbox" checked disabled> pcp_init / pcp_plan / pcp_done / pcp_status</li>
  <li><input type="checkbox" checked disabled> Proposal / Subtask 审批流程</li>
  <li><input type="checkbox" checked disabled> Blueprint 复杂任务支持</li>
  <li><input type="checkbox" checked disabled> Handoff / Intake</li>
  <li><input type="checkbox" checked disabled> Backlog / Concern Log</li>
  <li><input type="checkbox" checked disabled> pcp_review / pcp_review_apply</li>
  <li><input type="checkbox" disabled> v0.1 体验优化（进行中）</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Lessons Learned</h2>
<h2 data-lang="zh" style="display: none;">经验教训</h2>

<div data-lang="en">
<ol>
  <li><strong>Start with one agent pair</strong> — PM+Dev is complex enough; don't add more agents until this works</li>
  <li><strong>Evidence-first changes behavior</strong> — Requiring proof makes completion claims honest</li>
  <li><strong>Protocol is not executor</strong> — PCP guides workflow, doesn't run code</li>
  <li><strong>Self-use reveals gaps</strong> — Using PCP for my own development shows what's missing</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<ol>
  <li><strong>从一个 Agent 对开始</strong> — PM+Dev 已经够复杂了；先让它工作再加更多 Agent</li>
  <li><strong>证据优先改变行为</strong> — 要求证据让完成声明变得诚实</li>
  <li><strong>协议不是执行器</strong> — PCP 指导工作流，不运行代码</li>
  <li><strong>自用暴露问题</strong> — 用 PCP 控制自己的开发才发现缺失什么</li>
</ol>
</div>

<hr>

<h2 data-lang="en">Related Problems</h2>
<h2 data-lang="zh" style="display: none;">相关问题</h2>

<ul>
  <li>P001: <span data-lang="en">Self-reference problem</span><span data-lang="zh" style="display: none;">自指问题</span> — developing PCP while using PCP</li>
  <li>P004: <span data-lang="en">Context handoff across platforms</span><span data-lang="zh" style="display: none;">跨平台上下文交接</span></li>
</ul>

<hr>

<h2 data-lang="en">Future</h2>
<h2 data-lang="zh" style="display: none;">未来计划</h2>

<div data-lang="en">
<p><strong>v0.1</strong>: UX polish — smoother intake, better prompts, less noise</p>
<p><strong>v0.2</strong>: Cross-tool handoff — Claude Code, Cursor adapters</p>
<p><strong>v0.3</strong>: Smarter protocol — semantic intent, multi-host support</p>
<p><strong>Long-term</strong>: Maybe return to the original multi-agent vision — but only after PM+Dev works reliably.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>v0.1</strong>: 体验优化 — 更顺的 intake，更好的提示，更少的噪音</p>
<p><strong>v0.2</strong>: 跨工具交接 — Claude Code、Cursor 适配器</p>
<p><strong>v0.3</strong>: 更智能的协议 — 语义意图、多宿主支持</p>
<p><strong>长期</strong>: 也许回到最初的多 Agent 愿景 — 但要等 PM+Dev 稳定可靠之后。</p>
</div>