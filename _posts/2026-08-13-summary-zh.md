---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 40 条内容中筛选出 10 条重要资讯。

---

1. [Google DeepMind 发布 Gemini 3.7 Flash](#item-1) ⭐️ 9.0/10
2. [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，声称推理速度提升 7 倍](#item-2) ⭐️ 8.0/10
3. [理解代码成为软件开发的新瓶颈](#item-3) ⭐️ 8.0/10
4. [DeepSeek Harness 开发者预览版：开源、可追踪的 AI 代理框架](#item-4) ⭐️ 8.0/10
5. [DRAM“意大利面化”攻击：绕过硬件防护的新技术](#item-5) ⭐️ 8.0/10
6. [选择无聊的技术：关于创新代币的经典文章](#item-6) ⭐️ 8.0/10
7. [OpenAI 的 GPT-5.6 构建者指南](#item-7) ⭐️ 8.0/10
8. [DeepSeek V4 Pro 0813 发布，开放权重](#item-8) ⭐️ 8.0/10
9. [DeepMind 的 SL2T 将手语转文字 AI 带到 Pixel 11](#item-9) ⭐️ 8.0/10
10. [alchemy-utils 0.1a1 提升 DuckDB 导出与 CSV 导入性能](#item-10) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Google DeepMind 发布 Gemini 3.7 Flash](https://deepmind.google/blog/introducing-gemini-3-7-flash/) ⭐️ 9.0/10

Google DeepMind 发布了 Gemini 3.7 Flash，这是 Gemini 3 系列中的新 AI 模型，具有改进的推理、编码和智能体能力。该模型现已通过 Gemini API 提供，定位为高性价比的主力模型。 此次发布增强了 Google 在 AI 模型市场中的竞争地位，提供了一个低成本、高性能的选择，挑战了 OpenAI 的 GPT-5.6 Luna 等竞争对手。对于寻求经济实惠模型以处理高容量任务（如摘要、解析和智能体工作流）的开发者和企业尤为重要。 Gemini 3.7 Flash 比 3.6 Flash 便宜 35%，提示缓存命中率提高 8%，工具错误更少。在 GDP.pdf 基准上显著优于 3.6 Flash（34.0% 对 22.0%），且介绍性定价将于 2026 年 12 月 31 日翻倍。

rss · Google DeepMind Blog · 8月13日 17:04

**背景**: Gemini 3.7 Flash 是 Google DeepMind 的 Gemini 3 模型系列的一部分，该系列专注于以高效方式提供先进的 AI 能力。Flash 系列专为低成本、高容量的使用场景设计，此版本对其核心推理基础进行了算法改进。该模型还支持智能体工作流，能够编排子智能体并生成交互式网页。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.7 Flash — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3.7 Flash: our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3.7 Flash - Model Card — Google DeepMind</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：一些人称赞 Gemini 3.7 Flash 的视觉到 HTML 能力，指出它在与更昂贵的模型（如 Opus 5）相比时表现良好。其他人批评其定价策略，指出介绍性价格在几个月内翻倍很不寻常，并将其与更便宜的替代品（如 GPT-5.6 Luna）进行不利比较，有些人认为后者在成本上提供了更好的性能。

**标签**: `#AI`, `#Google DeepMind`, `#Gemini`, `#Machine Learning`

---

<a id="item-2"></a>
## [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，声称推理速度提升 7 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI 与 Cerebras 宣布推出 GPT-5.6 Sol Ultrafast，这是 OpenAI API 中由 Cerebras 硬件驱动的新服务层级，运行速度比标准处理快达 14 倍，每秒可生成多达 750 个输出 token。在评估中，它用 11 小时 11 分钟回答了全部 2500 个 HLE 问题，以接近 7 倍的速度达到了与 Claude Fable 5 相当的准确率。 此次合作标志着 AI 推理速度的一个重要里程碑，可能推动更多交互式和实时应用的发展。速度的提升可能将焦点从模型原始质量转向推理效率，影响开发者构建和部署 AI 产品的方式。 该服务层级由 Cerebras 晶圆级引擎技术驱动，提供超低延迟和高解码性能。然而，公告并未明确确认与标准 GPT-5.6 Sol 的性能完全一致，且未披露定价细节。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: GPT-5.6 Sol 是 OpenAI 的前沿 AI 模型，而 Cerebras 专注于晶圆级芯片，提供极快的推理速度。Humanity's Last Exam（HLE）是一个基准测试，旨在测试 AI 模型在跨领域专家级问题上的表现。此次合作旨在将 OpenAI 的模型能力与 Cerebras 的硬件相结合，以实现前所未有的推理速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai">Accelerating GPT - 5 . 6 Sol Ultrafast with OpenAI</a></li>
<li><a href="https://openai.com/index/previewing-ultrafast/">Previewing Ultrafast mode: GPT - 5 . 6 Sol at up to 14X the... | OpenAI</a></li>
<li><a href="https://artificialanalysis.ai/evaluations/humanitys-last-exam">Humanity's Last Exam Benchmark Leaderboard | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: 社区评论对速度提升表示兴奋，但也对性能一致性表示担忧，并指出公告未明确确认 Ultrafast 模式是否与标准 Sol 的准确性完全一致。一些用户强调速度对迭代思维的重要性，而另一些用户则注意到缺乏定价信息，并质疑速度是否以牺牲质量为代价。

**标签**: `#LLM`, `#AI acceleration`, `#OpenAI`, `#Cerebras`, `#inference`

---

<a id="item-3"></a>
## [理解代码成为软件开发的新瓶颈](https://www.geoffreylitt.com/2026/07/02/understanding-is-the-new-bottleneck) ⭐️ 8.0/10

Geoffrey Litt 的文章认为，随着 LLM 自动化代码生成，软件开发的主要瓶颈从编写代码转向理解代码，并呼吁新的工具和实践。这篇文章引发了社区的热烈讨论，评分达到 8.0/10。 这一转变对软件工程角色、工具和教育具有重大影响，开发者必须优先考虑理解能力而非纯粹的编码速度。它也凸显了 AI 辅助开发中日益严峻的挑战，即对生成代码的信任和验证变得至关重要。 文章指出，现有的工具如 LLM 生成的 PR 描述往往不受欢迎，因为它们缺乏动机和上下文。文章还指出，依赖 LLM 理解代码会削弱人工验证过程，因为 LLM 可能是错误的。

hackernews · sebg · 8月13日 18:47 · [社区讨论](https://news.ycombinator.com/item?id=49290299)

**背景**: LLM（大型语言模型）是在大量文本（包括代码）上训练的 AI 系统，能够生成类似人类的响应。在软件开发中，它们越来越多地被用于根据自然语言描述编写代码，但这引发了对代码质量和可维护性的担忧。代码理解工具（如 CodeCompass）通过可视化和交叉引用帮助开发者理解现有代码库，随着 AI 生成更多代码，这一点变得更加关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/chiragdoshi_the-question-is-not-how-do-we-generate-more-activity-7480100833318211584-Pq-Q">Code Generation Bottleneck : Alignment and Testing | LinkedIn</a></li>
<li><a href="https://www.sonarsource.com/resources/library/llm-code-generation/">LLMs for Code Generation : A summary of the research on quality</a></li>
<li><a href="https://codecompass.net/">CodeCompass: An Open Software Comprehension Framework</a></li>

</ul>
</details>

**社区讨论**: 社区评论反映了复杂的情绪：一些人同意问题存在但质疑提出的解决方案，指出这个问题在 LLM 出现之前就已存在。其他人强调人类理解对于验证的重要性，还有一些人对文章缺乏具体证据表示不满。

**标签**: `#LLM`, `#software engineering`, `#code comprehension`, `#developer tools`, `#AI-assisted development`

---

<a id="item-4"></a>
## [DeepSeek Harness 开发者预览版：开源、可追踪的 AI 代理框架](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek 发布了 Harness 的开源开发者预览版，这是一个以插件为先的 AI 代理运行时，源代码已在 GitHub 上以 MIT 许可证提供。该工具通过仅追加的会话日志提供代理运行的完整可追溯性，支持恢复、分叉、搜索和重放操作。 此次发布解决了 AI 代理开发中的一个关键缺口：透明度和可重放性。与美国模型通常加密或混淆痕迹不同，DeepSeek Harness 提供开放、可检查的日志，这可能促进代理开发中更高的信任度和调试能力。它还引入了插件架构，允许替换和重新组合每个能力，可能影响未来代理框架的设计。 该框架基于 Cordis v4 构建，支持热重载和动态启用/禁用插件而无需重启进程，并能在卸载时还原状态和副作用。开发者预览版处于早期阶段，作者指出预计会有粗糙之处和破坏兼容性的更改。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: AI 代理是能够通过交互工具和模型自主执行任务的软件系统。可追溯性是指记录和检查代理所做的每个动作和决策的能力，这对于调试、审计和改进性能至关重要。插件架构允许模块化定制，其中模型、工具和 UI 等组件可以替换或重新组合。DeepSeek Harness 利用这些概念为代理开发提供了灵活且透明的运行时。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://deepseek-code.com/">DeepSeek Harness: Open-Source AI Agent Framework</a></li>
<li><a href="https://github.com/HenryZ838978/deepseek-harness">GitHub - HenryZ838978/deepseek-harness: Harness for DeepSeek V4-Pro / V4-Flash. Python lib (pip install deepseek-harness) + dsh CLI + MCP server (npx @deepseek-harness/mcp) + Anthropic SKILL.md. 16 documented protocol quirks, 12 probes, 270+ trials. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区反馈总体积极，一位用户称可追溯性功能是“杀手级功能”，并与美国模型不透明的痕迹形成对比。一位作者承认这是早期预览版，存在粗糙之处。另一位用户指出了底层的 Cordis v4 技术，该技术支持热重载和状态还原，而有些人则表达了插件疲劳，质疑对插件架构的过度依赖。

**标签**: `#AI`, `#Open Source`, `#Developer Tools`, `#Traceability`, `#DeepSeek`

---

<a id="item-5"></a>
## [DRAM“意大利面化”攻击：绕过硬件防护的新技术](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 8.0/10

安全研究员 Christopher Domas 发布了一项名为“DRAM 意大利面化”的技术，能够在某些 AMD 处理器上实现完全内存访问并绕过硬件防护。该方法已在 GitHub 仓库中展示，并预计将在 Black Hat 大会上公布。 这项研究揭示了一种在硬件层面破坏系统安全的新方法，可能影响较老的 AMD CPU，并引发对游戏机安全的担忧。它凸显了 DRAM 中日益增长的攻击面以及现代内存子系统安全防护的难度。 该技术适用于 AMD Jaguar（16h 系列），并提到 Zen 3 的内存控制器寄存器基地址不同，但对更新 CPU 的完整影响尚不明确。攻击需要 ring-0 权限，但一旦获得，就能访问隐藏的“负环”区域，可能绕过内存加密等防护。

hackernews · matt_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 是一种易失性存储器，每个位存储在电容器中，需要定期刷新。现代 DRAM 控制器复杂且常依赖专有固件，形成了巨大的攻击面。此前如 Rowhammer 等攻击已表明 DRAM 可被操纵以绕过安全防护，而这项新技术延续了这一趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dynamic_random-access_memory">Dynamic random-access memory - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Row_hammer">Row hammer - Wikipedia</a></li>
<li><a href="https://www.darkreading.com/vulnerabilities-threats/cheap-hardware-module-amd-intel-memory-encryption">Cheap Device Bypasses AMD, Intel Memory Encryption</a></li>

</ul>
</details>

**社区讨论**: 评论者对研究员的 Black Hat 演讲表示期待，并称赞他过去的演讲。一些人指出该攻击可能影响游戏机安全，而另一些人则质疑其对更新 CPU 的适用性，指出演示的 AMD Jaguar 是 2013 年的产品，并询问对 Zen 3 及以后的影响。

**标签**: `#security`, `#DRAM`, `#hardware`, `#exploit`, `#reverse engineering`

---

<a id="item-6"></a>
## [选择无聊的技术：关于创新代币的经典文章](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

丹·麦金利（Dan McKinley）于 2015 年发表的《选择无聊的技术》一文认为，公司应该在大多数问题上优先选择成熟、无聊的技术，并将“创新代币”节省下来，用于能带来真正竞争优势的领域。这篇文章在社区讨论中重新浮出水面，并出现了一个新颖的延伸观点：在 AI 代理时代，应将所有创新代币投入代理，而其他一切则使用无聊的技术。 这篇文章已成为务实工程文化的基石，影响着团队如何做出技术选择和权衡。它的重新流行，尤其是与 AI 代理相关的延伸，表明在快速发展的技术栈和新工具炒作中，它对于指导决策仍然具有现实意义。 核心概念是每家公司拥有有限数量的“创新代币”，用于采用新的或新颖的技术，这些代币应保留给直接有助于竞争优势的领域。文章强调，“无聊的技术”并非贬义，而是指成熟、被充分理解且可靠的技术，能降低风险和运营负担。

hackernews · tosh · 8月13日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=49289512)

**背景**: 这篇文章由丹·麦金利于 2015 年撰写，他曾就职于 Etsy 和 Stripe 等公司。文章针对工程师们常见的倾向：在没有充分考虑长期成本（如维护、招聘和调试）的情况下采用最新技术。“创新代币”的比喻为做出深思熟虑的技术选择提供了一个简单的框架。

**社区讨论**: 社区讨论总体上是积极的，许多人称赞“创新代币”概念是做出权衡的有用思维模型。一些人提出反对意见，认为这个概念过于武断，工程师应根据需求和风险来评估技术，而不是看其新颖性。一个值得注意的评论将这一想法扩展到 AI 代理，建议将所有创新代币花在代理上，而其余部分则使用无聊的技术。

**标签**: `#technology-choice`, `#engineering-culture`, `#innovation`, `#software-engineering`, `#essay`

---

<a id="item-7"></a>
## [OpenAI 的 GPT-5.6 构建者指南](https://openai.com/index/builders-guide-to-gpt-5-6) ⭐️ 8.0/10

OpenAI 发布了 GPT-5.6 的构建者指南，展示了初创公司如何通过更智能的模型选择和新的 Responses API 功能，构建更快、更具成本效益的 AI 代理。该指南介绍了三个模型变体：GPT-5.6 Sol 用于复杂推理，GPT-5.6 Terra 用于平衡智能和成本，GPT-5.6 Luna 用于成本敏感、高吞吐量的工作负载。 该指南意义重大，因为它为开发者提供了利用 GPT-5.6 改进的成本-性能权衡的实用指导，可能降低构建先进 AI 代理的门槛。它还凸显了 OpenAI API 生态系统的演进，Responses API 正成为代理应用的核心工具。 该指南强调“更智能的模型选择”以避免浪费 token，指出 GPT-5.6 Sol 对于数据提取等简单任务可能过于强大，而最大推理设置对于会议摘要等任务可能造成浪费。Responses API 于 2025 年 3 月 11 日发布，结合了 Chat Completions API 的易用性和高级工具调用能力，支持文本和图像输入、文本输出，以及文件搜索、网络搜索和计算机使用等内置工具。

rss · OpenAI Blog · 8月13日 11:00

**背景**: GPT-5.6 是 OpenAI 的新模型系列，旨在让前沿级别的代理性能更加实惠。Responses API 是一个开发者工具，旨在通过提供统一的接口来简化代理应用的创建，支持有状态交互和工具使用。模型选择对于成本优化至关重要，因为不同变体在智能和成本之间提供了不同的权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/builders-guide-to-gpt-5-6/">The builder’s guide to GPT ‑ 5 . 6 | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/reference/responses/overview">Responses Overview | OpenAI API Reference</a></li>
<li><a href="https://developers.openai.com/api/docs/models">Explore all available models on the OpenAI Platform. | OpenAI API</a></li>

</ul>
</details>

**标签**: `#GPT-5.6`, `#OpenAI`, `#AI agents`, `#Responses API`, `#LLM`

---

<a id="item-8"></a>
## [DeepSeek V4 Pro 0813 发布，开放权重](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 8.0/10

DeepSeek 已发布 V4 Pro 0813 模型，现可通过 OpenRouter 的 API 使用，并在 Hugging Face 上开放权重（1.7T 参数，893 GB）。该模型引入了新的推理级别（低、中、高）并增强了智能体能力，峰谷定价将于 2026 年 8 月 17 日生效。 这一来自主要 AI 实验室的开放权重发布可能对 LLM 生态系统产生重大影响，提供了一个具有先进智能体能力的高参数模型。在 OpenRouter 和 Hugging Face 上的可用性使其对开发者和研究人员可及，可能加速 AI 应用的创新。 该模型最初仅通过 API 提供，但现在权重已在 Hugging Face 上。值得注意的是，模型在不同推理级别（低、中、高）下产生非常不同的输出，正如在鹈鹕图像生成测试中观察到的那样。基准测试通过非官方渠道（微信、Reddit、Hacker News）分享，因为官方帖子被删除。

rss · Simon Willison · 8月12日 23:59

**背景**: DeepSeek 是一家以发布开放权重模型而闻名的中国 AI 研究公司。V4 Pro 是一个拥有 1.7 万亿参数的大型语言模型，专为编码、工具使用和智能体工作流设计。OpenRouter 是一个用于访问各种 LLM 的统一 API，而 Hugging Face 是一个托管和共享模型权重的平台。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/multimodalart/DeepSeek-V4-Pro-0813">multimodalart/ DeepSeek - V 4 - Pro - 0813 · Hugging Face</a></li>
<li><a href="https://nano-gpt.com/models/text/deepseek/deepseek-v4-pro-0813">DeepSeek V 4 Pro 0813 model | NanoGPT</a></li>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 提供的内容不包含社区评论，但提到的 Hacker News 帖子中有一个 ASCII 艺术基准表，表明有一定的社区参与。然而，没有具体的情绪或观点可用。

**标签**: `#AI`, `#DeepSeek`, `#model release`, `#open weights`, `#LLM`

---

<a id="item-9"></a>
## [DeepMind 的 SL2T 将手语转文字 AI 带到 Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

谷歌 DeepMind 发布了多语言手语转文字模型 SL2T，并首次将其部署到消费产品中：Pixel 11 上的 Gboard 和 Live Transcribe，最初支持美国手语（ASL）转英语。该模型使用超过 10 万小时、涵盖 50 多种手语的数据进行训练，在 FLEURS-ASL 基准上零样本 BLEURT 得分达到 70。 这标志着无障碍 AI 迈出了重要一步，因为它是首个在真实消费产品中推出的手语 AI，可能改善聋人和听力障碍用户的沟通体验。同时，它也展示了 DeepMind 将多模态翻译模型扩展到实际应用的能力，可能影响整个行业未来的无障碍功能。 为保护隐私，SL2T 仅处理手部和身体姿态关键点，而非原始视频，确保用户数据不泄露。该模型最初仅限于 Pixel 11 上的 ASL 转英语，未来计划扩展到更多设备和语言。

telegram · zaihuapd · 8月13日 08:55

**背景**: 手语翻译历来在主流机器翻译研究中处于边缘地位。FLEURS-ASL 是 2024 年推出的基准，将 FLORES 和 FLEURS 基准扩展至包含美国手语，由认证聋人翻译员翻译，用于评估手语理解能力。BLEURT 是一种用于文本质量评估的学习型指标，70 分表示与人工参考高度相似。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datanorth.ai/news/google-deepmind-releases-sl2t">Google DeepMind releases SL 2 T sign language AI - DataNorth</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/google-sign-language-model-body-landmarks">Google's new model turns sign language into text for web searches</a></li>
<li><a href="https://arxiv.org/abs/2408.13585">FLEURS-ASL: Including American Sign Language in Massively ... (PDF) FLEURS-ASL: Including American Sign Language in ... Title:FLEURS-ASL: Including American Sign Language in ... [PDF] FLEURS-ASL: Including American Sign Language in ... AITopics | FLEURS-ASL: Including American Sign Language in ... FLEURS-ASL: Including American Sign Language in Massively ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Accessibility`, `#Sign Language`, `#DeepMind`, `#Machine Learning`

---

<a id="item-10"></a>
## [alchemy-utils 0.1a1 提升 DuckDB 导出与 CSV 导入性能](https://simonwillison.net/2026/Aug/13/alchemy-utils/) ⭐️ 5.0/10

alchemy-utils 0.1a1 已发布，主要改进了 DuckDB 导出和 CSV 导入的性能。该版本已在 GitHub 上发布，并在 Simon Willison 的博客上进行了公告。 此版本对使用 DuckDB 和 CSV 工作流的开发者很重要，因为更快的导出和导入可以显著减少数据处理时间。同时，它也展示了 alchemy-utils 库的持续改进，该库旨在跨多种数据库提供一致的 table-first API。 性能提升主要针对 DuckDB 导出和 CSV 导入，但发布说明中未提供具体的基准测试或实现细节。根据 GitHub 仓库描述，该库基于 SQLAlchemy Core 构建，支持 SQLite、PostgreSQL 和 DuckDB。

rss · Simon Willison · 8月13日 03:03

**背景**: alchemy-utils 是一个跨数据库的实用工具库，灵感来自 sqlite-utils，提供 table-first 的数据库操作 API。它使用 SQLAlchemy Core 支持多种数据库，包括 DuckDB——一种以快速查询性能著称的进程内分析数据库。导出和导入操作的性能改进很有价值，因为 DuckDB 常用于数据管道，数据传输速度至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/alchemy-utils">GitHub - simonw/alchemy-utils: Cross-database sqlite-utils ...</a></li>
<li><a href="https://duckdb.org/2024/06/26/benchmarks-over-time.html">Benchmarking Ourselves over Time at DuckDB – DuckDB</a></li>

</ul>
</details>

**标签**: `#DuckDB`, `#CSV`, `#Python`, `#release`, `#performance`

---