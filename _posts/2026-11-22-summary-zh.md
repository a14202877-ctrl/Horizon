---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 60 条内容中筛选出 3 条重要资讯。

---

**AI 创作者雷达**
1. [Lean 社区帖声称黎曼猜想获形式化验证](#item-ai-creator-1) ⭐️ 8.0/10
2. [OpenRouter 披露推理提供商数据处理事件](#item-ai-creator-2) ⭐️ 8.0/10
3. [Google Gemini 将拆分历史保存与训练设置](#item-ai-creator-3) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [Lean 社区帖声称黎曼猜想获形式化验证](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 8.0/10

据条目中的 Lean community blog 与 Telegram 摘要，Levent Alpöge 于 2026 年 11 月 20 日发布黎曼猜想的 Lean 形式化证明，代码库约 1700 万行；11 月 21 日 Lean FRO 与 Mathlib Initiative 联合声明称命题与证明均正确，社区称其命题与 Mathlib 的 RiemannHypothesis 一致、代码可无错编译，并由多个独立检查器验证。Hacker News 评论把它视为一次重大的 AI 辅助形式化成果，同时围绕检查器可靠性和人类监督展开争论。不过，条目未提供原帖技术细节，评论中亦出现 GRH 表述，因此黎曼猜想与广义黎曼猜想的准确范围、以及 AI 与人类各自贡献仍待确认。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**「为何现在值得注意」** 之所以当下值得注意，是因为它把争议从“模型能否做数学”推进到“形式化检查器与人类审核能否支撑如此重大的结论”；如果上述认证细节成立，AI 数学声明的验证流程会成为关注点。但材料尚不足以确认原帖技术细节和 RH/GRH 的准确表述。

**「内容切入角度」** 可做角度：以这次 Lean 形式化验证争议为切口，拆解“检查器通过”与“数学命题被证明”之间的核验链条——目标命题是否与 Mathlib 中的 RiemannHypothesis 一致、代码库能否无错编译、多个检查器是否真正独立，以及人类专家在环审了什么。

**「社区讨论」** 评论普遍认可结果重要，并把功劳部分归于 Claude、部分归于 Levent；分歧集中在检查器可靠性：有人认为多语言、多实现及一致性证明使“证明利用漏洞”的可能性极小，也有人提醒假 Collatz 反驳曾通过某个独立检查器，检查器独立性可能被高估。另有评论指出需要人类专家在环，但同时质疑陈述中的四点并非都依赖人类参与。

**标签**: `#Lean`, `#Riemann Hypothesis`, `#AI-assisted proof`, `#formal verification`, `#Claude`

---

<a id="item-ai-creator-2"></a>
### [OpenRouter 披露推理提供商数据处理事件](https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/) ⭐️ 8.0/10

OpenRouter 发布公告，披露其推理提供商发生数据处理事件。公告标题与现有材料显示，讨论集中在数据留存、供应商审核以及零数据保留承诺；但材料未给出事件范围、受影响提供商名单和具体处置细节，相关影响仍不明确。对使用模型路由服务的开发者和用户而言，这涉及如何评估下游提供商的数据处理与信任边界。

hackernews · sdko · 11月22日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50595554)

**「当下关注点」** 该公告在 Hacker News 引发讨论，焦点是模型路由平台如何审核下游推理提供商以及如何说明数据留存风险；材料未提供事件时间线或整改结果，实际影响范围仍不明确。

**「内容角度」** 可做角度：从 OpenRouter 的公告出发，梳理模型路由平台在“平台—推理提供商—最终用户”链条中的数据处理责任边界，并区分公告已确认的信息、社区推测与仍待补充的细节。

**「社区讨论」** 评论中多位用户对推理提供商的数据留存承诺持怀疑，认为应默认数据可能被记录；一名自称受影响的用户称仅一条提示受影响、影响不大，但更担忧“提供商”本身。

**标签**: `#OpenRouter`, `#数据隐私`, `#推理提供商`, `#AI 基础设施`, `#供应商信任`

---

<a id="item-ai-creator-3"></a>
### [Google Gemini 将拆分历史保存与训练设置](https://blog.google/innovation-and-ai/products/gemini-app/updated-controls/) ⭐️ 7.0/10

Gemini 团队通知称，将在未来几周内用两项独立设置取代 Gemini 应用的“保留活动记录”：一项控制历史记录保存时长，另一项单独决定对话内容（含文字与附件）是否可用于训练生成式 AI 模型，因此用户可以保留记录但关闭训练授权。通知还称，变更生效时两项设置会按原开关状态同步开关；关闭历史记录后，新的 Gemini 对话约保存 2 个月，并可能在人工审核员协助下用于回复、处理反馈及保护 Google、Google 用户和公众。音频与 Gemini Live 录音默认仍不用于改进 Google 服务。

telegram · zaihuapd · 11月22日 01:24

**「为何值得注意」** 值得注意之处在于，隐私控制从单一的“保留活动记录”拆成历史保存与训练授权两项，用户可以在保留聊天记录的同时单独关闭训练用途。目前这仍是计划中的设置调整，实际推送节奏尚待观察。

**「内容角度」** 可做角度：围绕“保留聊天记录但关闭训练授权”这一具体变化，做一篇设置说明，逐项解释历史记录保存时长与训练用途开关分别影响什么，并说明变更生效时两项设置会按原开关状态同步。

**标签**: `#Google Gemini`, `#privacy settings`, `#model training data`, `#product update`, `#user control`

---