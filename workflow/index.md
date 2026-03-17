---
layout: default
title: Development Workflow
---

<h1 data-lang="en">Development Workflow</h1>
<h1 data-lang="zh" style="display: none;">开发流程</h1>

<p data-lang="en">How I work with AI tools day-to-day.</p>
<p data-lang="zh" style="display: none;">我如何日常使用 AI 工具工作。</p>

<hr>

<h2 data-lang="en">My AI Tool Stack</h2>
<h2 data-lang="zh" style="display: none;">AI 工具栈</h2>

<div data-lang="en">
<table>
  <thead>
    <tr><th>Tool</th><th>Primary Use</th><th>Why</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>Cursor</strong></td><td>Company projects</td><td>Subscription, integrated IDE</td></tr>
    <tr><td><strong>Codex</strong></td><td>Daily projects</td><td>Strong code generation, structured</td></tr>
    <tr><td><strong>Claude Code</strong></td><td>Daily projects</td><td>Good reasoning, complements Codex</td></tr>
    <tr><td><strong>OpenCode</strong></td><td>Flexible model selection</td><td>More freedom, larger quota</td></tr>
    <tr><td><strong>GLM-5</strong> (via Ali Bailian)</td><td>High-volume tasks</td><td>Premium subscription, cost-effective</td></tr>
    <tr><td><strong>ChatGPT</strong></td><td>Pre-development planning</td><td>Voice input saves typing time</td></tr>
  </tbody>
</table>
</div>
<div data-lang="zh" style="display: none;">
<table>
  <thead>
    <tr><th>工具</th><th>主要用途</th><th>原因</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>Cursor</strong></td><td>公司项目</td><td>订阅，集成 IDE</td></tr>
    <tr><td><strong>Codex</strong></td><td>日常项目</td><td>代码生成强，规范</td></tr>
    <tr><td><strong>Claude Code</strong></td><td>日常项目</td><td>推理好，与 Codex 互补</td></tr>
    <tr><td><strong>OpenCode</strong></td><td>灵活选模型</td><td>更自由，配额大</td></tr>
    <tr><td><strong>GLM-5</strong> (阿里百炼)</td><td>高用量任务</td><td>高级订阅，性价比高</td></tr>
    <tr><td><strong>ChatGPT</strong></td><td>开发前规划</td><td>语音输入节省打字时间</td></tr>
  </tbody>
</table>
</div>

<hr>

<h2 data-lang="en">Model Selection Logic</h2>
<h2 data-lang="zh" style="display: none;">模型选择逻辑</h2>

<div data-lang="en">
<p><strong>Problem</strong>: Subscription plans have usage limits. As I run 3-4 projects in parallel, I often hit quotas.</p>
<p><strong>Solution</strong>:</p>
<pre><code>Codex/Opus (best quality)
      ↓ quota exhausted?
GLM-5 (close second, unlimited)
      ↓ need specific API?
OpenAI API (for embeddings, specific tasks)</code></pre>
<p>GLM-5 is the closest to Codex/Opus in quality. When subscriptions run out, it becomes my daily driver.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>问题</strong>：订阅计划有用量限制。我同时跑 3-4 个项目，经常触达配额。</p>
<p><strong>解决方案</strong>：</p>
<pre><code>Codex/Opus（质量最好）
      ↓ 配额用完？
GLM-5（仅次于前者，无限量）
      ↓ 需要特定 API？
OpenAI API（用于 embedding 等特定任务）</code></pre>
<p>GLM-5 是质量上最接近 Codex/Opus 的模型。订阅用完后，它成为我的主力。</p>
</div>

<hr>

<h2 data-lang="en">Development Flow</h2>
<h2 data-lang="zh" style="display: none;">开发流程</h2>

<h3 data-lang="en">Phase 1: Pre-Development (ChatGPT)</h3>
<h3 data-lang="zh" style="display: none;">阶段一：开发前（ChatGPT）</h3>

<div data-lang="en">
<p><strong>Before writing any code, I talk to ChatGPT.</strong></p>
<p>Using voice input (saves typing time), I discuss:</p>
<ul>
  <li>Project architecture</li>
  <li>Competitor analysis</li>
  <li>Task breakdown</li>
  <li>Development standards</li>
  <li>Process design</li>
</ul>
<p>This phase clarifies direction before diving into implementation.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>写代码之前，先和 ChatGPT 聊。</strong></p>
<p>用语音输入（节省打字时间），讨论：</p>
<ul>
  <li>项目架构</li>
  <li>竞品分析</li>
  <li>任务拆解</li>
  <li>开发规范</li>
  <li>流程设计</li>
