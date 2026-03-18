---
layout: post
title: Expense Tracker (记账)
date: 2026-03-18
tags: [ios, ocr, finance, swift]
status: paused
---

<h2 data-lang="en">Why I Build This</h2>
<h2 data-lang="zh" style="display: none;">为什么做这个</h2>

<div data-lang="en">
<p>French banking apps have problems that drive me crazy:</p>
<ol>
  <li><strong>Unreliable balance</strong> — Transactions appear but aren't actually deducted. I once saw €100 available, couldn't even spend €10.</li>
  <li><strong>Dumb categorization</strong> — I spent an hour manually categorizing one month. Next month? Same stores, no auto-categorization. Useless.</li>
  <li><strong>Cryptic merchant names</strong> — Unlike Alipay in China, French banks show obscure codes. I have to Google each one.</li>
  <li><strong>Internal transfers counted as expense</strong> — Moving money between my own accounts shows as "income" and "expense". Not objective.</li>
</ol>
<p>I need a tool that tells me <strong>how much money I actually have</strong>.</p>
</div>
<div data-lang="zh" style="display: none;">
<p>法国银行软件有几个让我抓狂的问题：</p>
<ol>
  <li><strong>余额不可靠</strong> — 交易显示出来了但其实没扣。我曾经看到余额 €100，结果 €10 都刷不出来。</li>
  <li><strong>分类不智能</strong> — 我花了一小时手动归类一个月的消费。下个月？同一家店，照样不自动归类。没用。</li>
  <li><strong>商户名看不懂</strong> — 不像国内的支付宝会告诉你是什么店，法国银行只显示一串代码。每次都得自己搜。</li>
  <li><strong>内部转账算收支</strong> — 自己账户间转账被记为"收入"和"支出"。不客观。</li>
</ol>
<p>我需要一个工具，告诉我<strong>卡里实际还有多少钱</strong>。</p>
</div>

<hr>

<h2 data-lang="en">The Goal</h2>
<h2 data-lang="zh" style="display: none;">目标</h2>

<div data-lang="en">
<p><strong>Vision</strong>: Effortless expense tracking on iOS.</p>
<p>The ideal state:</p>
<ul>
  <li>Capture expenses via Apple Pay notifications + bank app screenshots</li>
  <li>Auto-import from <em>relevé</em> (French bank statement file)</li>
  <li>Know the <strong>real balance</strong> — not the fake one banks show</li>
  <li>Auto-categorize, detect recurring payments, match deposits and refunds</li>
</ul>
<p><strong>Safety first</strong>: If I can't guarantee security, this stays personal-use only. No product release.</p>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>愿景</strong>：iOS 无感记账。</p>
<p>理想状态：</p>
<ul>
  <li>通过 Apple Pay 弹窗 + 银行 app 截图捕获消费</li>
  <li>从 <em>relevé</em>（法国银行账单文件）自动导入</li>
  <li>知道<strong>真实余额</strong> — 不是银行显示的那个假数字</li>
  <li>自动分类、检测周期消费、配对押金和退款</li>
</ul>
<p><strong>安全优先</strong>：如果不能保证安全性，就只做个人使用，不发布产品。</p>
</div>

<hr>

<h2 data-lang="en">How It Works</h2>
<h2 data-lang="zh" style="display: none;">工作原理</h2>

<div data-lang="en">
<p><strong>The baseline approach</strong>:</p>
<ol>
  <li>Start from <em>relevé</em>'s last date + balance as <strong>baseline</strong></li>
  <li>OCR all screenshots from that date forward</li>
  <li>Baseline + transactions = <strong>calculated balance</strong></li>
  <li>Compare with latest screenshot → detect pending transactions, missing income</li>
</ol>
<p><strong>Smart features</strong>:</p>
<ul>
  <li>Auto-categorize same merchant</li>
  <li>Detect monthly recurring expenses</li>
  <li>Match deposits with refunds (e.g., hotel deposits)</li>
  <li>Alert if deposit not returned</li>
  <li>Pre-enter known upcoming expenses</li>
  <li>Deduplication (OCR might capture same receipt twice)</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>基线方法</strong>：</p>
<ol>
  <li>以 <em>relevé</em> 的最后日期 + 余额作为<strong>基线</strong></li>
  <li>OCR 处理从那个日期起的所有截图</li>
  <li>基线 + 交易 = <strong>计算余额</strong></li>
  <li>和最新截图对比 → 检测未扣款、未入账收入</li>
</ol>
<p><strong>智能功能</strong>：</p>
<ul>
  <li>同一商户自动归类</li>
  <li>检测每月固定消费</li>
  <li>配对押金和退款（比如酒店押金）</li>
  <li>提醒押金未退</li>
  <li>预输入已知即将发生的消费</li>
  <li>去重（OCR 可能重复捕获同一张单据）</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Current Status</h2>
