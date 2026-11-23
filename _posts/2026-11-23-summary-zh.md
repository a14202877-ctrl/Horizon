---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 76 条内容中筛选出 3 条重要资讯。

---

**AI 创作者雷达**
1. [OpenAI 文章《Perplexity and Intelligence》引发模型评估讨论](#item-ai-creator-1) ⭐️ 7.0/10
2. [厂商称 NVMe KV 缓存池与同容量 DRAM 差距不足 1%](#item-ai-creator-2) ⭐️ 7.0/10
3. [蚂蚁集团领投 Simplexity Robotics 1 亿美元 pre-A 轮](#item-ai-creator-3) ⭐️ 7.0/10

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [OpenAI 文章《Perplexity and Intelligence》引发模型评估讨论](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI 网站上一篇题为《Perplexity and Intelligence》的文章在 Hacker News 引发讨论，核心议题是困惑度/交叉熵是否仍能反映语言模型智能水平。提供的材料没有原文正文，因此文章的方法、数据和结论无法核实，可确认的只有标题、链接与社区评论。讨论涉及困惑度的定义、对交叉熵趋势的意外，以及据称微软分享 MAI-2 Base 评测结果的说法，后者仅为评论转述。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「内容角度」** 可做角度：以“困惑度还能不能作为模型智能的代理指标”为问题，梳理文章标题所指向的争议，并明确区分评论中的定义、个人判断与微软方面据称的评测声明，不把社区观点当作原文结论。

**「社区讨论」** 评论中有人先指出原文没有定义困惑度并给出通俗定义；也有人对交叉熵与模型能力之间仍有清晰趋势感到意外，认为这种简单基准有价值，另有评论从压缩/世界模型角度认为二者对应并不意外。关于微软是否把 MAI 模型加入同一评测，目前只有评论转述的推文说法，材料未提供可核实细节。

**标签**: `#OpenAI`, `#困惑度`, `#模型评估`, `#语言模型`, `#AI研究`

---

<a id="item-ai-creator-2"></a>
### [厂商称 NVMe KV 缓存池与同容量 DRAM 差距不足 1%](https://vllm.ai/blog/2026-11-23-skip-the-dram-tier) ⭐️ 7.0/10

AMD 与 Embedded LLM 在一篇博客中称，在 AMD Instinct MI355X 上通过 vLLM 运行 Kimi-K3 时，基于 NVMe 的 MoRI UMBP KV 缓存池在相同容量下与 DRAM 池的性能差距在 1% 以内。博客还给出成本对比：用于存放一天 agent KV 的驱动器，成本低于只能存放 31 分钟 KV 的 DRAM。上述结果来自厂商基准，材料未提供完整测试方法，也没有独立验证，因此应视为待核实的主张。

rss · vLLM Blog · 11月23日 00:00

**「为何值得关注」** 这条结果值得注意，是因为它直接针对 agent 长时 KV 缓存的内存成本，并给出了与同容量 DRAM 的对比基线；但当前证据仅来自厂商博客，尚未证实可广泛复现。

**「可做角度」** 可做角度：把“NVMe KV 缓存池在相同容量下与 DRAM 差距不到 1%”当作待验证的厂商主张，拆解其测试条件——Kimi-K3、vLLM、AMD MI355X、MoRI UMBP——并追问缺少的方法细节与独立复现，而不是直接下结论说 DRAM 层可被跳过。

**标签**: `#KV cache`, `#LLM inference`, `#vLLM`, `#AMD Instinct`, `#NVMe`

---

<a id="item-ai-creator-3"></a>
### [蚂蚁集团领投 Simplexity Robotics 1 亿美元 pre-A 轮](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

彭博报道，中国具身智能公司 Simplexity Robotics 完成 1 亿美元 pre-A 轮融资，由蚂蚁集团领投，投后估值 16 亿美元；阿里巴巴、腾讯、HongShan（红杉中国）和蓝驰创投等老股东跟投，董事长兼联合创始人 Wang Kai 向彭博确认。公司 2025 年 7 月成立于杭州，核心团队来自理想汽车，贾鹏任 CEO、王佳佳任 COO。报道还称，公司今年 3 月曾披露成立半年内完成五轮融资、累计 20 亿元人民币，当时投后估值已超 10 亿美元；本轮资金将用于同宇树、优必选等更成熟厂商争夺市场。

telegram · zaihuapd · 11月23日 02:02

**「为何现在」** 这笔融资的关键变化是蚂蚁集团领投、老股东继续跟投，使一家成立时间不长的具身智能公司在 pre-A 轮就获得 16 亿美元投后估值。材料尚未给出产品、技术或实际使用层面的新增验证，因此其对人形机器人竞争格局的影响仍待观察。

**「内容角度」** 可做角度：从“pre-A 轮 1 亿美元、投后估值 16 亿美元”与今年 3 月累计融资 20 亿元人民币的披露对照切入，梳理领投和跟投结构、资金用途，并追问具身智能融资热度与商业化验证之间的距离。

**标签**: `#具身智能`, `#人形机器人`, `#融资`, `#蚂蚁集团`, `#中国AI`

---