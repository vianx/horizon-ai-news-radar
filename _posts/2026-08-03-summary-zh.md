---
layout: default
title: "Horizon Summary: 2026-08-03 (ZH)"
date: 2026-08-03
lang: zh
---

> 从 30 条内容中筛选出 8 条重要资讯。

---

1. [Karpathy 强调 Pelican 基准测试与 LLM 物理世界理解差距](#item-1) ⭐️ 8.0/10
2. [Kakehashi：通过用户态翻译在 Linux ARM 上运行 macOS 二进制文件](#item-2) ⭐️ 8.0/10
3. [科技巨头与 AI 领袖就开放权重模型产生分歧](#item-3) ⭐️ 8.0/10
4. [Karpathy 点赞 sqliteai/waste：基于 SQLite 的 LLM 推理引擎](#item-4) ⭐️ 7.0/10
5. [F*：一种通用的面向证明的编程语言](#item-5) ⭐️ 7.0/10
6. [eBay 骚扰活动导致 5600 万美元赔偿及监禁判决](#item-6) ⭐️ 7.0/10
7. [NeurIPS 2026 反驳通知故障让作者陷入困境](#item-7) ⭐️ 7.0/10
8. [condense-json 1.0 发布，包含非破坏性修复](#item-8) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Karpathy 强调 Pelican 基准测试与 LLM 物理世界理解差距](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 8.0/10

Andrej Karpathy 分享了一条关于“Pelican”的推文，引发了关于前沿 LLM 在创建可玩弹球游戏等任务上的困难以及新基准测试需求的讨论。讨论指出，即使是先进的模型也常常在此类任务上失败，而 Opus 5 是第一个在特定环境中“一次性”完成该任务的模型。 这很重要，因为它凸显了当前 LLM 在物理世界理解方面的局限性，而这对于游戏开发和模拟等应用至关重要。同时，它也标志着向更定性、基于行为的基准测试转变，这些基准能更好地衡量真实世界能力，可能指导未来的模型开发。 讨论中提到了具体的失败案例，如墙壁阻挡发射滑道、挡板旋转错误以及孔洞导致球掉落。还指出 Anthropic 模型可能专门针对 three.js 代码生成进行了训练，这可能会影响基准测试结果，并建议此类基准测试需要定性和主观的测量方法。

hackernews · delichon · 8月2日 04:05 · [社区讨论](https://news.ycombinator.com/item?id=49140998)

**背景**: “Pelican”基准测试由 Simon Willison 推广，要求生成一个骑自行车的鹈鹕的 SVG 图像，已成为一个非正式但广泛使用的 LLM 能力测试。类似地，弹球游戏任务正成为物理世界理解的基准，因为它需要协调安排元素以创建可玩的游戏。这些基准凸显了 LLM 在需要空间推理和物理一致性的任务上常常遇到困难，尽管它们在基于文本的推理上表现出色。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/pelican-bicycle">GitHub - simonw/pelican-bicycle: LLM benchmark: Generate an SVG of a pelican riding a bicycle · GitHub</a></li>
<li><a href="https://dylancastillo.co/posts/pelicanmaxxing.html">Are AI labs pelicanmaxxing? – Dylan Castillo</a></li>
<li><a href="https://simonwillison.net/2025/Jun/6/six-months-in-llms/">The last six months in LLMs, illustrated by pelicans on bicycles</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了复杂的情绪：一些人强调最终产品的糟糕表现是局限性的证据，而另一些人则将其视为物理世界理解的新基准。还有人怀疑模型是否针对特定任务（如 three.js）进行了专门训练，这可能会夸大性能，并呼吁采用定性测量方法。

**标签**: `#AI`, `#LLM`, `#benchmark`, `#Karpathy`, `#physical world understanding`

---

<a id="item-2"></a>
## [Kakehashi：通过用户态翻译在 Linux ARM 上运行 macOS 二进制文件](https://github.com/wie-project/kakehashi) ⭐️ 8.0/10

Kakehashi 是一个实验性的用户态翻译层，能够在 Linux aarch64 上原生运行 macOS ARM64 二进制文件，目前已有 7-Zip、curl 和 Xcode Git 工具的工作原型。它加载 Darwin Mach-O 文件，映射独立的 libSystem，并翻译 BSD 系统调用，无需 JIT。 该项目解决了跨操作系统二进制兼容性方面的重大技术挑战，有望使 macOS 命令行工具在 Linux ARM 硬件上运行。如果成功，它可能通过提供对 macOS 特定软件的访问来扩展 Linux 生态系统，类似于 Wine/Proton 对 Windows 应用程序所做的那样。 该项目以命令行优先，不使用 JIT，专注于翻译 BSD 系统调用并提供独立的 libSystem。目前性能上 7-Zip 比原生 Linux 慢约 5.2 倍，但作者已有明确的优化计划。该项目可在 GitHub 上获取，并可通过 cargo install kakehashi 安装。

hackernews · vlad_kalinkin · 8月2日 16:26 · [社区讨论](https://news.ycombinator.com/item?id=49145937)

**背景**: 操作系统之间的二进制兼容性具有挑战性，因为每个操作系统都有自己的内核接口、系统调用约定和运行时库。像 Wine 和 Darling 这样的项目试图通过翻译 API 调用和系统调用来提供这种兼容性。Kakehashi 专门针对 Linux aarch64 上的 macOS ARM64 二进制文件，利用共享的 ARM 架构来简化翻译过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/wie-project/kakehashi">wie-project/ kakehashi : Userspace macOS translation layer for Linux ...</a></li>
<li><a href="https://savepearlharbor.com/?p=489422">Kakehashi : запуск macOS бинарников на Linux ARM . Часть...</a></li>

</ul>
</details>

**社区讨论**: 社区表现出浓厚的兴趣和乐观态度，用户将其与 Darling 进行比较，并建议可能的合作。一些人对技术方法表示好奇，例如如果不需要可再分发的库，虚拟化框架是否会更简单。其他人则希望未来能通过类似 yabridge 的层在 Linux 上运行 Audio Unit 二进制文件。

**标签**: `#macOS`, `#Linux`, `#ARM`, `#binary compatibility`, `#userspace`

---

<a id="item-3"></a>
## [科技巨头与 AI 领袖就开放权重模型产生分歧](https://simonwillison.net/2026/Aug/2/open-letters/#atom-everything) ⭐️ 8.0/10

微软牵头于 2026 年 7 月 24 日发布了一封名为《开放权重与美国 AI 领导力》的公开信，已有包括 NVIDIA、亚马逊和 OpenAI 在内的超过 235 家公司签署，支持开放权重 AI 模型。相比之下，Anthropic 在三天后发布了自己的立场，表达了对风险的担忧并呼吁打击蒸馏行为，而另一封由前沿 AI 公司 1324 名员工签署的《Pacing the Frontier》信函则敦促美国政府支持国际合作以控制自动化 AI 发展的节奏。 这场辩论凸显了 AI 发展的关键政策十字路口，开源倡导者与关注安全的阵营对立，主要行业参与者纷纷站队。其结果可能影响美国对开放权重模型的监管，进而影响创新、竞争和全球 AI 领导地位。 微软的信函明确支持蒸馏做法，有些人认为这可能涉及不当使用，且值得注意的是 Anthropic 并未签署。Anthropic 在 CEO Dario Amodei 的领导下回应，警告威权政府带来的风险，并呼吁打击工业规模的蒸馏操作，同时澄清其从未主张禁止开放权重模型。

rss · Simon Willison · 8月2日 04:16

**背景**: 开放权重模型是指公开其训练参数的 AI 模型，允许任何人下载、检查和修改，但再分发权利取决于许可证。这与保持专有的封闭模型形成对比。争论的焦点在于如何在透明度与创新之间取得平衡，同时防范潜在的滥用和国家安全风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/">Open Weights and American AI Leadership</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/wp-content/uploads/2026/07/open-weight-models-letter-1.pdf">Open Weights and American AI Leadership July 24, 2026</a></li>

</ul>
</details>

**标签**: `#AI`, `#open source`, `#policy`, `#industry`, `#Simon Willison`

---

<a id="item-4"></a>
## [Karpathy 点赞 sqliteai/waste：基于 SQLite 的 LLM 推理引擎](https://github.com/sqliteai/waste) ⭐️ 7.0/10

Andrej Karpathy 在 GitHub 上为 sqliteai/waste 仓库点了星，该项目通过直接从 NVMe 流式传输激活权重，在超出可用 RAM 的情况下运行 2.78 万亿参数的 Kimi K3 模型。该项目是一个无依赖、可嵌入的 C 语言推理引擎，采用 Apache 2.0 许可证发布。 来自 AI 领域知名人物的点赞表明该项目具有高度相关性，并可能加速其采用，该项目解决了在有限硬件上运行大型语言模型日益增长的需求。通过利用 SQLite 和 NVMe，它提供了一种新颖的方法，可能影响未来的推理引擎设计和边缘 AI 部署。 waste 引擎从 NVMe 流式传输激活权重，无需将整个模型加载到 RAM 中，并且设计为无依赖、可嵌入。它是 SQLite AI 生态系统的一部分，该生态系统包括 sqlite-ai 和 sqlite-agent 等扩展，用于设备端推理和自主代理。

github · karpathy · 8月2日 17:19

**背景**: SQLite 是一种广泛使用的嵌入式 SQL 数据库引擎，SQLite AI 项目旨在将其转变为面向边缘设备的 AI 原生数据库，增加设备端推理和代理支持等功能。运行万亿参数模型通常需要巨大的 GPU 内存，但从存储中流式传输权重可以在消费级硬件上实现推理，尽管可能带来延迟方面的权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/sqliteai/waste">GitHub - sqliteai/waste: Run the full 2.78-trillion-parameter Kimi K3 model beyond available RAM by streaming activated weights directly from NVMe. A dependency-free, embeddable C inference engine. · GitHub</a></li>
<li><a href="https://marcobambini.substack.com/p/the-waste-inference-engine">The WASTE inference engine - Marco Bambini</a></li>
<li><a href="https://www.sqlite.ai/">SQLite AI - Smart Edge Databases with Cloud Sync and Intelligence</a></li>

</ul>
</details>

**标签**: `#GitHub`, `#SQLite`, `#AI`, `#Karpathy`, `#Open Source`

---

<a id="item-5"></a>
## [F*：一种通用的面向证明的编程语言](https://fstar-lang.org/) ⭐️ 7.0/10

F* 是一种通用的、面向证明的编程语言，支持纯函数式和带效果的编程，并在 Hacker News 社区获得了 146 分和 64 条评论的关注。该语言旨在进行程序验证，允许开发者在代码中编写数学证明。 F* 的重要性在于它弥合了现实世界软件开发与形式验证之间的差距，使得证明加密协议和安全敏感代码等关键系统的正确性成为可能。其学术和工业相关性，包括微软研究院的贡献，凸显了它对软件可靠性的潜在影响。 F* 是微软研究院和法国国家信息与自动化研究所（INRIA）的联合项目，灵感来源于 ML、Caml 和 OCaml。它是一种依赖类型语言，类似于 Coq 和 Agda，但旨在更实用，适用于现实世界的软件验证。

hackernews · ducktective · 8月2日 12:31 · [社区讨论](https://news.ycombinator.com/item?id=49143925)

**背景**: 形式验证是数学上证明系统行为符合其规范的过程。F* 是一种面向证明的编程语言，将这种能力直接集成到编程语言中，允许开发者在代码旁边编写证明。这种方法对于高可信软件尤其有价值，例如加密协议和安全关键系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F*_(programming_language)">F* (programming language) - Wikipedia</a></li>
<li><a href="https://fstar-lang.org/">F*: A Proof-Oriented Programming Language</a></li>
<li><a href="https://github.com/FStarLang/FStar">GitHub - FStarLang/FStar: A Proof-oriented Programming Language · GitHub</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论表现出复杂的情绪：一些用户赞赏 F* 表达外部库调用和从 C 语言增量迁移的能力，而另一些用户则批评主页缺乏代码示例，并质疑其行业采用情况。还有用户幽默地指出，没有副作用就无法实现响应式样式表，这涉及 F* 对带效果编程的支持。

**标签**: `#programming language`, `#formal verification`, `#proof-oriented`, `#functional programming`, `#F*`

---

<a id="item-6"></a>
## [eBay 骚扰活动导致 5600 万美元赔偿及监禁判决](https://www.ft.com/content/06ec1b03-d4af-40cf-b12a-4ba5a410f6d2) ⭐️ 7.0/10

eBay 已同意向大卫和伊娜·施泰纳夫妇支付 5600 万美元，这对夫妇曾是 eBay 前安全主管策划的骚扰活动的目标，这些主管也已获刑。该活动包括发送威胁信息、监视，甚至向夫妇家中寄送带血的猪面具。 此案凸显了企业不当行为的严重后果以及安全团队滥用权力的可能性，引发了对科技公司问责制的质疑。同时，它也警示企业可能采取极端手段压制批评者，影响公众对企业治理的信任。 eBay 安全团队的七名成员（包括前警察队长）参与了针对施泰纳夫妇的活动，这对夫妇曾发布批评 eBay 的通讯。判决包括前高级总监吉姆·鲍获刑 57 个月，其他人获较轻刑罚，5600 万美元的和解协议于 2024 年宣布。

hackernews · JumpCrisscross · 8月2日 19:19 · [社区讨论](https://news.ycombinator.com/item?id=49147435)

**背景**: 施泰纳夫妇经营名为“eBay's EcommerceBytes”的通讯，批评 eBay，导致 2019 年的骚扰活动。活动包括寄送带血的猪面具和一本关于配偶谋杀后生存的书，以及监视和威胁。此案强调了企业安全运营中道德行为的重要性，以及越界者的法律后果。

**社区讨论**: 评论者怀疑骚扰活动仅限于施泰纳夫妇，质疑是否还有其他批评者成为目标。一些人还对前警察的参与以及企业问责制的更广泛影响表示担忧，而另一些人则转而讨论 eBay 与竞争对手相比的高额费用。

**标签**: `#eBay`, `#harassment`, `#corporate accountability`, `#legal`, `#security`

---

<a id="item-7"></a>
## [NeurIPS 2026 反驳通知故障让作者陷入困境](https://www.reddit.com/r/MachineLearning/comments/1vdu92a/neurips_2026_acs_and_reviewers_have_disappeared_d/) ⭐️ 7.0/10

一位 NeurIPS 2026 作者报告称，在官方讨论期（AoE 7 月 27 日）之前通过“反驳”按钮提交的反驳未能触发对审稿人和领域主席的通知，导致四位审稿人和领域主席完全沉默。该问题也影响了同时担任审稿人的作者，因为他们没有收到所审论文早期反驳的邮件通知。 该问题可能损害 NeurIPS 审稿过程的公平性，因为早期反驳可能被忽视，从而影响论文录用决定。它凸显了会议通知系统中的系统性缺陷，可能影响当前周期内的许多作者和审稿人。 作者尝试了几种变通方法，包括对所有人可见的元评论、审稿人提醒以及给程序主席发邮件，但讨论期仅剩约一天，他们不确定该如何继续。该帖子标记为 [D]（讨论），作者提到根据初始分数他们原本希望获得口头报告或亮点展示。

reddit · r/MachineLearning · /u/extricableforsythia · 8月2日 21:33

**背景**: NeurIPS（神经信息处理系统大会）是顶级机器学习会议。其审稿过程通常包括反驳期，作者可以回应审稿人意见，以及作者-审稿人-领域主席讨论期。通常当有新评论或反驳时，系统会通过邮件发送通知，但此次事件表明系统存在缺陷，导致早期提交的通知未发送。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://neurips.cc/Conferences/2025/ReviewerGuidelines">2025 Reviewer Guidelines</a></li>
<li><a href="https://neurips.cc/Conferences/2025/AC-Guidelines">NeurIPS 2025 AC Guidelines</a></li>

</ul>
</details>

**标签**: `#NeurIPS`, `#peer review`, `#conference`, `#rebuttal`, `#academic publishing`

---

<a id="item-8"></a>
## [condense-json 1.0 发布，包含非破坏性修复](https://simonwillison.net/2026/Aug/2/condense-json/#atom-everything) ⭐️ 5.0/10

Simon Willison 宣布 condense-json 1.0 发布，这是一个用于压缩 JSON 数据的 Python 库。该版本在一年半的开发后包含了一些合理且非破坏性的修复。 此次发布标志着该工具的一个里程碑，它通过替换重复子串来减小 JSON 体积，特别适用于高效存储 LLM 生成的日志。这表明该工具已成熟稳定，开发者可以放心用于生产环境。 该库提供 condense_json 和 uncondense_json 函数，使用替换字典将子串替换为紧凑语法，如 {"$r": [...]}。它被用于 Simon Willison 的 LLM 项目，以节省 SQLite 日志空间，如 PR #1586 所示。

rss · Simon Willison · 8月2日 22:19

**背景**: condense-json 是一个 Python 库，通过将重复的子串替换为更短的引用来压缩 JSON，使输出更紧凑。它特别适用于存储包含来自相关结构的重复数据的 JSON，例如 LLM 工具的日志。1.0 版本标志着经过实际使用后的稳定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/condense-json">GitHub - simonw/condense-json: Python function for condensing JSON using replacement strings · GitHub</a></li>
<li><a href="https://pypi.org/project/condense-json/">condense-json · PyPI</a></li>

</ul>
</details>

**标签**: `#JSON`, `#Python`, `#library`, `#release`

---