---
layout: default
title: "Horizon Summary: 2026-11-06 (ZH)"
date: 2026-11-06
lang: zh
---

> 从 60 条内容中筛选出 4 条重要资讯。

---

**AI 创作者雷达**
1. [聊天机器人广告商业化提速：报道称 ChatGPT 广告主超 10 万家](#item-ai-creator-1) ⭐️ 8.0/10
2. [GitHub issue 称 Claude Code 会把用户邮箱发给网站，官方尚未确认](#item-ai-creator-2) ⭐️ 7.0/10
3. [百度发布 ERNIE 5.5 Flash Base](#item-ai-creator-3) ⭐️ 7.0/10
4. [Hugging Face 作者发布 MoE 训练手册，覆盖 Megatron-LM 实操与 serving/RL](#item-ai-creator-4) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [聊天机器人广告商业化提速：报道称 ChatGPT 广告主超 10 万家](https://www.wired.com/story/ads-in-chatbots-have-arrived-heres-whats-working-and-whats-not/) ⭐️ 8.0/10

据该条目转述 WIRED 的报道，OpenAI 自 2026 年 2 月上线广告以来，ChatGPT 广告主已超过 10 万家；Google 在报道所称的“上周”将 AI Mode 广告扩展到美国以外 10 个国家；Anthropic 则仍不在 Claude 中投放广告，其 IPO 文件也未提及广告创收。条目还引用创业公司 Koah 的说法称，其为 200 多款应用提供广告、客户量约为 OpenAI 的十分之一，并称 AI 参与的广告点击率翻倍、整体约 3%。上述数字来自二手摘要，尚待原文或官方信息核验。

telegram · zaihuapd · 11月6日 03:15

**「为何值得注意」** 聊天机器人广告正从试验走向规模化投放，OpenAI、Google 与 Anthropic 的路线差异让平台变现、用户体验和广告生态同时成为观察点；但广告效果数据仍主要来自相关公司口径，实际影响尚未独立验证。

**「内容角度」** 可做角度：以“同一件事，三种选择”为线索，对比 OpenAI 扩大广告主、Google 扩展 AI Mode 广告地域、Anthropic 不在 Claude 投广告的公开立场，讨论聊天机器人广告在变现与体验之间的取舍，并把 10 万广告主、10 国扩展和 3% 点击率标注为待核验的报道口径。

**标签**: `#OpenAI`, `#ChatGPT广告`, `#AI广告商业化`, `#Google AI Mode`, `#Anthropic`

---

<a id="item-ai-creator-2"></a>
### [GitHub issue 称 Claude Code 会把用户邮箱发给网站，官方尚未确认](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 7.0/10

一个 GitHub issue（编号 \#107757）称 Claude Code 会将用户邮箱地址发送给访问的网站，该议题在 Hacker News 上引发讨论。评论中有人指出，至少 SEC 的 data.sec.gov API 会因为其文档要求 User-Agent 中包含邮箱、否则拒绝请求而触发这一行为，因此实际影响范围可能比标题所述窄得多。目前核心指控仍主要来自该 issue 与 HN 讨论，尚无 Anthropic 官方确认，也没有公开的范围界定或修复说明。受影响的场景主要是使用 Claude Code 发起网络请求、尤其是调用要求身份标识的 API 的开发者。

hackernews · motoroco · 11月5日 22:17 · [社区讨论](https://news.ycombinator.com/item?id=50385272)

**「为何值得注意」** 该议题把广泛使用的 AI 编程工具与用户身份信息外泄放在一起，讨论焦点明确且有可追查的 issue。但截至目前，已发生的只是社区围绕一个 issue 的争论与一条技术线索，是否构成产品层面的普遍行为、以及是否已有改动，均未被证实。

**「内容切入角度」** 可做角度：沿着“User-Agent 里为什么会出现邮箱”这条线索，梳理指控从 issue 标题到 SEC API 文档要求之间的落差，说明哪些环节已被评论验证、哪些仍只是推测，并提醒读者区分“工具主动外发信息”与“第三方 API 强制要求标识”这两种不同性质的问题。

**「社区讨论」** 评论中的主要分歧在于归因：varenc 表示许多人是在使用 SEC API 时看到该行为，并援引 SEC API 文档要求 User-Agent 含邮箱、否则请求被拒。grey-area 则从应然层面主张 Claude 不应在未经明确许可时接触用户数据或联网，且请求应有完整日志。另有一条评论称切换工具后工作邮箱垃圾邮件明显增多，属个人轶事，无法据此建立因果。

**标签**: `#Claude Code`, `#隐私安全`, `#AI 编程工具`, `#开发者信任`, `#HN 讨论`

---

<a id="item-ai-creator-3"></a>
### [百度发布 ERNIE 5.5 Flash Base](https://ernie.baidu.com/release/ernie-5-5-flash-base/) ⭐️ 7.0/10

百度发布 ERNIE 5.5 Flash Base，官方发布页标题可确认这一型号，但现有材料未提供模型规模、评测结果、价格或许可证全文。Hacker News 讨论中，有评论称许可证排除欧盟、英国和韩国，并要求衍生品开发者确保这些地区无人使用；该限制尚未由公告正文核实。对希望基于这个 base 模型继续训练或分发衍生模型的开发者来说，许可范围与合规责任是当前最需要确认的部分。

hackernews · pretext · 11月5日 09:29 · [社区讨论](https://news.ycombinator.com/item?id=50377078)

**「为何现在」** 当下值得注意的不是性能结论，而是“基础模型发布”与“地域限制许可”同时出现后，对下游开发者实际可用性的影响；在许可证全文和能力评测缺失前，这一影响仍不确定。

**「内容角度」** 可做角度：把“能不能用、能不能改、改了谁负责”拆成一份许可证核对清单，对照 ERNIE 5.5 Flash Base 的发布信息与社区提到的地域限制，明确哪些是已确认条款、哪些仍需查原文。

**「社区讨论」** 讨论并不一致：有人担心许可证对衍生品的限制过强，有人质疑 ERNIE 的品牌与代际感知，也有人欢迎 base 模型开放并询问多节点继续训练该用哪套工具链。关于 ERNIE 4 的实际体验被描述为“直接、不绕弯”，但这属于个人回顾，不能当作模型能力结论。

**标签**: `#Baidu`, `#ERNIE`, `#base model`, `#开源许可证`, `#AI 开发者工具`

---

<a id="item-ai-creator-4"></a>
### [Hugging Face 作者发布 MoE 训练手册，覆盖 Megatron-LM 实操与 serving/RL](https://www.reddit.com/r/MachineLearning/comments/1xorgq0/the_ultimate_moe_training_handbook_training/) ⭐️ 7.0/10

Hugging Face 的 Nouamane（曾参与 Ultra-Scale 与 Smol Training Playbooks）发布了一份面向已训练过 dense 模型、想进一步训练 MoE 的开发者的手册，核心是用 Megatron-LM 跑通流程。手册第 2 章给出硬件测试、镜像构建、dense baseline 与单节点首个 MoE 对比的 runbook；第 3 章拆解 router、路由、负载均衡、专家与 block 布局等，第 4 章延伸到 serving 和 RL，其中第 3、4 章无需 GPU。作者称经验来自 CSCS 的 Alps 集群上约 80 万 GH200 GPU 小时，并区分自测结果、前沿模型论文/配置/代码引用与标注过的玩具模拟。随手册发布的还有 55 张图的 gallery、脚本，以及汇总推荐 flag 的单个 Megatron-LM 配置块。

reddit · r/MachineLearning · /u/Norlax\_42 · 11月5日 19:13

**「为什么现在值得注意」** 材料显示手册及相关脚本、图表已发布，价值在于把 MoE 训练从 Megatron-LM 实操到 serving/RL 串成可查阅的流程；但它是否适用于特定集群与模型规模，材料未给出独立验证。

**「可做角度」** 可做角度：从“已训练 dense 模型，下一步如何用 Megatron-LM 跑通首个单节点 MoE”切入，按手册第 2 章的硬件测试、镜像构建、dense baseline、单节点 MoE 对比流程拆解，并明确标注哪些是作者自测、哪些是引用前沿模型论文或玩具模拟。

**标签**: `#MoE`, `#Megatron-LM`, `#模型训练`, `#Hugging Face`, `#技术教程`

---