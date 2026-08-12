---
layout: default
title: "Horizon Summary: 2026-08-12 (ZH)"
date: 2026-08-12
lang: zh
---

> 从 43 条内容中筛选出 11 条重要资讯。

---

1. [研究人员从 LLM API 中窃取隐藏推理](#item-1) ⭐️ 9.0/10
2. [压缩即预测：一种基本等价关系](#item-2) ⭐️ 8.0/10
3. [Mojo 1.0 发布，但闭源编译器和 Python 兼容性问题仍存疑](#item-3) ⭐️ 8.0/10
4. [解耦下降：通过 AMP 实现精确的训练-测试误差跟踪](#item-4) ⭐️ 8.0/10
5. [Nvidia 发布 Nemotron 3.5 Lightning 和 NeMo Switchyard](#item-5) ⭐️ 7.0/10
6. [Go 的简洁性使其成为 AI 辅助开发的理想选择](#item-6) ⭐️ 7.0/10
7. [OpenAI Daybreak 模型现已在 AWS Bedrock 上可用](#item-7) ⭐️ 7.0/10
8. [自然语言文本不存在无损转换](#item-8) ⭐️ 7.0/10
9. [ChatGPT 广告扩展至五国，面向免费及 Go 用户](#item-9) ⭐️ 6.0/10
10. [字节跳动 CEO 拒绝将模型蒸馏作为 AI 战略捷径](#item-10) ⭐️ 6.0/10
11. [TVB 与 Gaw Capital 合资进军 AI 计算，股价大涨](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [研究人员从 LLM API 中窃取隐藏推理](https://stolen-thoughts.com/) ⭐️ 9.0/10

研究人员展示了一种方法，通过将痕迹重放到较弱的模型中，从专有 LLM API 中提取隐藏的思维链推理。该技术无需直接访问即可恢复更强模型的推理，详见 stolen-thoughts.com。 这引发了对模型对齐和知识产权的严重担忧，因为专有模型的内部推理可能被暴露。它可能影响 AI 安全政策和 API 提供商的竞争优势。 该攻击涉及将前沿模型的痕迹重放到较弱的兄弟模型中，并对其进行越狱以恢复推理。论文指出，API 摘要可能无法保留诸如模型在推导之前陈述答案等区别。

hackernews · quantumgarbage · 8月11日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49257876)

**背景**: 思维链（CoT）推理是一种技术，LLM 在回答前生成逐步推理，以提高复杂任务的性能。专有 API 通常加密或隐藏这些痕迹以保护知识产权和对齐。模型提取攻击通常利用可观察的输出训练学生模型，但此方法利用跨模型重放来访问隐藏推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2505.15634">[2505.15634] Feature Extraction and Steering for Enhanced ... Feature Extraction and Steering for Enhanced Chain-of-Thought ... Think Faster Than Words: Efficient LLM Chain-of-Thought ... Chain-of-Thought Prompting: Step-by-Step Reasoning with LLMs Chain of Thought Prompting Explained (with examples) Stealing Reasoning Traces from Proprietary LLM APIs Thinking to recall: How reasoning unlocks parametric ...</a></li>
<li><a href="https://ai-alert.org/posts/model-extraction-attacks-explained/">Model Extraction Attacks : How Adversaries Steal AI via the API</a></li>
<li><a href="https://arxiv.org/pdf/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>

</ul>
</details>

**社区讨论**: 评论者就“窃取”推理的伦理问题展开辩论，有人认为既然用户为 token 付费，这属于合理使用。其他人则指出了替代方法，例如使用“deep_think”工具绕过思考限制，并分享了类似提取技术的经验。

**标签**: `#LLM security`, `#chain-of-thought`, `#model extraction`, `#AI alignment`, `#proprietary APIs`

---

<a id="item-2"></a>
## [压缩即预测：一种基本等价关系](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

ngrok 博客发表了一篇文章，基于信息论和机器学习原理，论证压缩与预测在本质上是等价的。该文章在 Hacker News 上获得了大量关注，获得了 199 分和 92 条评论。 这一观点统一了两个重要领域，对理解大型语言模型为何有效具有深远意义，可能影响未来的人工智能研究和模型设计。它引起了社区的共鸣，引发了关于泛化能力和智能本质的讨论。 文章可能解释了通过算术编码，能够预测后验概率的系统可用于最优压缩，反之亦然。社区评论强调了细微差别，例如当测试分布与训练数据不同时压缩与预测的区别，并引用了相关资源，如 Grant Sanderson 的视频系列。

hackernews · nikolay · 8月11日 19:49 · [社区讨论](https://news.ycombinator.com/item?id=49263497)

**背景**: 在信息论中，压缩通过利用统计规律来减小数据大小，而预测则基于过去的数据估计未来的数据。这种等价性源于两者都依赖于对潜在概率分布的建模：更好的预测带来更好的压缩，反之亦然。这一概念对于理解现代机器学习至关重要，例如 LLM 等模型通过预测下一个 token 进行训练，实际上是在压缩训练数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Data_compression">Data compression - Wikipedia</a></li>
<li><a href="https://dev.to/trismegistus/compression-is-prediction-and-it-explains-why-llms-actually-work-209e">Compression Is Prediction — and It Explains Why LLMs Actually ...</a></li>
<li><a href="https://medium.com/@EleventhHourEnthusiast/compression-and-prediction-why-language-models-are-really-compression-engines-317c97babe04">Compression and Prediction. Why Language Models Are Really Compression Engines | by Eleventh Hour Enthusiast | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍认同核心观点，有人指出探讨同一主题的学术课程和视频。然而，ssivark 的一条重要评论认为，只有当数据分布完全代表所有未来问题时，压缩才在功能上等同于预测，强调了泛化的重要性。其他人幽默地指出 ngrok 博客的质量，还有一条评论将类比扩展到进化即压缩。

**标签**: `#compression`, `#prediction`, `#information theory`, `#machine learning`, `#AI`

---

<a id="item-3"></a>
## [Mojo 1.0 发布，但闭源编译器和 Python 兼容性问题仍存疑](https://www.modular.com/blog/modular-26-5-mojo-1-0-is-here) ⭐️ 8.0/10

Modular 宣布发布 Mojo 1.0，这标志着这个旨在用于高性能 AI 应用的 Python 超集语言的一个重要里程碑。该版本包括完全开源的标准库，并计划在 2026 年开源编译器和工具链。 Mojo 1.0 意义重大，因为它旨在将 Python 的易用性与 C 语言般的性能相结合，可能对 AI 和系统编程产生影响。然而，闭源编译器和对完全 Python 兼容性的不确定性可能影响其采用和社区信任。 Mojo 标准库已在 GitHub 上完全开源，但编译器在 2026 年之前仍保持闭源。路线图表明 Mojo 可能不会成为 Python 的完全超集，目前与 Python 的互操作性依赖于 CPython 运行时，以便从 Mojo 调用 Python。

hackernews · dayanruben · 8月11日 16:56 · [社区讨论](https://news.ycombinator.com/item?id=49261128)

**背景**: Mojo 是由 Modular Inc. 创建的编程语言，该公司由 Chris Lattner（Swift 和 LLVM 的创造者）和 Tim Davis 创立。它旨在弥合 Python 的易用性与 AI 应用所需性能之间的差距。该语言使用 Python 风格语法，并支持调用 Python 模块，但其与 Python 的完全兼容性仍在发展中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>
<li><a href="https://mojolang.org/docs/manual/python/">Python interoperability | Mojo - Modular</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了复杂的情绪：一些人质疑闭源编译器的价值，而另一些人则指出该语言缺乏清晰的目标概述。还有人担心编译器开源延迟以及 Python 超集目标可能被放弃。

**标签**: `#programming-languages`, `#mojo`, `#compiler`, `#python`, `#performance`

---

<a id="item-4"></a>
## [解耦下降：通过 AMP 实现精确的训练-测试误差跟踪](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

该论文提出了一种新颖的训练方法——解耦下降（DD），利用近似消息传递（AMP）的 Onsager 修正来确保神经网络中训练误差与测试误差的精确跟踪。在风格化的高斯混合模型上，该方法保证了训练误差在每次参数迭代时渐近等于测试误差。 这项工作解决了神经网络训练中泛化差距的根本问题，即训练误差可能降至零而测试误差停滞或恶化。通过提供训练-测试误差对齐的理论保证，它为最优停止和超参数调优开辟了新途径，有望提高模型的可靠性和效率。 该方法基于风格化高斯混合模型上的全批量梯度下降，其中数据重用偏差被认为是泛化差距的原因。该论文是理论性的，利用高维统计理论（特别是 AMP）推导出算法；未来计划发布一个 PyTorch 兼容的软件包。

reddit · r/MachineLearning · /u/mlovik1 · 8月11日 21:06

**背景**: 近似消息传递（AMP）是高维统计学中的一种迭代算法，利用 Onsager 修正来考虑自干扰，从而在线性逆问题中实现精确推断。在机器学习中，受 AMP 启发的技术已被用于构建具有更高精度和效率的深度网络。泛化差距是指训练性能与测试性能之间的差异，通常由对训练数据的过拟合引起。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.27883v1">Decoupled Descent : Exact Test Error Tracking Via Approximate...</a></li>
<li><a href="https://www.emergentmind.com/topics/onsager-correction-in-goamp">Onsager Correction in GOAMP - emergentmind.com</a></li>
<li><a href="https://arxiv.org/pdf/1612.01183">AMP-Inspired Deep Networks for Sparse Linear Inverse Problems</a></li>

</ul>
</details>

**社区讨论**: 作者积极寻求社区反馈和未来功能建议，表现出开放和协作的态度。讨论可能聚焦于理论贡献和潜在的实际应用，同时对扩展到大型模型的可扩展性存在一些怀疑。

**标签**: `#machine learning`, `#optimization`, `#approximate message passing`, `#generalization`, `#theory`

---

<a id="item-5"></a>
## [Nvidia 发布 Nemotron 3.5 Lightning 和 NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 7.0/10

Nvidia 发布了 Nemotron 3.5 Lightning 模型，这是一个拥有 30B 参数、3B 激活参数的混合专家（MoE）模型，以及 NeMo Switchyard，一个开源的模型路由库。这些工具旨在提升智能体 AI 工作流的效率和智能水平。 这一发布标志着向更小、更高效的智能体 AI 模型转变，可能降低成本和延迟，同时保持高性能。开源路由库可能使 AI 系统在多个提供商之间的部署更加灵活和经济高效。 Nemotron 3.5 Lightning 采用混合架构，交错使用 Mamba-2 和 MoE 层，并包含部分注意力层，提供 NVFP4 格式。NeMo Switchyard 是一个基于 Rust 的代理和库，可在多个提供商之间路由请求，转换 OpenAI 和 Anthropic API，并提供可组合的路由算法。

hackernews · droidjj · 8月11日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49263340)

**背景**: 智能体 AI 指能够自主完成任务、通常使用多个模型组成的集成系统的技术。模型路由是一种动态选择最适合每个请求或步骤的模型的技术，以平衡准确性、成本和延迟。Nvidia 的新产品旨在为构建常驻智能体的开发者简化这一过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4">nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4 · Hugging Face</a></li>
<li><a href="https://github.com/NVIDIA-NeMo/Switchyard">GitHub - NVIDIA-NeMo/Switchyard · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区评论凸显了关于向更小、更高效模型趋势的辩论，一些人认为这将推动结构性改进。其他人则提出了关于路由的实际问题，如提示缓存和会话一致性，并质疑基准比较中省略了 Qwen 模型。

**标签**: `#Nvidia`, `#LLM`, `#AI infrastructure`, `#model routing`, `#open source`

---

<a id="item-6"></a>
## [Go 的简洁性使其成为 AI 辅助开发的理想选择](https://developers.googleblog.com/why-go-is-an-ideal-language-for-ai-assisted-software-engineering/) ⭐️ 7.0/10

谷歌的博客文章认为，Go 的简洁性、强大的工具和清晰的约定使其特别适合 AI 辅助软件工程。该文章在 Hacker News 上引发了热烈讨论，获得了 218 个点赞和 270 条评论。 这一观点意义重大，因为 AI 辅助开发正在迅速改变软件工程，而编程语言的选择可能影响 AI 工具辅助开发者的效率。如果 Go 确实具有优势，它可能会影响语言采用趋势和工具投资。 文章强调 Go 的简单语法、内置并发、强大的标准库和强大的工具（如 gofmt、go vet）是减少 AI 模型歧义的因素。然而，批评者认为该论点存在偏见，因为它来自 Go 的创造者，并且有些人更喜欢 Rust 等语言，因为其严格的编译器可以在编译时捕获错误。

hackernews · 0xedb · 8月11日 16:57 · [社区讨论](https://news.ycombinator.com/item?id=49261133)

**背景**: Go 是一种静态类型、编译型编程语言，由 Robert Griesemer、Rob Pike 和 Ken Thompson 于 2007 年在谷歌设计。它以其简单性、效率和内置并发而闻名，广泛用于云和后端服务。AI 辅助软件工程涉及使用 AI 工具（如大型语言模型）来帮助开发者编写、审查和维护代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Go_(programming_language)">Go (programming language) - Wikipedia</a></li>
<li><a href="https://go.dev/">The Go Programming Language</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI-assisted_software_development">AI-assisted software development - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论显示出混合但实质性的观点。一些人同意，比如 Netflix Go 语言公会负责人报告 AI 生成的 Go 代码更好，而另一些人则批评该论点的偏见，并认为 Rust 的严格编译器更适合 AI 辅助。还有关于 Go 并发模型以及工具在提高代码信心方面的作用的辩论。

**标签**: `#Go`, `#AI-assisted development`, `#software engineering`, `#programming languages`

---

<a id="item-7"></a>
## [OpenAI Daybreak 模型现已在 AWS Bedrock 上可用](https://openai.com/index/daybreak-models-are-now-available-on-aws) ⭐️ 7.0/10

OpenAI 的 Daybreak 网络安全模型现已在 Amazon Bedrock 上可用，支持企业安全工作流。此次集成将 OpenAI 的前沿网络能力带给 AWS 客户。 此次合作使先进的 AI 驱动网络安全工具能够触达更广泛的企业用户，可能提升漏洞检测与响应能力。同时，它也增强了 OpenAI 在企业云市场的影响力，并凸显了 AI 驱动的安全解决方案日益增长的趋势。 Daybreak 模型通过 Amazon Bedrock 集成，使企业能够在现有安全和开发工作流中使用它们。这些模型旨在帮助防御者在攻击者利用漏洞之前发现、验证并修复漏洞。

rss · OpenAI Blog · 8月11日 10:00

**背景**: Amazon Bedrock 是一项托管服务，通过统一 API 提供来自多家提供商的基础模型。OpenAI 的 Daybreak 计划结合了前沿网络模型、Codex Security 和可信工作流，以协助安全团队。此次集成使企业无需管理底层基础设施即可利用这些能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://openai.com/index/daybreak-securing-the-world/">Daybreak: Tools for securing every organization in the world</a></li>
<li><a href="https://aws.amazon.com/bedrock/">Amazon Bedrock – Build genAI applications and agents at production...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AWS`, `#Cybersecurity`, `#AI`, `#Enterprise`

---

<a id="item-8"></a>
## [自然语言文本不存在无损转换](https://simonwillison.net/2026/Aug/11/there-are-no-lossless-transformations-of-natural-language-text/#atom-everything) ⭐️ 7.0/10

Sophie Alpert 发布了一项关于工程师使用 AI 写作的内部政策，指出自然语言文本不存在无损转换。该政策强调工程师必须对自己文档中的每一个观点和句子负责。 该政策为使用 LLM 的工程师提供了实用指导，促进了 AI 辅助写作中的责任感和清晰度。它可能影响团队采用 AI 工具的方式，鼓励他们避免盲目接受 AI 生成的文本，并确保文档准确反映作者的意图。 该政策指出，每一次重写或改写都会改变写作的含义，如果由不具备作者详细心智模型的实体完成，信息将会丢失。它还断言，用“哦，抱歉，那是 AI 写的，忽略它”来搪塞 AI 生成的句子是不可接受的。

rss · Simon Willison · 8月11日 23:48

**背景**: 大型语言模型（LLM）越来越多地被用于辅助写作，包括技术文档。然而，LLM 无法访问作者的私人想法和意图，因此它们进行的任何转换都可能引入微妙的含义变化。该政策解决了信息丢失的风险，并强调了在 AI 辅助写作中人工监督的重要性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sophiebits.com/2026/06/25/there-are-no-lossless-transformations-of-natural-language-text">There are no lossless transformations of natural-language text – Sophie Alpert</a></li>
<li><a href="https://news.ycombinator.com/item?id=48980425">There are no lossless transformations of natural - language text</a></li>

</ul>
</details>

**标签**: `#AI`, `#writing`, `#LLM`, `#engineering-practices`, `#documentation`

---

<a id="item-9"></a>
## [ChatGPT 广告扩展至五国，面向免费及 Go 用户](https://openai.com/index/testing-ads-in-chatgpt/) ⭐️ 6.0/10

8 月 11 日，OpenAI 宣布 ChatGPT 广告已在英国、墨西哥、巴西、日本和韩国上线，扩展了自 2 月在美国开始的广告测试。广告仅面向已登录的成年免费及 Go 档用户，Plus、Pro 等更高档位保持无广告。 这一扩展表明 OpenAI 越来越依赖广告来维持 ChatGPT 的免费访问，是其商业模式的重要转变。这可能为 AI 助手如何整合广告、同时平衡用户信任和隐私树立先例，影响全球数百万用户。 OpenAI 表示广告不会影响回答，并会明确标注为赞助内容。广告商只能看到曝光量、点击量等汇总数据，且广告不会展示给未成年用户，也不会出现在健康、政治等敏感话题附近。

telegram · OpenAI Blog · 8月12日 00:00

**背景**: ChatGPT Go 是 2026 年 1 月推出的低成本订阅档位，提供对 GPT-5.2 Instant 的扩展访问、更高的使用限制和更长的记忆。OpenAI 的广告政策强调品牌安全和用户信任，并设有防护措施防止在敏感情境中展示广告。公司于 2026 年 2 月更新了隐私政策，正式明确了广告的运作方式及广告商可访问的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/testing-ads-in-chatgpt/">Testing ads in ChatGPT - OpenAI</a></li>
<li><a href="https://openai.com/policies/ad-policies/">Ad policies - OpenAI</a></li>
<li><a href="https://help.openai.com/en/articles/11989085-what-is-chatgpt-go">What is ChatGPT Go? - OpenAI Help Center</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#advertising`, `#business model`, `#privacy`

---

<a id="item-10"></a>
## [字节跳动 CEO 拒绝将模型蒸馏作为 AI 战略捷径](https://news.google.com/rss/articles/CBMirgFBVV95cUxNUERWZDVySDZuLUJYR3VFTGk5a0RlODVYTUNDRTVSekZESVdTOFRUZHk2dGpqamNudzdsMC01V0NmeXJHZkZOY3lKaXlDX2JLUnNxTFpWdDRBVTJ5d3hyOFg1aUp4M1pmak9FRmJ0dGZvSUFkcm1IUGoyeE1SU0JVNG0ybVJNbHBZSzBfNGhFZDZYMHdXNWduX2FYakdUR18tM0NPYmRpOU1VZUtzY0E?oc=5) ⭐️ 6.0/10

字节跳动 CEO 张一鸣公开拒绝将模型蒸馏作为公司长期 AI 发展战略的捷径，强调可持续增长而非快速取胜。 这一立场表明字节跳动致力于从零开始构建自主 AI 能力，可能影响行业实践并为其他科技巨头树立先例。这也凸显了长期 AI 研究相对于短期优化的重要性日益增加。 模型蒸馏涉及训练一个较小的“学生”模型来模仿较大的“教师”模型，降低计算成本但可能限制创新。张一鸣的拒绝表明字节跳动将优先考虑原创研发，可能增加对基础 AI 技术的投资。

google_news · 一财全球Yicai Global · 8月11日 19:59

**背景**: 模型蒸馏是 AI 中常用的技术，将大型模型压缩为更小、更高效的模型，常用于在边缘设备上部署 AI。字节跳动以 TikTok 和抖音等应用闻名，一直在积极扩展其 AI 能力，据报道计划对 AI 基础设施进行大规模投资。该公司的战略似乎侧重于长期竞争力而非短期成本节约。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://www.openxcell.com/blog/model-distillation">Model Distillation — How It Works & Why It Matters</a></li>
<li><a href="https://intellibytes.substack.com/p/ai-distillation-explained-what-it">AI Distillation Explained: What It Is, How It Works, Legality ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#ByteDance`, `#model distillation`, `#industry strategy`

---

<a id="item-11"></a>
## [TVB 与 Gaw Capital 合资进军 AI 计算，股价大涨](https://news.google.com/rss/articles/CBMivgFBVV95cUxQR3lLdEkxUFVGOGx4ZGJfWlUwWUZid1lBMTVmVzZCV3hLWEZxaHpuQmxkWWdtQTVCclZWYWVZRjBjWVNjVGk0bDlJMXFtWkRKM3pRc2c3bFlIY2ttWHh2b1NZTHlqT2RobFhObUJid0JJaHFoVFE5dl84N0JpVktGRnE3aHB0bl8yakJiRXFJakc4ODdjMWpaSHp2bGExODlMWWZZWWkxUWowUDduZWo3MHRoRGEybUpSQi1TNm13?oc=5) ⭐️ 5.0/10

香港主要地面电视广播公司 TVB 宣布与 Gaw Capital 的关联公司成立合资企业，开展基于订阅的 AI 计算业务，股价随之大涨。该合资企业将开发 AI 计算设施，包括在 TVB 将军澳园区建设数据中心，并采购 GPU 和 CPU。 此举标志着 TVB 的重大多元化转型，其核心广播业务一直承压，也反映出传统媒体公司对 AI 基础设施市场日益浓厚的兴趣。这可能为 TVB 带来新的收入来源，并促进香港 AI 生态系统的发展。 合资企业计划在 TVB 位于将军澳工业园区的公司园区内建设数据中心，并已与一家“领先的全球科技集团”签署意向书，以大规模订阅 AI 计算服务。TVB 的广播收入在 2025 年同比下降 2%至 32 亿港元，但公司已恢复盈利。

google_news · 一财全球Yicai Global · 8月11日 13:12

**背景**: AI 计算涉及提供 GPU 和 CPU 等计算资源，以运行 AI 模型和应用。香港正积极发展 AI 生态系统，已有超过 300 家 AI 公司在此运营。TVB 作为传统广播公司，在广播收入下滑的背景下寻求新的增长领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yicaiglobal.com/news/tvb-jumps-after-hong-kong-broadcaster-targets-ai-computing-market-with-new-joint-venture">TVB Jumps After Hong Kong Broadcaster Targets AI Computing ...</a></li>
<li><a href="https://www.minichart.com.sg/2026/08/11/tvb-plans-ai-advanced-computing-joint-venture-with-gaw-capital-and-signs-loi-with-global-tech-group/">TVB Plans AI Advanced Computing Joint Venture With Gaw ...</a></li>
<li><a href="https://www.mingtiandi.com/real-estate/data-centres/gaw-expanding-links-with-hong-kongs-tvb-in-ai-computing-plan/">Gaw Expanding Links with Hong Kong's TVB in AI Computing Plan - Mingtiandi</a></li>

</ul>
</details>

**标签**: `#AI computing`, `#Hong Kong`, `#joint venture`, `#business news`

---