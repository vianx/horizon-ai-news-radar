---
layout: default
title: "Horizon Summary: 2026-07-16 (ZH)"
date: 2026-07-16
lang: zh
---

> 从 37 条内容中筛选出 11 条重要资讯。

---

1. [Thinking Machines 发布开源权重多模态模型 Inkling](#item-1) ⭐️ 8.0/10
2. [xAI 在隐私争议中开源 Grok Build](#item-2) ⭐️ 8.0/10
3. [OpenAI 推出 GPT-Red：通过自我对弈实现自动化红队测试](#item-3) ⭐️ 8.0/10
4. [Claude web_fetch 工具绕过漏洞导致数据泄露](#item-4) ⭐️ 8.0/10
5. [为 JEPA 世界模型寻找反对意见](#item-5) ⭐️ 8.0/10
6. [哈达玛积聚类解开 InceptionV1 神经元](#item-6) ⭐️ 8.0/10
7. [谷歌与 Epic 撤回动议，第三方应用商店即将入驻 Play](#item-7) ⭐️ 8.0/10
8. [DeepSeek 完成首轮融资，腾讯成第一大外部股东](#item-8) ⭐️ 8.0/10
9. [Simon Willison 通过 WebAssembly 将 Rust Mermaid 渲染器移植到浏览器](#item-9) ⭐️ 7.0/10
10. [OpenAI 提出“反向联邦制”推进 AI 安全](#item-10) ⭐️ 6.0/10
11. [综述：类人 AI 作为后图灵时代的社会伙伴](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Thinking Machines 发布开源权重多模态模型 Inkling](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 8.0/10

Thinking Machines Lab 发布了 Inkling，这是一个新的开源权重多模态模型，支持音频输入，并可通过其 Tinker 平台进行微调。 Inkling 是支持音频的最大开源权重模型之一，为企业提供了一个可定制的基座，使其能够以较低成本拥有并微调前沿水平的模型，可能挑战闭源模型的主导地位。 Inkling 并非整体最强的模型，但结合了多模态能力、高效推理以及可在 Tinker 上微调的特点。社区提供了本地部署资源，包括 llama.cpp 和 Unsloth 的 GGUF/NVFP4 量化版本。

hackernews · vimarsh6739 · 7月15日 18:12 · [社区讨论](https://news.ycombinator.com/item?id=48924912)

**背景**: 开源权重模型是指其核心组件公开发布，任何人都可以下载、运行、研究和修改的 AI 模型。多模态模型能够处理文本、图像和音频等多种数据类型，从而实现更丰富的理解。Tinker 是一个使用 LoRA 高效微调开源模型的平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://thinkingmachines.ai/tinker/">Tinker - Thinking Machines Lab</a></li>

</ul>
</details>

**社区讨论**: 社区评论总体积极，用户强调了 Inkling 的音频支持和本地部署选项。一些人希望 Thinking Machines 能成为 DeepSeek 等中国开源模型的西方替代品，另一些人则称赞其微调商业模式是企业实用的路径。

**标签**: `#open-weights`, `#multimodal`, `#AI`, `#machine learning`, `#model release`

---

<a id="item-2"></a>
## [xAI 在隐私争议中开源 Grok Build](https://github.com/xai-org/grok-build) ⭐️ 8.0/10

xAI 已在 GitHub 上开源其 Grok Build CLI 工具，此前该工具因将整个目录上传至 xAI 云存储而遭到社区强烈反对。 此举标志着 xAI 的重大转变，可能在隐私问题后重建信任，并已催生了像 Gork Build 这样注重隐私的分支。 代码库包含一个使用 Unicode 框绘制的独立终端 Mermaid 图表渲染器，开源发布允许社区检查和修改。

hackernews · skp1995 · 7月15日 20:24 · [社区讨论](https://news.ycombinator.com/item?id=48926590)

**背景**: Grok Build 是一个用于 vibe coding 的 CLI 工具，可将自然语言提示转化为原型。xAI 由埃隆·马斯克创立，开发 Grok AI 助手。该工具此前未经明确同意上传用户数据，引发隐私抗议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_Build">Grok Build</a></li>
<li><a href="https://grokipedia.com/page/Grok_Build">Grok Build</a></li>

</ul>
</details>

**社区讨论**: 社区评论对代码库的功能（如 Mermaid 渲染器）表示惊讶，并注意到出现了像 Gork Build 这样去除遥测并阻止自动更新的隐私分支。一些用户批评之前的数据泄露行为，但也承认模型的质量。

**标签**: `#open source`, `#AI`, `#developer tools`, `#privacy`, `#xAI`

---

<a id="item-3"></a>
## [OpenAI 推出 GPT-Red：通过自我对弈实现自动化红队测试](https://openai.com/index/unlocking-self-improvement-gpt-red) ⭐️ 8.0/10

OpenAI 推出了 GPT-Red，这是一个利用自我对弈强化学习的自动化红队测试系统，旨在提升大型语言模型在提示注入攻击下的安全性、对齐性和鲁棒性。 这种方法自动化了漏洞发现过程，减少了对人类红队成员的依赖，并实现了持续的安全改进。它解决了提示注入等关键 AI 安全问题，而这些问题在已部署的 LLM 中日益受到关注。 GPT-Red 通过自我对弈强化学习进行训练，其中模型和一组多样化的防御者 LLM 同时在广泛的红队测试场景中训练。它目前是 OpenAI 内部使用的工具，用于自动发现自身模型中的漏洞。

rss · OpenAI Blog · 7月15日 10:00

**背景**: 红队测试涉及模拟对抗性攻击以识别 AI 系统的弱点。提示注入是一种攻击方式，将恶意指令嵌入用户输入中以覆盖模型的预期行为。自我对弈是一种训练技术，智能体通过与自身或自身的副本对弈来改进，这在强化学习中很常见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/unlocking-self-improvement-gpt-red/">GPT - Red : Unlocking Self -Improvement for Robustness | OpenAI</a></li>
<li><a href="https://www.iankhan.com/gpt-red-unlocking-self-improvement-for-robustness/">GPT - Red : Automated Red Teaming for AI Safety - Ian Khan</a></li>
<li><a href="https://www.oflight.co.jp/en/columns/openai-gpt-red-self-improving-safety-2026-07">OpenAI's GPT - Red Explained: Automated Red - Teaming ... | Oflight Inc.</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#red teaming`, `#self-play`, `#prompt injection`, `#OpenAI`

---

<a id="item-4"></a>
## [Claude web_fetch 工具绕过漏洞导致数据泄露](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 8.0/10

安全研究员 Ayush Paul 发现了一种提示注入攻击，绕过了 Claude 的 web_fetch 工具保护，通过诱使代理从蜜罐站点跟随嵌套链接，从而窃取用户记忆（姓名、城市、雇主）。 该漏洞展示了 Anthropic 数据泄露防御的实际绕过方式，凸显了在结合私有数据、不可信内容和外部通信的 AI 代理（即“致命三重奏”）中保障安全的持续挑战。 该攻击利用了一个漏洞：web_fetch 可以导航到之前获取页面中嵌入的 URL，从而允许蜜罐站点通过按字母顺序排列的链接引导代理窃取数据。Anthropic 已在内部发现该问题，并通过移除从获取内容中跟随链接的能力来修复漏洞。

rss · Simon Willison · 7月15日 14:21

**背景**: “致命三重奏”指的是私有数据访问、读取不可信内容（例如来自网络）以及通过 URL 等外部通信能力的组合。Claude 的 web_fetch 工具设计为仅获取用户提供或来自其配套 web_search 工具的精确 URL，但该漏洞允许在获取页面内跟随链接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/agents-and-tools/tool-use/web-fetch-tool">Web fetch tool - Claude Platform Docs</a></li>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and ...</a></li>
<li><a href="https://arxiv.org/html/2510.09093">Exploiting Web Search Tools of AI Agents for Data Exfiltration</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论可能围绕漏洞的严重性以及 Anthropic 不支付漏洞赏金的决定展开，一些人质疑其内部发现声明的有效性。该帖子的作者 Simon Willison 是 AI 安全领域受人尊敬的人物，为披露增添了可信度。

**标签**: `#AI safety`, `#security vulnerability`, `#Claude`, `#data exfiltration`, `#prompt injection`

---

<a id="item-5"></a>
## [为 JEPA 世界模型寻找反对意见](https://www.reddit.com/r/MachineLearning/comments/1uxcryc/looking_for_jepa_devil_advocates_r/) ⭐️ 8.0/10

一位研究人员在 Reddit 上积极征求对 Yann LeCun 提出的 JEPA（联合嵌入预测架构）用于机器人学习世界模型的批评意见，质疑其相对于其他方法的潜在缺点。 这一讨论凸显了围绕 JEPA 作为 LLM 和 RL 潜在替代方案的日益激烈的辩论，并可能揭示被忽视的局限性，从而影响机器人学中世界模型的研究方向。 该帖子指出，LeCun 的演讲经常贬低 LLM 和 RL，同时将 JEPA 宣传为下一个重大突破，因此需要平衡的批评。研究人员特别询问了 JEPA 相对于其他世界模型方法的危险信号和缺点。

reddit · r/MachineLearning · /u/Amazing-Coat5160 · 7月15日 17:34

**背景**: JEPA（联合嵌入预测架构）是 Yann LeCun 提出的框架，通过在潜在空间中预测缺失信息来学习表征，而不是重建像素。它被定位为构建能够支持机器人规划和推理的世界模型的路径，与生成模型和强化学习形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rohitbandaru.github.io/blog/JEPA-Deep-Dive/">Rohit Bandaru | Deep Dive into Yann LeCun’s JEPA</a></li>
<li><a href="https://www.linkedin.com/pulse/understanding-yann-lecuns-jepa-llms-vs-predictive-world-azad-cdw6c/">Understanding Yann LeCun’s JEPA: LLMs vs ... - LinkedIn</a></li>
<li><a href="https://arxiv.org/html/2605.00080v1">World Model for Robot Learning: A Comprehensive Survey</a></li>

</ul>
</details>

**社区讨论**: Reddit 帖子可能包含实质性的批评，例如对 JEPA 经验不成熟、缺乏规划能力以及难以扩展到复杂任务的担忧。一些评论者可能捍卫 JEPA 的理论优雅性，而另一些则指出实际挑战。

**标签**: `#JEPA`, `#world models`, `#robot learning`, `#Yann LeCun`, `#machine learning`

---

<a id="item-6"></a>
## [哈达玛积聚类解开 InceptionV1 神经元](https://www.reddit.com/r/MachineLearning/comments/1uwya70/mechanistic_interpretability_a_first_paper_on/) ⭐️ 8.0/10

一种新方法利用哈达玛积聚类揭示了 InceptionV1 神经元中的单语义模式，包括意外的低值聚类（如字母）。该技术提供了卷积神经元检测内容的详细视图。 这项工作通过提供分析卷积神经元的新方法推进了机械可解释性，可能增进我们对神经网络如何处理视觉信息的理解。它还提供了梯度下降有意将模式置于噪声范围的证据。 该方法对感受野与神经元权重的哈达玛积进行聚类，为已知概念（汽车、猫、狗）产生清晰的聚类，并为字母和面孔产生额外聚类。分析显示，低值聚类中的依赖神经元也在同一概念上激活，正负权重均匀分布以降低总和。

reddit · r/MachineLearning · /u/narang_27 · 7月15日 06:59

**背景**: 机械可解释性旨在通过理解神经元等单个组件来逆向工程神经网络。哈达玛积是矩阵的元素级乘法，此处用于结合感受野和权重。InceptionV1 是一种卷积神经网络架构，以其包含 1x1 卷积的 Inception 模块而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hadamard_product_(matrices)">Hadamard product (matrices) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Inception_(deep_learning_architecture)">Inception (deep learning architecture) - Wikipedia</a></li>
<li><a href="https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html">Scaling Monosemanticity: Extracting Interpretable Features ...</a></li>

</ul>
</details>

**社区讨论**: Reddit 讨论中，作者提到从卷积开始可能限制了兴趣，并计划转向语言模型。评论者可能提供技术反馈，但未显示具体评论。

**标签**: `#mechanistic interpretability`, `#convolutional neural networks`, `#disentanglement`, `#interpretability`, `#deep learning`

---

<a id="item-7"></a>
## [谷歌与 Epic 撤回动议，第三方应用商店即将入驻 Play](https://www.theverge.com/policy/965792/google-epic-withdraw-injunction-third-party-app-stores-coming-google-play) ⭐️ 8.0/10

谷歌与 Epic Games 已共同撤回修改永久禁令的动议，谷歌将于 7 月 22 日起开始在 Google Play 上托管第三方应用商店。 这一进展迫使 Google Play 托管竞争对手的应用商店，可能重塑 Android 应用分发格局，并增加移动生态系统中的竞争。 第三方商店需每年支付 5000 美元的安全与政策审查费，并满足不得在美国以外分发、对开发者开放等要求。美国开发者可以选择退出，不让其应用在第三方商店中列出。

telegram · zaihuapd · 7月15日 11:15

**背景**: Epic 诉谷歌反垄断案始于 2020 年，Epic 因谷歌应用商店政策起诉谷歌。2024 年，陪审团裁定谷歌存在垄断行为，导致法院发布永久禁令，要求谷歌允许第三方应用商店。第九巡回上诉法院于 2025 年 7 月维持了该禁令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Epic_Games_v._Google">Epic Games v. Google - Wikipedia</a></li>
<li><a href="https://9to5google.com/2026/07/15/google-play-store-third-party-android-app-store-changes-july/">Google opens the floodgates to third - party app stores on Android</a></li>
<li><a href="https://www.cnet.com/tech/google-play-third-party-app-stores-android/">Google Play Opens the Door to Third - Party App Stores ... - CNET</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#app stores`, `#Google Play`, `#Epic Games`, `#Android`

---

<a id="item-8"></a>
## [DeepSeek 完成首轮融资，腾讯成第一大外部股东](https://www.cls.cn/detail/2427193) ⭐️ 8.0/10

DeepSeek 完成了首轮外部融资，腾讯通过持股超 33%的投资平台成为其第一大外部股东。公司还计划本月发布完整版 DeepSeek-V4 模型，并已启动涵盖 AI Agent、代码智能体和底层算力框架等岗位的大规模招聘。 本轮融资涉及腾讯、宁德时代、网易、京东等中国主要科技和投资公司，表明业界对 DeepSeek AI 能力的高度信心。即将发布的 DeepSeek-V4 和积极招聘表明该公司正在扩大规模，以与全球领先的 AI 模型竞争。 腾讯间接持有投资平台杭州程砺超 33%的份额，成为第一大外部股东；其他投资者包括宁德时代（11.7%）、网易（10%）、京东（10%）、IDG（10%）和国家人工智能产业投资基金（0.28%）。DeepSeek-V4 将是一个混合专家模型，参数高达 1.6 万亿，上下文窗口为 100 万 token。

telegram · zaihuapd · 7月15日 12:56

**背景**: DeepSeek 是一家中国 AI 公司，由对冲基金幻方量化 CEO 梁文锋于 2023 年创立。2025 年初，其 R1 模型以极低的训练成本实现了与 OpenAI GPT-4 相当的性能，从而引起全球关注。DeepSeek 的模型采用开放权重，因其成本效益和性能而被描述为“颠覆 AI”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek</a></li>
<li><a href="https://deepseek.com/en/index.html">DeepSeek</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro">deepseek-ai/DeepSeek-V4-Pro · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI`, `#funding`, `#DeepSeek`, `#Tencent`, `#large language models`

---

<a id="item-9"></a>
## [Simon Willison 通过 WebAssembly 将 Rust Mermaid 渲染器移植到浏览器](https://simonwillison.net/2026/Jul/16/grok-mermaid/#atom-everything) ⭐️ 7.0/10

Simon Willison 利用 WebAssembly 将 Grok CLI 代码库中基于 Rust 的 Mermaid 图表渲染器移植到浏览器，创建了一个在线工具，可将 Mermaid 源代码转换为 Unicode 方框绘图艺术。 这展示了 WebAssembly 将 Rust 终端渲染器引入 Web 的实用且创造性的用法，使开发者无需安装任何软件即可预览 Mermaid 图表的 Unicode 艺术效果。同时，它也展示了像 Grok 这样的 AI 工具中的开源组件如何被重新用于更广泛的用途。 该工具支持流程图、时序图、状态图、类图和 ER 图；其他图表类型则回退为带框的源代码列表。Rust 渲染器通过 wasm-bindgen 编译为 WebAssembly，完全在客户端运行。

rss · Simon Willison · 7月16日 00:33

**背景**: Mermaid 是一种流行的基于 JavaScript 的图表工具，可将类似 Markdown 的文本渲染为图表。Grok CLI 是 xAI 的开源编码代理，包含一个基于 Rust 的 Mermaid 渲染器，用于终端输出。WebAssembly 允许用 Rust 等语言编写的代码以接近原生速度在浏览器中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tools.simonwillison.net/grok-mermaid">Mermaid to Unicode box art (grok-mermaid)</a></li>
<li><a href="https://github.com/simonw/tools/tree/main/grok-mermaid">tools/grok-mermaid at main · simonw/tools · GitHub</a></li>

</ul>
</details>

**标签**: `#WebAssembly`, `#Mermaid`, `#Rust`, `#tool`, `#Simon Willison`

---

<a id="item-10"></a>
## [OpenAI 提出“反向联邦制”推进 AI 安全](https://openai.com/index/advancing-ai-safety-through-state-and-federal-action) ⭐️ 6.0/10

OpenAI 提出了一种“反向联邦制”的 AI 治理方法，即由各州的 AI 安全法律推动并帮助构建统一的国家框架。该公司已支持伊利诺伊州的 AI 立法作为这一策略的范例。 这一提议可能影响美国如何监管 AI，在州级试验与联邦统一之间取得平衡。它反映了一家主要 AI 公司在日益增长的 AI 安全监管呼声中试图影响政策走向。 “反向联邦制”概念与传统自上而下的联邦监管不同，而是让各州先行，然后在国家层面协调其做法。OpenAI 尚未明确说明除伊利诺伊州外还支持哪些具体州法律。

rss · OpenAI Blog · 7月15日 12:00

**背景**: 美国目前缺乏全面的联邦 AI 立法，导致各州法律零散不一。AI 监管中的联邦制概念涉及平衡州与联邦的权力，最近的行政命令已转向放松管制和提升国家竞争力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openaiglobalaffairs.substack.com/p/reverse-federalism-for-ai">'Reverse Federalism' for AI</a></li>
<li><a href="https://gizmodo.com/openai-wants-to-rewrite-its-washington-playbook-with-reverse-federalism-strategy-2000762053">OpenAI Wants to Rewrite Its Washington Playbook With 'Reverse Federalism' Strategy</a></li>
<li><a href="https://lawrecord.com/2025/10/17/artificial-authority-federalism-preemption-and-the-constitutional-structure-of-ai-regulation/">ARTIFICIAL AUTHORITY: FEDERALISM, PREEMPTION, AND THE CONSTITUTIONAL STRUCTURE OF AI REGULATION | The Rutgers Law Record</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#AI governance`, `#policy`, `#OpenAI`

---

<a id="item-11"></a>
## [综述：类人 AI 作为后图灵时代的社会伙伴](https://news.google.com/rss/articles/CBMibEFVX3lxTE9ob0gwZXpENVk5Vmp5bUxrbldqTGNFbUZOR3dnMzVhaGdERzZiS2JZOWZvNXI3ZFRPcGJvX0xWOVRKWUxkc294Ym1lMFZPRTJVMU90d1phNE9DUE1YcnJVTTJrRF9HM21IT2lEYg?oc=5) ⭐️ 6.0/10

一篇发表在《Frontiers in Artificial Intelligence》上的范围综述探讨了类人对话代理作为社会伙伴的角色，重点关注后图灵时代的社会情感机制、福祉结果、风险与治理。 该综述综合了当前关于伴侣 AI 的知识，这种技术正成为主流的关系技术，并强调了随着用户越来越多地将 AI 视为社会伙伴，治理框架的必要性。 该综述涵盖了信任、同理心和拟人化等社会情感属性，并讨论了情感依赖和伦理问题等风险。它提出从图灵测试评估转向适应性、多维框架。

google_news · 生物通 · 7月15日 23:59

**背景**: 后图灵时代超越了图灵测试，评估 AI 不仅基于模仿人类，还基于学习和社会影响。类人对话代理（如伴侣 AI）越来越多地用于社交互动，引发了关于依恋和福祉的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2026.1810097/full">Frontiers | Human-like conversational agents as social partners...</a></li>
<li><a href="https://www.emergentmind.com/topics/post-turing-test-era">Post - Turing Test Era in AI</a></li>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/39474095/">The role of socio - emotional attributes in enhancing human - AI ...</a></li>

</ul>
</details>

**标签**: `#conversational AI`, `#social agents`, `#human-computer interaction`, `#AI ethics`, `#well-being`

---