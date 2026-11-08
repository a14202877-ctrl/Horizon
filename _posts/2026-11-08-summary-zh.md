---
layout: default
title: "Horizon Summary: 2026-11-08 (ZH)"
date: 2026-11-08
lang: zh
---

> 从 57 条内容中筛选出 3 条重要资讯。

---

**AI 创作者雷达**
1. [Claude Code 被指联网搜索时发送登录邮箱](#item-ai-creator-1) ⭐️ 8.0/10
2. [安全厂商称 1,122 个公开 GitHub 文件含 Claude Code 配置泄露密钥](#item-ai-creator-2) ⭐️ 7.0/10
3. [法官裁定 Anthropic 须就 Claude Max 用量宣传部分指控应诉](#item-ai-creator-3) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [Claude Code 被指联网搜索时发送登录邮箱](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 8.0/10

转述材料显示，有开发者投诉称，Claude Code 在联网搜索时把用户登录邮箱填入请求并发送，导致其每天收到大量诈骗邮件；不过，这一因果关系在现有材料中尚未得到验证。Anthropic 工程师回应称，此前为解决 Claude 乱填作者名的问题，把登录邮箱放进了模型上下文；相关问题今年 7 月已有人报告，邮箱曾被发往 Wikipedia、美国证券交易委员会等站点。2.1.317 版已加入拦截，但可被 Python 脚本绕过，公司计划在下一版本从模型上下文中移除登录邮箱。

telegram · zaihuapd · 11月7日 08:09

**「为何现在」** 现在值得注意，是因为工程师已提到 2.1.317 版加过拦截，并计划在下一版本移除邮箱，说明处理仍在推进。已发生的是版本中的拦截与后续移除计划；泄露范围、绕过细节以及诈骗邮件与泄露之间的因果关系，仍需以 GitHub issue 原文核实。

**「内容角度」** 可做角度：以这次开发者投诉为线索，核对 Claude Code 在联网搜索时把登录邮箱带入请求的说法、2.1.317 版拦截为何可被 Python 脚本绕过，以及官方计划在下一版本移除邮箱的处理路径，写成面向开发者的隐私风险核查清单。

**标签**: `#Claude Code`, `#隐私泄露`, `#AI 编程工具`, `#安全漏洞`, `#Anthropic`

---

<a id="item-ai-creator-2"></a>
### [安全厂商称 1,122 个公开 GitHub 文件含 Claude Code 配置泄露密钥](https://apiiro.com/blog/coding-agents-leaking-secrets-github-dont-ask-again) ⭐️ 7.0/10

安全厂商 Apiiro 发文称，在 1,122 个公开 GitHub 仓库文件中发现 Claude Code 本地权限配置 .claude/settings.local.json 里保存了含密钥或密码的已批准命令。该文件按设计应只留在本地，Claude Code 团队在 Hacker News 上回应称，当 Claude 自己创建该文件时会自动将其加入 gitignore，因此这批文件属于用户手动创建并提交到仓库。Claude Code 团队成员 bcherny 表示，Claude Code 过去没有做密钥擦除（secret scrubbing），但正在研究可采取的防护措施。需要注意，1,122 这一数字来自厂商自述扫描，未见独立验证，且泄露前提是用户把明文密钥写入权限配置并提交到公开仓库。

hackernews · shmulc · 11月7日 20:45 · [社区讨论](https://news.ycombinator.com/item?id=50407882)

**「为何此刻值得注意」** 这是少数由 Claude Code 团队成员直接出面对此类问题表态的场合：团队承认历史上不做 secret scrubbing，并称正在研究防护手段，但尚未公布具体方案或时间表。事件本身不是产品自动泄密，而是围绕 AI 编程代理本地权限配置的实践风险被具体量化。

**「内容切入角度」** 可做角度：把它当作一条配置卫生提醒来写——讲清 .claude/settings.local.json 的定位（应留在本地、Claude 自动创建时会被 gitignore），说明“Don&\#x27;t Ask Again”本身不会泄露，风险来自把含明文密钥的已批准命令写进该文件并提交，再结合团队“过去不做 secret scrubbing、正在研究防护”的表态，给出提交前自查的实操建议，而不是把它写成产品重大安全事件。

**「社区讨论」** 评论普遍认为标题有误导性：必须由用户手动创建并提交本地 Claude 配置，且配置中本来就有含密钥的命令，才会造成暴露，单纯点击“Don&\#x27;t Ask Again”并不会泄露。也有用户分享了自己的隔离做法，例如为每个任务使用隔离网络上的临时虚拟机配合 --dangerously-skip-permissions，并通过 API 代理限制对外部服务的权限。

**标签**: `#Claude Code`, `#AI Agent 安全`, `#密钥泄露`, `#开发者配置管理`, `#GitHub 仓库安全`

---

<a id="item-ai-creator-3"></a>
### [法官裁定 Anthropic 须就 Claude Max 用量宣传部分指控应诉](https://thenextweb.com/news/anthropic-claude-max-lawsuit-ruling-usage-claims) ⭐️ 7.0/10

美国加州北区联邦法院一名法官裁定，Anthropic 须就 Claude Max 套餐用量宣传的误导指控应诉。原告称，100 美元与 200 美元档宣称比 Pro 多用 5 倍和 20 倍，但按周计算实际约为 3.5 倍和 6 倍。法官指出，按会话计算的说明藏在销售页两个超链接之外，而用户按月付费，可合理理解为按月计算。过失虚假陈述和违约指控获准继续，加州不正当经营和虚假广告两项指控被驳回；这是程序性裁定，并非最终责任认定。

telegram · zaihuapd · 11月7日 12:44

**「为何值得注意」** 这是一起围绕 AI 订阅用量宣传的法院阶段性裁定：案件将进入应诉阶段，但 Anthropic 是否构成误导尚无最终结论。它把订阅页如何标注计量周期、说明是否足够显眼的问题摆到了台面上。

**「内容切入角度」** 可做角度：对照 Claude Max 各档宣传的“5 倍、20 倍”与诉状所称按周约 3.5 倍、6 倍，讨论订阅页计量周期标注与超链接说明的可见性，并明确区分原告主张、法官的程序性判断与尚未作出的责任认定。

**标签**: `#Claude Max`, `#Anthropic`, `#AI订阅定价`, `#消费者诉讼`, `#广告合规`

---