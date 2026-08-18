---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 36 条内容中筛选出 12 条重要资讯。

---

1. [Mojo 编程语言在 Apache 2 许可下开源](#item-1) ⭐️ 9.0/10
2. [Turbovec：用 Rust 实现 Google 的 TurboQuant 向量搜索](#item-2) ⭐️ 8.0/10
3. [用 20 美元工具修复变砖的 Framework 笔记本，引发 BIOS 更新担忧](#item-3) ⭐️ 8.0/10
4. [Linux 7.3 在显存耗尽时提升性能](#item-4) ⭐️ 8.0/10
5. [OpenAI 以新的网络保障措施调整模型开发节奏](#item-5) ⭐️ 8.0/10
6. [Asana 借助 Codex 在两周内完成五年工程量](#item-6) ⭐️ 8.0/10
7. [Qwen 3.8 27B 在智能指数上追平 GPT-5.6 Luna](#item-7) ⭐️ 8.0/10
8. [国产 AI 芯片 2026 年将主导国内市场](#item-8) ⭐️ 8.0/10
9. [亚马逊广告驱动的搜索结果带来隐性成本](#item-9) ⭐️ 7.0/10
10. [冰岛食品公司讽刺管理顾问](#item-10) ⭐️ 7.0/10
11. [OpenAI 与 CodeAI 合作，为数百万青少年提供 AI 教育](#item-11) ⭐️ 6.0/10
12. [NVIDIA 借助 ChatGPT Work 扩展 AI 专业知识](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Mojo 编程语言在 Apache 2 许可下开源](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

Modular 已将 Mojo 编程语言开源，其编译器和工具链在 Apache 2 许可下发布。这紧随上周 Mojo 1.0 的发布，兑现了 2023 年 5 月做出的承诺。 Mojo 是人工智能和高性能计算领域备受期待的语言，其在宽松许可下开源可能会加速采用和社区贡献。此举也可能影响 Python 生态系统和 AI 工具的开发，因为 Mojo 旨在提供类似 Python 的语法和系统级性能。 Mojo 最初旨在成为 Python 的超集，但这一目标在 2025 年 8 月左右被放弃或推迟，现在它已成为一种独立的语言。它基于 MLIR 编译器框架构建，能够针对 CPU、GPU、TPU 和其他加速器，并融合了受 Rust 启发的静态类型和借用检查等特性。

rss · Simon Willison · 8月18日 21:39

**背景**: Mojo 是由 Modular 开发的一种编程语言，旨在将 Python 的易用性与 C++ 和 Rust 等系统语言的性能相结合。它利用 MLIR 编译器框架，为各种硬件生成高效代码，特别适合 AI 工作负载。Apache 2 许可是一种宽松的开源许可，允许用户自由使用、修改和分发软件，限制极少。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language)</a></li>
<li><a href="https://www.modular.com/blog/the-path-to-mojo-1-0">Modular: The path to Mojo 1.0</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apache_License">Apache License</a></li>

</ul>
</details>

**社区讨论**: 鉴于开源期待已久，Lobste.rs 上的讨论可能会很积极。社区成员可能会对社区驱动开发和改进的潜力表示兴奋，而有些人可能会讨论 Mojo 不再是 Python 超集的影响及其对 Python 兼容性的影响。

**标签**: `#Mojo`, `#open source`, `#programming language`, `#AI/ML`, `#compiler`

---

<a id="item-2"></a>
## [Turbovec：用 Rust 实现 Google 的 TurboQuant 向量搜索](https://github.com/RyanCodrai/turbovec) ⭐️ 8.0/10

Turbovec 是一个新的 Rust 库，将 Google 的 TurboQuant 向量搜索算法引入 Rust 生态系统，提供高效的内存使用和本地、隐私优先应用的潜力。它最近在 GitHub 上发布，并获得了社区的高度关注。 这意义重大，因为它将最先进的向量搜索算法引入 Rust，使开发者能够用系统级语言构建高性能、内存高效的搜索应用。它可能加速本地、隐私保护搜索解决方案的采用，并为现有向量数据库提供 Rust 原生替代方案。 据报道，该库处理 1000 万份文档仅需 4GB 内存，展示了其高效性。社区成员讨论了将其编译为 WASM 以用于浏览器扩展，并指出 Qdrant 已经整合 TurboQuant 数月，暗示了潜在的竞争或合作机会。

hackernews · fittingopposite · 8月18日 18:07 · [社区讨论](https://news.ycombinator.com/item?id=49349898)

**背景**: TurboQuant 是 Google 开发的一种压缩方法，能在零精度损失的情况下大幅减小模型大小，并用于 KV 缓存压缩和向量搜索。向量搜索，特别是近似最近邻（ANN）搜索，是向量数据库中用于高效查找与查询点最近数据点的技术，对图像和文本检索等应用至关重要。Rust 是一种以性能和内存安全著称的系统编程语言，因此非常适合实现此类算法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TurboQuant">TurboQuant - Wikipedia</a></li>
<li><a href="https://research.google/blog/turboquant-redefining-ai-efficiency-with-extreme-compression/">TurboQuant: Redefining AI efficiency with extreme compression</a></li>
<li><a href="https://www.mongodb.com/resources/basics/ann-search">What is Approximate Nearest Neighbor (ANN) Search? | MongoDB</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户称赞其内存效率和本地、隐私优先搜索的潜力。一些用户建议改进 README 以促进采用，而另一些用户则讨论了 Qdrant 等替代方案，后者已整合 TurboQuant。此外，还有人对将该库编译为 WASM 以用于浏览器表示好奇。

**标签**: `#vector search`, `#Rust`, `#TurboQuant`, `#ANN`, `#privacy`

---

<a id="item-3"></a>
## [用 20 美元工具修复变砖的 Framework 笔记本，引发 BIOS 更新担忧](https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/) ⭐️ 8.0/10

2026 年 8 月 16 日发布了一份详细指南，展示了如何仅用 20 美元的工具修复因 BIOS 更新（3.20 版）失败而变砖的 Framework 13 笔记本。该指南强调了恢复过程以及 BIOS 更新可靠性的更广泛问题。 这很重要，因为 BIOS 更新失败可能导致昂贵的笔记本变砖，造成电子垃圾和消费者不满。它强调了制造商需要承担更多责任、提供可靠的更新机制和便捷的维修选项，尤其是对于像 Framework 这样倡导可维修性的模块化笔记本。 该指南使用廉价工具（约 20 美元）来恢复笔记本，可能涉及硬件编程器来重新刷写 BIOS 芯片。失败的更新是 3.20 版，由 Framework 通过新闻通讯推荐，刷写过程中系统挂起并显示损坏图像。

hackernews · jp_sc · 8月18日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49345220)

**背景**: BIOS（基本输入输出系统）是启动时初始化硬件的固件。BIOS 更新失败可能导致设备“变砖”，无法使用。许多制造商提供恢复方法，但通常需要专业技术或特定硬件。Framework 以其模块化、可维修的笔记本而闻名，但这次事件表明即使是这类设备也可能遇到 BIOS 更新问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.adafruit.com/2026/08/18/fixing-a-bricked-framework-laptop/">Fixing a bricked Framework laptop - Adafruit Industries</a></li>
<li><a href="https://community.frame.work/t/two-bricked-devices-after-bios-updates-how-can-i-escalate-my-support-request/84047">Two bricked devices after BIOS updates - how can I escalate ...</a></li>
<li><a href="https://www.dell.com/support/kbdoc/en-us/000132453/how-to-recover-the-bios-on-a-dell-computer-or-tablet">Recover BIOS on Dell Computer or Tablet After Boot or POST ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对制造商的不满，有人建议对错误的 BIOS 更新采取法律行动（如小额索赔法院）。其他人分享了其他品牌的类似经历，还有人后悔购买 Framework，因为零件市场缺乏竞争且存在库存问题。也有人呼吁当官方更新导致问题时延长保修期。

**标签**: `#hardware`, `#repair`, `#BIOS`, `#Framework`, `#consumer-rights`

---

<a id="item-4"></a>
## [Linux 7.3 在显存耗尽时提升性能](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

Linux 内核 7.3 引入了针对显存耗尽场景的性能改进，相关内核补丁集已合并到上游并计划在 7.3 中发布。该增强专注于更好的后台显存管理，尤其有利于显存为 8 GB 或更低的 GPU。 这一改进解决了显存有限的游戏玩家和专业用户的常见痛点，在显存耗尽时减少卡顿和崩溃。它也凸显了 Linux 内核开发的主动性，与 Windows 的更新模式形成对比，并可能影响 GPU 内存管理的标准。 该补丁集包含六个补丁，改进了显存超卖处理，但仍需用户空间工具如 dmemcg-booster。内核可能会偶尔就地整理虚拟内存碎片，这可能导致明显的卡顿，但能提升整体性能。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: 显存（VRAM）是 GPU 上的专用内存，当它耗尽时，系统必须回退到系统内存，这会更慢并导致性能下降。Linux 内核开发者一直在改进显存管理，特别是对于显存有限的 GPU，以提升游戏和计算性能。内核中的 TTM（Translation Table Maps）子系统负责内存放置和驱逐的管理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49342719">Linux 7.3 improves performance when running out of vRAM | Hacker News</a></li>
<li><a href="http://pixelcluster.dev/VRAM-Mgmt-fixed/">Fixing AMDGPU's VRAM management for low-end GPUs | pixelcluster's GPU blog</a></li>
<li><a href="https://www.techpowerup.com/348178/valve-engineer-improves-linux-memory-management-for-gpus-with-8-gb-vram-or-less">Valve Engineer Improves Linux Memory Management for GPUs with 8 GB VRAM or Less | TechPowerUp</a></li>

</ul>
</details>

**社区讨论**: 社区对这一改进反应热烈，用户称赞内核开发速度和作者的工作。一些使用 Nvidia 硬件的用户对缺乏分页支持表示沮丧，而其他人则讨论内存碎片化问题以及应用程序在内存分配中的作用。

**标签**: `#Linux`, `#VRAM`, `#performance`, `#kernel`, `#memory management`

---

<a id="item-5"></a>
## [OpenAI 以新的网络保障措施调整模型开发节奏](https://openai.com/index/pacing-model-development-cyber-capabilities) ⭐️ 8.0/10

OpenAI 宣布了新的保障措施，以指导前沿 AI 模型开发的节奏，重点加强监控、对齐和安全性。该举措还包括为政府机构提供工具和培训，以支持在国家安全领域对 AI 的民主监督。 这标志着前沿 AI 开发者在管理网络关键能力方面发生了重大转变，可能为负责任的开发节奏树立行业先例。它可能影响整个生态系统的 AI 政策和安全实践，影响开发者、政策制定者和公众。 这些保障措施包括在模型开发过程中进行更详细的监控，并在后训练阶段更加强调对齐和安全性，正如 TechCrunch 最近报道的那样。OpenAI 还启动了一项举措，以加强国家安全领域 AI 的民主监督，为政府机构提供工具、培训和专业知识。

rss · OpenAI Blog · 8月18日 11:00

**背景**: 前沿 AI 模型是先进的系统，其能力如果被滥用可能会带来风险，尤其是在网络安全领域。AI 对齐确保这些系统追求人类预期的目标，而监控有助于检测对齐偏差。OpenAI 于 2026 年 5 月宣布的“前沿治理框架”概述了与新兴法规一致的安全实践，而这一新公告正是建立在该框架的基础上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/pacing-model-development-cyber-capabilities/">Pacing model development in an era of cyber-critical ... - OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/08/18/openai-institutes-new-safeguards-after-hugging-face-breach/">OpenAI institutes new safeguards after Hugging Face breach</a></li>
<li><a href="https://openai.com/index/openai-frontier-governance-framework/">OpenAI’s Frontier Governance Framework</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#OpenAI`, `#frontier models`, `#cybersecurity`, `#AI policy`

---

<a id="item-6"></a>
## [Asana 借助 Codex 在两周内完成五年工程量](https://openai.com/index/asana) ⭐️ 8.0/10

Asana 使用 OpenAI Codex 在短短两周内替换了过时的测试系统，完成了预计需要五年才能完成的工作，成本约为 12,000 美元。 这一案例研究凸显了 AI 编程代理在软件工程中的变革潜力，展示了显著的生产力提升和成本节约。这可能会鼓励更多公司采用 AI 驱动的开发工具，重塑工程团队处理遗留系统迁移的方式。 该项目涉及替换过时的测试系统，最初估计需要五年时间。这项工作在两周内完成，成本约为 12,000 美元，展示了 Codex 高效处理大规模、复杂工程任务的能力。

rss · OpenAI Blog · 8月18日 07:00

**背景**: OpenAI Codex 是一个轻量级编码代理，可在开发者的本地计算机上运行，能够自动化编码任务。它是 AI 辅助开发工具这一更广泛趋势的一部分，旨在通过处理重复或复杂的编码工作来提高程序员的生产力。Asana 是一家项目管理软件公司，很可能使用 Codex 来现代化其测试基础设施，这是成长中的科技公司面临的常见挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>
<li><a href="https://chatgpt.com/ru-RU/codex/">Codex в ChatGPT | ИИ-агенты для написания кода и разработки ПО</a></li>

</ul>
</details>

**标签**: `#AI coding`, `#OpenAI Codex`, `#software engineering`, `#productivity`, `#case study`

---

<a id="item-7"></a>
## [Qwen 3.8 27B 在智能指数上追平 GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 8.0/10

Qwen 3.8 27B，一个 270 亿参数的模型，在 Artificial Analysis 智能指数上获得 52 分，追平了 GPT-5.6 Luna（max），仅比 GLM-5.2（753B）和 DeepSeek V4 Pro（1.7T）低 1 分。Simon Willison 于 2026 年 8 月 17 日报道了这一消息。 这意义重大，因为一个相对较小的 270 亿参数模型能达到与参数多出数十倍甚至数百倍的模型相当的性能，标志着 AI 效率的重大里程碑。这可能使高质量 AI 的获取更加普及，能够在消费级硬件上部署，并降低企业成本。 Artificial Analysis 智能指数 v4.1.1 包含 GDPval-AA v2、Terminal-Bench v2.1 和 Humanity's Last Exam 等基准测试。Qwen 3.8 27B 在评估期间生成了 1.6 亿个 token，与中位数的 4300 万个 token 相比明显冗长。

rss · Simon Willison · 8月17日 23:58

**背景**: Artificial Analysis 智能指数是一个综合衡量模型“智能”的指标，已发展到包含代理能力和长上下文推理。Qwen 3.8 27B 是阿里巴巴 Qwen 团队的开源权重模型，以相对较小的规模实现强大性能而闻名。GLM-5.2 和 DeepSeek V4 Pro 是更大的开源权重模型，其中 GLM-5.2 采用混合专家架构，总参数 7530 亿，但每个 token 仅激活 400 亿参数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/qwen3-8-27b">Qwen 3 . 8 27 B - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen / Qwen 3 . 8 - 27 B · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（条目 49334544）可能强调了 Qwen 3.8 27B 令人印象深刻的效率及其对本地 AI 部署的影响。一些评论者可能对基准测试的可靠性表示怀疑，或注意到其高 token 生成冗长性。

**标签**: `#AI`, `#LLMs`, `#Qwen`, `#model efficiency`, `#benchmarks`

---

<a id="item-8"></a>
## [国产 AI 芯片 2026 年将主导国内市场](https://www.tomshardware.com/tech-industry/artificial-intelligence/chinas-homegrown-ai-accelerators-to-supply-90-percent-of-the-countrys-domestic-market-analysts-suggest-cambricon-and-huawei-expected-to-be-the-biggest-winners-in-the-shift-away-from-nvidia-and-amd) ⭐️ 8.0/10

TrendForce 预测，到 2026 年，中国国产 AI 加速器将占据国内市场的近 90%，高于去年的 45%。在这一从英伟达和 AMD 转移的趋势中，寒武纪和华为预计将成为最大赢家。 这标志着中国 AI 芯片市场的重大战略转变，在美国出口管制下减少对外国供应商的依赖。这可能重塑全球 AI 芯片格局，并推动寒武纪和华为等本土企业的发展。 2025 年，英伟达以 220 万颗占据中国市场 55%的份额，而华为出货 81.2 万颗，占 20.3%。为实现 2026 年的目标，中国必须将高端 AI 芯片产量提升 2.2 倍至约 196 万颗，这引发了关于产能的疑问。

telegram · zaihuapd · 8月18日 13:03

**背景**: AI 加速器是专为加速 AI 计算而设计的硬件，对于数据中心的训练和推理至关重要。由于美国对先进芯片的出口管制，中国一直在推动半导体自给自足，这促进了寒武纪和华为等本土企业的发展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/chinas-homegrown-ai-accelerators-to-supply-90-percent-of-the-countrys-domestic-market-analysts-suggest-cambricon-and-huawei-expected-to-be-the-biggest-winners-in-the-shift-away-from-nvidia-and-amd">China's homegrown AI accelerators to supply 90% of the country's domestic market, analysts suggest — Cambricon and Huawei expected to be the biggest winners in the shift away from Nvidia and AMD | Tom's Hardware</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/cambricon-targets-500000-ai-chips-in-2026-as-china-accelerates-domestic-hardware-push">Cambricon targets 500,000 AI chips in 2026 as China accelerates domestic hardware push — low yields and limited HBM supply could threaten chip ambitions | Tom's Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cambricon_Technologies">Cambricon Technologies - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#China`, `#semiconductors`, `#market analysis`, `#Huawei`

---

<a id="item-9"></a>
## [亚马逊广告驱动的搜索结果带来隐性成本](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 7.0/10

Seth Godin 的文章《亚马逊税》指出，亚马逊广告驱动的搜索结果给消费者和出版商带来了隐性成本，引发了关于此类做法伦理和合法性的讨论。 这很重要，因为它影响消费者信任和购买决策，并引发对电子商务平台透明度和公平性的质疑。它可能影响监管审查和消费者权益倡导。 文章指出，亚马逊的广告可能优先展示竞争对手而非用户搜索的确切产品，并提到亚马逊广告成本大幅上升，2026 年平均每次点击费用达到 1.18 美元。这给消费者带来了“税”，他们可能最终支付更多或购买次优产品。

hackernews · herbertl · 8月18日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49345263)

**背景**: 亚马逊是一个占主导地位的电子商务平台，卖家为搜索结果中的广告位付费。这些广告可能影响消费者的选择，而广告成本的上升对卖家和消费者都构成担忧。争论的焦点在于这种做法是否合乎道德，以及是否违反消费者保护法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://epinium.com/en/blog/amazon-advertising-cost/">Amazon Advertising Cost: CPC Benchmarks 2026 | Epinium</a></li>
<li><a href="https://epinium.com/en/blog/amazon-search-engine-advertising-costs/">Amazon Search Engine Advertising Costs | Epinium</a></li>
<li><a href="https://sellermetrics.app/cost-of-amazon-ads/">How much are Amazon Ads? Amazon Advertising Cost: 2026</a></li>

</ul>
</details>

**社区讨论**: 评论观点不一：有人认为广告可以相关且有益，而另一些人则认为它们可能侵犯商标或误导消费者。还有关于广告在电子商务中的合法性和作用的讨论。

**标签**: `#Amazon`, `#advertising`, `#e-commerce`, `#consumer behavior`, `#ethics`

---

<a id="item-10"></a>
## [冰岛食品公司讽刺管理顾问](https://about.iceland.co.uk/our-story/the-dark-ages/beware-management-consultants/) ⭐️ 7.0/10

冰岛食品公司在其网站上发布了一个题为“当心管理顾问”的讽刺幻灯片，嘲弄管理顾问的做法和行话。该作品在 Hacker News 上引起关注，引发了关于咨询价值和陷阱的讨论。 这种讽刺引起了许多经历过咨询负面影响的专业人士的共鸣，例如高成本和泛泛而谈的建议。它凸显了对管理咨询的更广泛怀疑，这可能影响公司评估使用外部顾问的方式。 幻灯片故意使用糟糕的用户体验设计来吸引读者，正如评论中所指出的。它是冰岛食品公司“黑暗时代”系列的一部分，该系列似乎是对企业生活的幽默解读。该作品没有提供具体例子，而是依赖于常见的咨询刻板印象。

hackernews · KolmogorovComp · 8月18日 19:29 · [社区讨论](https://news.ycombinator.com/item?id=49351324)

**背景**: 管理咨询是一个价值数十亿美元的行业，公司为组织提供战略、运营和管理方面的建议。批评者经常认为顾问提供泛泛的建议、缺乏责任感且成本高昂，而支持者则声称他们带来专业知识和客观性。这种讽刺利用了这些持续的争论。

**社区讨论**: Hacker News 上的评论褒贬不一。一些用户分享了与顾问合作的积极经验，指出他们在复杂项目中提供了价值。其他人则批评咨询行业，认为激励措施错位以及管理层对顾问的迷恋。一位用户欣赏这种故意的糟糕用户体验，而另一位则反思自己在类似工作中的角色。

**标签**: `#management consulting`, `#satire`, `#business`, `#critique`, `#workplace`

---

<a id="item-11"></a>
## [OpenAI 与 CodeAI 合作，为数百万青少年提供 AI 教育](https://openai.com/index/chatgpt-for-teens/) ⭐️ 6.0/10

2026 年 8 月 18 日，OpenAI 宣布与 CodeAI（原 Code.org）合作，帮助学生和教师学习负责任地使用 AI，同时推出带有增强安全功能和家长控制的 ChatGPT for Teens。未来一年，双方将通过联合咨询委员会、AI 素养课程、学生挑战赛和职业项目，覆盖数百万学生。 此次合作意义重大，旨在为下一代提供必要的 AI 技能，满足教育领域日益增长的 AI 素养需求。同时，这也扩大了 OpenAI 在青少年市场的影响力，可能影响年轻人学习和使用 AI 技术的方式。 合作包括由 CodeAI 开发免费的高中 AI Foundations 课程，并得到 OpenAI 的支持。ChatGPT for Teens 对 18 岁以下用户默认启用安全保护，包括健康使用功能和额外的家长控制，即使在年龄不确定时也会提供更安全的体验。

telegram · OpenAI Blog · 8月18日 12:06

**背景**: CodeAI 前身为 Code.org，是由 Hadi 和 Ali Partovi 创立的非营利组织，致力于扩大计算机科学教育的覆盖面。OpenAI 的 ChatGPT for Teens 是专为年轻用户设计的 AI 聊天机器人版本，内置保护措施以确保安全和负责任的使用。此次合作反映了将 AI 素养融入 K-12 教育的更广泛趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/chatgpt-for-teens/">Introducing ChatGPT for Teens: Built for learning, backed by ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Code.org">Code .org - Wikipedia</a></li>
<li><a href="https://chatgpt.com/parent-resources/safety-protections/">Teen default safety protections - chatgpt.com</a></li>

</ul>
</details>

**标签**: `#AI education`, `#OpenAI`, `#partnership`, `#ChatGPT`, `#youth`

---

<a id="item-12"></a>
## [NVIDIA 借助 ChatGPT Work 扩展 AI 专业知识](https://openai.com/index/nvidia/chatgpt-work) ⭐️ 6.0/10

NVIDIA 已采用由 Codex 和 GPT-5.6 驱动的智能体 AI 工具 ChatGPT Work，以自动化任务并在全球团队中扩展成功的工作流程。OpenAI 发布的案例研究强调了 NVIDIA 如何减少手动工作并连接快速变化的信号。 这一采用标志着企业使用智能体 AI 来简化运营和扩展专业知识的趋势日益增长。它为大型组织展示了实际价值，可能影响工作场所中 AI 的更广泛采用。 ChatGPT Work 是一个智能体，可以在应用和文件之间采取行动，持续处理项目数小时，并将目标转化为完成的工作。它是 ChatGPT Enterprise 的一部分，提供企业级安全、集中管理和高级工具。

rss · OpenAI Blog · 8月18日 00:00

**背景**: ChatGPT Enterprise 是 OpenAI 为企业提供的产品，提供企业级隐私、安全和管理控制。ChatGPT Work 通过智能体能力扩展了这一点，使 AI 能够跨各种应用自主执行任务。作为领先的 AI 硬件公司，NVIDIA 正在利用它来优化内部工作流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/nvidia/chatgpt-work/">How NVIDIA scales expertise with ChatGPT Work - OpenAI</a></li>
<li><a href="https://openai.com/index/introducing-chatgpt-enterprise/">Introducing ChatGPT Enterprise | OpenAI</a></li>
<li><a href="https://help.openai.com/en/articles/8265053-what-is-chatgpt-enterprise">What is ChatGPT Enterprise? | OpenAI Help Center</a></li>

</ul>
</details>

**标签**: `#AI`, `#Enterprise`, `#ChatGPT`, `#NVIDIA`, `#Workflow`

---