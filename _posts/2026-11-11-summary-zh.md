---
layout: default
title: "Horizon Summary: 2026-11-11 (ZH)"
date: 2026-11-11
lang: zh
---

> 从 73 条内容中筛选出 5 条重要资讯。

---

**AI 创作者雷达**
1. [Chrome 发布 modern-web-guidance 1.0，引导编程代理改用现代 Web 原生 API](#item-ai-creator-1) ⭐️ 8.0/10
2. [llm-gemini 0.36 发布，Gemini 4 Carbon 开放并计划涨价](#item-ai-creator-2) ⭐️ 8.0/10
3. [Meta AI 发布 Muse Ember：面向智能体任务的小模型，短提示定价对齐竞品](#item-ai-creator-3) ⭐️ 8.0/10
4. [Anthropic 将 Claude 可用范围改为白名单制，中国大陆及港澳不在名单内](#item-ai-creator-4) ⭐️ 8.0/10
5. [稀宇科技开源 MiniMax H3 Image，厂商宣称约 10 秒生成 4K 图像](#item-ai-creator-5) ⭐️ 8.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [Chrome 发布 modern-web-guidance 1.0，引导编程代理改用现代 Web 原生 API](https://github.com/GoogleChrome/modern-web-guidance) ⭐️ 8.0/10

Google Chrome 团队发布开源指南集 modern-web-guidance 1.0，包含 200+ 篇、约 1.7MB 的 Web 实现最佳实践，目标是让编程代理默认使用 CSS.highlights、&lt;dialog&gt;/showModal\(\)、field-sizing 等平台原生能力，而不是继续沿用 div 加 JS 的旧模式。项目提供 npm 安装、search 和 legacy-scan 三条命令，作者称 legacy-scan 基于 3 万个 GitHub 仓库训练，在留出仓库上平均精度 92%，并称在 200 个任务、约 1700 条 Playwright/AST 断言的内部评测中，代理通过率从无指南的 55% 升到有指南的 92%。这些数字均为团队自述，尚无独立验证；作者同时表示该 1.0 是与 Firefox、MDN 和 Edge 合作完成的。

hackernews · paulirish · 11月10日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=50443812)

**「为何现在」** 这次发布把“代理是否真的改用原生 API”做成了可度量的问题：除了指南文本，还一并给出评测基础设施和旧模式扫描工具。但评论已指出，指南中部分特性目前只在 Chrome 稳定支持，Firefox 与 Safari 尚未跟进，因此它对跨浏览器项目的实际适用性仍不确定。

**「内容角度」** 可做角度：从“模型知道 API 名字，却不会默认使用它”这一作者观察切入，对照 55% 到 92% 的自评评测数据，讨论给 AI 编码工具补领域知识时，为什么评测体系和分发方式（npm/CLI 还是可直接 grep 的 Markdown 索引）与指南内容本身同样关键。

**「社区讨论」** 评论中的主要分歧在跨浏览器兼容性：有评论者列出 CSS @function、calc-size\(\)、corner-shape、flex-wrap: balance 等一批在 Chrome 稳定但 Firefox 和 Safari 未支持的特性，也有人担心各家 LLM 都跟随 Chrome 团队的开发指南会加剧单一浏览器主导。另有评论者建议额外发布可用 grep 检索的 Markdown 索引以减少安装依赖，并有人反馈应使用 fromBase64/toBase64 替代 atob/btoa；这些属于个别用户意见，不代表整体共识。

**标签**: `#coding agents`, `#web development`, `#developer tools`, `#browser standards`, `#open source`

---

<a id="item-ai-creator-2"></a>
### [llm-gemini 0.36 发布，Gemini 4 Carbon 开放并计划涨价](https://simonwillison.net/2026/Nov/10/llm-gemini/) ⭐️ 8.0/10

Simon Willison 发布 llm-gemini 0.36，并称 Gemini 4 Carbon 在面向“部分网络安全防御者”公布两周后，现已向其他所有用户开放。文中给出的发布价为每百万输入 token 2 美元、每百万输出 token 10 美元，并计划在 12 月 1 日翻倍至 4 美元和 20 美元；谷歌将这款模型描述为迄今最好的 Gemini。Willison 还展示了低、中、高三种思考强度下的“鹈鹕骑自行车”生成结果（默认中档），并用 Google Antigravity IDE 测试了一个 Three.js 动画提示。更新部分提到 Sundar Pichai 分享的 Antigravity /swarm 演示，称 Carbon 用子代理在 Blender 中建模、以 Three.js/WebGL 构建游戏，并结合 Web Audio 与 Lyria 音效。

rss · Simon Willison · 11月10日 20:09

**「为何现在」** 当下值得注意的变化是 Gemini 4 Carbon 从有限开放转为更广泛可用，同时 llm-gemini 0.36 已发布；发布价和 12 月 1 日涨价计划是材料中可核对的具体信息，但材料没有提供独立性能基准。

**「内容角度」** 可做角度：以 llm-gemini 0.36 的发布和 Gemini 4 Carbon 的可用范围变化为切口，梳理发布价、12 月 1 日翻倍价与默认中档 thinking effort 这些可核对信息，并明确区分谷歌的宣传表述与尚缺独立基准的性能判断。

**标签**: `#Gemini 4 Carbon`, `#llm-gemini`, `#API pricing`, `#model release`, `#Simon Willison`

---

<a id="item-ai-creator-3"></a>
### [Meta AI 发布 Muse Ember：面向智能体任务的小模型，短提示定价对齐竞品](https://simonwillison.net/2026/Nov/10/muse-ember/) ⭐️ 8.0/10

Meta AI 发布 Muse Ember 1.0，称其为自家最小、最高效的模型，面向工具调用、编码子任务、路由、抽取和长文档解析等智能体重复工作。短提示定价为每百万输入 token 0.10 美元、输出 0.50 美元，与 GPT-6 Luna 和 Claude Haiku 5.5 相同；但超过 200k token 后输入涨至 0.30 美元、输出 1.50 美元，阈值和涨幅介于两者之间。Artificial Analysis 的图表显示，Muse Ember 的 xhigh 与 max 档约每任务 0.12/0.14 美元，智能指数约 34/36，位于其帕累托线上；Meta 据此称其处于效率前沿。Simon Willison 实测六个推理档生成 SVG 时，high 档未返回完整 SVG，且推理档位与视觉质量没有清晰对应。

rss · Simon Willison · 11月10日 07:28

**「为何关注」** Muse Ember 进入的是 Claude Haiku/GPT Luna 所在的小模型低价区间，发布时直接把短提示价格对齐到同一水平，并用长提示分档和 Artificial Analysis 的单任务成本做区分。当前材料能确认的是发布、定价和第三方图表位置，尚不能确认它在真实智能体工作流中的稳定性。

**「内容切入」** 可做角度：做一张三款 Haiku 级模型的价格阈值对比表，重点标出 Muse Ember 在 200k 前后从 0.10/0.50 跳到 0.30/1.50 美元的变化，并说明为什么每百万 token 单价不能直接等同于智能体任务成本。

**标签**: `#Meta AI`, `#small language model`, `#model pricing`, `#AI agents`, `#tool use`

---

<a id="item-ai-creator-4"></a>
### [Anthropic 将 Claude 可用范围改为白名单制，中国大陆及港澳不在名单内](https://www.anthropic.com/legal/supported-regions) ⭐️ 8.0/10

Anthropic 发布《支持地区政策》，将 Claude 产品可用范围改为白名单制：Claude.ai、Claude Code、Cowork、API，以及经云平台和授权经销商提供的 Claude 模型，仅在名单所列的 185 个国家和地区可用，未列入者一律不支持。名单包括中国台湾，中国大陆、香港、澳门均不在列；政策还规定，身处不支持地区时使用即违规，在不支持地区注册或设总部的实体及其人员使用违规，被不支持地区主体直接或间接多数持股或控制的公司人员同样违规。材料称该政策于 11 月 12 日生效，但未注明生效年份和公告日期，具体条款与时间仍需以官方页面核对。

telegram · zaihuapd · 11月10日 13:44

**「为何值得注意」** 值得注意的已发生事实是，Claude 的可用范围从地区说明转为白名单制，并附带三条使用限制，直接影响中国大陆及港澳的开发者、创作者和企业用户。材料未给出完整生效年份、公告日期与执行细节，实际影响仍需以 Anthropic 官方页面确认。

**「内容角度」** 可做角度：以“白名单加三条禁止”为线索，梳理这项政策如何把合规判断从“人在哪里”扩展到实体注册地、控制关系和出差场景，并对照名单中中国台湾在列、中国大陆及港澳不在列等细节，提醒读者先核对官方条款，而不是只看地区名单。

**标签**: `#Anthropic`, `#Claude`, `#区域限制`, `#开发者影响`, `#AI合规`

---

<a id="item-ai-creator-5"></a>
### [稀宇科技开源 MiniMax H3 Image，厂商宣称约 10 秒生成 4K 图像](https://huggingface.co/MiniMaxAI/MiniMax-H3-Image) ⭐️ 8.0/10

稀宇科技发布图像模型 MiniMax H3 Image 并开放权重，支持文生图、图像参考与图像编辑，官方称可生成 4096×4096（约 1600 万像素）图像，单张生成约 10 秒，最多接受 16 张参考图。同步推出 Highspeed 高速版本，官方口径为标准模式速度约为主流工具的 1.5 至 2 倍、高速模式 3 至 4 倍。模型已上线 Hugging Face 与开放平台 API，并接入 MiniMax Code、海螺等产品，标准版 4K 单张约 0.069 美元，发布首周优惠价约 0.034 美元。上述速度、倍数与价格均来自官方宣传口径，材料本身是 Telegram 聚合帖，权重许可、实际性能与计费方式仍需以 Hugging Face 模型页和官方 API 公告复核。

telegram · zaihuapd · 11月10日 15:39

**「为何值得注意」** 这条消息把“开放权重”和可比较的具体数字放在了同一处：4K 分辨率、约 10 秒、16 张参考图、单张 0.069 美元。这些数字目前只有官方来源，材料中没有独立实测，因此可以确认的是发布与上线动作，还不能确认实际生成速度与成本。

**「内容角度」** 可做角度：把“10 秒一张 4K”拆成可逐项核对的清单——4096×4096 是否为默认输出、10 秒对应标准版还是 Highspeed 版、16 张参考图在编辑任务中是否真正生效、0.069 美元是按张还是按调用计费，再对照 Hugging Face 模型页与 API 文档逐条标注“已证实/仅官方口径”，做成发布前的核对表。

**标签**: `#MiniMax`, `#开源图像模型`, `#4K文生图`, `#多图参考`, `#图像编辑`

---