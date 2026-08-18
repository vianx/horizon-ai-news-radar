---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 37 条内容中筛选出 12 条重要资讯。

---

1. [Mojo 编程语言以 Apache 2 协议开源](#item-1) ⭐️ 9.0/10
2. [Turbovec：谷歌 TurboQuant 向量搜索的 Rust 实现](#item-2) ⭐️ 8.0/10
3. [用 20 美元工具修复变砖的 Framework 笔记本，引发保修争议](#item-3) ⭐️ 8.0/10
4. [Linux 7.3 提升 VRAM 超量分配性能](#item-4) ⭐️ 8.0/10
5. [Asana 借助 Codex 在两周内完成五年工程工作量](#item-5) ⭐️ 8.0/10
6. [Qwen 3.8 27B 在智能指数上追平 GPT-5.6 Luna](#item-6) ⭐️ 8.0/10
7. [中国要求政府机构提前卸载定制版 Windows 10](#item-7) ⭐️ 8.0/10
8. [Seth Godin 批评亚马逊搜索和用户体验下降](#item-8) ⭐️ 7.0/10
9. [火车窗变平板扫描仪：创意狭缝扫描项目](#item-9) ⭐️ 7.0/10
10. [OpenAI 发起倡议，加强国家安全中人工智能的民主监督](#item-10) ⭐️ 7.0/10
11. [OpenAI 加强保障措施以调控前沿模型开发节奏](#item-11) ⭐️ 7.0/10
12. [OpenAI 与 CodeAI 合作推动青少年 AI 教育](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Mojo 编程语言以 Apache 2 协议开源](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

Modular 已将 Mojo 编程语言（包括其编译器和工具链）以 Apache 2 许可证开源。此举紧随上周 Mojo 1.0 的发布，并兑现了 2023 年 5 月做出的承诺。 这对 AI/ML 生态系统来说是一个重要里程碑，因为 Mojo 旨在将 Python 的易用性与异构硬件的高性能相结合。在宽松许可证下开源可能会加速采用和社区贡献，可能使 Mojo 成为 AI 基础设施的关键语言。 Mojo 基于 MLIR 编译器框架构建，能够针对 CPU、GPU、TPU 和其他加速器。最初成为 Python 超集的目标在 2025 年 8 月左右被放弃，Mojo 现在是一种拥有 Python 风格语法的独立语言。

rss · Simon Willison · 8月18日 21:39

**背景**: Mojo 是由 Modular Inc. 开发的系统编程语言，专为高性能 AI 基础设施而设计。它采用类似 Python 的语法，但包含受 Rust 启发的静态类型和借用检查等功能。Apache 2 许可证是一种宽松的开源许可证，允许用户自由使用、修改和分发软件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apache_License">Apache License</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>

</ul>
</details>

**标签**: `#Mojo`, `#open source`, `#programming language`, `#AI/ML`, `#compiler`

---

<a id="item-2"></a>
## [Turbovec：谷歌 TurboQuant 向量搜索的 Rust 实现](https://github.com/RyanCodrai/turbovec) ⭐️ 8.0/10

Turbovec 是一个新的 Rust 向量索引，带有 Python 绑定，实现了谷歌研究院的 TurboQuant 算法，提供了一种数据无关的量化器，具有接近最优的失真且无需单独的训练阶段。它支持在线数据摄入，并显著减少了向量搜索的内存占用。 这很重要，因为它将最先进的压缩算法带到了 Rust 生态系统中，为本地和隐私优先的应用实现了更快、更节省内存的向量搜索。它还开启了 WASM 编译的可能性，这可能使向量搜索直接在浏览器中运行。 Turbovec 声称与传统方法相比内存使用减少 87%，并且比 FAISS 更快，提供了基准测试。它用 Rust 构建，带有 Python 绑定，社区热切期待 SQLite 绑定的推出以便更容易集成。

hackernews · fittingopposite · 8月18日 18:07 · [社区讨论](https://news.ycombinator.com/item?id=49349898)

**背景**: 向量搜索是一种通过将项目表示为高维向量来查找相似项目的技术，常用于推荐系统和语义搜索等 AI 应用中。TurboQuant 是谷歌研究院提出的一种压缩算法，可减少向量量化中的内存开销，从而更高效地存储和搜索大型数据集。Turbovec 用 Rust 实现了该算法，Rust 是一种以性能和安全著称的系统编程语言，适合本地和注重隐私的部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/RyanCodrai/turbovec">GitHub - RyanCodrai/ turbovec : A vector index built on TurboQuant...</a></li>
<li><a href="https://research.google/blog/turboquant-redefining-ai-efficiency-with-extreme-compression/">TurboQuant: Redefining AI efficiency with extreme compression</a></li>
<li><a href="https://medium.com/data-science-in-your-pocket/turbovec-googles-turboquant-makes-vector-search-smaller-faster-and-simpler-fdea72674aad">turbovec : Google’s TurboQuant Makes Vector Search Smaller, Faster, and Simpler | by Mehul Gupta | Data Science in Your Pocket | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区对 Turbovec 的潜力充满热情，评论强调其内存效率（1000 万文档仅需 4GB）以及构建更快反向索引的可能性。一些用户认为它非常适合本地、隐私优先的搜索，并询问 WASM 编译情况，而另一些用户指出 Qdrant 已经集成了 TurboQuant，质疑新库的必要性。还有反馈称 README 可以更人性化一些。

**标签**: `#vector-search`, `#Rust`, `#TurboQuant`, `#AI/ML`, `#open-source`

---

<a id="item-3"></a>
## [用 20 美元工具修复变砖的 Framework 笔记本，引发保修争议](https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/) ⭐️ 8.0/10

一位用户仅用价值 20 美元的工具成功修复了一台变砖的 AMD 7040 系列 Framework 13 笔记本电脑，并在博客中详细记录了整个过程。文章指出，尽管 Framework 鼓励用户进行 BIOS 更新，但对这台过保设备未提供任何支持。 这一事件凸显了笔记本电脑行业中对固件更新可靠性和制造商责任的日益关注。它也引发了关于维修权以及公司是否应对软件导致的硬件故障负责的讨论。 修复过程涉及使用廉价工具直接刷写 BIOS 芯片，无需昂贵设备或专业服务。作者批评 Framework 未提供恢复解决方案，并指出该笔记本其他方面均完好无损。

hackernews · jp_sc · 8月18日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=49345220)

**背景**: “变砖”的笔记本电脑是指因固件更新失败等原因而完全无法使用的设备。BIOS 更新对系统稳定性和安全性至关重要，但如果中断或出错，可能导致设备无法使用。Framework 以其模块化、可维修的笔记本电脑而闻名，但此案例凸显了其在固件相关问题支持上的局限性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://community.frame.work/t/framework-laptop-16-firmware-update-bricked-my-notebook/77722">Framework laptop 16 firmware update bricked my notebook</a></li>
<li><a href="https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/">Fixing a bricked AMD 7040 series Framework 13” laptop with $20 tools</a></li>
<li><a href="https://technewst.com/the-framework-laptop-has-a-firmware-update-problem-but-maybe-not-for-long/">Framework Laptop Update Woes (But Hope Remains) | TechNewst</a></li>

</ul>
</details>

**社区讨论**: 评论者对制造商缺乏责任感表示不满，有人建议通过小额索赔法庭采取法律行动。其他人分享了在其他品牌上的类似经历，也有人因零部件供应有限和库存问题而后悔购买 Framework 产品。

**标签**: `#hardware`, `#firmware`, `#repair`, `#laptop`, `#consumer rights`

---

<a id="item-4"></a>
## [Linux 7.3 提升 VRAM 超量分配性能](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

Linux 内核 7.3 引入了处理 VRAM 超量分配的性能改进，在 GPU 内存超出时减少卡顿并改善内存管理。这项工作由 Valve 工程师 Natalie Vock 主导，并将在即将发布的内核版本中落地。 这一改进对于使用有限 VRAM 的 GPU 的游戏玩家和专业人士意义重大，因为它增强了内存压力下的系统稳定性和性能。这也凸显了 Linux 内核在内存管理方面的前瞻性，与 Windows 形成对比，并可能影响未来的 GPU 驱动开发。 内核工作侧重于改善视频内存管理行为，特别是针对 VRAM 为 8 GB 或更少的 GPU。该实现旨在减少 VRAM 超量分配时的性能下降，并且在 7.3 的初始更改之外还在追求进一步的改进。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: Linux 内核支持内存超量分配，允许进程分配超过物理可用内存的内存，具有启发式和始终超量分配等模式。VRAM 超量分配发生在 GPU 内存使用超过物理 VRAM 时，需要内核管理内存分页或交换，如果处理效率不高可能会导致卡顿。这一改进正是为了解决这一挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.phoronix.com/news/Linux-7.3-Improving-vRAM-Mgmt">Linux 7.3 To Land Initial Code Improving vRAM Management ...</a></li>
<li><a href="https://www.nitin-rachabathuni.com/blog/linux-kernel-vram-overcommit-performance">Optimizing VRAM Overcommit: How Linux Kernel Improvements ...</a></li>
<li><a href="https://www.techpowerup.com/348178/valve-engineer-improves-linux-memory-management-for-gpus-with-8-gb-vram-or-less">Valve Engineer Improves Linux Memory Management for GPUs with ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论对这一改进表示热情，用户注意到与 Windows 更新的对比，并称赞内核开发工作。一些使用 Nvidia 硬件的用户对缺乏分页支持表示沮丧，而其他人则讨论虚拟内存的碎片整理以及应用程序在告知内核内存粘性方面的作用。

**标签**: `#Linux`, `#VRAM`, `#performance`, `#kernel`, `#memory management`

---

<a id="item-5"></a>
## [Asana 借助 Codex 在两周内完成五年工程工作量](https://openai.com/index/asana) ⭐️ 8.0/10

Asana 使用 OpenAI Codex 在两周内替换了一个过时的测试系统，完成了预计需要五年才能完成的工作，成本约为 1.2 万美元。 这一案例研究展示了 AI 编程代理在现代化遗留系统方面的变革潜力，带来了显著的时间和成本节省。它凸显了 AI 工具正成为软件工程不可或缺的一部分的趋势，可能重塑团队对大规模重构任务的优先级和执行方式。 该项目涉及替换一个过时的测试系统，这一任务通常需要五年的工程工作量。然而，这项工作在短短两周内完成，成本约为 1.2 万美元，展示了 Codex 在处理复杂、耗时任务方面的高效性。

rss · OpenAI Blog · 8月18日 07:00

**背景**: OpenAI Codex 是 OpenAI 于 2025 年 4 月发布的 AI 编程代理，可通过 ChatGPT、命令行工具和 IDE 集成使用。它旨在自动化软件工程任务，如编写代码、修复错误和重构，使开发者能够将常规或大规模工作委托给 AI。Asana 作为项目管理平台，利用 Codex 对其测试基础设施进行现代化改造，展示了 AI 在遗留系统现代化中的实际应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software ... - OpenAI</a></li>

</ul>
</details>

**标签**: `#AI coding`, `#software engineering`, `#productivity`, `#OpenAI`, `#case study`

---

<a id="item-6"></a>
## [Qwen 3.8 27B 在智能指数上追平 GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 8.0/10

Qwen 3.8 27B，一个 270 亿参数的开源权重模型，在 Artificial Analysis 智能指数上获得 52 分，与 GPT-5.6 Luna（最高）持平，仅落后 GLM-5.2（753B）和 DeepSeek V4 Pro（1.7T）一分。该结果由 Simon Willison 于 2026 年 8 月 17 日报道。 这一里程碑表明，紧凑的开源权重模型可以与更大的专有模型相媲美，可能使高性能 AI 的获取更加民主化，并降低计算成本。它标志着 AI 开发向效率和可及性发展的趋势，惠及依赖开源模型的研究人员、初创企业和开发者。 Artificial Analysis 智能指数 v4.1.1 包含 GDPval-AA v2、Terminal-Bench v2.1、SciCode 和 GPQA Diamond 等基准。Qwen 3.8 27B 针对视觉、文本生成和智能体工作负载进行了指令微调，其自我报告的基准显示相对于 Qwen 3.6 27B 和闭源权重的 Qwen 3.7-Plus 均有提升。

rss · Simon Willison · 8月17日 23:58

**背景**: Artificial Analysis 智能指数是一个综合基准，通过多种任务评估 AI 模型，提供单一分数以便比较。像 Qwen 这样的开源权重模型公开发布其训练参数，允许开发者进行微调和本地部署，而专有模型通常只能通过 API 访问。这种透明度促进了 AI 研究的创新和可复现性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/">AI Model & API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://simonwillison.net/2026/Aug/16/qwen-38-27b/">Qwen 3.8 27B is excellent, but it defaults to wildly ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（条目 49334544）可能庆祝这一成就，同时争论指数的有效性以及小模型匹配大模型的实际意义。有些人可能质疑基准的全面性，或指出实际性能可能有所不同，但鉴于高分，总体情绪似乎是积极的。

**标签**: `#AI`, `#LLMs`, `#Qwen`, `#open-weights`, `#model-efficiency`

---

<a id="item-7"></a>
## [中国要求政府机构提前卸载定制版 Windows 10](https://www.bloomberg.com/news/articles/2026-08-18/china-axing-microsoft-windows-from-state-agencies-ahead-of-plan) ⭐️ 8.0/10

中国国家安全部已要求部分政府相关机构提前卸载定制版 Windows 10，原定 2027 年 2 月的停用计划被提前，理由是数据安全担忧。微软表示，未发现影响该产品的安全事件，该产品仍在定期获得安全更新。 此举标志着中国与西方科技供应商之间的数据安全紧张局势升级，可能加速中国向国产软件替代品的转变。这可能影响微软的政府相关收入，并为其他国家审查国家系统中的外国软件树立先例。 该指令适用于与中国标准软件（CMIT）合作开发的定制版 Windows 10，具体安全漏洞未披露。加速措施将停用日期提前至原定 2027 年 2 月之前，尽管微软坚称该产品安全且受支持。

telegram · zaihuapd · 8月18日 06:22

**背景**: 中国一直在推动技术领域的进口替代，旨在减少政府和关键部门对外国软件的依赖。定制版 Windows 10 专为中国政府使用而定制，其提前移除反映了对数据安全和潜在间谍活动的日益担忧。这与中国在软硬件方面实现自力更生的更广泛努力一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kommersant.ru/doc/8891857">Китай отказывается от специальной версии Windows 10 для госучреждений</a></li>
<li><a href="https://3dnews.ru/1146995/gosudarstvennim-strukturam-knr-veleno-dosrochno-otkazatsya-ot-ispolzovaniya-adaptirovannoy-versii-microsoft-windows-10">Государственным структурам КНР велено досрочно отказаться от использования адаптированной версии Microsoft Windows 10</a></li>
<li><a href="https://www.vedomosti.ru/politics/news/2026/08/18/1221904-kitai-prekraschaet">Китай прекращает поддержку Windows для госорганов - Ведомости</a></li>

</ul>
</details>

**标签**: `#China`, `#Microsoft`, `#Windows 10`, `#cybersecurity`, `#government policy`

---

<a id="item-8"></a>
## [Seth Godin 批评亚马逊搜索和用户体验下降](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 7.0/10

Seth Godin 于 2026 年 8 月发表了一篇题为《The Amazon tax》的博客文章，批评亚马逊搜索质量和用户体验的下降。这篇文章在 Hacker News 上引发了广泛讨论，获得了 834 个点赞和 506 条评论。 这一批评凸显了亚马逊平台的重大转变，搜索结果日益被广告和不相关建议充斥，影响了数百万购物者。它强调了用户不满情绪的加剧，以及替代平台可能获得更多关注。 评论者报告称，亚马逊搜索结果中高达四分之三是赞助广告，使得寻找特定产品变得困难。一些用户正在转向 Etsy 和本地商店等替代平台，还有人建议就搜索广告中的商标侵权采取法律行动。

hackernews · herbertl · 8月18日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49345263)

**背景**: 亚马逊是最大的电子商务平台，但其搜索功能已从简单的产品定位器演变为优先展示赞助内容的语义搜索引擎。这一转变反映了大型科技公司中普遍存在的趋势，即为了广告收入而牺牲用户体验。

**社区讨论**: 社区讨论大多批评亚马逊，用户分享了搜索质量下降和广告泛滥的个人经历。一些人建议使用 Geizhals.de 等价格比较网站作为替代，另一些人则讨论针对搜索广告中商标滥用的潜在法律补救措施。

**标签**: `#Amazon`, `#e-commerce`, `#search`, `#user experience`, `#platform criticism`

---

<a id="item-9"></a>
## [火车窗变平板扫描仪：创意狭缝扫描项目](https://philo.gay/linecam/) ⭐️ 7.0/10

一个名为“将铁路网络用作平板扫描仪”（linecam）的创意项目展示了利用火车车窗和线阵相机实现平板扫描仪效果。该项目在 Hacker News 上分享，引发了讨论和参与。 该项目突显了狭缝扫描成像技术在日常生活场景中的创意应用，激励他人尝试类似概念。它连接了艺术与技术，鼓励社区参与和成像领域的创新。 该项目使用安装在火车车窗上的线阵相机，在火车移动时连续捕捉线条，从而有效扫描风景。社区成员指出，类似实验中每条“线”的宽度约为 15 像素，并分享了如 slitscan.space 等工具供实践尝试。

hackernews · otherayden · 8月18日 12:43 · [社区讨论](https://news.ycombinator.com/item?id=49344825)

**背景**: 狭缝扫描摄影是一种在长时间曝光期间将狭缝置于相机与被摄体之间的技术，产生拉伸或抽象的图像。线阵相机常用于工业检测，随着被摄体移动逐行捕捉以构建完整图像。该项目创造性地将这些原理应用于火车旅程，将车窗变成扫描仪。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Slit-scan_photography">Slit-scan photography - Wikipedia</a></li>
<li><a href="https://www.lomography.com/magazine/283280-making-a-slit-scan-camera">Making a Slit Scan Camera · Lomography</a></li>
<li><a href="https://handsonfilmhistoryproject.uoregon.edu/slit-scan-photography/">Slit-Scan Photography – THE HANDS-ON FILM HISTORY PROJECT</a></li>

</ul>
</details>

**社区讨论**: 社区成员分享了类似经历，如 2008 年使用 iSight 相机在铁路轨道附近进行的实验，以及其他人通过手动拼接帧创建动画。一些人表示有兴趣将这项技术应用于锯木厂等新场景，另一些人则提供了狭缝扫描的工具和资源。总体情绪积极且鼓舞人心，赞赏其实用性与艺术性的结合。

**标签**: `#imaging`, `#creative-coding`, `#slit-scan`, `#hardware`, `#hacker-news`

---

<a id="item-10"></a>
## [OpenAI 发起倡议，加强国家安全中人工智能的民主监督](https://openai.com/index/strengthening-democratic-oversight-in-national-security) ⭐️ 7.0/10

2026 年 8 月 18 日，OpenAI 宣布了一项新倡议，旨在加强国家安全中人工智能的民主监督，承诺投入 500 万美元用于培训、技术支持和 OpenAI 积分，以支持政府监督机构。 该倡议回应了政府机构在国家安全领域理解并监督人工智能使用的日益增长的需求，可能为负责任的人工智能治理树立先例。它有望增强公众信任，确保在敏感领域部署人工智能符合民主价值观。 该倡议包括向政府监督机构提供工具、培训和专业知识，并承诺投入 500 万美元。其重点是支持民主机构履行监督职责，但具体的工具和培训项目尚未详细说明。

rss · OpenAI Blog · 8月18日 19:00

**背景**: 人工智能在国家安全领域（如情报分析和军事规划）的应用日益增多，引发了对问责制和公民自由的担忧。民主监督机制对于确保人工智能的使用符合法律和道德标准至关重要。OpenAI 的倡议旨在为政府机构提供必要的知识和资源，以有效监督这些应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/strengthening-democratic-oversight-in-national-security/">Strengthening Democratic Oversight in National Security - OpenAI</a></li>
<li><a href="https://www.unite.ai/openai-puts-5m-behind-ai-training-and-tools-for-national-security-oversight-bodies/">OpenAI Puts $5M Behind AI Training and Tools for National ...</a></li>
<li><a href="https://www.gao.gov/blog/how-artificial-intelligence-transforming-national-security">How Artificial Intelligence Is Transforming National Security | U.S. GAO</a></li>

</ul>
</details>

**标签**: `#AI governance`, `#national security`, `#OpenAI`, `#policy`, `#democratic oversight`

---

<a id="item-11"></a>
## [OpenAI 加强保障措施以调控前沿模型开发节奏](https://openai.com/index/pacing-model-development-cyber-capabilities) ⭐️ 7.0/10

OpenAI 宣布在监控、对齐和安全方面采取新的保障措施，以引导前沿模型的开发节奏，回应关于网络关键能力的担忧。该公司正在更新其安全流程，以适应前沿模型更快的发展速度。 此举表明 OpenAI 在 AI 安全方面采取主动态度，可能为其他实验室树立先例。它回应了人们对先进 AI 双重用途（尤其是在网络安全领域）日益增长的担忧，并可能影响政策和行业标准。 该公告侧重于加强监控、对齐和安全，但缺乏具体的技术细节或指标。OpenAI 正在根据模型的潜在能力调整开发速度，在以前的速度继续之前需要额外的保障措施。

rss · OpenAI Blog · 8月18日 11:00

**背景**: 前沿 AI 模型是能力极强的系统，如果被滥用可能带来风险，尤其是在网络安全领域。AI 对齐是 AI 安全的一个子领域，专注于确保这些系统按预期行为。监控和安全是这一努力的关键组成部分，有助于检测和防止有害行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/pacing-model-development-cyber-capabilities/">Pacing model development in an era of cyber-critical... | OpenAI</a></li>
<li><a href="https://techbeat.co/story/openai-tightens-frontier-ai-safeguards-to-pace-model-development">OpenAI Tightens Frontier AI Safeguards to Pace Model Development</a></li>
<li><a href="https://cyberinsider.com/openai-slows-model-development-over-concerns-about-cyber-capabilities/">OpenAI slows model development over concerns about cyber...</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#OpenAI`, `#frontier models`, `#cybersecurity`, `#AI policy`

---

<a id="item-12"></a>
## [OpenAI 与 CodeAI 合作推动青少年 AI 教育](https://openai.com/index/chatgpt-for-teens/) ⭐️ 6.0/10

2026 年 8 月 18 日，OpenAI 宣布与 CodeAI（原 Code.org）合作，推动学生和教师负责任地使用 AI，并同步推出 ChatGPT for Teens。该合作计划在未来一年通过联合咨询委员会、AI 素养课程、学生挑战赛和职业项目，覆盖数百万学生。 此次合作显著扩大了 K-12 学生的 AI 教育覆盖面，回应了学校对 AI 素养日益增长的需求。同时，它展示了 OpenAI 对年轻用户安全部署 AI 的承诺，可能为 AI 公司与教育非营利组织的合作树立先例。 ChatGPT for Teens 包含针对青少年的引导流程、更强的内置保护、健康使用功能以及额外的家长控制。合作还支持 CodeAI 开发免费的高中 AI Foundations 课程，并将成立联合咨询委员会来指导该计划。

telegram · OpenAI Blog · 8月18日 12:06

**背景**: Code.org 是一家专注于 K-12 学生计算机科学教育的非营利组织，于 2026 年 6 月更名为 CodeAI，以反映其向 AI 教育的转型。ChatGPT for Teens 是 OpenAI 聊天机器人的新模式，可自动限制某些对话以更好地保护 13-17 岁用户，此举正值对 AI 影响青少年的担忧日益加剧之际。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Code.org">Code.org - Wikipedia</a></li>
<li><a href="https://code.org/en-US/codeai">Code.org is now CodeAI</a></li>
<li><a href="https://www.geekwire.com/2026/solidifying-its-shift-to-ai-education-code-org-rebrands-as-codeai/">Code.org rebrands as CodeAI, solidifying its shift to AI education – GeekWire</a></li>
<li><a href="https://help.openai.com/en/articles/20001421-chatgpt-for-teens">ChatGPT for Teens | OpenAI Help Center</a></li>
<li><a href="https://9to5mac.com/2026/08/18/chatgpt-for-teens-openai/">ChatGPT for Teens launches with protections and features ... - 9to5Mac</a></li>
<li><a href="https://www.nytimes.com/2026/08/18/technology/chatgpt-for-teens-openai.html">OpenAI Introduces ‘ ChatGPT for Teens ’ as Safety Concerns Grow</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI education`, `#ChatGPT for Teens`, `#partnership`, `#youth`

---