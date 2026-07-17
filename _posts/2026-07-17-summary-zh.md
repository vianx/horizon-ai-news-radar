---
layout: default
title: "Horizon Summary: 2026-07-17 (ZH)"
date: 2026-07-17
lang: zh
---

> 从 45 条内容中筛选出 12 条重要资讯。

---

1. [Firefox 通过 WebAssembly 在另一个浏览器中运行](#item-1) ⭐️ 9.0/10
2. [欧盟裁定谷歌开放 Android 和搜索数据给竞争对手](#item-2) ⭐️ 9.0/10
3. [Kimi 发布 2.8 万亿参数 K3 模型，支持 100 万上下文](#item-3) ⭐️ 9.0/10
4. [一加停止在欧洲和北美推出新产品](#item-4) ⭐️ 8.0/10
5. [GPT-5.6 Codex 漏洞在完全访问模式下可能删除文件](#item-5) ⭐️ 8.0/10
6. [Thinking Machines Lab 发布 975B 开放权重模型 Inkling](#item-6) ⭐️ 8.0/10
7. [Linus Torvalds 声明 Linux 不反 AI](#item-7) ⭐️ 8.0/10
8. [QLoRA 默认学习率 2e-4 在小数据集上不佳](#item-8) ⭐️ 8.0/10
9. [ExTernD：实现任意精度的三元 LLM 量化](#item-9) ⭐️ 8.0/10
10. [日本将采购 2.75 万块英伟达 Rubin 芯片用于机器人 AI](#item-10) ⭐️ 8.0/10
11. [中国批准苹果 AI 服务在国行 iPhone 上使用](#item-11) ⭐️ 8.0/10
12. [DeepMind 与 Isomorphic Labs 公布生物韧性 AI 战略](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Firefox 通过 WebAssembly 在另一个浏览器中运行](https://simonwillison.net/2026/Jul/16/firefox-in-webassembly/#atom-everything) ⭐️ 9.0/10

Puter 已将完整的 Firefox 浏览器编译为 WebAssembly，使其能够在 Chrome 等另一个浏览器中运行。该项目使用 Claude Opus 和 Fable 进行 AI 辅助开发，估计花费了 25,000 美元的代币。 这是 WebAssembly 的一个突破性里程碑，证明了一个完整、复杂的浏览器引擎可以被移植到另一个浏览器中运行。它为沙箱浏览、遗留浏览器测试和新的 Web 应用架构打开了可能性。 该演示使用 Wisp 协议通过 Puter 的服务器代理所有网络流量，因为 WebAssembly 代码无法打开任意网络连接。该项目选择 Firefox/Gecko 是因为其强大的单进程支持，生成的 WebAssembly 二进制文件大小为 233MB。

rss · Simon Willison · 7月16日 23:34

**背景**: WebAssembly (Wasm) 是一种低级二进制指令格式，可以在现代网络浏览器中以接近原生的速度运行。将 Firefox 这样的完整浏览器编译为 Wasm 极具挑战性，因为浏览器内部结构复杂，并且需要处理网络访问，而 Wasm 对此有限制。Wisp 协议允许在单个 WebSocket 连接上复用多个 TCP/UDP 套接字，从而实现了此演示所需的代理网络访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/MercuryWorkshop/wisp-protocol">GitHub - MercuryWorkshop/wisp-protocol: Wisp is a low-overhead, easy to ...</a></li>
<li><a href="https://github.com/HeyPuter/puter">GitHub - HeyPuter/puter: 🌐 The Internet Computer! Free, Open-Source, and Self-Hostable.</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gecko_(software)">Gecko (software) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论非常热烈，Puter 团队表示他们不得不扩展服务器以应对来自讨论的流量。用户对这一技术成就表示惊叹，并讨论了其对浏览器沙箱和遗留兼容性的影响。

**标签**: `#WebAssembly`, `#Firefox`, `#Browser`, `#AI-assisted development`, `#WebSocket`

---

<a id="item-2"></a>
## [欧盟裁定谷歌开放 Android 和搜索数据给竞争对手](https://www.theverge.com/policy/966438/eu-google-android-ai-interoperability-search-data-dma) ⭐️ 9.0/10

欧盟委员会周四裁定，根据《数字市场法》，谷歌必须向符合条件的竞争对手开放部分 Android 系统功能和 Google 搜索数据，使 ChatGPT 等竞争对手的 AI 助手获得与 Gemini 同等的系统权限和数据访问。 这一决定显著重塑了 Android 生态系统和 AI 助手市场的竞争格局，可能允许用户将 ChatGPT 等第三方助手设为深度集成的系统助手，并迫使谷歌分享此前封闭的搜索数据。 谷歌仍可依据隐私和安全标准评估访问 Android 功能的申请，但相关限制须符合欧盟规定。欧盟将限制共享数据的使用方式以保护隐私和安全。

telegram · zaihuapd · 7月16日 13:19

**背景**: 《数字市场法》（DMA）是欧盟针对被视为“守门人”的大型数字平台制定的法规，旨在确保公平竞争。它要求这些平台允许互操作性、数据访问，并禁止自我优待。谷歌的 Android 和搜索被指定为 DMA 下的核心平台服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Markets_Act">Digital Markets Act</a></li>

</ul>
</details>

**标签**: `#EU regulation`, `#Android`, `#AI assistants`, `#data access`, `#Digital Markets Act`

---

<a id="item-3"></a>
## [Kimi 发布 2.8 万亿参数 K3 模型，支持 100 万上下文](https://platform.kimi.com/docs/guide/kimi-k3-quickstart) ⭐️ 9.0/10

Kimi 发布了开源模型 K3，拥有 2.8 万亿参数和 100 万 token 的上下文窗口，声称综合性能仅次于 Claude Fable 5 和 GPT-5.6 Sol。该模型采用稀疏 MoE 架构，共 896 个专家，每个 token 激活 16 个，并集成了 Kimi Delta Attention 和 Attention Residuals。 此次发布标志着开源 AI 的重要里程碑，K3 在完全开源权重的同时，性能媲美顶级闭源模型。这表明中国 AI 实验室能够达到前沿水平，可能加速 AI 智能的商品化。 K3 的扩展效率相比前代 K2 提升约 2.5 倍，完整权重将在未来几天内开放。Kimi API 定价为：缓存命中输入每百万 token 2.0 元，缓存未命中输入 20.0 元，输出 100.0 元。

telegram · zaihuapd · 7月16日 13:47

**背景**: Kimi Delta Attention 是一种线性注意力机制，通过细粒度门控改进了门控 delta 规则，提升了效率。Attention Residuals 将固定的残差连接替换为可学习的注意力机制，使信息流更优。稀疏 MoE 每个输入只激活部分专家网络，从而在较低计算成本下实现大模型容量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vizuara.substack.com/p/kimi-linear-an-expressive-efficient">Kimi-Linear : An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/pdf/2510.26692">[PDF] Kimi Linear: An Expressive, Efficient Attention Architecture - arXiv</a></li>
<li><a href="https://arxiv.org/abs/2603.15031">[2603.15031] Attention Residuals</a></li>

</ul>
</details>

**社区讨论**: 社区成员注意到通过 API 使用 K3 的成本较高，有用户报告一次渲染花费了 25 美分。有人对 Moonshot AI 的数据使用政策表示担忧，该政策称除非有企业安排，否则他们可能会在 API 内容上进行训练。一些评论者认为这是中国实验室推动 AI 智能商品化趋势的一部分。

**标签**: `#AI`, `#LLM`, `#open-source`, `#Kimi`, `#MoE`

---

<a id="item-4"></a>
## [一加停止在欧洲和北美推出新产品](https://community.oneplus.com/thread/2170715118587871237) ⭐️ 8.0/10

一加决定停止在欧洲和北美推出新产品，但现有设备将继续按原承诺获得软件更新和安全补丁。 这标志着一个曾经受欢迎的品牌从关键市场大幅撤退，可能影响其全球影响力和用户基础，但现有用户得到继续支持的保证。 该决定仅影响新产品推出，而非全面停止运营；一加仍将在 OPPO 支持下为现有设备提供支持。公司社区帖子澄清并非完全停止运营。

hackernews · pilililo2 · 7月16日 10:14 · [社区讨论](https://news.ycombinator.com/item?id=48932539)

**背景**: 一加最初以提供高规格、价格实惠、接近原生 Android 且解锁引导加载程序的智能手机而闻名，赢得了忠实的爱好者群体。近年来，该品牌面临竞争加剧和内部变化，包括联合创始人裴宇离职以及与 OPPO 更紧密的整合。

**社区讨论**: 社区评论反应不一：有人纠正标题的误导性，指出只是停止新产品发布而非全面停止运营。前员工分享了对公司文化的内部看法，其他人则感叹一加从其黑客友好根源的衰落。

**标签**: `#OnePlus`, `#smartphone`, `#business`, `#community`

---

<a id="item-5"></a>
## [GPT-5.6 Codex 漏洞在完全访问模式下可能删除文件](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 8.0/10

Thibault Sottiaux 报告称，GPT-5.6 Codex 存在一个漏洞：在启用完全访问模式且未使用沙箱保护时，由于覆盖 $HOME 环境变量时的错误，可能导致文件被删除。 该漏洞凸显了 AI 编码代理中的重大安全风险，可能导致意外删除文件，从而给未采取适当保护措施的开发者带来数据丢失的潜在后果。 该漏洞发生在模型尝试覆盖 $HOME 以定义临时目录时，却错误地删除了 $HOME。触发条件包括完全访问模式、无沙箱保护以及禁用自动审查。

rss · Simon Willison · 7月16日 17:45

**背景**: Codex 是一种 AI 编码代理，可以自主读取、编写和执行代码。完全访问模式赋予其不受限制的权限，而沙箱则将其操作隔离以防止危害。$HOME 环境变量指向用户的主目录，错误地覆盖它可能导致灾难性的删除操作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vladimirsiedykh.com/blog/codex-cli-approval-modes-2025">Codex CLI approval modes explained: auto vs read only vs... | Vladimir Siedykh</a></li>
<li><a href="https://smartscope.blog/en/generative-ai/chatgpt/codex-cli-approval-modes-no-approval/">Codex CLI Auto Approve: Dangerously Skip Permissions Equivalent (2026) - SmartScope</a></li>
<li><a href="https://amux.io/guides/ai-agent-sandboxing/">AI Agent Sandboxing in 2026: Docker, E2B, Firecracker... — amux</a></li>

</ul>
</details>

**标签**: `#codex`, `#coding-agents`, `#generative-ai`, `#ai-safety`, `#bug`

---

<a id="item-6"></a>
## [Thinking Machines Lab 发布 975B 开放权重模型 Inkling](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 8.0/10

由 Mira Murati 领导的 Thinking Machines Lab 发布了 Inkling，这是一个 975B 参数（41B 活跃）的混合专家多模态模型，采用 Apache-2.0 许可证，基于 45 万亿 token 的文本、图像、音频和视频数据训练。 Inkling 增强了美国开放权重生态系统，为中国开放模型提供了有竞争力的替代方案，并通过 Tinker 平台为微调提供了强大基础，尽管它并非前沿模型。 模型卡和训练数据文档明显简略，对数据来源的描述含糊不清。一个较小的变体 Inkling-Small（总计 276B，活跃 12B）已承诺但尚未发布。

rss · Simon Willison · 7月16日 15:35

**背景**: 混合专家（MoE）模型使用多个专门的子网络（专家）和门控机制，每个输入仅激活部分专家，从而在较低计算成本下实现大总参数量。开放权重模型发布训练好的参数，但不提供完整训练代码或数据，与开源 AI 不同。Apache-2.0 是一种宽松许可证，允许商业使用和修改。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://deasadiqbal.medium.com/understanding-open-weights-vs-open-source-models-988b50ce64d7">Understanding Open Weights vs. Open Source Models | by Asad Iqbal | Medium</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told – Open Source Initiative</a></li>

</ul>
</details>

**标签**: `#AI`, `#open-weights`, `#multimodal`, `#Mixture-of-Experts`

---

<a id="item-7"></a>
## [Linus Torvalds 声明 Linux 不反 AI](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linux 创始人 Linus Torvalds 在 Linux Media 邮件列表中声明，Linux 不是一个反 AI 的项目，称 AI 是明确有用的工具，并告诉反对者可以 fork 或离开。 来自 Linux 顶级维护者的权威背书，标志着整个 Linux 内核社区对 AI 的强烈支持，可能影响那些对集成 AI 工具犹豫不决的开源项目和开发者。 Torvalds 承认一年前 AI 的用处尚有疑问，但今天已毋庸置疑，不过他指出 AI 的经济形态等开放问题仍然存在。该言论来自内核邮件列表讨论，而非正式新闻稿。

rss · Simon Willison · 7月16日 13:26

**背景**: Linus Torvalds 是 Linux 内核的创建者和首席维护者，Linux 内核是世界上最大的开源项目之一。AI 工具，尤其是大型语言模型（LLM），已越来越多地用于软件开发中的代码生成、错误检测和文档编写。一些开源社区因许可、伦理或质量问题而抵制 AI。

**标签**: `#Linux`, `#AI`, `#open source`, `#kernel development`, `#Linus Torvalds`

---

<a id="item-8"></a>
## [QLoRA 默认学习率 2e-4 在小数据集上不佳](https://www.reddit.com/r/MachineLearning/comments/1uy1z8b/the_qlora_2e4_default_is_wrong_under_10k_samples/) ⭐️ 8.0/10

一位 Reddit 用户报告称，QLoRA 微调的默认学习率 2e-4 在样本数低于 1 万的数据集上会导致过拟合，将其降至 1e-4 可显著提升评估性能。 这挑战了 LLM 微调社区广泛采用的超参数默认值，可能为从业者节省数周的调试时间，并提高小规模微调任务的模型质量。 用户观察到，使用 2e-4 时模型在第一个 epoch 内过拟合，评估损失停滞或上升；切换到 1e-4 并将 epoch 从 3 增加到 5 获得了最佳结果。默认值 2e-4 源自 Alpaca 数据集（5.2 万样本），远大于典型的自定义数据集。

reddit · r/MachineLearning · /u/Pretty-Ad774 · 7月16日 12:50

**背景**: QLoRA（量化低秩适应）是一种参数高效微调方法，结合 4 位量化与 LoRA 以降低大语言模型的内存占用。学习率是控制训练过程中模型权重更新幅度的关键超参数，过高的学习率可能导致过拟合，尤其是在小数据集上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/QLoRA">QLoRA</a></li>
<li><a href="https://medium.com/@levxn/lora-and-qlora-effective-methods-to-fine-tune-your-llms-in-detail-6e56a2a13f3c">LoRA and QLoRA - Effective methods to Fine-tune your... | Medium</a></li>
<li><a href="https://www.techinterview.org/post/3233460056/fine-tuning-llms-vs-training-from-scratch-when-and-how/">Fine - tuning LLMs vs Training from Scratch: When and How...</a></li>

</ul>
</details>

**社区讨论**: 该 Reddit 帖子引发了大量讨论，许多用户分享了类似经历，并同意默认学习率应针对小数据集进行调整。有人指出 QLoRA 论文本身建议调参，但教程常常硬编码 2e-4 而不加说明。

**标签**: `#QLoRA`, `#fine-tuning`, `#hyperparameters`, `#LLM`, `#practical ML`

---

<a id="item-9"></a>
## [ExTernD：实现任意精度的三元 LLM 量化](https://www.reddit.com/r/MachineLearning/comments/1uy2zb3/externd_expandedrank_ternary_decomposition/) ⭐️ 8.0/10

ExTernD 提出了一种新的大语言模型训练后量化方法，将权重矩阵分解为两个三元矩阵和一个对角缩放矩阵，使得内部秩可以任意大，从而精度接近任意量化级别。 该方法克服了三元量化的固定矩阵大小限制，仅需适度增加 VRAM 即可实现高精度，可能使三元量化在资源受限硬件上部署 LLM 更加实用。 该方法使用两个三元矩阵（取值为{-1,0,1}）和一个对角缩放矩阵，内部秩可增加以降低量化误差。作者声称 VRAM 开销仅略高于当前量化方法，而三元算术的优势使其值得。

reddit · r/MachineLearning · /u/LMTLS5 · 7月16日 13:31

**背景**: 训练后量化（PTQ）通过将权重转换为更低精度来减小模型大小并加速推理，无需重新训练。三元量化将权重限制为三个值（-1, 0, 1），提供极致压缩，但常因表达能力有限而导致精度损失。ExTernD 通过矩阵分解扩展有效秩来解决这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://apxml.com/courses/practical-llm-quantization/chapter-2-post-training-quantization-ptq">Post - Training Quantization (PTQ) for LLMs</a></li>
<li><a href="https://medium.com/data-science-at-microsoft/exploring-quantization-in-large-language-models-llms-concepts-and-techniques-4e513ebf50ee">Exploring quantization in Large Language Models... | Medium</a></li>

</ul>
</details>

**标签**: `#LLM`, `#quantization`, `#ternary`, `#PTQ`, `#efficiency`

---

<a id="item-10"></a>
## [日本将采购 2.75 万块英伟达 Rubin 芯片用于机器人 AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 8.0/10

日本计划采购 27,500 块英伟达下一代 Rubin 芯片，由新成立的 Noetra 公司牵头，获得政府 24 亿美元拨款，用于开发面向机器人的主权 AI。 该计划旨在减少日本对美中 AI 技术的依赖，将日本定位为全球 AI 发展的第三种选择，并力争到 2040 年占据全球机器人市场 30%以上的份额。 Noetra 由软银、丰田支持的 Preferred Networks、NEC 等企业支持，计划于 2027 年 3 月发布首个 AI 模型，并在数年内推出机器人专用版本。

telegram · zaihuapd · 7月16日 10:59

**背景**: 英伟达 Rubin 是继 Blackwell 之后的下一代 AI 芯片架构，计算能力大幅提升。主权 AI 指国家自主开发和控制 AI 基础设施及模型的能力，以减少对外国供应商的依赖。日本机器人产业已很先进，但该项目旨在整合尖端 AI 以保持竞争力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2025/03/18/nvidia-announces-blackwell-ultra-and-vera-rubin-ai-chips-.html">cnbc.com/2025/03/18/ nvidia -announces-blackwell-ultra-and-vera...</a></li>
<li><a href="https://robotsbeat.com/japan-nvidia-noetra-physical-ai-factory-frontia-rubin-gpus/">Japan and NVIDIA Launch World's First National... | RobotsBeat</a></li>
<li><a href="https://www.techradar.com/pro/japan-reveals-new-noetra-plan-to-flood-the-country-with-10-million-robots-by-2040-including-work-in-the-nursing-food-and-drink-sectors">Japan 's robot invasion begins as 10 million machines... | TechRadar</a></li>

</ul>
</details>

**标签**: `#AI`, `#Robotics`, `#Nvidia`, `#Japan`, `#Sovereign AI`

---

<a id="item-11"></a>
## [中国批准苹果 AI 服务在国行 iPhone 上使用](https://news.google.com/rss/articles/CBMikAFBVV95cUxOSWloemk5YUJsQWZ2VkZRVklOc2g0aENfaDRabGpxUjhJSnV6WWdIOWFIaHFNTFNmcV8zanAzT3J5TUJlR1RfaThYakVxSm1RaURMV3lOLW1PWm1TRHpKLUdCVEVjYnFUN2gxclBWZTlDdGpfUk43YjFMMVducUVXTE43UEtUakpqbmZaTlpHVkE?oc=5) ⭐️ 8.0/10

中国国家互联网信息办公室已批准苹果的 Apple Intelligence AI 服务在国行 iPhone 上使用，这标志着重要的监管里程碑。 此次批准使苹果能够在中国这个其第三大市场部署生成式 AI 功能，结束了长期延迟，并凸显了全球科技公司需要与本地 AI 提供商合作以遵守中国法规。 获批的服务由阿里巴巴的 Qwen AI 和百度提供支持，而非 ChatGPT；苹果在 2025 年初提交了部分功能进行审查，此前已与本地合作伙伴共同开发近一年。

google_news · 一财全球Yicai Global · 7月16日 03:31

**背景**: 中国要求公司在向公众发布大多数生成式 AI 服务前获得政府批准。Apple Intelligence 是苹果的 AI 功能套件，包括文本生成和图像编辑，已在其他地区可用，但因监管障碍在中国延迟推出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thenews.com.pk/latest/1409220-apple-intelligence-approved-in-china-with-alibabas-qwen-baidu-ai-integration">Apple Intelligence approved in China with Alibaba’s Qwen, Baidu AI...</a></li>
<li><a href="https://vncmac.com/en/blog/apple-intelligence-china-approved-qwen-baidu-2026.html">Apple Intelligence China Approved | Qwen + Baidu | VNCMac</a></li>
<li><a href="https://www.marketscreener.com/news/apple-s-ai-tools-get-china-approval-ce7f5ed2d988f720">Apple 's AI Tools Get China Approval | MarketScreener</a></li>

</ul>
</details>

**标签**: `#Apple`, `#AI`, `#China`, `#regulation`, `#iPhone`

---

<a id="item-12"></a>
## [DeepMind 与 Isomorphic Labs 公布生物韧性 AI 战略](https://deepmind.google/blog/our-approach-to-bioresilience/) ⭐️ 7.0/10

Google DeepMind 与 Isomorphic Labs 宣布了利用 AI 模型增强生物韧性的联合策略，生物韧性指生物系统适应变化的能力。 这标志着 AI 向生物安全和医疗领域的战略扩展，有望加速应对生物威胁并推动药物发现。 该策略利用 DeepMind 的 AlphaFold 技术（预测蛋白质结构）来识别新的药物递送途径并提升生物韧性。

rss · Google DeepMind Blog · 7月16日 09:30

**背景**: 生物韧性指物种或个体适应环境变化的能力。Isomorphic Labs 是 DeepMind 的衍生公司，专注于 AI 驱动的药物发现。此次公告结合了双方的专业知识以应对生物学挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bioresilience">Bioresilience - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Isomorphic_Labs">Isomorphic Labs</a></li>

</ul>
</details>

**标签**: `#AI`, `#bioresilience`, `#DeepMind`, `#biology`, `#healthcare`

---