<h2 data-lang="zh" style="display: none;">当前状态</h2>

<div data-lang="en">
<p><strong>Status</strong>: Paused</p>
<p><strong>Blocker</strong>: The calculation logic keeps failing.</p>
<p>Every test run wastes API credits (using Anthropic for OCR). The math doesn't add up — calculated balance never matches screenshot.</p>
<p><strong>Need to solve</strong>:</p>
<ul>
  <li>Cheaper OCR alternative (Anthropic is expensive for this use case)</li>
  <li>Reliable calculation algorithm</li>
  <li>Better test methodology without burning API credits</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>状态</strong>：暂停</p>
<p><strong>卡点</strong>：计算逻辑一直算不对。</p>
<p>每次测试都浪费 API 费用（用 Anthropic 做 OCR）。算出来的余额永远对不上截图。</p>
<p><strong>需要解决</strong>：</p>
<ul>
  <li>更便宜的 OCR 方案（Anthropic 做这个太贵）</li>
  <li>可靠的计算算法</li>
  <li>更好的测试方法，不用烧 API 钱</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Tech Stack</h2>
<h2 data-lang="zh" style="display: none;">技术栈</h2>

<div data-lang="en">
<p><strong>Not decided yet</strong>. Initial thoughts:</p>
<ul>
  <li><strong>Platform</strong>: iOS (Swift/SwiftUI)</li>
  <li><strong>OCR</strong>: ? (Anthropic too expensive, need alternative)</li>
  <li><strong>Data source</strong>: Apple Pay notifications, bank app screenshots, relevé files</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<p><strong>未定</strong>。初步想法：</p>
<ul>
  <li><strong>平台</strong>：iOS (Swift/SwiftUI)</li>
  <li><strong>OCR</strong>：？（Anthropic 太贵，需要替代方案）</li>
  <li><strong>数据源</strong>：Apple Pay 弹窗、银行 app 截图、relevé 文件</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Open Questions</h2>
<h2 data-lang="zh" style="display: none;">待解决问题</h2>

<div data-lang="en">
<ul>
  <li><strong>Security vs convenience</strong>: How to do "effortless" without exposing financial data?</li>
  <li><strong>OCR cost</strong>: Is there a cheaper alternative that handles French receipts well?</li>
  <li><strong>Calculation logic</strong>: Why does the math keep failing? Edge cases I'm missing?</li>
  <li><strong>Apple Pay access</strong>: Can iOS apps read Apple Pay transaction notifications?</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li><strong>安全 vs 便利</strong>：如何实现"无感"又不暴露财务数据？</li>
  <li><strong>OCR 成本</strong>：有没有更便宜的方案能处理法文收据？</li>
  <li><strong>计算逻辑</strong>：为什么算出来老是不对？有什么边界情况漏了？</li>
  <li><strong>Apple Pay 访问</strong>：iOS app 能读取 Apple Pay 交易通知吗？</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Progress</h2>
<h2 data-lang="zh" style="display: none;">进度</h2>

<div data-lang="en">
<ul>
  <li><input type="checkbox" checked disabled> Problem definition</li>
  <li><input type="checkbox" checked disabled> Data source analysis (relevé, screenshots, Apple Pay)</li>
  <li><input type="checkbox" checked disabled> Baseline calculation concept</li>
  <li><input type="checkbox" disabled> Working OCR pipeline</li>
  <li><input type="checkbox" disabled> Correct balance calculation</li>
  <li><input type="checkbox" disabled> iOS app prototype</li>
  <li><input type="checkbox" disabled> Auto-categorization</li>
</ul>
</div>
<div data-lang="zh" style="display: none;">
<ul>
  <li><input type="checkbox" checked disabled> 问题定义</li>
  <li><input type="checkbox" checked disabled> 数据源分析（relevé、截图、Apple Pay）</li>
  <li><input type="checkbox" checked disabled> 基线计算概念</li>
  <li><input type="checkbox" disabled> 可用的 OCR 管道</li>
  <li><input type="checkbox" disabled> 正确的余额计算</li>
  <li><input type="checkbox" disabled> iOS app 原型</li>
  <li><input type="checkbox" disabled> 自动分类</li>
</ul>
</div>

<hr>

<h2 data-lang="en">Related Problems</h2>
<h2 data-lang="zh" style="display: none;">相关问题</h2>

<ul>
  <li>P00?: <span data-lang="en">OCR cost optimization</span><span data-lang="zh" style="display: none;">OCR 成本优化</span></li>
  <li>P00?: <span data-lang="en">Financial data security</span><span data-lang="zh" style="display: none;">财务数据安全</span></li>
</ul>