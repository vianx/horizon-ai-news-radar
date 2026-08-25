---
layout: default
title: "Horizon Summary: 2026-08-25 (ZH)"
date: 2026-08-25
lang: zh
---

> 从 43 条内容中筛选出 10 条重要资讯。

---

1. [苹果发布 M6 和 M5 Ultra 芯片，AI 与性能大幅提升](#item-1) ⭐️ 9.0/10
2. [OpenAI 的 Jalapeño 芯片在测试中超越英伟达 Blackwell](#item-2) ⭐️ 9.0/10
3. [FDA 批准首款可穿戴双葡萄糖-酮体监测仪](#item-3) ⭐️ 8.0/10
4. [Nitter 因收到 X Corp. 的停止函而关闭](#item-4) ⭐️ 8.0/10
5. [OpenAI 首席财务官解读智能充裕背后的全栈](#item-5) ⭐️ 8.0/10
6. [OpenAI 封禁俄罗斯相关账户，涉秘密影响力行动](#item-6) ⭐️ 8.0/10
7. [EVE Online 开始从 Stackless Python 2.7 迁移到 Python 3](#item-7) ⭐️ 8.0/10
8. [持续学习使开放权重前沿模型实现主权 AI](#item-8) ⭐️ 8.0/10
9. [SpaceX 计划 2027 年将英伟达 Vera Rubin NVL72 送入轨道](#item-9) ⭐️ 8.0/10
10. [OpenAI 推出 ChatGPT Work 和 Codex 的管理员插件](#item-10) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [苹果发布 M6 和 M5 Ultra 芯片，AI 与性能大幅提升](https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/) ⭐️ 9.0/10

2026 年 8 月 25 日，苹果发布了 M6 和 M5 Ultra 芯片，其中 M6 采用 2nm 工艺，M5 Ultra 采用四芯片 UltraFusion 架构，性能和 AI 计算能力大幅提升。 这一发布标志着苹果芯片的重大飞跃，可能重塑高性能计算和 AI 领域。新芯片有望为未来的 Mac 和 Pro 设备提供动力，影响依赖苹果硬件的开发者、创意人员和 AI 研究人员。 M6 采用 2nm 工艺，配备三种 CPU 核心和 12 核 CPU；M5 Ultra 则结合四个 3nm 芯片，内存带宽达 1.2TB/s，拥有 32 核神经引擎，并支持同时播放 33 路 8K ProRes 422 视频。顶配价格可超过 24,000 美元。

hackernews · interpol_p · 8月25日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49433292)

**背景**: Apple silicon 是苹果用于 Mac 和 iPad 的 ARM 架构处理器系列。M6 和 M5 Ultra 是该系列的最新成员，接替 M5 系列。M5 Ultra 采用新的 UltraFusion 技术，将四个芯片组合成一个系统，这在苹果历史上尚属首次。这些芯片旨在处理 AI 推理和高端视频编辑等繁重任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_M6">Apple M 6 - Wikipedia</a></li>
<li><a href="https://xenospectrum.com/en/apple-silicon-chip-architecture/">Apple 's M 6 Chip Debuts 2nm Process, While... | XenoSpectrum</a></li>
<li><a href="https://www.macrumors.com/2026/08/25/apple-debuts-m5-ultra/">Apple Debuts M5 Ultra as Most Powerful Chip Ever - MacRumors</a></li>

</ul>
</details>

**社区讨论**: 社区评论中既有兴奋也有担忧。一些用户对性能提升印象深刻，而另一些则讨论高昂的定价，指出经通胀调整后的价格与早期 Mac 相当。还有猜测认为苹果可能会跳过 M6 Pro/Max/Ultra，专注于面向 AI 的 M7 芯片。

**标签**: `#Apple`, `#hardware`, `#AI`, `#chips`, `#performance`

---

<a id="item-2"></a>
## [OpenAI 的 Jalapeño 芯片在测试中超越英伟达 Blackwell](https://newsletter.semianalysis.com/p/openai-jalapeno-better-than-nvidia) ⭐️ 9.0/10

OpenAI 发布了其自研推理芯片 Jalapeño 的首批基准测试结果，声称其在能效和延迟方面优于英伟达 Blackwell。在 GPT-OSS 120B、DeepSeek R1 670B 和 Kimi K2.5 1T 等模型上，该芯片每单位功耗产出的 AI 工作量是对比系统的 1.5 至 1.9 倍，端到端延迟低 1.7 至 3.6 倍，高交互场景性能高 2.1 至 4.1 倍。 这是 AI 硬件领域的一项重大进展，表明 OpenAI 等 AI 公司的自研推理芯片可能挑战英伟达的主导地位。如果这些结果在实际部署中得到验证，可能会导致更多竞争、更低成本和更快的 AI 基础设施创新。 Jalapeño 是与博通合作开发的，专为 LLM 推理优化。基准测试使用了 SemiAnalysis 的 InferenceX 基准，OpenAI 硬件负责人 Richard Ho 称结果显示“相对于现有技术有非常显著的性能提升”。该芯片以高吞吐量和低延迟为特点，但芯片尺寸和其他架构细节尚未完全披露。

hackernews · bmulholland · 8月25日 14:06 · [社区讨论](https://news.ycombinator.com/item?id=49434378)

**背景**: 英伟达的 Blackwell 架构是当前 AI 加速器的先进技术，为 B200 和 GB200 等 GPU 提供动力。OpenAI 和其他主要 AI 实验室历来依赖英伟达 GPU 进行训练和推理，但一直在探索定制芯片以降低成本和提高性能。定制推理芯片专为运行训练好的模型而设计，相比通用 GPU 可能提供效率优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/openai-broadcom-jalapeno-inference-chip/">OpenAI and Broadcom unveil LLM-optimized inference chip | OpenAI</a></li>
<li><a href="https://openai.com/index/jalapeno-first-results/">Jalapeño’s first results show industry-leading speed and efficiency in AI inference | OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/08/25/openais-jalapeno-chip-is-built-for-fast-inference-at-scale-benchmarks-show/">OpenAI’s Jalapeño chip is built for fast inference at scale, benchmarks show | TechCrunch</a></li>

</ul>
</details>

**社区讨论**: 社区评论既有兴奋也有怀疑。一些人将其与早期 3dfx 图形芯片时代相提并论，猜测哪家公司将主导推理市场。另一些人指出与人类大脑的效率差距，还有评论者强调使用 DeepSeek 和 Kimi 作为基准的趋势，表明 AI 模型格局正在转变。

**标签**: `#AI hardware`, `#OpenAI`, `#Nvidia`, `#chip design`, `#inference`

---

<a id="item-3"></a>
## [FDA 批准首款可穿戴双葡萄糖-酮体监测仪](https://www.fda.gov/news-events/press-announcements/fda-authorizes-first-wearable-device-continuously-monitors-both-ketone-levels-and-blood-sugar) ⭐️ 8.0/10

美国食品药品监督管理局（FDA）已批准 Libre Duo 10 天连续双葡萄糖酮体监测系统，这是首款可同时连续监测酮体水平和血糖的可穿戴设备，适用于 2 岁及以上糖尿病患者。 这一监管里程碑可能通过提供葡萄糖和酮体的实时数据，显著改善糖尿病管理，有助于预防糖尿病酮症酸中毒（DKA）并实现更个性化的护理。它还可能为更先进的闭环系统铺平道路，并扩大患者（尤其是 1 型糖尿病儿童）获得关键代谢监测的机会。 该设备被批准用于 2 岁及以上糖尿病患者。它将连续血糖监测（CGM）与连续酮体监测（CKM）结合在一个可穿戴传感器中，这是同类首创的组合。FDA 的授权基于 de novo 分类请求，表明这是一种具有中等风险的新型设备。

hackernews · sunnynagra · 8月25日 19:07 · [社区讨论](https://news.ycombinator.com/item?id=49439017)

**背景**: 连续血糖监测仪（CGM）是可穿戴设备，可实时跟踪血糖水平，广泛用于糖尿病患者。酮体监测传统上通过血液或尿液检测进行，但连续酮体监测（CKM）是一种新兴技术，可跟踪间质液中的β-羟基丁酸等酮体。酮体升高可能导致糖尿病酮症酸中毒（DKA），这是一种危及生命的并发症，因此连续监测有助于检测和预防这种情况。FDA 对新型设备的审批过程通常涉及 de novo 途径，该途径建立新的设备分类，可能需要数月至数年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fda.gov/news-events/press-announcements/fda-authorizes-first-wearable-device-continuously-monitors-both-ketone-levels-and-blood-sugar">FDA Authorizes First Wearable Device That Continuously Monitors Both Ketone Levels and Blood Sugar | FDA</a></li>
<li><a href="https://www.envisioning.com/research/helix/wearable-continuous-ketone-monitors">Wearable Continuous Ketone Monitors (CKM) | Helix | Envisioning</a></li>
<li><a href="https://pubs.acs.org/doi/10.1021/acssensors.3c02677">Continuous Ketone Monitoring via Wearable Microneedle Patch Platform | ACS Sensors</a></li>

</ul>
</details>

**社区讨论**: 社区评论反映了个人情感与技术怀疑的混合。一位用户分享了一位朋友因糖尿病酮症酸中毒去世的感人故事，并对进展表示感激。其他人对自动化血糖控制和报销表示希望，而一些人则质疑酮体监测对普通糖尿病患者的实用性，并提到了其他可穿戴传感器。总体而言，情绪是谨慎乐观的，重点关注可及性和实际影响。

**标签**: `#FDA`, `#wearable`, `#diabetes`, `#health tech`, `#medical devices`

---

<a id="item-4"></a>
## [Nitter 因收到 X Corp. 的停止函而关闭](https://github.com/zedeus/nitter/issues/1442) ⭐️ 8.0/10

Nitter，一个注重隐私的 Twitter 前端，收到了 X Corp. 的停止函，导致其所有实例在可预见的未来关闭。项目维护者在 GitHub 上宣布了这一消息，并表示正在等待法律建议。 这一事件凸显了依赖网络抓取的开源项目在法律上的脆弱性，并可能对公共信息获取和 AI 训练数据产生更广泛的影响。它还引发了关于企业对公共话语的控制以及对此类项目提供法律保护必要性的讨论。 根据 xcancel 网站上的消息，停止函于 8 月 24 日（周一）美国东部时间晚上 8 点收到。维护者指出，在获得法律建议之前，所有 Nitter 实例将保持关闭，目前没有更多细节。

hackernews · Banditoz · 8月25日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=49437283)

**背景**: Nitter 是一个免费开源的 Twitter 替代前端，注重隐私，无 JavaScript 或广告，所有请求都通过后端处理。它受到 Invidious 项目的启发，允许用户在不被追踪的情况下浏览推文。停止函是一种正式要求停止涉嫌非法或侵权活动的请求，常用于商标或版权纠纷。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nlnet.nl/project/Nitter/">NLnet; Nitter</a></li>
<li><a href="https://alternativeto.net/software/nitter/about/">Nitter : Free and open-source front-end mirror of Twitter... | AlternativeTo</a></li>
<li><a href="https://www.investopedia.com/terms/c/cease-and-desist.asp">investopedia.com/terms/c/ cease - and - desist .asp</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了沮丧和担忧，一些人指出 Nitter 对于访问仍依赖 X 的组织的更新至关重要。其他人建议中等强国应为这类项目提供法律保护，一位评论者推测关闭可能与 AI 公司对 Twitter 数据的需求有关，因为观察到 Claude AI 使用 Nitter 获取推文。

**标签**: `#open-source`, `#legal`, `#twitter`, `#privacy`, `#web-scraping`

---

<a id="item-5"></a>
## [OpenAI 首席财务官解读智能充裕背后的全栈](https://openai.com/index/the-full-stack-behind-abundant-intelligence) ⭐️ 8.0/10

OpenAI 首席财务官 Sarah Friar 发布博客文章，阐述了芯片、算力、模型和产品方面的进步如何协同作用，以更大规模、更低成本提供更有用的智能。文章强调了 OpenAI 对整个 AI 栈的战略关注，包括与博通合作开发的 Jalapeño 推理芯片等定制硅片。 这标志着 OpenAI 致力于垂直整合和降低成本，可能重塑 AI 基础设施的竞争格局。其重要性在于，它表明 OpenAI 正从完全依赖英伟达等外部芯片转向开发内部解决方案，可能降低 AI 部署的门槛并影响行业趋势。 该文章提到了整个栈的复合进步，但具体技术细节有限。网络搜索结果透露，OpenAI 已组建了一个约 20 人的芯片专家团队，包括曾参与 TPU 工作的前谷歌工程师，并与博通和台积电合作开发其首款自研 AI 芯片 Jalapeño，该芯片专为推理设计。

rss · OpenAI Blog · 8月25日 07:05

**背景**: AI 扩展定律描述了模型性能如何随着数据、参数或计算量的增加而提升。OpenAI 的战略涉及优化从芯片到产品的整个栈，以实现“智能充裕”——使 AI 更易获取且更经济。像 Jalapeño 这样的定制推理芯片旨在降低服务模型的成本并提高效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://btw.co/node/11271729/openai-chip/">OpenAI Chip - Break The Web</a></li>
<li><a href="https://www.ainews.com/p/openai-partners-with-broadcom-and-tsmc-for-first-in-house-ai-chip">OpenAI Partners with Broadcom and TSMC for First In-House AI Chip</a></li>
<li><a href="https://blogs.nvidia.com/blog/ai-scaling-laws/">How Scaling Laws Drive Smarter, More Powerful AI | NVIDIA Blog</a></li>

</ul>
</details>

**标签**: `#AI`, `#OpenAI`, `#compute`, `#chips`, `#strategy`

---

<a id="item-6"></a>
## [OpenAI 封禁俄罗斯相关账户，涉秘密影响力行动](https://openai.com/index/disrupting-malicious-uses-of-ai-influence-campaign-russia) ⭐️ 8.0/10

OpenAI 已封禁一批源自俄罗斯的 ChatGPT 账户，这些账户被用于进行秘密影响力行动。该行动推广一个虚假的以色列智库和一个“主权”指数，该指数赞扬俄罗斯并批评西方。 此次打击行动凸显了 AI 在虚假信息中的实际滥用，并强调了 AI 驱动影响力行动日益增长的威胁。这对 AI 安全和网络安全具有重要意义，因为它展示了像 OpenAI 这样的平台如何积极应对此类威胁。 该行动此前未被报道，使用 AI 生成社交媒体内容。OpenAI 的此次行动是其更广泛努力的一部分，旨在检测和破坏欺骗性影响力行动，如其最近报告中详述的五起此类行动。

rss · OpenAI Blog · 8月25日 00:00

**背景**: 影响力行动是协调一致的努力，旨在操纵公众舆论，通常使用虚假账户和内容。像 ChatGPT 这样的 AI 工具可能被滥用以大规模生成令人信服的文本，使此类操作更加高效。OpenAI 此前曾破坏类似的行动，包括来自伊朗的一次，并继续开发方法来识别和封禁恶意账户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/disrupting-malicious-uses-of-ai-influence-campaign-russia/">Disrupting a new covert influence campaign from Russia | OpenAI</a></li>
<li><a href="https://the-decoder.com/russia-used-chatgpt-to-run-a-covert-influence-campaign-pushing-pro-kremlin-narratives-across-the-west/">Russia used ChatGPT to run a covert influence campaign pushing...</a></li>
<li><a href="https://www.aa.com.tr/en/world/openai-shuts-down-russia-linked-chatgpt-accounts-over-covert-influence-campaign-/4037086">OpenAI shuts down Russia -linked ChatGPT accounts over ‘ covert ...</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#disinformation`, `#OpenAI`, `#cybersecurity`, `#influence operations`

---

<a id="item-7"></a>
## [EVE Online 开始从 Stackless Python 2.7 迁移到 Python 3](https://simonwillison.net/2026/Aug/25/eve-online-move-to-python-3/) ⭐️ 8.0/10

EVE Online 宣布开始从 Stackless Python 2.7 迁移到 Python 3，使用 futurize 脚本处理 240 万行代码，并手动审查约 2 万个行为差异。 此次迁移意义重大，因为它解决了生产环境中规模最大、历史最悠久的 Python 代码库之一长期存在的技术债务，为其他遗留 Python 2 系统提供了切实可行的迁移路径。同时，它也凸显了升级庞大且关键任务代码库所面临的挑战和策略。 迁移将使用 futurize 脚本自动转换代码，然后手动审查约 2 万个 Python 2 和 3 行为不同的地方，例如整数除法。公告未说明如何替换 Stackless，但他们此前曾介绍过使用 carbonengine/scheduler 库为游戏 EVE Frontier 提供的解决方案。

rss · Simon Willison · 8月25日 22:59

**背景**: EVE Online 自 2003 年起一直运行在 Stackless Python 上，上一次重大升级是在 2010 年升级到 Stackless Python 2.7。Stackless Python 是 Python 的一个变体，支持微线程（tasklets）以实现轻量级并发。futurize 脚本是 python-future 项目的一部分，用于帮助将 Python 2 代码转换为兼容 Python 3。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stackless_Python">Stackless Python</a></li>
<li><a href="https://python-future.org/futurize.html">futurize: Py2 to Py2/3 — Python-Future documentation</a></li>
<li><a href="https://github.com/stackless-dev/stackless/wiki/">Home · stackless-dev/stackless Wiki · GitHub</a></li>

</ul>
</details>

**标签**: `#Python`, `#Migration`, `#EVE Online`, `#Stackless Python`, `#Legacy Code`

---

<a id="item-8"></a>
## [持续学习使开放权重前沿模型实现主权 AI](https://www.reddit.com/r/MachineLearning/comments/1vxvzju/continual_learning_of_frontier_models_for/) ⭐️ 8.0/10

一份新的技术报告介绍了 Thomson，这是一个通过在开放权重模型上进行持续学习训练出的通用前沿模型，证明了以大幅降低的计算和人员预算即可实现前沿级性能。该模型在各项能力上展现出独特的π形改进模式，同时最大程度减少了灾难性遗忘。 这项工作挑战了前沿 AI 开发仅属于少数资金充裕实验室的假设，为更广泛的机构实现主权 AI 提供了具体路径。通过展示在开放权重模型上进行持续学习可以获得有竞争力的结果，它可能使 AI 开发民主化，并减少开发者与用户之间的权力不对称。 该报告强调了一个带有可塑性和稳定性保障的中期和后期训练栈，Thomson 在包括智能体任务、安全、法律、税务、多语言和深度研究等领域进行了评估。π形模式表明广泛改进，同时几乎消除了窄领域适应中常见的遗忘问题。

reddit · r/MachineLearning · /u/Forsaken_Scientist · 8月25日 10:30

**背景**: 持续学习是一种 AI 方法，模型在顺序学习新任务的同时保留先前学到的知识，解决了适应不断变化的数据分布的挑战。主权 AI 是指组织或国家利用自己的基础设施、数据和模型独立开发、部署和管理 AI 系统的能力。开放权重模型是公开其学习参数的 AI 模型，允许他人下载、修改和运行，这是实现这种独立开发的关键推动因素。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/continual-learning">What is Continual Learning? | IBM</a></li>
<li><a href="https://www.opentext.com/what-is/sovereign-ai">What is sovereign AI? Enterprise AI for global compliance</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>

</ul>
</details>

**标签**: `#continual learning`, `#frontier models`, `#SovereignAI`, `#open weights`, `#AI democratization`

---

<a id="item-9"></a>
## [SpaceX 计划 2027 年将英伟达 Vera Rubin NVL72 送入轨道](https://www.theregister.com/off-prem/2026/08/25/spacex-claims-it-will-put-a-vera-rubin-nvl72-rack-scale-system-into-orbit-next-year/5292067) ⭐️ 8.0/10

SpaceX 宣布计划在 2027 年将一套英伟达 Vera Rubin NVL72 机架级 AI 系统送入轨道，以测试太空 AI 数据中心技术。该系统由 72 颗 Rubin GPU 和 36 颗 Vera CPU 组成，功耗超过 100 千瓦。 这一举措可能开创轨道 AI 数据中心的先河，为国防和商业应用提供低延迟的太空计算能力。同时，它也凸显了太空探索与 AI 基础设施日益融合的趋势，SpaceX 和英伟达等主要参与者正在合作。 NVL72 系统需要复杂的液冷和供电设施，必须针对太空环境（包括辐射和热管理）进行改造。SpaceX 尚未公布具体的发射时间、轨道高度以及系统在太空中的供电和冷却方案。

telegram · zaihuapd · 8月25日 08:03

**背景**: 太空数据中心是一个提议中的概念，旨在轨道上建造 AI 数据中心，利用天基太阳能和辐射冷却。历史上，像战略防御计划的“ Brilliant Pebbles”等军事项目曾设想在轨数据处理，最近，太空发展局也在推进分散式太空架构。英伟达的 Vera Rubin NVL72 是一款机架级 AI 超级计算机，通过 NVLink 6 将 72 颗 Rubin GPU 和 36 颗 Vera CPU 统一起来，专为高性能 AI 工作负载设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/nvidia-vera-rubin-nvl72">NVIDIA Vera Rubin NVL72</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/technologies/rubin/">Infrastructure for Scalable AI Reasoning | NVIDIA Vera Rubin Platform</a></li>
<li><a href="https://en.wikipedia.org/wiki/Space-based_data_center">Space-based data center</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#NVIDIA`, `#AI infrastructure`, `#Space computing`, `#Orbital data center`

---

<a id="item-10"></a>
## [OpenAI 推出 ChatGPT Work 和 Codex 的管理员插件](https://openai.com/index/introducing-admin-plugin) ⭐️ 7.0/10

OpenAI 推出了适用于 ChatGPT Work 和 Codex 的管理员插件，使管理员能够直接在这些工具中管理工作区使用情况、成员、权限、限制和管理员请求。该插件将管理员的指令映射到支持的读取或写入操作，并返回结构化结果。 该插件通过简化管理任务并提供权限感知工具，显著增强了企业对 ChatGPT Work 和 Codex 的采用。它使组织能够更高效地管理其 AI 工具，可能降低开销并改善治理。 该插件将 Admin Console 的功能作为权限感知工具提供给 ChatGPT Work 和 Codex。它支持分析工作区使用情况、管理成员和权限、调整限制以及处理管理员请求等操作。

rss · OpenAI Blog · 8月25日 00:00

**背景**: ChatGPT Work 是 ChatGPT 的付费层级，专为专业用途设计，而 Codex 是 OpenAI 的 AI 驱动的编程助手。企业计划通常包括 Owner、Admin、Member 和 Analytics Viewer 等角色，并提供自定义角色和 RBAC 以实现更精细的控制。管理员插件旨在通过将这些管理任务集成到对话界面中来简化管理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-admin-plugin/">Introducing the Admin plugin for ChatGPT Work and Codex | OpenAI</a></li>
<li><a href="https://learn.chatgpt.com/docs/enterprise/work-admin-faq">ChatGPT Work admin FAQ | ChatGPT Learn</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#Codex`, `#Admin`, `#Enterprise`

---