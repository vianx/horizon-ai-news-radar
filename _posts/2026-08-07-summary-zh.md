---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [通过批处理、算子融合和 SIMD 使 Postgres 分析性能提升 300 倍](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Flash 0731：更快、更便宜、更强大](#item-2) ⭐️ 8.0/10
3. [汇编耻辱堂：奇葩 x86 指令合集](#item-3) ⭐️ 8.0/10
4. [科技从业者幻灭：当整个阶层失去信心会发生什么](#item-4) ⭐️ 8.0/10
5. [OpenAI 公布 Astra 模型网络安全防护措施](#item-5) ⭐️ 8.0/10
6. [甲骨文禁止 OpenJDK 使用 AI 生成代码](#item-6) ⭐️ 8.0/10
7. [SDSS DR20 绘制全天 50 万个超大质量黑洞地图](#item-7) ⭐️ 8.0/10
8. [Codex 搭配 GPT-5.6 Sol Ultra 在浣熊抢劫游戏中胜过 Claude Fable 5](#item-8) ⭐️ 7.0/10
9. [代币末日：企业争相削减 AI 开支](#item-9) ⭐️ 7.0/10
10. [中国科技巨头加速 AI 人才招聘](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [通过批处理、算子融合和 SIMD 使 Postgres 分析性能提升 300 倍](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 9.0/10

pgrust（一个基于 Rust 重新实现的 PostgreSQL）的作者详细介绍了他们如何通过批处理、算子融合和 SIMD 优化查询引擎，使分析查询速度提升数百倍。他们还通过形式化验证和差分测试强调正确性，已证明超过 1000 个面向用户的函数与 Postgres 等价。 这项工作表明，对于兼容 Postgres 的系统，实现显著的性能提升是可能的，为需要更快分析性能而又不想放弃 Postgres 生态的用户提供了一条路径。它还展示了自适应规划和现代优化技术的可行性，而 Postgres 核心团队一直不愿采用这些技术，这可能会影响未来的数据库发展。 优化重点在于减少查询引擎的 CPU 和内存带宽使用。作者提到使用形式化验证和差分模糊测试来确保正确性，并在专门目录中提供了证明。该项目名为 pgrust，帖子还讨论了 IO 调度器和线程调度器，以解决“吵闹邻居”问题。

hackernews · poly2it · 8月7日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49208535)

**背景**: PostgreSQL 是一个广泛使用的开源关系型数据库，但其查询引擎并未针对处理大量数据的分析工作负载进行优化。批处理（一次处理多行）、算子融合（合并多个操作以减少开销）和 SIMD（单指令多数据）等技术在现代分析数据库中很常见，用于提高性能。差分测试是一种软件测试技术，通过比较不同实现的输出来发现错误，而形式化验证则使用数学证明来确保正确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/">Rebuilding Postgres for 300x faster analytics: batching, operator ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Differential_testing">Differential testing - Wikipedia</a></li>
<li><a href="https://quadric.ai/blog/operator-fusion-npu-ai-compilers-on-device">Operator Fusion in NPUs: How AI Compilers... | Quadric Blog</a></li>

</ul>
</details>

**社区讨论**: 作者积极参与讨论，通过强调对正确性的关注（形式化验证和差分测试）来回应信任问题。一些评论者对采用表示怀疑，指出对 Postgres 团队的信任和长期连续性至关重要。其他人则对自适应规划表现出热情，而 Postgres 核心团队一直不愿实施这一技术，并询问了 IO 调度器和线程调度器的更多细节。

**标签**: `#Postgres`, `#database`, `#performance`, `#SIMD`, `#query-engine`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731：更快、更便宜、更强大](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek 于 2025 年 7 月 31 日发布了 V4 Flash 0731 模型，这是 V4 Flash 系列的更新版本，在性能、速度和成本效益方面均有显著提升。社区测试显示，尽管激活参数更少，它在多项基准测试中超越了之前的预览版，甚至超过了 V4 Pro（预览版）。 此次发布通过提供高能力且低成本的模型，增强了 DeepSeek 在竞争激烈的 AI 模型市场中的地位，使更多开发者和企业能够使用先进的 AI。其强大的智能体编码能力和 100 万 token 的上下文窗口，可能会促使更多用户从昂贵的专有模型转向该模型。 该模型具有 100 万 token 的上下文窗口和可调节的推理努力，适合智能体编码任务。社区基准测试显示，在 2x RTX Pro 6000 Blackwell 硬件上，其预填充速度约为 8k tokens/s，单流生成速度约为 250 tokens/s，用户报告即使大量使用，每日成本也低于 5 美元。

hackernews · tosh · 8月7日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49214008)

**背景**: DeepSeek 是一家以发布可与专有模型匹敌的开源权重模型而闻名的中国 AI 公司。V4 Flash 系列旨在平衡性能与效率，提供比完整 V4 模型更小、更快、更便宜的替代方案。0731 更新是在早期预览版之后发布的，现已在 Hugging Face、ModelScope 和 Together AI 等平台上提供。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek -ai/ DeepSeek - V 4 - Flash - 0731 · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.together.ai/models/deepseek-v4-flash-0731">DeepSeek V 4 Flash 0731 API | Together AI</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户称赞该模型的速度、能力和成本效益。一些用户指出在智能体任务中存在无限循环和 token 浪费的问题，并且对 DeepSeek 宣布的即将到来的价格上涨表示担忧。

**标签**: `#AI`, `#DeepSeek`, `#LLM`, `#Machine Learning`, `#Model Release`

---

<a id="item-3"></a>
## [汇编耻辱堂：奇葩 x86 指令合集](https://github.com/xoreaxeaxeax/asm-hall-of-shame) ⭐️ 8.0/10

一个新的 GitHub 仓库“汇编耻辱堂”收集了一系列奇怪且缓慢的 x86 指令，展示了鲜为人知的 CPU 行为。它在 Hacker News 上获得了 222 分和 45 条评论，引起了广泛关注。 该资源对底层程序员和安全研究人员很有价值，因为它突出了可能影响性能和安全的异常指令。它促进了社区对鲜为人知的 CPU 特性及其潜在利用的讨论。 该仓库包含一个慢指令排行榜，其中一个显著的例子是向 ACPI IO 端口写入耗时 12 毫秒，这可能陷入 SMM。规则排除了被陷阱/模拟/虚拟化的指令的计时，但某些条目可能仍涉及此类处理。

hackernews · piotrgrabowski · 8月7日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=49214098)

**背景**: x86 是一种复杂的指令集架构（ISA），包含许多遗留和鲜为人知的指令。有些指令很少使用，但可能表现出令人惊讶的行为，如极高的延迟或异常的副作用。理解这些对于性能优化和安全研究很重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackaday.com/2021/02/25/oddball-x86-instructions/">Oddball X 86 Instructions | Hackaday</a></li>
<li><a href="https://en.wikipedia.org/wiki/TEST_(x86_instruction)">TEST ( x 86 instruction ) - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=10276384">Here's something to ponder: security implications of... | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 社区评论提到了相关项目，例如利用慢指令破坏 SMI，并与 Core War 进行类比。一些用户幽默地建议“nop”应排第一，因为它相对于其目的而言无限慢，而另一些用户则指出某些条目可能涉及 SMM 处理。

**标签**: `#assembly`, `#x86`, `#low-level`, `#security`, `#obscure instructions`

---

<a id="item-4"></a>
## [科技从业者幻灭：当整个阶层失去信心会发生什么](https://www.noemamag.com/why-is-everyone-in-tech-so-sad/) ⭐️ 8.0/10

《Noema》杂志上的一篇文章探讨了科技从业者普遍存在的悲伤和对职业失去信心的现象，在 Hacker News 上引发了大规模社区讨论，获得 349 分和 485 条评论。文章质疑了这种已成为有毒和不确定性代名词的职业道路的可持续性。 这很重要，因为科技从业者是推动创新和经济增长的关键劳动力；他们普遍的幻灭感可能导致生产力下降、人才流失和行业创新力减弱。这也凸显了一个更广泛的社会问题，即高压行业中知识工作者的心理健康和福祉。 文章和讨论提到了线上文化的毒性、90 年代与 20 年代互联网体验的对比，以及印刷行业衰落等历史类比。评论者分享了个人倦怠和幻灭的故事，有些人表达了完全离开该行业的愿望。

hackernews · RickJWagner · 8月7日 12:42 · [社区讨论](https://news.ycombinator.com/item?id=49209539)

**背景**: 科技行业长期以来被视为理想的职业道路，提供高薪和创新机会。然而，近年来，关于倦怠、裁员和有毒工作文化的报道越来越多，导致工人中幻灭感日益增强。这篇文章抓住了这种情绪，质疑科技职业的未来以及该行业对工人心理健康的影响。

**社区讨论**: 社区讨论非常深入，评论者将印刷行业的衰落与现代网络的毒性相提并论。一些人表达了个人倦怠和失去热情，而另一些人则认为文章的语气令人不快，但承认这一对话的社会重要性。

**标签**: `#tech industry`, `#worker morale`, `#career disillusionment`, `#mental health`, `#online culture`

---

<a id="item-5"></a>
## [OpenAI 公布 Astra 模型网络安全防护措施](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/) ⭐️ 8.0/10

OpenAI 发布了其即将推出的 Astra 模型的初步网络安全评估，表明该模型可能达到“关键”网络能力阈值，并宣布了更严格的安全控制措施，包括隔离测试环境。 这一公告意义重大，因为它凸显了 AI 在网络安全中日益增长的作用，既作为防御工具，也作为潜在的进攻威胁。随着 AI 模型能力的增强，它强调了采取强有力安全措施的必要性，影响开发者、安全研究人员以及更广泛的 AI 生态系统。 评估结果非常强，以至于 OpenAI 无法排除 Astra 达到“关键”网络能力的可能性。OpenAI 正在对更高能力模型实施更严格的安全控制，包括隔离测试环境，并计划扩大安全测试，这可能会推迟模型的发布。

hackernews · OpenAI Blog · 8月7日 16:39 · [社区讨论](https://news.ycombinator.com/item?id=49213029)

**背景**: AI 模型越来越多地被用于漏洞发现和利用，正如最近关于 AI 驱动的渗透测试框架的报道所示。然而，AI 发现漏洞的可靠性存在争议，一些报告显示误报率很高。OpenAI 的公告反映了先进 AI 在网络安全中的双重用途性质，需要仔细评估和防护措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/ai-vulnerability-exploitation-initial-access">Adversaries Leverage AI for Vulnerability Exploitation, Augmented Operations, and Initial Access | Google Cloud Blog</a></li>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>
<li><a href="https://www.akamai.com/blog/security-research/ai-vulnerability-discovery-human-oversight-caution">AI in Vulnerability Discovery: A Call for Human Oversight and Caution | Akamai</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了兴趣和怀疑的混合态度。一些用户分享了 AI 在漏洞发现方面的积极经验，而另一些用户则批评 OpenAI 对过去事件缺乏透明度，并质疑更严格控制的有效性。还有一种对处理 AI 模型的公司的不信任情绪，有些人建议将数据移回本地。

**标签**: `#AI safety`, `#cybersecurity`, `#OpenAI`, `#vulnerability research`, `#AI agents`

---

<a id="item-6"></a>
## [甲骨文禁止 OpenJDK 使用 AI 生成代码](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

甲骨文已实施一项临时政策，禁止向 OpenJDK 贡献 AI 生成的代码，理由是法律和审查负担方面的担忧。该政策已由 OpenJDK 管理委员会批准，并在 OpenJDK 法律页面上详细说明。 这一决定影响了 OpenJDK——一个广泛使用的开源项目，作为 Java 的参考实现，可能影响许多企业和开发者。它凸显了 AI 辅助开发与开源治理之间日益增长的紧张关系，尤其是在版权和来源方面。 该临时政策未解释为何甲骨文允许内部产品使用 AI 生成代码，但禁止用于 OpenJDK 贡献。最终政策正在由甲骨文的律师起草，临时措施旨在减轻人工审查者的负担。

hackernews · delduca · 8月7日 17:36 · [社区讨论](https://news.ycombinator.com/item?id=49213754)

**背景**: OpenJDK 是 Java 的开源参考实现，由贡献者社区开发并由甲骨文监管。AI 生成的代码引发了关于版权和开源许可证合规的法律问题，因为关于 AI 生成作品的法律仍在演变。甲骨文的决定反映了对代码来源的担忧，以及对于一个对许多企业至关重要的项目可能带来的法律风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.infoq.com/news/2026/06/oracle-genai-policies/">Oracle's OpenJDK Bans Generative AI Contributions While ...</a></li>
<li><a href="https://www.techzine.eu/news/devops/143395/oracle-bans-ai-generated-contributions-to-openjdk/">Oracle bans AI-generated contributions to OpenJDK</a></li>
<li><a href="https://openjdk.org/bylaws">Bylaws - OpenJDK</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：一些人认为考虑到 Java 的版权历史，这是明智的预防措施，而另一些人则觉得讽刺，甲骨文内部拥抱 AI 却外部禁止。还有人误解甲骨文在 OpenJDK 开发中的角色，一位评论者误以为它完全由社区驱动。

**标签**: `#OpenJDK`, `#AI-generated code`, `#Open source policy`, `#Oracle`, `#Legal`

---

<a id="item-7"></a>
## [SDSS DR20 绘制全天 50 万个超大质量黑洞地图](https://www.sdss.org/black-hole-mapper-release-20/) ⭐️ 8.0/10

斯隆数字巡天（SDSS）发布了第二十次数据发布（DR20），其中包含一张全天 50 万个超大质量黑洞的地图。同时，eROSITA X 射线巡天发布了第二个半天天区目录，将已知 X 射线源数量几乎翻倍至 200 万个。 此次数据发布大幅扩充了超大质量黑洞的普查数量，使得对其分布和演化的大规模统计研究成为可能。SDSS 与 eROSITA 数据的结合为天体物理学和宇宙学的多波段研究提供了前所未有的机遇。 与 DR19 相比，DR20 的超大质量黑洞数据量扩大了 3 到 4 倍。eROSITA 目录基于 1.5 年的运行数据，将已知 X 射线源数量几乎翻倍至 200 万个，其中大部分是活动星系核。

hackernews · MarcoDewey · 8月7日 15:24 · [社区讨论](https://news.ycombinator.com/item?id=49211921)

**背景**: 超大质量黑洞的质量是太阳的百万到十亿倍，位于大多数星系的中心。SDSS 是一项重要的多光谱巡天，在光学和红外波段绘制天空地图，而 eROSITA 是 SRG 卫星上的 X 射线望远镜，在 X 射线波段巡天。结合这些数据，天文学家可以识别并研究宇宙不同时期的超大质量黑洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Supermassive_black_hole">Supermassive black hole - Wikipedia</a></li>
<li><a href="https://starlust.org/sdss-data-release-20-reveals-all-sky-map-of-supermassive-black-holes/">SDSS Data Release 20 reveals all - sky map of supermassive black ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EROSITA">eROSITA - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区成员对这些大规模地图表现出浓厚兴趣，并将其与基因组数据分析相类比。一些人提出了关于地图中明显网格状图案的技术问题，怀疑它们是伪影还是真实特征，并询问绘制黑洞地图与绘制星系地图有何不同。

**标签**: `#astronomy`, `#data release`, `#supermassive black holes`, `#SDSS`, `#eROSITA`

---

<a id="item-8"></a>
## [Codex 搭配 GPT-5.6 Sol Ultra 在浣熊抢劫游戏中胜过 Claude Fable 5](https://simonwillison.net/2026/Aug/7/moonlight-mayhem/#atom-everything) ⭐️ 7.0/10

Simon Willison 将完全相同的提示词交给运行 GPT-5.6 Sol Ultra（Ultra 模式，积极使用子代理）的 Codex Desktop，结果它生成了一款名为“月光与混乱”的游戏，比他之前用 Claude Fable 5 生成的版本好得多。该游戏可在线试玩，完整记录和生成的资源已发布在 GitHub 仓库中。 这次实际对比为当前领先 AI 编码工具的能力提供了实用见解，表明 Codex 搭配 GPT-5.6 Sol Ultra 在复杂创意任务上能产生更优结果。它帮助开发者和 AI 爱好者了解不同智能体编码方法的优缺点，从而影响游戏开发等领域工具的选择。 Codex 在该项目上耗时 52 分钟，若按 API 全价估算成本为 23.28 美元（输入 token 70.07 万，缓存 token 3250 万，输出 token 14.8 万）。一次性提示词最初产生了一个 bug，即每只浣熊都有一个巨大的眼球球体，尽管 Codex 在开发过程中审查了截图，却未能发现；Willison 通过简单提示“为什么浣熊身上有巨大的黑色球体？”和“修复它”解决了问题。

rss · Simon Willison · 8月7日 19:18

**背景**: 像 Claude Code 和 OpenAI 的 Codex 这样的 AI 编码工具利用大型语言模型从自然语言提示生成代码。GPT-5.6 Sol Ultra 模式是一项新功能，允许模型并行生成和协调多个子代理，从而提升长周期任务的性能。子代理是在独立上下文窗口中处理特定子任务的 AI 代理，支持更复杂的工作流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-the-codex-app/">Introducing the Codex app | OpenAI</a></li>
<li><a href="https://betterstack.com/community/guides/ai/gpt-56-sol-ultra-mode/">GPT-5.6 Sol and Ultra Mode: What You Need to Know</a></li>
<li><a href="https://andrew.ooo/answers/gpt-5-6-sol-ultra-mode-subagents-terminal-bench-explained-july-2026/">What Is GPT-5.6 Sol Ultra Mode? Subagents, Terminal-Bench 2.1 ...</a></li>

</ul>
</details>

**标签**: `#AI coding`, `#Codex`, `#Claude`, `#GPT-5.6`, `#game development`

---

<a id="item-9"></a>
## [代币末日：企业争相削减 AI 开支](https://simonwillison.net/2026/Aug/7/pdfs-are-terrible/#atom-everything) ⭐️ 7.0/10

2026 年 6 月 24 日的一篇 404 Media 报道揭示，随着代币消耗激增，企业正紧急削减 AI 开支，埃森哲的内部数据显示非工程师和 PDF 转 Markdown 是主要成本驱动因素。 这凸显了 AI 采用带来的日益增长的财务负担，促使企业重新思考使用模式并优化代币效率。随着 AI 成为业务运营不可或缺的一部分，成本管理策略的需求变得尤为突出。 埃森哲的代理 AI 战略负责人 Justice Kwak 指出，非工程师推动了代币消耗，而将 PDF 转换为 Markdown 是一个主要的代币消耗点。Gartner 预测，由于代币消耗上升，到 2028 年 AI 编码成本将超过开发者的平均工资。

rss · Simon Willison · 8月7日 16:18

**背景**: 大型语言模型（LLM）以称为“代币”的单位处理文本，成本随代币使用量增加而上升。PDF 因包含格式和图像而效率低下，消耗的代币比纯文本多。将 PDF 转换为 Markdown 可减少代币使用和成本，例如 MarkItDown 等工具可将代币费用降低高达 80%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gartner.com/en/newsroom/press-releases/2026-06-24-gartner-predicts-ai-coding-costs-will-surpass-average-developer-salary-by-2028-as-token-consumption-surges">Gartner Predicts AI Coding Costs Will Surpass Average ...</a></li>
<li><a href="https://agentsroom.dev/blog/convert-pdf-to-markdown-save-tokens">Convert PDF to Markdown to Save LLM Tokens: The MarkItDown Guide</a></li>
<li><a href="https://www.mindstudio.ai/blog/convert-files-markdown-reduce-ai-tokens">How to Convert Files to Markdown to Reduce AI Token Usage by ...</a></li>

</ul>
</details>

**标签**: `#AI costs`, `#token consumption`, `#enterprise AI`, `#PDF processing`, `#AI adoption`

---

<a id="item-10"></a>
## [中国科技巨头加速 AI 人才招聘](https://news.google.com/rss/articles/CBMiuAFBVV95cUxQSWRLODU4dTdIZy1DeEZxblRrVzV4bFRCbGtJeEVjbG5PYkQ1enh1eGlmSmJfMEpFNU9RaHlNODlfaHNhX25sczBvczJSajF5ZjlVXzh6Y0RFSDhvbFBud1lBTHJISnB1em9FX0lwcGxfR09oODZheGNzdGgtRkFmUF83RGhLZmFLVnp5WFgyVlJrOHBqYnFFbkoyUkNIdVQxNnMxeDk0T3hTbFcwTXRJOEx4N3g1Ymxm?oc=5) ⭐️ 6.0/10

中国主要互联网公司正在提前招聘计划，以在日益激烈的竞争中争夺 AI 人才。此举反映了他们优先提升员工 AI 能力的战略转变。 这一趋势凸显了 AI 人才对于保持中国科技行业竞争优势的关键重要性。它可能导致薪资上涨和更激进的招聘策略，影响整体就业市场和创新格局。 一财全球的文章指出，公司正在“提前”招聘，即提前其招聘时间表。文中未提及具体公司或数字，但重点是整体招聘努力的加速。

google_news · 一财全球Yicai Global · 8月7日 08:42

**背景**: 中国科技行业一直在迅速扩展其 AI 能力，阿里巴巴、腾讯和百度等公司大力投资于 AI 研发。对熟练 AI 专业人才的需求激增，导致对顶尖人才的激烈竞争。

**标签**: `#AI talent`, `#China tech`, `#hiring`, `#industry trends`

---