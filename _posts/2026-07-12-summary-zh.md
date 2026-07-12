---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 29 条内容中筛选出 7 条重要资讯。

---

1. [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](#item-1) ⭐️ 9.0/10
2. [全球首例远程人形机器人活猪胆囊手术](#item-2) ⭐️ 9.0/10
3. [VultronRetriever 模型登顶 MTEB 排行榜](#item-3) ⭐️ 8.0/10
4. [苹果起诉 OpenAI 窃取商业机密](#item-4) ⭐️ 8.0/10
5. [特朗普政府推动英特尔复兴，苹果将采用其芯片](#item-5) ⭐️ 8.0/10
6. [U-Boot 六个漏洞可在系统启动前执行代码](#item-6) ⭐️ 8.0/10
7. [AI 代理的身份层终于开始建设](#item-7) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 将 Model Runner V2 设为所有稠密模型的默认执行路径，移除了旧的 PagedAttention 实现，并引入了新的流式解析引擎用于工具调用和推理解析。 此版本标志着 vLLM 的重大架构转变，提升了性能和模块化程度，同时简化了代码库。PagedAttention 的移除和 Model Runner V2 的成熟将使这个广泛使用的 LLM 推理引擎的所有用户受益。 该版本包含来自 232 位贡献者的 558 次提交，新增了对 LLaVA-OneVision-2 和 GLM-5 等模型的支持，并引入了针对异构词汇表的通用推测解码。Transformers 建模后端现在与原生 vLLM 速度相当。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，使用 PagedAttention 实现高效内存管理。Model Runner V2 是一个重新设计的执行核心，解决了原始 V1 架构的设计缺陷，提供了更好的模块化和性能。旧版 PagedAttention 的移除表明新的注意力后端（V1/MRv2）已经足够成熟，可以替代它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/v0.22.1/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention - Wikipedia</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#open source`, `#release`, `#AI/ML`

---

<a id="item-2"></a>
## [全球首例远程人形机器人活猪胆囊手术](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 9.0/10

外科医生远程操控宇树 G1 人形机器人，在活猪身上完成了全球首例微创胆囊切除手术，结果发表在《自然》期刊。 这表明低成本通用人形机器人能够执行复杂手术任务，有望在偏远地区、战场或太空等场景扩大机器人手术的可及性。 宇树 G1 基础款售价 13500 美元，配备灵巧手后约 67000 美元，远低于达芬奇等专用系统（超 50 万美元）。该机器人高 1.5 米，重 27 公斤。

telegram · zaihuapd · 7月11日 02:29

**背景**: 腹腔镜胆囊切除术是一种微创手术，用于切除胆囊，常用于治疗胆结石。达芬奇手术系统是广泛使用的机器人平台，但成本高达数十万至数百万美元。宇树 G1 是通用人形机器人，设计用于运动和操作，并非专为手术打造。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G1_Humanoid Robot Functions ... - Unitree G1</a></li>
<li><a href="https://en.wikipedia.org/wiki/Laparoscopic_cholecystectomy">Laparoscopic cholecystectomy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Da_Vinci_Surgical_System">Da Vinci Surgical System</a></li>

</ul>
</details>

**标签**: `#robotics`, `#surgery`, `#humanoid robot`, `#medical technology`, `#remote operation`

---

<a id="item-3"></a>
## [VultronRetriever 模型登顶 MTEB 排行榜](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

VultronRetriever 系列检索模型已在 HuggingFace 上发布，在 MTEB 排行榜上夺得第一，索引存储空间缩小 16 倍，吞吐量提升 12 倍，并可在 iPhone 上完全离线运行。 这一突破实现了移动和边缘设备上的高效本地检索，可能彻底改变离线问答和文档搜索等应用，同时降低基础设施成本。 该系列包括三个模型：Prime-8B（全球第一）、Core-4.5B（性能超越两倍大小的模型）和 Flash-0.8B（边缘设备运行凉爽，离线每分钟索引 60 张图像）。它们采用 Hydra 架构实现延迟交互检索，内存仅为同类模型的一半。

reddit · r/MachineLearning · /u/madkimchi · 7月11日 15:22

**背景**: MTEB（大规模文本嵌入基准）是评估嵌入模型在检索等任务上表现的流行排行榜。由 ColBERT 开创的延迟交互检索使用 token 级表示进行精确匹配。Hydra 架构在单一模型中统一了检索和生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://arxiv.org/html/2603.28554">Hydra: Unifying Document Retrieval and Generation in a Single Vision-Language Model</a></li>
<li><a href="https://weaviate.io/blog/late-interaction-overview">An Overview of Late Interaction Retrieval Models: ColBERT ...</a></li>

</ul>
</details>

**标签**: `#retrieval`, `#MTEB`, `#embedding`, `#on-device AI`, `#NLP`

---

<a id="item-4"></a>
## [苹果起诉 OpenAI 窃取商业机密](https://www.cnbc.com/2026/07/10/apple-openai-lawsuit-trade-secrets.html) ⭐️ 8.0/10

2026 年 7 月 10 日，苹果在美国加州北区联邦法院起诉 OpenAI、两名前员工及 io Products，指控他们系统性窃取苹果的产品设计、制造工艺及供应链机密，以加速 OpenAI 的消费级硬件研发。 这起诉讼凸显了主要科技公司在 AI 硬件竞争中的紧张局势升级，并可能为商业秘密法如何适用于员工流动和 AI 硬件开发树立先例。 苹果指控前员工 Chang Liu 离职后仍访问内部网络并下载数十份硬件文件，OpenAI 硬件负责人 Tang Yew Tan 在离职前将供应商资料发送至个人邮箱，并要求求职者携带苹果零部件参加面试。苹果还声称目前有超过 400 名前员工在 OpenAI 工作。

telegram · zaihuapd · 7月11日 03:14

**背景**: OpenAI 于 2025 年 5 月收购了 io Products，这是一家由前苹果设计师 Jony Ive 等人共同创立的硬件公司，负责领导其硬件产品开发。该诉讼的核心指控是 OpenAI 系统性地招募苹果员工并获取机密信息，以构建自己的消费硬件，直接与苹果竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Io_Products">Io Products</a></li>
<li><a href="https://aijourn.com/iyo-sues-former-engineer-after-io-founder-tang-yew-tan-admits-to-receiving-trade-secrets-from-him/">Iyo sues former engineer after io founder tang yew ...</a></li>

</ul>
</details>

**标签**: `#Apple`, `#OpenAI`, `#lawsuit`, `#trade secrets`, `#AI hardware`

---

<a id="item-5"></a>
## [特朗普政府推动英特尔复兴，苹果将采用其芯片](https://www.wsj.com/tech/the-white-house-intel-trump-apple-84fe833e) ⭐️ 8.0/10

特朗普政府已确保苹果成为英特尔芯片制造的客户，并将 90 亿美元的联邦拨款转换为英特尔 10%的股份，使政府成为最大股东。 这一干预标志着美国半导体政策的重大转变，政府通过主动持股来重振本土芯片制造商，减少对外国制造的依赖。 英特尔 CEO 陈立武每月与商务部会面，政府的芯片主管每季度听取英特尔 CFO 的简报。自 2025 年 3 月陈立武接任 CEO 以来，英特尔股价已翻了两倍。

telegram · zaihuapd · 7月11日 05:54

**背景**: 美国政府一直通过《芯片法案》等政策推动国内半导体生产。英特尔曾是占主导地位的芯片制造商，但近年来陷入困境，市场份额被台积电和 AMD 等竞争对手蚕食。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://edition.cnn.com/2025/08/19/tech/bessent-intel-government-stake">The Trump administration confirms it’s seeking a stake in Intel . Why?</a></li>
<li><a href="https://www.dailymotion.com/video/x9p5ji4">White House Confirms Talks To Take 10 % Intel Stake</a></li>
<li><a href="https://techcrunch.com/2025/09/26/the-trump-administration-is-going-after-semiconductor-imports/">The Trump administration is going after semiconductor imports</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#Intel`, `#Apple`, `#US policy`, `#chip manufacturing`

---

<a id="item-6"></a>
## [U-Boot 六个漏洞可在系统启动前执行代码](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

Binarly 披露了 U-Boot 的 FIT 签名验证中的六个漏洞，其中两个可导致任意代码执行，四个可导致设备崩溃，影响自 2013.07 版本以来的所有版本。 这些漏洞使攻击者能在操作系统启动前执行恶意代码，绕过安全软件，可能永久性地危害嵌入式设备，尤其是那些支持远程固件更新的设备。 两个代码执行漏洞（BRLY-2026-037 和 BRLY-2026-038）源于 fdt_get_name 中未检查的值，而递归漏洞（BRLY-2026-042）可耗尽栈内存。补丁已被上游接受，但需要厂商集成到固件更新中。

telegram · zaihuapd · 7月11日 08:32

**背景**: U-Boot 是嵌入式系统中广泛使用的引导程序，负责加载操作系统。FIT（扁平化镜像树）是一种用于打包多个固件组件并附带加密签名以确保真实性的格式。漏洞存在于签名验证代码中，允许精心构造的 FIT 镜像绕过验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/">New U-Boot flaws could enable stealthy firmware attacks</a></li>
<li><a href="https://thehackernews.com/2026/07/six-new-u-boot-flaws-could-let.html">Six New U-Boot Flaws Could Let Malicious Images Crash Devices or Run Code at Boot</a></li>
<li><a href="https://gbhackers.com/multiple-u-boot-vulnerabilities/">Multiple U-Boot Vulnerabilities Enable Pre-Authentication Code Execution and Device DoS Attacks</a></li>

</ul>
</details>

**标签**: `#security`, `#U-Boot`, `#firmware`, `#vulnerability`, `#bootloader`

---

<a id="item-7"></a>
## [AI 代理的身份层终于开始建设](https://news.google.com/rss/articles/CBMijwFBVV95cUxNQ2tDUjVMR1I4Z2RkYlhTZWhHaEJuT1Z4X2FGcXhxMzFBX3VtSjhwWlk2bTM3aTRUeWFaUVI3SWl3ZlVDb1hCTmtRQWIwWTRsbmtTTHRxdDNBWXY3eFhCZUY4LUQySXdpMGZza3RsNndUYnI0M1IwYzNoZFR2dTdTN0NjZTdqbS1TVFVZcXFBUQ?oc=5) ⭐️ 7.0/10

2026 年 3 月至 7 月间，AI 代理身份层的概念从抽象讨论转向具体实施，出现在协议发布、企业功能和研究论文中。像 notme.bot 这样的开源项目现在为 AI 代理提供加密身份，与人类持有的令牌分离。 这一发展至关重要，因为 AI 代理目前缺乏标准化的身份机制，导致安全风险和集成挑战。专用身份层能够为自主 AI 系统实现安全委托、访问控制和可审计性，这对于企业采用和多代理生态系统至关重要。 该身份层使用去中心化标识符（DID）和零信任原则，如云安全联盟为代理 AI 制定的新 IAM 框架所述。守护代理作为一个自主控制层，在执行层管理 AI 代理的身份和行为。

google_news · HackerNoon · 7月11日 19:25

**背景**: AI 代理是代表用户执行任务的自主程序，但传统上它们依赖人类凭证（如 API 密钥）进行身份验证，造成安全漏洞。身份层为每个代理提供唯一、可验证的加密身份，实现细粒度访问控制和审计追踪。这类似于电子邮件如何成为人类在互联网上的身份层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackernoon.com/the-identity-layer-for-ai-agents-is-finally-being-built">hackernoon.com/the- identity - layer - for - ai - agents -is-finally-being-built</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/agentic-ai-identity-and-access-management-a-new-approach">Agentic AI Identity & Access Management | CSA</a></li>
<li><a href="https://thehackernews.com/2026/06/guardian-agents-next-layer-of-identity.html">Guardian Agents: The Next Layer of Identity Governance</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#identity`, `#infrastructure`, `#security`

---