</ul>
<p>这个阶段在动手之前理清方向。</p>
</div>

<h3 data-lang="en">Phase 2: Development (Codex/Claude/GLM)</h3>
<h3 data-lang="zh" style="display: none;">阶段二：开发中（Codex/Claude/GLM）</h3>

<div data-lang="en">
<p><strong>AI controls the entire coding process.</strong></p>
<ul>
  <li>Continue tasks iteratively</li>
  <li>AI writes code, I review</li>
  <li>Keep context in one session per project</li>
  <li>One directory = one conversation (no parallel mixing)</li>
</ul>
<p><strong>When stuck</strong>:</p>
<ol>
  <li>Handoff context to ChatGPT</li>
  <li>Talk through the problem</li>
  <li>Return to coding session with clarity</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>AI 全程控制编码过程。</strong></p>
<ul>
  <li>迭代式继续任务</li>
  <li>AI 写代码，我 review</li>
  <li>每个项目一个会话保持上下文</li>
  <li>一个目录 = 一个对话（不并行混合）</li>
</ul>
<p><strong>卡住时</strong>：</p>
<ol>
  <li>把上下文交给 ChatGPT</li>
  <li>聊通问题</li>
  <li>带着清晰思路回到编码会话</li>
</ol>
</div>

<h3 data-lang="en">Phase 3: Review</h3>
<h3 data-lang="zh" style="display: none;">阶段三：Review</h3>

<div data-lang="en">
<p><strong>What I check</strong>:</p>
<ul>
  <li>Logic correctness (primary focus)</li>
  <li>Sometimes request visual verification</li>
  <li>API testing</li>
  <li>Application-level validation</li>
</ul>
<p><strong>When issues found</strong>:</p>
<ol>
  <li>Clarify the logic first</li>
  <li>Ask AI to rewrite (not fix blindly)</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>检查什么</strong>：</p>
<ul>
  <li>逻辑正确性（主要关注）</li>
  <li>有时要求可视化验证</li>
  <li>API 测试</li>
  <li>应用级别验证</li>
</ul>
<p><strong>发现问题</strong>：</p>
<ol>
  <li>先理清逻辑</li>
  <li>让 AI 重写（不是盲目修复）</li>
</ol>
</div>

<hr>

<h2 data-lang="en">Managing Multiple Projects</h2>
<h2 data-lang="zh" style="display: none;">多项目管理</h2>

<div data-lang="en">
<p><strong>Challenge</strong>: 3-4 projects running in parallel.</p>
<p><strong>How I avoid context mixing</strong>:</p>
<ul>
  <li>One project directory = one AI session</li>
  <li>Never run multiple projects in the same conversation</li>
  <li>Switch projects = switch context completely</li>
</ul>
<p><strong>Managing ideas</strong>:</p>
<ul>
  <li>Create a folder when an idea emerges</li>
  <li>Start prototyping immediately</li>
  <li>Ideas that stay are the ones worth building</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>挑战</strong>：同时跑 3-4 个项目。</p>
<p><strong>如何避免上下文混淆</strong>：</p>
<ul>
  <li>一个项目目录 = 一个 AI 会话</li>
  <li>从不在同一个对话里跑多个项目</li>
  <li>切项目 = 完全切换上下文</li>
</ul>
<p><strong>想法管理</strong>：</p>
<ul>
  <li>有想法时创建文件夹</li>
  <li>立即开始原型</li>
  <li>能留下来的想法才值得做</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Key Learnings</h2>
<h2 data-lang="zh" style="display: none;">关键经验</h2>

<div data-lang="en">
<ol>
  <li><strong>Voice input is underrated</strong> — ChatGPT voice saves 80% of typing time during planning</li>
  <li><strong>Quota management matters</strong> — Having a fallback model (GLM-5) prevents workflow interruption</li>
  <li><strong>One session per project</strong> — Prevents AI from confusing contexts</li>
  <li><strong>Clarify before rewrite</strong> — Fixing logic &gt; fixing code</li>
  <li><strong>AI controls, human reviews</strong> — I don't write code anymore, I review it</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<ol>
  <li><strong>语音输入被低估了</strong> — ChatGPT 语音在规划阶段节省 80% 打字时间</li>
  <li><strong>配额管理很重要</strong> — 有备用模型（GLM-5）防止工作流中断</li>
  <li><strong>一个会话一个项目</strong> — 避免 AI 混淆上下文</li>
  <li><strong>先理清再重写</strong> — 修复逻辑 &gt; 修复代码</li>
  <li><strong>AI 控制，人审核</strong> — 我不再写代码了，我只审核代码</li>
</ol>
</div>