---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 65 条内容中筛选出 3 条重要资讯。

---

**AI 创作者雷达**
1. [用 Lovable 构建的应用被曝泄露护照信息与逾 20 万条私信](#item-ai-creator-1) ⭐️ 8.0/10
2. [Cloudflare 开源 AI 代理浏览器 Kitesurf](#item-ai-creator-2) ⭐️ 8.0/10
3. [Google Research 展示 Antigravity /teamwork 科研工程案例](#item-ai-creator-3) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [用 Lovable 构建的应用被曝泄露护照信息与逾 20 万条私信](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

安全研究者披露，用 Lovable 构建的应用暴露了护照信息和超过 20 万条私信，问题很大程度上指向 Supabase 行级安全（RLS）配置不足。Lovable 安全负责人回应称，这些应用的根因是 RLS 不足，并称平台会在发布前自动扫描应用，提供更深入的 SAST 扫描以及修复选项。具体受影响应用数量、数据范围和修复细节仍需结合研究者披露与厂商说明判断。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**「为何现在」** 文章作者称，该披露两周前提交到 Hacker News 时未获多少关注，此次重新提交后，Lovable 安全负责人也在讨论中回应了根因与修复机制。

**「内容角度」** 可做角度：围绕“AI 生成应用的默认安全该由谁兜底”，把研究者披露的 RLS 不足导致护照信息与私信暴露，和 Lovable 安全负责人所说的发布前扫描、SAST、自动修复放在一起对照，追问默认配置、平台扫描与开发者责任各自覆盖到什么程度。

**「社区讨论」** 讨论对责任归属存在分歧：有评论认为 Supabase 的默认配置也应承担部分责任，并称相关默认值修复对既有项目可能仍未生效；Lovable 安全负责人则强调 RLS 不足是根因，并介绍扫描与修复机制。也有评论认为 AI 生成应用数量多、攻击门槛低，平台应采用默认拒绝的数据库权限等更安全的默认设置。

**标签**: `#AI app builder security`, `#Lovable`, `#Supabase RLS`, `#data exposure`, `#vibe coding`

---

<a id="item-ai-creator-2"></a>
### [Cloudflare 开源 AI 代理浏览器 Kitesurf](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 8.0/10

Cloudflare 以 Apache 2.0 协议开源了面向 AI 代理的无状态浏览器 Kitesurf，代码已发布在 GitHub。它基于 Cloudflare Workers 构建，无需浏览器容器即可解析 HTML、处理 CSS 并执行 JavaScript，目标是让 AI 代理以更轻量的方式访问网页并按需扩展。Cloudflare 还宣称其相比 Chromium 占用更少 CPU 和内存，但材料未提供基准、版本、成熟度或限制说明，这一性能对比目前只能视为公司主张。

telegram · zaihuapd · 11月14日 09:33

**「内容角度」** 可做角度：从“无状态、无需浏览器容器”的 Workers 架构切入，梳理 Kitesurf 对 AI 代理网页自动化的公开定位与潜在适用场景，并把“比 Chromium 更省 CPU/内存”明确标注为 Cloudflare 单方说法，等待基准和限制披露。

**标签**: `#Cloudflare`, `#AI 代理`, `#开源`, `#浏览器自动化`, `#Serverless`

---

<a id="item-ai-creator-3"></a>
### [Google Research 展示 Antigravity /teamwork 科研工程案例](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) ⭐️ 7.0/10

Google Research 博客发文展示 Antigravity 的 /teamwork 功能在科学与工程任务中的协作案例。现有材料未包含原文细节，具体任务、性能与成本数据无法从帖子本身核实。对关注 AI 编程和多智能体工作流的开发者而言，这是一份官方应用案例，但缺少可复现的评测细节；HN 讨论则把焦点放在多智能体协作的成本、上下文重复和上手门槛上。

hackernews · acossta · 11月14日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=50496811)

**「为何现在」** 这不是一次全新的功能发布：评论指出 /teamwork 的部分内容此前已在 Antigravity 博客公布，本文的作用是补充科研与工程场景的案例。与此同时，HN 的讨论转向多智能体协作的成本与上下文管理，但这些体验来自其他工具，不能直接当作 /teamwork 的实测结论。

**「内容角度」** 可做角度：对照官方 showcase 与 HN 反馈，拆解多智能体协作在科研/工程任务中的价值主张和落地摩擦——哪些环节靠角色分工获益，哪些成本（上下文重复、token、存储）容易被案例叙述忽略，以及用户为什么仍觉得“没讲怎么用”。

**「社区讨论」** 评论区分歧大于共识：一位用户称在用 oh-my-claudecode 的 teams 选项时，工作完成质量好且耗时更短，但因各 agent 重复上下文，Max 20x 套餐的周 token 约两天耗尽，worktree 也占满硬盘；另一位评论者则质疑 /teamwork 与 Claude 动态工作流差异不明、Antigravity 作为 harness 缺少 auto 模式，并认为帖子没讲清使用方法。还有评论指出官方此前已发布过 /teamwork 的部分内容，本文更像案例展示。

**标签**: `#Google Antigravity`, `#多智能体协作`, `#AI 编程`, `#科研自动化`, `#开发者工具`

---