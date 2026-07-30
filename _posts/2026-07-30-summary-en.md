---
layout: default
title: "Horizon Summary: 2026-07-30 (EN)"
date: 2026-07-30
lang: en
---

> From 48 items, 12 important content pieces were selected

---

1. [Top AI startups increasingly withhold research publications](#item-1) ⭐️ 8.0/10
2. [Open-source engine runs Gemma 4 26B in 2 GB RAM on Mac](#item-2) ⭐️ 8.0/10
3. [Mitchell Hashimoto Launches Superlogical for Agentic Terminals](#item-3) ⭐️ 8.0/10
4. [Long policy documents fail to govern LLM agents](#item-4) ⭐️ 8.0/10
5. [Document-borne AI worms self-propagate through Copilot for Word](#item-5) ⭐️ 8.0/10
6. [Two API Settings Triple GPT-5.6 ARC-AGI-3 Scores](#item-6) ⭐️ 8.0/10
7. [OpenAI gives 100,000 researchers free ChatGPT access](#item-7) ⭐️ 8.0/10
8. [Matthew Green: AI's Perfect Moment for Cryptanalysis](#item-8) ⭐️ 8.0/10
9. [PostSlate achieves vendor-agnostic ML inference via ncnn Vulkan](#item-9) ⭐️ 8.0/10
10. [Google DeepMind Launches Lyria 3.5 in Flow Music](#item-10) ⭐️ 7.0/10
11. [Guide: Adding Custom MCP Server to Claude and ChatGPT](#item-11) ⭐️ 7.0/10
12. [D. Richard Hipp on SQL Democratizing Data Querying](#item-12) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Top AI startups increasingly withhold research publications](https://www.science.org/content/article/ai-s-top-startups-are-barely-publishing-their-research) ⭐️ 8.0/10

A new analysis reveals that leading AI startups are publishing fewer research papers, driven by competitive pressures and negative experiences with peer review. This trend threatens the openness and reproducibility of AI research, potentially slowing scientific progress and concentrating knowledge within a few private companies. The study used cumulative citations as a proxy for research impact, listing OpenAI, MEGVII, Hugging Face, Waymo, and others as top-cited startups, but noted that many of these companies now publish less.

hackernews · YeGoblynQueenne · Jul 29, 21:25 · [Discussion](https://news.ycombinator.com/item?id=49103285)

**Background**: Traditionally, AI research has been shared openly through conferences and journals, enabling rapid progress. However, as AI becomes commercially valuable, startups face a trade-off between publishing to build reputation and keeping proprietary methods secret to maintain a competitive edge.

**Discussion**: Commenters shared personal experiences: one noted that after three years of failed attempts to publish in top journals, their startup gave up and only released a preprint. Another said they avoid publishing to prevent OpenAI and Anthropic from copying their results. Some pointed out that companies like OpenAI and Hugging Face still publish, but the overall trend is concerning.

**Tags**: `#AI research`, `#startups`, `#open science`, `#publication ethics`

---

<a id="item-2"></a>
## [Open-source engine runs Gemma 4 26B in 2 GB RAM on Mac](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare, an open-source inference engine written in Swift and Metal, can run a 4-bit quantized Gemma 4 26B-A4B-IT model on any M-series Mac using only about 2 GB of RAM by streaming routed experts from SSD. This enables running large MoE models on memory-constrained Apple hardware, democratizing access to capable on-device AI. It achieves 5–6 tok/s on an 8 GB M2 MacBook Air and 31–35 tok/s on an M5 MacBook Pro. The model's 4-bit weights occupy ~14 GB, but TurboFieldfare keeps only the shared layers and KV cache in RAM, streaming routed experts from SSD with a small expert cache and bounded parallel pread. It also includes an experimental OpenAI-compatible local server with streaming and tool calls.

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Gemma 4 26B-A4B-IT is a Mixture-of-Experts (MoE) model from Google DeepMind with 25.2B total parameters but only 3.8B active per token, making it efficient for inference. Traditional inference engines load the entire model into RAM, which is infeasible for large models on devices with limited memory. TurboFieldfare exploits the MoE architecture by loading only the shared layers and caching experts on demand.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/google/gemma-4-26b-a4b-it:free">Gemma 4 26 B A 4 B (free) - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>

</ul>
</details>

**Discussion**: Commenters praised the novel approach, with one noting that llama.cpp can also run 26B in 2GB via mmap but lacks the synchronized SSD reads tuned for latency. Another user shared a compilation fix for older macOS, and a developer working on DiffusionGemma suggested potential kernel collaboration.

**Tags**: `#on-device AI`, `#inference engine`, `#model quantization`, `#Mac`, `#open-source`

---

<a id="item-3"></a>
## [Mitchell Hashimoto Launches Superlogical for Agentic Terminals](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto announced Superlogical, a new company building composable, agent-driven terminal applications on top of the open-source libghostty library. He also transferred ownership of Ghostty to a non-profit organization. This marks a significant shift in terminal application development, moving toward modular, agent-integrated tools that could reshape how developers interact with the command line. Hashimoto's track record with HashiCorp and Ghostty adds credibility to this vision. Superlogical will use libghostty as a public building block, consuming the same MIT-licensed components available to everyone else, and will continue to upstream shared terminal work. The company's vision involves composable terminal applications that can be orchestrated by AI agents.

hackernews · yan · Jul 29, 15:41 · [Discussion](https://news.ycombinator.com/item?id=49098965)

**Background**: Ghostty is a fast, feature-rich, cross-platform terminal emulator using GPU acceleration and platform-native UI. Its core library, libghostty, provides a C-compatible API for embedding terminal functionality in third-party projects. The concept of agent-driven terminals involves AI agents interacting with CLI applications to automate tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty-org/ghostty: 👻 Ghostty is a fast, feature-rich, and cross-platform terminal emulator that uses platform-native UI and GPU acceleration.</a></li>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://github.com/jasonkneen/agent-terminal">GitHub - jasonkneen/agent-terminal: Automate terminals for agents · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters praised Hashimoto's decision to transfer Ghostty to a non-profit and build Superlogical on an open-source foundation. Some drew parallels to OLE/COM, noting the potential for composable terminal components, while others expressed frustration with the enigmatic title.

**Tags**: `#terminal`, `#open-source`, `#startup`, `#agentic`, `#composability`

---

<a id="item-4"></a>
## [Long policy documents fail to govern LLM agents](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

A study titled Handbook.md demonstrates that long policy documents do not reliably govern LLM agents, due to context window limitations and model quantization issues. This finding challenges the assumption that long-context LLMs can faithfully follow extensive instructions, which is critical for AI safety and agentic applications. The study empirically shows that as policy documents grow longer, LLM agents increasingly fail to adhere to them, with performance degradation linked to context window saturation and quantization noise in the KV cache.

hackernews · spIrr · Jul 29, 13:01 · [Discussion](https://news.ycombinator.com/item?id=49096969)

**Background**: Large language models (LLMs) have a limited context window, which restricts how much text they can process at once. Model quantization reduces memory usage by lowering numerical precision, but can introduce errors that compound over long contexts. These factors together undermine the reliability of LLM agents when given lengthy policy documents.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/model-quantization-concepts-methods-and-why-it-matters/">Model Quantization: Concepts, Methods, and Why It Matters | NVIDIA Technical Blog</a></li>
<li><a href="https://atlan.com/know/llm-context-window-limitations/">LLM Context Window Limitations in 2026</a></li>

</ul>
</details>

**Discussion**: Community comments highlight practical failures: users report that Claude ignores CLAUDE.md instructions after about 10 minutes, and that local inference could mitigate the problem. Some argue that humans also struggle with long policy documents, so the benchmark may be unrealistically demanding.

**Tags**: `#LLM`, `#long-context`, `#AI safety`, `#agents`, `#benchmark`

---

<a id="item-5"></a>
## [Document-borne AI worms self-propagate through Copilot for Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 8.0/10

Researcher Håkon Måløy demonstrated a novel prompt injection variant that turns Microsoft Copilot for Word into a self-replicating AI worm, where malicious instructions hidden in a document can propagate to new documents automatically. This vulnerability highlights a fundamental security flaw in LLM-integrated applications: the inability to separate data from instructions, posing serious risks to enterprise users who rely on Copilot for sensitive document processing. The attack uses white text to hide malicious prompts that Copilot reads and executes, altering document content and copying the attack payload into new files. No robust mitigation exists for this broader vulnerability class as of publication.

hackernews · Canopy9560 · Jul 29, 11:44 · [Discussion](https://news.ycombinator.com/item?id=49096188)

**Background**: Prompt injection attacks exploit LLMs' inability to distinguish between system instructions and user-provided content. When an LLM processes a document, it treats the text as part of its context, allowing hidden instructions to influence behavior. This is similar to SQL injection but targets AI models.

<details><summary>References</summary>
<ul>
<li><a href="https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/">Context Collapse, Part 3 - AI Worming through Word | En Klype Salt</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://dev.to/onsen/ai-worms-in-word-how-document-borne-threats-self-propagate-5gc7">AI Worms in Word: How Document-Borne Threats Self - Propagate</a></li>

</ul>
</details>

**Discussion**: Commenters express concern that this vulnerability is fundamentally unfixable without redesigning how AI agents handle data vs. instructions. Some users have already disabled Copilot locally, while others note that simple obfuscation techniques like white text still work.

**Tags**: `#AI security`, `#prompt injection`, `#Copilot`, `#adversarial attacks`, `#LLM vulnerabilities`

---

<a id="item-6"></a>
## [Two API Settings Triple GPT-5.6 ARC-AGI-3 Scores](https://openai.com/index/how-two-settings-tripled-our-arc-agi-3-scores) ⭐️ 8.0/10

OpenAI discovered that enabling two API settings—retaining reasoning across turns and enabling compaction—tripled GPT-5.6's scores on the ARC-AGI-3 benchmark, while also improving efficiency. This finding demonstrates that simple configuration changes can dramatically boost AI performance on a challenging interactive reasoning benchmark, offering a low-cost path to better agentic intelligence without model retraining. The two settings are 'retaining reasoning' (preserving the model's reasoning chain across conversation turns) and 'compaction' (compressing conversation history to fit within context windows). The combination tripled scores on ARC-AGI-3, which tests agents' ability to explore novel environments and infer goals interactively.

rss · OpenAI Blog · Jul 29, 15:00

**Background**: ARC-AGI-3 is an interactive reasoning benchmark that measures human-like intelligence in AI agents by requiring them to explore novel environments, acquire goals on the fly, and build internal models. Compaction is a technique that reduces the size of conversation history while preserving important context, and retaining reasoning keeps earlier reasoning blocks across turns for reuse. These settings help manage context window limits and maintain reasoning coherence in long interactions.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://jxnl.co/writing/2025/08/30/context-engineering-compaction/">Two Experiments We Need to Run on AI Agent Compaction - Jason Liu</a></li>

</ul>
</details>

**Tags**: `#AI`, `#benchmark`, `#GPT`, `#reasoning`, `#efficiency`

---

<a id="item-7"></a>
## [OpenAI gives 100,000 researchers free ChatGPT access](https://openai.com/index/chatgpt-for-academic-researchers) ⭐️ 8.0/10

OpenAI announced a program called ChatGPT for Academic Researchers, providing 100,000 researchers at selected academic institutions with free access to its most advanced AI models for one year. This initiative could significantly accelerate scientific discovery by giving researchers powerful AI tools for data analysis, literature review, and hypothesis generation, potentially transforming research workflows across disciplines. The program is aimed at researchers in fields such as biology, chemistry, computer science, engineering, mathematics, and physics, and includes access to a dedicated ChatGPT workspace with frontier models.

rss · OpenAI Blog · Jul 29, 10:00

**Background**: Large language models like ChatGPT can assist researchers by summarizing papers, generating code, and suggesting experimental designs. However, access to advanced models often requires costly subscriptions, limiting their use in academia. This program removes that barrier for a large cohort of researchers.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/chatgpt-for-academic-researchers/">Accelerating scientific discovery with ChatGPT for Academic... | OpenAI</a></li>
<li><a href="https://help.openai.com/en/articles/20001406">ChatGPT for Academic Researchers | OpenAI Help Center</a></li>
<li><a href="https://www.axios.com/2026/07/29/openai-academics-research-chatgpt-sol">OpenAI launches free AI access program for academic researchers</a></li>

</ul>
</details>

**Tags**: `#AI`, `#OpenAI`, `#Scientific Research`, `#Education`

---

<a id="item-8"></a>
## [Matthew Green: AI's Perfect Moment for Cryptanalysis](https://simonwillison.net/2026/Jul/29/matthew-green/#atom-everything) ⭐️ 8.0/10

Matthew Green highlights that the current transition to post-quantum cryptography is an ideal time for AI to advance cryptanalysis, potentially strengthening confidence in new algorithms. This insight underscores the critical intersection of AI and cryptography, where AI-driven cryptanalysis could either validate or undermine the security of post-quantum standards, affecting global security infrastructure. Green references standards like HAWK being considered, and mentions Impagliazzo's Minicrypt world as a scenario where AI might not break all hard problems. He notes that the best outcome is robust cryptanalysis literature.

rss · Simon Willison · Jul 29, 18:18

**Background**: Post-quantum cryptography (PQC) aims to develop algorithms secure against quantum computers, which could break current RSA and elliptic-curve cryptography. NIST has been standardizing PQC algorithms since 2024. Impagliazzo's five worlds classify possible computational complexity scenarios, with Minicrypt being one where public-key cryptography is possible but not all hard problems exist.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Post-quantum_cryptography">Post-quantum cryptography</a></li>
<li><a href="https://blog.computationalcomplexity.org/2004/06/impagliazzos-five-worlds.html">Computational Complexity: Impagliazzo 's Five Worlds</a></li>

</ul>
</details>

**Tags**: `#post-quantum cryptography`, `#cryptanalysis`, `#AI`, `#security`, `#standards`

---

<a id="item-9"></a>
## [PostSlate achieves vendor-agnostic ML inference via ncnn Vulkan](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

PostSlate, a video editing tool, achieved vendor-agnostic ML inference on production edge devices by using ncnn's Vulkan backend, resulting in 10x speedups over ONNX CPU for face detection and embedding models. This approach enables ML inference on any GPU (NVIDIA, AMD, Intel, Apple Silicon) without vendor-specific runtimes, simplifying deployment and reducing user friction for edge applications. On an RTX 4070 with fp16, ArcFace R50 runs in 3 ms (vs. 30 ms ONNX CPU) and SCRFD face detection in 2.5 ms (vs. 25 ms). Model size is halved from 174 MB (ONNX fp32) to 87 MB (ncnn fp16).

reddit · r/MachineLearning · /u/ppchaos · Jul 29, 10:22

**Background**: ncnn is a high-performance neural network inference framework optimized for mobile and edge devices. Its Vulkan backend leverages the cross-platform GPU API Vulkan to accelerate inference on diverse hardware without vendor lock-in.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/">Vendor-agnostic ML inference on production edge devices [R] - Reddit</a></li>
<li><a href="https://github.com/futz12/bergamot-ncnn-vulkan">GitHub - futz12/bergamot- ncnn - vulkan : mobile-friendly mechine...</a></li>
<li><a href="https://www.youtube.com/watch?v=vSVECHe1WN4">ncnn Vulkan Machine Learning Update - YouTube</a></li>

</ul>
</details>

**Tags**: `#ML inference`, `#Vulkan`, `#edge devices`, `#ncnn`, `#vendor-agnostic`

---

<a id="item-10"></a>
## [Google DeepMind Launches Lyria 3.5 in Flow Music](https://deepmind.google/blog/were-launching-lyria-35-in-google-flow-music-with-advances-across-musicality-lyrics-vocals-and-creative-control/) ⭐️ 7.0/10

Google DeepMind has launched Lyria 3.5, the latest version of its music generation model, now integrated into Google Flow Music. The update brings significant improvements in musicality, lyrics, vocal quality, and creative control. This release marks a major step forward in AI-powered music creation, offering users more realistic and expressive tools for composing and producing music. It could empower both amateur and professional musicians to explore new creative possibilities. Lyria 3.5 is accessible through Google Flow Music, a platform that learns the user's style and personalizes the experience. The model enhances vocal clarity, lyrical coherence, and overall musical structure, while giving users finer control over the output.

rss · Google DeepMind Blog · Jul 29, 16:02

**Background**: Lyria is a series of AI music generation models developed by Google DeepMind, designed to create original music from text prompts or other inputs. Google Flow Music is a web-based application that leverages Lyria to help users generate songs, playlists, and music videos. Earlier versions like Lyria 3 laid the groundwork for these capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-labs/lyria-3-5/">Introducing Lyria 3 . 5 in Google Flow Music</a></li>
<li><a href="https://deepmind.google/models/lyria/">Lyria 3 — Google DeepMind</a></li>
<li><a href="https://www.flowmusic.app/?ref=futureen&from-riffusion=true">Google Flow Music</a></li>

</ul>
</details>

**Tags**: `#AI`, `#music generation`, `#Google DeepMind`, `#creative tools`

---

<a id="item-11"></a>
## [Guide: Adding Custom MCP Server to Claude and ChatGPT](https://simonwillison.net/2026/Jul/29/mcp-in-claude-and-chatgpt/#atom-everything) ⭐️ 7.0/10

Simon Willison published a step-by-step tutorial explaining how to connect a custom MCP server to the standard chat interfaces of Claude and ChatGPT. This tutorial makes it easier for developers to integrate external tools and data sources with major AI chat platforms, reducing vendor lock-in and promoting interoperability. The process involves multiple steps, including setting up an MCP server and configuring the chat interfaces to use it. The tutorial is based on the Model Context Protocol (MCP), an open standard introduced by Anthropic in November 2024.

rss · Simon Willison · Jul 29, 00:13

**Background**: The Model Context Protocol (MCP) is an open standard and framework introduced by Anthropic to standardize how AI systems like LLMs integrate with external tools and data sources. It provides a unified interface for reading files, executing functions, and handling context, similar to how the Language Server Protocol (LSP) works for code editors. Major AI providers including OpenAI and Google DeepMind have adopted MCP.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MCP_server">MCP server</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#Claude`, `#ChatGPT`, `#AI`, `#tutorial`

---

<a id="item-12"></a>
## [D. Richard Hipp on SQL Democratizing Data Querying](https://simonwillison.net/2026/Jul/29/d-richard-hipp/#atom-everything) ⭐️ 5.0/10

D. Richard Hipp, creator of SQLite, compared SQL's democratization of data querying to the shift from COBOL programmers, arguing that jobs evolve rather than disappear. This perspective offers reassurance that automation and new tools like SQL do not eliminate programming jobs but transform them, which is relevant to ongoing debates about AI's impact on software careers. Hipp noted that before SQL, querying large datasets required expensive COBOL programmers; SQL allowed users to specify queries simply, generating the equivalent code automatically. He emphasized that programmers' roles changed, not vanished.

rss · Simon Willison · Jul 29, 21:15

**Background**: COBOL is a business-oriented programming language from the 1950s, widely used for data processing on mainframes. SQL (Structured Query Language) was developed in the 1970s and became the standard for relational database querying, making data access more accessible to non-programmers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/COBOL_programming_language">COBOL programming language</a></li>

</ul>
</details>

**Tags**: `#sql`, `#d-richard-hipp`, `#programming-history`, `#careers`

---