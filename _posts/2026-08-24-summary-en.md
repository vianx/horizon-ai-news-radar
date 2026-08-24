---
layout: default
title: "Horizon Summary: 2026-08-24 (EN)"
date: 2026-08-24
lang: en
---

> From 40 items, 11 important content pieces were selected

---

1. [Xiaomi XRing O3 CPU Matches Apple Single-Core, Beats Multi-Core](#item-1) ⭐️ 8.0/10
2. [MS Paint and Photos Embed Invisible GUID Watermarks in Local AI Images](#item-2) ⭐️ 8.0/10
3. [San Francisco Recreated as Playable Web Game from GIS Data](#item-3) ⭐️ 8.0/10
4. [Oceans Hit Record High Temperatures, Signaling Accelerating Climate Crisis](#item-4) ⭐️ 8.0/10
5. [IPFS Maintainers Sunset Centralized Support at Shipyard](#item-5) ⭐️ 8.0/10
6. [OpenAI's GPT-5.6 in Kiro Boosts Developer Price-Performance](#item-6) ⭐️ 8.0/10
7. [Linux Hack: SQLite Database as Executable](#item-7) ⭐️ 8.0/10
8. [LLMs as Spatial Software Generators for Programmable 3D Objects](#item-8) ⭐️ 8.0/10
9. [Insilico Medicine Launches O3DC Open Alliance for AI Drug Discovery Benchmarks](#item-9) ⭐️ 7.0/10
10. [llm-anthropic 0.27 adds compatibility with anthropic v1.0.0](#item-10) ⭐️ 5.0/10
11. [Chinese Consumers Increasingly Use AI for Product Research](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Xiaomi XRing O3 CPU Matches Apple Single-Core, Beats Multi-Core](https://twitter.com/lemire/status/2091894299289874926) ⭐️ 8.0/10

Xiaomi has unveiled its new XRing O3 mobile SoC, which reportedly matches Apple's single-core performance and exceeds it in multi-core benchmarks. The chip, built on a 3nm process, features a 10-core all-big-core CPU and is the first mobile processor to support LPDDR6 memory. This marks a significant competitive shift in the mobile chip market, as Xiaomi, the third-largest smartphone manufacturer, now has an in-house chip that rivals Apple's performance. It poses a direct threat to Qualcomm and MediaTek, potentially reshaping the industry landscape. The XRing O3 scores 3,945 in Geekbench single-core and 15,221 in multi-core, compared to Apple M5's 3,556 and 15,285 respectively. It also achieves an AnTuTu score of 5.22 million, and its GPU, the G2-Ultra NX, offers an 85% performance boost with 64% lower power consumption.

hackernews · tosh · Aug 24, 15:08 · [Discussion](https://news.ycombinator.com/item?id=49420873)

**Background**: Mobile SoCs are the brains of smartphones, integrating CPU, GPU, and other components. Apple's M-series chips have long been the performance benchmark, but Xiaomi's new chip, built on TSMC's N3P node, uses an all-big-core design that ditches efficiency cores to maximize performance. This is part of a broader trend of smartphone makers developing in-house chips to differentiate and reduce reliance on third-party suppliers.

<details><summary>References</summary>
<ul>
<li><a href="https://gadgets.beebom.com/guides/xiaomi-xring-o3-benchmark-specs">Xiaomi Xring O 3 : Benchmarks and Specs | Beebom Gadgets</a></li>
<li><a href="https://www.gizmochina.com/2026/08/24/xiaomi-xring-o3-o100-d100-chipsets-launched-xiaomi-18-fold/">Xring O3 launches with 5.22M AnTuTu score and LPDDR6, Xiaomi ...</a></li>
<li><a href="https://www.notebookcheck.net/Xiaomi-launches-XRing-O3-claims-it-is-the-fastest-smartphone-SoC-with-an-AnTuTu-score-of-over-5-million.1376668.0.html">Xiaomi launches XRing O3, claims it is the fastest smartphone ...</a></li>

</ul>
</details>

**Discussion**: Community comments highlight concerns about power efficiency, noting that raw performance numbers don't reflect real-world usage in phones. Some point out that Xiaomi's chip is similar to MediaTek's Dimensity 9500, and that while it matches Apple's single-core, it falls short in multi-core when comparing core counts. Others see this as a positive sign for Xiaomi's chip ambitions, but note Apple still leads in efficiency.

**Tags**: `#CPU`, `#Xiaomi`, `#Apple`, `#mobile`, `#semiconductors`

---

<a id="item-2"></a>
## [MS Paint and Photos Embed Invisible GUID Watermarks in Local AI Images](https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/) ⭐️ 8.0/10

Reverse engineering reveals that Microsoft Paint and Photos embed a server-issued 16-byte GUID as an invisible watermark in every locally generated AI image, even when generation is performed offline. The GUID is obtained from a mandatory remote moderation request to an Azure Front Door endpoint before local generation runs. This raises significant privacy and anonymity concerns because the invisible watermark can be used to trace images back to the user's Microsoft account, potentially enabling copyright subpoenas or surveillance. It also highlights a broader trend of software embedding hidden identifiers without user consent, which could erode trust in AI tools. The watermark is embedded in approximately 74% of the image's pixels and contains an 18-byte payload with the GUID. If the watermarking step fails, Paint cancels the generation entirely, meaning users cannot opt out. The watermark is invisible and cannot be disabled, even though a visible watermark can be turned off.

hackernews · ComputerGuru · Aug 24, 15:28 · [Discussion](https://news.ycombinator.com/item?id=49421158)

**Background**: Watermarking is a technique used to embed identifying information into digital media, often to protect copyright or verify authenticity. Invisible watermarks are designed to be imperceptible to humans but can be detected by software. Microsoft's implementation ties the watermark to a remote moderation server, meaning even local AI generation is not fully private. This practice aligns with industry efforts to combat misinformation by tracing AI-generated content, but it also raises concerns about user control and anonymity.

<details><summary>References</summary>
<ul>
<li><a href="https://mangodeveloper.com/articles/microsoft-paint-embeds-invisible-guid-watermarks-in-local-ai-images-via-remote-moderation-server">Microsoft Paint Embeds Invisible GUID Watermarks in Local AI ...</a></li>
<li><a href="https://byteiota.com/ms-paint-invisible-server-guid-watermark-ai-image/">MS Paint Embeds Invisible Server GUIDs in Every AI Image</a></li>

</ul>
</details>

**Discussion**: The community is largely critical, with users expressing shock that MS Paint has become more than a simple pixel editor and accusing Microsoft of 'evil' behavior. A key concern is that the hidden unique identifier could be used to de-anonymize users via copyright subpoenas, undermining internet anonymity. Some users also note Microsoft's past sloppy implementations of similar features, leading to recommendations against using Paint or other LLM-enabled apps.

**Tags**: `#privacy`, `#watermarking`, `#Microsoft`, `#AI`, `#security`

---

<a id="item-3"></a>
## [San Francisco Recreated as Playable Web Game from GIS Data](https://sf.thijs.gg/) ⭐️ 8.0/10

A developer has created a web-based interactive 3D recreation of San Francisco as a playable video game, built entirely from GIS data. The project, hosted at sf.thijs.gg, allows users to explore the city in a game-like environment. This project demonstrates the potential of using publicly available GIS data to create immersive, interactive urban experiences, which could inspire new forms of digital tourism, urban planning visualization, and game development. It has sparked significant community interest, with discussions about integrating more data and expanding the concept to other cities. The recreation is built from GIS data, likely including building footprints, elevation, and road networks, rendered in a web browser. The current version includes driving mechanics and collectible coins, but lacks a deeper game narrative; community members have suggested adding indoor blueprints, street view imagery, and more interactive elements.

hackernews · centrosphere · Aug 24, 17:05 · [Discussion](https://news.ycombinator.com/item?id=49422784)

**Background**: GIS (Geographic Information System) is a technology that captures, analyzes, and displays spatial or geographic data. 3D city models are increasingly used in urban management and simulations, but tools for evaluating them are limited. Procedural generation in games uses algorithms to create content like maps and levels, which can reduce development costs and create unique experiences.

<details><summary>References</summary>
<ul>
<li><a href="https://www.esri.com/en-us/what-is-gis/overview">What is GIS ? | Geographic Information System Mapping Technology</a></li>
<li><a href="https://en.wikipedia.org/wiki/Procedural_generation">Procedural generation - Wikipedia</a></li>
<li><a href="https://research.birmingham.ac.uk/en/publications/assessing-and-benchmarking-3d-city-models/">Assessing and benchmarking 3 D city models - University of Birmingham</a></li>

</ul>
</details>

**Discussion**: Community comments express emotional resonance, with one user who lived in SF for 20 years finding it moving to revisit familiar places. Others suggest technical improvements like integrating indoor blueprints, using LLMs to process GIS data, and adding street view imagery for higher fidelity. Some users share similar projects, such as a Philadelphia-based game, and discuss the potential for a pipeline to generate GTA-style maps from city data.

**Tags**: `#GIS`, `#3D rendering`, `#procedural generation`, `#web game`, `#San Francisco`

---

<a id="item-4"></a>
## [Oceans Hit Record High Temperatures, Signaling Accelerating Climate Crisis](https://www.bbc.com/news/articles/c62m4gpnp78o) ⭐️ 8.0/10

Oceans have reached their highest recorded temperature, according to a recent report, marking a critical milestone in the accelerating climate crisis. This record underscores the severity of global warming and its far-reaching impacts on marine ecosystems, weather patterns, and coastal communities worldwide. It highlights the urgent need for policy action to mitigate climate change. The record temperature was observed in early 2024, with ocean heat content reaching unprecedented levels. This warming is largely attributed to human-induced greenhouse gas emissions, compounded by natural phenomena like El Niño.

hackernews · tcp_handshaker · Aug 24, 19:19 · [Discussion](https://news.ycombinator.com/item?id=49424606)

**Background**: Oceans absorb about 90% of the excess heat from global warming, making ocean temperature a key indicator of climate change. Rising ocean temperatures can lead to coral bleaching, sea-level rise, and more intense storms, affecting biodiversity and human livelihoods.

**Discussion**: Community comments express concern over government inaction, with some pointing to the US expanding fossil fuel extraction and attacking renewables. Others highlight the scientific nuances, such as the role of melting ice in ocean heating, and anticipate increased weather unpredictability due to El Niño.

**Tags**: `#climate change`, `#ocean temperature`, `#environment`, `#science`, `#policy`

---

<a id="item-5"></a>
## [IPFS Maintainers Sunset Centralized Support at Shipyard](https://ipshipyard.com/blog/2026-the-end-of-ipfs-at-shipyard/) ⭐️ 8.0/10

The IPFS maintainers at Shipyard have announced they are winding down their centralized support, transitioning to individual grants for maintainers. The IPFS project itself is not shutting down, but rather shifting its maintenance model. This marks a significant shift in the decentralized web ecosystem, as IPFS is a foundational technology for many projects. The move to individual grants could affect the pace and coordination of IPFS development, but it also opens opportunities for more diverse contributions. The announcement clarifies that only the Shipyard maintainer team is sunsetting, not the IPFS project. The transition to individual grants is part of a new governance structure, with grants now focused on integrations, extensions, and new implementations.

hackernews · iand · Aug 24, 15:48 · [Discussion](https://news.ycombinator.com/item?id=49421489)

**Background**: IPFS (InterPlanetary File System) is a peer-to-peer protocol for storing and sharing content-addressed data, widely used for decentralized web applications. Shipyard has been one of the key maintainer teams for IPFS implementations, and this change reflects a broader trend of decentralizing maintenance efforts.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ipfs/devgrants">GitHub - ipfs/devgrants: The IPFS Grant platform connects funding organizations with builders and researchers in the IPFS community. · GitHub</a></li>
<li><a href="https://blog.ipfs.tech/2020-04-20-ipfs-grants-platform/">IPFS Grants Platform | IPFS Blog & News</a></li>
<li><a href="https://docs.ipfs.tech/concepts/ipfs-implementations/">IPFS implementations | IPFS Docs</a></li>

</ul>
</details>

**Discussion**: Community members expressed confusion about the announcement, with some initially thinking IPFS itself was shutting down. Others suggested alternative projects like Iroh, and some criticized the use of Google Forms for feedback, highlighting a desire for more decentralized solutions.

**Tags**: `#IPFS`, `#decentralization`, `#open source`, `#maintenance`, `#p2p`

---

<a id="item-6"></a>
## [OpenAI's GPT-5.6 in Kiro Boosts Developer Price-Performance](https://openai.com/index/gpt-5-6-in-kiro) ⭐️ 8.0/10

OpenAI has announced that GPT-5.6 is now available in Kiro, an AI-powered developer tool, offering improved price-performance for planning, building, reviewing, and testing software. This release follows OpenAI's broader push to advance the price-performance frontier with GPT-5.6, which includes models like Sol, Terra, and Luna. This update is significant for developers as it provides a more cost-effective and efficient way to leverage AI in software development, potentially lowering barriers for adoption. It also signals OpenAI's continued focus on optimizing price-performance, which is crucial for businesses looking to integrate AI without prohibitive costs. Kiro, developed by AWS, is an agentic IDE and CLI that uses spec-driven development, turning ideas into written plans before generating code. GPT-5.6's price-performance improvements include Luna, which delivers performance comparable to frontier-class models from a year ago at roughly 6 cents per task and nearly nine times the speed, while Sol offers up to 2.5x faster speeds at twice the price.

rss · OpenAI Blog · Aug 24, 12:00

**Background**: GPT-5.6 is a family of AI models from OpenAI designed to offer various trade-offs between intelligence, speed, and cost. Kiro is an AI-powered development environment that integrates with such models to assist developers in writing software more efficiently. The integration aims to combine Kiro's structured development approach with GPT-5.6's enhanced price-performance to streamline the software development lifecycle.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/advancing-the-price-performance-frontier-with-gpt-5-6/">Advancing the price-performance frontier with GPT-5.6 | OpenAI</a></li>
<li><a href="https://www.eesel.ai/blog/gpt-5-6-pricing">GPT-5.6 pricing (2026): Sol, Terra and Luna rates explained | eesel AI</a></li>
<li><a href="https://toolquestor.com/tool/kiro">Kiro – AWS Agentic IDE for Spec-Driven Coding</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#AI model`, `#developer tools`, `#price-performance`

---

<a id="item-7"></a>
## [Linux Hack: SQLite Database as Executable](https://simonwillison.net/2026/Aug/24/your-executable-is-a-sqlite-database/) ⭐️ 8.0/10

Farid Zakaria has developed a technique that allows a SQLite database file to be executed directly as a Linux binary. This is achieved by embedding ELF components into SQLite tables and using a custom interpreter called self-exec. This innovation showcases a creative fusion of file formats, potentially enabling new ways to package and distribute applications. It could inspire developers to explore unconventional uses of SQLite and ELF, leading to novel software distribution and execution methods. The technique sets the SQLite file's 4-byte application ID (at offset 68) to 'SELF', and arranges ELF components into SQLite tables using a specific schema. The self-exec interpreter, written in C, extracts and executes the necessary parts, and binfmt_misc can be used to register the pattern for automatic execution.

rss · Simon Willison · Aug 24, 11:38

**Background**: SQLite databases have a header field called 'application_id' that can store a custom identifier, which is typically used by applications to identify their file format. ELF (Executable and Linkable Format) is the standard binary format for executables on Linux. binfmt_misc is a Linux kernel feature that allows the kernel to recognize and execute arbitrary binary formats by matching magic byte sequences.

<details><summary>References</summary>
<ul>
<li><a href="https://stackoverflow.com/questions/21929457/sqlite-how-to-use-pragma-application-id">SQLite: how to use PRAGMA application_id? - Stack Overflow</a></li>
<li><a href="https://en.wikipedia.org/wiki/Executable_and_Linkable_Format">Executable and Linkable Format - Wikipedia</a></li>
<li><a href="https://docs.kernel.org/admin-guide/binfmt-misc.html">Kernel Support for miscellaneous Binary Formats (binfmt_misc) — The Linux Kernel documentation</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion likely includes reactions to the cleverness of the hack, with some users discussing the practicality and potential security implications. There may be debates about the usefulness of such a technique compared to traditional packaging methods.

**Tags**: `#SQLite`, `#ELF`, `#Linux`, `#executable`, `#file-format`

---

<a id="item-8"></a>
## [LLMs as Spatial Software Generators for Programmable 3D Objects](https://www.reddit.com/r/MachineLearning/comments/1vxcc1h/r_using_ai_as_a_spatial_software_generator_to/) ⭐️ 8.0/10

The paper introduces a novel approach that uses large language models (LLMs) to generate 3D objects as programmable software, rather than traditional mesh blobs. These objects are inherently animation-ready and can adapt their appearance based on compute environment. This approach could significantly impact 3D content creation, especially in industries like game development, industrial design, and AR/VR/XR, by making objects more flexible and easier to animate. It also suggests a trend where code-based 3D generation may eventually complement or replace traditional AI generators for certain use cases. The generated 3D objects have hierarchical structure and hinge/socket articulation, and can include logic to render differently on weak vs. powerful devices. However, they currently lag behind traditional AI 3D generators in creating complex organic shapes.

reddit · r/MachineLearning · /u/mhb_11 · Aug 24, 19:10

**Background**: Traditional AI 3D generators typically output monolithic mesh blobs that are difficult to animate or modify. Spatial programming is a concept where 3D objects are defined by code, allowing for programmatic control and flexibility. This paper leverages LLMs' growing capability in code generation to produce 3D objects as software, building on prior work like LLaMA-Mesh and pySpatial.

<details><summary>References</summary>
<ul>
<li><a href="https://pyspatial.github.io/">pySpatial: Generating 3D Visual Programs for Zero-Shot ...</a></li>
<li><a href="https://arxiv.org/abs/2506.11148">[2506.11148] LLM-to-Phy3D: Physically Conform Online 3D Object Generation with LLMs</a></li>
<li><a href="https://arxiv.org/html/2411.09595v1">LLaMA-Mesh: Unifying 3D Mesh Generation with Language Models</a></li>

</ul>
</details>

**Discussion**: The author's active engagement and provision of demos and code were positively received. Some commenters may have expressed interest in the trade-offs between organic shape complexity and programmability, but no specific comments were provided.

**Tags**: `#3D generation`, `#LLM`, `#spatial programming`, `#AI`, `#computer graphics`

---

<a id="item-9"></a>
## [Insilico Medicine Launches O3DC Open Alliance for AI Drug Discovery Benchmarks](https://news.google.com/rss/articles/CBMic0FVX3lxTE1nVE05VlZZQVI0OVVVME1ZdU5ZaHJHRkFqN1lpQ1lKS29Qa2VPLXo3UENzZ2t1RXYwUlhJTU5zYXJpVXJnOUtYel9VNTJjNGZGWEVfN016VDBPWEdocTBtVGFZUS1kMFljazR6eWZQU2ZrTjg?oc=5) ⭐️ 7.0/10

Insilico Medicine has initiated the formation of the O3DC (Open Drug Discovery and Development Consortium) open alliance, aimed at establishing benchmark quality standards for AI-driven drug discovery. The alliance will maintain a community-driven Benchmark Index mapping open benchmarks in the field. This initiative addresses the critical need for standardized, high-quality benchmarks in AI drug discovery, which is essential for reproducibility and real-world applicability. It could significantly improve how AI models are evaluated, benefiting researchers, pharmaceutical companies, and ultimately patients by accelerating the development of effective therapies. The O3DC Benchmark Index is a community-maintained resource that catalogs open benchmarks, including repositories, maintainers, live update status, and per-benchmark discussion. This collaborative approach aims to improve data quality and address the issue of models overfitting to benchmark scores rather than solving real-world drug discovery problems.

google_news · EurekAlert! · Aug 24, 19:11

**Background**: AI-driven drug discovery uses machine learning to accelerate the identification and development of new drugs. However, the field has faced challenges with data quality and benchmark standards, as models often achieve high scores on benchmarks but fail in practical applications. Insilico Medicine, a biotech company known for its generative AI platforms like Chemistry42, is taking a leading role in addressing these issues through the O3DC alliance.

<details><summary>References</summary>
<ul>
<li><a href="https://o3dc.org/">O 3 DC · Drug Discovery Benchmark Index</a></li>
<li><a href="https://divingintogeneticsandgenomics.com/post/ai-drug-discovery-data-quality-not-quantity/">AI in Drug Discovery : Data Quality , Not Quantity, Is the Bottleneck</a></li>
<li><a href="https://en.wikipedia.org/wiki/Insilico_Medicine">Insilico Medicine - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI`, `#drug discovery`, `#benchmarking`, `#open alliance`, `#biotech`

---

<a id="item-10"></a>
## [llm-anthropic 0.27 adds compatibility with anthropic v1.0.0](https://simonwillison.net/2026/Aug/24/llm-anthropic/) ⭐️ 5.0/10

llm-anthropic 0.27 has been released to ensure compatibility with the anthropic v1.0.0 Python library, which migrated from httpx to httpx2. The update was largely automated using Claude Code, with the resulting pull request available for review. This release is significant because it keeps the LLM plugin ecosystem functional with the latest Anthropic SDK, which is crucial for developers relying on LLM to interact with Claude models. The underlying shift from httpx to httpx2 reflects a broader industry trend, as OpenAI also adopted httpx2 in its v3.0.0 SDK, indicating a move towards more actively maintained HTTP clients. The anthropic v1.0.0 SDK requires Python 3.10 or later, up from 3.9, and its HTTP layer now uses httpx2, an API-compatible fork maintained by the Pydantic team. The migration was guided by Anthropic's official migration guide, and the author used Claude Code with the prompt 'Upgrade to anthropic>=1 - read MIGRATION.md and get the tests passing' to automate the process.

rss · Simon Willison · Aug 24, 16:27

**Background**: LLM is a command-line tool and Python library by Simon Willison that provides a unified interface for interacting with various large language models. Plugins like llm-anthropic extend LLM to support specific providers, such as Anthropic's Claude models. The anthropic Python SDK is the official library for accessing Claude, and its recent major version 1.0.0 introduced breaking changes, including the switch from httpx to httpx2. httpx2 is a continuation of the httpx project, which is no longer actively maintained, and is developed by the Pydantic team.

<details><summary>References</summary>
<ul>
<li><a href="https://pypi.org/project/httpx2/">httpx2 · PyPI</a></li>
<li><a href="https://github.com/pydantic/httpx2">GitHub - pydantic/httpx2: A next generation HTTP client for ...</a></li>
<li><a href="https://github.com/anthropics/anthropic-sdk-python/blob/main/MIGRATION.md">anthropic-sdk-python/MIGRATION.md at main · anthropics/anthropic-sdk-python</a></li>

</ul>
</details>

**Tags**: `#llm`, `#anthropic`, `#python`, `#sdk`, `#release`

---

<a id="item-11"></a>
## [Chinese Consumers Increasingly Use AI for Product Research](https://news.google.com/rss/articles/CBMizwFBVV95cUxPdllrWXMwZUd1Q1NueUZWdFotVlU0VUlHMGYzbGU2cy0xQzRHWWtEYVBKVjFzenhFbXRSLWk1eXV1eFJmVC1PWW5vM09jWEF0SWJzcnF1dTJpRzQ0S2F1SzZ4T3NDMmtrdkdiUjJja0xFMllFY1JEOWxyWUFhRTZTeEpHbjJLRElQcEVUdGIxUkJBeGVLTjlvVHVmSVdzbU1tVHZaTHg5bmZvN3p1S05aT1JVdDFCLWVtTHRpN3JJck9UMEtxSUwwNU00aHN1MkE?oc=5) ⭐️ 5.0/10

A recent report reveals that most Chinese consumers now consult AI before purchasing new products, a trend that is prompting brands to adapt their marketing and sales strategies. The report highlights a significant shift in consumer behavior driven by AI adoption. This trend signals a major shift in how consumers make purchasing decisions, with AI becoming a trusted advisor in the shopping journey. Brands that fail to integrate AI into their customer engagement strategies risk losing relevance in the Chinese market, which is a global leader in e-commerce and AI adoption. The report does not specify the exact percentage of consumers using AI, but it indicates that the majority now do so. Brands are adapting by incorporating AI tools into their customer service and product recommendation systems to meet this new consumer expectation.

google_news · 一财全球Yicai Global · Aug 24, 09:12

**Background**: AI-powered chatbots and recommendation engines have become increasingly common in e-commerce, helping consumers compare products, read reviews, and make informed decisions. In China, platforms like Alibaba and JD.com have integrated AI into their services, and consumers are now accustomed to using AI for pre-purchase research. This trend reflects the broader adoption of AI in daily life and its impact on consumer behavior.

**Tags**: `#AI`, `#consumer behavior`, `#China`, `#e-commerce`

---