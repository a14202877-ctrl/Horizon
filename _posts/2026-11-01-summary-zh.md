---
layout: default
title: "Horizon Summary: 2026-11-01 (ZH)"
date: 2026-11-01
lang: zh
---

> 从 64 条内容中筛选出 3 条重要资讯。

---

**AI 创作者雷达**
1. [Parameter Labs 披露 ChatGPT HTML 预览账户接管攻击链](#item-ai-creator-1) ⭐️ 8.0/10
2. [ChatGPT 与 Codex 额度将共享并按 token 计量](#item-ai-creator-2) ⭐️ 7.0/10
3. [南华早报：苹果拟 12 月通过阿里巴巴在华上线 iPhone AI 功能](#item-ai-creator-3) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [Parameter Labs 披露 ChatGPT HTML 预览账户接管攻击链](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 8.0/10

据 Simon Willison 转述，Parameter Labs 披露了一条针对 ChatGPT HTML 预览沙箱的复杂攻击链，最终可在其他已登录用户打开分享链接时读取其私有数据或代其执行操作。转述称，攻击从沙箱 iframe 通过 postMessage 触发父页面中 MathLive 虚拟键盘开始，利用接收代码的 innerHTML 注入一个不受沙箱限制的新 iframe。随后借助 CSP 允许的 YouTube oEmbed 端点反射并执行 JavaScript，再调用 API 获取私有数据，并通过图片引用外传。Simon Willison 表示 OpenAI 已修复漏洞并支付 5000 美元赏金，他同时认为这一金额偏低。

rss · Simon Willison · 10月31日 23:15

**「为什么现在值得注意」** 这条披露值得现在关注，因为它把 AI 产品内 HTML 预览的沙箱边界、CSP 白名单和第三方库消息处理串成了一条可验证的攻击路径。不过现有材料是 Simon Willison 的转述且正文截断，原始披露的完整攻击链、实际影响范围以及 OpenAI 的正式说明仍需核对。

**「内容角度」** 可做角度：从这条攻击链拆解 AI 应用里“沙箱 iframe + postMessage + CSP 白名单”三者叠加的风险，重点讲为什么一个被允许的第三方端点也可能成为脚本执行跳板，而不是只复述“账户接管”的结论。

**「社区讨论」** 评论区有人称 OpenAI 已确认前后端都拒绝了报告中的消息、问题已解决，总赏金为 5000 美元，并指出利用需要用户点击链接，但认为赏金偏低；也有人批评原文叙事难以跟上实际攻击步骤。另有评论提到 ChatGPT 桌面端的文件系统访问问题，但材料未确认它与本案的关联。

**标签**: `#ChatGPT`, `#安全漏洞`, `#沙箱逃逸`, `#账户安全`, `#AI安全`

---

<a id="item-ai-creator-2"></a>
### [ChatGPT 与 Codex 额度将共享并按 token 计量](https://x.com/thsottiaux/status/2116692529970311254) ⭐️ 7.0/10

据材料，OpenAI 计划自 12 月起在 Plus、Pro 和 Business 计划中合并 ChatGPT 与 Codex 的用量额度，并改为按 token 计量，背景是 Work 的智能体能力将并入 ChatGPT 主体验。材料称即时聊天不占用额度，用户可在设置中查看合并后的剩余用量与重置时间；超出后可等待重置、升级套餐或购买积分。材料未给出具体额度数值和生效年份，相关细节仍需以官方说明为准。

telegram · zaihuapd · 11月1日 01:29

**「为何当下」** 这项变化会直接改变 Plus、Pro 和 Business 用户对 ChatGPT 与 Codex 的成本预期和使用方式，因此值得在规则生效前解释清楚；但材料尚未提供具体额度与官方公告原文，影响范围仍不确定。

**「内容角度」** 可做角度：围绕“聊天不占额度、Codex/智能体任务按 token 消耗”这一差异，梳理用户最需要弄清的使用边界，并明确标注具体额度、生效年份与官方细则仍待确认。

**标签**: `#OpenAI`, `#ChatGPT`, `#Codex`, `#用量额度`, `#token计量`, `#订阅计划`

---

<a id="item-ai-creator-3"></a>
### [南华早报：苹果拟 12 月通过阿里巴巴在华上线 iPhone AI 功能](https://news.google.com/rss/articles/CBMiuAFBVV95cUxNN2tkN3NFenBvWmVSMHFlWEJGWnlfeWpyVzFQQzhoUllDZ3ljS05venFUT1ZnT3pQai13c3hmUHU0RTlESklTekVvU2VuTXJXeDF0Z1k4THFicC1ybU0wcVk5MVBuNmdaMXVCUlZ3dTBPcmtLTVBjTnBKV2lHZEFGRmlKU0loWWttaWlXbDM3QkxLS1RkaHhic04xYm5FWGcyWWxDZDZFT01kVXl5WTFWQUtrcW1uZU020gG4AUFVX3lxTFA4YTg1dUhJeDhZajg5NTFxU29RRWNNeVZzZXRxMmpoUjZ3QTNuWktwS0FQVkxvbUQ3YjQ1NGcwa3hVRDE3TnNOTmVhdXk5QTVuYUhuMGgxR0tmWHZGbDdKV09tdnhWQWhJWTdnaW9mNmhZRWowaV9wQmdvZTRTa3FzdExZakVlTHpXT0RGNGxYS0RpeXd1emlfYXBqVkVCMk1MUjJhbmlQdV90M2RqN3FiakNEM3VYU2w?oc=5) ⭐️ 7.0/10

南华早报报道称，苹果计划于 12 月通过阿里巴巴的合作，在中国推出 iPhone 的 AI 功能。报道给出的关键信息包括上线时间、合作方和受影响市场，但未提供具体功能清单、上线范围或合作细节。该消息目前缺少苹果或阿里巴巴的官方确认，实际可用时间和功能形态仍有不确定性。

google\_news · South China Morning Post · 10月31日 10:02

**「为何值得关注」** 这条消息值得注意，是因为它涉及中国 iPhone 用户获得 AI 功能的时间点，以及苹果通过当地合作伙伴推进功能落地的方式。但现阶段只有媒体标题级信息，尚无官方确认，不能据此判断功能范围或实际体验。

**「内容角度」** 可做角度：以“报道称 12 月上线”为事实边界，梳理目前已知的时间、合作方与受影响用户，并明确哪些关键信息仍待苹果或阿里巴巴回应，避免把功能细节和合作安排当成既定事实。

**标签**: `#Apple Intelligence`, `#中国市场`, `#阿里巴巴`, `#iPhone`, `#AI功能落地`

---