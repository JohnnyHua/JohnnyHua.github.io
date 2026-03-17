---
layout: post
title: aibrain
date: 2026-03-17
tags: [python, discord, ai, personal-tool]
status: paused
github: https://github.com/JohnnyHua/aibrain
---

<h2 data-lang="en">Goal</h2>
<h2 data-lang="zh" style="display: none;">目标</h2>

<p data-lang="en">Personal AI memory assistant - collects data from my daily activities and helps me remember and retrieve information.</p>
<p data-lang="zh" style="display: none;">个人AI记忆助手 - 收集日常活动数据，帮助记忆和检索信息。</p>

<h2 data-lang="en">Tech Stack</h2>
<h2 data-lang="zh" style="display: none;">技术栈</h2>

<div data-lang="en">
<ul>
  <li><strong>Backend</strong>: Python, FastAPI, SQLAlchemy, SQLite</li>
  <li><strong>Frontend</strong>: React, TypeScript, Vite</li>
  <li><strong>Bot</strong>: Discord.py</li>
  <li><strong>AI</strong>: OpenAI API, Claude API</li>
  <li><strong>Infrastructure</strong>: Docker, Docker Compose</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li><strong>后端</strong>: Python, FastAPI, SQLAlchemy, SQLite</li>
  <li><strong>前端</strong>: React, TypeScript, Vite</li>
  <li><strong>机器人</strong>: Discord.py</li>
  <li><strong>AI</strong>: OpenAI API, Claude API</li>
  <li><strong>基础设施</strong>: Docker, Docker Compose</li>
</ul>
</div>

<h2 data-lang="en">Progress</h2>
<h2 data-lang="zh" style="display: none;">进度</h2>

<div data-lang="en">
<ul>
  <li><input type="checkbox" checked disabled> Discord Bot with slash commands</li>
  <li><input type="checkbox" checked disabled> Multi-source collectors (Git, Terminal, Claude, OpenCode, Codex)</li>
  <li><input type="checkbox" checked disabled> Reminder scheduler with DM notifications</li>
  <li><input type="checkbox" checked disabled> Dashboard backend API</li>
  <li><input type="checkbox" disabled> Dashboard frontend (in progress)</li>
  <li><input type="checkbox" disabled> AI-powered memory retrieval</li>
  <li><input type="checkbox" disabled> Natural language queries</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li><input type="checkbox" checked disabled> Discord Bot（带斜杠命令）</li>
  <li><input type="checkbox" checked disabled> 多数据源收集器（Git、Terminal、Claude、OpenCode、Codex）</li>
  <li><input type="checkbox" checked disabled> 提醒调度器（DM通知）</li>
  <li><input type="checkbox" checked disabled> Dashboard 后端 API</li>
  <li><input type="checkbox" disabled> Dashboard 前端（进行中）</li>
  <li><input type="checkbox" disabled> AI 驱动的记忆检索</li>
  <li><input type="checkbox" disabled> 自然语言查询</li>
</ul>
</div>

<h2 data-lang="en">Why Paused</h2>
<h2 data-lang="zh" style="display: none;">为什么暂停</h2>

<div data-lang="en">
<ul>
  <li>Time constraints</li>
  <li>Pivoted to other projects</li>
  <li>Core functionality works for personal use</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li>时间限制</li>
  <li>转向其他项目</li>
  <li>核心功能已满足个人使用需求</li>
</ul>
</div>

<h2 data-lang="en">Architecture</h2>
<h2 data-lang="zh" style="display: none;">架构</h2>

<pre><code data-lang="en">Collectors → SQLite → Dashboard
                 ↓
            Discord Bot
                 ↓
            Scheduler (Reminders)</code>
<code data-lang="zh" style="display: none;">收集器 → SQLite → Dashboard
               ↓
          Discord Bot
               ↓
          调度器（提醒）</code></pre>

<h2 data-lang="en">Key Decisions</h2>
<h2 data-lang="zh" style="display: none;">关键决策</h2>

<h3 data-lang="en">Why Discord Bot?</h3>
<h3 data-lang="zh" style="display: none;">为什么选 Discord Bot？</h3>

<p data-lang="en">I'm already on Discord. Lower friction than a separate app.</p>
<p data-lang="zh" style="display: none;">我本来就常用 Discord。比单独的 App 更方便。</p>

<h3 data-lang="en">Why SQLite?</h3>
<h3 data-lang="zh" style="display: none;">为什么选 SQLite？</h3>

<p data-lang="en">Simpler for personal tool. Can migrate to PostgreSQL if needed.</p>
<p data-lang="zh" style="display: none;">个人工具用这个够简单。需要时可以迁移到 PostgreSQL。</p>

<h3 data-lang="en">Why Multiple Collectors?</h3>
<h3 data-lang="zh" style="display: none;">为什么多个收集器？</h3>

<p data-lang="en">Different sources have different formats. Separate collectors allow independent parsing logic.</p>
<p data-lang="zh" style="display: none;">不同数据源格式不同。分离收集器让解析逻辑独立。</p>

<h2 data-lang="en">Lessons Learned</h2>
<h2 data-lang="zh" style="display: none;">经验教训</h2>

<div data-lang="en">
<ol>
  <li><strong>Start with one collector</strong> - I built multiple collectors too early, should have validated with one first</li>
  <li><strong>Discord Bot is great for personal tools</strong> - Instant notifications, already integrated in daily life</li>
  <li><strong>SQLite is enough</strong> - Don't over-engineer for scale you don't need</li>
</ol>
</div>
<div data-lang="zh" style="display: none;">
<ol>
  <li><strong>先从一个收集器开始</strong> - 我太早做了多个，应该先用一个验证</li>
  <li><strong>Discord Bot 适合个人工具</strong> - 即时通知，已融入日常生活</li>
  <li><strong>SQLite 够用</strong> - 不要为你不需要的规模过度设计</li>
</ol>
</div>

<h2 data-lang="en">Related Problems</h2>
<h2 data-lang="zh" style="display: none;">相关问题</h2>

<ul>
  <li>P001: <span data-lang="en">NLP intent parsing for reminders</span><span data-lang="zh" style="display: none;">提醒的 NLP 意图解析</span></li>
  <li>P002: <span data-lang="en">Deduplication of collected events</span><span data-lang="zh" style="display: none;">收集事件的去重</span></li>
</ul>

<h2 data-lang="en">Future</h2>
<h2 data-lang="zh" style="display: none;">未来计划</h2>

<div data-lang="en">
<p>Would continue if:</p>
<ul>
  <li>I need more sophisticated memory retrieval</li>
  <li>I want to share with others (would need multi-tenancy)</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p>以下情况会继续：</p>
<ul>
  <li>需要更复杂的记忆检索</li>
  <li>想分享给他人使用（需要多租户支持）</li>
</ul>
</div>