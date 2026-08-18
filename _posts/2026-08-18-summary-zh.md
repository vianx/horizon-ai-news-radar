---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 37 条内容中筛选出 12 条重要资讯。

---

1. [Mojo 编程语言在 Apache 2 许可下开源](#item-1) ⭐️ 9.0/10
2. [用 20 美元工具修复变砖的 Framework 笔记本，引发维修担忧](#item-2) ⭐️ 8.0/10
3. [Linux 7.3 在显存不足时提升性能](#item-3) ⭐️ 8.0/10
4. [OpenAI 启动国家安全 AI 民主监督计划](#item-4) ⭐️ 8.0/10
5. [Asana 借助 OpenAI Codex 在两周内完成五年工程工作量](#item-5) ⭐️ 8.0/10
6. [Qwen 3.8 27B 在智能指数上追平 GPT-5.6 Luna](#item-6) ⭐️ 8.0/10
7. [中国要求政府机构提前卸载定制版 Windows 10](#item-7) ⭐️ 8.0/10
8. [亚马逊广告驱动的搜索结果构成隐性“税”](#item-8) ⭐️ 7.0/10
9. [Turbovec：用 Rust 实现谷歌 TurboQuant 向量搜索](#item-9) ⭐️ 7.0/10
10. [冰岛食品公司讽刺管理顾问](#item-10) ⭐️ 7.0/10
11. [OpenAI 加强前沿 AI 开发的安全保障](#item-11) ⭐️ 7.0/10
12. [OpenAI 与 CodeAI 合作，为数百万青少年提供 AI 教育](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Mojo 编程语言在 Apache 2 许可下开源](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

Modular 已将 Mojo 编程语言开源，在 Apache 2 许可下发布了其编译器和工具链。这紧随上周 Mojo 1.0 的发布，并兑现了 2023 年 5 月做出的承诺。 这对开发者社区来说是一个重要里程碑，因为 Mojo 旨在结合 Python 的易用性和类似 C 的性能，特别是在 GPU 和 AI 工作负载方面。在宽松许可下开源可能会加速采用和社区贡献，可能重塑高性能计算和 AI 开发。 Mojo 最初旨在成为 Python 的超集，但该目标在 2025 年 8 月左右被放弃或无限期推迟。该语言现在专注于使用受 Python 启发的语法进行 GPU 编程，并基于 MLIR 编译器框架而非直接基于 LLVM。

rss · Simon Willison · 8月18日 21:39

**背景**: Mojo 是由 Modular Inc. 开发的系统编程语言，专为高性能 AI 基础设施和异构硬件设计。它使用类似 Python 的语法，但包含受 Rust 启发的静态类型和借用检查器。Apache 2 许可证是一种宽松的开源许可证，允许用户自由使用、修改和分发软件，限制极少。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language)</a></li>
<li><a href="https://www.apache.org/licenses/LICENSE-2.0.html">Apache License, Version 2.0 | Apache Software Foundation</a></li>
<li><a href="https://www.infoworld.com/article/4081105/revisiting-mojo-a-faster-python.html">Revisiting Mojo : A faster Python? | InfoWorld</a></li>

</ul>
</details>

**社区讨论**: Lobste.rs 上的讨论对开源表示兴奋，许多人注意到这一期待已久的承诺终于兑现。一些评论者对语言偏离 Python 超集兼容性的演变及其对 GPU 编程的潜在影响表示好奇。

**标签**: `#Mojo`, `#open source`, `#programming language`, `#compiler`, `#high-performance computing`

---

<a id="item-2"></a>
## [用 20 美元工具修复变砖的 Framework 笔记本，引发维修担忧](https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/) ⭐️ 8.0/10

quantum5.ca 的一篇详细博客文章记录了如何仅用价值 20 美元的工具成功修复一台因 BIOS 更新失败而变砖的 Framework 13 笔记本（AMD Ryzen 7040 系列）。文章强调了 BIOS 更新失败的普遍性，并呼吁制造商承担更多责任。 这个故事凸显了现代笔记本在 BIOS 更新过程中的脆弱性，以及维修权的重要性。它表明，借助易于获得的工具和知识，消费者可以修复那些制造商可能认为无法修复的设备，从而可能减少电子垃圾，并对保修政策提出挑战。 维修过程使用了价值 20 美元的工具包，可能包括芯片编程器和夹子，直接对 BIOS 芯片进行重新刷写。作者指出，BIOS 更新失败在 PC 制造商中仍然很常见，这个过程需要一定的技术技能，但对于有决心的用户来说是可行的。

hackernews · jp_sc · 8月18日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49345220)

**背景**: “变砖”的笔记本电脑是指完全无法使用的设备，通常是由于 BIOS/UEFI 固件更新失败所致。BIOS（基本输入输出系统）是启动时初始化硬件的固件；如果损坏，系统将无法启动。Framework Laptop 是一个模块化、可维修的笔记本品牌，但即使是它也可能会遇到此类故障。维修权倡导者认为，制造商应提供工具和文档，以便用户自行维修，从而减少电子垃圾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://community.frame.work/t/fw16-laptop-bois-update-failed-but-not-4-0-1-4-0-2-successfull-but-not-on-first-try/79151">FW16 Laptop BOIS Update failed but not... 4.0.1 -> 4.0.2 (Successfull...</a></li>
<li><a href="https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/">Fixing a bricked AMD 7040 series Framework 13” laptop with $20 tools</a></li>
<li><a href="https://thetechylife.com/can-a-bricked-pc-be-fixed/">Reviving a Bricked PC: Is It Possible to Fix a Dead Computer?</a></li>

</ul>
</details>

**社区讨论**: 评论者对制造商表示不满，有人建议对导致故障的 BIOS 更新采取法律行动，并指出此类失败仍然很常见。其他人则因零件供应有限和库存问题而后悔购买 Framework，还有用户提议安装官方更新应延长保修期。

**标签**: `#hardware`, `#repair`, `#Framework Laptop`, `#BIOS`, `#right-to-repair`

---

<a id="item-3"></a>
## [Linux 7.3 在显存不足时提升性能](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

Linux 内核 7.3 版本引入了针对显存不足情况的性能改进，解决了 GPU 内存耗尽时系统卡顿的长期问题。这一改动引发了社区的广泛讨论和期待。 这一改进对使用显存有限的 GPU 的游戏玩家、内容创作者和开发者意义重大，可以减少卡顿并提升系统响应速度。同时，它也凸显了 Linux 内核在内存管理上的积极主动，与用户常常畏惧的 Windows 更新形成鲜明对比。 该改进可能涉及更高效地处理显存超量分配，可能通过更优的驱逐策略或改进与 GTT（图形转换表）的交互。社区评论提到需要 Nvidia 支持，因为 Nvidia 目前缺乏分页支持，并讨论了潜在的内存碎片整理策略。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: VRAM（显存）是 GPU 上的专用内存，用于存储纹理、帧缓冲和其他图形数据。当显存满时，内核必须决定是将数据驱逐到系统内存（通过 GTT）还是使分配失败，这可能导致崩溃。Linux 一直在改进显存管理，近期 Valve 工程师 Natalie Vock 的补丁专注于保护前台应用并使用 cgroups 进行动态优先级分配。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://pixelcluster.dev/VRAM-Mgmt-fixed/">Fixing AMDGPU's VRAM management for low-end GPUs | pixelcluster's GPU blog</a></li>
<li><a href="https://www.xda-developers.com/a-valve-engineer-just-stopped-linux-from-stealing-vram-from-your-8gb-gpu/">A Valve engineer just stopped Linux from stealing VRAM from your 8GB GPU</a></li>
<li><a href="https://www.techpowerup.com/348178/valve-engineer-improves-linux-memory-management-for-gpus-with-8-gb-vram-or-less">Valve Engineer Improves Linux Memory Management for GPUs with 8 GB VRAM or Less | TechPowerUp</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户称赞这一改进并对即将发布的版本表示期待。一些用户希望类似修复能应用于内存耗尽问题，另一些则指出 Nvidia 缺乏分页支持，并建议内核级内存碎片整理。还有用户对开发者的努力表示赞赏，并与 Windows 更新文化形成对比。

**标签**: `#Linux`, `#VRAM`, `#performance`, `#kernel`, `#memory management`

---

<a id="item-4"></a>
## [OpenAI 启动国家安全 AI 民主监督计划](https://openai.com/index/strengthening-democratic-oversight-in-national-security) ⭐️ 8.0/10

OpenAI 启动了一项计划，以加强国家安全领域 AI 的民主监督，为政府机构提供工具、培训和专业知识。该公告是在此前“AI 的民主输入”计划之后发布的，该计划资助了 AI 规则制定民主过程的实验。 该计划意义重大，因为它解决了随着 AI 日益融入国家安全领域而对治理框架日益增长的需求。它可能为私营 AI 公司如何与政府合作以确保问责制和民主监督树立先例，影响政策和公众信任。 该计划包括向政府机构提供工具、培训和专业知识，但具体细节尚未披露。它建立在 OpenAI 早先的“AI 的民主输入”计划之上，该计划为 AI 规则制定的民主过程实验提供了十笔 10 万美元的资助。

rss · OpenAI Blog · 8月18日 19:00

**背景**: 国家安全领域的 AI 治理是一个紧迫的问题，因为 AI 系统越来越多地用于国防和情报，引发了关于问责制和民主控制的担忧。OpenAI 的计划旨在通过支持民主监督机制来解决这些问题。更广泛的背景包括关于私营 AI 公司在国防中定义操作边界的争论，例如 Anthropic 的 AI 被标记为国家安全风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/democratic-inputs-to-ai/">Democratic inputs to AI | OpenAI</a></li>
<li><a href="https://time.com/6684266/openai-democracy-artificial-intelligence/">time.com/6684266/ openai - democracy -artificial-intelligence</a></li>
<li><a href="https://www.linkedin.com/posts/openai_democratic-inputs-to-ai-activity-7067584596900548608-fefq">Democratic inputs to AI | OpenAI | 416 comments</a></li>

</ul>
</details>

**社区讨论**: 社区对 OpenAI 相关的“AI 的民主输入”计划的评论大多积极，称赞该计划具有开创性，并激励了 AI 引导的民主化。一些人强调了约束性过程而非咨询性磋商的重要性，正如查塔姆研究所的一位成员所指出的。

**标签**: `#AI governance`, `#national security`, `#OpenAI`, `#policy`

---

<a id="item-5"></a>
## [Asana 借助 OpenAI Codex 在两周内完成五年工程工作量](https://openai.com/index/asana) ⭐️ 8.0/10

Asana 使用 OpenAI Codex 在短短两周内替换了一个过时的测试系统，完成了预计需要五年才能完成的工作，成本约为 12,000 美元。 这一案例研究展示了 AI 辅助编程的变革潜力，表明复杂的工程任务可以大幅加速并显著节省成本。它凸显了一个日益增长的趋势，即像 Codex 这样的 AI 代理正成为软件开发团队的重要工具。 该项目涉及替换过时的测试系统，这通常需要大量人工投入。约 12,000 美元的成本包括使用 Codex 的费用，Codex 可通过 ChatGPT、CLI、桌面应用和 IDE 集成使用。

rss · OpenAI Blog · 8月18日 07:00

**背景**: OpenAI Codex 是一款 AI 编程代理，专为编写代码和修复错误等软件工程任务而设计。它于 2025 年 4 月以 Codex CLI 形式发布，可通过多种界面使用，使开发人员能够自动化编码工作流程。这一案例研究展示了 AI 代理如何处理以前耗时且资源密集的大规模重构和现代化项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/asana/">Asana cleared 5 years of engineering work in 2 weeks with Codex | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software Engineering | OpenAI</a></li>

</ul>
</details>

**标签**: `#AI coding`, `#OpenAI Codex`, `#software engineering`, `#productivity`, `#case study`

---

<a id="item-6"></a>
## [Qwen 3.8 27B 在智能指数上追平 GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 8.0/10

Qwen 3.8 27B，一个 270 亿参数的模型，在 Artificial Analysis 智能指数上获得 52 分，与 GPT-5.6 Luna（max）持平，仅比 GLM-5.2（max）和 DeepSeek V4 Pro 0813（max）低一分。这一结果由 Simon Willison 于 2026 年 8 月 17 日报道。 这一成果意义重大，因为一个相对较小的 27B 模型达到了与更大模型（GLM-5.2 为 753B，DeepSeek V4 Pro 为 1.7T）相当的性能，凸显了 AI 领域的重大效率突破。它可能使高质量 AI 更加普及，能够在消费级硬件上部署并降低成本。 Artificial Analysis 智能指数 v4.1.1 包含 GDPval-AA v2、Terminal-Bench v2.1、SciCode、Humanity's Last Exam、GPQA Diamond 等基准测试。Qwen 3.8 27B 是阿里巴巴 Qwen 系列中的指令微调模型，专为视觉、文本生成和智能体工作负载而设计。

rss · Simon Willison · 8月17日 23:58

**背景**: Artificial Analysis 智能指数是一个综合衡量模型“智能”的指标，已发展到包含智能体能力和长上下文推理。Qwen 3.8 27B 是阿里巴巴开源权重 Qwen 系列的一部分，该系列因其相对于模型尺寸的强劲性能而备受关注。该模型的自报基准显示其优于先前版本，独立基准测试现在也证实了其能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://simonwillison.net/2026/Aug/16/qwen-38-27b/">Qwen 3.8 27B is excellent, but it defaults to wildly ...</a></li>

</ul>
</details>

**社区讨论**: 文章引用的 Hacker News 讨论可能对 Qwen 3.8 27B 的效率表示惊讶和兴奋，一些用户指出这对本地部署和成本降低的影响。但由于没有直接评论，情绪是从文章语气和模型的接受度推断的。

**标签**: `#AI`, `#LLMs`, `#Qwen`, `#model efficiency`, `#benchmark`

---

<a id="item-7"></a>
## [中国要求政府机构提前卸载定制版 Windows 10](https://www.bloomberg.com/news/articles/2026-08-18/china-axing-microsoft-windows-from-state-agencies-ahead-of-plan) ⭐️ 8.0/10

中国国家安全部已要求部分政府相关机构卸载定制版 Windows 10，将原定 2027 年 2 月的停用计划提前至更早时间。该指令源于数据安全担忧，但未指明具体漏洞。 此举加速了中国减少对美国技术依赖的努力，可能影响微软在中国政府领域的存在，并表明数据安全审查更加严格。这也可能影响其他国家的采购决策，加剧地缘政治技术紧张局势。 定制版 Windows 10 由微软中国与神州网信联合开发，于 2016 年推出以满足中国的安全要求。微软表示，未发现影响该产品的安全事件，该产品仍在定期获得安全更新。

telegram · zaihuapd · 8月18日 06:22

**背景**: 中国一直在推动技术自主，特别是在政府和国有部门，以减少对外国技术的依赖。定制版 Windows 10 是微软在中国运营并满足当地安全要求的折中方案。这一指令与推广麒麟、统信 UOS 等国产操作系统的更广泛努力相一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/software/operating-systems/china-reportedly-orders-state-agencies-to-uninstall-its-government-only-edition-of-windows-10">China reportedly orders state agencies to uninstall ... | Tom's Hardware</a></li>
<li><a href="https://www.straitstimes.com/asia/east-asia/china-removes-microsoft-windows-at-state-users-ahead-of-plan">China removes Microsoft Windows at state users... | The Straits Times</a></li>
<li><a href="https://wccftech.com/china-state-agencies-uninstall-windows-10-cmit-government-edition/">China ’s State-Linked Firms Are Moving Away From Windows 10 Due...</a></li>

</ul>
</details>

**社区讨论**: 提供的评论很少，但 Telegram 帖子强调这是微软在中国的又一次挫折，并强调了与神州网信的联合开发。没有详细的社区讨论。

**标签**: `#cybersecurity`, `#geopolitics`, `#Microsoft`, `#Windows 10`, `#data security`

---

<a id="item-8"></a>
## [亚马逊广告驱动的搜索结果构成隐性“税”](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 7.0/10

Seth Godin 认为，亚马逊的搜索广告每周产生近十亿美元的利润，通过优先展示赞助产品而非最佳选项，扭曲了搜索结果，对消费者构成了一种隐性“税”。这篇文章引发了社区的热烈讨论，获得 842 分和 509 条评论。 这一批评凸显了电子商务中广告伦理日益增长的担忧，即为了利润而损害消费者的信任和选择。它可能影响监管审查和消费者行为，并引发关于针对欺骗性广告行为的法律补救措施的讨论。 据 Godin 称，亚马逊每周从搜索广告中获利近十亿美元。社区成员指出，按“畅销榜”排序可以消除广告，一些人建议采取商标侵权和欺诈索赔等法律途径。

hackernews · herbertl · 8月18日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49345263)

**背景**: 亚马逊是一个主要的电子商务平台，赞助产品很常见。赞助产品是按点击付费的广告，出现在搜索结果中，通常位于顶部，这可能会将自然结果下移。这种做法因误导消费者并可能抬高价格而受到批评，因为卖家将广告成本转嫁给买家。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://seths.blog/2026/08/the-amazon-tax/">The Amazon tax | Seth's Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Amazon_(company)">Amazon (company) - Wikipedia</a></li>
<li><a href="https://www.sellerapp.com/blog/amazon-sponsored-products-vs-sponsored-brands/">Amazon Sponsored Products vs. Amazon Sponsored Brands...</a></li>

</ul>
</details>

**社区讨论**: 社区意见分歧：一些人认为广告是商业的正常组成部分，也是新产品获得曝光的方式，而另一些人则认为广告具有欺骗性，并建议通过按畅销榜排序等变通方法。有人提议采取法律行动，商标侵权和欺诈是潜在的主张。

**标签**: `#Amazon`, `#advertising`, `#e-commerce`, `#consumer protection`, `#search`

---

<a id="item-9"></a>
## [Turbovec：用 Rust 实现谷歌 TurboQuant 向量搜索](https://github.com/RyanCodrai/turbovec) ⭐️ 7.0/10

Turbovec 是谷歌 TurboQuant 算法在 Rust 中的一个新实现，用于向量搜索，仅用 4GB 内存即可处理 1000 万文档。它旨在将高效的近似最近邻（ANN）搜索引入 Rust 生态系统，并保持低内存占用。 该项目可显著提升 Rust 构建的向量搜索应用的性能和内存效率，成为 FAISS 和 Qdrant 等现有解决方案的有力替代。它也表明 TurboQuant 在谷歌自家系统之外的采用日益广泛，可能影响整个向量数据库和语义搜索领域。 Turbovec 利用 TurboQuant 的两阶段压缩（PolarQuant 用于方向，QJL 用于残差），实现每通道约 3.5 比特的压缩，同时保持与 FP16 相当的质量。该项目在 GitHub 上开源，社区对其潜在的 WASM 编译和 SQLite 绑定表现出兴趣。

hackernews · fittingopposite · 8月18日 18:07 · [社区讨论](https://news.ycombinator.com/item?id=49349898)

**背景**: 向量搜索是一种利用机器学习将非结构化数据表示为数值向量的技术，通过近似最近邻（ANN）等算法实现相似性搜索。TurboQuant 是谷歌研究院推出的一种压缩方法，在几乎不损失精度的情况下减小模型大小和内存占用，最初用于 KV 缓存压缩，但也适用于向量搜索。Rust 是一种以性能和内存安全著称的系统编程语言，非常适合实现高性能的向量搜索库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/turboquant-redefining-ai-efficiency-with-extreme-compression/">TurboQuant : Redefining AI efficiency with extreme compression</a></li>
<li><a href="https://turbo-quant.com/turboquant">TurboQuant Algorithm : PolarQuant + QJL Explained for Developers</a></li>
<li><a href="https://www.elastic.co/what-is/vector-search">What is vector search? Better search with ML | Elastic</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调了该项目令人印象深刻的内存效率及其在本地、隐私优先搜索中的潜力，一些用户期待 SQLite 绑定和 WASM 编译。然而，有评论者质疑在 Qdrant 已集成 TurboQuant 的情况下为何还需要新实现，还有人建议 README 可以更人性化以促进采用。

**标签**: `#vector search`, `#Rust`, `#TurboQuant`, `#ANN`, `#performance`

---

<a id="item-10"></a>
## [冰岛食品公司讽刺管理顾问](https://about.iceland.co.uk/our-story/the-dark-ages/beware-management-consultants/) ⭐️ 7.0/10

冰岛食品公司在其网站上发布了一个题为“当心管理顾问”的讽刺幻灯片，嘲讽管理顾问的做法。该演示文稿在 Hacker News 上迅速传播，引发了热烈讨论，获得 416 分和 110 条评论。 这种讽刺性观点引起了许多科技和商业界人士的共鸣，他们曾经历过管理咨询的弊端，如高成本和价值存疑。它突出了一个常见的行业痛点，并引发了对顾问在现代组织中角色的反思。 该幻灯片故意采用糟糕的用户体验设计，迫使读者认真阅读内容，一位评论者指出这能有效防止略读。讨论中包括前顾问的个人经历以及对管理层依赖外部建议的批评。

hackernews · KolmogorovComp · 8月18日 19:29 · [社区讨论](https://news.ycombinator.com/item?id=49351324)

**背景**: 管理顾问是组织聘请的外部专家，就战略、运营或技术提供建议。虽然他们能带来专业知识，但常因收费高昂、建议千篇一律和缺乏责任感而受到批评。英国超市连锁冰岛食品公司通过讽刺表达了对这一行业做法的不满。

**社区讨论**: 评论者观点不一：一些人捍卫顾问，称其在复杂项目中有价值，而另一些人则批评该行业激励错位和过度依赖。一位评论者指出，故意糟糕的用户体验让他读完了整个内容，另一位则反思自己在类似内部治理工作中的角色。

**标签**: `#management consulting`, `#satire`, `#tech industry`, `#organizational behavior`

---

<a id="item-11"></a>
## [OpenAI 加强前沿 AI 开发的安全保障](https://openai.com/index/pacing-model-development-cyber-capabilities) ⭐️ 7.0/10

OpenAI 宣布加强监控、对齐和安全措施，以指导前沿 AI 模型的开发节奏，特别是针对网络关键能力。此前，该公司曾表示其即将推出的 Astra 模型可能已达到网络安全方面的“关键”能力。 这标志着前沿 AI 实验室在管理先进模型风险方面的战略转变，可能为行业树立主动安全措施的先例。它可能影响监管讨论以及其他 AI 开发者处理模型部署和节奏的方式。 该公告缺乏具体的技术细节，但提到了 2023 年 12 月首次发布的“准备框架”，该框架指导公司在能力出现时的应对措施。OpenAI 尚未排除其 Astra 模型可能对复杂防御系统发起网络攻击的可能性，因此加强了这些保障措施。

rss · OpenAI Blog · 8月18日 11:00

**背景**: 前沿 AI 模型是最先进的 AI 系统，使用极大的计算预算进行训练，并能在多个领域超越现有技术水平。AI 对齐是指将人类价值观和目标编码到这些模型中，使其安全可靠。随着模型接近网络关键能力，像 OpenAI 这样的实验室必须在创新与安全之间取得平衡，通常使用“准备框架”等工具来评估和缓解风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-alignment">What Is AI Alignment? | IBM</a></li>
<li><a href="https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/">Responding to the next frontier of critical cyber capabilities</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#frontier AI`, `#OpenAI`, `#cybersecurity`, `#model development`

---

<a id="item-12"></a>
## [OpenAI 与 CodeAI 合作，为数百万青少年提供 AI 教育](https://openai.com/index/chatgpt-for-teens/) ⭐️ 6.0/10

OpenAI 于 2026 年 8 月 18 日宣布与 CodeAI 合作，帮助学生和教师学习负责任地使用 AI，同时推出 ChatGPT for Teens。合作将包括联合咨询委员会、AI 素养课程、学生挑战赛和职业项目，目标是在未来一年覆盖数百万学生。 这一举措可能显著提升青少年的 AI 素养，为他们迎接 AI 驱动的未来做好准备。同时，它通过引入安全功能和家长控制，回应了人们对青少年使用 AI 的担忧，可能为教育类 AI 产品树立标准。 ChatGPT for Teens 包含更强的内置安全保护、健康使用功能和额外的家长控制。合作还支持 CodeAI 开发免费的高中 AI Foundations 课程。

telegram · OpenAI Blog · 8月18日 12:06

**背景**: CodeAI 是 Code.org 更名后的名称，Code.org 是一家致力于扩大计算机科学教育覆盖面的非营利组织。OpenAI 的 ChatGPT for Teens 是专为青少年用户设计的新产品，具有学习模式等功能，以鼓励学习和批判性思维。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/chatgpt-for-teens/">Introducing ChatGPT for Teens: Built for learning, backed by ...</a></li>
<li><a href="https://code.org/en-US/codeai">Code.org is now CodeAI</a></li>
<li><a href="https://techcrunch.com/2026/08/18/openai-launches-a-safer-chatgpt-for-teens-years-after-teens-started-using-it/">OpenAI launches a safer ChatGPT for teens — years... | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI education`, `#OpenAI`, `#ChatGPT`, `#partnership`, `#youth`

---