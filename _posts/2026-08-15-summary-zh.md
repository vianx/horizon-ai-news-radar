---
layout: default
title: "Horizon Summary: 2026-08-15 (ZH)"
date: 2026-08-15
lang: zh
---

> 从 36 条内容中筛选出 7 条重要资讯。

---

1. [将《毁灭战士》渲染器编译为 210 亿参数 Transformer，无需训练](#item-1) ⭐️ 9.0/10
2. [Qwen 3.8 27B：社区验证的强本地大模型](#item-2) ⭐️ 8.0/10
3. [走向黑暗与执法黑客的转变](#item-3) ⭐️ 8.0/10
4. [RustDesk 在 Wayland 上实现真正的无人值守访问](#item-4) ⭐️ 8.0/10
5. [Firefox 成为唯一支持 uBlock Origin 的主流浏览器](#item-5) ⭐️ 8.0/10
6. [AI 机器人实验室年测 300 万人体组织样本，有望终结动物测试](#item-6) ⭐️ 8.0/10
7. [别分类，去幻觉：一种新的标签生成技术](#item-7) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [将《毁灭战士》渲染器编译为 210 亿参数 Transformer，无需训练](https://www.reddit.com/r/MachineLearning/comments/1voazhm/i_compiled_dooms_renderer_into_a_21bparameter/) ⭐️ 9.0/10

作者将《毁灭战士》的渲染算法移植为计算图，并使用自定义编译器 torchwright 将其转换为 210 亿参数 Transformer 的权重。该模型生成像素绘制命令，执行这些命令即可重现游戏中的 E1M1 画面。 这展示了一种无需训练即可将复杂算法嵌入神经网络权重的新方法，可能为编程和控制 Transformer 提供新途径。它可能激发进一步研究，将任意计算编译进模型，连接传统软件与神经计算。 生成的检查点是标准 Transformers 检查点，无需 trust_remote_code 即可加载。渲染一帧需要 3,614 个 token 的提示并生成 53,747 个 token，在 B200 GPU 上约需 40 分钟，相当于每天约 35 帧，而原版《毁灭战士》在 486 上可达 35 FPS。

reddit · r/MachineLearning · /u/notforrob · 8月14日 15:50

**背景**: Transformer 是一种神经网络架构，通过注意力机制处理序列，通常在大数据集上训练。将计算图编译为 Transformer 权重是一种新兴技术，将程序逻辑直接编码到模型参数中，使模型在推理时执行程序。《毁灭战士》的渲染器使用二叉空间分割（BSP）等算法高效绘制 3D 场景，作者将其移植为图表示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/physicsrob/torchwright">physicsrob/torchwright: A compiler that transforms computation ...</a></li>
<li><a href="https://www.doomwiki.org/wiki/Rendering_engine">Doom rendering engine - The Doom Wiki at DoomWiki.org</a></li>

</ul>
</details>

**标签**: `#transformer`, `#compilation`, `#Doom`, `#neural networks`, `#AI`

---

<a id="item-2"></a>
## [Qwen 3.8 27B：社区验证的强本地大模型](https://huggingface.co/Qwen/Qwen3.8-27B-FP8) ⭐️ 8.0/10

Qwen 3.8 27B 是一款新发布的本地大语言模型，展现出强大的推理能力和性能，社区成员报告了成功的基准测试和在消费级硬件上的高效推理。它是 Qwen3.6-27B 的继任者，将 3.8 代的训练改进带到了可自托管的规模。 此次发布对本地大模型社区意义重大，因为它提供了一个可在消费级硬件上运行的高性能模型，可能使先进 AI 能力的获取更加民主化。社区的积极反响和关于推理引擎的实用见解表明其参与度和认可度很高，这可能影响未来模型的开发和应用。 社区基准测试显示相比上一版本有显著提升，Terminal-Bench 2.1 从 63.4 升至 73.0，DeepSWE 1.1 从 13.3 升至 42.2，OSWorld-Verified 从 63.9 升至 84.3，SWE-MM 从 25.7 升至 38.6。然而，阿里巴巴尚未公布架构细节（密集或 MoE）、上下文长度或许可证，且部分用户报告其 VRAM 使用效率低于其他模型。

hackernews · erdaltoprak · 8月14日 15:00 · [社区讨论](https://news.ycombinator.com/item?id=49299605)

**背景**: Qwen 是阿里巴巴开发的一系列大语言模型，以其强大的性能和开源可用性而闻名。本地大模型是指可以在消费级硬件（如笔记本电脑或台式机 GPU）上运行、无需依赖云服务的模型。这通过量化技术和高效推理引擎等实现，这些技术减少了内存占用并提高了速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yottalabs.ai/post/qwen-3-8-27b-specs-hardware-requirements-how-to-run-2026">Qwen 3.8 27B: Specs, Hardware Requirements, and How to Run It (2026) | Yotta Labs</a></li>
<li><a href="https://kingy.ai/blog/qwen3-8-27b-specs-benchmarks-local-hardware/">Qwen3.8-27B: Specs, Benchmarks & Verdict</a></li>
<li><a href="https://medium.com/practical-llm-systems/qwen-3-8-benchmarks-what-the-numbers-actually-say-4eeb8885ce70">Qwen 3.8 Benchmarks: What the Numbers Actually Say | by Rost Glukhov | Practical LLM Systems | Aug, 2026 | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区成员普遍对该模型的推理能力印象深刻，一位用户指出它是第二个能正确通过其私人基准测试的本地模型。其他人报告使用替代推理引擎可获得较高的 token 生成速度，还有人观察到与之前版本相比，模型的思考轨迹风格发生了显著变化。同时也有对 VRAM 效率的担忧，以及推测独特的思考模式可能影响多 token 预测性能。

**标签**: `#LLM`, `#local-models`, `#AI`, `#open-source`, `#benchmarks`

---

<a id="item-3"></a>
## [走向黑暗与执法黑客的转变](https://blog.cryptographyengineering.com/2026/08/14/everything-is-about-to-go-dark/) ⭐️ 8.0/10

文章分析了“走向黑暗”问题，并指出执法机构正越来越多地转向黑客技术，如利用软件漏洞来访问加密通信。文章认为，通过合法请求进行大规模监控的时代可能正在结束，取而代之的是有针对性的黑客行动。 这种转变对隐私、安全以及政府与公民之间的权力平衡具有重大影响。随着执法黑客行为日益普遍，它引发了关于漏洞利用限度及滥用可能性的问题，影响政策制定者、安全研究人员和公众。 文章指出，有用的软件漏洞数量可能达到上限，从而限制黑客作为执法工具的有效性。文章还讨论了运行窃听的成本和实际挑战，将过去的物理窃听与现代数字监控进行对比。

hackernews · vslira · 8月14日 20:52 · [社区讨论](https://news.ycombinator.com/item?id=49304447)

**背景**: “走向黑暗”问题指的是执法机构即使拥有合法法院命令，也难以访问加密通信和数据。随着加密技术的普及，机构开始探索黑客技术，如部署恶意软件或利用漏洞来绕过加密。这一趋势是隐私与安全更广泛辩论的一部分，FBI 等机构主张合法访问，而隐私倡导者则警告不要削弱加密。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theiacp.org/resources/critical-issues-encryption-going-dark">Critical Issues: Encryption & Going Dark</a></li>
<li><a href="https://carnegieendowment.org/research/2024/04/exploring-law-enforcement-hacking-as-a-tool-against-transnational-cyber-crime">Exploring Law Enforcement Hacking as a Tool Against Transnational Cyber ...</a></li>
<li><a href="https://observed.org/can-police-use-hacking-techniques/">Can Police Use Hacking Techniques? | Know Your Rights</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了不同观点：一些人强调了窃听的历史成本，而另一些人则怀疑软件漏洞并未减少，指出 AI 生成的代码引入了更多漏洞。一条讽刺评论批评了政府监控，另一条则指出复杂的执法黑客与许多组织糟糕的安全实践之间的对比。

**标签**: `#encryption`, `#law enforcement`, `#surveillance`, `#security`, `#privacy`

---

<a id="item-4"></a>
## [RustDesk 在 Wayland 上实现真正的无人值守访问](https://rustdesk.com/blog/unattended-remote-access-wayland/) ⭐️ 8.0/10

RustDesk 宣布支持在 Wayland 上实现真正的无人值守远程访问，这是 Linux 用户高度期待的功能。目前已经为基于 x86_64 Debian/Ubuntu 的系统提供了预览版，并支持多显示器。 此更新解决了依赖 Wayland 的 Linux 用户长期以来的痛点，因为之前的解决方案通常需要手动选择屏幕或在锁定会话中失效。它增强了 RustDesk 作为开源远程桌面工具的竞争力，可能吸引更多用户从 VNC 和专有替代方案转移过来。 该功能目前以预览版形式提供给基于 x86_64 Debian/Ubuntu 的系统，并支持多显示器。用户应注意这是预览版，因此在不同 Wayland 合成器上的稳定性和兼容性可能有所不同。

hackernews · rustdesk · 8月14日 16:12 · [社区讨论](https://news.ycombinator.com/item?id=49300759)

**背景**: Wayland 是一种显示服务器协议，已成为许多现代 Linux 发行版的默认协议，取代了较旧的 X11。与 X11 不同，Wayland 限制应用程序在未经用户明确许可的情况下捕获整个屏幕，这历来使得无人值守远程访问变得困难。RustDesk 是一款开源远程桌面工具，允许用户远程访问和控制计算机，类似于 TeamViewer 或 AnyDesk。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rustdesk.com/blog/unattended-remote-access-wayland/">Unattended Remote Access on Wayland with RustDesk</a></li>
<li><a href="https://github.com/rustdesk/rustdesk/discussions/10016">Wayland: Select the screen to be shared (Operate on the peer ...</a></li>
<li><a href="https://stackademic.com/blog/remote-desktop-on-wayland-in-2025-what-changed-for-linux-support-engineers">Remote Desktop on Wayland in 2025: What Changed for Linux ...</a></li>

</ul>
</details>

**社区讨论**: 社区成员对这一更新表示热情，一位用户提到他们两天前刚遇到这个问题。其他人则提出了关于自托管时 RustDesk 加密的疑问、与 VNC 在特定用例中的比较，以及它与通过 SSH 和 Tailscale 使用 Remmina 等解决方案的对比。

**标签**: `#RustDesk`, `#Wayland`, `#remote desktop`, `#open source`, `#Linux`

---

<a id="item-5"></a>
## [Firefox 成为唯一支持 uBlock Origin 的主流浏览器](https://www.pcworld.com/article/3212428/firefox-is-now-the-last-major-browser-that-still-supports-ublock-origin.html) ⭐️ 8.0/10

随着 Chrome 转向 Manifest V3 并限制了该扩展的功能，Firefox 现在成为唯一仍完全支持 uBlock Origin 的主流浏览器。这一转变标志着广告拦截领域的一次重大变化。 这很重要，因为 uBlock Origin 被广泛认为是最强大的广告拦截器之一，其在 Chrome 上功能的削弱影响了数百万依赖它进行隐私保护和广告拦截的用户。这也凸显了浏览器厂商与用户对网页内容控制权之间日益加剧的紧张关系。 Manifest V3 将扩展的规则数量限制在 30,000 条以内，而有效的广告拦截器通常需要超过 300,000 条规则。uBlock Origin 依赖 webRequest API 和动态过滤，这些在 MV3 下受到严重限制，迫使 Chromium 浏览器使用功能削减的“uBlock Origin Lite”。

hackernews · DemiGuru · 8月14日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49303202)

**背景**: Manifest V3 是基于 Chromium 的浏览器的最新扩展规范，定义了扩展能做什么和不能做什么。它用功能较弱的 declarativeNetRequest API 取代了强大的 webRequest API，限制了广告拦截器检查和阻止网络请求的方式。这一变化由谷歌引入，而谷歌本身也是大型广告业务的所有者，引发了利益冲突的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://adblock-tester.com/ad-blockers/manifest-v3-ad-blocker-impact/">The Manifest V3 Changes — Did Google Just Break Your Ad Blocker? (And What to Do Next) - AdBlock Tester</a></li>
<li><a href="https://www.techradar.com/pro/how-chromes-manifest-v3-will-change-the-game-for-ad-blockers">How Chrome’s Manifest V3 will change the game for ad blockers | TechRadar</a></li>
<li><a href="https://nordvpn.com/blog/manifest-v3-ad-blockers/">Is Google's Manifest V3 the end of ad blockers? | NordVPN</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 Firefox 审查 uBlock Origin 等流行扩展表示赞赏，并批评谷歌受广告驱动的决策。一些用户表示 uBlock Origin Lite 对他们来说够用，而另一些用户则对 Chrome 上功能完整的广告拦截器的消失感到遗憾。

**标签**: `#Firefox`, `#uBlock Origin`, `#ad-blocking`, `#Manifest V3`, `#privacy`

---

<a id="item-6"></a>
## [AI 机器人实验室年测 300 万人体组织样本，有望终结动物测试](https://www.fastcompany.com/91589344/the-worlds-largest-biological-datacenter-could-help-make-animal-testing-obsolete) ⭐️ 8.0/10

Vivodyne 在旧金山南部启动了全球最大的人体生物数据中心，配备 12 个机器人“蜂巢”实验室，每年可对人体组织进行超过 300 万次受控实验。这一容量是美国所有临床试验总和的两倍。 这一进展可能显著减少药物开发中对动物测试的依赖，解决临床试验失败率高的问题（约 90%在动物测试后仍失败）。它可能加速药物发现，并提高药物在人体中疗效和安全性的可预测性。 Vivodyne 已筹集 4000 万美元的 A 轮融资，以扩大其机器人和 AI 方法。该系统利用 AI 设计的实验，在实验室培养的全功能人体组织上进行，旨在使人类生物学在 AI 规模上可计算。

telegram · zaihuapd · 8月14日 01:48

**背景**: 动物测试长期以来一直是新药进入人体试验前的标准评估方法，但成本高昂且常常无法预测人体反应。组织工程和微流控芯片的进步催生了可能更好模拟人体生理的人体组织模型。现在，AI 和机器人技术被应用于自动化和规模化这些模型，可能提供一种更道德、更高效的动物测试替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://svdaily.com/2025/06/02/vivodyne-raises-40-million-to-open-lab-in-south-san-francisco/">Vivodyne Raises $40 Million to Open Lab in South San ...</a></li>
<li><a href="https://finance.yahoo.com/healthcare/articles/vivodyne-launches-world-largest-human-130000478.html?fr=sycsrp_catchall">Vivodyne Launches the World’s Largest Human Biological ...</a></li>
<li><a href="https://www.linkedin.com/pulse/vivodyne-lands-40m-replace-animal-testing-drug-phil-newman-gihge/">Vivodyne lands $40m to replace animal testing in drug development</a></li>

</ul>
</details>

**标签**: `#AI`, `#biotech`, `#drug discovery`, `#lab automation`, `#animal testing`

---

<a id="item-7"></a>
## [别分类，去幻觉：一种新的标签生成技术](https://simonwillison.net/2026/Aug/14/dont-classify-hallucinate/) ⭐️ 7.0/10

Doug Turnbull 提出了一种技术，让 LLM 在不知道现有词汇的情况下生成新标签，然后通过向量嵌入将这些想象中的标签匹配到最接近的真实标签。Simon Willison 在他的博客上强调了这种方法，指出其对于给未标记内容打标签的实用性。 该技术解决了向 LLM 输入数千个标签的可扩展性问题，为大型内容库实现高效准确的标签生成。它利用了 LLM 的创造力和嵌入相似性，为信息检索和内容管理领域的开发者提供了一种实用方法。 示例提示包含标签形状示例以指导模型，例如“家具 / 客厅家具 / 咖啡桌和边桌 / 咖啡桌”。匹配步骤使用向量嵌入来找到最接近的现有标签，从而避免将整个标签列表输入 LLM。

rss · Simon Willison · 8月14日 21:54

**背景**: LLM 幻觉通常指生成虚假或捏造的信息，但在这里被重新用作创造性生成步骤。向量嵌入将文本含义表示为数值向量，从而可以进行语义相似性比较。该技术结合了这些概念，将新标签映射到现有分类体系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2306.06085">Trapping LLM Hallucinations Using Tagged Context Prompts Trapping LLM “Hallucinations” Using Tagged Context Prompts Detecting and Correcting Hallucinations in LLMs via ... Detecting hallucinations in large language models using ... Detecting hallucinations with LLM-as-a-judge: Prompt ... 5 Practical Techniques to Detect and Mitigate LLM ... LLM Hallucinations: What They Are & How to Detect Them</a></li>
<li><a href="https://hackernoon.com/automating-content-tagging-in-laravel-using-openai-embeddings-and-cron-jobs">Automating Content Tagging in Laravel Using OpenAI Embeddings ...</a></li>
<li><a href="https://www.ibm.com/think/topics/vector-embedding">What is Vector Embedding ? | IBM</a></li>

</ul>
</details>

**标签**: `#LLM`, `#embeddings`, `#tagging`, `#information retrieval`, `#AI`

---