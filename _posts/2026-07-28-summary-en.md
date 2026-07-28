---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 33 items, 12 important content pieces were selected

---

1. [Moonshot AI Releases 2.8T Parameter Kimi K3 Open Weights](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0: Inkling support, DeepSeek-V4 optimizations, flexible attention](#item-2) ⭐️ 8.0/10
3. [Anthropic Clarifies Stance on Open-Weights Models](#item-3) ⭐️ 8.0/10
4. [Python-build-standalone: Portable Python Distributions](#item-4) ⭐️ 8.0/10
5. [Judge Rejects Google's DMCA Defense Against Scraping](#item-5) ⭐️ 8.0/10
6. [Solo Study Finds Left-Leaning Bias in 6 Frontier LLMs](#item-6) ⭐️ 8.0/10
7. [Google Teases Gemini 4 as Most Ambitious Pretraining Yet](#item-7) ⭐️ 8.0/10
8. [MCP Transforms AI Agent Development](#item-8) ⭐️ 7.0/10
9. [JD.com's High-Risk AI Transformation to Embodied Intelligence](#item-9) ⭐️ 7.0/10
10. [OpenAI Study: AI Expands Workers' Task Range](#item-10) ⭐️ 6.0/10
11. [Ethan Mollick's Updated AI Guide: From Chat to Agents](#item-11) ⭐️ 6.0/10
12. [Chinese AI Cost Advantage Widens: UBS](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Moonshot AI Releases 2.8T Parameter Kimi K3 Open Weights](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

Moonshot AI has released the open weights of Kimi K3, a 2.8 trillion parameter model, on Hugging Face. The model features a new architecture with Kimi Delta Attention and Attention Residuals, supporting 1 million token context and native multimodal understanding. Kimi K3 is the world's first open 3T-class model, marking a major milestone in open-weight AI. Its release challenges proprietary frontier models and provides the community with a powerful, freely available model for long-horizon coding, knowledge work, and reasoning. The model uses a Stable LatentMoE framework with 896 experts, activating 16 per token, and achieves about 2.5x scaling efficiency over Kimi K2. The weights are 1.56TB on Hugging Face, and the license requires a separate agreement for large Model-as-a-Service businesses with over $20M annual revenue.

rss · Simon Willison · Jul 27, 23:39

**Background**: Moonshot AI is a Beijing-based AI company founded in March 2023, known for its Kimi series of large language models. Open-weight models allow anyone to download, inspect, and run the model locally, unlike closed-source models. The modified license for K3 adds restrictions for large commercial users, distinguishing it from fully open-source licenses.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://openlm.ai/kimi-k3/">Kimi K3 - openlm.ai</a></li>

</ul>
</details>

**Discussion**: The Telegram community praised the release as a major breakthrough, highlighting the model's 2.8T parameters and new architecture. Some noted the license restrictions as a caveat but overall sentiment was positive about the open-weight availability.

**Tags**: `#AI`, `#open-source`, `#large language model`, `#Hugging Face`, `#Moonshot AI`

---

<a id="item-2"></a>
## [vLLM v0.26.0: Inkling support, DeepSeek-V4 optimizations, flexible attention](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 adds full support for the Thinking Machines Lab Inkling model family, including base modeling, CUDA graphs, FlashAttention 4 relative attention, speculative decoding, LoRA, and ModelOpt NVFP4 quantization. It also delivers significant performance optimizations for DeepSeek-V4, introduces fp32 lm_head for generation models, and enables per-KV-cache-group attention backend selection. This release strengthens vLLM as a leading open-source LLM inference engine by supporting cutting-edge models like Inkling (a 1T-parameter multimodal MoE) and improving performance for DeepSeek-V4 across GPU vendors. The flexible attention backend and fp32 lm_head enhance accuracy and adaptability for hybrid models and generation tasks. The release includes 411 commits from 212 contributors, with 61 new contributors. Key technical additions include piecewise CUDA graph support for Inkling, a specialized routing kernel for DeepSeek-V4 (2.94% E2E TPOT improvement), and the ability to select different attention backends per KV-cache group.

github · khluu · Jul 27, 01:06

**Background**: vLLM is a high-performance open-source library for LLM inference and serving, widely used in production. The Inkling model is a 975B-parameter (41B active) multimodal MoE model from Thinking Machines Lab with up to 1M token context. FlashAttention 4 is the latest iteration of the efficient attention algorithm, optimized for Hopper and Blackwell GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://recipes.vllm.ai/thinkingmachines/Inkling">thinkingmachines/Inkling | vLLM Recipes</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance | vLLM Blog</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#performance optimization`, `#open source`, `#GPU`

---

<a id="item-3"></a>
## [Anthropic Clarifies Stance on Open-Weights Models](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic published a policy statement clarifying that it does not advocate for a ban on open-weights models, but instead supports mandatory safety testing for all sufficiently capable models, both open and closed. This statement is significant because it positions Anthropic in the ongoing debate over AI regulation, advocating for a middle ground that could shape future policy. However, critics argue that mandatory testing could effectively restrict open models if the testing process is costly or controlled by a single authority. Anthropic CEO Dario Amodei previously opposed bans on open-weights models, but the company now supports measures like banning chip sales to China and cracking down on smuggling, which some see as contradictory. The proposal for mandatory safety testing raises questions about who administers the tests and what happens if access is denied.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weights models are AI models where the trained parameters (weights) are publicly released, but the training data and code may not be fully open. This differs from fully open-source AI, which includes the complete source code and training data. Mandatory safety testing for AI models is a debated policy idea, with some governments considering legislation to require evaluations before deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2025/04/open-weight-models/">What are Open Source and Open Weight Models ? | Analytics Vidhya</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI_safety">AI safety - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments are highly critical of Anthropic's position. Users argue that mandatory safety testing is effectively a ban on open-weights models, as the testing process could be costly or controlled by a single entity. Others point out contradictions in Anthropic's stance, such as opposing bans on open models while supporting hardware export controls.

**Tags**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#policy`

---

<a id="item-4"></a>
## [Python-build-standalone: Portable Python Distributions](https://gregoryszorc.com/docs/python-build-standalone/main/) ⭐️ 8.0/10

Python-build-standalone provides self-contained, highly-portable Python distributions that are used by uv, pipx, Hatch, Poetry, Bazel, and many other tools to bundle Python into applications. These distributions simplify Python deployment by eliminating dependencies on system Python installations, enabling consistent Python environments across different operating systems and platforms. The project is now maintained by Astral (the company behind uv) and has seen over 70 million downloads since its release. It produces standalone builds that include the Python interpreter and standard library without requiring a system Python.

hackernews · jcbhmr · Jul 27, 18:43 · [Discussion](https://news.ycombinator.com/item?id=49073942)

**Background**: Traditionally, Python applications depend on a system-wide Python installation, which can lead to version conflicts and portability issues. Python-build-standalone solves this by providing pre-built, self-contained Python binaries that can be bundled directly with applications, similar to how static linking works in compiled languages.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/astral-sh/python-build-standalone">GitHub - astral-sh/ python - build - standalone : Produce redistributable...</a></li>
<li><a href="https://astral.sh/blog/python-build-standalone">A new home for python - build - standalone</a></li>
<li><a href="https://gregoryszorc.com/docs/python-build-standalone/main/">Python Standalone Builds — python - build - standalone documentation</a></li>

</ul>
</details>

**Discussion**: Community members praised the distributions for their utility in bundling Python into desktop apps and noted that Astral's maintenance ensures ongoing support. Some also mentioned alternative approaches like PyOxidizer and Cosmopolitan cross-platform binaries.

**Tags**: `#Python`, `#tooling`, `#distribution`, `#portability`, `#open source`

---

<a id="item-5"></a>
## [Judge Rejects Google's DMCA Defense Against Scraping](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

A U.S. judge ruled that Google cannot use the DMCA safe harbor provisions to block third-party scraping of its search results, rejecting Google's attempt to treat its search results as copyrighted compilations. This ruling sets a legal precedent that search engine results may not qualify for copyright protection, potentially reshaping the balance between copyright law and open web principles, and affecting how companies can protect their data from scraping. The court found that Google's search results lacked the minimal creativity required for copyright protection, as they are essentially factual listings. The case involved SerpAPI, a service that scrapes Google results for clients.

hackernews · cdrnsf · Jul 27, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49073513)

**Background**: The DMCA's safe harbor provisions (Section 512) limit liability for online service providers for user-generated content, but do not grant copyright protection to the provider's own content. Web scraping legality depends on factors like terms of service and whether the scraped data is copyrighted. Google had argued that scraping its search results violated its copyright in the compilation of results.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Online_Copyright_Infringement_Liability_Limitation_Act">Online Copyright Infringement Liability Limitation Act - Wikipedia</a></li>
<li><a href="https://www.congress.gov/crs-product/IF11478">Digital Millennium Copyright Act (DMCA) Safe Harbor Provisions for Online Service Providers: A Legal Overview | Congress.gov | Library of Congress</a></li>
<li><a href="https://www.copyright.gov/512/">Section 512 of Title 17: Resources on Online Service Provider Safe Harbors and Notice-and-Takedown System | U.S. Copyright Office</a></li>

</ul>
</details>

**Discussion**: Commenters largely supported the ruling, criticizing Google for hypocrisy given its own web crawling origins. Many noted that Google's deprecation of its search API created demand for scraping services, and some highlighted the importance of scraping for exposing scams like fake ETA/ESTA sites.

**Tags**: `#legal`, `#web scraping`, `#copyright`, `#Google`, `#DMCA`

---

<a id="item-6"></a>
## [Solo Study Finds Left-Leaning Bias in 6 Frontier LLMs](https://www.reddit.com/r/MachineLearning/comments/1v8fnzw/evaluated_6_frontier_llms_gpt54_claude_sonnet_46/) ⭐️ 8.0/10

A solo evaluation of six frontier LLMs (GPT-5.4, Claude Sonnet 4.6, Claude Opus 4.7, Gemini Pro, Gemini Flash, Grok 4.3) across 8 bias benchmarks (~20,600 examples) found that all models exhibit left-leaning political bias, including Grok despite its right-leaning self-report. This study provides empirical evidence of systematic political bias in frontier LLMs, raising concerns about fairness and neutrality in AI systems used for content moderation, information retrieval, and decision support. Grok self-reports as right-leaning but behaves left-leaning when classifying content or answering policy questions; refusal rates on race-related questions varied from ~5% (Claude Sonnet 4.6, Gemini Pro) to 20.3% (GPT-5.4).

reddit · r/MachineLearning · /u/marggggggggg · Jul 27, 22:37

**Background**: Bias benchmarks like WinoBias, BBQ, and SeeGULL are designed to measure social biases in language models. WinoBias focuses on gender bias in coreference resolution, BBQ covers stereotypes across nine social dimensions, and SeeGULL captures stereotypes about identity groups across countries. The Political Compass and other political bias datasets assess ideological leanings in model outputs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/winobias">WinoBias : Gender Bias in Coreference Benchmark</a></li>
<li><a href="https://huggingface.co/datasets/heegyu/bbq">heegyu/bbq · Datasets at Hugging Face</a></li>
<li><a href="https://github.com/google-research-datasets/seegull">GitHub - google-research-datasets/seegull: SeeGULL is a broad-coverage stereotype dataset in English containing stereotypes about identity groups spanning 178 countries across 8 different geo-political regions across 6 continents, as well as state-level identities within the US and India. · GitHub</a></li>

</ul>
</details>

**Discussion**: The Reddit community engaged in substantive debate: some praised the thoroughness of the evaluation, while others questioned the methodology (single prompt template, no multi-run averaging) and the interpretation of 'bias' as inherently problematic. Several commenters noted the importance of transparency in bias auditing.

**Tags**: `#LLM bias`, `#fairness`, `#benchmarking`, `#political bias`, `#AI safety`

---

<a id="item-7"></a>
## [Google Teases Gemini 4 as Most Ambitious Pretraining Yet](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

Google CEO Sundar Pichai announced during Alphabet's Q2 2026 earnings call that Gemini 4, the next-generation large language model, is now in training as the company's most ambitious pretraining project, with a target release by the end of 2026. Gemini 4 represents Google's next major leap in AI, potentially setting new benchmarks for large language models and intensifying competition with rivals like OpenAI. Its release could significantly impact AI capabilities available to developers and enterprises. Pichai emphasized that Google will prioritize allocating compute resources to frontier AGI research to ensure Gemini 4 remains at the cutting edge upon release. The Gemini 3.x Flash series will continue with near-monthly updates, focusing on improving intelligent coding and other capabilities.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Gemini is Google's family of large language models, with each major version (e.g., Gemini 1, 2, 3) bringing significant improvements in reasoning, coding, and multimodal understanding. Pretraining is the initial phase where a model learns from vast amounts of data, requiring immense computational resources. Google typically releases new Gemini models annually, with Gemini 3 launching in early 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://temperature2.com/p/2026-07-22-gemini-4-pretraining-before-3-5-pro-ships/">Google starts Gemini 4 pretraining before 3.5 Pro ships · temperature2</a></li>
<li><a href="https://coursiv.io/blog/gemini-4-pretraining">Gemini 4 Training Has Begun: Release Date & What... | Coursiv Blog</a></li>
<li><a href="https://andrew.ooo/answers/gemini-4-pretraining-tease-what-we-know-july-2026/">Gemini 4 Pretraining Tease: What We Know So Far... — andrew.ooo</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google`, `#Gemini`, `#large language model`, `#pretraining`

---

<a id="item-8"></a>
## [MCP Transforms AI Agent Development](https://news.google.com/rss/articles/CBMie0FVX3lxTE5WdHA1RUxfZGtfaVIxOXY3MVNYYlpUbmNZSmZlNE9FWTdEZDJUcjdIVm9xQ0k5a241UjNaX2tWeXdab0M5LXZvRXB0SThvTGN0R1VOb18wUWszQkJFaUNrWXZUWlZMR3RpZ0VIWjM3bm15cExVcE02V3lxUQ?oc=5) ⭐️ 7.0/10

The Model Context Protocol (MCP), an open standard introduced by Anthropic in November 2024, is now being adopted to standardize context sharing and interoperability among AI agents, enabling seamless integration with external tools and data sources. MCP addresses a critical fragmentation in AI agent development by providing a universal protocol for context exchange, similar to USB-C for AI applications. This could accelerate the creation of interoperable, multi-agent systems and reduce custom integration efforts. MCP uses JSON-RPC 2.0 messages for communication and is designed to connect AI applications like Claude or ChatGPT to local files, databases, search engines, and other tools. It is an open-source standard maintained by Anthropic.

google_news · HackerNoon · Jul 27, 00:39

**Background**: AI agents are software systems that use large language models (LLMs) to perform tasks autonomously, often requiring access to external tools and data. Previously, each agent had to be custom-integrated with each tool, leading to high development costs and limited interoperability. MCP standardizes this integration, allowing any MCP-compatible agent to connect to any MCP-compatible tool.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>
<li><a href="https://docs.anthropic.com/en/docs/mcp">Model Context Protocol ( MCP ) - Anthropic</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI agents`, `#protocol`, `#development`

---

<a id="item-9"></a>
## [JD.com's High-Risk AI Transformation to Embodied Intelligence](https://news.google.com/rss/articles/CBMiqgFBVV95cUxNYlY4U2dqSnpuSjhsbUlNQm50VF8wTjVOYTNCeVF3UklfRW05SzZuRlU3Z1VUeFg4WVo0SmZZN3ZGNEVacmpLQ0g0Ymd1cTRIT3c0ZjlDOUhmWVF5ZUNLRjJOSWVlUnRsMEFLci1EUmRmXzNxOFVERU9rbF9oSVdsZ0lRX0diVldCTlpldVFxR3pfYVhKOHVjcFgzbzNId2Raa2FBNzJKZndRdw?oc=5) ⭐️ 7.0/10

JD.com is undertaking a high-risk AI transformation to convert its heavy-asset logistics network into an embodied intelligence system, integrating AI with physical infrastructure. This move could redefine logistics efficiency by enabling autonomous decision-making and physical automation, potentially giving JD.com a competitive edge over rivals like Alibaba and Amazon. The transformation involves embedding AI into JD.com's warehouses, delivery vehicles, and supply chain operations, leveraging embodied intelligence to enable robots and systems to interact with the physical world.

google_news · Moomoo · Jul 27, 07:05

**Background**: Embodied intelligence refers to AI systems that have a physical body, allowing them to perceive and act in the real world, unlike traditional AI confined to software. JD.com's heavy-asset logistics network includes warehouses, trucks, and delivery infrastructure, which are capital-intensive but offer control over operations. This transformation aims to make these assets smarter and more autonomous.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Embodied_intelligence">Embodied intelligence</a></li>
<li><a href="https://cargospot.io/">Cargospot | Collaborative Logistics Operating System</a></li>
<li><a href="https://www.capstonelogistics.com/blog/asset-light-3pls-a-smarter-strategy/">Asset -Light 3PL: A Smarter Enterprise Logistics Strategy</a></li>

</ul>
</details>

**Tags**: `#AI`, `#logistics`, `#JD.com`, `#embodied intelligence`, `#transformation`

---

<a id="item-10"></a>
## [OpenAI Study: AI Expands Workers' Task Range](https://openai.com/index/how-ai-is-expanding-what-people-do-at-work) ⭐️ 6.0/10

OpenAI released research showing that ChatGPT users are taking on a broader variety of tasks across different job roles, effectively blurring traditional job boundaries. This suggests AI may reshape job descriptions and organizational structures, potentially increasing worker autonomy and productivity while challenging existing role definitions. The research is based on usage data from ChatGPT, but specific metrics, sample sizes, and methodologies were not disclosed in the summary.

rss · OpenAI Blog · Jul 27, 03:30

**Background**: AI tools like ChatGPT are increasingly used in workplaces for tasks such as writing, coding, and analysis. This study examines how access to such tools changes the scope of work individuals perform.

**Tags**: `#AI`, `#work`, `#ChatGPT`, `#research`

---

<a id="item-11"></a>
## [Ethan Mollick's Updated AI Guide: From Chat to Agents](https://simonwillison.net/2026/Jul/27/an-opinionated-guide-to-which-ai-to-use-to-do-stuff/#atom-everything) ⭐️ 6.0/10

Ethan Mollick released an updated opinionated guide to AI tools, shifting focus from chat-based models to agentic systems that can perform hours of human work autonomously. Notably, Gemini was dropped from the list because Google lacks a competitive product in the Codex/ChatGPT Work/Cowork category. This guide reflects a major industry shift from simple chat interfaces to agentic AI capable of executing complex, multi-step tasks, which could redefine productivity tools. The omission of Gemini highlights Google's current gap in the agentic workspace market, potentially affecting enterprise adoption. Mollick explains that ChatGPT Work and Claude Cowork are the modes for giving AI access to a computer, while Codex and Code are developer-focused coding agents. The naming is confusing: ChatGPT Work on mobile differs from the desktop app, where it acts as a skin over Codex with internet access enabled.

rss · Simon Willison · Jul 27, 21:55

**Background**: Agentic systems are AI designs that can autonomously perform tasks by using tools, accessing the internet, and executing code. ChatGPT Work and Claude Cowork are modes that allow the AI to operate on the user's computer, while Codex and Code are specialized coding agents. Gemini Spark is Google's attempt at an agentic assistant, but it has yet to prove itself in this category.

<details><summary>References</summary>
<ul>
<li><a href="https://datadrivenblogs.medium.com/when-ai-starts-acting-a-look-at-agentic-systems-d19817013a54">When AI Starts Acting: A Look at Agentic Systems | Medium</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_Spark">Gemini Spark</a></li>

</ul>
</details>

**Tags**: `#AI`, `#agentic systems`, `#LLMs`, `#tool comparison`, `#opinion`

---

<a id="item-12"></a>
## [Chinese AI Cost Advantage Widens: UBS](https://news.google.com/rss/articles/CBMimwFBVV95cUxQLWZwSUxTaURXeGhVLUdfYjlWTTFMTmNXaFhiS3ZyVVRXQ0Vvbm1DMUdhTjRkaVJQM2EyNklzSVNOZGlhTWFNM0lYTGo2WmFYaHcxZUV4YkJLV1pCQWdxdjBhQUEwOUZpVDZTYVhjU2NOdXBDMksyNlE1U3FVS21lSUF2UnpxbUxOWkdhbnhxTFh0alhZaXVPQThzOA?oc=5) ⭐️ 6.0/10

UBS Securities reports that Chinese AI companies are further widening their cost advantage over global competitors, driven by lower labor costs, efficient supply chains, and government subsidies. This cost advantage could accelerate the adoption of AI solutions in China and pressure global AI firms to reduce prices or innovate faster, potentially reshaping the competitive landscape of the AI industry. The report highlights that Chinese AI companies benefit from a 30-50% cost advantage in model training and deployment compared to US counterparts, with the gap expected to widen further as domestic hardware and software ecosystems mature.

google_news · 一财全球Yicai Global · Jul 27, 07:59

**Background**: AI development requires significant investment in computing power, data, and talent. Chinese companies have historically benefited from lower operational costs and strong government support, enabling them to offer competitive pricing while maintaining rapid iteration cycles.

**Tags**: `#AI`, `#China`, `#cost advantage`, `#finance`

---