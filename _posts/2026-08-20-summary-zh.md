---
layout: default
title: "Horizon Summary: 2026-08-20 (ZH)"
date: 2026-08-20
lang: zh
---

> 从 41 条内容中筛选出 10 条重要资讯。

---

1. [恶意 arrayref Rust crate 在构建时执行载荷](#item-1) ⭐️ 9.0/10
2. [GitHub 8 月 17 日宕机：重试漏洞放大 10 倍流量](#item-2) ⭐️ 8.0/10
3. [Aaron Swartz 因爬取数据被起诉，而 Meta 却逍遥法外](#item-3) ⭐️ 8.0/10
4. [AliExpress 使用无声 WebAudio 指纹识别，破坏蓝牙多点连接](#item-4) ⭐️ 8.0/10
5. [用 125M Transformer 实现设备端钢琴自动补全](#item-5) ⭐️ 8.0/10
6. [Linux 7.2 发布，支持 HDMI 2.1](#item-6) ⭐️ 8.0/10
7. [Bun 1.4 的 Bun.WebView 驱动一个类似 shot-scraper 的 JSON API](#item-7) ⭐️ 8.0/10
8. [OpenAI 推出 AI Futures 博客系列，探讨社会影响](#item-8) ⭐️ 7.0/10
9. [临港新片区目标成为全球代币服务出口枢纽](#item-9) ⭐️ 6.0/10
10. [Stampli 借助 ChatGPT Work 将发布生产时间缩短 68%](#item-10) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [恶意 arrayref Rust crate 在构建时执行载荷](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

流行的 Rust crate 'arrayref'（0.3.10）发布了一个恶意版本，它引入了拼写错误的依赖'proc-macro1'，其构建脚本在编译期间下载并运行远程二进制文件。Rust 项目已从 crates.io 删除了这些恶意版本。 这次攻击凸显了 Rust 生态系统在供应链攻击面前的脆弱性，尤其是通过构建脚本进行的攻击。它影响了使用这些 crate 的开发者，可能危及他们的构建环境和 CI/CD 管道，并强调了加强沙箱和安全措施的必要性。 arrayref 的恶意版本添加了对'proc-macro1'的依赖，这是对合法 crate 'proc-macro2'的拼写错误模仿。'proc-macro1'的构建脚本下载并执行远程二进制文件，可能安装后门。其他 crate 如'internment'和'append-only-vec'也在此次协同攻击中被入侵。

hackernews · abhisek · 8月20日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=49374269)

**背景**: Rust crate 通常包含构建脚本（build.rs），这些脚本在编译时执行任意代码，可能被恶意利用。供应链攻击涉及破坏合法软件包以向下游用户分发恶意软件。Rust 生态系统依赖 crates.io 作为中央仓库，此类攻击凸显了加强安全措施（如沙箱化构建脚本）的必要性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/">Malicious Rust Crate arrayref Runs a Build-Time Payload - Real-time Open Source Software Supply Chain Security</a></li>
<li><a href="https://www.stepsecurity.io/blog/arrayref-rust-crate-supply-chain-attack">Rust Supply-Chain Attack: arrayref, internment, and append-only-vec Poisoned by the proc-macro1 Build-Time Dropper - StepSecurity</a></li>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build-Time Malware in Crates with...</a></li>

</ul>
</details>

**社区讨论**: 社区对 crates.io 的回应表示担忧，指出恶意版本消失时没有明确的 yank 指示或安全公告。一些人呼吁在 Cargo 中更好地沙箱化构建脚本，而另一些人则讨论了依赖膨胀的广泛问题，以及需要'内置电池'的标准库以减少对第三方 crate 的依赖。

**标签**: `#supply-chain security`, `#Rust`, `#malware`, `#crates.io`, `#open source`

---

<a id="item-2"></a>
## [GitHub 8 月 17 日宕机：重试漏洞放大 10 倍流量](https://github.blog/news-insights/company-news/the-august-17-outage-and-the-work-ahead/) ⭐️ 8.0/10

8 月 17 日，GitHub 遭遇了持续 7 小时 47 分钟的宕机，影响核心服务。事后分析显示，VS Code 中一个潜在的重试漏洞将流量放大了约 10 倍，导致 Copilot Token Service 恢复延迟。 此次宕机凸显了大规模基础设施在快速增长下的脆弱性，尤其是自 4 月以来 AI 驱动的提交量翻倍。这强调了需要健壮的重试逻辑和自动扩展策略，以防止级联故障。 最初的触发因素是 GitHub 美国中部数据中心负载均衡器的网络饱和，但 VS Code 的重试漏洞延长了宕机时间。GitHub 还指出，自 4 月以来，月度提交量从 14 亿增长到 29 亿，给系统增加了压力。

hackernews · 0xedb · 8月20日 19:22 · [社区讨论](https://news.ycombinator.com/item?id=49378957)

**背景**: 重试风暴是指客户端自动重试失败的请求，从而放大负载并可能压垮服务器。GitHub 的宕机表明，单个延迟的端点可能引发此类风暴，尤其是在客户端重试逻辑过于激进的情况下。自动扩展（根据需求动态调整资源）未能跟上突发的流量激增，暴露了容量规划中的盲点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/saas/2026/08/19/github-blames-8-hour-outage-on-autoscaling-fail-and-vs-code-retry-storm/5289547">GitHub blames 8-hour outage on autoscaling fail and VS Code retry ...</a></li>
<li><a href="https://juniortoexpert.com/en/what-is-retry-storm/">What is Retry Storm? Causes, Consequences, and Examples</a></li>
<li><a href="https://www.computing.co.uk/news/2026/security/github-outage-exposes-flaws-in-autoscaling-and-retry-systems">GitHub outage exposes flaws in autoscaling and retry systems</a></li>

</ul>
</details>

**社区讨论**: 社区评论对重试逻辑表示担忧，有人认为向用户隐藏错误会导致更糟糕的结果。其他人对提交量的快速增长感到惊讶，将其归因于 AI 驱动的生产力提升，并讨论了向提交收费是否会阻止 AI 重度使用，指出微软有推广 AI 采用的动机。

**标签**: `#outage`, `#postmortem`, `#reliability`, `#GitHub`, `#retry`

---

<a id="item-3"></a>
## [Aaron Swartz 因爬取数据被起诉，而 Meta 却逍遥法外](https://blog.curiousquail.com/im-upset-again-about-a-co-creator-of-rss-being-prosecuted-for-something-meta-is-doing-with-little-consequence/) ⭐️ 8.0/10

一篇博客文章指出，Aaron Swartz 因爬取学术论文而被起诉，而 Meta 从事类似的数据爬取却未面临法律后果，凸显了科技执法中明显的双重标准。 这种对比引发了关于数据爬取法律待遇公平性和一致性的重要问题，尤其是在人工智能发展日益依赖大规模数据收集的背景下。它可能影响公众舆论以及关于数据访问和企业责任的政策辩论。 该文章提到 Swartz 根据《计算机欺诈和滥用法》（CFAA）被起诉，涉及通过 MIT 网络未经授权访问 JSTOR。相比之下，Meta 也卷入了关于数据爬取的法律纠纷，但最近的裁决，如 Meta v. Bright Data 案，有利于爬取方，且 Meta 已放弃部分诉讼。

hackernews · speckx · 8月20日 20:07 · [社区讨论](https://news.ycombinator.com/item?id=49379550)

**背景**: Aaron Swartz 是一位程序员和互联网活动家，共同创建了 RSS 并帮助开发了知识共享（Creative Commons）。2011 年，他因从 JSTOR 下载数百万篇学术文章而被捕，面临联邦指控，可能面临最高 35 年的刑期。他于 2013 年自杀身亡，引发了对检察官过度起诉的广泛批评。数据爬取，即从网站自动收集数据，已成为一个有争议的法律问题，法院最近裁定爬取公共数据可能不违反 CFAA 等法律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/United_States_v._Swartz">United States v. Swartz - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Aaron_Swartz">Aaron Swartz - Wikipedia</a></li>
<li><a href="https://www.courthousenews.com/federal-judge-rules-against-meta-in-data-scraping-case/">Federal judge rules against Meta in data scraping case | Courthouse News Service</a></li>
<li><a href="https://www.socialmediatoday.com/news/meta-abandons-legal-case-data-scraping-losing-key-judgment/708538/">Meta Abandons Legal Case Over Data Scraping After Losing Key Judgment | Social Media Today</a></li>
<li><a href="https://www.fbm.com/publications/major-decision-affects-law-of-scraping-and-online-data-collection-meta-platforms-v-bright-data/">Major Decision Affects Law of Scraping and Online Data Collection, Meta Platforms v. Bright Data</a></li>

</ul>
</details>

**社区讨论**: 评论者提供了细致的纠正，指出 Swartz 的行为涉及物理入侵和 MAC 地址轮换，而不仅仅是简单的爬取，且 35 年刑期是法定最高刑期，并非实际寻求的判决。一些人对围绕 Swartz 的浪漫化叙事表示不满，强调他的个人挣扎和案件的复杂性。

**标签**: `#scraping`, `#legal`, `#ethics`, `#Aaron Swartz`, `#Meta`

---

<a id="item-4"></a>
## [AliExpress 使用无声 WebAudio 指纹识别，破坏蓝牙多点连接](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

发现 AliExpress 在其网站上运行无声的 WebAudio 指纹识别，这无意中干扰了用户设备的蓝牙多点连接。这一发现揭示了一种新颖的侵犯隐私的技术，同时也导致了现实世界中的可用性问题。 这很重要，因为它暴露了浏览器在音频指纹识别防护方面的漏洞，并影响了大量依赖蓝牙多点连接实现无缝音频切换的用户。这一事件凸显了加强隐私保护和更好检测无声音频播放的必要性。 该指纹识别技术利用 Web Audio API 生成唯一的设备标识符，而无需播放可听见的声音，这可能会触发蓝牙多点连接切换音频源。这一行为已在 AliExpress 上被观察到，并且可能允许网站在移动浏览器后台继续运行。

hackernews · emctech · 8月20日 10:08 · [社区讨论](https://news.ycombinator.com/item?id=49372583)

**背景**: WebAudio 指纹识别是一种跟踪方法，利用设备通过 Web Audio API 处理音频信号时的细微差异来创建唯一标识符。蓝牙多点连接是一项允许单个耳机同时连接多个设备并在它们之间自动切换音频的功能。冲突的产生是因为无声音频播放可能被误认为是活动音频流，导致耳机意外切换音源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fingerprint.com/blog/audio-fingerprinting/">Audio Fingerprinting: What It Is + How It Works with Web API</a></li>
<li><a href="https://www.soundguys.com/bluetooth-multipoint-explained-28601/">What is Bluetooth multipoint? - SoundGuys</a></li>
<li><a href="https://www.howtogeek.com/820840/what-is-multipoint-bluetooth/">What Is Multipoint Bluetooth? - How-To Geek Bluetooth Multipoint Pairing: Complete Guide 2026 Multipoint Bluetooth explained: what is it, and how ... - Stuff What is Bluetooth multipoint and why your next earbuds or ... What is Bluetooth Multipoint? What devices support it?</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了沮丧和担忧，用户分享了与 AliExpress 相关的蓝牙中断的个人经历。一些用户建议浏览器应显示无声音频播放的指示器，而另一些用户则指出，Firefox 等浏览器已经对 WebAudio 指纹识别进行了缓解。还有人对苹果 App Store 的政策表示怀疑，因为 AliExpress 应用可能也有类似行为。

**标签**: `#privacy`, `#web security`, `#fingerprinting`, `#WebAudio`, `#browsers`

---

<a id="item-5"></a>
## [用 125M Transformer 实现设备端钢琴自动补全](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

一位开发者训练了一个 125M 参数的 Transformer 模型，在 iPhone 15 上实时自动补全钢琴演奏，推理速度约为每秒 108 个音符。该应用免费供用户试用，模型完全在设备端运行。 这证明了在消费级硬件上无需云端依赖即可运行复杂音乐生成模型的可行性，为交互式音乐工具和创意应用开辟了新可能。同时，它也凸显了设备端 AI 日益增长的趋势，该趋势提供了隐私、低延迟和离线能力等优势。 该模型是一个 125M 参数的 Transformer，每次推进一个完整的音符，而不是通过多次传递生成音符属性。它针对 Apple 设备上的 Core ML 进行了优化，在 iPhone 15 上实现了实时性能。开发者提到许多方法并未奏效，这表明了巨大的工程投入。

hackernews · simedw · 8月20日 12:04 · [社区讨论](https://news.ycombinator.com/item?id=49373456)

**背景**: Transformer 已被成功应用于符号音乐生成，如 Music Transformer 论文（ICLR 2019）所示，该论文使用相对注意力进行音乐生成建模。设备端 AI 推理，特别是通过 Apple 的 Core ML 和神经引擎，实现了低延迟、私密和离线的应用。该项目将这些技术应用于创建“MIDI 的 GitHub Copilot”，用户通过弹奏几个音符来提示模型，模型则继续演奏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simedw.com/2026/08/20/midi-autocomplete/">Training a 125M-parameter Model to Autocomplete Piano - SimEdw's Blog</a></li>
<li><a href="https://openreview.net/pdf?id=rJe4ShAcF7">Published as a conference paper at ICLR 2019 MUSIC TRANSFORMER:</a></li>
<li><a href="https://huggingface.co/docs/transformers/model_doc/musicgen">MusicGen · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 社区评论称赞该项目的创新性和黑客新闻精神，一些人将其与古典音乐训练方法和基于 AI 的 UX 设计工具相提并论。用户还询问了训练数据规模，并指出听到熟悉曲目转向新方向时会产生令人不安的效果。

**标签**: `#AI/ML`, `#Music Generation`, `#On-device`, `#Transformer`, `#Core ML`

---

<a id="item-6"></a>
## [Linux 7.2 发布，支持 HDMI 2.1](https://www.igalia.com/2026/08/19/Linux-72-Released.html) ⭐️ 8.0/10

Linux 内核 7.2 于 2026 年 8 月 16 日发布，引入了显著改进，包括 HDMI 2.1 支持和更注重缓存感知的任务调度器。 此次发布意义重大，因为它为 Linux 内核带来了期待已久的 HDMI 2.1 支持，可能改善使用现代显示器和 GPU 的用户体验。调度器的改进也有望提升多核系统的性能。 HDMI 2.1 支持解决了此前 HDMI 论坛对开源驱动程序的限制。调度器的更改侧重于将共享数据的任务放置在同一个最后一级缓存域中，以提高缓存效率。

hackernews · mariuz · 8月20日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=49376265)

**背景**: HDMI 2.1 是一项支持 8K 和 4K@120Hz 等更高分辨率以及 VRR、ALLM 和动态 HDR 等功能的规范，带宽高达 48 Gbit/s。此前，AMD 的开源驱动程序因 HDMI 论坛的限制而无法实现 HDMI 2.1，但此次发布表明情况有所改变。Linux 内核是许多操作系统的核心，其开发由社区驱动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kernelnewbies.org/Linux_7.2">Linux_7.2 - Linux Kernel Newbies</a></li>
<li><a href="https://www.hdmi.org/spec/index">HDMI Technology: Specifications and Programs</a></li>
<li><a href="https://www.pcworld.com/article/394982/do-you-need-an-hdmi-21-monitor.html">Do you need an HDMI 2 . 1 monitor? | PCWorld</a></li>

</ul>
</details>

**社区讨论**: 社区成员对在论坛限制下如何实现 HDMI 2.1 支持表示好奇，有些人将报道与 LWN 进行比较。还有人询问目标受众以及 HDMI 相对于 DisplayPort 的优势，而一位用户则对更新其 Raspberry Pi 4 内核感到兴奋。

**标签**: `#Linux`, `#kernel`, `#HDMI`, `#open source`, `#release`

---

<a id="item-7"></a>
## [Bun 1.4 的 Bun.WebView 驱动一个类似 shot-scraper 的 JSON API](https://simonwillison.net/2026/Aug/20/bun-webview-json-api/) ⭐️ 8.0/10

Simon Willison 使用 Bun 1.4 的新 Bun.WebView 构建了一个原型 JSON API，该 API 可以加载网页并对其执行 JavaScript，类似于他的 shot-scraper javascript 命令行工具。Bun 1.4 是 Rust 重写后的首个稳定版本，引入了多个新 API，包括 Bun.WebView、Bun.Image 和 Bun.cron()。 这展示了 Bun.WebView 的一个新颖用例，可能通过消除对 Puppeteer 或 Playwright 等外部工具的需求，简化浏览器自动化和抓取任务。同时，它也凸显了 Bun 1.4 显著的性能改进和新功能，这可能使 JavaScript/TypeScript 开发者和系统研究人员受益。 这个用 TypeScript 编写的原型服务器，经 cgroups 测试，需要 192MB-256MB 的容器才能对复杂网页运行完整的 Chrome。Bun.WebView 支持 macOS WebKit 或通过 Chrome DevTools 协议（CDP）控制本地 Chromium 进程。

rss · Simon Willison · 8月20日 15:37

**背景**: Bun 是一个快速的 JavaScript 运行时，旨在成为 Node.js 的直接替代品。Bun 1.4 在 Rust 重写后发布，声称将空闲 CPU 使用率降低 5 倍，内存使用率降低高达 35%，并在 Linux 上启动速度提高 50%。Bun.WebView 是一个内置的无头浏览器 API，允许加载页面、执行 JavaScript、模拟用户输入和捕获截图，而无需外部依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.com/docs/runtime/webview">WebView | Bun Docs</a></li>
<li><a href="https://bun.com/reference/bun/WebView">Bun.WebView object | API Reference | Bun</a></li>
<li><a href="https://shot-scraper.datasette.io/en/stable/javascript.html">Scraping pages using JavaScript - shot-scraper</a></li>

</ul>
</details>

**社区讨论**: 提供的内容中不包含社区评论，因此没有可用的讨论摘要。

**标签**: `#Bun`, `#JavaScript`, `#WebView`, `#API`, `#Rust`

---

<a id="item-8"></a>
## [OpenAI 推出 AI Futures 博客系列，探讨社会影响](https://openai.com/index/introducing-ai-futures) ⭐️ 7.0/10

OpenAI 宣布推出 AI Futures，这是一个新的博客系列，致力于探讨变革性 AI 如何重塑权力、治理、经济和个体自由。该系列已在 OpenAI 网站上发布，标志着其战略重点转向 AI 的社会影响。 这一举措意义重大，因为它将 OpenAI 定位为 AI 治理和政策讨论的思想领袖，可能影响公众辩论和监管框架。随着 AI 能力的提升，理解和塑造社会影响对开发者、政策制定者和公众都至关重要。 该博客系列将涵盖变革性 AI 背景下的权力动态、治理结构、经济转型和个体自由等主题。虽然公告缺乏技术细节，但表明 OpenAI 致力于主动应对先进 AI 带来的社会挑战。

rss · OpenAI Blog · 8月20日 07:00

**背景**: 变革性 AI 指的是其影响可能堪比农业或工业革命的 AI 系统，重塑经济、政府和日常生活。AI 治理包括确保 AI 可信赖和有益的政策、流程和控制措施。OpenAI 的新系列旨在探索这些广泛的社会影响，建立在 AI 社区现有讨论的基础上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lesswrong.com/w/transformative-ai">Transformative AI</a></li>
<li><a href="https://forum.effectivealtruism.org/topics/transformative-artificial-intelligence">Transformative artificial intelligence - EA Forum</a></li>
<li><a href="https://www.ibm.com/think/insights/ai-governance-implementation">Guide for Implementing an AI Governance Framework | IBM</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI policy`, `#AI governance`, `#societal impact`

---

<a id="item-9"></a>
## [临港新片区目标成为全球代币服务出口枢纽](https://news.google.com/rss/articles/CBMitAFBVV95cUxQd3NmbXppeDV1cUJ1Y3NQdERlcGlJbG1KRV9ER1BUamtPZXVNVWE1VWIwMXBLTWJSVGZESmhCdW80X0diLWVScy1iVDNuanNhMXV5V3Z5eEtEU185aHFWVFh2a3pEWjVXR2RseGNxZDlpQUFjMGQ4a2J0LWw5aUExamk3VmxPS1Zfb1JWRFlRcFBVOElfODZRbzMyMmY4UUl2LUZTUWZNb1ZtVlZvcTliMXBHWFQ?oc=5) ⭐️ 6.0/10

8 月 20 日，上海自贸区临港新片区宣布其目标，即成为具有全球影响力的代币服务出口枢纽，这是其在中国数字贸易中作用日益增强的一部分。 这标志着中国区块链和金融科技领域一个显著的政策方向，可能使临港成为全球代币经济的关键参与者。它可能吸引国际企业和投资，并影响其他地区的监管方式。 临港新片区是上海自贸区内经贸政策的重要试验田。该公告强调了其在代币服务领域领先的雄心，但简短报道中未提供具体的实施细节和时间表。

google_news · 一财全球Yicai Global · 8月20日 07:08

**背景**: 临港新片区于 2019 年 8 月启动，是上海自贸试验区的一部分，旨在提供多元化的金融服务和优惠政策以吸引企业。代币服务可能指基于区块链的数字代币，用于数字资产和智能合约等多种应用。中国一直在探索区块链技术，同时对加密货币交易保持严格控制，因此此举可能代表在受监管环境中促进创新的微妙做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yicaiglobal.com/news/shanghai-ftzs-lingang-special-area-to-become-global-hub-for-token-services-export">Shanghai FTZ's Lingang Special Area to Become Global Hub for...</a></li>
<li><a href="https://en.lingang.gov.cn/">Lin - gang Special Area</a></li>
<li><a href="https://news.cgtn.com/news/2019-08-20/Shanghai-officially-launches-new-FTZ-Lingang-Special-Area--Ji8c5s6WL6/index.html">Shanghai officially launches new FTZ , Lingang Special Area - CGTN</a></li>

</ul>
</details>

**标签**: `#blockchain`, `#fintech`, `#Shanghai`, `#token services`, `#policy`

---

<a id="item-10"></a>
## [Stampli 借助 ChatGPT Work 将发布生产时间缩短 68%](https://openai.com/index/stampli) ⭐️ 5.0/10

采购到付款软件公司 Stampli 使用 OpenAI 的 ChatGPT Work 和 Codex，将发布生产时间缩短了 68%，把数周的工作压缩到几天内完成。该案例研究发布在 OpenAI 的博客上。 这展示了 AI 编程代理和 AI 驱动的工作工具对实际业务运营的实际影响，可能鼓励更多公司采用类似技术。这也凸显了 AI 辅助软件开发和流程自动化日益增长的趋势。 68% 的缩减是在发布生产中实现的，这通常涉及创建和部署营销或产品发布材料。尽管设计资源已投入其他项目且截止日期固定，Stampli 仍使用 Codex 处理编码任务，并使用 ChatGPT Work 进行更广泛的工作流自动化。

rss · OpenAI Blog · 8月20日 00:00

**背景**: Stampli 是一个采购到付款平台，利用 AI 自动化财务任务，每周处理超过 40 万张发票。ChatGPT Work 是 OpenAI 面向企业的产品，由 GPT-5.6 驱动，旨在帮助团队自动化任务和管理项目；而 Codex 是一个 AI 编程代理，可协助编写代码和修复错误等软件工程任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.stampli.com/">Stampli | Procure-to-Pay that does 87% of finance work</a></li>
<li><a href="https://openai.com/chatgpt-work/">ChatGPT Work for every team | OpenAI</a></li>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software ... - OpenAI</a></li>

</ul>
</details>

**标签**: `#AI`, `#case study`, `#productivity`, `#OpenAI`, `#software engineering`

---