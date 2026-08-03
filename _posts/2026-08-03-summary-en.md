---
layout: default
title: "Horizon Summary: 2026-08-03 (EN)"
date: 2026-08-03
lang: en
---

> From 30 items, 8 important content pieces were selected

---

1. [Karpathy Highlights Pelican Benchmark and LLM Physical World Gaps](#item-1) ⭐️ 8.0/10
2. [Kakehashi: Run macOS Binaries on Linux ARM via Userspace Translation](#item-2) ⭐️ 8.0/10
3. [Tech Giants and AI Leaders Clash Over Open-Weight Models](#item-3) ⭐️ 8.0/10
4. [Karpathy Stars sqliteai/waste: SQLite-Powered LLM Inference Engine](#item-4) ⭐️ 7.0/10
5. [F*: A General-Purpose Proof-Oriented Programming Language](#item-5) ⭐️ 7.0/10
6. [eBay harassment campaign leads to $56M payout and prison sentences](#item-6) ⭐️ 7.0/10
7. [NeurIPS 2026 Rebuttal Notification Glitch Leaves Authors in the Dark](#item-7) ⭐️ 7.0/10
8. [condense-json 1.0 Released with Non-Disruptive Fixes](#item-8) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Karpathy Highlights Pelican Benchmark and LLM Physical World Gaps](https://twitter.com/karpathy/status/2083749667410727319) ⭐️ 8.0/10

Andrej Karpathy shared a tweet about 'Pelican', sparking discussion on frontier LLMs' struggles with tasks like creating playable pinball games and the need for new benchmarks. The discussion highlights that even advanced models often fail at such tasks, with Opus 5 being the first to 'one shot' it in a harness. This matters because it underscores the limitations of current LLMs in physical world understanding, which is crucial for applications like game development and simulation. It also signals a shift toward more qualitative, behavior-based benchmarks that better measure real-world capabilities, potentially guiding future model development. The discussion references specific failures like walls blocking launch chutes, flippers pivoting incorrectly, and holes causing balls to drop. It also notes that Anthropic models may be specifically trained for three.js code generation, which could skew benchmark results, and suggests that qualitative/subjective measurements are necessary for such benchmarks.

hackernews · delichon · Aug 2, 04:05 · [Discussion](https://news.ycombinator.com/item?id=49140998)

**Background**: The 'Pelican' benchmark, popularized by Simon Willison, involves generating an SVG of a pelican riding a bicycle and has become an informal but widely used test for LLM capabilities. Similarly, the pinball game task is emerging as a benchmark for physical world understanding, as it requires arranging elements coherently to create a playable game. These benchmarks highlight that LLMs often struggle with tasks that require spatial reasoning and physical consistency, despite excelling in text-based reasoning.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/simonw/pelican-bicycle">GitHub - simonw/pelican-bicycle: LLM benchmark: Generate an SVG of a pelican riding a bicycle · GitHub</a></li>
<li><a href="https://dylancastillo.co/posts/pelicanmaxxing.html">Are AI labs pelicanmaxxing? – Dylan Castillo</a></li>
<li><a href="https://simonwillison.net/2025/Jun/6/six-months-in-llms/">The last six months in LLMs, illustrated by pelicans on bicycles</a></li>

</ul>
</details>

**Discussion**: Community comments express mixed sentiments: some highlight the poor end products as evidence of limitations, while others see them as a new benchmark for physical world understanding. There is also skepticism about models being specifically trained for certain tasks (e.g., three.js), which could inflate performance, and a call for qualitative measurements.

**Tags**: `#AI`, `#LLM`, `#benchmark`, `#Karpathy`, `#physical world understanding`

---

<a id="item-2"></a>
## [Kakehashi: Run macOS Binaries on Linux ARM via Userspace Translation](https://github.com/wie-project/kakehashi) ⭐️ 8.0/10

Kakehashi is an experimental userspace translation layer that enables macOS ARM64 binaries to run natively on Linux aarch64, with working prototypes for 7-Zip, curl, and Xcode Git tools. It loads Darwin Mach-O files, maps a freestanding libSystem, and translates BSD syscalls without a JIT. This project addresses a significant technical challenge in cross-OS binary compatibility, potentially enabling macOS CLI tools to run on Linux ARM hardware. If successful, it could expand the Linux ecosystem by providing access to macOS-specific software, similar to how Wine/Proton did for Windows applications. The project is CLI-first and does not use a JIT, focusing on translating BSD syscalls and providing a freestanding libSystem. Current performance shows 7-Zip running about 5.2x slower than native Linux, but the author has a clear optimization plan. The project is available on GitHub and can be installed via cargo install kakehashi.

hackernews · vlad_kalinkin · Aug 2, 16:26 · [Discussion](https://news.ycombinator.com/item?id=49145937)

**Background**: Binary compatibility between operating systems is challenging because each OS has its own kernel interfaces, system call conventions, and runtime libraries. Projects like Wine and Darling attempt to provide such compatibility by translating API calls and system calls. Kakehashi specifically targets macOS ARM64 binaries on Linux aarch64, leveraging the shared ARM architecture to simplify the translation process.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/wie-project/kakehashi">wie-project/ kakehashi : Userspace macOS translation layer for Linux ...</a></li>
<li><a href="https://savepearlharbor.com/?p=489422">Kakehashi : запуск macOS бинарников на Linux ARM . Часть...</a></li>

</ul>
</details>

**Discussion**: The community shows strong interest and optimism, with users comparing it to Darling and suggesting potential collaborations. Some express curiosity about the technical approach, such as whether a virtualization framework could be simpler if it didn't require redistributable libraries. Others hope for future applications like running Audio Unit binaries on Linux via a yabridge-like layer.

**Tags**: `#macOS`, `#Linux`, `#ARM`, `#binary compatibility`, `#userspace`

---

<a id="item-3"></a>
## [Tech Giants and AI Leaders Clash Over Open-Weight Models](https://simonwillison.net/2026/Aug/2/open-letters/#atom-everything) ⭐️ 8.0/10

Microsoft spearheaded an open letter titled 'Open Weights and American AI Leadership' dated July 24, 2026, signed by over 235 companies including NVIDIA, Amazon, and OpenAI, advocating for open-weight AI models. In contrast, Anthropic published its own position three days later, expressing concerns about risks and calling for a crackdown on distillation, while a separate letter 'Pacing the Frontier' signed by 1,324 employees of frontier AI companies urged the U.S. government to support international efforts to pace automated AI development. This debate highlights a critical policy crossroads for AI development, pitting open-source advocates against safety-focused concerns, with major industry players taking sides. The outcome could shape U.S. regulations on open-weight models, affecting innovation, competition, and global AI leadership. The Microsoft letter explicitly supports distillation, a practice some see as potential misappropriation, and notably lacks Anthropic's signature. Anthropic's response, led by CEO Dario Amodei, warns of risks from authoritarian governments and calls for a crackdown on industrial-scale distillation, while clarifying it has never advocated for a ban on open-weights models.

rss · Simon Willison · Aug 2, 04:16

**Background**: Open-weight models are AI models whose trained parameters are publicly released, allowing anyone to download, inspect, and modify them, though redistribution rights depend on the license. This contrasts with closed models, which are kept proprietary. The debate centers on balancing transparency and innovation against potential misuse and national security risks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/">Open Weights and American AI Leadership</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/wp-content/uploads/2026/07/open-weight-models-letter-1.pdf">Open Weights and American AI Leadership July 24, 2026</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open source`, `#policy`, `#industry`, `#Simon Willison`

---

<a id="item-4"></a>
## [Karpathy Stars sqliteai/waste: SQLite-Powered LLM Inference Engine](https://github.com/sqliteai/waste) ⭐️ 7.0/10

Andrej Karpathy starred the sqliteai/waste repository on GitHub, highlighting a project that runs the 2.78-trillion-parameter Kimi K3 model beyond available RAM by streaming activated weights directly from NVMe. The project is a dependency-free, embeddable C inference engine released under the Apache 2.0 license. This star from a prominent AI figure signals high relevance and could accelerate adoption of the project, which addresses the growing need to run large language models on limited hardware. By leveraging SQLite and NVMe, it offers a novel approach that may influence future inference engine designs and edge AI deployments. The waste engine streams activated weights from NVMe, avoiding the need to load the entire model into RAM, and is designed to be dependency-free and embeddable. It is part of the SQLite AI ecosystem, which includes extensions like sqlite-ai and sqlite-agent for on-device inference and autonomous agents.

github · karpathy · Aug 2, 17:19

**Background**: SQLite is a widely used embedded SQL database engine, and the SQLite AI project aims to transform it into an AI-native database for edge devices, adding features like on-device inference and agent support. Running trillion-parameter models typically requires massive GPU memory, but streaming weights from storage can enable inference on consumer hardware, though with potential latency trade-offs.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/sqliteai/waste">GitHub - sqliteai/waste: Run the full 2.78-trillion-parameter Kimi K3 model beyond available RAM by streaming activated weights directly from NVMe. A dependency-free, embeddable C inference engine. · GitHub</a></li>
<li><a href="https://marcobambini.substack.com/p/the-waste-inference-engine">The WASTE inference engine - Marco Bambini</a></li>
<li><a href="https://www.sqlite.ai/">SQLite AI - Smart Edge Databases with Cloud Sync and Intelligence</a></li>

</ul>
</details>

**Tags**: `#GitHub`, `#SQLite`, `#AI`, `#Karpathy`, `#Open Source`

---

<a id="item-5"></a>
## [F*: A General-Purpose Proof-Oriented Programming Language](https://fstar-lang.org/) ⭐️ 7.0/10

F* is a general-purpose, proof-oriented programming language that supports both purely functional and effectful programming, and it has gained attention in the Hacker News community with 146 points and 64 comments. The language is designed for program verification, allowing developers to write mathematical proofs as part of their code. F* is significant because it bridges the gap between real-world software development and formal verification, making it possible to prove the correctness of critical systems such as cryptographic protocols and security-sensitive code. Its academic and industrial relevance, including contributions from Microsoft Research, highlights its potential impact on software reliability. F* is a joint project of Microsoft Research and the French Institute for Research in Computer Science (INRIA), and it is inspired by ML, Caml, and OCaml. It is a dependently typed language, similar to Coq and Agda, but designed to be more practical for real-world software verification.

hackernews · ducktective · Aug 2, 12:31 · [Discussion](https://news.ycombinator.com/item?id=49143925)

**Background**: Formal verification is the process of mathematically proving that a system behaves correctly according to its specification. F* is a proof-oriented programming language that integrates this capability directly into the programming language, allowing developers to write proofs alongside their code. This approach is particularly valuable for high-assurance software, such as cryptographic protocols and safety-critical systems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F*_(programming_language)">F* (programming language) - Wikipedia</a></li>
<li><a href="https://fstar-lang.org/">F*: A Proof-Oriented Programming Language</a></li>
<li><a href="https://github.com/FStarLang/FStar">GitHub - FStarLang/FStar: A Proof-oriented Programming Language · GitHub</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion shows mixed sentiment: some users appreciate F*'s ability to express external library calls and incremental migration from C, while others criticize the lack of code examples on the homepage and question its industry adoption. A user also humorously noted that responsive stylesheets cannot be implemented without side effects, referencing F*'s effectful programming support.

**Tags**: `#programming language`, `#formal verification`, `#proof-oriented`, `#functional programming`, `#F*`

---

<a id="item-6"></a>
## [eBay harassment campaign leads to $56M payout and prison sentences](https://www.ft.com/content/06ec1b03-d4af-40cf-b12a-4ba5a410f6d2) ⭐️ 7.0/10

eBay has agreed to pay $56 million to David and Ina Steiner, a couple targeted by a harassment campaign orchestrated by eBay's former security executives, who have also received prison sentences. The campaign included sending threatening messages, surveillance, and even a delivery of a bloody pig mask to the couple's home. This case highlights the severe consequences of corporate misconduct and the potential for security teams to abuse their power, raising questions about accountability in tech companies. It also serves as a warning about the lengths companies might go to silence critics, impacting public trust in corporate governance. Seven members of eBay's security team, including former police captains, were involved in the campaign against the Steiners, who published a newsletter critical of eBay. The sentencing included 57 months for former Senior Director Jim Baugh, while others received lesser sentences, and the $56 million settlement was announced in 2024.

hackernews · JumpCrisscross · Aug 2, 19:19 · [Discussion](https://news.ycombinator.com/item?id=49147435)

**Background**: The Steiners ran a newsletter called 'eBay's EcommerceBytes' that was critical of eBay, leading to the harassment campaign in 2019. The campaign included sending disturbing items like a bloody pig mask and a book about surviving a spouse's murder, as well as surveillance and threats. The case underscores the importance of ethical conduct in corporate security operations and the legal repercussions for those who overstep.

**Discussion**: Commenters expressed skepticism that the harassment was limited to the Steiners, questioning if other critics were targeted. Some also raised concerns about the involvement of former police officers and the broader implications for corporate accountability, while others diverted to discussing eBay's high fees compared to competitors.

**Tags**: `#eBay`, `#harassment`, `#corporate accountability`, `#legal`, `#security`

---

<a id="item-7"></a>
## [NeurIPS 2026 Rebuttal Notification Glitch Leaves Authors in the Dark](https://www.reddit.com/r/MachineLearning/comments/1vdu92a/neurips_2026_acs_and_reviewers_have_disappeared_d/) ⭐️ 7.0/10

A NeurIPS 2026 author reports that rebuttals submitted via the 'Rebuttal' button before the official discussion period (Jul 27 AoE) failed to trigger notifications to reviewers and ACs, resulting in complete silence from all four reviewers and the AC. The issue also affected authors who are reviewing other papers, as they received no email notifications for early rebuttals on papers they were reviewing. This issue could undermine the fairness of the NeurIPS review process, as early rebuttals may be overlooked, potentially affecting paper acceptance decisions. It highlights a systemic flaw in the conference's notification system that could impact many authors and reviewers in the current cycle. The author tried several workarounds, including meta-comments visible to everyone, reviewer reminders, and emailing the PCs, but with only about one day left in the discussion period, they are uncertain how to proceed. The post is tagged with [D] (discussion), and the author mentions they had hoped for an oral or spotlight presentation based on initial scores.

reddit · r/MachineLearning · /u/extricableforsythia · Aug 2, 21:33

**Background**: NeurIPS (Conference on Neural Information Processing Systems) is a top-tier machine learning conference. Its review process typically includes a rebuttal period where authors can respond to reviewer comments, and an author-reviewer-AC discussion period. Notifications are usually sent via email when new comments or rebuttals are posted, but this incident suggests a bug in the system that prevented such notifications for early submissions.

<details><summary>References</summary>
<ul>
<li><a href="https://neurips.cc/Conferences/2025/ReviewerGuidelines">2025 Reviewer Guidelines</a></li>
<li><a href="https://neurips.cc/Conferences/2025/AC-Guidelines">NeurIPS 2025 AC Guidelines</a></li>

</ul>
</details>

**Tags**: `#NeurIPS`, `#peer review`, `#conference`, `#rebuttal`, `#academic publishing`

---

<a id="item-8"></a>
## [condense-json 1.0 Released with Non-Disruptive Fixes](https://simonwillison.net/2026/Aug/2/condense-json/#atom-everything) ⭐️ 5.0/10

Simon Willison announced the 1.0 release of condense-json, a Python library for condensing JSON data. The release includes sensible, non-disruptive fixes after a year and a half of development. This release marks a milestone for a utility that helps reduce JSON size by replacing repeated substrings, which is particularly useful for storing LLM-generated logs efficiently. It demonstrates a mature, stable tool that developers can rely on for production use. The library provides condense_json and uncondense_json functions that use a replacements dictionary to substitute substrings with a compact syntax like {"$r": [...]}. It is used in Simon Willison's LLM project to save space in SQLite logs, as seen in PR #1586.

rss · Simon Willison · Aug 2, 22:19

**Background**: condense-json is a Python library that condenses JSON by replacing repeated substrings with shorter references, making the output more compact. It is particularly useful when storing JSON that contains duplicated data from related structures, such as logs from LLM tools. The 1.0 release signifies stability after a period of real-world usage.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/simonw/condense-json">GitHub - simonw/condense-json: Python function for condensing JSON using replacement strings · GitHub</a></li>
<li><a href="https://pypi.org/project/condense-json/">condense-json · PyPI</a></li>

</ul>
</details>

**Tags**: `#JSON`, `#Python`, `#library`, `#release`

---