---
layout: default
title: "Horizon Summary: 2026-08-15 (EN)"
date: 2026-08-15
lang: en
---

> From 36 items, 7 important content pieces were selected

---

1. [Doom Renderer Compiled into 21B-Parameter Transformer Without Training](#item-1) ⭐️ 9.0/10
2. [Qwen 3.8 27B: Strong Local LLM with Community Validation](#item-2) ⭐️ 8.0/10
3. [Going Dark and the Shift to Law Enforcement Hacking](#item-3) ⭐️ 8.0/10
4. [RustDesk Adds True Unattended Access on Wayland](#item-4) ⭐️ 8.0/10
5. [Firefox is now the last major browser supporting uBlock Origin](#item-5) ⭐️ 8.0/10
6. [AI Robotic Labs Test 3M Human Tissue Samples Yearly, Could End Animal Testing](#item-6) ⭐️ 8.0/10
7. [Don't Classify, Hallucinate: A New Tagging Technique](#item-7) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Doom Renderer Compiled into 21B-Parameter Transformer Without Training](https://www.reddit.com/r/MachineLearning/comments/1voazhm/i_compiled_dooms_renderer_into_a_21bparameter/) ⭐️ 9.0/10

The author ported Doom's rendering algorithm into a computation graph and used a custom compiler, torchwright, to convert it into the weights of a 21B-parameter transformer checkpoint. The model generates pixel-drawing commands that reproduce the game's E1M1 frame when executed. This demonstrates a novel approach to embedding complex algorithms into neural network weights without training, potentially enabling new ways to program and control transformers. It could inspire further research into compiling arbitrary computations into models, bridging traditional software and neural computation. The generated checkpoint is a standard transformers checkpoint loadable without trust_remote_code. Rendering one frame requires a 3,614-token prompt and generates 53,747 tokens, taking about 40 minutes on a B200 GPU, achieving roughly 35 frames per day compared to Doom's original 35 FPS on a 486.

reddit · r/MachineLearning · /u/notforrob · Aug 14, 15:50

**Background**: Transformers are neural network architectures that process sequences using attention mechanisms, typically trained on large datasets. Compiling computation graphs into transformer weights is an emerging technique where a program's logic is encoded directly into the model's parameters, allowing the model to execute the program during inference. Doom's renderer uses algorithms like binary space partitioning (BSP) to efficiently draw 3D scenes, which the author ported into a graph representation.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/physicsrob/torchwright">physicsrob/torchwright: A compiler that transforms computation ...</a></li>
<li><a href="https://www.doomwiki.org/wiki/Rendering_engine">Doom rendering engine - The Doom Wiki at DoomWiki.org</a></li>

</ul>
</details>

**Tags**: `#transformer`, `#compilation`, `#Doom`, `#neural networks`, `#AI`

---

<a id="item-2"></a>
## [Qwen 3.8 27B: Strong Local LLM with Community Validation](https://huggingface.co/Qwen/Qwen3.8-27B-FP8) ⭐️ 8.0/10

Qwen 3.8 27B is a newly released local large language model that demonstrates strong reasoning and performance, with community members reporting successful benchmarks and efficient inference on consumer hardware. It is the successor to Qwen3.6-27B, carrying the 3.8 generation's training improvements to a self-hostable scale. This release is significant for the local LLM community as it offers a high-performing model that can run on consumer hardware, potentially democratizing access to advanced AI capabilities. The community's positive reception and practical insights on inference engines indicate strong engagement and validation, which could influence future model development and adoption. Community benchmarks show significant improvements over the previous version, with Terminal-Bench 2.1 rising from 63.4 to 73.0, DeepSWE 1.1 from 13.3 to 42.2, OSWorld-Verified from 63.9 to 84.3, and SWE-MM from 25.7 to 38.6. However, Alibaba has not yet published architecture details (dense or MoE), context length, or a license, and some users report less efficient VRAM usage compared to other models.

hackernews · erdaltoprak · Aug 14, 15:00 · [Discussion](https://news.ycombinator.com/item?id=49299605)

**Background**: Qwen is a series of large language models developed by Alibaba, known for their strong performance and open-source availability. Local LLMs are models that can run on consumer hardware, such as laptops or desktop GPUs, without relying on cloud services. This is made possible through techniques like quantization and efficient inference engines, which reduce memory usage and improve speed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.yottalabs.ai/post/qwen-3-8-27b-specs-hardware-requirements-how-to-run-2026">Qwen 3.8 27B: Specs, Hardware Requirements, and How to Run It (2026) | Yotta Labs</a></li>
<li><a href="https://kingy.ai/blog/qwen3-8-27b-specs-benchmarks-local-hardware/">Qwen3.8-27B: Specs, Benchmarks & Verdict</a></li>
<li><a href="https://medium.com/practical-llm-systems/qwen-3-8-benchmarks-what-the-numbers-actually-say-4eeb8885ce70">Qwen 3.8 Benchmarks: What the Numbers Actually Say | by Rost Glukhov | Practical LLM Systems | Aug, 2026 | Medium</a></li>

</ul>
</details>

**Discussion**: Community members are generally impressed with the model's reasoning capabilities, with one user noting it is only the second local model to correctly reason through a private benchmark. Others report high token generation speeds using alternative inference engines, and some observe a distinctive change in the model's thinking trace style compared to previous versions. There are also concerns about VRAM efficiency and speculation that the unique thinking pattern may affect multi-token prediction performance.

**Tags**: `#LLM`, `#local-models`, `#AI`, `#open-source`, `#benchmarks`

---

<a id="item-3"></a>
## [Going Dark and the Shift to Law Enforcement Hacking](https://blog.cryptographyengineering.com/2026/08/14/everything-is-about-to-go-dark/) ⭐️ 8.0/10

The article analyzes the 'going dark' problem and argues that law enforcement is increasingly turning to hacking techniques, such as exploiting software vulnerabilities, to access encrypted communications. It suggests that the era of mass surveillance through legal requests may be ending, replaced by targeted hacking operations. This shift has significant implications for privacy, security, and the balance of power between governments and citizens. As law enforcement hacking becomes more common, it raises questions about the limits of vulnerability exploitation and the potential for abuse, affecting policymakers, security researchers, and the public. The article notes that the number of useful software bugs may hit a ceiling, limiting the effectiveness of hacking as a law enforcement tool. It also discusses the costs and practical challenges of running wiretaps, contrasting past physical wiretapping with modern digital surveillance.

hackernews · vslira · Aug 14, 20:52 · [Discussion](https://news.ycombinator.com/item?id=49304447)

**Background**: The 'going dark' problem refers to the difficulty law enforcement faces in accessing encrypted communications and data, even with lawful court orders. As encryption becomes widespread, agencies have explored hacking techniques, such as deploying malware or exploiting vulnerabilities, to bypass encryption. This trend is part of a broader debate over privacy versus security, with agencies like the FBI advocating for lawful access while privacy advocates warn against weakening encryption.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theiacp.org/resources/critical-issues-encryption-going-dark">Critical Issues: Encryption & Going Dark</a></li>
<li><a href="https://carnegieendowment.org/research/2024/04/exploring-law-enforcement-hacking-as-a-tool-against-transnational-cyber-crime">Exploring Law Enforcement Hacking as a Tool Against Transnational Cyber ...</a></li>
<li><a href="https://observed.org/can-police-use-hacking-techniques/">Can Police Use Hacking Techniques? | Know Your Rights</a></li>

</ul>
</details>

**Discussion**: Commenters expressed mixed views: some highlighted the historical costs of wiretapping, while others doubted that software bugs are decreasing, citing AI-generated code introducing more vulnerabilities. A sarcastic comment criticized government surveillance, and another noted the contrast between sophisticated law enforcement hacking and poor security practices in many organizations.

**Tags**: `#encryption`, `#law enforcement`, `#surveillance`, `#security`, `#privacy`

---

<a id="item-4"></a>
## [RustDesk Adds True Unattended Access on Wayland](https://rustdesk.com/blog/unattended-remote-access-wayland/) ⭐️ 8.0/10

RustDesk has announced support for true unattended remote access on Wayland, a highly requested feature for Linux users. A preview build for x86_64 Debian/Ubuntu-based systems is now available, with multi-monitor support. This update addresses a long-standing pain point for Linux users who rely on Wayland, as previous solutions often required manual screen selection or failed on locked sessions. It enhances RustDesk's competitiveness as an open-source remote desktop tool, potentially attracting more users from VNC and proprietary alternatives. The feature is currently available as a preview build for x86_64 Debian/Ubuntu-based systems, and it includes multi-monitor support. Users should note that this is a preview, so stability and compatibility may vary across different Wayland compositors.

hackernews · rustdesk · Aug 14, 16:12 · [Discussion](https://news.ycombinator.com/item?id=49300759)

**Background**: Wayland is a display server protocol that has become the default on many modern Linux distributions, replacing the older X11. Unlike X11, Wayland restricts applications from capturing the entire screen without explicit user permission, which historically made unattended remote access difficult. RustDesk is an open-source remote desktop tool that allows users to access and control computers remotely, similar to TeamViewer or AnyDesk.

<details><summary>References</summary>
<ul>
<li><a href="https://rustdesk.com/blog/unattended-remote-access-wayland/">Unattended Remote Access on Wayland with RustDesk</a></li>
<li><a href="https://github.com/rustdesk/rustdesk/discussions/10016">Wayland: Select the screen to be shared (Operate on the peer ...</a></li>
<li><a href="https://stackademic.com/blog/remote-desktop-on-wayland-in-2025-what-changed-for-linux-support-engineers">Remote Desktop on Wayland in 2025: What Changed for Linux ...</a></li>

</ul>
</details>

**Discussion**: Community members expressed enthusiasm for the update, with one user noting they had just encountered the issue two days prior. Others raised questions about RustDesk's encryption when self-hosting, comparisons with VNC for specific use cases, and how it stacks up against solutions like Remmina over SSH and Tailscale.

**Tags**: `#RustDesk`, `#Wayland`, `#remote desktop`, `#open source`, `#Linux`

---

<a id="item-5"></a>
## [Firefox is now the last major browser supporting uBlock Origin](https://www.pcworld.com/article/3212428/firefox-is-now-the-last-major-browser-that-still-supports-ublock-origin.html) ⭐️ 8.0/10

Firefox is now the only major browser that still fully supports uBlock Origin, following Chrome's transition to Manifest V3 which limits the extension's capabilities. This shift marks a significant change in the ad-blocking landscape. This matters because uBlock Origin is widely regarded as one of the most powerful ad blockers, and its reduced functionality on Chrome affects millions of users who rely on it for privacy and ad blocking. It also highlights the growing tension between browser vendors and user control over web content. Manifest V3 restricts extensions to a maximum of 30,000 rules, while effective ad blockers often need over 300,000 rules. uBlock Origin relies on the webRequest API and dynamic filtering, which are severely limited under MV3, forcing a pared-down 'uBlock Origin Lite' on Chromium browsers.

hackernews · DemiGuru · Aug 14, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49303202)

**Background**: Manifest V3 is the latest extension specification for Chromium-based browsers, defining what extensions can and cannot do. It replaces the powerful webRequest API with a less capable declarativeNetRequest API, which limits how ad blockers can inspect and block network requests. This change was introduced by Google, which also owns a major advertising business, raising concerns about conflicts of interest.

<details><summary>References</summary>
<ul>
<li><a href="https://adblock-tester.com/ad-blockers/manifest-v3-ad-blocker-impact/">The Manifest V3 Changes — Did Google Just Break Your Ad Blocker? (And What to Do Next) - AdBlock Tester</a></li>
<li><a href="https://www.techradar.com/pro/how-chromes-manifest-v3-will-change-the-game-for-ad-blockers">How Chrome’s Manifest V3 will change the game for ad blockers | TechRadar</a></li>
<li><a href="https://nordvpn.com/blog/manifest-v3-ad-blockers/">Is Google's Manifest V3 the end of ad blockers? | NordVPN</a></li>

</ul>
</details>

**Discussion**: Community comments express appreciation for Firefox's vetting of popular extensions like uBlock Origin, and criticism of Google's advertising-driven decisions. Some users note that uBlock Origin Lite works adequately for them, while others lament the loss of full-featured ad blocking on Chrome.

**Tags**: `#Firefox`, `#uBlock Origin`, `#ad-blocking`, `#Manifest V3`, `#privacy`

---

<a id="item-6"></a>
## [AI Robotic Labs Test 3M Human Tissue Samples Yearly, Could End Animal Testing](https://www.fastcompany.com/91589344/the-worlds-largest-biological-datacenter-could-help-make-animal-testing-obsolete) ⭐️ 8.0/10

Vivodyne has launched the world's largest human biological datacenter in South San Francisco, featuring 12 robotic 'hive' labs that can conduct over 3 million controlled experiments on human tissues annually. This capacity is twice the total of all U.S. clinical trials combined. This development could significantly reduce reliance on animal testing in drug development, addressing the high failure rate of clinical trials (about 90% fail after animal tests). It may accelerate drug discovery and improve the predictability of drug efficacy and safety in humans. Vivodyne raised $40 million in Series A financing to scale its robotics and AI approach. The system uses AI-designed experiments on lab-grown, fully functional human tissues, aiming to make human biology computable at AI scale.

telegram · zaihuapd · Aug 14, 01:48

**Background**: Animal testing has long been the standard for evaluating new drugs before human trials, but it is expensive and often fails to predict human responses. Advances in tissue engineering and microfluidic chips have led to human tissue models that may better mimic human physiology. AI and robotics are now being applied to automate and scale these models, potentially offering a more ethical and efficient alternative to animal testing.

<details><summary>References</summary>
<ul>
<li><a href="https://svdaily.com/2025/06/02/vivodyne-raises-40-million-to-open-lab-in-south-san-francisco/">Vivodyne Raises $40 Million to Open Lab in South San ...</a></li>
<li><a href="https://finance.yahoo.com/healthcare/articles/vivodyne-launches-world-largest-human-130000478.html?fr=sycsrp_catchall">Vivodyne Launches the World’s Largest Human Biological ...</a></li>
<li><a href="https://www.linkedin.com/pulse/vivodyne-lands-40m-replace-animal-testing-drug-phil-newman-gihge/">Vivodyne lands $40m to replace animal testing in drug development</a></li>

</ul>
</details>

**Tags**: `#AI`, `#biotech`, `#drug discovery`, `#lab automation`, `#animal testing`

---

<a id="item-7"></a>
## [Don't Classify, Hallucinate: A New Tagging Technique](https://simonwillison.net/2026/Aug/14/dont-classify-hallucinate/) ⭐️ 7.0/10

Doug Turnbull proposed a technique where an LLM generates novel tags without seeing the existing vocabulary, then vector embeddings match these imagined tags to the closest real tags. Simon Willison highlighted this approach on his blog, noting its practicality for tagging untagged content. This technique solves the scalability problem of feeding thousands of tags to an LLM, enabling efficient and accurate tagging for large content repositories. It leverages LLM creativity and embedding similarity, offering a practical approach for developers in information retrieval and content management. The example prompt includes sample tag shapes to guide the model, such as 'Furniture / Living Room Furniture / Coffee Tables & End Tables / Coffee Tables'. The matching step uses vector embeddings to find the closest existing tags, avoiding the need to feed the entire tag list to the LLM.

rss · Simon Willison · Aug 14, 21:54

**Background**: LLM hallucination typically refers to generating false or fabricated information, but here it is repurposed as a creative generation step. Vector embeddings represent the meaning of text as numerical vectors, allowing semantic similarity comparison. This technique combines these concepts to map novel tags to an existing taxonomy.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2306.06085">Trapping LLM Hallucinations Using Tagged Context Prompts Trapping LLM “Hallucinations” Using Tagged Context Prompts Detecting and Correcting Hallucinations in LLMs via ... Detecting hallucinations in large language models using ... Detecting hallucinations with LLM-as-a-judge: Prompt ... 5 Practical Techniques to Detect and Mitigate LLM ... LLM Hallucinations: What They Are & How to Detect Them</a></li>
<li><a href="https://hackernoon.com/automating-content-tagging-in-laravel-using-openai-embeddings-and-cron-jobs">Automating Content Tagging in Laravel Using OpenAI Embeddings ...</a></li>
<li><a href="https://www.ibm.com/think/topics/vector-embedding">What is Vector Embedding ? | IBM</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#embeddings`, `#tagging`, `#information retrieval`, `#AI`

---