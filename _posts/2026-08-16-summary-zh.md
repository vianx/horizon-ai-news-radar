---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 33 条内容中筛选出 9 条重要资讯。

---

1. [Anthropic 发布 Claude 系统提示词，引发社区分析](#item-1) ⭐️ 8.0/10
2. [AI 模型正故意变笨](#item-2) ⭐️ 8.0/10
3. [Stripe 以超 70 亿美元收购 AI 公司 OpenRouter](#item-3) ⭐️ 8.0/10
4. [Cloudflare 在切换域名服务器时静默注入分析代码](#item-4) ⭐️ 8.0/10
5. [Qwen 3.8 27B：功能强大但默认过度思考](#item-5) ⭐️ 8.0/10
6. [SSOG-Attention：通过可分离高斯实现次二次注意力](#item-6) ⭐️ 8.0/10
7. [Anthropic 第二季营收暴涨 14 倍，超 115 亿美元](#item-7) ⭐️ 8.0/10
8. [达里奥·阿莫迪：AI 不信任是信任危机，而非营销问题](#item-8) ⭐️ 7.0/10
9. [斯坦福和 MIT 发布全球最大系统提示词库](#item-9) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Anthropic 发布 Claude 系统提示词，引发社区分析](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 首次正式公开了 Claude 网页版和移动应用所使用的系统提示词，使其可供公众访问。此次发布涵盖了 Opus 4.8 以及新提到的 Fable 5 和 Mythos 5 等模型的提示词。 这种透明度使开发者和研究人员能够了解 Claude 的指令方式，可能有助于改进提示工程和模型行为分析。同时，它也引发了关于系统提示词最佳长度和设计的社区讨论，可能影响未来 AI 开发实践。 Simon Willison 创建了提示词的 git 历史以追踪变更，并特别指出了关于 Claude Fable 5 和 Mythos 5 的一个新增内容。这些提示词比许多社区成员预期的要长得多，引发了关于如此冗长是否必要的质疑。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是在每次对话开始时提供给 AI 模型的隐藏指令，用于设定上下文和引导行为。Anthropic 的发布是 AI 公司分享其系统提示词的更广泛趋势的一部分，类似 ChatGPT 和 Gemini 等其他模型的提示词也曾被泄露或公开。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs</a></li>
<li><a href="https://decrypt.co/246695/claude-ai-system-prompts-anthropic-tips">Secret Claude AI System Prompts Revealed–What Can We... - Decrypt</a></li>
<li><a href="https://github.com/Piebald-AI/claude-code-system-prompts">GitHub - Piebald-AI/claude-code-system-prompts: All parts of Claude Code's system prompt, 27 builtin tool descriptions, sub agent prompts (Plan/Explore/Task), utility prompts (CLAUDE.md, compact, statusline, magic docs, WebFetch, Bash cmd, security review, agent creation). Updated for each Claude Code version. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区成员对提示词的长度表示惊讶，一些人质疑在建议保持提示词简短的情况下，如此冗长是否合理。其他人则对论坛可能存在的审查表示担忧，还有人指出即使是 Opus 4.8 这样强大的模型也需要明确的指令来处理基本的常识问题。

**标签**: `#AI`, `#LLM`, `#system prompts`, `#Anthropic`, `#Claude`

---

<a id="item-2"></a>
## [AI 模型正故意变笨](https://w4g1.dev/blog/models-are-getting-dumber-on-purpose) ⭐️ 8.0/10

文章认为，AI 模型正越来越多地依赖外部工具而非内部知识，可能导致模块化、可插拔的知识库。这种转变可能使模型知识减少，但更灵活、更新。 这一趋势可能从根本上改变 AI 模型的设计和部署方式，使其更具适应性，并减少对大规模训练数据的需求。它还可能通过促进工具集成和专业化知识模块来影响 AI 生态系统。 文章引用了 SimpleQA 等基准测试，即使最好的模型也会漏掉一半问题，凸显了内部知识的局限性。它设想未来模型卡不再列出知识截止日期，因为权重会在数年尺度上过时。

hackernews · hruvhwe · 8月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=49322695)

**背景**: 大型语言模型（LLM）在海量数据集上训练，并将知识存储在权重中。然而，这些知识会过时，且受训练数据限制。外部工具，如检索增强生成（RAG）和工具调用，使模型能够按需访问最新信息，可能减少对内部知识存储的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.19749">[2604.19749] The Tool-Overuse Illusion: Why Does LLM Prefer External Tools over Internal Knowledge?</a></li>
<li><a href="https://arxiv.org/html/2604.19749">The Tool-Overuse Illusion: Why Does LLM Prefer External Tools over Internal Knowledge?</a></li>
<li><a href="https://labelstud.io/learningcenter/external-knowledge-why-augmented-language-models-need-more-than-what-they-re-trained-on/">How External Knowledge Improves LLMs | Label Studio</a></li>

</ul>
</details>

**社区讨论**: 评论者对可插拔知识库表示兴趣，一位用户设想针对不同领域的模块化模型。另一位指出文章数据过时，并提到更新的模型。还有讨论关于推理和事实是否真的可以分离，因为推理往往需要事实背景。

**标签**: `#AI`, `#LLM`, `#model design`, `#knowledge bases`, `#tool use`

---

<a id="item-3"></a>
## [Stripe 以超 70 亿美元收购 AI 公司 OpenRouter](https://www.bloomberg.com/news/articles/2026-08-16/stripe-nears-deal-to-buy-ai-firm-openrouter-for-over-7-billion) ⭐️ 8.0/10

Stripe Inc. 已敲定协议，以超过 70 亿美元收购帮助企业在 AI 模型之间切换的初创公司 OpenRouter Inc.。该交易由彭博社于 2026 年 8 月 16 日报道。 此次收购使 Stripe 有望成为 LLM API 的支付和路由层，可能重塑 AI 基础设施的经济格局。同时，这也回应了 Stripe 对失去主要 AI 支付量的担忧，因为 OpenAI 最近将支付服务商换成了 Adyen。 OpenRouter 通过单一 API 为开发者提供 500 多个 AI 模型的访问，并具备内置路由和故障转移功能。该交易对 OpenRouter 的估值超过 70 亿美元，较几个月前报道的 13 亿美元估值有大幅跃升。

hackernews · zacharyozer · 8月16日 20:31 · [社区讨论](https://news.ycombinator.com/item?id=49323381)

**背景**: OpenRouter 是一个提供 LLM 统一接口的平台，允许开发者将请求路由到不同提供商的各种 AI 模型。Stripe 是一家领先的在线支付处理公司，以其 API 优先的方法和处理高容量、延迟敏感请求的能力而闻名。此次收购符合 Stripe 的雄心，不仅要抽象金融基础设施，还要抽象 LLM 的基础设施，因为代币代表了一种轻量级的有价值资产。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-08-16/stripe-nears-deal-to-buy-ai-firm-openrouter-for-over-7-billion">Stripe Nears Deal to Buy AI Firm OpenRouter for Over $7 Billion</a></li>
<li><a href="https://openrouter.ai/about">About - The Unified Interface For LLMs | OpenRouter</a></li>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 社区评论既反映了战略上的支持，也反映了对估值的怀疑。一些人认为 Stripe 是理想的拥有者，因为其 API 专业知识和处理高容量请求的能力，而另一些人则质疑 70 亿美元的价格，指出 OpenRouter 的技术可能更容易被复制，并且这笔交易可能主要是为了确保支付量。

**标签**: `#acquisition`, `#AI infrastructure`, `#payments`, `#LLM`, `#Stripe`

---

<a id="item-4"></a>
## [Cloudflare 在切换域名服务器时静默注入分析代码](https://news.ycombinator.com/item?id=49322107) ⭐️ 8.0/10

一位用户发现，将域名服务器切换到 Cloudflare 后，其纯 HTML 网站被静默注入了 JavaScript 分析代码，需要手动在分析仪表板中禁用。该行为在 Hacker News 上被报道，引发了社区讨论。 这引发了重大的隐私和透明度担忧，因为作为主要 CDN 提供商的 Cloudflare 在未经用户明确同意的情况下默认启用分析功能。这影响了可能无意中暴露访客数据的 Web 开发者和网站所有者，凸显了默认选择加入而非选择退出的必要性。 注入的脚本来自 static.cloudflareinsights.com，并包含版本和令牌，如评论所示。用户可以通过设置内容安全策略（CSP）头来限制脚本来源，或在 Cloudflare 仪表板中禁用 Web Analytics 来缓解此问题。该行为似乎发生在 Cloudflare 作为代理时，而不仅仅是纯 DNS 设置。

hackernews · stagas · 8月16日 17:49

**背景**: Cloudflare 提供 Web Analytics，这是一项注重隐私的分析服务，在使用 Cloudflare 代理时会自动注入。当用户将域名服务器切换到 Cloudflare 时，可能会无意中启用代理，从而允许 Cloudflare 修改 HTML 响应。这是 Cloudflare 更广泛服务套件的一部分，但分析注入的默认开启性质已招致批评。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cloudflare.com/web-analytics/">Cloudflare Web Analytics | Cloudflare</a></li>
<li><a href="https://blog.cloudflare.com/wallets/">Announcing Cloudflare Wallets: The programmable... | Cloudflare Blog</a></li>

</ul>
</details>

**社区讨论**: 社区成员表达了担忧，并分享了解决方法，例如使用 CSP 头来阻止脚本。一些人指出，注入仅发生在 Cloudflare 作为代理时，而不是纯 DNS 设置。其他人提供了 Cloudflare 博客和文档的链接以获取更多详细信息。

**标签**: `#Cloudflare`, `#privacy`, `#analytics`, `#web development`, `#security`

---

<a id="item-5"></a>
## [Qwen 3.8 27B：功能强大但默认过度思考](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

阿里巴巴 Qwen 实验室发布了 Apache 2 许可的 27B 参数视觉能力大语言模型 Qwen 3.8 27B，其基准测试成绩较前代及闭源的 Qwen 3.7-Plus 均有显著提升。然而，Simon Willison 的实测评论显示，该模型默认采用“xhigh”推理强度，导致 token 消耗过多、生成时间过长。 此次发布意义重大，因为它提供了一个可在消费级硬件上运行的强大开放权重模型，有望推动先进 AI 能力的普及。过度思考的问题凸显了用户面临的实际挑战，默认设置可能并非最优，影响效率和用户体验。 该模型原生支持 262,144 token 的上下文长度，可通过 RoPE 扩展至 1M。Simon Willison 在 M5 Max MacBook Pro 和 NVIDIA DGX Spark 上运行了 17GB 的 Q4_K_M 量化版本，发现默认的“xhigh”推理强度会耗尽 LM Studio 的 8,192 token 上下文限制，需将上下文长度调至最大。生成一个简单的 SVG 图像耗时 21 分钟，消耗了 22,276 个推理 token。

rss · Simon Willison · 8月16日 22:00

**背景**: Qwen 是阿里云开发的大语言模型系列，以在 Apache 2.0 等宽松许可下发布开放权重模型而闻名。27B 参数规模被认为是高端笔记本运行模型的理想选择，在能力与资源需求之间取得平衡。推理强度是一个可配置参数，控制模型在生成答案前“思考”所花费的计算量，设置越高，回答越全面但速度越慢。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lmstudio.ai/models/qwen3.8">Qwen 3 . 8</a></li>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apache_License">Apache License</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#open-source`, `#AI`, `#benchmarks`

---

<a id="item-6"></a>
## [SSOG-Attention：通过可分离高斯实现次二次注意力](https://www.reddit.com/r/MachineLearning/comments/1vpt6ay/ssogattention_sum_of_separable_gaussians_as_a/) ⭐️ 8.0/10

SSOG-Attention 用可分离高斯之和替代缩放点积注意力（SDPA），将复杂度从 O(N²·d) 降低到 O(N·√N·d)。实验表明，在 CIFAR-100 上它优于 SDPA，在 ImageNet-1k 上性能相当且收敛更快。 这为标准注意力提供了一种可扩展的替代方案，解决了 Transformer 中的二次方瓶颈。它可能使大规模模型的训练和推理更加高效，惠及更广泛的机器学习社区。 该方法为每个头学习少量高斯原子，并根据查询令牌对其进行几何引导，从而可分解为可分离的和。作者指出部分代码和博客内容使用了 AI，但对其工作负责。

reddit · r/MachineLearning · /u/4rtemi5 · 8月16日 10:06

**背景**: 缩放点积注意力（SDPA）计算所有查询和键令牌之间的相似度分数，导致 O(N²) 复杂度。次二次注意力方法旨在降低这一成本同时保持性能。SSOG 使用可分离高斯来近似注意力，实现次二次复杂度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.openai-hub.com/news/1620/">SSOG- Attention ... - OpenAI Hub</a></li>
<li><a href="https://arxiv.org/abs/2505.14840">[2505.14840] Subquadratic Algorithms and Hardness for Attention with Any Temperature</a></li>

</ul>
</details>

**标签**: `#attention`, `#efficiency`, `#machine learning`, `#transformers`

---

<a id="item-7"></a>
## [Anthropic 第二季营收暴涨 14 倍，超 115 亿美元](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic 第二季初步营收超过 115 亿美元，同比增长逾 14 倍，高于去年同期的 7.87 亿美元和 2026 年第一季的 47.3 亿美元。当季调整后营业利润也转为正数。 这一营收激增表明 Anthropic 在商业上取得了强劲进展，使其在潜在的 IPO 前成为 AI 行业的重要参与者。调整后营业利润转正表明财务状况改善，可能吸引投资者并影响 AI 市场的竞争格局。 据彭博社报道，这些数字为初步数据，仍可能调整。公司正筹备可能在今秋启动的大型 IPO，但尚未确认官方时间表。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是一家以开发 Claude 系列大语言模型而闻名的 AI 安全和研究公司。其营收的快速增长反映了企业对生成式 AI 解决方案需求的增加，因为企业正在将 AI 整合到其运营中。

**标签**: `#Anthropic`, `#AI industry`, `#revenue`, `#IPO`, `#business`

---

<a id="item-8"></a>
## [达里奥·阿莫迪：AI 不信任是信任危机，而非营销问题](https://simonwillison.net/2026/Aug/16/dario-amodei/) ⭐️ 7.0/10

Anthropic 首席执行官达里奥·阿莫迪表示，公众对 AI 的不信任源于对机构更广泛的信任危机，而非 AI 领袖对风险的警告。他认为，重建信任需要实实在在的成果，比如真正治愈癌症，而不是营销活动。 这位 AI 领军人物的评论挑战了“AI 领袖的警告导致公众不信任”的常见说法，提供了细致的视角，可能影响 AI 公司处理沟通和建立信任的方式。它强调了 AI 承诺与实际成果之间的差距，这对行业信誉至关重要。 阿莫迪明确拒绝了为 Anthropic 开展“华丽正面营销活动”的想法，称“AI 将治愈癌症”之类的说法是陈词滥调且具有欺骗性。他承认对 AI 公司最准确的批评是未能兑现造福世界的重大承诺，并引导批评者关注这一点，而非信息传播。

rss · Simon Willison · 8月16日 15:05

**背景**: 达里奥·阿莫迪是 Anthropic 的首席执行官，该公司是领先的 AI 安全公司，以开发 Claude 模型系列而闻名。随着 AI 技术日益普及，围绕公众对 AI 信任的讨论愈演愈烈，涉及失业、错误信息和生存风险等担忧。阿莫迪的评论出现在关于 AI 公司应如何向公众传达风险和收益的辩论中。

**标签**: `#AI ethics`, `#public trust`, `#Anthropic`, `#AI industry`, `#Dario Amodei`

---

<a id="item-9"></a>
## [斯坦福和 MIT 发布全球最大系统提示词库](https://news.google.com/rss/articles/CBMiiAFBVV95cUxOeXlXY1hnRGxuUVlVVzlJaDFDWlB1MXNUT2JpSko0SW4zM3dGOVBtUjZBZGNxWi1jcll3aUkwNGVGTndLdHRITlg1VTA5QURRcDVpZDFtMUhiVGtkY0F0WmJQRjl1VE9Sa3VYXzlhWE5OWkJjbjB6aVBSMF9ZZTdCbnFYTlBGMi1y?oc=5) ⭐️ 7.0/10

斯坦福大学和麻省理工学院联合发布了全球最大的系统提示词库，这是一个面向 AI 模型的全面系统提示词集合。此次发布为 AI 研究人员和开发者提供了重要资源。 该词库之所以重要，是因为它标准化并集中了系统提示词，而系统提示词对于控制 AI 行为和性能至关重要。它可能加速提示工程研究，并提高整个行业 AI 实验的可重复性。 该词库包含大量系统提示词，可能涵盖多种模型和用例，并设计为开放可访问。具体细节如提示词的确切数量和托管平台在现有信息中尚未披露。

google_news · 搜狐网 · 8月16日 05:56

**背景**: 系统提示词是在对话开始时给 AI 模型的指令，用于设置上下文和引导行为。它们对于角色扮演、输出格式化和确保安全等任务至关重要。一个大型、精选的提示词库可以帮助开发者避免重复造轮子，并推广最佳实践。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/danielrosehill/System-Prompt-Library">GitHub - danielrosehill/ System - Prompt - Library : System prompts for...</a></li>
<li><a href="https://veprompts.com/prompts/system/">System Prompt Library — 100+ Expert Prompts | VePrompts</a></li>
<li><a href="https://prompts.danielrosehill.com/">System Prompt Library - Daniel Rosehill</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#prompt engineering`, `#research`

---