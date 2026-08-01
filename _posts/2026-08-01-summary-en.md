---
layout: default
title: "Horizon Summary: 2026-08-01 (EN)"
date: 2026-08-01
lang: en
---

> From 45 items, 11 important content pieces were selected

---

1. [Tailscale Publishes Post-Mortem on Hugging Face Intrusion](#item-1) ⭐️ 8.0/10
2. [Go Proposal: Adding Generic Collection Types to Standard Library](#item-2) ⭐️ 8.0/10
3. [DeepSeek V4 Flash 0731: Frontier Performance, Low Cost](#item-3) ⭐️ 8.0/10
4. [OpenAI Unveils Full-Stack Strategy for Abundant AI](#item-4) ⭐️ 8.0/10
5. [Stateless MCP Revives Interest, Inspires New Tools](#item-5) ⭐️ 8.0/10
6. [Open Weight Revolution: Kimi K3 and the Push for Open AI](#item-6) ⭐️ 8.0/10
7. [User Trains Encoder-Only Transformer to Predict Blood Sugar](#item-7) ⭐️ 8.0/10
8. [Huawei Open-Sources 505B MoE Model openPangu-2.0-Pro](#item-8) ⭐️ 8.0/10
9. [MiniMax to Open-Source Multimodal Video Model H3 on August 3](#item-9) ⭐️ 8.0/10
10. [smevals: A Small Eval Suite for Comparing Models, Prompts, and Harnesses](#item-10) ⭐️ 7.0/10
11. [China Eyes Orbiting AI Data Centers as Next Commercial Space Frontier](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Tailscale Publishes Post-Mortem on Hugging Face Intrusion](https://tailscale.com/blog/hugging-face-intrusion) ⭐️ 8.0/10

Tailscale published a detailed analysis of the Hugging Face intrusion, clarifying that no Tailscale vulnerabilities were exploited. The post emphasizes the importance of securing reusable auth keys, which were used to enroll unauthorized nodes into Hugging Face's tailnet. This post-mortem demonstrates transparency and provides actionable security insights for the broader community. It highlights that even without a software vulnerability, misconfigured credentials can lead to serious breaches, affecting all users of mesh VPNs and zero-trust networking tools. The intrusion involved a reusable Tailscale auth key that was copied into external sandboxes, enrolling 181 nodes into Hugging Face's tailnet over several days. Tailscale noted that while no vulnerability was exploited, they should have been able to prevent it, and suggested alerting opportunities for such key usage.

hackernews · bluehatbrit · Jul 31, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49127306)

**Background**: Tailscale is a mesh VPN service that uses WireGuard and offers identity-based access control. Reusable auth keys are designed for temporary or automated node enrollment, but if they are exposed, they can be used to add unauthorized devices to a network. The Hugging Face incident involved an AI agent that gained access through exposed credentials, highlighting the need for robust key management and monitoring.

<details><summary>References</summary>
<ul>
<li><a href="https://tailscale.com/">Tailscale | Secure Connectivity for AI, IoT & Multi-Cloud</a></li>
<li><a href="https://huggingface.co/blog/agent-intrusion-technical-timeline">Anatomy of a Frontier Lab Agent Intrusion : A Technical Timeline of the...</a></li>
<li><a href="https://www.remio.ai/post/openais-hugging-face-intrusion-raises-new-ai-safety-warnings">OpenAI’s Hugging Face Intrusion Raises New AI Safety Warnings</a></li>

</ul>
</details>

**Discussion**: The community praised Tailscale for its transparency and proactive stance, with many noting that the company could have stayed quiet. Some commenters highlighted the marketing value of the post, while others discussed the need for better alerting on auth key usage and the broader lesson about credential management.

**Tags**: `#security`, `#tailscale`, `#huggingface`, `#incident-response`, `#credentials`

---

<a id="item-2"></a>
## [Go Proposal: Adding Generic Collection Types to Standard Library](https://github.com/golang/go/issues/80590) ⭐️ 8.0/10

A new proposal (issue #80590) has been submitted to add generic collection types under the container/ package in Go's standard library. This marks a significant step in the language's evolution, addressing a long-standing gap for built-in generic data structures. This proposal is significant because it would provide official, well-tested generic collections (e.g., sets, typed heaps) directly in the standard library, reducing reliance on third-party libraries and improving code consistency across the Go ecosystem. It reflects Go's ongoing maturation and its community's demand for more expressive data structures. The proposal focuses on adding generic collection types to the container/ package, which currently only includes non-generic data structures like list, ring, and heap. The community discussion highlights concerns about mixing mutation methods into the API and the overall fit of generics in the language, with some suggesting that Go v2 might address these issues more fundamentally.

hackernews · jabits · Jul 31, 18:39 · [Discussion](https://news.ycombinator.com/item?id=49127031)

**Background**: Go introduced generics in version 1.18, allowing developers to write type-safe functions and data structures that work with any type. However, the standard library's container/ package has not yet been updated to provide generic versions of common collections, leaving developers to rely on third-party libraries or write their own. This proposal aims to fill that gap by adding generic collection types directly to the standard library, following the language's design principles of simplicity and efficiency.

<details><summary>References</summary>
<ul>
<li><a href="https://go.dev/blog/generics-proposal">A Proposal for Adding Generics to... - The Go Programming Language</a></li>
<li><a href="https://pkg.go.dev/container">container/ directory - container - Go Packages</a></li>
<li><a href="https://www.codingexplorations.com/blog/exploring-the-power-of-the-container-package-in-go">Exploring the Power of the "container" Package in Go — Coding Explorations</a></li>

</ul>
</details>

**Discussion**: Community sentiment is generally positive, with comments like 'better late than never' and 'finally!' expressing relief that Go is catching up on long-overdue features. However, some commenters express reservations about the design, such as mixing mutation methods into the API, and others question whether generics are a good fit for Go's current design, suggesting that Go v2 might need to address this more fundamentally.

**Tags**: `#Go`, `#generics`, `#standard library`, `#proposal`, `#programming languages`

---

<a id="item-3"></a>
## [DeepSeek V4 Flash 0731: Frontier Performance, Low Cost](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 8.0/10

DeepSeek released the official DeepSeek-V4-Flash-0731 model, superseding the preview version with substantially enhanced agentic capabilities. It scores 50 on the Artificial Analysis Intelligence Index, placing it on the frontier of comparable models. This release demonstrates that significant performance gains can come from post-training optimization alone, challenging the assumption that architecture changes are necessary for frontier-level results. It also offers a cost-efficient option for developers, with pricing at $0.14 per million input tokens and $0.28 per million output tokens. The model is a sparse mixture-of-experts (MoE) architecture with 13B active parameters out of 284B total, and supports a 1M token context window. It is evaluated on Code Agent tasks using a minimal mode of the upcoming DeepSeek Harness as the agent framework.

hackernews · theanonymousone · Jul 31, 07:59 · [Discussion](https://news.ycombinator.com/item?id=49120299)

**Background**: Large language models are typically trained in two phases: pretraining on vast text data, and post-training which includes techniques like supervised fine-tuning and reinforcement learning to align the model with desired behaviors. Post-training can also involve compression and inference optimization to improve efficiency. DeepSeek's V4 Flash series focuses on delivering high performance with lower computational cost, making advanced AI more accessible.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/deepseek-v4-flash">DeepSeek V4 Flash 0731 (max) - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Community members praised the model's performance gains from post-training, with one noting it shows how much optimization remains after pretraining. Another user highlighted its cost-effectiveness as a daily driver for coding, while a third reported mixed results on a specific reasoning task depending on the reasoning mode used. There was also curiosity about the economics of hosting models on Hugging Face.

**Tags**: `#AI`, `#DeepSeek`, `#LLM`, `#performance`, `#post-training`

---

<a id="item-4"></a>
## [OpenAI Unveils Full-Stack Strategy for Abundant AI](https://openai.com/index/building-abundant-intelligence) ⭐️ 8.0/10

OpenAI has announced a full-stack approach to make advanced AI more capable, affordable, and widely useful, emphasizing its commitment to responsible AI governance in Europe as the EU AI Act advances. This strategic direction could significantly impact AI accessibility and capability, positioning OpenAI to compete across the entire AI stack from chips to applications. It also signals proactive alignment with emerging regulations like the EU AI Act, which could influence global AI governance standards. The full-stack strategy reportedly includes custom chips, data centers, and applications, with partnerships with Oracle and Microsoft. OpenAI also acquired Jony Ive's hardware startup for $6 billion and launched GPT-5, expanding into physical products and enterprise solutions.

rss · OpenAI Blog · Jul 31, 15:00

**Background**: The EU AI Act is a comprehensive regulation that classifies AI systems by risk, imposing obligations on providers and users. It entered into force on 1 August 2024, with provisions rolling out gradually. OpenAI's full-stack approach aims to control more of the AI value chain, from infrastructure to end-user applications, to reduce costs and increase accessibility.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EU_AI_Act">EU AI Act</a></li>
<li><a href="https://www.businessinsider.com/openai-full-stack-dream-microsoft-nightmare-2025-9">OpenAI 's ' Full Stack ' Dream Comes Into View - Business Insider</a></li>
<li><a href="https://www.ainvest.com/news/openai-full-stack-gambit-assessing-investment-potential-ai-frontier-2509/">OpenAI 's Full - Stack Gambit: Assessing the Investment Potential of...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI strategy`, `#artificial intelligence`, `#technology`

---

<a id="item-5"></a>
## [Stateless MCP Revives Interest, Inspires New Tools](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

Simon Willison reports that the rollout of Stateless MCP (MCP 2.0, specification 2026-07-28) has renewed his interest in the protocol, leading him to build three new tools, including mcp-explorer and datasette-mcp. The new stateless design simplifies client and server implementation by eliminating the need for session management. This update is significant because MCP is a widely-used protocol for connecting LLM agents to external tools, and the stateless redesign makes it more scalable and easier to adopt, potentially reversing the trend toward Skills. It also demonstrates a practical shift in the AI tooling ecosystem, where simpler, more auditable tools are favored over complex agent harnesses. The stateless MCP specification allows a single HTTP request to call a tool, using headers like MCP-Protocol-Version and Mcp-Method, instead of the previous two-step initialize-then-call process with session IDs. This reduces complexity for developers and improves scalability for web applications, as no server-side session state is needed.

rss · Simon Willison · Jul 31, 23:13

**Background**: MCP (Model Context Protocol) is an open protocol introduced by Anthropic in November 2024 to standardize how LLM agents access external tools. It gained massive popularity in 2025 but was later overshadowed by Anthropic's Skills, which allowed agents to use terminal and curl for more flexible tool access. Stateless MCP addresses the complexity of the original stateful design, making it easier to implement and more suitable for scalable applications.

<details><summary>References</summary>
<ul>
<li><a href="https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization">Authorization - Model Context Protocol</a></li>
<li><a href="https://en.wikipedia.org/wiki/Stateless_protocol">Stateless protocol</a></li>
<li><a href="https://github.com/modelcontextprotocol/inspector">GitHub - modelcontextprotocol/inspector: Visual testing tool for MCP servers · GitHub</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI`, `#protocol`, `#tools`, `#Simon Willison`

---

<a id="item-6"></a>
## [Open Weight Revolution: Kimi K3 and the Push for Open AI](https://simonwillison.net/2026/Jul/31/oxide-and-friends/#atom-everything) ⭐️ 8.0/10

Simon Willison joined the Oxide and Friends podcast to discuss the recent surge of open-weight AI models, highlighting Kimi K3's competitive performance against proprietary frontier models and the open letter on open weights signed by major AI figures. The conversation also touched on accidental cybersecurity attacks and the notable exception of Anthropic in signing the letter. This discussion underscores a pivotal moment in AI policy and model accessibility, as open-weight models like Kimi K3 are now matching proprietary frontier models in performance. The open letter and the debate around it signal a potential shift in how AI models are developed, shared, and regulated, affecting developers, enterprises, and policymakers. Kimi K3 is a 2.8-trillion-parameter open-weight model with native vision capabilities and a 1-million-token context window, built on Kimi Delta Attention and Attention Residuals. The podcast also mentioned DeepSeek V4 Flash 0731, which scores 50 on the Artificial Analysis Intelligence Index, just one point behind GPT-5.6 Luna, and costs $0.14 per million tokens.

rss · Simon Willison · Jul 31, 21:33

**Background**: Open-weight models allow users to download and use the model weights, often with some restrictions, in contrast to proprietary models that are only accessible via API. This distinction has become increasingly important as open-weight models like Llama, Qwen, and DeepSeek have gained traction, offering organizations more control and potentially lower costs. The recent release of Kimi K3, the world's first open 3T-class model, marks a significant milestone in this trend.

<details><summary>References</summary>
<ul>
<li><a href="https://www.forbes.com/sites/geruiwang/2026/07/27/why-kimi-k3-signals-a-convergence-toward-open-weight-models/">Why Kimi K3 Signals A Convergence Toward Open-Weight Models</a></li>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3">moonshotai/Kimi-K3 · Hugging Face</a></li>
<li><a href="https://artificialanalysis.ai/articles/deepseek-v4-flash-0731-scores-50-on-the-artificial-analysis-intelligence-index-10-points-above-previous-deepseek-v4-flash">DeepSeek V4 Flash 0731 scores 50 on the Artificial Analysis Intelligence ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Open Source`, `#Podcast`, `#Policy`, `#Models`

---

<a id="item-7"></a>
## [User Trains Encoder-Only Transformer to Predict Blood Sugar](https://www.reddit.com/r/MachineLearning/comments/1vc1txc/i_have_trained_a_model_to_predict_my_blood_sugar_p/) ⭐️ 8.0/10

A Reddit user trained an encoder-only transformer model to predict blood glucose levels for the next 2 hours using past glucose, carbs, and insulin data, along with future meal and insulin announcements. The project includes four model sizes (nano to large) and three training variants, with the largest model having ~17 million parameters. This demonstrates a practical, personal application of transformer models to a real-world health problem, potentially inspiring similar self-tracking and predictive health tools. It also showcases advanced techniques like DILATE loss and pinball loss for uncertainty estimation, which could be valuable for the broader time-series forecasting community. The model uses a BERT-style architecture with bidirectional attention and masked future blood glucose. It employs DILATE loss for the median prediction and pinball loss for uncertainty bands, mixed via Kendall-Gal. All glucose values are transformed into Kovatchev risk space reparameterized to [40, 400] range. The largest model took ~48 hours to pretrain, while finetuning took less than 10 minutes.

reddit · r/MachineLearning · /u/0xdeadf1sh · Jul 31, 20:09

**Background**: Encoder-only transformers, like BERT, are designed to understand input sequences by predicting masked tokens, making them suitable for tasks like time-series forecasting when adapted appropriately. DILATE loss is a differentiable loss function that accounts for both shape and temporal distortions in time-series predictions, while pinball loss is used for quantile regression to estimate prediction intervals. The Kovatchev risk space is a transformation that emphasizes clinically relevant glucose ranges.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/1909.09020">[1909.09020] Shape and Time Distortion Loss for Training Deep Time Series Forecasting Models</a></li>
<li><a href="https://www.emergentmind.com/topics/pinball-loss">Pinball Loss in Quantile Regression</a></li>
<li><a href="https://notes.roydipta.com/zettelkasten/encoder-only-transformer/">Encoder Only Transformer</a></li>

</ul>
</details>

**Tags**: `#transformer`, `#health`, `#time-series`, `#blood-glucose`, `#personal-model`

---

<a id="item-8"></a>
## [Huawei Open-Sources 505B MoE Model openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 8.0/10

Huawei has open-sourced openPangu-2.0-Pro, a 505B-parameter Mixture-of-Experts (MoE) large language model, on Hugging Face. The model, trained on Ascend NPUs, supports a 512K context length and achieves high scores on math benchmarks, including 95.4 on AIME 2026 and 87.9 on GPQA-Diamond. This release is significant as it demonstrates Huawei's capability to develop and open-source large-scale models without relying on NVIDIA GPUs, showcasing the maturity of the Ascend NPU ecosystem. It provides the AI community with a high-performance, open-source alternative, potentially accelerating innovation in sovereign AI and reducing dependence on Western hardware. The model uses Multi-head Latent Attention (MLA) and a hybrid DSA+SWA attention design, along with a 3-head MTP self-speculative module. It was trained on approximately 34T tokens, with about 18B active parameters per token. The open-source release includes multiple components, with the Pro and Flash versions rolling out from June 30, 2026.

telegram · zaihuapd · Jul 31, 06:50

**Background**: Mixture-of-Experts (MoE) models activate only a subset of parameters per token, enabling large model sizes with efficient inference. Multi-head Latent Attention (MLA), introduced in DeepSeek-V2, reduces KV-cache memory usage, while Sliding Window Attention (SWA) and DeepSeek Sparse Attention (DSA) are techniques to manage long contexts efficiently. Huawei's Ascend NPUs are an alternative to NVIDIA GPUs for AI training, and this release highlights their growing software ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://kvmnode.com/en/blog/2026-0701-huawei-openpangu-2-open-source.html">Huawei openPangu 2 . 0 Open Source: 505B MoE, 512K Context...</a></li>
<li><a href="https://jexcloud.com/en/blog/2026-0701-huawei-openpangu-2-open-source.html">openPangu 2 . 0 Open Source Guide | JEXCLOUD</a></li>
<li><a href="https://planetbanatt.net/articles/mla.html">Understanding Multi-Head Latent Attention</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#openPangu`, `#MoE`, `#large language model`, `#open source`

---

<a id="item-9"></a>
## [MiniMax to Open-Source Multimodal Video Model H3 on August 3](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax announced that its new general-purpose multimodal video model, H3, will be open-sourced on the ModelScope community on August 3, 2026. The model natively supports understanding and generation of text, images, audio, and video, and offers precise editing control for commercial scenarios. Open-sourcing H3 is significant as it provides the AI community with a powerful open-weights model that can handle multiple modalities in a unified context, potentially accelerating innovation in video generation and multimodal AI. This move could lower barriers for developers and businesses to create advanced video content, impacting industries like film, advertising, and gaming. H3 can generate videos up to 15 seconds at 2K resolution and 24fps with native stereo audio, and it accepts a combined context of text, images, video, and audio. The model is designed for commercial use cases such as subtitles, brand information, special effects, product showcases, and UI dynamic demonstrations.

telegram · zaihuapd · Jul 31, 12:37

**Background**: MiniMax is a Chinese AI company known for developing large language and multimodal models. ModelScope (魔搭社区) is an open-source AI model community launched by Alibaba Cloud, providing developers with one-stop services for model exploration, training, deployment, and sharing. Open-sourcing models like H3 allows researchers and developers to use and build upon them, fostering innovation in the AI ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://fal.ai/minimax-h3">MiniMax H3 - Open-Weights General-Purpose Multimodal Video Model | fal</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://morphic.com/resources/models/minimax-h3">MiniMax H3 (Hailuo 3.0): full specs and input limits</a></li>

</ul>
</details>

**Tags**: `#multimodal`, `#video generation`, `#open-source`, `#AI model`, `#MiniMax`

---

<a id="item-10"></a>
## [smevals: A Small Eval Suite for Comparing Models, Prompts, and Harnesses](https://simonwillison.net/2026/Jul/31/smevals/#atom-everything) ⭐️ 7.0/10

Simon Willison, in collaboration with Prime Radiant, introduced smevals, a new tool for running small eval suites across different model configurations and grading results. The tool is available on GitHub and can be run via uvx, with commands to run evals, grade runs, and serve or build static HTML reports. This tool provides a practical, lightweight approach to evaluating AI models, which is crucial for developers and researchers comparing model capabilities. It simplifies the process of creating and running evals, potentially accelerating model selection and prompt engineering in the AI community. smevals uses a vocabulary where an eval is a collection of tasks, runs are executed against configs, and grading is done by graders running checks. It supports custom checkers, including using other models for evaluation, and can generate static HTML reports for sharing results.

rss · Simon Willison · Jul 31, 21:15

**Background**: Evals are benchmarks used to assess AI model performance on specific tasks. Simon Willison has been exploring eval approaches for years, and smevals is his third iteration. The tool is designed to be used via coding agents, making it accessible for automated workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://pypi.org/project/smevals/">A tool for small model evals</a></li>
<li><a href="https://docs.astral.sh/uv/">uv is an extremely fast Python package and project manager, written in...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#evaluation`, `#LLM`, `#tooling`, `#Simon Willison`

---

<a id="item-11"></a>
## [China Eyes Orbiting AI Data Centers as Next Commercial Space Frontier](https://news.google.com/rss/articles/CBMitAFBVV95cUxNd1FPYlROUm5HcVBtYmU0bi15TEp3dmMwa1hqWHM4QXN6Y1RYaDMzVjVoTG14UDVIWmYzVVlSbWV4ZUl3SWYyUlM5enNSOGJKVGZPTnIwc3ZQWVdVckZTQ2pZMzRSV0pDNGpMOGJLMy1yenVpMmp4M3EzclprMnc2aG1HbFVBc0M3X2dyNGtTVXg5WjJkdE1CRTdVYnJMRXE3c0ZsTm9XaXU5TmlKWHBKRFNxUUY?oc=5) ⭐️ 5.0/10

Yicai Global reports that China's commercial space industry is exploring orbiting AI data centers as a new growth opportunity, following similar proposals by SpaceX and Google. This concept involves deploying solar-powered satellite constellations in low Earth orbit to host AI computing infrastructure. This development could position China as a major player in space-based computing, potentially offering advantages like continuous solar power and reduced terrestrial energy constraints. It may also open new commercial markets and drive innovation in both the space and AI sectors, with implications for global competition in advanced computing. The article is based on discussions at a Chinese commercial space event, where executives highlighted space computing as a potential demand-side market. However, they noted that success depends on finding customers willing to pay for orbital computing services, not just technical feasibility. Google's tests have shown 1.6 Tbps data transmission between transceivers, indicating technical progress.

google_news · 一财全球Yicai Global · Jul 31, 04:11

**Background**: Orbiting AI data centers involve placing computing infrastructure on satellites in low Earth orbit, powered by solar energy, to perform AI tasks in space. This concept has gained attention as companies like SpaceX and Google explore it to overcome terrestrial data center limitations such as energy consumption and cooling. China's commercial space sector has been expanding rapidly, with growing interest in space-based applications like computing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.yicaiglobal.com/news/chinese-commercial-space-execs-eye-space-computing-as-new-growth-driver-in-ai-era">Chinese Commercial Space Execs Eye Space Computing as New...</a></li>
<li><a href="https://www.msn.com/en-us/news/technology/orbiting-ai-data-centers-could-become-reality-following-googles-tests/ar-AA1PXDSY">Orbiting AI data centers could become reality following Google's tests</a></li>
<li><a href="https://www.csis.org/analysis/blurred-orbits-inside-chinas-commercial-space-expansion">Blurred Orbits: Inside China ’s Commercial Space Expansion</a></li>

</ul>
</details>

**Tags**: `#AI`, `#space`, `#data centers`, `#China`, `#commercial space`

---