---
layout: default
title: "Horizon Summary: 2026-08-24 (EN)"
date: 2026-08-24
lang: en
---

> From 48 items, 11 important content pieces were selected

---

1. [seL4 Security Proofs Complete on AArch64](#item-1) ⭐️ 9.0/10
2. [MS Paint and Photos invisibly watermark AI images with GUID](#item-2) ⭐️ 8.0/10
3. [San Francisco Recreated as Interactive 3D Web Game](#item-3) ⭐️ 8.0/10
4. [Oceans Hit Record High Temperatures, Signaling Accelerating Climate Change](#item-4) ⭐️ 8.0/10
5. [IPFS Maintainer Team Shipyard Sunsets, Project Continues](#item-5) ⭐️ 8.0/10
6. [OpenAI's GPT-5.6 in Kiro Boosts Developer Price-Performance](#item-6) ⭐️ 8.0/10
7. [Your Executable is a SQLite Database](#item-7) ⭐️ 8.0/10
8. [AI as Spatial Software Generator for Programmable 3D Objects](#item-8) ⭐️ 8.0/10
9. [Insilico Medicine Launches O3DC Open Alliance for AI Drug Discovery Benchmarks](#item-9) ⭐️ 7.0/10
10. [llm-anthropic 0.27 Adds Compatibility with Anthropic SDK v1.0.0](#item-10) ⭐️ 5.0/10
11. [Chinese Consumers Increasingly Use AI for Purchase Decisions](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [seL4 Security Proofs Complete on AArch64](https://proofcraft.systems/news-2026/#2026-08-21) ⭐️ 9.0/10

The seL4 microkernel's formal security proofs have been completed for the AArch64 architecture, marking a significant milestone in formal verification. This extends seL4's proven confidentiality, integrity, and availability properties to the 64-bit ARM architecture. This is significant because AArch64 is widely used in mobile, embedded, and server systems, and having formally verified security properties on this architecture enhances trust in systems built on seL4. It could accelerate adoption in security-critical domains such as automotive, avionics, and defense. The proof covers the non-MCS (mixed criticality systems) configuration and is limited to uniprocessor (unicore) systems, as noted in the fine print. This means the proof does not yet cover multicore or MCS configurations, which are important for many real-world deployments.

hackernews · snvzz · Aug 24, 11:32 · [Discussion](https://news.ycombinator.com/item?id=49418255)

**Background**: seL4 is an open-source, capability-based microkernel known for its high-assurance properties, achieved through formal mathematical verification. Formal verification involves proving that the kernel's implementation meets its specification, ensuring properties like confidentiality, integrity, and availability. AArch64 is the 64-bit execution state of the ARM architecture, widely used in modern processors. Completing the proof on AArch64 extends seL4's verified assurance to a new, widely adopted architecture.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SeL4">seL4 - Wikipedia</a></li>
<li><a href="https://cacm.acm.org/research/sel4-formal-verification-of-an-operating-system-kernel/">seL4: Formal Verification of an Operating-System Kernel</a></li>
<li><a href="https://sel4.systems/Research/pdfs/comprehensive-formal-verification-os-microkernel.pdf">Comprehensive Formal Verification of an OS Microkernel</a></li>

</ul>
</details>

**Discussion**: Community comments highlight concerns about side-channel timing attacks potentially invalidating the result, and point out the proof's limitations (non-MCS, unicore). Some users discuss the adoption of seL4 in various operating systems and question its practical impact without a native seL4/Linux, suggesting that secure-boot virtualization platforms are common.

**Tags**: `#seL4`, `#formal verification`, `#AArch64`, `#security`, `#microkernel`

---

<a id="item-2"></a>
## [MS Paint and Photos invisibly watermark AI images with GUID](https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/) ⭐️ 8.0/10

Microsoft Paint and Photos have been found to embed invisible, server-issued GUID watermarks into images that have been AI-manipulated, even when the processing is done locally. The watermark is applied silently and cannot be disabled by the user. This raises significant privacy concerns because the GUID can be traced back to the user's Microsoft account, potentially linking anonymous images to individuals. It also highlights the tension between AI transparency efforts and user privacy, especially as AI-generated content becomes more prevalent. The watermark is applied via a function called ApplyWatermark, which uses a GUID associated with the prompt generation ID. In Paint, a watermarking failure causes the image generation to fail, while in Photos, it logs an error but still returns the image. The watermark is separate from C2PA metadata and is not disclosed to users.

hackernews · ComputerGuru · Aug 24, 15:28 · [Discussion](https://news.ycombinator.com/item?id=49421158)

**Background**: Digital watermarking is a technique used to embed hidden information into media to identify ownership or provenance. The EU AI Act, which took effect in August 2026, requires AI-generated content to carry detectable marks, but it does not mandate prompt-specific GUIDs. Microsoft has disclosed C2PA metadata but not the server-issued watermark GUID, raising questions about compliance and user consent.

<details><summary>References</summary>
<ul>
<li><a href="https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/">Microsoft Paint and Photos Embed Server-Issued GUIDs as Invisible Watermarks in Locally-Generated Images :: Xusheng Li</a></li>
<li><a href="https://en.wikipedia.org/wiki/Digital_watermarking">Digital watermarking - Wikipedia</a></li>
<li><a href="https://www.brookings.edu/articles/detecting-ai-fingerprints-a-guide-to-watermarking-and-beyond/">Detecting AI fingerprints: A guide to watermarking and beyond | Brookings</a></li>

</ul>
</details>

**Discussion**: Community comments express concern about the hidden unique identifier, with one user noting it could be used to subpoena Microsoft for user data, undermining internet anonymity. Another user points out that Microsoft has been sloppy with AI-related features, citing a previous incident with Azure DevOps commits, and recommends avoiding Paint and other LLM-enabled apps.

**Tags**: `#privacy`, `#watermarking`, `#Microsoft`, `#AI`, `#security`

---

<a id="item-3"></a>
## [San Francisco Recreated as Interactive 3D Web Game](https://sf.thijs.gg/) ⭐️ 8.0/10

A web-based project at sf.thijs.gg renders the entire city of San Francisco as an interactive 3D environment, allowing users to explore streets and buildings in a video game-like manner. The project has gained significant attention, with 306 points and 106 comments on Hacker News. This project showcases the potential of web-based 3D rendering for creating immersive digital twins of real cities, which could impact interactive mapping, urban planning, and game development. Its high community engagement suggests strong interest in accessible, browser-based virtual exploration. The project uses web technologies to render the city in real-time, and community members have suggested enhancements such as adding street names, landmarks, and address-based teleportation. Some users have proposed integrating Street View imagery or using GIS data to further improve realism.

hackernews · centrosphere · Aug 24, 17:05 · [Discussion](https://news.ycombinator.com/item?id=49422784)

**Background**: 3D city models are digital representations of urban environments, often built from GIS data, elevation models, and building footprints. Web-based 3D viewers, such as those using Cesium or WebGL, enable interactive exploration of these models in a browser without requiring specialized software. This project leverages similar technologies to create a game-like experience of San Francisco.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/3D_city_models">3D city model - Wikipedia</a></li>
<li><a href="https://github.com/3dcitydb/3dcitydb-web-map">GitHub - 3dcitydb/3dcitydb-web-map: Cesium-based 3D viewer and JavaScript API for the 3D City Database · GitHub</a></li>
<li><a href="https://demo.f4map.com/">F4map Demo - Interactive 3D map</a></li>

</ul>
</details>

**Discussion**: Community comments are overwhelmingly positive, with users expressing emotional connections to the city and excitement about the project's potential. Suggestions for improvement include adding more interactive elements, using higher-resolution data, and integrating with game engines like GTA. Some users also shared similar projects they are working on, indicating a broader interest in city-scale 3D rendering.

**Tags**: `#3D rendering`, `#interactive maps`, `#San Francisco`, `#web technology`, `#game development`

---

<a id="item-4"></a>
## [Oceans Hit Record High Temperatures, Signaling Accelerating Climate Change](https://www.bbc.com/news/articles/c62m4gpnp78o) ⭐️ 8.0/10

Oceans have reached their highest recorded temperature, according to recent data, highlighting the accelerating pace of climate change. This record underscores the urgent need for action to mitigate global warming. This milestone is significant because ocean warming drives sea-level rise, intensifies storms, and disrupts marine ecosystems, affecting billions of people worldwide. It also serves as a stark reminder of the consequences of continued greenhouse gas emissions. The record temperature was observed in early 2024, with the average sea surface temperature surpassing previous highs. Scientists attribute this to a combination of human-induced climate change and the El Niño phenomenon, which is expected to continue influencing weather patterns.

hackernews · tcp_handshaker · Aug 24, 19:19 · [Discussion](https://news.ycombinator.com/item?id=49424606)

**Background**: Oceans absorb about 90% of the excess heat from greenhouse gas emissions, making ocean temperature a key indicator of global warming. The El Niño-Southern Oscillation (ENSO) is a natural climate pattern that can temporarily raise global temperatures, exacerbating the effects of climate change.

**Discussion**: Commenters expressed concern over government inaction and the worsening climate crisis, with some highlighting the role of fossil fuel expansion and data centers. Others shared educational resources and personal reflections on the severity of a few degrees of warming, while one user noted the upcoming El Niño could bring more unpredictability.

**Tags**: `#climate change`, `#ocean temperature`, `#environment`, `#science`, `#global warming`

---

<a id="item-5"></a>
## [IPFS Maintainer Team Shipyard Sunsets, Project Continues](https://ipshipyard.com/blog/2026-the-end-of-ipfs-at-shipyard/) ⭐️ 8.0/10

The IPFS maintainer team Shipyard announced it is winding down, ceasing dedicated maintenance of nine IPFS implementations including Kubo, Helia, and IPFS Desktop. The IPFS project itself is not shutting down but will shift to individual maintainer grants. This marks a significant shift in the decentralized web ecosystem, as Shipyard was a major contributor to IPFS development. It raises questions about the long-term sustainability of open-source projects and the future of IPFS implementations, affecting developers and users who rely on these tools. The affected projects include Kubo, Helia, Boxo, Rainbow, IPFS Desktop, IPFS Companion, Someguy, Service Worker Gateway, and IPFS Check. The IPFS Implementation Fund, established in 2022, will continue to provide grants for individual maintainers.

hackernews · iand · Aug 24, 15:48 · [Discussion](https://news.ycombinator.com/item?id=49421489)

**Background**: IPFS (InterPlanetary File System) is a peer-to-peer protocol for storing and sharing content-addressed data. Shipyard was one of several teams maintaining IPFS implementations, funded by Protocol Labs. The sunsetting of Shipyard reflects broader challenges in sustaining open-source infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://ipshipyard.com/blog/2026-the-end-of-ipfs-at-shipyard/">The end of IPFS at Shipyard</a></li>
<li><a href="https://ipfsgrants.io/utility-grants/">IPFS Implementation Fund</a></li>
<li><a href="https://byteiota.com/ipfs-shipyard-shuts-down-what-developers-must-do-now/">IPFS Shipyard Shuts Down: What Developers Must Do Now</a></li>

</ul>
</details>

**Discussion**: Community members clarified that the announcement is about Shipyard, not the entire IPFS project, and expressed sadness over the loss. Some suggested alternatives like Iroh, built by ex-IPFS developers, while others criticized the focus on IPNS and the irony of using Google Forms for feedback.

**Tags**: `#IPFS`, `#decentralized web`, `#open source`, `#maintainership`, `#p2p`

---

<a id="item-6"></a>
## [OpenAI's GPT-5.6 in Kiro Boosts Developer Price-Performance](https://openai.com/index/gpt-5-6-in-kiro) ⭐️ 8.0/10

OpenAI has announced the availability of GPT-5.6 in Kiro, its agentic engineering platform, marking the first time OpenAI models are offered in Kiro. The release includes three tiers—Sol, Terra, and Luna—designed to balance agentic performance and cost, with testing showing up to 82% cost reduction on Terminal-Bench 2.1. This release is significant for developers as it directly addresses the need for better price-performance in AI-assisted software development, potentially lowering the barrier to entry for using frontier models. It also signals OpenAI's expansion into agentic engineering tools, intensifying competition with other AI coding platforms. GPT-5.6 in Kiro offers three model tiers: Sol, Terra, and Luna, each balancing performance and cost. Kiro's spec-driven approach grounds the model in clear requirements and technical designs, enabling faster, more efficient task completion. The integration with AWS has optimized the environment, contributing to the reported cost reductions.

rss · OpenAI Blog · Aug 24, 12:00

**Background**: Kiro is an agentic engineering platform that helps developers turn prompts into executable specs, validate code correctness, and build across large codebases with parallel agents. GPT-5.6 is a newer generation model from OpenAI, distinct from GPT-4o, offering improved intelligence and performance. The integration of GPT-5.6 into Kiro represents a convergence of frontier AI models with specialized development tools.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-5-6-in-kiro/">Advancing price-performance for developers with GPT‑5.6 in Kiro</a></li>
<li><a href="https://kiro.dev/">Kiro: Move beyond AI coding to agentic engineering</a></li>
<li><a href="https://kiro.dev/docs/models/">Models - Docs - Kiro</a></li>

</ul>
</details>

**Tags**: `#AI`, `#OpenAI`, `#GPT-5.6`, `#developer tools`, `#price-performance`

---

<a id="item-7"></a>
## [Your Executable is a SQLite Database](https://simonwillison.net/2026/Aug/24/your-executable-is-a-sqlite-database/) ⭐️ 8.0/10

Farid Zakaria has developed a technique to create a single file that is both a valid SQLite database and a Linux executable. The method sets the SQLite application ID to 'SELF' and stores ELF components in SQLite tables, with a custom interpreter to execute them. This hack demonstrates the flexibility of SQLite as a file format and opens up possibilities for embedding executable code within databases, which could be useful for self-contained applications or data-driven executables. It also showcases creative use of Linux's binfmt_misc mechanism. The SQLite application ID is set to 'SELF' at byte offset 68, and the ELF components are stored in tables as per the provided schema. The custom interpreter 'self-exec' extracts and executes the ELF parts, and binfmt_misc can be configured to automatically invoke it for files with this pattern.

rss · Simon Willison · Aug 24, 11:38

**Background**: SQLite is a widely-used embedded database that stores data in a single file, and its format includes a 4-byte application ID that can be used to identify the file type. ELF is the standard executable format on Linux, containing headers and sections that define how the program should be loaded and run. binfmt_misc is a Linux kernel feature that allows custom binary formats to be executed by associating them with an interpreter.

<details><summary>References</summary>
<ul>
<li><a href="https://sqlite.org/forum/info/6a768e7dca11a7b2">SQLite User Forum: Usage of application_id and magic.txt</a></li>
<li><a href="https://en.wikipedia.org/wiki/Executable_and_Linkable_Format">Executable and Linkable Format - Wikipedia</a></li>
<li><a href="https://docs.kernel.org/admin-guide/binfmt-misc.html">Kernel Support for miscellaneous Binary Formats (binfmt_misc) — The Linux Kernel documentation</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion likely appreciates the cleverness of the hack and its potential applications, though some may question its practicality or security implications. The technique is novel and well-explained, generating interest in the intersection of database and executable formats.

**Tags**: `#sqlite`, `#elf`, `#linux`, `#executable`, `#hack`

---

<a id="item-8"></a>
## [AI as Spatial Software Generator for Programmable 3D Objects](https://www.reddit.com/r/MachineLearning/comments/1vxcc1h/r_using_ai_as_a_spatial_software_generator_to/) ⭐️ 8.0/10

The paper introduces a novel approach using LLMs to generate 3D objects as spatial software, enabling inherent programmability, hierarchical structure, and animation readiness. The authors provide visual demonstrations at nova3d.xyz and a GitHub repository. This approach could significantly impact industries like industrial design, game development, simulations, and AR/VR/XR by making 3D objects more useful and adaptable. It addresses limitations of traditional AI 3D generators that produce monolithic mesh blobs. The generated 3D objects are animation-ready and programmable from inception, can adapt to different compute environments, and feature full hierarchical structure with hinge/socket articulation. However, they lag behind traditional AI 3D generators in creating complex organic shapes.

reddit · r/MachineLearning · /u/mhb_11 · Aug 24, 19:10

**Background**: Traditional AI 3D generators typically output monolithic mesh blobs that are difficult to edit or animate. Procedural generation, on the other hand, creates data algorithmically, allowing for smaller file sizes and more flexibility. This paper leverages LLMs' coding capabilities to generate 3D objects as software, combining the benefits of procedural generation with the ease of natural language prompts.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Procedural_generation">Procedural generation</a></li>
<li><a href="https://arxiv.org/abs/2506.11148">[2506.11148] LLM-to-Phy3D: Physically Conform Online 3D ... LLM-to-Phy3D: Physically Conform Online 3D Object Generation ... Awesome-LLM-3D - GitHub GitHub - NVIDIA-AI-Blueprints/3d-object-generation LLMto3D - Generation of parametric, 3D printable objects ... LLMto3D - Generating Parametric Objects from Text Prompts LLM-to-Phy3D: Physically Conform Online 3D Object Generation ...</a></li>

</ul>
</details>

**Tags**: `#AI 3D generation`, `#LLMs`, `#spatial programming`, `#procedural generation`, `#machine learning`

---

<a id="item-9"></a>
## [Insilico Medicine Launches O3DC Open Alliance for AI Drug Discovery Benchmarks](https://news.google.com/rss/articles/CBMic0FVX3lxTE1nVE05VlZZQVI0OVVVME1ZdU5ZaHJHRkFqN1lpQ1lKS29Qa2VPLXo3UENzZ2t1RXYwUlhJTU5zYXJpVXJnOUtYel9VNTJjNGZGWEVfN016VDBPWEdocTBtVGFZUS1kMFljazR6eWZQU2ZrTjg?oc=5) ⭐️ 7.0/10

Insilico Medicine announced the launch of the O3DC (Open Drug Discovery and Development Consortium) open alliance on August 24, 2025, aiming to establish benchmark quality standards for AI-driven drug discovery. The consortium will provide a community-maintained map of open benchmarks in the field. This initiative could standardize the evaluation of AI models in drug discovery, addressing the current fragmentation of benchmarks across the field. It may accelerate progress by enabling fair comparisons and fostering collaboration among researchers, industry, and academia. The O3DC Benchmark Index is a community-maintained resource listing open benchmarks with repositories, maintainers, live update status, and per-benchmark discussion. Insilico Medicine also generates approximately 1,200 benchmarks from each developmental candidate, many of which will be made available through the consortium.

google_news · EurekAlert! · Aug 24, 19:11

**Background**: AI-driven drug discovery uses generative models and other machine learning techniques to design and test new molecules, potentially reducing the time and cost of drug development. However, the evaluation landscape is scattered across dozens of repositories, making it difficult to compare models and track progress. Open alliances like O3DC aim to consolidate these benchmarks and promote transparency and collaboration in the field.

<details><summary>References</summary>
<ul>
<li><a href="https://www.o3dc.org/">O3DC · Drug Discovery Benchmark Index</a></li>
<li><a href="https://www.linkedin.com/pulse/insilico-medicine-convenes-o3dc-open-consortium-benchmark-shy5c">Insilico Medicine Convenes O3DC, an Open Consortium for ...</a></li>
<li><a href="https://insilico.com/">Main | Insilico Medicine</a></li>

</ul>
</details>

**Tags**: `#AI drug discovery`, `#benchmarking`, `#open alliance`, `#pharmaceutical research`, `#standards`

---

<a id="item-10"></a>
## [llm-anthropic 0.27 Adds Compatibility with Anthropic SDK v1.0.0](https://simonwillison.net/2026/Aug/24/llm-anthropic/) ⭐️ 5.0/10

llm-anthropic 0.27 has been released, updating the Anthropic plugin for LLM to be compatible with the anthropic v1.0.0 Python library, which switches from httpx to httpx2. The update was largely automated using Claude Code with Fable 5, resulting in a pull request that gets tests passing. This update ensures that users of the LLM tool can continue to use Anthropic's Claude models without disruption as the underlying SDK undergoes a major version change. It also reflects a broader ecosystem shift towards httpx2, following OpenAI's similar move in their v3.0.0 release, which may signal a new standard for Python HTTP clients. The release was driven by a prompt to Claude Code to upgrade to anthropic>=1 and read the migration guide, resulting in PR #84. The anthropic v1.0.0 library and OpenAI's v3.0.0 both adopt httpx2, a next-generation HTTP client that supports HTTP/1.1 and HTTP/2 with sync and async APIs.

rss · Simon Willison · Aug 24, 16:27

**Background**: LLM is a command-line tool and Python library by Simon Willison that provides a unified interface to various language models, including Anthropic's Claude series. Plugins like llm-anthropic extend LLM's functionality by adding support for specific model providers. The anthropic Python SDK is the official library for interacting with Anthropic's API, and its major version 1.0.0 introduced a breaking change by switching its underlying HTTP client from httpx to httpx2, necessitating updates in dependent projects.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Aug/24/llm-anthropic/">Release: llm- anthropic 0.27 | Simon Willison’s Weblog</a></li>
<li><a href="https://github.com/simonw/llm-anthropic">GitHub - simonw/llm-anthropic: LLM access to models by ...</a></li>
<li><a href="https://pypi.org/project/httpx2/">httpx2 · PyPI</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Anthropic`, `#Python`, `#SDK`, `#httpx2`

---

<a id="item-11"></a>
## [Chinese Consumers Increasingly Use AI for Purchase Decisions](https://news.google.com/rss/articles/CBMizwFBVV95cUxPdllrWXMwZUd1Q1NueUZWdFotVlU0VUlHMGYzbGU2cy0xQzRHWWtEYVBKVjFzenhFbXRSLWk1eXV1eFJmVC1PWW5vM09jWEF0SWJzcnF1dTJpRzQ0S2F1SzZ4T3NDMmtrdkdiUjJja0xFMllFY1JEOWxyWUFhRTZTeEpHbjJLRElQcEVUdGIxUkJBeGVLTjlvVHVmSVdzbU1tVHZaTHg5bmZvN3p1S05aT1JVdDFCLWVtTHRpN3JJck9UMEtxSUwwNU00aHN1MkE?oc=5) ⭐️ 5.0/10

A recent report reveals that a majority of Chinese consumers now consult AI tools before purchasing new products, and brands are adapting their marketing strategies to accommodate this trend. This shift indicates AI's growing influence on consumer behavior in one of the world's largest markets, prompting brands to integrate AI into their customer engagement and product recommendation strategies. It also highlights the need for businesses to understand and leverage AI-driven decision-making processes. The report does not specify the exact percentage of consumers using AI, but it emphasizes that the trend is significant enough for brands to adapt. The adaptation likely includes using AI for personalized recommendations, chatbots for customer service, and AI-generated content in marketing.

google_news · 一财全球Yicai Global · Aug 24, 09:12

**Background**: AI adoption in China has been rapid, with consumers using AI assistants like Alibaba's Tongyi Qianwen and Baidu's Ernie Bot for various tasks, including shopping advice. E-commerce platforms are increasingly embedding AI features to enhance user experience and drive sales. This trend reflects a broader global movement where AI is becoming a trusted advisor in consumer purchasing decisions.

**Tags**: `#AI`, `#consumer behavior`, `#China`, `#e-commerce`

---