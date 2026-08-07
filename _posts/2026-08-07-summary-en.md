---
layout: default
title: "Horizon Summary: 2026-08-07 (EN)"
date: 2026-08-07
lang: en
---

> From 38 items, 10 important content pieces were selected

---

1. [Making Postgres 300x Faster for Analytics with Batching, Fusion, and SIMD](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Flash 0731: Faster, Cheaper, and More Capable](#item-2) ⭐️ 8.0/10
3. [Assembly Hall of Shame: A Collection of Bizarre x86 Instructions](#item-3) ⭐️ 8.0/10
4. [Tech Worker Disillusionment: What Happens When an Entire Class Loses Faith](#item-4) ⭐️ 8.0/10
5. [OpenAI Unveils Cyber Security Measures for Astra Model](#item-5) ⭐️ 8.0/10
6. [Oracle Bans AI-Generated Code from OpenJDK](#item-6) ⭐️ 8.0/10
7. [SDSS DR20 Maps 500,000 Supermassive Black Holes Across the Sky](#item-7) ⭐️ 8.0/10
8. [Codex with GPT-5.6 Sol Ultra Outshines Claude Fable 5 in Raccoon Heist Game](#item-8) ⭐️ 7.0/10
9. [Tokenpocalypse: Companies Scramble to Cut AI Spending](#item-9) ⭐️ 7.0/10
10. [China's Tech Giants Accelerate AI Talent Hiring](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Making Postgres 300x Faster for Analytics with Batching, Fusion, and SIMD](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 9.0/10

The author of pgrust, a Rust-based reimplementation of PostgreSQL, details how they achieved hundreds of times speedup for analytical queries by optimizing the query engine using batching, operator fusion, and SIMD. They also emphasize correctness through formal verification and differential testing, having proven over 1000 user-facing functions equivalent to Postgres. This work demonstrates that significant performance gains are possible for Postgres-compatible systems, potentially offering a path for users needing faster analytics without abandoning the Postgres ecosystem. It also highlights the viability of adaptive planning and modern optimization techniques that the Postgres core team has been reluctant to adopt, which could influence future database development. The optimizations focus on reducing CPU and memory bandwidth usage in the query engine. The author mentions formal verification and differential fuzz testing to ensure correctness, with proofs available in a dedicated directory. The project is called pgrust, and the post includes a discussion of the IO scheduler and thread scheduler, addressing the 'noisy neighbor' problem.

hackernews · poly2it · Aug 7, 11:00 · [Discussion](https://news.ycombinator.com/item?id=49208535)

**Background**: PostgreSQL is a widely used open-source relational database, but its query engine is not optimized for analytical workloads that process large volumes of data. Techniques like batching (processing multiple rows at once), operator fusion (combining multiple operations to reduce overhead), and SIMD (Single Instruction, Multiple Data) are common in modern analytical databases to improve performance. Differential testing is a software testing technique that compares outputs of different implementations to find bugs, and formal verification uses mathematical proofs to ensure correctness.

<details><summary>References</summary>
<ul>
<li><a href="https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/">Rebuilding Postgres for 300x faster analytics: batching, operator ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Differential_testing">Differential testing - Wikipedia</a></li>
<li><a href="https://quadric.ai/blog/operator-fusion-npu-ai-compilers-on-device">Operator Fusion in NPUs: How AI Compilers... | Quadric Blog</a></li>

</ul>
</details>

**Discussion**: The author actively participated in the discussion, addressing trust concerns by highlighting their focus on correctness through formal verification and differential testing. Some commenters expressed skepticism about adoption, noting that trust in the Postgres team and long-term continuity are crucial. Others showed enthusiasm for adaptive planning, which the Postgres core team has been reluctant to implement, and asked for more details on the IO scheduler and thread scheduler.

**Tags**: `#Postgres`, `#database`, `#performance`, `#SIMD`, `#query-engine`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731: Faster, Cheaper, and More Capable](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek released the V4 Flash 0731 model on July 31, 2025, an updated version of its V4 Flash line that offers significant performance improvements, higher speed, and better cost-effectiveness. Community testing shows it outperforms the previous preview and even the V4 Pro (Preview) on several benchmarks despite a smaller activated parameter count. This release strengthens DeepSeek's position in the competitive AI model market by offering a highly capable model at a very low cost, making advanced AI accessible to more developers and businesses. Its strong agentic coding performance and 1M-token context window could shift adoption away from more expensive proprietary models. The model features a 1M-token context window and adjustable reasoning effort, making it suitable for agentic coding tasks. Community benchmarks show it achieves ~8k tokens/s prefill and ~250 tokens/s on a single stream on 2x RTX Pro 6000 Blackwell hardware, with users reporting costs under $5 per day even with heavy usage.

hackernews · tosh · Aug 7, 17:56 · [Discussion](https://news.ycombinator.com/item?id=49214008)

**Background**: DeepSeek is a Chinese AI company known for releasing open-weight models that rival proprietary counterparts. The V4 Flash series is designed to balance performance and efficiency, offering a smaller, faster, and cheaper alternative to the full V4 models. The 0731 update follows an earlier preview release and is now available on platforms like Hugging Face, ModelScope, and Together AI.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek -ai/ DeepSeek - V 4 - Flash - 0731 · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.together.ai/models/deepseek-v4-flash-0731">DeepSeek V 4 Flash 0731 API | Together AI</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely positive, with users praising the model's speed, capability, and cost-effectiveness. Some users noted issues like infinite loops and token waste in agentic tasks, and there are concerns about an upcoming price increase announced by DeepSeek.

**Tags**: `#AI`, `#DeepSeek`, `#LLM`, `#Machine Learning`, `#Model Release`

---

<a id="item-3"></a>
## [Assembly Hall of Shame: A Collection of Bizarre x86 Instructions](https://github.com/xoreaxeaxeax/asm-hall-of-shame) ⭐️ 8.0/10

A new GitHub repository, 'Assembly Hall of Shame', curates a collection of bizarre and slow x86 instructions, showcasing obscure CPU behaviors. It has gained significant attention with 222 points and 45 comments on Hacker News. This resource is valuable for low-level programmers and security researchers, as it highlights unusual instructions that can have performance and security implications. It fosters community discussion on obscure CPU features and their potential exploitation. The repository includes a leaderboard of slow instructions, with a notable example being a 12ms write to an ACPI IO port, which may trap to SMM. The rules exclude trapped/emulated/virtualized instructions from timing, but some entries may still involve such handling.

hackernews · piotrgrabowski · Aug 7, 18:01 · [Discussion](https://news.ycombinator.com/item?id=49214098)

**Background**: x86 is a complex instruction set architecture (ISA) with many legacy and obscure instructions. Some instructions are rarely used but can exhibit surprising behavior, such as extremely high latency or unusual side effects. Understanding these can be important for performance optimization and security research.

<details><summary>References</summary>
<ul>
<li><a href="https://hackaday.com/2021/02/25/oddball-x86-instructions/">Oddball X 86 Instructions | Hackaday</a></li>
<li><a href="https://en.wikipedia.org/wiki/TEST_(x86_instruction)">TEST ( x 86 instruction ) - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=10276384">Here's something to ponder: security implications of... | Hacker News</a></li>

</ul>
</details>

**Discussion**: Community comments highlight related projects, such as using slow instructions to break SMI, and draw parallels to Core War. Some users humorously suggest that 'nop' should be #1 for being infinitely slow relative to its purpose, while others note that certain entries may involve SMM handling.

**Tags**: `#assembly`, `#x86`, `#low-level`, `#security`, `#obscure instructions`

---

<a id="item-4"></a>
## [Tech Worker Disillusionment: What Happens When an Entire Class Loses Faith](https://www.noemamag.com/why-is-everyone-in-tech-so-sad/) ⭐️ 8.0/10

An article on Noema Magazine explores the widespread sadness and loss of faith among tech workers, sparking a large community discussion on Hacker News with 349 points and 485 comments. The piece questions the sustainability of a career path that has become synonymous with toxicity and uncertainty. This matters because tech workers are a critical workforce driving innovation and economic growth; their widespread disillusionment could lead to reduced productivity, talent drain, and a less innovative industry. It also highlights a broader societal issue about the mental health and well-being of knowledge workers in high-pressure industries. The article and discussion reference the toxic nature of online culture, the contrast between the 1990s and 2020s internet experiences, and historical analogies like the decline of the printing trade. Commenters share personal stories of burnout and disillusionment, with some expressing a desire to escape the industry entirely.

hackernews · RickJWagner · Aug 7, 12:42 · [Discussion](https://news.ycombinator.com/item?id=49209539)

**Background**: The tech industry has long been seen as a desirable career path, offering high salaries and opportunities for innovation. However, recent years have seen increasing reports of burnout, layoffs, and a toxic work culture, leading to a growing sense of disillusionment among workers. This article taps into that sentiment, questioning the future of tech careers and the industry's impact on workers' mental health.

**Discussion**: The community discussion is deeply engaged, with commenters drawing parallels to the decline of the printing trade and noting the toxic nature of the modern web. Some express personal burnout and a loss of passion, while others find the article's tone off-putting but acknowledge the societal importance of the conversation.

**Tags**: `#tech industry`, `#worker morale`, `#career disillusionment`, `#mental health`, `#online culture`

---

<a id="item-5"></a>
## [OpenAI Unveils Cyber Security Measures for Astra Model](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/) ⭐️ 8.0/10

OpenAI has released preliminary cybersecurity evaluations for its upcoming Astra model, indicating it may reach 'critical' cyber capability thresholds, and announced stricter security controls including isolated testing environments. This announcement is significant as it highlights the growing role of AI in cybersecurity, both as a defensive tool and a potential offensive threat. It underscores the need for robust safety measures as AI models become more capable, impacting developers, security researchers, and the broader AI ecosystem. The evaluation results were strong enough that OpenAI could not rule out Astra reaching 'critical' cyber capability. OpenAI is implementing stricter security controls for higher-capability models, including isolated testing environments, and plans to expand security testing, which may delay the model's release.

hackernews · OpenAI Blog · Aug 7, 16:39 · [Discussion](https://news.ycombinator.com/item?id=49213029)

**Background**: AI models are increasingly being used for vulnerability discovery and exploitation, as seen in recent reports of AI-driven penetration testing frameworks. However, the reliability of AI-discovered vulnerabilities is debated, with some reports showing high false positive rates. OpenAI's announcement reflects the dual-use nature of advanced AI in cybersecurity, necessitating careful evaluation and safeguards.

<details><summary>References</summary>
<ul>
<li><a href="https://cloud.google.com/blog/topics/threat-intelligence/ai-vulnerability-exploitation-initial-access">Adversaries Leverage AI for Vulnerability Exploitation, Augmented Operations, and Initial Access | Google Cloud Blog</a></li>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>
<li><a href="https://www.akamai.com/blog/security-research/ai-vulnerability-discovery-human-oversight-caution">AI in Vulnerability Discovery: A Call for Human Oversight and Caution | Akamai</a></li>

</ul>
</details>

**Discussion**: Community comments express a mix of interest and skepticism. Some users share positive experiences with AI in vulnerability discovery, while others criticize OpenAI's lack of transparency about past incidents and question the effectiveness of stricter controls. There is also a sentiment of distrust towards companies handling AI models, with some suggesting moving data back on-premises.

**Tags**: `#AI safety`, `#cybersecurity`, `#OpenAI`, `#vulnerability research`, `#AI agents`

---

<a id="item-6"></a>
## [Oracle Bans AI-Generated Code from OpenJDK](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

Oracle has implemented an interim policy banning AI-generated code contributions to OpenJDK, citing legal and review burden concerns. The policy was approved by the OpenJDK Governing Board and is detailed on the OpenJDK legal page. This decision affects OpenJDK, a widely-used open-source project that serves as the reference implementation of Java, potentially impacting many businesses and developers. It highlights the growing tension between AI-assisted development and open-source governance, especially regarding copyright and provenance. The interim policy does not explain why Oracle allows AI-generated code for internal products but prohibits it for OpenJDK contributions. The final policy is being drafted by Oracle's lawyers, and the interim measure aims to reduce the burden on human reviewers.

hackernews · delduca · Aug 7, 17:36 · [Discussion](https://news.ycombinator.com/item?id=49213754)

**Background**: OpenJDK is the open-source reference implementation of Java, developed by a community of contributors and overseen by Oracle. AI-generated code raises legal questions about copyright and open-source license compliance, as the law on AI-generated works is still evolving. Oracle's decision reflects concerns about the provenance of code and the potential legal risks for a project central to many businesses.

<details><summary>References</summary>
<ul>
<li><a href="https://www.infoq.com/news/2026/06/oracle-genai-policies/">Oracle's OpenJDK Bans Generative AI Contributions While ...</a></li>
<li><a href="https://www.techzine.eu/news/devops/143395/oracle-bans-ai-generated-contributions-to-openjdk/">Oracle bans AI-generated contributions to OpenJDK</a></li>
<li><a href="https://openjdk.org/bylaws">Bylaws - OpenJDK</a></li>

</ul>
</details>

**Discussion**: Community comments express mixed reactions: some see it as a sensible precaution given Java's copyright history, while others find it ironic that Oracle embraces AI internally but bans it externally. There is also confusion about Oracle's role in OpenJDK development, with one commenter mistakenly believing it was purely community-driven.

**Tags**: `#OpenJDK`, `#AI-generated code`, `#Open source policy`, `#Oracle`, `#Legal`

---

<a id="item-7"></a>
## [SDSS DR20 Maps 500,000 Supermassive Black Holes Across the Sky](https://www.sdss.org/black-hole-mapper-release-20/) ⭐️ 8.0/10

The Sloan Digital Sky Survey (SDSS) released its twentieth data release (DR20), featuring an all-sky map of 500,000 supermassive black holes. Concurrently, the eROSITA X-ray survey released its second half-sky catalog, nearly doubling the known X-ray sources to 2 million. This data release significantly expands the census of supermassive black holes, enabling large-scale statistical studies of their distribution and evolution. The combined SDSS and eROSITA datasets provide unprecedented opportunities for multi-wavelength research in astrophysics and cosmology. DR20 includes a 3-to-4-fold expansion in supermassive black hole data compared to DR19. The eROSITA catalog, based on 1.5 years of operations, nearly doubles the known X-ray sources to 2 million, with most being active galactic nuclei.

hackernews · MarcoDewey · Aug 7, 15:24 · [Discussion](https://news.ycombinator.com/item?id=49211921)

**Background**: Supermassive black holes, with masses millions to billions of times that of the Sun, reside at the centers of most galaxies. SDSS is a major multi-spectral survey that maps the sky in optical and infrared wavelengths, while eROSITA is an X-ray telescope aboard the SRG satellite that surveys the sky in X-rays. Combining these datasets allows astronomers to identify and study supermassive black holes across cosmic time.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Supermassive_black_hole">Supermassive black hole - Wikipedia</a></li>
<li><a href="https://starlust.org/sdss-data-release-20-reveals-all-sky-map-of-supermassive-black-holes/">SDSS Data Release 20 reveals all - sky map of supermassive black ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/EROSITA">eROSITA - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community members expressed fascination with the large-scale maps, drawing parallels to genomics data analysis. Some raised technical questions about apparent gridded patterns in the map, wondering if they are artifacts or real features, and asked how mapping black holes differs from mapping galaxies.

**Tags**: `#astronomy`, `#data release`, `#supermassive black holes`, `#SDSS`, `#eROSITA`

---

<a id="item-8"></a>
## [Codex with GPT-5.6 Sol Ultra Outshines Claude Fable 5 in Raccoon Heist Game](https://simonwillison.net/2026/Aug/7/moonlight-mayhem/#atom-everything) ⭐️ 7.0/10

Simon Willison posed the exact same prompt to Codex Desktop running GPT-5.6 Sol Ultra in Ultra Mode, which aggressively uses sub-agents, and it produced a much better game called 'Moonlight & Mayhem' compared to his earlier Claude Fable 5 version. The game is playable online, with the full transcript and generated assets available in a GitHub repository. This hands-on comparison provides practical insights into the current capabilities of leading AI coding tools, showing that Codex with GPT-5.6 Sol Ultra can deliver superior results on complex, creative tasks. It helps developers and AI enthusiasts understand the strengths and weaknesses of different agentic coding approaches, influencing tool choices for game development and beyond. Codex spent 52 minutes on the project, with an estimated API cost of $23.28 (700.7K input tokens, 32.5M cached tokens, and 148K output tokens) if not using a subscription. The one-shot prompt initially produced a bug where each raccoon had an oversized eyeball sphere, which Codex failed to spot despite reviewing screenshots; Willison fixed it with simple prompts 'Why do the raccoons have huge black spheres on them?' and 'Fix it'.

rss · Simon Willison · Aug 7, 19:18

**Background**: AI coding tools like Claude Code and OpenAI's Codex use large language models to generate code from natural language prompts. GPT-5.6 Sol Ultra Mode is a new capability that allows the model to spawn and coordinate multiple sub-agents in parallel, improving performance on long-horizon tasks. Sub-agents are independent AI agents that handle specific sub-tasks in isolated context windows, enabling more complex workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-the-codex-app/">Introducing the Codex app | OpenAI</a></li>
<li><a href="https://betterstack.com/community/guides/ai/gpt-56-sol-ultra-mode/">GPT-5.6 Sol and Ultra Mode: What You Need to Know</a></li>
<li><a href="https://andrew.ooo/answers/gpt-5-6-sol-ultra-mode-subagents-terminal-bench-explained-july-2026/">What Is GPT-5.6 Sol Ultra Mode? Subagents, Terminal-Bench 2.1 ...</a></li>

</ul>
</details>

**Tags**: `#AI coding`, `#Codex`, `#Claude`, `#GPT-5.6`, `#game development`

---

<a id="item-9"></a>
## [Tokenpocalypse: Companies Scramble to Cut AI Spending](https://simonwillison.net/2026/Aug/7/pdfs-are-terrible/#atom-everything) ⭐️ 7.0/10

A 404 Media report from June 24, 2026, reveals that companies are urgently reducing AI spending as token consumption surges, with Accenture's internal data showing non-engineers and PDF-to-markdown conversions are major cost drivers. This highlights a growing financial burden of AI adoption, prompting enterprises to rethink usage patterns and optimize token efficiency. It underscores the need for cost management strategies as AI becomes integral to business operations. Accenture's agentic AI strategy lead, Justice Kwak, noted that non-engineers drive token consumption, and converting PDFs to markdown is a significant token chewer. Gartner predicts AI coding costs will surpass average developer salaries by 2028 due to rising token consumption.

rss · Simon Willison · Aug 7, 16:18

**Background**: Large language models (LLMs) process text in units called tokens, and costs scale with token usage. PDFs are inefficient because they include formatting and images, consuming more tokens than plain text. Converting PDFs to markdown reduces token usage and costs, as tools like MarkItDown can cut token bills by up to 80%.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gartner.com/en/newsroom/press-releases/2026-06-24-gartner-predicts-ai-coding-costs-will-surpass-average-developer-salary-by-2028-as-token-consumption-surges">Gartner Predicts AI Coding Costs Will Surpass Average ...</a></li>
<li><a href="https://agentsroom.dev/blog/convert-pdf-to-markdown-save-tokens">Convert PDF to Markdown to Save LLM Tokens: The MarkItDown Guide</a></li>
<li><a href="https://www.mindstudio.ai/blog/convert-files-markdown-reduce-ai-tokens">How to Convert Files to Markdown to Reduce AI Token Usage by ...</a></li>

</ul>
</details>

**Tags**: `#AI costs`, `#token consumption`, `#enterprise AI`, `#PDF processing`, `#AI adoption`

---

<a id="item-10"></a>
## [China's Tech Giants Accelerate AI Talent Hiring](https://news.google.com/rss/articles/CBMiuAFBVV95cUxQSWRLODU4dTdIZy1DeEZxblRrVzV4bFRCbGtJeEVjbG5PYkQ1enh1eGlmSmJfMEpFNU9RaHlNODlfaHNhX25sczBvczJSajF5ZjlVXzh6Y0RFSDhvbFBud1lBTHJISnB1em9FX0lwcGxfR09oODZheGNzdGgtRkFmUF83RGhLZmFLVnp5WFgyVlJrOHBqYnFFbkoyUkNIdVQxNnMxeDk0T3hTbFcwTXRJOEx4N3g1Ymxm?oc=5) ⭐️ 6.0/10

China's major internet companies are advancing their hiring schedules to secure AI talent amid intensifying competition. This move reflects a strategic shift to prioritize AI capabilities in their workforce. This trend underscores the critical importance of AI talent for maintaining competitive advantage in China's tech industry. It could lead to higher salaries and more aggressive recruitment strategies, impacting the broader job market and innovation landscape. The article from Yicai Global highlights that companies are 'preponing' hiring, meaning they are moving up their recruitment timelines. Specific companies or numbers are not mentioned, but the focus is on the overall acceleration of hiring efforts.

google_news · 一财全球Yicai Global · Aug 7, 08:42

**Background**: China's tech industry has been rapidly expanding its AI capabilities, with companies like Alibaba, Tencent, and Baidu investing heavily in AI research and development. The demand for skilled AI professionals has surged, leading to intense competition for top talent.

**Tags**: `#AI talent`, `#China tech`, `#hiring`, `#industry trends`

---