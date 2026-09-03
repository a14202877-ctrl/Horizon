---
layout: default
title: "Horizon Summary: 2026-09-03 (ZH)"
date: 2026-09-03
lang: zh
---

> 从 79 条内容中筛选出 7 条重要资讯。

---

**AI 创作者雷达**
1. [Gemini 3.8 Flash 与 3.8 Flash Cyber 发布](#item-ai-creator-1) ⭐️ 9.0/10
2. [llm-gemini 0.34 发布：新增支持 Gemini 3.8 Flash 及三档思考等级](#item-ai-creator-2) ⭐️ 9.0/10
3. [Meta 发布 Muse Spark 1.3，社区实测称价格便宜且 SVG 输出更稳](#item-ai-creator-3) ⭐️ 8.0/10
4. [三网站批量生成 21.5 万个推荐页，报告称 Perplexity 直接引用](#item-ai-creator-4) ⭐️ 8.0/10
5. [Claude 系统提示词更新：更明确拒绝复制歌词并限制版权图像](#item-ai-creator-5) ⭐️ 7.0/10
6. [Paint.NET 为 WINE 加入约 18 万行由 Claude 逆向重写的 Direct2D 实现](#item-ai-creator-6) ⭐️ 7.0/10
7. [Jasper Research 发布从零训练文本到图像模型教程及 1 亿图像数据集](#item-ai-creator-7) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [Gemini 3.8 Flash 与 3.8 Flash Cyber 发布](https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/) ⭐️ 9.0/10

Google DeepMind 发布了 Gemini 3.8 Flash 和 Gemini 3.8 Flash Cyber，并在博客与 DeepMind 模型卡页面中给出说明。社区首批反馈主要集中在这两个模型的生成速度与成本：有开发者用一个约 1.8 美分、耗时 13 秒的示例，从提示词“make me a cool thing in html”生成了网页；也有人提到它在第三方智能评分上达到与 Opus 5 medium 相同的分数，但对真实使用体验仍持保留态度。开发者、前端原型和媒体分析类场景可能最先受到关注。

hackernews · bratao · 9月2日 15:12 · [社区讨论](https://news.ycombinator.com/item?id=49537553)

**「为什么现在值得注意」** 这是 Google DeepMind Flash 系列的新版本发布，官方页面与社区评测几乎同步出现，属于当下可观察的模型更新话题。已发生的变化是模型卡上线、第三方榜单已有排名；尚未证实的是它能否在更复杂的真实项目中稳定替代现有旗舰模型。

**「内容角度」** 可做角度：以“Flash 模型跑出与旗舰相当的榜单分数，但实际体验仍需验证”为张力，整理 Gemini 3.8 Flash 在第三方基准和开发者生成测试中的表现，重点讨论低价、高速的前端 HTML/JavaScript 生成会给原型制作带来什么变化；避免把它包装成对现有工作流的必然替代或明确产品建议。

**「社区讨论」** 社区评论普遍认可 Gemini 3.8 Flash 的速度和成本，尤其对 HTML/JavaScript 生成给出了正面示例。分歧在于：有人说它在第三方榜单上“超过 Opus 5”或智能分持平，但“用起来怎么样还不好说”；也有人对比上一代 3.7 后认为 3.8 的低思考档位出现回退。多位评论者同时强调，Gemini 的音频/视频多模态输入仍是相对 OpenAI 和 Anthropic 图片输入方案的差异点。

**标签**: `#Gemini`, `#Google DeepMind`, `#AI模型发布`, `#编程助手`, `#AI成本`

---

<a id="item-ai-creator-2"></a>
### [llm-gemini 0.34 发布：新增支持 Gemini 3.8 Flash 及三档思考等级](https://simonwillison.net/2026/Sep/2/llm-gemini/) ⭐️ 9.0/10

llm-gemini 0.34 已发布，新增对 Google 新模型 gemini-3.8-flash 的支持，并提供 low、medium、high 三档思考等级。Google 当天正式发布 Gemini 3.8 Flash，还公开了仅限受信防御者使用的 3.8 Flash Cyber。开发者 Simon Willison 在发布说明中用该模型生成并对比了不同思考等级的示例图，并记录了一次“用 HTML 做个酷东西”的实测：耗时约 13 秒、花费 1.8 美分。他还用 Gemini 3.8 Flash 配合自研编码代理，为自己的 markdown-svg-renderer 工具加入了 HTML 渲染支持。

rss · Simon Willison · 9月2日 16:39

**「为什么现在值得关注」** 该版本在 Google 发布 Gemini 3.8 Flash 当天上线，属于模型更新与第三方工具同步跟进的关键节点。Flash 系列以快速、低成本著称，但新模型在不同思考等级下的实际表现差异，仍需更多独立测试来验证。

**「内容角度」** 可做角度：围绕 Simon Willison 用 Gemini 3.8 Flash 在 13 秒、1.8 美分内完成一个 HTML 互动页面的实测，写一篇关于“Flash 系列在便宜、快、能写前端代码”方向的体验记录，同时说明 llm-gemini 0.34 已经加入三档思考等级可供开发者选用。

**标签**: `#Gemini 3.8 Flash`, `#Google`, `#llm-gemini`, `#模型发布`, `#开发者工具`

---

<a id="item-ai-creator-3"></a>
### [Meta 发布 Muse Spark 1.3，社区实测称价格便宜且 SVG 输出更稳](https://developer.meta.com/ai/models/muse-spark/) ⭐️ 8.0/10

Meta 通过研究博客发布 Muse Spark 1.3，并更新了面向开发者的模型页面；本次材料未注明具体发布日期。社区记录中，一次生成 SVG 的调用花费 4.2266 美分、耗时 38 秒，评论者对比 Muse Spark 1.2 后认为 1.3 的自行车架、翅膀和帽子等细节更好，也更愿意遵守“不要动画化”这类要求。另有评论称它在 DeepSWE 上拿到 75.4 分并暂列榜首，不过这条基准传闻尚未在本次材料中出现官方佐证。

hackernews · bvaldivielso · 9月2日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49541256)

**「为什么现在值得注意」** Muse Spark 1.3 刚发布，社区已经在同一时间把它和 Google Gemini 3.8 Flash 等模型放在成本与基准的比较语境里讨论。已发生的变化是模型版本更新和可调用入口出现；尚未证实的影响是它是否真的在综合基准上领先，以及是否引发价格竞争。

**「内容切入点」** 可做角度：以评论者实测的“鹈鹕骑自行车”SVG 为例，对比 Muse Spark 1.3 与 1.2 在同样提示下的输出差异，讨论这类非顶尖、但价格很低的模型在开发辅助和原型工作中究竟够不够用。

**「社区讨论」** 评论区对低价开发用模型的接受度较高：有人从 1.2 开始使用并感到惊喜，也有人认为把“允许训练”与更低价格明确挂钩的做法值得推广。分歧集中在开源承诺上：有用户仍在等待 Meta 兑现 Muse Spark 1.2 的权重发布；关于 DeepSWE 登顶的说法属于单一评论，不宜直接当作已确认结论。

**标签**: `#Meta`, `#Muse Spark`, `#模型发布`, `#开发者工具`, `#AI成本`

---

<a id="item-ai-creator-4"></a>
### [三网站批量生成 21.5 万个推荐页，报告称 Perplexity 直接引用](https://trellner.com/reports/manufactured-sources-behind-ai-recommendations/) ⭐️ 8.0/10

一份发布于 trellner.com 的报告称，三个网站制造了 215,128 个“最佳软件”页面，并被 AI 搜索工具 Perplexity 引用。报告认为，这种现象暴露了 AI 驱动推荐在来源可信度上的漏洞：AI 可能把批量生产的推荐页当作真实用户评价。现有材料未提供报告原文细节，也没说明这三个网站名称、页面被抓取的时间范围，或这些引用占 Perplexity 结果的比例。

hackernews · jakobgreenfeld · 9月2日 13:59 · [社区讨论](https://news.ycombinator.com/item?id=49536375)

**「当下为何值得注意」** 这篇报告被提交到 Hacker News 后，已有评论者称这是首页近期第三篇针对 Perplexity 的批评帖，显示 AI 搜索引用可信度正在被持续讨论。不过，帖子内容是否构成“系统性攻击”只是社区中的观察；目前能确认的，是报告披露了数十万个批量页面曾被 AI 工具引用这一案例。

**「内容角度」** 可做角度：以“21.5 万个批量制造的推荐页被 Perplexity 引用”为起点，解释 AI 搜索在引用机制上缺乏来源审查的具体表现，并梳理用户判断 AI 推荐是否可信时应注意的信号。角度应围绕报告披露的事实展开，不延伸到投资或产品建议。

**「社区讨论」** 评论中较多用户同意 AI 模型和搜索工具对来源不够怀疑：有用户称自己让 Claude、Codex 搜索时遇到过生成的网站，也有用户觉得 Perplexity 为了速度牺牲了结果质量。另有用户提出反向怀疑，认为这类帖子连续批评 Perplexity，其本身也可能成为未来 LLM 引用素材。

**标签**: `#AI search`, `#content farming`, `#Perplexity`, `#AI-generated content`, `#misinformation`

---

<a id="item-ai-creator-5"></a>
### [Claude 系统提示词更新：更明确拒绝复制歌词并限制版权图像](https://simonwillison.net/2026/Sep/2/claudes-new-system-prompt/) ⭐️ 7.0/10

Anthropic 在官方文档中公开了 Claude 消费端（Claude.ai 与移动应用）的系统提示词，并把原来的单一页面重组为索引页和按模型区分的页面，还支持给页面加 .md 获取 Markdown，方便对比历史版本。报道重点对比了 Fable 5 与 Fable 5.1：新版新增了较长的“不复制歌词、诗歌、书籍和文章段落”限制，包括整段、最后一句、副歌、逐音符旋律，以及用户分次粘贴自称原创的内容；同一对话中拒绝后还会继续拒绝改写版本，并会转而提供描述或分析。针对图像生成，新版也禁止用 SVG、CSS、HTML 等方式绘制受版权保护的角色、标志或特定设计，并给出“蓝色刺猬生日横幅”的示例。报道称这些新增内容出现在索尼音乐出版与华纳查普尔起诉 Anthropic 使用歌词库训练模型的消息传出后数天内，但并未证实两者有直接因果关系。

rss · Simon Willison · 9月2日 14:16

**「为什么现在值得注意」** 已然可见的变化是，Claude 消费端的版权边界在系统提示词层面变得更强硬，且提示词文档本身更易追踪和 diff。报道指出 Fable 5.1 的更新与索尼/华纳歌词版权诉讼报道在时间上接近，但目前只能视为作者猜测，尚未有材料证实这次提示词改动是直接回应诉讼。

**「内容角度」** 可做角度：以新版系统提示词中“蓝刺猬生日横幅”的示例为切入口，结合用户实际追问，解释 Claude 如何从描述中识别版权角色、选择拒绝并提供原创替代设计；再对比生成式 AI 产品对文本和图像版权的不同限制方式，讨论大模型厂商在哪一层面设置版权防线。

**标签**: `#Claude`, `#Anthropic`, `#系统提示词`, `#AI版权`, `#内容政策`

---

<a id="item-ai-creator-6"></a>
### [Paint.NET 为 WINE 加入约 18 万行由 Claude 逆向重写的 Direct2D 实现](https://simonwillison.net/2026/Sep/2/rick-brewster/) ⭐️ 7.0/10

Paint.NET 作者 Rick Brewster 在论坛帖子中宣布，Paint.NET 新增了一个在 WINE/Linux 上使用的 Direct2D 实现。这个实现存放在 PaintDotNet.Windows.Direct2D1.Managed.dll，由 Claude 从零开始、洁净室式逆向重写，规模约 18 万行代码，通过 /wine 参数触发。Rick 表示 Direct2D 一直是 Paint.NET 在 WINE 上的最大障碍，并形容该功能“极度实验性”；他承认大部分代码属于“vibe coded”，未经充分审查，而 Paint.NET 其余代码约 70 万行，是他 20 多年来积累的成果。

rss · Simon Willison · 9月2日 05:50

**「为什么现在值得注意」** 这是一个具体的大规模 AI 编程案例：Claude 在真实桌面应用中生成了约 18 万行兼容代码，并被作者用于解决长期未完成的 WINE 支持问题。目前该功能仍是实验性的，且作者明确表示代码未经充分审查，真正的产品影响还有待验证。

**「可做角度」** 可做角度：以 Paint.NET 的 18 万行“vibe coded”代码为样本，讨论 AI 编写大规模兼容代码进入真实项目时，作者作为维护者如何描述收益与风险，包括资源管理错误、需要“盯梢”纠正设计，以及在无法逐行审查的情况下如何划定实验边界。

**标签**: `#Paint.NET`, `#Claude`, `#AI代码生成`, `#WINE`, `#Direct2D`

---

<a id="item-ai-creator-7"></a>
### [Jasper Research 发布从零训练文本到图像模型教程及 1 亿图像数据集](https://www.reddit.com/r/MachineLearning/comments/1w5c9rd/detailed_explanation_of_how_to_create_a/) ⭐️ 7.0/10

Jasper Research 发布了一份从零构建文本到图像模型的 cookbook，公开了背后的完整推理过程和中间结果，并附带了名为 monet 的 1 亿图像数据集，以及名为 nano-t2i 的轻量代码库。教程以交互式报告形式托管在 Hugging Face Spaces，代码库位于 GitHub，数据集托管在 Hugging Face Datasets。它面向希望深入理解文本到图像模型、或想从零训练一个小型模型的开发者。目前没有看到社区评论或第三方验证结果。

reddit · r/MachineLearning · /u/dh7net · 9月2日 14:40

**「为什么现在值得注意」** 这是一份刚发布的开源教学资源，把教程、代码库和数据集同时提供出来，降低了从零复现文本到图像模型的门槛。需要注意的是，它属于教育性内容发布，并不代表某个前沿模型的能力更新。

**「可做内容角度」** 可做角度：拆解 Jasper Research 这条“从零训练文本到图像模型”的公开路径——教程覆盖了哪些环节、nano-t2i 代码库规模如何，以及 1 亿图像数据集在实际训练流程中承担什么角色。

**标签**: `#text-to-image`, `#教程`, `#开源项目`, `#数据集`, `#生成模型`

---