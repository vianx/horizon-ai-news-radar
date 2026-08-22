---
layout: default
title: "Horizon Summary: 2026-08-22 (EN)"
date: 2026-08-22
lang: en
---

> From 30 items, 9 important content pieces were selected

---

1. [SGLang v0.5.18: Major Release with New Models and Performance Boosts](#item-1) ⭐️ 8.0/10
2. [Linus Torvalds Credits AI in Debugging Linux Kernel Bug](#item-2) ⭐️ 8.0/10
3. [Developer Builds 60MB Quantized LLM from Scratch with Disk Cache](#item-3) ⭐️ 8.0/10
4. [DelveRL: Open-Source Roguelike for Training RL Agents](#item-4) ⭐️ 8.0/10
5. [Evaluation Resolution Artifact Skews Brain-Likeness of Untrained CNNs](#item-5) ⭐️ 8.0/10
6. [Open Models Catch Up Faster, Gap Halves Each Generation](#item-6) ⭐️ 8.0/10
7. [US Groups Urge FTC to Probe AI Firms' Book Destruction](#item-7) ⭐️ 8.0/10
8. [Coding Agents Need More Than Code Review](#item-8) ⭐️ 7.0/10
9. [llm 0.33 Release: OpenAI 3.x Upgrade and Embedding Key Support](#item-9) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.18: Major Release with New Models and Performance Boosts](https://github.com/sgl-project/sglang/releases/tag/v0.5.18) ⭐️ 8.0/10

SGLang v0.5.18 has been released, incorporating 710 pull requests from 212 contributors. This release adds support for several new models, including Muse Glimmer, Intern-S2-Mobius, and SANA-Video, along with performance optimizations such as overlapped checkpoint staging and TP LMHead with All-to-All. This release significantly expands SGLang's model coverage and improves inference efficiency, which is crucial for developers deploying large language models in production. The performance gains, such as faster startup and reduced latency, will benefit users running models like DeepSeek-V4 on high-end hardware. Key optimizations include overlapped checkpoint staging that speeds up Qwen3-32B startup by up to 2.38x on H100, and TP LMHead with All-to-All reducing LMHead time from 320us to 169us on DeepSeek-V4-Pro B200. The release also unifies compiled-kernel caches under SGLANG_CACHE_DIR and updates dependencies to torch 2.13.0, flashinfer 0.6.17, and sgl-kernel 0.4.6.post1.

github · Fridge003 · Aug 22, 00:09

**Background**: SGLang is a high-performance serving framework for large language models and multimodal models, designed to optimize inference throughput and latency. It supports a wide range of models and provides features like continuous batching, CUDA graphs, and FlashInfer integration. The release includes new models such as Muse Glimmer, a 30B parameter agentic model from Meta, and Intern-S2-Mobius, a 35B foundation model from InternLM, reflecting the growing diversity of open-source AI models.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sgl-project/sglang/releases">Releases · sgl-project/ sglang</a></li>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://huggingface.co/internlm/Intern-S2-Mobius">internlm/Intern-S2-Mobius - Hugging Face</a></li>

</ul>
</details>

**Tags**: `#SGLang`, `#LLM inference`, `#release`, `#AI models`, `#open source`

---

<a id="item-2"></a>
## [Linus Torvalds Credits AI in Debugging Linux Kernel Bug](https://simonwillison.net/2026/Aug/22/linus-torvalds/) ⭐️ 8.0/10

Linus Torvalds publicly acknowledged that an AI significantly helped him debug a challenging Linux kernel graphics driver issue, even letting the AI write the commit message. The fix, commit 818bebeb63dd, addresses the Xe driver incorrectly handing out flat CCS storage as usable VRAM. This marks a notable endorsement of AI-assisted development from one of the most influential figures in software engineering, potentially encouraging wider adoption of AI tools in kernel and systems programming. It also highlights AI's practical utility in complex debugging while acknowledging its limitations, such as prematurely declaring problems unsolvable. The debugging process involved 24 debug patches and 18 kernel boots, ultimately tracing the bug to a single line where round_up() should have been round_down(). Torvalds noted that the AI repeatedly stated the problem was impossible and unsolvable, but it faithfully continued adding debug code and analyzing results when pushed.

rss · Simon Willison · Aug 22, 21:04

**Background**: The Linux kernel is the core of many operating systems, and its development is typically managed by maintainers like Linus Torvalds. The Xe driver is Intel's newer graphics driver for Linux, and the bug involved the Compute Command Streamer (CCS) storage being incorrectly exposed as usable VRAM, leading to memory corruption. AI-assisted programming tools, such as large language models, are increasingly used to generate code and assist with debugging, though their reliability in complex systems remains a topic of debate.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/torvalds/linux/commit/818bebeb63dd6bf5f4e07e145f6cdbace520a34c">drm/xe: Don't hand out the flat CCS storage as usable VRAM · torvalds/linux@818bebe</a></li>
<li><a href="https://www.phoronix.com/news/Linus-Torvalds-Debug-AI">Linus Torvalds Endures A Debug Session From Hell ... - Phoronix</a></li>
<li><a href="https://itsfoss.com/news/torvalds-used-ai-fix-kernel-bug/">Linux Creator Linus Torvalds Just Used AI to Fix a Kernel Bug</a></li>

</ul>
</details>

**Tags**: `#AI-assisted development`, `#Linus Torvalds`, `#debugging`, `#Linux kernel`, `#AI limitations`

---

<a id="item-3"></a>
## [Developer Builds 60MB Quantized LLM from Scratch with Disk Cache](https://www.reddit.com/r/MachineLearning/comments/1vv2nkh/i_developed_my_own_quantized_llm_from_scratch/) ⭐️ 8.0/10

A developer trained a 250M parameter LLM from scratch on 30B tokens of FineWeb, quantized to under 2 bits, achieving a 60 MB deployment that runs at 400 tok/s on CPU. The model uses a disk-based cache for long context, compressing older tokens to 1 bit and storing them on disk. This demonstrates a practical approach to extreme model compression and efficient long-context handling, potentially enabling LLM deployment on resource-constrained devices. It also introduces a novel fixed 512-bit token embedding that requires no trained parameters, which could inspire further research in efficient token representations. The model's vocabulary uses fixed 512-bit codes for 131k tokens, totaling 8.4 MB with zero trained parameters, and achieves a Spearman correlation of 0.619 on WordSim-353. The long-context cache stores older tokens at 320 bytes per token, allowing 1 million tokens of history to fit in about 320 MB on disk, and the model was trained to retrieve from this cache up to 100M tokens.

reddit · r/MachineLearning · /u/Final-Data-1410 · Aug 22, 04:39

**Background**: LLM quantization reduces model size by lowering the precision of weights, often to 4-bit or 2-bit, but extreme compression typically degrades quality. Traditional KV caches store all past tokens in high precision, which grows linearly with context length, making long contexts memory-intensive. This project combines aggressive quantization with a disk-based cache to address both size and context length challenges.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2508.05571">[2508.05571] iFairy: the First 2-bit Complex LLM with All Parameters in $\{\pm1, \pm i\}$</a></li>
<li><a href="https://github.com/pprp/awesome-llm-quantization">GitHub - pprp/Awesome-LLM-Quantization: Awesome list for LLM quantization · GitHub</a></li>
<li><a href="https://hackernoon.com/optimizing-llm-performance-with-lm-cache-architectures-strategies-and-real-world-applications">Optimizing LLM Performance with LM Cache ... | HackerNoon</a></li>

</ul>
</details>

**Discussion**: The Reddit community responded positively, with the author expressing gratitude for the curious and helpful comments. The discussion likely focused on the technical novelty, potential applications, and trade-offs of the approach.

**Tags**: `#LLM`, `#quantization`, `#efficient inference`, `#long context`, `#from-scratch training`

---

<a id="item-4"></a>
## [DelveRL: Open-Source Roguelike for Training RL Agents](https://www.reddit.com/r/MachineLearning/comments/1vvii1j/i_built_an_opensource_roguelike_specifically_for/) ⭐️ 8.0/10

The author released DelveRL, an open-source roguelike game designed specifically for training game-playing agents. It features a structured API, deterministic simulation, procedural levels, partial observability, and includes a recurrent PPO trainer with baseline results reaching a median floor of 18 and extended runs reaching floor 33. This project bridges game development and reinforcement learning research by providing a human-playable environment that is easy to integrate with agent harnesses, addressing a gap in existing environments. It offers a benchmark for the community to test diverse RL approaches, potentially accelerating progress in game-playing AI. DelveRL runs entirely locally, including batched renderer-free environments and a recurrent PPO trainer. The game, training code, checkpoint, bridge documentation, and raw benchmarks are all open source, inviting community contributions and baseline improvements.

reddit · r/MachineLearning · /u/SnyderConsulting · Aug 22, 17:32

**Background**: Roguelikes are a genre of games characterized by procedural generation, turn-based gameplay, and permadeath, making them challenging for AI agents due to partial observability and strategic depth. Reinforcement learning (RL) agents learn by interacting with environments, and PPO (Proximal Policy Optimization) is a popular on-policy algorithm. Recurrent PPO uses recurrent neural networks to handle partial observability by maintaining memory across time steps.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/MarcoMeter/recurrent-ppo-truncated-bptt">GitHub - MarcoMeter/recurrent-ppo-truncated-bptt: Baseline ...</a></li>
<li><a href="https://docs.pytorch.org/tutorials/intermediate/reinforcement_ppo.html">Reinforcement Learning (PPO) with TorchRL Tutorial</a></li>

</ul>
</details>

**Tags**: `#reinforcement learning`, `#open-source`, `#game environment`, `#AI training`, `#procedural generation`

---

<a id="item-5"></a>
## [Evaluation Resolution Artifact Skews Brain-Likeness of Untrained CNNs](https://www.reddit.com/r/MachineLearning/comments/1vvdxwt/the_evaluation_resolution_has_been_shown_to_have/) ⭐️ 8.0/10

A new preprint demonstrates that the apparent brain-likeness of untrained CNNs at V1 is largely an artifact of evaluation resolution, not a genuine property of the learning rule. The study shows that the gap between trained and untrained backpropagation CNNs narrows from -0.001±0.007 at 32px to +0.044±0.006 at 224px, a non-monotonic trend across image sizes. This finding challenges a common claim in computational neuroscience that untrained CNNs can match or surpass trained ones at V1, which has implications for how model-brain comparisons are conducted. It underscores the need for careful control of evaluation parameters to avoid misleading conclusions about biological plausibility. The study used a small CNN trained at 32px on a CIFAR-10 subset, five learning rules (random init, backprop, feedback alignment, predictive coding, STDP), and evaluated on THINGS-fMRI stimuli at six resolutions from 32px to 224px. They ruled out train/eval resolution matching, Gabor/pixel low-level structure, uncalibrated batch-norm, and convergence to global brightness, and found that the backprop > untrained effect at LOC survives across all resolutions.

reddit · r/MachineLearning · /u/ConfusionSpiritual19 · Aug 22, 14:30

**Background**: In model-brain comparisons, researchers often use representational similarity analysis (RSA) to measure how well a model's internal representations align with brain activity. A common claim is that untrained CNNs can match or surpass trained ones at early visual cortex (V1), suggesting that learning rules like backpropagation may not be necessary for brain-like representations. This study investigates whether such claims are artifacts of evaluation resolution, which can affect the apparent similarity.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Spike-timing-dependent_plasticity">Spike-timing-dependent plasticity - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/feedback-alignment-fa">Feedback Alignment in Neural Networks</a></li>
<li><a href="https://arxiv.org/html/2505.19458">Recurrent Self - Attention Dynamics: An Energy-Agnostic Perspective...</a></li>

</ul>
</details>

**Discussion**: The Reddit discussion highlights the importance of this methodological finding, with commenters noting that it could invalidate previous studies that did not control for evaluation resolution. Some debate the interpretation of the LOC effect and the generalizability to other architectures and datasets.

**Tags**: `#computational neuroscience`, `#CNN`, `#brain-like models`, `#evaluation methodology`, `#RSA`

---

<a id="item-6"></a>
## [Open Models Catch Up Faster, Gap Halves Each Generation](https://newsletter.semianalysis.com/p/are-open-models-catching-up) ⭐️ 8.0/10

SemiAnalysis reports that open-source models are catching up to closed-source ones at an accelerating rate, with the gap halving each generation, especially in the agentic era. For example, Kimi K2.6 surpassed Opus 4.5 in 4.8 months, and GLM-5.2 exceeded GPT-5.2 in 6 months. This trend signals the commoditization of the model layer, shifting pricing power and margin expansion to silicon and infrastructure layers. It could reshape competitive dynamics, as open models like GLM 5.3 and Kimi K3 can now handle many coding and agentic tasks that previously drove Anthropic's revenue. SemiAnalysis divides model history into three eras: early scaling, inference, and agentic, noting that the capability gap fluctuates cyclically. Despite benchmark gains, the article cautions that benchmarks are not everything, and Anthropic's productization strength remains an advantage.

telegram · zaihuapd · Aug 22, 08:26

**Background**: Open-source models are AI models with publicly available weights, allowing developers to use and modify them freely. Closed-source models, like those from OpenAI and Anthropic, are proprietary and accessed via APIs. The agentic era refers to AI systems that can act autonomously on tools and data, not just respond to prompts.

<details><summary>References</summary>
<ul>
<li><a href="https://x.com/SemiAnalysis_/status/2090842316655243463">SemiAnalysis on X: "Are Open Models Catching Up? Comparing ...</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-the-agentic-era-google-io-2026">What Is the Agentic Era? How Google I/O 2026 Defined the Next Phase of AI | MindStudio</a></li>
<li><a href="https://www.reddit.com/r/aiagents/comments/1rqtjjf/opus_46_vs_kimi_25_i_ran_a_logic_stress_test_for/">r/aiagents on Reddit: Opus 4.6 vs Kimi 2.5: I ran a logic stress test for agent workflows (no synthetic benchmarks)</a></li>

</ul>
</details>

**Discussion**: Community discussions highlight real-world comparisons, such as Reddit users testing Opus 4.6 vs Kimi 2.5 for agent workflows, noting that premium pricing may not be justified. Others point out that cost differences are dramatic, with K2.6 enabling more extensive retry strategies and parallel workers.

**Tags**: `#open-source AI`, `#model comparison`, `#AI trends`, `#SemiAnalysis`, `#commoditization`

---

<a id="item-7"></a>
## [US Groups Urge FTC to Probe AI Firms' Book Destruction](https://www.axios.com/2026/08/21/ftc-ai-companies-book-destruction-investigate) ⭐️ 8.0/10

On August 21, 2026, over a dozen US civil society groups, including Demand Progress Education Fund and the Consumer Federation of America, sent a joint letter to the Federal Trade Commission (FTC) urging an investigation into AI companies that buy, scan, and destroy physical books to train their models, alleging this constitutes unfair competition under Section 5 of the FTC Act. This marks a significant expansion of the AI training data debate from copyright into antitrust and competition regulation. If the FTC takes up the case, it could impose new constraints on how AI companies acquire training data, potentially affecting major players like Anthropic, Google, Microsoft, and OpenAI, and shaping the future of AI development. The letter specifically cites Anthropic's practice of spending millions of dollars to buy books, cutting off spines, and scanning pages for training Claude. The groups argue that this 'hoard-and-destroy' approach raises rivals' costs and builds a moat, but they do not advocate restricting AI training itself.

telegram · zaihuapd · Aug 22, 15:40

**Background**: AI companies need vast amounts of text data to train large language models (LLMs) like Claude, GPT-4, and Gemini. While much data comes from the internet, some companies have resorted to purchasing physical books, especially rare or out-of-print ones, to access high-quality content. This practice has drawn criticism because it destroys the physical copies, potentially losing valuable works forever. The FTC's Section 5 authority allows it to police unfair methods of competition, and this complaint seeks to apply that to AI training data acquisition.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nationpress.com/all/ftc-urged-to-probe-ai-book-destruction-practices">FTC urged to probe AI firms buying and destroying books for ...</a></li>
<li><a href="https://startupfortune.com/ai-firms-are-buying-and-pulping-rare-books-after-scanning-them-for-training-data/">AI Firms Are Buying and Pulping Rare Books After Scanning ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#FTC`, `#regulation`, `#training data`, `#competition`

---

<a id="item-8"></a>
## [Coding Agents Need More Than Code Review](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/) ⭐️ 7.0/10

Simon Willison argues that the key skill for using coding agents is confidently instructing and verifying changes, which may not always involve line-by-line code review. He suggests that other verification methods can be more effective than reviewing every line of code. This perspective challenges the traditional emphasis on code review in AI-assisted development, potentially changing how developers approach validation. It highlights a practical skill gap that many developers face when adopting coding agents, which could influence training and tooling. Willison emphasizes that 'eyeballing every line of code has never been the most effective way to validate a change.' He implies that alternative verification strategies, such as running tests or using other automated checks, may be more reliable.

rss · Simon Willison · Aug 22, 15:56

**Background**: Coding agents are AI tools that can autonomously write or modify code based on user instructions. Agentic engineering is an emerging discipline that involves orchestrating these agents with human oversight. Traditional code review involves manually inspecting every line of code, but as AI-generated code becomes more common, developers are exploring more efficient verification methods.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/Agentic_Engineering">Agentic Engineering</a></li>
<li><a href="https://coder.com/solutions/agents">Coder Agents - AI Coding Agents on Your Infrastructure | Coder</a></li>

</ul>
</details>

**Tags**: `#coding-agents`, `#code-review`, `#AI`, `#LLMs`, `#agentic-engineering`

---

<a id="item-9"></a>
## [llm 0.33 Release: OpenAI 3.x Upgrade and Embedding Key Support](https://simonwillison.net/2026/Aug/22/llm/) ⭐️ 6.0/10

llm 0.33 has been released, upgrading to the OpenAI Python library 3.x and switching the HTTP client dependency from httpx to httpx2. It also adds --key support for llm embed and llm embed-multi commands, and allows repeating -t/--template to combine templates. This release improves consistency and flexibility for llm users, particularly in embedding workflows and template composition. The upgrade to OpenAI 3.x ensures compatibility with the latest OpenAI API changes, which is crucial for developers relying on the tool. The embedding models now use the same key pattern as regular LLM models, with a compatibility fallback for existing plugins. Additionally, reasoning-capable Responses API models now support a reasoning_summary option with auto, concise, and detailed values, useful for models that imitate the OpenAI Responses API.

rss · Simon Willison · Aug 22, 17:01

**Background**: llm is a command-line tool for interacting with large language models, allowing users to run prompts, manage templates, and perform embeddings. The OpenAI Python library is the official client for accessing OpenAI's API, and httpx2 is an HTTP client library used for making requests. This release addresses a previous fix and introduces new features to enhance usability.

<details><summary>References</summary>
<ul>
<li><a href="https://pypi.org/project/openai/">The official Python library for the openai API</a></li>
<li><a href="https://github.com/simonw/llm/issues/757">llm embed -- key option · Issue #757 · simonw/ llm · GitHub</a></li>

</ul>
</details>

**Tags**: `#llm`, `#release`, `#OpenAI`, `#embedding`, `#CLI`

---