---
layout: default
title: "Horizon Summary: 2026-07-17 (EN)"
date: 2026-07-17
lang: en
---

> From 45 items, 12 important content pieces were selected

---

1. [Firefox Runs Inside Another Browser via WebAssembly](#item-1) ⭐️ 9.0/10
2. [EU Orders Google to Open Android and Search Data to Rivals](#item-2) ⭐️ 9.0/10
3. [Kimi releases 2.8T parameter K3 model with 1M context](#item-3) ⭐️ 9.0/10
4. [OnePlus halts new product launches in Europe and North America](#item-4) ⭐️ 8.0/10
5. [GPT-5.6 Codex Bug Can Delete Files in Full Access Mode](#item-5) ⭐️ 8.0/10
6. [Thinking Machines Lab Releases Inkling, a 975B Open-Weights Model](#item-6) ⭐️ 8.0/10
7. [Linus Torvalds Declares Linux Not Anti-AI](#item-7) ⭐️ 8.0/10
8. [QLoRA default learning rate 2e-4 is suboptimal for small datasets](#item-8) ⭐️ 8.0/10
9. [ExTernD: Ternary LLM Quantization with Arbitrary Accuracy](#item-9) ⭐️ 8.0/10
10. [Japan to Buy 27,500 Nvidia Rubin Chips for Robot AI](#item-10) ⭐️ 8.0/10
11. [China Approves Apple's AI Services for Mainland iPhones](#item-11) ⭐️ 8.0/10
12. [DeepMind and Isomorphic Labs Unveil Bioresilience AI Strategy](#item-12) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Firefox Runs Inside Another Browser via WebAssembly](https://simonwillison.net/2026/Jul/16/firefox-in-webassembly/#atom-everything) ⭐️ 9.0/10

Puter has compiled the full Firefox browser to WebAssembly, enabling it to run inside another browser like Chrome. The project uses AI-assisted development with Claude Opus and Fable, costing an estimated $25,000 in tokens. This is a groundbreaking milestone for WebAssembly, proving that a full, complex browser engine can be ported to run within another browser. It opens up possibilities for sandboxed browsing, legacy browser testing, and new web application architectures. The demo uses the Wisp protocol to proxy all network traffic through Puter's server because WebAssembly code cannot open arbitrary network connections. The project chose Firefox/Gecko for its strong single-process support, and the resulting WebAssembly binary is 233MB.

rss · Simon Willison · Jul 16, 23:34

**Background**: WebAssembly (Wasm) is a low-level binary instruction format that runs in modern web browsers at near-native speed. Compiling a full browser like Firefox to Wasm is extremely challenging due to the complexity of browser internals and the need to handle network access, which is restricted in Wasm. The Wisp protocol allows multiplexing multiple TCP/UDP sockets over a single WebSocket connection, enabling the proxied network access required for this demo.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/MercuryWorkshop/wisp-protocol">GitHub - MercuryWorkshop/wisp-protocol: Wisp is a low-overhead, easy to ...</a></li>
<li><a href="https://github.com/HeyPuter/puter">GitHub - HeyPuter/puter: 🌐 The Internet Computer! Free, Open-Source, and Self-Hostable.</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gecko_(software)">Gecko (software) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion was highly engaged, with the Puter team noting they had to scale servers to handle traffic from the conversation. Users expressed amazement at the technical achievement and discussed the implications for browser sandboxing and legacy compatibility.

**Tags**: `#WebAssembly`, `#Firefox`, `#Browser`, `#AI-assisted development`, `#WebSocket`

---

<a id="item-2"></a>
## [EU Orders Google to Open Android and Search Data to Rivals](https://www.theverge.com/policy/966438/eu-google-android-ai-interoperability-search-data-dma) ⭐️ 9.0/10

The European Commission ruled on Thursday that Google must open certain Android system features and Google Search data to qualifying competitors under the Digital Markets Act, granting rival AI assistants like ChatGPT equal system permissions and data access as Gemini. This decision significantly reshapes competition in the Android ecosystem and AI assistant market, potentially allowing users to set third-party assistants like ChatGPT as deeply integrated system assistants, and forcing Google to share search data that was previously closed. Google can still assess applications for Android feature access based on privacy and security standards, but restrictions must comply with EU rules. The EU will limit how the shared data can be used to protect privacy and security.

telegram · zaihuapd · Jul 16, 13:19

**Background**: The Digital Markets Act (DMA) is an EU regulation that targets large digital platforms deemed 'gatekeepers' to ensure fair competition. It requires them to allow interoperability, data access, and prevent self-preferencing. Google's Android and Search are designated as core platform services under the DMA.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_Markets_Act">Digital Markets Act</a></li>

</ul>
</details>

**Tags**: `#EU regulation`, `#Android`, `#AI assistants`, `#data access`, `#Digital Markets Act`

---

<a id="item-3"></a>
## [Kimi releases 2.8T parameter K3 model with 1M context](https://platform.kimi.com/docs/guide/kimi-k3-quickstart) ⭐️ 9.0/10

Kimi has released K3, an open-source model with 2.8 trillion parameters and a 1 million token context window, claiming performance second only to Claude Fable 5 and GPT-5.6 Sol. The model uses a sparse Mixture of Experts architecture with 896 experts, activating 16 per token, and incorporates Kimi Delta Attention and Attention Residuals. This release marks a significant milestone for open-source AI, as K3 rivals top proprietary models while being fully open-weight. It demonstrates that Chinese AI labs can achieve frontier-level performance, potentially accelerating commoditization of AI intelligence. K3 achieves 2.5x better scaling efficiency than its predecessor K2, and its full weights will be released in the coming days. Pricing on the Kimi API is ¥2.0 per million tokens for cached input, ¥20.0 for uncached input, and ¥100.0 for output.

telegram · zaihuapd · Jul 16, 13:47

**Background**: Kimi Delta Attention is a linear attention mechanism that refines the gated delta rule with fine-grained gating, improving efficiency. Attention Residuals replace fixed residual connections with a learnable attention mechanism, allowing better information flow. Sparse Mixture of Experts (MoE) activates only a subset of expert networks per input, enabling large model capacity with lower computational cost.

<details><summary>References</summary>
<ul>
<li><a href="https://vizuara.substack.com/p/kimi-linear-an-expressive-efficient">Kimi-Linear : An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://arxiv.org/pdf/2510.26692">[PDF] Kimi Linear: An Expressive, Efficient Attention Architecture - arXiv</a></li>
<li><a href="https://arxiv.org/abs/2603.15031">[2603.15031] Attention Residuals</a></li>

</ul>
</details>

**Discussion**: Community members noted the high cost of using K3 via API, with one user reporting a 25-cent cost for a single rendering. Concerns were raised about Moonshot AI's data usage policy, which states they may train on API content unless enterprise arrangements are made. Some commenters see this as part of a trend toward commoditized AI intelligence driven by Chinese labs.

**Tags**: `#AI`, `#LLM`, `#open-source`, `#Kimi`, `#MoE`

---

<a id="item-4"></a>
## [OnePlus halts new product launches in Europe and North America](https://community.oneplus.com/thread/2170715118587871237) ⭐️ 8.0/10

OnePlus has decided to stop launching new products in Europe and North America, but existing devices will continue to receive software updates and security patches as originally committed. This marks a significant retreat from key markets for a once-popular brand, potentially affecting its global presence and user base, though existing users are reassured of continued support. The decision only affects new product rollouts, not full operations; OnePlus will still support existing devices backed by OPPO. The company's community post clarifies that operations are not completely halted.

hackernews · pilililo2 · Jul 16, 10:14 · [Discussion](https://news.ycombinator.com/item?id=48932539)

**Background**: OnePlus was originally known for offering high-spec, affordable smartphones with near-stock Android and an unlocked bootloader, gaining a loyal enthusiast following. In recent years, the brand has faced increased competition and internal changes, including the departure of co-founder Carl Pei and closer integration with OPPO.

**Discussion**: Community comments express mixed reactions: some correct the editorialized title, noting it's only new product launches that are halted, not full operations. Former employees share insider perspectives on company culture, while others lament OnePlus's decline from its hacker-friendly roots.

**Tags**: `#OnePlus`, `#smartphone`, `#business`, `#community`

---

<a id="item-5"></a>
## [GPT-5.6 Codex Bug Can Delete Files in Full Access Mode](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 8.0/10

Thibault Sottiaux reported that GPT-5.6 Codex has a bug where it can delete files when full access mode is enabled without sandboxing, due to a mistake in overriding the $HOME environment variable. This bug highlights significant safety risks in AI coding agents, as it can cause unintended file deletions, potentially leading to data loss for developers who rely on these tools without proper safeguards. The bug occurs when the model attempts to override $HOME to define a temporary directory but mistakenly deletes $HOME instead. It requires full access mode, no sandboxing, and auto review disabled.

rss · Simon Willison · Jul 16, 17:45

**Background**: Codex is an AI coding agent that can autonomously read, write, and execute code. Full access mode grants it unrestricted permissions, while sandboxing isolates its actions to prevent harm. The $HOME environment variable points to the user's home directory, and overriding it incorrectly can lead to catastrophic deletions.

<details><summary>References</summary>
<ul>
<li><a href="https://vladimirsiedykh.com/blog/codex-cli-approval-modes-2025">Codex CLI approval modes explained: auto vs read only vs... | Vladimir Siedykh</a></li>
<li><a href="https://smartscope.blog/en/generative-ai/chatgpt/codex-cli-approval-modes-no-approval/">Codex CLI Auto Approve: Dangerously Skip Permissions Equivalent (2026) - SmartScope</a></li>
<li><a href="https://amux.io/guides/ai-agent-sandboxing/">AI Agent Sandboxing in 2026: Docker, E2B, Firecracker... — amux</a></li>

</ul>
</details>

**Tags**: `#codex`, `#coding-agents`, `#generative-ai`, `#ai-safety`, `#bug`

---

<a id="item-6"></a>
## [Thinking Machines Lab Releases Inkling, a 975B Open-Weights Model](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 8.0/10

Thinking Machines Lab, led by Mira Murati, released Inkling, a 975B-parameter (41B active) Mixture-of-Experts multimodal model under the Apache-2.0 license, trained on 45 trillion tokens of text, images, audio, and video. Inkling strengthens the US open-weights ecosystem, offering a competitive alternative to Chinese open models and providing a strong base for fine-tuning via the Tinker platform, despite not being a frontier model. The model card and training data documentation are notably sparse, with vague descriptions of data sources. A smaller variant, Inkling-Small (276B total, 12B active), is promised but not yet released.

rss · Simon Willison · Jul 16, 15:35

**Background**: Mixture-of-Experts (MoE) models use multiple specialized sub-networks (experts) with a gating mechanism to activate only a subset per input, enabling large total parameters with lower computational cost. Open-weights models release trained parameters but not full training code or data, differing from open-source AI. Apache-2.0 is a permissive license allowing commercial use and modification.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://deasadiqbal.medium.com/understanding-open-weights-vs-open-source-models-988b50ce64d7">Understanding Open Weights vs. Open Source Models | by Asad Iqbal | Medium</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told – Open Source Initiative</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-weights`, `#multimodal`, `#Mixture-of-Experts`

---

<a id="item-7"></a>
## [Linus Torvalds Declares Linux Not Anti-AI](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linus Torvalds, the creator of Linux, stated on the Linux Media mailing list that Linux is not an anti-AI project, calling AI a clearly useful tool and telling dissenters to fork or leave. This authoritative endorsement from the top Linux maintainer signals a strong pro-AI stance for the entire Linux kernel community, potentially influencing open-source projects and developers who were hesitant about integrating AI tools. Torvalds acknowledged that AI's usefulness was questionable a year ago but is no longer in doubt today, though he noted other open questions like the economy of AI. The quote comes from a kernel mailing list discussion, not a formal press release.

rss · Simon Willison · Jul 16, 13:26

**Background**: Linus Torvalds is the creator and lead maintainer of the Linux kernel, one of the world's largest open-source projects. AI tools, especially large language models (LLMs), have been increasingly used in software development for code generation, bug detection, and documentation. Some open-source communities have resisted AI due to concerns about licensing, ethics, or quality.

**Tags**: `#Linux`, `#AI`, `#open source`, `#kernel development`, `#Linus Torvalds`

---

<a id="item-8"></a>
## [QLoRA default learning rate 2e-4 is suboptimal for small datasets](https://www.reddit.com/r/MachineLearning/comments/1uy1z8b/the_qlora_2e4_default_is_wrong_under_10k_samples/) ⭐️ 8.0/10

A Reddit user reports that the default learning rate of 2e-4 for QLoRA fine-tuning causes overfitting on datasets under 10k samples, and reducing it to 1e-4 significantly improves evaluation performance. This challenges a widely adopted hyperparameter default in the LLM fine-tuning community, potentially saving practitioners weeks of debugging and improving model quality for small-scale fine-tuning tasks. The user observed that with 2e-4, the model overfits within the first epoch and eval loss stagnates or climbs; switching to 1e-4 and increasing epochs from 3 to 5 produced the best results. The default 2e-4 originates from the Alpaca dataset (52k samples), which is much larger than typical custom datasets.

reddit · r/MachineLearning · /u/Pretty-Ad774 · Jul 16, 12:50

**Background**: QLoRA (Quantized Low-Rank Adaptation) is a parameter-efficient fine-tuning method that combines 4-bit quantization with LoRA to reduce memory usage for large language models. The learning rate is a critical hyperparameter that controls how much the model weights are updated during training. A rate that is too high can cause overfitting, especially on small datasets.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/QLoRA">QLoRA</a></li>
<li><a href="https://medium.com/@levxn/lora-and-qlora-effective-methods-to-fine-tune-your-llms-in-detail-6e56a2a13f3c">LoRA and QLoRA - Effective methods to Fine-tune your... | Medium</a></li>
<li><a href="https://www.techinterview.org/post/3233460056/fine-tuning-llms-vs-training-from-scratch-when-and-how/">Fine - tuning LLMs vs Training from Scratch: When and How...</a></li>

</ul>
</details>

**Discussion**: The Reddit post generated significant discussion, with many users sharing similar experiences and agreeing that the default learning rate should be tuned for small datasets. Some pointed out that the QLoRA paper itself recommends tuning, but tutorials often hardcode 2e-4 without caveats.

**Tags**: `#QLoRA`, `#fine-tuning`, `#hyperparameters`, `#LLM`, `#practical ML`

---

<a id="item-9"></a>
## [ExTernD: Ternary LLM Quantization with Arbitrary Accuracy](https://www.reddit.com/r/MachineLearning/comments/1uy2zb3/externd_expandedrank_ternary_decomposition/) ⭐️ 8.0/10

ExTernD proposes a novel post-training quantization method for large language models that decomposes a weight matrix into two ternary matrices and a diagonal scaling matrix, allowing the inner rank to be arbitrarily large to achieve accuracy approaching any quantization level. This approach overcomes the fixed matrix size limitation of ternary quantization, enabling high accuracy with only a modest increase in VRAM, which could make ternary quantization more practical for deploying LLMs on resource-constrained hardware. The method uses two ternary matrices (values in {-1,0,1}) and a diagonal scaling matrix, where the inner rank can be increased to reduce quantization error. The author claims the VRAM overhead is only slightly higher than current quantization methods, justified by the benefits of ternary arithmetic.

reddit · r/MachineLearning · /u/LMTLS5 · Jul 16, 13:31

**Background**: Post-training quantization (PTQ) reduces model size and speeds up inference by converting weights to lower precision without retraining. Ternary quantization restricts weights to three values (-1, 0, 1), offering extreme compression but often suffering from accuracy loss due to limited expressiveness. ExTernD addresses this by expanding the effective rank through matrix decomposition.

<details><summary>References</summary>
<ul>
<li><a href="https://apxml.com/courses/practical-llm-quantization/chapter-2-post-training-quantization-ptq">Post - Training Quantization (PTQ) for LLMs</a></li>
<li><a href="https://medium.com/data-science-at-microsoft/exploring-quantization-in-large-language-models-llms-concepts-and-techniques-4e513ebf50ee">Exploring quantization in Large Language Models... | Medium</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#quantization`, `#ternary`, `#PTQ`, `#efficiency`

---

<a id="item-10"></a>
## [Japan to Buy 27,500 Nvidia Rubin Chips for Robot AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 8.0/10

Japan plans to purchase 27,500 Nvidia Rubin chips to build a sovereign AI for robotics, led by the newly formed company Noetra with $2.4 billion in government funding. This initiative aims to reduce Japan's dependency on US and Chinese AI technologies, positioning Japan as a third option in global AI development and targeting over 30% of the global robotics market by 2040. Noetra, backed by SoftBank, Toyota-backed Preferred Networks, NEC, and others, plans to release its first AI model by March 2027 and a robot-specific version within a few years.

telegram · zaihuapd · Jul 16, 10:59

**Background**: Nvidia's Rubin is the next-generation AI chip architecture succeeding Blackwell, offering significant leaps in computational power. Sovereign AI refers to a nation's ability to develop and control its own AI infrastructure and models, reducing reliance on foreign providers. Japan's robotics industry is already advanced, but this project aims to integrate cutting-edge AI to maintain competitiveness.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2025/03/18/nvidia-announces-blackwell-ultra-and-vera-rubin-ai-chips-.html">cnbc.com/2025/03/18/ nvidia -announces-blackwell-ultra-and-vera...</a></li>
<li><a href="https://robotsbeat.com/japan-nvidia-noetra-physical-ai-factory-frontia-rubin-gpus/">Japan and NVIDIA Launch World's First National... | RobotsBeat</a></li>
<li><a href="https://www.techradar.com/pro/japan-reveals-new-noetra-plan-to-flood-the-country-with-10-million-robots-by-2040-including-work-in-the-nursing-food-and-drink-sectors">Japan 's robot invasion begins as 10 million machines... | TechRadar</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Robotics`, `#Nvidia`, `#Japan`, `#Sovereign AI`

---

<a id="item-11"></a>
## [China Approves Apple's AI Services for Mainland iPhones](https://news.google.com/rss/articles/CBMikAFBVV95cUxOSWloemk5YUJsQWZ2VkZRVklOc2g0aENfaDRabGpxUjhJSnV6WWdIOWFIaHFNTFNmcV8zanAzT3J5TUJlR1RfaThYakVxSm1RaURMV3lOLW1PWm1TRHpKLUdCVEVjYnFUN2gxclBWZTlDdGpfUk43YjFMMVducUVXTE43UEtUakpqbmZaTlpHVkE?oc=5) ⭐️ 8.0/10

China's Cyberspace Administration has approved Apple's Apple Intelligence AI service for use on iPhones sold in mainland China, marking a key regulatory milestone. This approval allows Apple to deploy generative AI features in China, its third-largest market, after a prolonged delay, and highlights the need for global tech firms to partner with local AI providers to comply with Chinese regulations. The approved service is powered by Alibaba's Qwen AI and Baidu, not ChatGPT, and Apple first submitted some features for review in early 2025 after nearly a year of co-development with local partners.

google_news · 一财全球Yicai Global · Jul 16, 03:31

**Background**: China requires companies to obtain government approval before releasing most generative AI services to the public. Apple Intelligence is Apple's suite of AI features, including text generation and image editing, which had been available in other regions but was delayed in China due to regulatory hurdles.

<details><summary>References</summary>
<ul>
<li><a href="https://www.thenews.com.pk/latest/1409220-apple-intelligence-approved-in-china-with-alibabas-qwen-baidu-ai-integration">Apple Intelligence approved in China with Alibaba’s Qwen, Baidu AI...</a></li>
<li><a href="https://vncmac.com/en/blog/apple-intelligence-china-approved-qwen-baidu-2026.html">Apple Intelligence China Approved | Qwen + Baidu | VNCMac</a></li>
<li><a href="https://www.marketscreener.com/news/apple-s-ai-tools-get-china-approval-ce7f5ed2d988f720">Apple 's AI Tools Get China Approval | MarketScreener</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#AI`, `#China`, `#regulation`, `#iPhone`

---

<a id="item-12"></a>
## [DeepMind and Isomorphic Labs Unveil Bioresilience AI Strategy](https://deepmind.google/blog/our-approach-to-bioresilience/) ⭐️ 7.0/10

Google DeepMind and Isomorphic Labs have announced their joint approach to using AI models to enhance bioresilience, the ability of biological systems to adapt to change. This marks a strategic expansion of AI into biosecurity and healthcare, potentially enabling faster responses to biological threats and advancing drug discovery. The approach leverages DeepMind's AlphaFold technology, which predicts protein structures, to identify new pathways for drug delivery and improve biological resilience.

rss · Google DeepMind Blog · Jul 16, 09:30

**Background**: Bioresilience refers to the ability of a species or individual to adapt to environmental changes. Isomorphic Labs, a spin-off from DeepMind, focuses on AI-driven drug discovery. This announcement combines their expertise to address biological challenges.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bioresilience">Bioresilience - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Isomorphic_Labs">Isomorphic Labs</a></li>

</ul>
</details>

**Tags**: `#AI`, `#bioresilience`, `#DeepMind`, `#biology`, `#healthcare`

---