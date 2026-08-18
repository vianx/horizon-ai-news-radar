---
layout: default
title: "Horizon Summary: 2026-08-18 (EN)"
date: 2026-08-18
lang: en
---

> From 37 items, 12 important content pieces were selected

---

1. [Mojo Programming Language Goes Open Source Under Apache 2.0](#item-1) ⭐️ 9.0/10
2. [Turbovec: Rust Implementation of Google's TurboQuant for Vector Search](#item-2) ⭐️ 8.0/10
3. [Fixing a Bricked Framework Laptop with $20 Tools](#item-3) ⭐️ 8.0/10
4. [Linux 7.3 Boosts Performance When VRAM Runs Out](#item-4) ⭐️ 8.0/10
5. [OpenAI Strengthens Frontier AI Safeguards to Pace Model Development](#item-5) ⭐️ 8.0/10
6. [Asana Completes 5 Years of Engineering Work in 2 Weeks with Codex](#item-6) ⭐️ 8.0/10
7. [Qwen 3.8 27B Scores 52 on Intelligence Index, Matching GPT-5.6 Luna](#item-7) ⭐️ 8.0/10
8. [China Orders Early Removal of Custom Windows 10 from State Agencies](#item-8) ⭐️ 8.0/10
9. [Amazon's Search Degrades into Ad Minefield](#item-9) ⭐️ 7.0/10
10. [Iceland Foods Satirizes Management Consultants](#item-10) ⭐️ 7.0/10
11. [OpenAI Launches Initiative to Strengthen Democratic Oversight of AI in National Security](#item-11) ⭐️ 7.0/10
12. [OpenAI and CodeAI Partner to Expand AI Education for Teens](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Mojo Programming Language Goes Open Source Under Apache 2.0](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

Modular has open-sourced the Mojo programming language, including its compiler and toolchain, under the Apache 2.0 license, fulfilling a promise made in May 2023. This release follows the shipping of Mojo 1.0 last week. This open-sourcing is a major milestone for the AI/ML ecosystem, as Mojo is designed to combine Python-like syntax with high performance for GPU and other accelerators. It enables broader adoption, community contributions, and potentially accelerates the development of AI infrastructure. Mojo was originally intended to be a superset of Python, but this goal was abandoned around August 2025; it is now its own language with Python-inspired syntax. The compiler is built on the MLIR framework, allowing it to target CPUs, GPUs, TPUs, and other accelerators.

rss · Simon Willison · Aug 18, 21:39

**Background**: Mojo is a systems programming language developed by Modular Inc., designed for high-performance AI infrastructure. It uses a syntax reminiscent of Python but includes features like static typing and a borrow checker, inspired by Rust. The language leverages the MLIR compiler framework to optimize for various hardware, making it particularly well-suited for AI workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language)</a></li>
<li><a href="https://www.apache.org/licenses/LICENSE-2.0">Apache License, Version 2.0 | Apache Software Foundation</a></li>
<li><a href="https://spdx.org/licenses/Apache-2.0.html">Apache License 2.0 | Software Package Data Exchange (SPDX)</a></li>

</ul>
</details>

**Discussion**: The community discussion on Lobste.rs is not provided, but based on the news, sentiment is likely positive, with excitement about the open-sourcing and potential for community-driven development. Some may express concerns about the abandonment of Python superset compatibility.

**Tags**: `#Mojo`, `#open source`, `#programming language`, `#AI/ML`, `#compiler`

---

<a id="item-2"></a>
## [Turbovec: Rust Implementation of Google's TurboQuant for Vector Search](https://github.com/RyanCodrai/turbovec) ⭐️ 8.0/10

Turbovec is a new Rust library that implements Google's TurboQuant algorithm for vector search, offering a memory-efficient and fast solution. It can fit a 10 million document corpus in 4 GB of RAM and searches faster than FAISS. This is significant because it brings a state-of-the-art vector quantization algorithm to the Rust ecosystem, enabling local and privacy-first search applications with lower memory footprint. It also provides a competitive alternative to existing tools like FAISS and Qdrant, potentially influencing the vector search landscape. Turbovec is built on TurboQuant, a data-oblivious quantizer with near-optimal distortion and no separate training phase. It includes Python bindings, and the community has expressed interest in WASM and SQLite bindings for broader use cases.

hackernews · fittingopposite · Aug 18, 18:07 · [Discussion](https://news.ycombinator.com/item?id=49349898)

**Background**: TurboQuant is an online vector quantization algorithm proposed by Google Research in 2025, which compresses high-dimensional vectors while preserving geometric structure. It is used for both KV cache compression and vector search, achieving high compression ratios with minimal accuracy loss. Vector search is a technique for finding similar items by comparing vector embeddings, commonly used in recommendation systems, semantic search, and AI applications.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/RyanCodrai/turbovec">GitHub - RyanCodrai/ turbovec : A vector index built on TurboQuant...</a></li>
<li><a href="https://lib.rs/crates/turbovec">turbovec — Rust implementation // Lib.rs</a></li>
<li><a href="https://research.google/blog/turboquant-redefining-ai-efficiency-with-extreme-compression/">TurboQuant: Redefining AI efficiency with extreme compression</a></li>

</ul>
</details>

**Discussion**: The community is excited about the memory efficiency (4GB for 10M documents) and potential for faster development workflows, with interest in SQLite bindings. Some users suggest improving the README for better adoption, while others note that Qdrant already integrates TurboQuant, reducing novelty. There is also curiosity about compiling to WASM for browser extensions.

**Tags**: `#vector search`, `#Rust`, `#TurboQuant`, `#ANN`, `#machine learning`

---

<a id="item-3"></a>
## [Fixing a Bricked Framework Laptop with $20 Tools](https://quantum5.ca/2026/08/16/fixing-bricked-amd-7040-series-framework-13-laptop-with-20-tools/) ⭐️ 8.0/10

A detailed guide was published on August 16, 2026, describing how to fix a Framework 13 laptop with an AMD 7040-series processor that was bricked by a failed BIOS update, using only $20 worth of tools instead of replacing the motherboard as suggested by Framework support. This story highlights the ongoing issue of firmware update reliability and the high cost of manufacturer-recommended repairs, potentially pushing for better accountability and more repairable designs in the laptop industry. The author used a $20 toolset to manually flash the BIOS chip, avoiding a costly motherboard replacement. The guide includes specific steps and has sparked discussion about warranty and legal liability for faulty firmware updates.

hackernews · jp_sc · Aug 18, 13:18 · [Discussion](https://news.ycombinator.com/item?id=49345220)

**Background**: Framework laptops are designed to be modular and repairable, but firmware updates can still fail and 'brick' the device, rendering it unusable. In such cases, manufacturers often recommend replacing the motherboard, which is expensive and wasteful. This guide demonstrates a low-cost alternative for technically skilled users.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.adafruit.com/2026/08/18/fixing-a-bricked-framework-laptop/">Fixing a bricked Framework laptop - Adafruit Industries</a></li>
<li><a href="https://community.frame.work/t/solved-framework-13-firmware-upgrade-brick/66763">[Solved] - Framework 13 firmware upgrade brick - Community Support - Framework Community</a></li>
<li><a href="https://community.frame.work/t/framework-laptop-16-firmware-update-bricked-my-notebook/77722">Framework laptop 16 firmware update bricked my notebook - Community Support - Framework Community</a></li>

</ul>
</details>

**Discussion**: Comments express frustration with firmware update failures and manufacturer accountability, with some suggesting legal action and others sharing similar experiences. There is also criticism of Framework's parts monopoly and stock issues, leading some to regret their purchase.

**Tags**: `#hardware`, `#firmware`, `#repair`, `#laptop`, `#Framework`

---

<a id="item-4"></a>
## [Linux 7.3 Boosts Performance When VRAM Runs Out](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

Linux kernel version 7.3 introduces performance improvements for scenarios where VRAM is exhausted, addressing memory allocation and fragmentation issues. The update aims to reduce performance degradation when GPU memory limits are exceeded. This improvement is significant for users running memory-intensive workloads like AI inference or large graphics applications, as it can prevent severe slowdowns when VRAM is full. It also highlights the Linux kernel's ongoing focus on optimizing GPU memory management, which benefits the broader open-source ecosystem. The update specifically targets virtual memory fragmentation and improves the kernel's handling of overcommitted VRAM. It is expected to be upstreamed eventually, but users on Nvidia hardware may not benefit immediately due to lack of paging support.

hackernews · flaburgan · Aug 18, 07:51 · [Discussion](https://news.ycombinator.com/item?id=49342719)

**Background**: VRAM (video RAM) is dedicated memory on a GPU used for storing textures, frame buffers, and other graphics data. When VRAM is exhausted, the system must fall back to system RAM or swap, which can cause significant performance drops. Linux kernel developers have been working on improving memory management to handle such overcommit scenarios more gracefully, including techniques like memory compaction and better allocation strategies.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nitin-rachabathuni.com/blog/linux-kernel-vram-overcommit-performance">Optimizing VRAM Overcommit: How Linux Kernel Improvements ...</a></li>
<li><a href="https://www.linuxoperatingsystem.net/linux-kernel-vram-tuning-ttm-parameters-gpus-linux/">Linux Kernel VRAM Tuning via TTM Parameters for AMD GPUs ...</a></li>
<li><a href="https://www.pingcap.com/blog/linux-kernel-vs-memory-fragmentation-1/">Memory Fragmentation in Linux : Causes, Fixes & Tools</a></li>

</ul>
</details>

**Discussion**: Community comments are generally positive, with users praising the improvement and looking forward to its upstreaming. Some users express concerns about Nvidia's lack of paging support, while others appreciate the kernel's continuous performance enhancements compared to Windows updates.

**Tags**: `#Linux`, `#kernel`, `#VRAM`, `#performance`, `#memory management`

---

<a id="item-5"></a>
## [OpenAI Strengthens Frontier AI Safeguards to Pace Model Development](https://openai.com/index/pacing-model-development-cyber-capabilities) ⭐️ 8.0/10

OpenAI announced on August 18, 2026, that it is strengthening monitoring, alignment, and security for frontier AI models, with new safeguards guiding the pace of model development. This includes a more robust monitoring system and chain-of-thought monitoring, where classifiers review the internal reasoning processes of AI models. This move signals a significant shift in how frontier AI developers balance capability advancement with safety, potentially setting a precedent for the industry. It addresses growing concerns about AI agents acting unpredictably and the need for proactive safeguards in an era of cyber-critical capabilities. The new safeguards include a more robust system for monitoring AI models, and specifically chain-of-thought monitoring, where classifiers review the internal 'thinking' processes generated by AI reasoning models. These measures are part of OpenAI's broader effort to pace model development responsibly, though the announcement lacks technical depth and detailed discussion.

rss · OpenAI Blog · Aug 18, 11:00

**Background**: AI alignment is a subfield of AI safety focused on building AI systems that behave as intended. Other subfields include robustness, monitoring, and capability control. The announcement comes amid heightened concerns about AI agents going rogue, as highlighted by WIRED's report on OpenAI overhauling safety protocols after such incidents. The new safeguards aim to address these risks by enhancing monitoring and alignment techniques.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/pacing-model-development-cyber-capabilities/">Pacing model development in an era of cyber-critical... | OpenAI</a></li>
<li><a href="https://techbeat.co/story/openai-tightens-frontier-ai-safeguards-to-pace-model-development">OpenAI Tightens Frontier AI Safeguards to Pace Model ... // Tech Beat</a></li>
<li><a href="https://www.wired.com/story/openai-overhauls-safety-protocols-after-its-ai-agents-went-rogue/">OpenAI Overhauls Safety Protocols After Its AI Agents Went... | WIRED</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#OpenAI`, `#frontier AI`, `#model development`, `#cyber security`

---

<a id="item-6"></a>
## [Asana Completes 5 Years of Engineering Work in 2 Weeks with Codex](https://openai.com/index/asana) ⭐️ 8.0/10

Asana used OpenAI Codex to replace an outdated testing system, completing an estimated five years of engineering work in just two weeks for about $12,000. This case study highlights a dramatic acceleration in software development productivity. This demonstrates the transformative potential of AI coding agents, showing that tasks previously requiring years of human effort can be completed in days. It could reshape how engineering teams allocate resources and plan projects, and may accelerate the adoption of AI-assisted development across the industry. The project involved replacing an outdated testing system, a task that would have taken five years using traditional methods. The total cost was approximately $12,000, which is significantly lower than the cost of hiring engineers for such a duration.

rss · OpenAI Blog · Aug 18, 07:00

**Background**: OpenAI Codex is an AI coding agent released in April 2025, designed to assist with software engineering tasks such as writing code, fixing bugs, and refactoring. It is available through ChatGPT, a CLI, and IDE integrations, and has gained over 5 million weekly users. AI-assisted development is moving from providing suggestions to executing entire workflows, enabling faster and more efficient software delivery.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software ... - OpenAI</a></li>
<li><a href="https://openai.com/index/codex-for-every-role-tool-workflow/">Codex for every role, tool, and workflow - OpenAI</a></li>

</ul>
</details>

**Tags**: `#AI coding`, `#OpenAI Codex`, `#software engineering`, `#productivity`, `#case study`

---

<a id="item-7"></a>
## [Qwen 3.8 27B Scores 52 on Intelligence Index, Matching GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 8.0/10

Qwen 3.8 27B, a compact open-weights model, achieved a score of 52 on the Artificial Analysis Intelligence Index, matching the score of GPT-5.6 Luna (max) and just one point behind much larger models like GLM-5.2 (753B) and DeepSeek V4 Pro (1.7T). This result was highlighted by Simon Willison on August 17, 2026. This milestone demonstrates that a relatively small, open-weights model can rival the performance of much larger proprietary models, potentially democratizing access to high-quality AI and reducing the computational resources required for advanced tasks. It could accelerate the adoption of efficient AI in resource-constrained environments and challenge the assumption that bigger models are always better. The Artificial Analysis Intelligence Index aggregates nine challenging evaluations across mathematics, science, coding, and reasoning. Qwen 3.8 27B is a native vision-language model that understands images and videos, with flexible thinking control, and can be run on a single GPU with about 56GB VRAM at BF16, ~28GB at FP8, or ~14-16GB at 4-bit quantization.

rss · Simon Willison · Aug 17, 23:58

**Background**: The Artificial Analysis Intelligence Index is a composite benchmark that provides a holistic measure of AI capabilities, updated in v4.1 to shift toward agentic workloads. Qwen is a series of open-weights models developed by Alibaba, and the 27B variant is part of the Qwen 3.8 family, which includes larger models like Qwen 3.8-Max (API-only). GPT-5.6 Luna is a cost-efficient variant in OpenAI's GPT-5.6 family, designed for high-volume workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://www.yottalabs.ai/post/qwen-3-8-27b-specs-hardware-requirements-how-to-run-2026">Qwen 3.8 27B: Specs, Hardware Requirements, and How to Run It (2026) | Yotta Labs</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion (referenced in the news item) likely includes community validation and technical debate, but no specific comments were provided in the search results. Therefore, no detailed sentiment can be summarized.

**Tags**: `#AI`, `#LLMs`, `#Qwen`, `#model efficiency`, `#open-source`

---

<a id="item-8"></a>
## [China Orders Early Removal of Custom Windows 10 from State Agencies](https://www.bloomberg.com/news/articles/2026-08-18/china-axing-microsoft-windows-from-state-agencies-ahead-of-plan) ⭐️ 8.0/10

China's Ministry of State Security has ordered some state-linked organizations to uninstall the customized Windows 10 government edition, moving up the planned retirement date from February 2027 by several months. The directive is reportedly driven by data security concerns, though no specific vulnerabilities were cited. This move signals escalating data security scrutiny in China and could accelerate the shift away from foreign operating systems in government and state-linked sectors. It may also impact Microsoft's business in China and reflect broader geopolitical tensions in technology. Microsoft stated it has found no security incidents affecting the product and that it continues to receive regular security updates. The customized Windows 10 was developed through a joint venture with China Electronics Technology Group Corporation (CETC) to meet Chinese government requirements, including keeping data within China.

telegram · zaihuapd · Aug 18, 06:22

**Background**: In 2016, Microsoft partnered with China Electronics Technology Group Corporation (CETC) to create a joint venture, C&M Information Technology, to develop a customized Windows 10 for the Chinese government. This version removed features like OneDrive and entertainment, and ensured data stayed within China, with local activation, patching, and updates managed by the joint venture. The early retirement of this version reflects growing concerns over data security and self-reliance in technology.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/software/operating-systems/china-reportedly-orders-state-agencies-to-uninstall-its-government-only-edition-of-windows-10">China reportedly orders state agencies to uninstall its ...</a></li>
<li><a href="https://news.mydrivers.com/1/533/533778.htm">中国定制政府版Windows 10是这样：数据不出境</a></li>
<li><a href="https://www.techspot.com/news/113529-china-finally-pulling-windows-10-government-machines-ahead.html">China pulls the plug on Windows 10 for government machines ...</a></li>

</ul>
</details>

**Tags**: `#China`, `#Microsoft`, `#Windows 10`, `#data security`, `#geopolitics`

---

<a id="item-9"></a>
## [Amazon's Search Degrades into Ad Minefield](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 7.0/10

Seth Godin's blog post 'The Amazon tax' criticizes Amazon's search experience, noting that results are increasingly dominated by sponsored ads, making it hard to find specific products. The post has sparked a wide discussion with 835 points and 507 comments on Hacker News. This highlights a significant shift in Amazon's platform incentives, prioritizing ad revenue over user experience, which could drive users to alternative platforms and erode customer trust. It also raises broader concerns about the degradation of search quality in large tech platforms. Community comments report that roughly 3/4 of Amazon search results are sponsored ads, and users feel the platform nudges them toward products it wants to sell, not what they searched for. Some users are considering deleting their long-standing Amazon accounts due to the degraded experience.

hackernews · herbertl · Aug 18, 13:22 · [Discussion](https://news.ycombinator.com/item?id=49345263)

**Background**: Amazon has evolved from a product search engine to an advertising platform, where sponsored results often outrank organic ones. This shift is part of a broader trend where tech companies prioritize ad revenue, potentially compromising user experience and trust.

**Discussion**: The discussion reflects widespread frustration with Amazon's search quality, with users sharing personal experiences of ad saturation and considering alternatives. Some commenters suggest legal avenues like trademark infringement or fraud to challenge Amazon's ad practices, while others note this is a common issue across platforms.

**Tags**: `#Amazon`, `#e-commerce`, `#search`, `#advertising`, `#user experience`

---

<a id="item-10"></a>
## [Iceland Foods Satirizes Management Consultants](https://about.iceland.co.uk/our-story/the-dark-ages/beware-management-consultants/) ⭐️ 7.0/10

Iceland Foods published a satirical slideshow titled 'Beware Management Consultants' on its website, humorously critiquing the role and incentives of management consultants in business. The satire resonates with many in the tech and business communities, sparking discussions about the value and incentives of consultants. It highlights a widespread skepticism toward consulting practices and their impact on organizational behavior. The slideshow intentionally uses bad UX to engage readers, as noted in community comments. It also references the company's trademark dispute with Iceland the country, adding a layer of inside humor.

hackernews · KolmogorovComp · Aug 18, 19:29 · [Discussion](https://news.ycombinator.com/item?id=49351324)

**Background**: Management consultants are often hired to provide expert advice on business strategy and operations, but their incentives can be misaligned with long-term company health. Iceland Foods, a UK supermarket chain, is known for its quirky marketing and has previously been involved in a legal battle with the Icelandic government over the use of the name 'Iceland'.

**Discussion**: Community comments express amusement and agreement with the critique, with some noting the intentional bad UX as a clever engagement tactic. Others reflect on their own roles in similar governance or consulting functions, questioning whether they are part of the problem.

**Tags**: `#management consulting`, `#satire`, `#business`, `#organizational behavior`, `#UX`

---

<a id="item-11"></a>
## [OpenAI Launches Initiative to Strengthen Democratic Oversight of AI in National Security](https://openai.com/index/strengthening-democratic-oversight-in-national-security) ⭐️ 7.0/10

OpenAI announced a new initiative on August 18, 2026, to support government institutions with tools, training, and expertise for democratic oversight of AI in national security. The initiative includes a $5 million commitment in training, technical support, and OpenAI credits. This initiative is significant because it addresses the growing need for democratic accountability in the use of AI for national security, a domain often shrouded in secrecy. It could set a precedent for how AI companies engage with governments, promoting transparency and public trust while mitigating risks of misuse. The initiative commits $5 million to provide training, technical support, and OpenAI credits to government oversight bodies. It builds on OpenAI's previously stated principles for government and national security partnerships, emphasizing democratic accountability and public safety.

rss · OpenAI Blog · Aug 18, 19:00

**Background**: AI technologies are increasingly used in national security contexts, raising concerns about oversight and democratic control. OpenAI, as a leading AI company, has been developing policies to ensure responsible use of its technology, including partnerships with government entities. This initiative aims to equip oversight bodies with the necessary tools and knowledge to effectively monitor AI applications in sensitive areas.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/openai-puts-5m-behind-ai-training-and-tools-for-national-security-oversight-bodies/">OpenAI Puts $5M Behind AI Training and Tools for National ...</a></li>
<li><a href="https://openai.com/index/government-national-security-partnerships/">Our approach to government and national security partnerships</a></li>

</ul>
</details>

**Tags**: `#AI governance`, `#national security`, `#OpenAI`, `#policy`, `#democratic oversight`

---

<a id="item-12"></a>
## [OpenAI and CodeAI Partner to Expand AI Education for Teens](https://openai.com/index/chatgpt-for-teens/) ⭐️ 6.0/10

On August 18, 2026, OpenAI announced a partnership with CodeAI (formerly Code.org) to promote responsible AI education for students and teachers, coinciding with the launch of ChatGPT for Teens, which includes enhanced safety features and parental controls. Over the next year, the collaboration aims to reach millions of students through joint advisory councils, AI literacy courses, student challenges, and career programs. This partnership is significant as it expands AI literacy to a younger demographic, potentially shaping how a generation learns to interact with AI responsibly. It also marks OpenAI's strategic move into the education sector, leveraging CodeAI's extensive school network to integrate AI education into classrooms, which could influence future AI adoption and policy. ChatGPT for Teens includes age-appropriate safety measures, parental controls, and learning tools designed to prevent harmful content and academic dishonesty. The partnership also supports CodeAI in developing a free high school AI Foundations course, and CodeAI has rebranded from Code.org to reflect its expanded focus on AI education.

telegram · OpenAI Blog · Aug 18, 12:06

**Background**: CodeAI, formerly known as Code.org, is a nonprofit organization dedicated to expanding access to computer science and AI education in schools. The rebranding to CodeAI reflects a strategic shift after AI disrupted its original mission. ChatGPT for Teens is a version of OpenAI's chatbot tailored for users under 18, with built-in protections and parental controls to address safety concerns.

<details><summary>References</summary>
<ul>
<li><a href="https://code.org/en-US/codeai">Code.org is now CodeAI</a></li>
<li><a href="https://code.org/en-US/about">About CodeAI – Our Mission, Impact, and Approach | CodeAI</a></li>
<li><a href="https://techcrunch.com/2026/08/18/openai-launches-a-safer-chatgpt-for-teens-years-after-teens-started-using-it/">OpenAI launches a safer ChatGPT for teens — years after teens started using it | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI education`, `#ChatGPT`, `#partnership`, `#teenagers`

---