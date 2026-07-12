---
layout: default
title: "Horizon Summary: 2026-07-12 (EN)"
date: 2026-07-12
lang: en
---

> From 29 items, 7 important content pieces were selected

---

1. [vLLM v0.25.0: Model Runner V2 Default, PagedAttention Removed](#item-1) ⭐️ 9.0/10
2. [World's first remote pig gallbladder surgery with humanoid robot](#item-2) ⭐️ 9.0/10
3. [VultronRetriever Models Top MTEB Leaderboard](#item-3) ⭐️ 8.0/10
4. [Apple Sues OpenAI Over Trade Secret Theft](#item-4) ⭐️ 8.0/10
5. [Trump Administration Pushes Intel Revival, Apple to Use Its Chips](#item-5) ⭐️ 8.0/10
6. [6 U-Boot Flaws Allow Code Execution Before OS Boot](#item-6) ⭐️ 8.0/10
7. [Identity Layer for AI Agents Finally Being Built](#item-7) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0: Model Runner V2 Default, PagedAttention Removed](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 makes Model Runner V2 the default execution path for all dense models, removes the legacy PagedAttention implementation, and introduces a new Streaming Parser Engine for tool-call and reasoning parsing. This release marks a major architectural shift in vLLM, improving performance and modularity while simplifying the codebase. The removal of PagedAttention and the maturation of Model Runner V2 will benefit all users of this widely-used LLM inference engine. The release includes 558 commits from 232 contributors, adds support for new models like LLaVA-OneVision-2 and GLM-5, and introduces universal speculative decoding for heterogeneous vocabularies. The Transformers modeling backend is now as fast as native vLLM.

github · khluu · Jul 11, 20:06

**Background**: vLLM is an open-source high-throughput LLM inference engine that uses PagedAttention for efficient memory management. Model Runner V2 is a redesigned execution core that addresses design flaws in the original V1 architecture, offering better modularity and performance. The removal of legacy PagedAttention indicates that the new attention backends (V1/MRv2) are now mature enough to replace it.

<details><summary>References</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/v0.22.1/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#open source`, `#release`, `#AI/ML`

---

<a id="item-2"></a>
## [World's first remote pig gallbladder surgery with humanoid robot](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 9.0/10

Surgeons remotely operated a Unitree G1 humanoid robot to perform the world's first laparoscopic cholecystectomy on live pigs, with results published in Nature. This demonstrates that low-cost general-purpose humanoid robots can perform complex surgical tasks, potentially expanding access to robotic surgery in remote, rural, battlefield, or space settings. The Unitree G1 base model costs $13,500, or about $67,000 with dexterous hands, far less than specialized systems like the da Vinci (over $500,000). The robot is 1.5 meters tall and weighs 27 kg.

telegram · zaihuapd · Jul 11, 02:29

**Background**: Laparoscopic cholecystectomy is a minimally invasive surgery to remove the gallbladder, commonly performed for gallstones. The da Vinci Surgical System is a widely used robotic platform for such procedures but costs hundreds of thousands to millions of dollars. The Unitree G1 is a general-purpose humanoid robot designed for locomotion and manipulation, not originally intended for surgery.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G1_Humanoid Robot Functions ... - Unitree G1</a></li>
<li><a href="https://en.wikipedia.org/wiki/Laparoscopic_cholecystectomy">Laparoscopic cholecystectomy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Da_Vinci_Surgical_System">Da Vinci Surgical System</a></li>

</ul>
</details>

**Tags**: `#robotics`, `#surgery`, `#humanoid robot`, `#medical technology`, `#remote operation`

---

<a id="item-3"></a>
## [VultronRetriever Models Top MTEB Leaderboard](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

VultronRetriever, a new family of retrieval models, has been released on HuggingFace, achieving #1 on the MTEB leaderboard with up to 16x smaller index and 12x higher throughput, and running fully offline on iPhone. This breakthrough enables highly efficient, on-device retrieval for mobile and edge devices, potentially transforming applications like offline Q&A and document search while reducing infrastructure costs. The family includes three models: Prime-8B (global #1), Core-4.5B (outperforms models twice its size), and Flash-0.8B (runs cool on edge, indexes 60 images/min offline). They use Hydra Architecture for late interaction retrieval with half the memory of comparable models.

reddit · r/MachineLearning · /u/madkimchi · Jul 11, 15:22

**Background**: MTEB (Massive Text Embedding Benchmark) is a popular leaderboard for evaluating embedding models on retrieval and other tasks. Late interaction retrieval, pioneered by ColBERT, uses token-level representations for precise matching. Hydra Architecture unifies retrieval and generation in a single model.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://arxiv.org/html/2603.28554">Hydra: Unifying Document Retrieval and Generation in a Single Vision-Language Model</a></li>
<li><a href="https://weaviate.io/blog/late-interaction-overview">An Overview of Late Interaction Retrieval Models: ColBERT ...</a></li>

</ul>
</details>

**Tags**: `#retrieval`, `#MTEB`, `#embedding`, `#on-device AI`, `#NLP`

---

<a id="item-4"></a>
## [Apple Sues OpenAI Over Trade Secret Theft](https://www.cnbc.com/2026/07/10/apple-openai-lawsuit-trade-secrets.html) ⭐️ 8.0/10

On July 10, 2026, Apple filed a lawsuit in the U.S. District Court for the Northern District of California against OpenAI, two former employees, and io Products, accusing them of systematically stealing trade secrets related to product design, manufacturing processes, and supply chain to accelerate OpenAI's consumer hardware development. This lawsuit highlights escalating tensions between major tech companies over AI hardware competition, and could set a precedent for how trade secret laws apply to employee mobility and AI hardware development. Apple alleges that former employee Chang Liu accessed internal networks and downloaded dozens of hardware files after leaving, and that OpenAI's hardware head Tang Yew Tan sent supplier information to his personal email before resigning and asked job candidates to bring Apple components to interviews. Apple also claims over 400 former employees now work at OpenAI.

telegram · zaihuapd · Jul 11, 03:14

**Background**: OpenAI acquired io Products in May 2025, a hardware company co-founded by former Apple designer Jony Ive and others, to lead its hardware product development. The lawsuit centers on allegations that OpenAI systematically recruited Apple employees and accessed confidential information to build its own consumer hardware, competing directly with Apple.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Io_Products">Io Products</a></li>
<li><a href="https://aijourn.com/iyo-sues-former-engineer-after-io-founder-tang-yew-tan-admits-to-receiving-trade-secrets-from-him/">Iyo sues former engineer after io founder tang yew ...</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#OpenAI`, `#lawsuit`, `#trade secrets`, `#AI hardware`

---

<a id="item-5"></a>
## [Trump Administration Pushes Intel Revival, Apple to Use Its Chips](https://www.wsj.com/tech/the-white-house-intel-trump-apple-84fe833e) ⭐️ 8.0/10

The Trump administration has secured Apple as a customer for Intel's chip manufacturing and converted a $9 billion federal grant into a 10% equity stake in Intel, making the government the largest shareholder. This intervention marks a significant shift in US semiconductor policy, with the government taking an active ownership role to revive a domestic chipmaker and reduce reliance on foreign manufacturing. Intel's CEO Lip-Bu Tan meets monthly with the Commerce Department, and the government's chip director receives quarterly briefings from Intel's CFO. Since Tan took over in March 2025, Intel's stock has tripled.

telegram · zaihuapd · Jul 11, 05:54

**Background**: The US government has been seeking to boost domestic semiconductor production through the CHIPS Act and other policies. Intel, once a dominant chipmaker, has struggled in recent years, losing market share to competitors like TSMC and AMD.

<details><summary>References</summary>
<ul>
<li><a href="https://edition.cnn.com/2025/08/19/tech/bessent-intel-government-stake">The Trump administration confirms it’s seeking a stake in Intel . Why?</a></li>
<li><a href="https://www.dailymotion.com/video/x9p5ji4">White House Confirms Talks To Take 10 % Intel Stake</a></li>
<li><a href="https://techcrunch.com/2025/09/26/the-trump-administration-is-going-after-semiconductor-imports/">The Trump administration is going after semiconductor imports</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#Intel`, `#Apple`, `#US policy`, `#chip manufacturing`

---

<a id="item-6"></a>
## [6 U-Boot Flaws Allow Code Execution Before OS Boot](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

Binarly disclosed six vulnerabilities in U-Boot's FIT signature verification, two of which allow arbitrary code execution and four that cause device crashes, affecting versions since 2013.07. These flaws enable attackers to execute malicious code before the operating system boots, bypassing security software and potentially compromising embedded devices permanently, especially those with remote firmware update capabilities. The two code-execution bugs (BRLY-2026-037 and BRLY-2026-038) stem from an unchecked value in fdt_get_name, while the recursion flaw (BRLY-2026-042) can exhaust stack memory. Patches have been accepted upstream but require vendor integration.

telegram · zaihuapd · Jul 11, 08:32

**Background**: U-Boot is a widely used bootloader for embedded systems, responsible for loading the operating system. FIT (Flattened Image Tree) is a format for packaging multiple firmware components with cryptographic signatures to ensure authenticity. The vulnerabilities reside in the signature verification code, allowing a crafted FIT image to bypass checks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/">New U-Boot flaws could enable stealthy firmware attacks</a></li>
<li><a href="https://thehackernews.com/2026/07/six-new-u-boot-flaws-could-let.html">Six New U-Boot Flaws Could Let Malicious Images Crash Devices or Run Code at Boot</a></li>
<li><a href="https://gbhackers.com/multiple-u-boot-vulnerabilities/">Multiple U-Boot Vulnerabilities Enable Pre-Authentication Code Execution and Device DoS Attacks</a></li>

</ul>
</details>

**Tags**: `#security`, `#U-Boot`, `#firmware`, `#vulnerability`, `#bootloader`

---

<a id="item-7"></a>
## [Identity Layer for AI Agents Finally Being Built](https://news.google.com/rss/articles/CBMijwFBVV95cUxNQ2tDUjVMR1I4Z2RkYlhTZWhHaEJuT1Z4X2FGcXhxMzFBX3VtSjhwWlk2bTM3aTRUeWFaUVI3SWl3ZlVDb1hCTmtRQWIwWTRsbmtTTHRxdDNBWXY3eFhCZUY4LUQySXdpMGZza3RsNndUYnI0M1IwYzNoZFR2dTdTN0NjZTdqbS1TVFVZcXFBUQ?oc=5) ⭐️ 7.0/10

Between March and July 2026, the concept of an identity layer for AI agents transitioned from abstract discussion to concrete implementation, appearing in protocol releases, enterprise features, and research papers. Open-source projects like notme.bot now provide cryptographic identities for AI agents, separate from human bearer tokens. This development is critical because AI agents currently lack a standardized identity mechanism, leading to security risks and integration challenges. A dedicated identity layer enables secure delegation, access control, and auditability for autonomous AI systems, which is essential for enterprise adoption and multi-agent ecosystems. The identity layer uses decentralized identifiers (DIDs) and zero-trust principles, as outlined by the Cloud Security Alliance's new IAM framework for agentic AI. Guardian agents serve as an autonomous control layer that governs identity and behavior of AI agents at the execution layer.

google_news · HackerNoon · Jul 11, 19:25

**Background**: AI agents are autonomous programs that perform tasks on behalf of users, but they have traditionally relied on human credentials (e.g., API keys) for authentication, creating security gaps. An identity layer gives each agent a unique, verifiable cryptographic identity, enabling fine-grained access control and audit trails. This is analogous to how email became the identity layer for humans on the internet.

<details><summary>References</summary>
<ul>
<li><a href="https://hackernoon.com/the-identity-layer-for-ai-agents-is-finally-being-built">hackernoon.com/the- identity - layer - for - ai - agents -is-finally-being-built</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/agentic-ai-identity-and-access-management-a-new-approach">Agentic AI Identity & Access Management | CSA</a></li>
<li><a href="https://thehackernews.com/2026/06/guardian-agents-next-layer-of-identity.html">Guardian Agents: The Next Layer of Identity Governance</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#identity`, `#infrastructure`, `#security`

---