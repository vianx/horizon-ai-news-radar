---
layout: default
title: "Horizon Summary: 2026-09-14 (EN)"
date: 2026-09-14
lang: en
---

> From 36 items, 9 important content pieces were selected

---

1. [Fable 5.1 Solves the 370-Year-Old Cyphral Distich Cipher](#item-1) ⭐️ 8.0/10
2. [Why Google Still Serves Scam Ads Despite Complaints](#item-2) ⭐️ 8.0/10
3. [Cars Collect and Sell Driver Data to Third Parties, Sparking Privacy Debate](#item-3) ⭐️ 8.0/10
4. [Perplexity trusts GPT-6 Astra with end-to-end systems](#item-4) ⭐️ 8.0/10
5. [CUDA Moat: AMD's DeepSeek v4.1 Performance Lags Up to 42x](#item-5) ⭐️ 8.0/10
6. [Homebrew 7.0.0 ships official native macOS GUI](#item-6) ⭐️ 8.0/10
7. [Kirin 9050 Pro Review: 3D Stacking Boosts Performance and Efficiency](#item-7) ⭐️ 8.0/10
8. [Simon Willison releases commit-rewriter 0.1 for cleaning up commit messages](#item-8) ⭐️ 6.0/10
9. [Z.AI Plans US$5.0 Billion Fund-Raising to Fuel AI Expansion](#item-9) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Fable 5.1 Solves the 370-Year-Old Cyphral Distich Cipher](https://www.vals.ai/blogs/fable-solves-cyphral-distich) ⭐️ 8.0/10

Vals AI researcher Geby Jaff reported that Claude Fable 5.1, Anthropic's newly released model, solved the Cyphral Distich — a 64-number cryptogram printed at the end of Sir Thomas Urquhart's 1653 book Logopandecteision. The writeup went viral on Hacker News with over 260 points and 80+ comments, and the solution was described as embarrassingly simple in hindsight. This is a notable milestone in AI-assisted cryptanalysis, showing that large language models can tackle historical puzzles that have resisted human experts for centuries. It also fuels the broader debate about whether AI's growing problem-solving ability reflects genuine reasoning or merely relentless brute-force persistence. The Cyphral Distich consists of two lines of 32 numbers each and appears on Klaus Schmeh's Top 50 unsolved encrypted messages list; the solution reportedly required no exotic technique, just persistence. Commenters noted that Fable 5.1 often falls back to the underlying Opus 5 model on such problems, and that many unsolved ciphers may simply have suffered from a lack of human attention.

hackernews · u1hcw9nx · Sep 13, 21:06 · [Discussion](https://news.ycombinator.com/item?id=49688695)

**Background**: A cryptogram is a short message deliberately encoded so it cannot be read without knowing the rule that produced it. Sir Thomas Urquhart was a 17th-century Scottish writer, and his 1653 book Logopandecteision ended with this numeric puzzle, which remained unsolved for roughly 370 years. Klaus Schmeh is a cryptography researcher whose blog catalogues the world's most famous unsolved encrypted messages, making them a common benchmark for testing new decryption methods.

<details><summary>References</summary>
<ul>
<li><a href="https://www.vals.ai/blogs/fable-solves-cyphral-distich">Claude Fable 5.1 Solves the Cyphral Distich - Vals AI</a></li>
<li><a href="https://www.explainx.ai/blog/claude-fable-5-1-solves-cyphral-distich-cipher-2026">Claude Fable 5.1 Solves 370-Year-Old Cipher (2026 ...</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Commenters were divided: some shared anecdotes of ChatGPT cracking personal ciphers in minutes, while others argued the result looks more like brute-force persistence than intelligence. A recurring theme was that many recent AI 'solves' may reflect low-hanging fruit and decades of human inattention rather than a leap in capability, alongside broader ambivalence about AI's trajectory.

**Tags**: `#AI`, `#cryptography`, `#cipher-solving`, `#Hacker News`, `#LLM`

---

<a id="item-2"></a>
## [Why Google Still Serves Scam Ads Despite Complaints](https://www.atomic14.com/2026/09/13/why-is-google-still-serving-dodgy-ads) ⭐️ 8.0/10

An article on atomic14.com, discussed on Hacker News with 555 upvotes and 263 comments, examines why Google continues to serve scam and deceptive ads despite widespread complaints. The discussion highlights that Google's domain-blocking system treats domains like azurestaticapps.net and netlify.app as TLDs, preventing publishers from blocking scam ads that rotate subdomains daily. This matters because Google's ad network powers a vast portion of the web, and its failure to curb scam ads affects millions of publishers and users, raising questions about platform accountability and the need for strict liability. The discussion suggests that AI-generated scam ads are proliferating, potentially eroding trust in digital advertising and prompting regulatory scrutiny. Google reportedly does not allow blocking of certain domains because it considers them TLDs, and scammers exploit this by using a new subdomain daily, such as abc.azurestaticapps.net. Additionally, a commenter who spent over $100 million on Google Ads claims Google is aggressively juicing revenue, possibly to mask AI losses and ahead of AI disrupting its ad business.

hackernews · iamflimflam1 · Sep 13, 17:37 · [Discussion](https://news.ycombinator.com/item?id=49686445)

**Background**: Google Ads is the dominant online advertising platform, and publishers often rely on it for revenue through programs like AdSense. Ad fraud detection typically involves monitoring traffic and click patterns, but scammers constantly evolve tactics, such as using free hosting subdomains, making it hard for automated systems to block them. Platform accountability efforts, like the IAB Tech Lab's Accountability Platform, aim to bring transparency to the ad supply chain, but enforcement remains challenging.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anura.io/ad-fraud-ultimate-guide/how-to-detect-ad-fraud">How to Detect Ad Fraud : Key Signs and Strategies | Anura</a></li>
<li><a href="https://iabtechlab.com/standards/accountability-platform/">Accountability Platform - IAB Tech Lab</a></li>

</ul>
</details>

**Discussion**: Commenters expressed frustration with Google's ad ecosystem, with one publisher describing thousands of scam ads on their site and another calling for strict liability, saying Google is complicit. Some speculated that Google is prioritizing short-term revenue due to AI competition, while others noted that AI-generated scam ads are rampant on YouTube and that Google's review process is overwhelmed.

**Tags**: `#Google Ads`, `#Ad Fraud`, `#Online Advertising`, `#Platform Accountability`, `#Web Security`

---

<a id="item-3"></a>
## [Cars Collect and Sell Driver Data to Third Parties, Sparking Privacy Debate](https://www.theverge.com/column/994172/your-car-is-selling-your-data) ⭐️ 8.0/10

A Verge article highlights how modern cars collect driver data and sell it to third parties, prompting a Hacker News discussion with 287 points and 153 comments. Community members shared personal experiences, legislative updates like California's AB-1542, and technical distinctions between car facts and driver data. This issue affects millions of drivers whose sensitive location and behavior data may be monetized without meaningful consent, raising significant privacy and safety concerns. It also underscores gaps in current data protection laws and the need for stronger regulation of automotive data practices. One commenter noted that even after disabling data collection in a Volkswagen's companion app and infotainment system, a Carfax request still surfaced mileage data, suggesting collection persists through other channels. Another pointed out that California's AB-1542 would classify geolocation data within a 1850-foot radius as sensitive, potentially banning its sale.

hackernews · bookofjoe · Sep 13, 13:45 · [Discussion](https://news.ycombinator.com/item?id=49683953)

**Background**: Connected cars are equipped with sensors and internet connectivity that collect a wide range of data, including location, speed, and driving patterns. Automakers often share or sell this data to third parties such as insurers, data brokers, and marketers, sometimes with unclear consent. In the US, privacy laws like the California Consumer Privacy Act (CCPA) and proposed bills like AB-1542 aim to give consumers more control, but enforcement remains limited.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ftc.gov/policy/advocacy-research/tech-at-ftc/2024/05/cars-consumer-data-unlawful-collection-use">Cars & Consumer Data: On Unlawful Collection & Use | Federal Trade Commission</a></li>
<li><a href="https://www.consumerreports.org/electronics/personal-information/how-to-stop-your-car-from-collecting-sharing-driving-data-a1233378612/">Stop Your Car From Collecting and Sharing Your Driving Data - Consumer Reports</a></li>
<li><a href="https://www.monda.ai/blog/automotive-data-monetization">Automotive Data Monetization: Trends & Examples 2025 | Monda</a></li>

</ul>
</details>

**Discussion**: Commenters expressed frustration over the difficulty of stopping data collection, with one sharing a detailed account of disabling features yet still finding data shared. Another distinguished between 'car facts' (VIN, odometer) and 'driver data' (speed, location), arguing the latter should be banned rather than anonymized. There was also discussion of legislative efforts like AB-1542 and technical measures such as Faraday cages.

**Tags**: `#privacy`, `#automotive`, `#data collection`, `#regulation`, `#surveillance`

---

<a id="item-4"></a>
## [Perplexity trusts GPT-6 Astra with end-to-end systems](https://openai.com/index/perplexity-improving-accuracy-with-astra) ⭐️ 8.0/10

Perplexity is now using OpenAI's GPT-6 Astra to autonomously write communications, modify software, and monitor production systems, checking in with humans far less often than with earlier models. OpenAI published a case study describing this deployment, highlighting Astra's ability to handle end-to-end operational tasks with reduced human oversight. This marks a significant shift toward trusting frontier AI models with critical production responsibilities, potentially setting a precedent for how enterprises integrate autonomous agents into their operations. If widely adopted, it could reshape software engineering, DevOps, and corporate communications workflows across the industry. GPT-6 Astra was released as a limited preview on September 3, 2026, and is OpenAI's first model to reach the Critical level of cybersecurity capability under its Preparedness Framework. Astra is rolling out to a limited set of organizations and will become available to ChatGPT Plus, Pro, Business, and Enterprise users, as well as through the OpenAI API, Microsoft Azure, and AWS Bedrock.

rss · OpenAI Blog · Sep 14, 00:00

**Background**: Perplexity AI is an American company known for its AI-powered answer engine that synthesizes real-time responses to user queries. GPT-6 Astra is OpenAI's latest frontier model, released after a delay following the Hugging Face incident in July 2026, which prompted additional safeguards. The deployment illustrates a growing trend of AI agents taking on autonomous roles in production environments, moving beyond simple chat interactions.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-astra/">GPT-6 Astra: A new generation of intelligence | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Perplexity_AI">Perplexity AI - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI`, `#GPT-6`, `#Perplexity`, `#autonomous systems`, `#OpenAI`

---

<a id="item-5"></a>
## [CUDA Moat: AMD's DeepSeek v4.1 Performance Lags Up to 42x](https://x.com/SemiAnalysis_/status/2098618867035557984) ⭐️ 8.0/10

SemiAnalysis reported that AMD released its DeepSeek v4.1 Flash image two days after CUDA vLLM support arrived, and that AMD's per-dollar performance trails NVIDIA's H200 by up to 14.8x and the B200/B300 by up to 42x. The image works out of the box, but the gap is purely one of economics and optimization maturity. The numbers quantify how much NVIDIA's CUDA ecosystem still buys in day-one optimization, which directly affects AI infrastructure procurement decisions and the total cost of ownership for anyone considering AMD accelerators. It suggests that raw hardware competitiveness alone is not enough to dislodge CUDA's position in AI workloads. The comparison is framed as per-dollar performance rather than raw throughput, meaning AMD's disadvantage reflects both software optimization gaps and price-to-performance economics. The two-day delay in shipping a working DeepSeek v4.1 Flash image illustrates how quickly NVIDIA's ecosystem can turn around support for new model releases.

telegram · zaihuapd · Sep 13, 05:55

**Background**: CUDA is NVIDIA's proprietary parallel computing platform and programming model, backed by millions of developers and thousands of GPU-accelerated libraries, which is widely described as a four-layer moat spanning programming model, ecosystem libraries, kernel compilers, and talent. DeepSeek v4.1 Flash is a newly released large language model that natively adds multimodal capabilities, compresses KV cache, and lowers pricing, replacing the earlier V4 Pro. SemiAnalysis is an independent research firm focused on semiconductors and AI infrastructure, known for accelerator benchmarks and AI cloud TCO models.

<details><summary>References</summary>
<ul>
<li><a href="https://irishemin.github.io/knowledge_base/ai-learning/2026/10/22/ai-learning-s2ep17-cuda-moat/">⚙️ CUDA 的真正护城河：为什么 10 年了还没人撼动 NVIDIA</a></li>
<li><a href="https://semianalysis.com/about/">About – SemiAnalysis</a></li>
<li><a href="https://ai-bot.cn/deepseek-v4-1-flash/">DeepSeek V 4 . 1 Flash - DeepSeek 开源的全新大语言模型 | AI工具集</a></li>

</ul>
</details>

**Tags**: `#CUDA`, `#AMD`, `#NVIDIA`, `#AI基础设施`, `#性能基准`

---

<a id="item-6"></a>
## [Homebrew 7.0.0 ships official native macOS GUI](https://brew.sh/2026/09/13/homebrew-7.0.0/) ⭐️ 8.0/10

Homebrew released version 7.0.0, introducing an official native macOS graphical interface alongside faster installs and upgrades, stricter sandboxing, and a built-in vulnerability scanning and security advisory database. The release also drops support for macOS 10.15 and earlier, moves Intel Macs to Tier 3 with no new precompiled bottles, and switches the Linux sandbox from Bubblewrap to Landlock. Homebrew is one of the most widely used package managers on macOS and Linux, so a major version bump with an official GUI, built-in security scanning, and stricter sandboxing affects a huge number of developers and end users. The platform support changes also signal a broader industry shift away from older macOS releases and Intel-based Macs. The Linux sandbox now relies on Landlock, a stackable Linux Security Module that lets unprivileged processes restrict their own filesystem access, replacing the user-namespace-based Bubblewrap approach. Intel Macs are demoted to Tier 3, meaning Homebrew still works there but with reduced automation coverage and community support, and no new precompiled bottles are produced.

telegram · zaihuapd · Sep 13, 11:23

**Background**: Homebrew is a command-line package manager that simplifies installing open-source software on macOS and Linux, and it has historically been distributed primarily through the terminal. Support tiers are Homebrew's way of describing how well the tool is expected to work on a given host system, ranging from fully maintained to best-effort. Sandboxing restricts what a process can access on the system, and both Bubblewrap and Landlock are Linux mechanisms for creating such restricted environments.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.brew.sh/Support-Tiers">Homebrew Documentation: Support Tiers</a></li>
<li><a href="https://landlock.io/">Landlock : the Linux sandboxing mechanism</a></li>
<li><a href="https://github.com/containers/bubblewrap">GitHub - containers/ bubblewrap : Low-level unprivileged sandboxing...</a></li>

</ul>
</details>

**Tags**: `#Homebrew`, `#macOS`, `#package-manager`, `#security`, `#release`

---

<a id="item-7"></a>
## [Kirin 9050 Pro Review: 3D Stacking Boosts Performance and Efficiency](https://www.bilibili.com/video/BV1HEYv6XETo) ⭐️ 8.0/10

A review from Geekerwan shows Huawei's Kirin 9050 Pro uses micro-circuit 3D stacking, with its 9-core/16-thread CPU cutting power consumption by over 30% at the same 2.75 GHz clock versus the previous generation, while peak 3.1 GHz frequency adds no significant power draw. The Maleoon 955 GPU improves 3DMark scores by nearly 40%, the NPU delivers a measured 67.7 INT8 TOPS, and the Mate XT 2 reaches Snapdragon 8 Elite-level performance in three heavy mobile games. This is a significant milestone for Huawei's domestic chip design, showing that 3D stacking can deliver flagship-level performance and efficiency without relying on advanced EUV lithography. It could reshape the competitive landscape of mobile SoCs and strengthen Huawei's position in the high-end smartphone market despite ongoing export restrictions. The chip reportedly uses a 9-core LinxiCore CPU with simultaneous multi-threading, a Maleoon 955 GPU with hardware ray tracing, a Da Vinci NPU, and an integrated Balong modem, built on SMIC's N+3 process with a LogicFolding architecture that bonds two logic layers. The 67.7 INT8 TOPS NPU figure is a peak theoretical metric, so real-world AI inference speed will also depend on memory bandwidth and software support.

telegram · zaihuapd · Sep 13, 13:22

**Background**: 3D stacking is an advanced packaging technique that bonds multiple chip layers vertically to increase transistor density and shorten interconnects, rather than shrinking transistors via a new process node. Huawei has been unable to access ASML's EUV lithography due to export controls, so it has turned to design and packaging innovations such as LogicFolding to compensate. The Kirin 9050 Pro is the chip powering Huawei's Mate XT 2 foldable phone, and it competes directly with Qualcomm's Snapdragon 8 Elite in the flagship Android segment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.huaweicentral.com/kirin-9050-pro/">Kirin 9050 Pro Chip: Architecture, Performance and More</a></li>
<li><a href="https://m1k.tech/2026/09/huawei-kirin-9050-pro-logic-folding-mate-xt2/">Kirin 9050 Pro: Huawei Folded the Chip Instead of Shrinking It</a></li>
<li><a href="https://www.qualcomm.com/news/onq/2024/04/a-guide-to-ai-tops-and-npu-performance-metrics">A guide to AI TOPS and NPU performance metrics | Qualcomm</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#Kirin 9050 Pro`, `#3D stacking`, `#mobile chip`, `#benchmark`

---

<a id="item-8"></a>
## [Simon Willison releases commit-rewriter 0.1 for cleaning up commit messages](https://simonwillison.net/2026/Sep/14/commit-rewriter/) ⭐️ 6.0/10

Simon Willison released commit-rewriter 0.1, a small web app that lets developers edit commit messages in a repository, runnable via `uvx commit-rewriter path/to/repo`. He built it to clean up coding-agent cruft and private issue-ID references in the commits behind the September 2026 Datasette security releases before publishing them. As AI coding agents generate more commits, developers increasingly need lightweight ways to sanitize commit history before making repositories public, and this tool addresses that workflow directly. It also reflects a broader trend of maintainers building small, focused utilities to manage the side effects of AI-assisted programming. When edits are submitted, the tool creates a timestamped branch of the current repo state so changes can be reverted, then rewrites every commit from the first edited one to the most recent. The interface includes a search box for message, author, or hash, an "Edited only" filter, and a toggle to view the full formatted diff.

rss · Simon Willison · Sep 14, 00:28

**Background**: Git commit messages are permanent parts of a repository's history, and rewriting them normally requires commands like `git rebase` or `git filter-repo`, which can be error-prone. Datasette is Simon Willison's open-source data exploration and publishing tool for Python, and its security releases involve commits that may contain internal references not meant for public view. `uvx` is a command from the `uv` Python package manager that runs Python tools without permanently installing them.

<details><summary>References</summary>
<ul>
<li><a href="https://uvx.sh/">uvx .sh | Astral</a></li>
<li><a href="https://datasette.io/blog/2026/september-security-releases/">Datasette 1.0a39 and 0.65.4 security releases - Datasette Blog</a></li>

</ul>
</details>

**Tags**: `#git`, `#developer-tools`, `#datasette`, `#commit-messages`, `#simon-willison`

---

<a id="item-9"></a>
## [Z.AI Plans US$5.0 Billion Fund-Raising to Fuel AI Expansion](https://news.google.com/rss/articles/CBMilwFBVV95cUxNaVlfVk1EaDZEUkFiMUp3ODlDeHVKUXZBNFdxTmJPUk5CZmFDWkxScnNuMXRSdk5IT0d1YUlSRHBlZk9DT1J3ckttWWhiSUt0b3VjaTkzbzdKVHlONVktNWVsREhyZ2NrZnNjdE5HRkhxMmZYOTRaOV91cExUTlZsdkVvdmxfclhDckhRWFFreDVQSHlmcGtB?oc=5) ⭐️ 6.0/10

Z.AI, the Chinese AI company formerly known as Zhipu AI, is planning to raise US$5.0 billion to fuel its AI expansion, according to a Wall Street Journal report. The move comes less than two months after the company raised US$4.0 billion through a share placement in July. This is one of the largest fund-raising efforts by a Chinese AI company and signals strong investor confidence in the sector despite intensifying global competition. It could accelerate Z.AI's development of the GLM model family and strengthen its position against rivals such as OpenAI, Anthropic, and other Chinese AI labs. The new round follows a US$4.0 billion share placement in July, meaning Z.AI could raise nearly US$9 billion within roughly two months. Z.AI's GLM models have been released under the free and open-source MIT License since July 2025, and the company also offers vision language models, text-to-video models, and the ZCode AI coding harness.

google_news · Moomoo · Sep 13, 23:45

**Background**: Z.AI is the international brand of Zhipu AI (智谱AI), a Chinese artificial intelligence company founded in 2019 based on technology developed at Tsinghua University in Beijing. The company adopted the Z.ai name on July 28, 2025, alongside the release of its GLM-4.5 model, to present a cleaner global identity. Its flagship product is the GLM (General Language Model) family of open-weights large language models, which compete with other leading LLMs worldwide.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Z.ai">Z.ai - Wikipedia</a></li>
<li><a href="https://www.wsj.com/tech/ai/z-ai-plans-5-0-billion-fundraising-to-fuel-ai-expansion-56da16dc">Z.AI Plans $5.0 Billion Fundraising to Fuel AI Expansion - WSJ</a></li>
<li><a href="https://aiwiki.ai/wiki/z_ai">Z.ai | AI Wiki Z.ai: What to Know About the Chinese Company Behind Ox Alpha ... Z.ai - LinkedIn</a></li>

</ul>
</details>

**Tags**: `#AI`, `#fundraising`, `#Z.AI`, `#investment`, `#industry news`

---