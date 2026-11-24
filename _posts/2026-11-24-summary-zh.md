---
layout: default
title: "Horizon Summary: 2026-11-24 (ZH)"
date: 2026-11-24
lang: zh
---

> 从 74 条内容中筛选出 5 条重要资讯。

---

**AI 创作者雷达**
1. [GLM-5.4 发布：Z.ai 首个循环 Transformer 模型](#item-ai-creator-1) ⭐️ 8.0/10
2. [百度称开源文心 5.5 Flash Preview，280B MoE 与 Apache 2.0](#item-ai-creator-2) ⭐️ 8.0/10
3. [vLLM 0.32.0 通过插件 Day-0 支持 ERNIE 5.5 Flash Preview](#item-ai-creator-3) ⭐️ 7.0/10
4. [新加坡总理表态：不容新加坡成为规避芯片管制通道](#item-ai-creator-4) ⭐️ 7.0/10
5. [诺华 CEO：AI 十年内难治愈癌症，研发周期或缩短四年](#item-ai-creator-5) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [GLM-5.4 发布：Z.ai 首个循环 Transformer 模型](https://simonwillison.net/2026/Nov/23/glm-54/) ⭐️ 8.0/10

Z.ai 发布 GLM-5.4，称其为首个采用循环 Transformer 架构的模型：一组权重共享层在一次前向中多次运行，以在不增加参数量的情况下加深网络。目前它尚未提供开放权重，且暂时无法通过常规 API 访问，作者需订阅 Coding Plan 才能调用；已有的 llm-zai 插件也尚未支持该模型。作者用 pelican 测试做了主观对比，称 5.4 与 5.3 观感相近，风格更接近 OpenAI 或 Anthropic 模型；材料未给出基准分数或编码任务实测结果。

rss · Simon Willison · 11月23日 23:40

**「为何值得注意」** 这是一周内第二次看到循环 Transformer 被提及：Thinking Machines Lab 在 11 月 20 日介绍 Inkling 2 Mini 时也采用了类似思路。架构讨论正在升温，但 GLM-5.4 的实际编码收益仍缺少公开基准和开放权重来验证。

**「内容角度」** 可做角度：围绕“循环 Transformer 是否让代码模型更强”做一次架构科普与证据核对，先解释权重共享层多次迭代如何加深网络，再对照作者可复现的 pelican 测试与 5.3 的相近表现，明确哪些是厂商主张、哪些尚无基准支撑。

**标签**: `#GLM-5.4`, `#Loop Transformer`, `#Z.ai`, `#代码模型`, `#模型架构`

---

<a id="item-ai-creator-2"></a>
### [百度称开源文心 5.5 Flash Preview，280B MoE 与 Apache 2.0](https://x.com/Baidu_Inc/status/2125077484442190137) ⭐️ 8.0/10

百度于 11 月 24 日通过官方 X 账号宣布开源文心 5.5 Flash Preview，声称其权重以 Apache 2.0 协议在 Hugging Face 和 ModelScope 开放，并可用 vLLM 或 SGLang 部署和微调。转述给出的模型规格为 MoE 架构、总参数 280B、每 token 激活 14B、上下文 1M token，且是基于 ERNIE 5.5 Flash Base 训练的首个后训练模型。流传的基准图表显示 Terminal-Bench 4.0 为 46.5 分、DeepSWE v1.1 为 71.2 分，但百度未说明是否经第三方独立验证。当前材料来自 Telegram 聚合号转述，未附 Hugging Face 或 ModelScope 仓库直链，许可证与参数仍需以仓库及模型卡为准。

telegram · zaihuapd · 11月24日 07:32

**「为何值得注意」** 这条消息在当下的价值在于：若仓库与 LICENSE 确为 Apache 2.0，280B MoE、1M 上下文和可商用许可会直接影响开发者的部署与微调选择；但在仓库直链和模型卡核验前，这一影响仍属待确认，而非已发生的事实。

**「内容角度」** 可做角度：以“可核验的开源”为主线，按仓库直链、LICENSE 是否为 Apache 2.0、模型卡的 280B/14B/1M 参数，以及 Terminal-Bench 与 DeepSWE 的评测配置逐项核对，明确哪些是百度声明、哪些仍属未验证的流传数据。

**标签**: `#开源大模型`, `#百度文心`, `#MoE 架构`, `#Apache 2.0 许可`, `#长上下文与部署`

---

<a id="item-ai-creator-3"></a>
### [vLLM 0.32.0 通过插件 Day-0 支持 ERNIE 5.5 Flash Preview](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 7.0/10

vLLM 官方博客称，已通过 vLLM-ERNIE 插件在已发布的 vllm==0.32.0 wheel 上 Day-0 支持百度 ERNIE 5.5 Flash Preview。博客列出的端到端推理加速技术包括结构感知算子融合、FlashIndexer、W4A8 QAT 和 DSpark 推测解码。该支持主要面向在 vLLM 上部署百度 ERNIE 模型的开发者和关注推理基础设施的团队；由于对象仍是 Preview，材料未提供基准数据或独立验证，实际性能影响尚不确定。

rss · vLLM Blog · 11月24日 00:00

**「为何值得注意」** 此次支持与 ERNIE 5.5 Flash Preview 同步出现，开发者可在 vllm==0.32.0 上通过插件直接尝试部署；但这是官方集成信息，材料未给出基准，实际推理加速幅度尚未证实。

**「内容角度」** 可做角度：以 vLLM-ERNIE 插件在 vllm==0.32.0 的 Day-0 支持为线索，逐项解释结构感知算子融合、FlashIndexer、W4A8 QAT 与 DSpark 推测解码各自作用于推理链路的哪个环节，并明确区分官方技术点与尚缺公开基准的性能结论。

**标签**: `#vLLM`, `#ERNIE 5.5 Flash Preview`, `#推理加速`, `#插件部署`, `#推测解码`

---

<a id="item-ai-creator-4"></a>
### [新加坡总理表态：不容新加坡成为规避芯片管制通道](https://www.bloomberg.com/news/articles/2026-11-24/singapore-won-t-be-conduit-to-skirt-us-chip-curbs-wong-says) ⭐️ 7.0/10

新加坡总理黄循财表示，不允许新加坡成为企业规避美国芯片出口管制的通道，并称当局正在调查 Megaspeed 采购英伟达芯片的交易。此前一天，美国商务部已将 Megaspeed 及另外 6 家东南亚企业列入贸易黑名单，《联邦公报》给出的理由是这些企业存在向未获授权用户转移先进计算产品的「重大风险」，名单涵盖其在马来西亚、泰国的关联实体。路透社报道称，阿里巴巴新加坡子公司 Apex Enterprise Solutions 同样在列，阿里表示从未转移受管制的先进计算芯片。上述信息来自 Telegram 对 Bloomberg 报道的摘要，具体调查进展与名单细节尚待原始报道核实。

telegram · zaihuapd · 11月24日 05:03

**「为何此时值得关注」** 新加坡总理的公开表态发生在美国商务部把 Megaspeed 等东南亚企业列入黑名单的次日，显示出口管制执法正从美国单边名单延伸到东南亚本地监管配合。目前可确认的是表态与名单本身，调查结论及对相关企业业务的实际影响尚未明确。

**「内容角度」** 可做角度：梳理这条消息里已确认的三层事实——新加坡总理的表态、美国商务部的黑名单及理由、阿里的否认——并说明「东南亚转口通道」为何成为芯片管制的执法焦点，同时标注信息目前仅来自媒体摘要、调查仍在进行。

**标签**: `#AI芯片出口管制`, `#新加坡`, `#英伟达`, `#合规与制裁`, `#东南亚AI算力`

---

<a id="item-ai-creator-5"></a>
### [诺华 CEO：AI 十年内难治愈癌症，研发周期或缩短四年](https://www.ft.com/content/1e5a9d70-221d-461d-ae03-dc235b1db340) ⭐️ 7.0/10

诺华 CEO 万思瀚（同时是 Anthropic 董事）在 FT 采访中表示，AI 不会在未来 5 到 10 年内治愈癌症；仅把药物研发周期从平均 12 年压缩到 8 年，就需要大约十年。他给出的具体判断是：人体试验前的早期发现阶段通常要 4 年，可缩短最多 2 年；进入人体试验的成功率能从 8%提到 12%，但动物实验和临床试验仍无法跳过。这与 Anthropic CEO 关于癌症等疾病将在十年内成为“历史遗迹”的说法相左，礼来 CEO 也公开表示怀疑。材料是 FT 采访的二手摘要，缺少原文细节和诺华官方公告，相关数字应视为其个人判断而非已实现结果。

telegram · zaihuapd · 11月24日 08:54

**「为何现在值得注意」** 在 AI 界对医疗前景普遍乐观的当下，这一来自大型药企 CEO 的量化判断提供了现实边界；但它仍是采访中的观点，尚不能视为诺华已经验证的研发成果。

**「内容角度」** 可做角度：把“AI 十年治愈癌症”的乐观叙事与诺华 CEO 给出的研发周期、成功率数字放在一起，讨论 AI 在药物研发中具体能压缩哪一段、哪些试验环节仍不可替代。

**标签**: `#AI制药`, `#医疗AI`, `#诺华`, `#行业观点`, `#AI预期管理`

---