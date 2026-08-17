---
layout: default
title: "Horizon Summary: 2026-08-17 (ZH)"
date: 2026-08-17
lang: zh
---

> 从 39 条内容中筛选出 11 条重要资讯。

---

1. [Rust GPU 卸载项目承诺安全、可移植的 GPU 编程](#item-1) ⭐️ 8.0/10
2. [DuckDB v2.0 预览：推出服务器模式与新 SQL 解析器](#item-2) ⭐️ 8.0/10
3. [AI 生成的 GitHub Actions 代码导致 Snowflake Jira 被入侵](#item-3) ⭐️ 8.0/10
4. [AirTag 追踪稀有书籍至亚马逊 AI 训练设施](#item-4) ⭐️ 8.0/10
5. [如何让稀疏注意力和 KV 压缩看起来效果好：一份批判性指南](#item-5) ⭐️ 8.0/10
6. [Stripe 以超 70 亿美元收购 OpenRouter](#item-6) ⭐️ 8.0/10
7. [美团高管反思代价高昂的“养虾运动”AI 计划](#item-7) ⭐️ 8.0/10
8. [OpenAI 阐述 AI 驱动的网络安全防御策略](#item-8) ⭐️ 7.0/10
9. [OpenAI 资助 14 个面向智能时代的人工智能政策项目](#item-9) ⭐️ 7.0/10
10. [OpenAI 加入 PORTS-Pike 项目，助力南俄亥俄州就业](#item-10) ⭐️ 6.0/10
11. [Markdown SVG 渲染器新增通过 ffmpeg.wasm 导出 MP4 功能](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Rust GPU 卸载项目承诺安全、可移植的 GPU 编程](https://arxiv.org/abs/2608.13759) ⭐️ 8.0/10

一篇 arXiv 论文详细介绍了一个新项目，旨在直接在 Rust 中实现安全、可移植且快速的 GPU 卸载，无需绑定。该项目提议使用 LLVM 进行 GPU 代码生成，并提供多种接口，包括自动数据移动。 这一进展可能显著简化 Rust 开发者的 GPU 编程，减少维护绑定的负担并提高安全性。它解决了 Rust 生态系统中的一个主要痛点，可能加速 Rust 在 HPC 和 GPU 加速应用中的采用。 该项目提供三种接口：自动管理、显式控制和 unsafe 低级控制。它利用 LLVM 的卸载运行时进行代码生成，并旨在实现厂商中立，支持多种 GPU 后端。

hackernews · linggen · 8月17日 17:54 · [社区讨论](https://news.ycombinator.com/item?id=49334991)

**背景**: 传统上，Rust 中的 GPU 编程需要绑定到 CUDA 或 OpenCL 等 C/C++ 库，这可能不安全且难以维护。该项目旨在提供原生 Rust 解决方案，利用编译器自动处理 GPU 卸载，类似于 C/C++ 中的 OpenMP 或 OpenACC。该方法仍在积极开发中，尚未合并到 Rust 编译器中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.13759">[2608.13759] GPU Offload in Rust : Portable, Safe, and Fast</a></li>
<li><a href="https://www.emergentmind.com/papers/2608.13759">GPU Offload in Rust</a></li>
<li><a href="https://rust-lang.github.io/rust-project-goals/2025h1/GPU-Offload.html">Expose experimental LLVM features for GPU offloading - Rust Project...</a></li>

</ul>
</details>

**社区讨论**: 社区评论显示对该项目的热情，一位用户表示摆脱了维护绑定的头痛。另一位用户质疑选择 LLVM 而非 MIR，认为现有的 Vulkan 绑定等解决方案可能更简单。一些用户询问代码可用性和目标受众。

**标签**: `#Rust`, `#GPU`, `#LLVM`, `#Programming Languages`, `#Systems`

---

<a id="item-2"></a>
## [DuckDB v2.0 预览：推出服务器模式与新 SQL 解析器](https://duckdb.org/2026/08/17/duckdb-20-highlights) ⭐️ 8.0/10

DuckDB 发布了即将于 2026 年秋季推出的 v2.0 预览版，重点介绍了多项主要功能，包括将 DuckDB 作为服务器、触发器、VARIANT 类型、异步 I/O、新的 SQL 解析器以及新的存储格式。该预览于 2026 年 8 月 17 日发布，引起了社区的高度关注。 DuckDB v2.0 是这款广泛使用的分析型数据库的一个重要里程碑，可能将其应用场景从嵌入式分析扩展到服务器部署。新功能可能对数据工程工作流产生重大影响，使 DuckDB 在与 ClickHouse 等其他 OLAP 系统的竞争中更具优势。 预览中提到了新的存储格式和新的 SQL 解析器，这些基础性变更可能会影响与现有 DuckDB 文件和查询的兼容性。此外，异步 I/O 和 VARIANT 类型的引入是值得注意的技术增强，而服务器模式可能支持新的部署架构。

hackernews · ibotty · 8月17日 13:46 · [社区讨论](https://news.ycombinator.com/item?id=49330781)

**背景**: DuckDB 是一个开源的进程内 SQL OLAP 数据库管理系统，专为分析工作负载设计，通常作为嵌入式数据库使用，类似于 SQLite，但针对大型数据集的复杂查询进行了优化。它采用列式存储，并支持超出内存的处理，因此在数据工程和分析领域广受欢迎。v2.0 预览版建立在最近的 1.5.x 版本之上，这些版本侧重于稳定性和 CLI 改进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://duckdb.org/2026/08/17/duckdb-20-highlights">A Preview of DuckDB v2.0 – DuckDB</a></li>
<li><a href="https://duckdb.org/">DuckDB – An in-process SQL OLAP database management system</a></li>
<li><a href="https://en.wikipedia.org/wiki/DuckDB">DuckDB - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，用户对 Quack（服务器模式）等功能表示兴奋，并称赞 DuckDB 在消费级硬件上处理大数据的能力。然而，一些用户对开发速度过快（不到 6 个月 10,000 次提交）以及 AI 的作用表示担忧，另一些用户则指出缺少增量物化视图，他们认为这是与 ClickHouse 竞争的关键功能。

**标签**: `#DuckDB`, `#database`, `#analytics`, `#data engineering`, `#release`

---

<a id="item-3"></a>
## [AI 生成的 GitHub Actions 代码导致 Snowflake Jira 被入侵](https://www.wiz.io/blog/red-agent-snowflake-copilot-cicd-bug) ⭐️ 8.0/10

Snowflake 的 Jira 工作流中一个由 AI 生成的 GitHub Actions 代码引入的漏洞，导致其 Jira 实例被入侵。Wiz 博客文章强调了这一事件，并指出在 CI/CD 管道中进行静态分析的必要性。 这一事件凸显了 AI 生成代码在 CI/CD 管道中日益增长的安全风险，因为此类代码可能引入微妙的漏洞，绕过传统审查。它强调了在部署前使用自动化静态分析工具捕获此类问题的紧迫性。 该漏洞是在 GitHub Actions 工作流（jira_issue.yml）中引入的，涉及模板注入，允许通过模板扩展进行代码注入。Wiz 博客文章和社区讨论提到了工具“zizmor”作为 GitHub Actions 的静态分析解决方案。

hackernews · galnagli · 8月17日 14:18 · [社区讨论](https://news.ycombinator.com/item?id=49331423)

**背景**: GitHub Actions 是一个 CI/CD 平台，用于自动化软件工作流，但其基于 YAML 的配置容易出错，且易受注入攻击。像 zizmor 这样的静态分析工具会扫描工作流文件以发现安全问题，帮助开发者在漏洞被利用之前捕获它们。这一事件凸显了保护 AI 生成代码的更大挑战，因为此类代码可能缺乏人工监督。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wiz.io/blog/github-actions-security-guide">Hardening GitHub Actions: Lessons from Recent Attacks | Wiz Blog</a></li>
<li><a href="https://github.blog/engineering/platform-security/fixing-security-vulnerabilities-with-ai/">Fixing security vulnerabilities with AI - The GitHub Blog</a></li>
<li><a href="https://www.perforce.com/resources/events/webinars/best-practices-checklist-static-analysis-cicd">Best Practices Checklist for Static Analysis in CI / CD | Perforce Software</a></li>

</ul>
</details>

**社区讨论**: 社区评论表示，这个错误可以理解，但强调不使用静态分析来检查 GitHub Actions 是疏忽。有人指出该漏洞与 Copilot 的建议无直接关系，而另一些人则指出 AI 降低了引入变更的成本，使瓶颈转向代码验证。

**标签**: `#AI security`, `#CI/CD`, `#GitHub Actions`, `#vulnerability`, `#supply chain`

---

<a id="item-4"></a>
## [AirTag 追踪稀有书籍至亚马逊 AI 训练设施](https://simonwillison.net/2026/Aug/17/we-tracked-a-shipment-of-rare-books-it-ended-at-an-amazon-ai-tra/) ⭐️ 8.0/10

404 Media 在一本书中藏入苹果 AirTag，追踪了一笔来自 Biblio 卖家的大宗稀有书籍订单，发现其被送往拉斯维加斯亚马逊 LAS8 设施的 VGT3 区域，该区域用于 AI 训练的破坏性书籍扫描。 这项调查提供了具体证据，将大宗书籍购买与 AI 训练操作联系起来，证实了书商界长期以来的怀疑。它凸显了 AI 训练数据来源的不透明性，并引发版权担忧，影响作者、出版商和 AI 公司。 AirTag 被放置在 7 月通过 Biblio 订购的约 1000 本书中的一本中。VGT3 设施以破坏性扫描大量书籍而闻名，这一点得到了亚马逊员工在线论坛讨论的证实。

rss · Simon Willison · 8月17日 15:21

**背景**: AI 公司通常使用大量文本（包括书籍）训练大型语言模型，这些文本可能通过批量购买获得。AirTag 是一种小型蓝牙追踪器，利用苹果的“查找”网络报告位置，实现隐蔽追踪。Biblio 是一个二手书和稀有书籍的在线市场，此类大宗订单已引起怀疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Biblio.com">Biblio.com - Wikipedia</a></li>
<li><a href="https://www.biblio.com/">Used Books and Rare Books from Antiquarian Booksellers - Biblio</a></li>
<li><a href="https://wairco.com/blogs/news/apple-airtag-tracking-technology">Apple AirTag Tracking Technology – wairco</a></li>

</ul>
</details>

**标签**: `#AI training data`, `#investigative journalism`, `#copyright`, `#Amazon`, `#books`

---

<a id="item-5"></a>
## [如何让稀疏注意力和 KV 压缩看起来效果好：一份批判性指南](https://www.reddit.com/r/MachineLearning/comments/1vqqqcs/how_to_make_any_sparse_attention_kv_compression/) ⭐️ 8.0/10

一位在高效注意力和 KV 缓存压缩领域有多年经验的研究者坦诚分享了可能夸大报告性能的可疑做法，例如挑选基准、避免隔离贡献以及使用聚合指标来掩盖弱点。该帖子呼吁社区采用更严格的评估标准。 这一点很重要，因为夸大的结果可能会误导研究人员和从业者采用次优方法，从而减缓高效 Transformer 推理的进展。它揭示了稀疏注意力和 KV 压缩方法评估中的系统性问题，可能促使转向更诚实和稳健的基准测试。 作者列出了具体策略：使用带有单个分布外键值对的“大海捞针”任务，通过比较次优超参数的基线来避免隔离贡献，在 RULER 等基准上仅报告聚合分数，以及利用模型已经表现不佳的饱和任务。他们还提到为自己的方法使用 LLM 生成的 Triton 内核，同时保持基线为 2023 年的原始实现。

reddit · r/MachineLearning · /u/korec1234 · 8月17日 12:18

**背景**: 稀疏注意力和 KV 缓存压缩是减少 Transformer 推理内存和计算成本的技术，尤其适用于长上下文。RULER 和“大海捞针”测试等基准常用于评估这些方法，但其设计可能被利用。该帖子基于作者的经验，并引用了 p_nawrot 的 Twitter 帖子，强调需要仔细评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2504.17768">The Sparse Frontier: Sparse Attention Trade-offs in Transformer LLMs</a></li>
<li><a href="https://arxiv.org/pdf/2502.11089">Hardware-Aligned and Natively Trainable Sparse Attention</a></li>
<li><a href="https://arxiv.org/html/2502.18137v4">SpargeAttention: Accurate and Training-free Sparse Attention Accelerating Any Model Inference</a></li>

</ul>
</details>

**标签**: `#sparse attention`, `#KV cache compression`, `#evaluation`, `#transformers`, `#efficient attention`

---

<a id="item-6"></a>
## [Stripe 以超 70 亿美元收购 OpenRouter](https://www.bloomberg.com/news/articles/2026-08-16/stripe-nears-deal-to-buy-ai-firm-openrouter-for-over-7-billion) ⭐️ 8.0/10

据报道，Stripe 已达成协议，以超过 70 亿美元收购 AI 模型聚合商 OpenRouter，但最终价格仍可能变动。该消息由彭博社于 2026 年 8 月 16 日报道。 此次收购标志着 AI 基础设施领域的整合，将广泛使用的 AI 模型网关纳入一家大型支付公司旗下。它可能重塑开发者访问和支付 AI 模型的方式，对更广泛的 AI 生态系统产生影响。 OpenRouter 成立于 2023 年，提供超过 400 个 AI 模型的访问服务，并据报道截至 2026 年 5 月已服务 800 万名开发者。关于具体价格，报道不一，有消息称 70 亿美元，也有称 80 亿美元，领英上甚至提到 100 亿美元。

telegram · zaihuapd · 8月17日 01:19

**背景**: OpenRouter 是一个 AI 模型聚合器，允许开发者通过单一的 OpenAI 兼容 API 访问来自不同提供商（如 Anthropic、OpenAI、Google）的模型。Stripe 是一家主要的在线支付处理平台，此次收购将把 AI 模型访问与支付基础设施相结合，可能简化开发者的计费和访问流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/sanjeev-fintech_fintech-stripe-infrastructure-activity-7487504922406711296-F_8B">Stripe Acquires OpenRouter for $10B to Expand AI... | LinkedIn</a></li>
<li><a href="https://nationalcioreview.com/articles-insights/extra-bytes/stripe-acquires-openrouter-for-more-than-7-billion/">Stripe Acquires OpenRouter for More... - The National CIO Review</a></li>
<li><a href="https://www.kucoin.com/news/flash/stripe-acquires-openrouter-in-7b-8b-deal-sources-disagree-on-price">Stripe Acquires OpenRouter in $7B–$8B Deal, Sources... | KuCoin</a></li>

</ul>
</details>

**标签**: `#acquisition`, `#AI`, `#Stripe`, `#OpenRouter`, `#business`

---

<a id="item-7"></a>
## [美团高管反思代价高昂的“养虾运动”AI 计划](https://weibo.com/1642634100/RdM6hhhpW) ⭐️ 8.0/10

美团核心本地商业 CEO 王莆中公开反思公司内部 AI 变革，透露 2 月至 3 月的“养虾运动”导致每日消耗上千万元 Token，并产生干扰真实经营的谬误。他指出，4 月起各事业部成立 AI 组织，到 7 月 AI 初步在内部产品流程中跑通并产生价值。 这家大型科技公司的坦诚反思凸显了企业采用 AI 的实际挑战，包括成本超支和与业务目标不一致。它强调了可衡量的生产力增长和战略对齐的必要性，这对 AI/ML 社区和其他进行 AI 转型的企业具有重要价值。 王莆中指出了认知、效率、场景、考核四重错配，这些错配阻碍了 AI 落地。他还提到，6 月和 7 月通过赛马机制明确了 AI 转型是业务、组织、技术三位一体的系统工程。美团 AI Agent 平台 CatPaw 于 7 月上线，已覆盖 9 万员工，搭建了 3 万个 Agent。

telegram · zaihuapd · 8月17日 02:09

**背景**: “养虾运动”指的是公司范围内鼓励所有员工使用 AI 的举措，比喻在业务的每个角落“养虾”。这导致了过度的 Token 消耗和输出错误，说明了将 AI 使用作为 KPI 而不考虑明确业务价值的陷阱。Tokenmaxxing 的概念，即 Token 消耗成为生产力的代理指标，已被专家如 Ethan Mollick 批评为有缺陷的指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linux.do/t/topic/2764304">王莆中聊 美 团 AI... - LINUX DO</a></li>
<li><a href="https://www.xiaoluo3.com/news/?30718.html">美 团 高管反思全员“ 养 虾 运 动 ”：日耗千万 Token...</a></li>
<li><a href="https://watermelonwater.tech/insights/日烧数亿token影响分析/">Tokenmaxxing泡沫：当 AI Token 消 耗 成 为KPI，古德哈特定律再次应验</a></li>

</ul>
</details>

**标签**: `#AI adoption`, `#enterprise AI`, `#cost management`, `#business strategy`, `#Meituan`

---

<a id="item-8"></a>
## [OpenAI 阐述 AI 驱动的网络安全防御策略](https://openai.com/index/the-defenders-window) ⭐️ 7.0/10

OpenAI 发布了一篇题为《防御者的窗口》的文章，讨论 AI 如何重塑网络安全，并为安全团队概述了防御策略。文章强调了 AI 在赋能攻击者和防御者方面的双重角色。 这一指导意义重大，因为它提供了来自领先 AI 组织关于安全团队如何适应不断变化的威胁环境的权威见解。它帮助组织了解利用 AI 进行防御的实用步骤，可能影响行业最佳实践。 文章可能涵盖具体的防御措施，如 AI 驱动的威胁检测、自动化响应，以及安全专业人员具备 AI 素养的重要性。它还可能讨论对抗性 AI 等挑战以及持续适应的必要性。

rss · OpenAI Blog · 8月17日 05:30

**背景**: AI 在网络安全中的应用日益广泛，攻击者利用它来自动化和增强攻击，防御者则用它来改进检测和响应。作为主要的 AI 开发者，OpenAI 对这些动态有独特的视角，并分享其自身的防御策略以帮助更广泛的社区。

**标签**: `#AI`, `#cybersecurity`, `#OpenAI`, `#defense`

---

<a id="item-9"></a>
## [OpenAI 资助 14 个面向智能时代的人工智能政策项目](https://openai.com/index/new-policy-ideas-for-the-intelligence-age) ⭐️ 7.0/10

OpenAI 宣布资助 14 个独立项目，探索旨在扩大经济机会和增强智能时代社会韧性的新人工智能政策构想。这一举措表明 OpenAI 在技术开发之外，战略性地参与塑造人工智能治理。 此举意义重大，因为它使 OpenAI 成为人工智能政策讨论的积极参与者，可能影响政府和机构如何应对人工智能监管和经济适应。它可能有助于制定政策，确保人工智能的益处得到广泛分享，并使社会更好地为人工智能驱动的变革做好准备。 这 14 个项目是独立的，意味着它们不受 OpenAI 直接控制，这可能增加研究的可信度和多样性。重点领域是经济机会和社会韧性，表明对人工智能颠覆面前的增长和稳定性的关注。

rss · OpenAI Blog · 8月17日 03:15

**背景**: “智能时代”指的是一个由数据和人工智能力量定义的未来时代，人工智能是经济和社会转型的核心。人工智能政策研究至关重要，因为它有助于建立管理人工智能对就业、不平等和社会结构影响的框架，确保技术进步惠及整个社会。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.imtnews.ph/preparing-for-the-intelligence-age/">Preparing for the intelligence age - Iloilo Metropolitan Times</a></li>
<li><a href="https://hai.stanford.edu/news/fostering-effective-policy-for-a-brave-new-ai-world-a-conversation-with-rishi-bommasani">Fostering Effective Policy for a Brave New AI World... | Stanford HAI</a></li>
<li><a href="https://www.publicfirst.co.uk/unlocking-the-200-billion-ai-opportunity">Unlocking the £200 Billion AI Opportunity - Public First</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#OpenAI`, `#economic opportunity`, `#societal resilience`, `#governance`

---

<a id="item-10"></a>
## [OpenAI 加入 PORTS-Pike 项目，助力南俄亥俄州就业](https://openai.com/index/openai-joins-ports-pike-project) ⭐️ 6.0/10

OpenAI 宣布参与位于俄亥俄州派克县的 PORTS-Pike 项目，这是一个规划中的人工智能基础设施和发电综合体。此举扩大了 OpenAI 的社区投资，预计将支持南俄亥俄州数千个就业岗位。 此次合作表明 OpenAI 在核心 AI 研究之外，致力于区域经济发展和社区投资。这可能为其他科技公司投资当地基础设施和创造就业机会树立先例，尤其是在欠发达地区。 PORTS-Pike 园区将为俄亥俄州创造数万个就业岗位，并以初始 8000 万美元的社区福利基金为基础。NVIDIA 也已向 SB Energy 投资 15 亿美元以支持该项目，该园区将独家托管 NVIDIA 的 AI 计算。

rss · OpenAI Blog · 8月17日 05:00

**背景**: PORTS-Pike 技术园区是一个规划中的人工智能基础设施和发电综合体，位于俄亥俄州皮克顿附近的美国能源部朴茨茅斯基地。该园区旨在为 AI 工作负载提供专用电力和计算资源，吸引 OpenAI 和 NVIDIA 等大型科技公司在该地区投资。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/ports_technology_campus">PORTS Technology Campus | AI Wiki</a></li>
<li><a href="https://investingnews.com/nvidia-guarantees-sb-energy-s-ports-pike-technology-campus-in-ohio-to-exclusively-host-nvidia-ai-compute/">NVIDIA Guarantees SB Energy's PORTS - Pike Technology Campus in...</a></li>
<li><a href="https://openai.com/index/openai-joins-ports-pike-project/">OpenAI joins PORTS - Pike project | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#community investment`, `#regional development`, `#Ohio`

---

<a id="item-11"></a>
## [Markdown SVG 渲染器新增通过 ffmpeg.wasm 导出 MP4 功能](https://simonwillison.net/2026/Aug/16/markdown-svg-upgrades/) ⭐️ 5.0/10

Simon Willison 升级了他的 markdown-svg-renderer 工具，新增了多项功能，其中最引人注目的是一个 MP4 标签页，它利用 ffmpeg.wasm 在浏览器中完全将动画 SVG 转换为 MP4 视频。该更新于今天提交，允许用户将 SVG 动画导出为 MP4 文件，以便在不支持 SVG 动画的平台上使用。 这一增强功能大大简化了在不支持 SVG 动画的平台上（如社交媒体或即时通讯应用）分享动画 SVG 内容的流程。同时，它也展示了 WebAssembly 在浏览器中直接执行视频编码等复杂任务的能力日益增强，这可能激励开发者生态中出现类似工具。 MP4 标签页会分析 SVG 中的动画，估算循环时长，渲染多帧图像，然后加载超过 30MB 的 ffmpeg.wasm 将这些帧编译成 MP4 视频。该工具还支持在浏览器中将 SVG 渲染为 PNG 和 JPEG 格式，并且可以从支持 CORS 的 URL 或 GitHub Gist 加载 Markdown，并提供可书签的 URL。

rss · Simon Willison · 8月16日 23:59

**背景**: Markdown 是一种轻量级标记语言，用于格式化纯文本；SVG 是一种矢量图像格式，可以包含动画。markdown-svg-renderer 是一个基于网页的工具，用于渲染 Markdown，并对围栏式 SVG 代码块进行特殊处理，将其转换为交互式标签页以供查看和导出。CORS（跨源资源共享）是一种允许网页从其他域请求资源的机制，因此该工具可以从外部 URL 获取内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tools.simonwillison.net/markdown-svg-renderer">tools .simonwillison.net/ markdown - svg - renderer</a></li>
<li><a href="https://devblogs.co/posts/markdown-svg-renderer">markdown - svg - renderer</a></li>
<li><a href="https://thebrieftide.com/brief/markdown-svg-renderer">markdown - svg - renderer : Simon Willison's SVG-aware Markdown tool</a></li>

</ul>
</details>

**标签**: `#Markdown`, `#SVG`, `#Developer Tools`, `#Simon Willison`

---