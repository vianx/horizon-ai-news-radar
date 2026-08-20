---
layout: default
title: "Horizon Summary: 2026-08-20 (ZH)"
date: 2026-08-20
lang: zh
---

> 从 41 条内容中筛选出 10 条重要资讯。

---

1. [恶意 Rust crate arrayref 在构建时执行载荷](#item-1) ⭐️ 9.0/10
2. [GitHub 8 月 17 日宕机：重试漏洞放大流量 10 倍](#item-2) ⭐️ 8.0/10
3. [速卖通无声 WebAudio 指纹识别破坏蓝牙多点连接](#item-3) ⭐️ 8.0/10
4. [125M Transformer 在 iPhone 上自动补全钢琴演奏](#item-4) ⭐️ 8.0/10
5. [Linux 7.2 内核发布，支持 HDMI 2.1](#item-5) ⭐️ 8.0/10
6. [Bun 1.4 的 Bun.WebView 驱动类似 shot-scraper 的 JSON API](#item-6) ⭐️ 8.0/10
7. [Stripe 同意收购 AI 模型网关 OpenRouter](#item-7) ⭐️ 8.0/10
8. [OpenAI 推出 AI Futures 博客系列，探讨社会影响](#item-8) ⭐️ 7.0/10
9. [阿里巴巴 2026 财年第一季度销售额增长 9%，但 AI 支出拖累利润](#item-9) ⭐️ 6.0/10
10. [临港新片区目标成为全球代币服务出口中心](#item-10) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [恶意 Rust crate arrayref 在构建时执行载荷](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

流行的 Rust crate 'arrayref' 的一个恶意版本被发布到 crates.io，其中包含一个构建脚本，在编译期间下载并执行远程载荷。Rust 安全响应团队已删除恶意版本并发布官方公告。 此事件凸显了 Rust 生态系统在供应链攻击面前的脆弱性，尤其是通过构建脚本发起的攻击。它强调了在 Cargo 和 crates.io 中加强沙箱和安全措施的必要性，以保护依赖流行 crate 的众多项目。 恶意构建脚本将 PowerShell 脚本写入 %TEMP%\rust-setup.ps1，并通过 wscript.exe 下的 VBScript 启动器执行。其他受影响的 crate 包括 proc-macro1、proc-macro-en、aovine、arone、aronenao 和 tinymember，这些都已从 crates.io 删除。

hackernews · abhisek · 8月20日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=49374269)

**背景**: Rust crate 通常包含构建脚本（build.rs），在编译期间运行以生成代码或链接本地库。此功能可能被滥用，在开发者的机器上执行任意代码。针对开源生态系统的供应链攻击日益增多，例如 TrapDoor 活动就针对 npm、PyPI 和 crates.io。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.rust-lang.org/2026/08/20/supply-chain-attack-on-arrayref/">Supply chain attack on arrayref | Rust Blog</a></li>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build-Time Malware in Crates ...</a></li>
<li><a href="https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/">Malicious Rust Crate arrayref Runs a Build -Time Payload</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 crates.io 和 GitHub 在事件期间缺乏透明度表示不满，指出恶意版本消失时没有明确的 yank 指示或安全公告。一些人呼吁在 Cargo 中对构建脚本进行更好的沙箱处理，而另一些人则讨论了最小化标准库与依赖膨胀之间的权衡，建议采用“电池全包”的方法来减少攻击面。

**标签**: `#supply-chain security`, `#Rust`, `#malware`, `#crates.io`, `#security incident`

---

<a id="item-2"></a>
## [GitHub 8 月 17 日宕机：重试漏洞放大流量 10 倍](https://github.blog/news-insights/company-news/the-august-17-outage-and-the-work-ahead/) ⭐️ 8.0/10

GitHub 发布了 2026 年 8 月 17 日宕机的事后分析，揭示 VS Code 中一个潜在的重试漏洞将流量放大了约 10 倍，导致 Copilot Token Service 恢复延迟。此次宕机持续约 8 小时，最初由美国中部数据中心负载均衡器的网络饱和引发。 此次宕机凸显了大规模基础设施中的系统性可靠性问题，尤其是客户端重试循环在恢复期间放大流量的危险。它还强调了在 AI 驱动的提交量激增（自 4 月以来每月从 14 亿增长到 29 亿）的情况下，扩展 GitHub 基础设施所面临的挑战。 根本原因是单个内部端点的延迟响应触发了 VS Code 中的重试漏洞。GitHub 的事后分析还讨论了导致宕机延长的自动扩缩容失败，公司正在努力改进以防止类似事件。

hackernews · 0xedb · 8月20日 19:22 · [社区讨论](https://news.ycombinator.com/item?id=49378957)

**背景**: 重试风暴是指客户端自动重试失败的请求，可能压垮正在恢复的服务。GitHub 是广泛使用的代码托管平台，VS Code 是拥有数百万用户的流行代码编辑器。此次宕机影响了 Copilot 等服务，这些服务依赖令牌服务，事件凸显了稳健的重试策略和容量规划的重要性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/saas/2026/08/19/github-blames-8-hour-outage-on-autoscaling-fail-and-vs-code-retry-storm/5289547">GitHub blames 8-hour outage on autoscaling fail and VS Code retry ...</a></li>
<li><a href="https://juniortoexpert.com/en/what-is-retry-storm/">What is Retry Storm? Causes, Consequences, and Examples</a></li>
<li><a href="https://www.computing.co.uk/news/2026/security/github-outage-exposes-flaws-in-autoscaling-and-retry-systems">GitHub outage exposes flaws in autoscaling and retry systems</a></li>

</ul>
</details>

**社区讨论**: 社区评论对向用户隐藏错误的趋势表示担忧，有用户指出重试可能掩盖真正的故障。其他人对提交量的快速增长感到惊叹，将其归因于 AI 驱动的生产力，还有人推测微软推广 AI 使用的激励措施可能影响 GitHub 的政策。

**标签**: `#outage`, `#postmortem`, `#GitHub`, `#reliability`, `#retry`

---

<a id="item-3"></a>
## [速卖通无声 WebAudio 指纹识别破坏蓝牙多点连接](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

速卖通网站被发现运行无声的 WebAudio 指纹识别，这无意中破坏了用户的蓝牙多点连接。该问题在一篇博客文章中被报道，并在 Hacker News 上引发了广泛讨论。 这凸显了一家大型电商平台使用的侵犯隐私的技术，并对用户硬件产生了实际副作用。它强调了浏览器需要更好地防范此类指纹识别方法，并引发了对用户同意和透明度的担忧。 该指纹识别在媒体元素 API 之外运行，用户除了关闭标签页外别无他法。Firefox 已对 WebAudio 指纹识别实施了缓解措施，但其他浏览器可能仍然容易受到攻击。

hackernews · emctech · 8月20日 10:08 · [社区讨论](https://news.ycombinator.com/item?id=49372583)

**背景**: WebAudio 指纹识别是一种利用 AudioContext API 根据设备的音频处理特性生成唯一标识符的技术。蓝牙多点连接允许设备同时与多个音频源保持连接，但无声音频播放可能会干扰此功能。该问题源于指纹识别播放听不见的音频，从而触发蓝牙协议栈切换音频流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.elseif.net/stories/aliexpress-runs-silent-webaudio-fingerprinting-that-breaks-bluetooth-m-4d2c69f">AliExpress silent WebAudio fingerprinting keeps Bluetooth... — elseif</a></li>
<li><a href="https://www.v2ex.com/t/1236018">AliExpress runs silent WebAudio fingerprinting that breaks... - V2EX</a></li>
<li><a href="https://shokz.com/blogs/news/bluetooth-multipoint-vs-dual-audio">Bluetooth Multipoint vs Dual Audio: What's the Difference?</a></li>

</ul>
</details>

**社区讨论**: 社区评论中，用户分享了在各种设备上遇到蓝牙中断的个人经历，有些人提到速卖通应用也有类似问题。一位评论者提到 Firefox 已对 WebAudio 指纹识别采取了缓解措施，另一位则讽刺地指出苹果可能会将应用从 App Store 下架，暗指其封闭生态系统的论点。

**标签**: `#privacy`, `#web security`, `#fingerprinting`, `#WebAudio`, `#Bluetooth`

---

<a id="item-4"></a>
## [125M Transformer 在 iPhone 上自动补全钢琴演奏](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

一位开发者训练了一个 125M 参数的 transformer 模型，用于实时自动补全钢琴演奏（在 iPhone 15 上约每秒 108 个音符），并以免费应用的形式发布。该模型完全在设备端通过 Core ML 运行，项目在 Hacker News 上展示了技术细节并引发了社区讨论。 该项目展示了小型 transformer 模型在实时、设备端音乐生成中的新颖应用，凸显了在无云端依赖的情况下本地运行创意 AI 工具的可行性。它可能激发更多交互式 AI 音乐工具和设备端生成模型的发展。 最大的改进来自于找到合适的 MIDI 表示、积极清理训练数据以及添加 DPO 后训练。模型每次推进一个完整的音符，而不是花费多次 transformer 传递来生成音符属性。

hackernews · simedw · 8月20日 12:04 · [社区讨论](https://news.ycombinator.com/item?id=49373456)

**背景**: Transformer 模型最初为自然语言处理而设计，后来被改编用于符号音乐生成，如 Music Transformer 等项目。像 Core ML 这样的设备端机器学习框架允许模型在移动硬件上高效运行，利用神经引擎进行加速。MIDI 是一种以数字方式表示音符的标准协议，因此非常适合此类生成任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simedw.com/2026/08/20/midi-autocomplete/">Training a 125M-parameter Model to Autocomplete Piano - SimEdw's Blog</a></li>
<li><a href="https://news.ycombinator.com/item?id=49373456">Show HN: I trained a 125M model to autocomplete piano on-device | Hacker News</a></li>
<li><a href="https://openreview.net/pdf?id=rJe4ShAcF7">Published as a conference paper at ICLR 2019 MUSIC TRANSFORMER:</a></li>

</ul>
</details>

**社区讨论**: 评论者将其与古典作曲家的训练方法和基于 AI 的 UX 设计工具相类比，指出当生成成本下降时，品味成为关键差异因素。一些人询问了数据集大小和训练细节，而另一些人则觉得意想不到的音乐方向令人不安却又引人入胜。

**标签**: `#AI/ML`, `#Music Generation`, `#On-device`, `#Transformer`, `#Core ML`

---

<a id="item-5"></a>
## [Linux 7.2 内核发布，支持 HDMI 2.1](https://www.igalia.com/2026/08/19/Linux-72-Released.html) ⭐️ 8.0/10

Linux 内核 7.2 已正式发布，引入了包括 HDMI 2.1 支持、缓存感知调度和扩展硬件兼容性在内的显著改进。此次发布经过了数月的开发，并包含对内核代码库的重大更新。 此次发布对 Linux 用户和开发者意义重大，因为它将现代显示连接（HDMI 2.1）引入内核，支持更高带宽和更好的 4K/8K 显示及高刷新率。缓存感知调度的改进也有望提升多核系统的性能，惠及各种工作负载。 根据早期候选版本说明，内核 7.2 版本包含关键的 PCIe 修复、移除旧驱动以及扩展 Rust 支持。HDMI 2.1 支持尤其引人注目，因为此前开源驱动被 HDMI 论坛阻止，社区对如何解决这一问题感到好奇。

hackernews · mariuz · 8月20日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=49376265)

**背景**: HDMI 2.1 是一种显示接口标准，支持更高带宽（最高 48Gbps），可实现 4K 120Hz、8K 60Hz 和动态 HDR 等功能。此前，AMD 开源驱动对 HDMI 2.1 的支持因 HDMI 论坛的许可限制而受阻，但此次发布表明情况有所变化。缓存感知调度是一种内核特性，根据 CPU 缓存拓扑优化任务放置，从而提升现代多核处理器的性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://itsfoss.com/news/linux-kernel-7-2-release/">Linux 7 . 2 Arrives With Cache Aware Scheduling After More Than...</a></li>
<li><a href="https://www.linuxteck.com/linux-kernel-7-2-rc1-release/">Linux Kernel 7 . 2 RC1 Drops With Powerful 43 Million Lines Update</a></li>
<li><a href="https://www.lifewire.com/hdmi-facts-high-definition-multimedia-interface-1847337">lifewire.com/ hdmi -facts- high - definition - multimedia - interface -1847337</a></li>

</ul>
</details>

**社区讨论**: 社区评论表现出好奇与热情。用户询问 HDMI 2.1 支持是如何解除限制的，将其报道与 LWN 进行比较，并好奇目标受众。一些人对更新树莓派表示兴奋，而另一些人则质疑在桌面使用中 HDMI 相比 DisplayPort 的实际优势。

**标签**: `#Linux`, `#Kernel`, `#HDMI 2.1`, `#Open Source`, `#Release`

---

<a id="item-6"></a>
## [Bun 1.4 的 Bun.WebView 驱动类似 shot-scraper 的 JSON API](https://simonwillison.net/2026/Aug/20/bun-webview-json-api/) ⭐️ 8.0/10

Simon Willison 使用 Bun 1.4 的新 Bun.WebView API 构建了一个类似 shot-scraper 的 JSON API，该 API 提供了对浏览器自动化的原生支持。该版本还包括 Rust 重写、性能改进和许多新功能。 这展示了 Bun.WebView 的实际应用场景，可能简化之前需要 Puppeteer 或 Playwright 等外部工具的浏览器自动化任务。它可以降低开发人员直接在 Bun 中构建抓取和自动化服务的门槛。 该原型服务器使用 TypeScript 实现，经 cgroups 测试，运行完整 Chrome 实例处理复杂网页需要 192MB-256MB 的容器。Bun.WebView 支持 macOS WebKit 或通过 Chrome DevTools 协议（CDP）控制本地 Chromium。

rss · Simon Willison · 8月20日 15:37

**背景**: Bun 是一个以速度和内置工具著称的 JavaScript 运行时。Bun 1.4 是一个重大版本，将运行时从 Zig 重写为 Rust，提高了性能和兼容性。Bun.WebView 是一个新 API，提供了内置于运行时的无头浏览器，允许开发人员加载页面、执行 JavaScript 和捕获截图，而无需外部依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.com/docs/runtime/webview">WebView | Bun Docs</a></li>
<li><a href="https://bun.com/reference/bun/WebView">Bun.WebView object | API Reference | Bun</a></li>
<li><a href="https://github.com/simonw/shot-scraper">GitHub - simonw/shot-scraper: A CLI utility for taking ...</a></li>

</ul>
</details>

**标签**: `#Bun`, `#JavaScript`, `#WebView`, `#API`, `#Rust`

---

<a id="item-7"></a>
## [Stripe 同意收购 AI 模型网关 OpenRouter](https://stripe.com/en-jp/newsroom/news/stripe-agrees-to-acquire-openrouter) ⭐️ 8.0/10

2026 年 8 月 19 日，Stripe 宣布已同意收购 AI 模型网关与路由平台 OpenRouter，该平台可在 80 多家提供商的 400 多个模型之间动态分配请求。此次收购旨在根据任务复杂度、价格、速度和可靠性选择最佳模型，从而帮助企业优化 Token 使用。 此次收购意义重大，它将 AI 基础设施与金融科技整合，可能重塑 AI 模型的访问和付费方式。通过将支付处理直接集成到 AI 模型路由中，它可能影响更广泛的 AI 生态系统，使依赖多家 AI 提供商的企业受益。 OpenRouter 平台支持基于成本、延迟和任务要求等实时信号的动态路由，并提供免费模型路由器，可自动选择兼容的免费模型。此次收购预计将在获得监管批准后完成，财务条款未披露。

telegram · zaihuapd · 8月20日 07:00

**背景**: OpenRouter 是一项通过单一 API 提供多种大型语言模型访问的服务，无需分别订阅多家 AI 提供商。动态路由是一种利用实时信号为每个请求做出决策的技术，以优化成本、速度和质量。Stripe 是一家主要的支付处理平台，此次收购与其向 AI 相关服务扩展的战略一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://medium.com/@tahirbalarabe2/what-is-open-router-a-unified-gateway-for-large-language-models-8b15597af7b7">What is Open Router ? A Unified Gateway for Large Language Models</a></li>
<li><a href="https://mixroute.ai/blog/llm-routing-strategies/">LLM Routing Strategies: Rules, Fallbacks, and Dynamic ... - MixRoute</a></li>

</ul>
</details>

**标签**: `#AI`, `#acquisition`, `#Stripe`, `#OpenRouter`, `#AI infrastructure`

---

<a id="item-8"></a>
## [OpenAI 推出 AI Futures 博客系列，探讨社会影响](https://openai.com/index/introducing-ai-futures) ⭐️ 7.0/10

OpenAI 宣布推出新的博客系列 AI Futures，致力于探讨变革性 AI 的社会影响，包括其对权力、治理、经济和个人自由的影响。该系列旨在促进讨论，并就先进 AI 系统如何重塑社会提供见解。 作为领先的 AI 组织，OpenAI 主动探讨社会影响，表明行业内越来越认识到需要考虑技术能力之外的更广泛影响。该系列可能会影响关于 AI 治理和伦理的公共讨论和政策制定，影响研究人员、政策制定者和公众。 该公告内容简短，未说明博客文章的发布频率、作者或具体主题。该系列是 OpenAI 更广泛的沟通策略的一部分，旨在参与围绕 AI 的社会问题，但目前尚未提供技术细节或具体政策建议。

rss · OpenAI Blog · 8月20日 07:00

**背景**: 变革性 AI 指的是可能对社会产生巨大影响的先进 AI 系统，即使它们可能未达到人类水平的认知能力。此类 AI 的社会影响包括权力动态、治理结构、经济体系和个人自由的变化，这些是专家们积极辩论的话题。OpenAI 的博客系列旨在通过提供一个探索这些复杂问题的平台来促进这一讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sciencedirect.com/science/article/pii/S0016328721001932">The transformative potential of artificial intelligence - ScienceDirect</a></li>
<li><a href="https://www.newamerica.org/planetary-politics/briefs/power-governance-ai-public-good/">Experts Reflect on Power and Governance in the Age of AI</a></li>
<li><a href="https://link.springer.com/article/10.1007/s43681-024-00635-y">A roadmap for governing AI: technology governance and power-sharing liberalism | AI and Ethics | Springer Nature Link</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI policy`, `#AI governance`, `#societal impact`, `#blog`

---

<a id="item-9"></a>
## [阿里巴巴 2026 财年第一季度销售额增长 9%，但 AI 支出拖累利润](https://news.google.com/rss/articles/CBMi4wFBVV95cUxOS3J2dThHdVdSVV92ZHF0bGxxZHVuYlpkb2QtX3BRVWtYeVhiQzZkaGNJalNYQVBPUU1UMmpQOGctcDRzNE9PYWxSTVJQcFFONTYxRFFFZFhBa1cyODNKVDNQUUtfS3ZiQXY0ZGdoTUh5UG9NTFk0X3hTZnhNN3ZKckI5Wldla3ZYeTlrNk8tS2xyOXpaM25ENm9hSE1ibzJ3VDhRei1fWVhvMnBlSG53REVzVms4NVpON0xZbW1oRTlXbWF0SktYMk9SbElHQWhXalhsN0o1MTdrTVFQNk1GR3VOQQ?oc=5) ⭐️ 6.0/10

阿里巴巴 2026 财年第一季度营收同比增长 9%，达到 2690 亿元人民币，但由于大力投资 AI 基础设施，归母净利润暴跌 76%至 105.37 亿元人民币。 这凸显了科技巨头在大力投资 AI 时所面临的财务权衡，阿里巴巴云业务收入激增 45%，但整体盈利能力受损。这表明 AI 领先地位需要大量资本投入，影响投资者预期和行业趋势。 阿里云外部收入增长 45%，AI 相关产品收入连续第十二个季度实现三位数增长。调整后每股 ADS 收益下降 42%至 1.26 美元，未达预期，调整后 EBITA 下降 30%至 40.3 亿美元。

google_news · Investing.com South Africa · 8月20日 02:26

**背景**: 阿里巴巴是中国主要的电子商务和云计算公司，在全球 AI 发展中竞争。其 2026 财年第一季度对应截至 2026 年 6 月的季度。公司一直在大力投资 AI 基础设施，以与腾讯、百度等国内竞争对手以及全球企业竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/news/story/ai-spending-weighs-on-alibabas-bottom-line-7511292/">AI spending weighs on Alibaba 's bottom line | LinkedIn</a></li>
<li><a href="https://finance.yahoo.com/markets/stocks/articles/alibaba-stock-dips-q2-profit-101348014.html">Alibaba stock dips as Q2 profit misses estimates despite strong AI ...</a></li>
<li><a href="https://www.benzinga.com/markets/earnings/26/08/61326198/alibaba-says-ai-spending-could-pay-off-in-3-years">Why Is Alibaba Stock Falling Thursday? - Alibaba Gr Hldgs (NYSE:BABA) - Benzinga</a></li>

</ul>
</details>

**标签**: `#Alibaba`, `#earnings`, `#AI investment`, `#financial results`

---

<a id="item-10"></a>
## [临港新片区目标成为全球代币服务出口中心](https://news.google.com/rss/articles/CBMitAFBVV95cUxQd3NmbXppeDV1cUJ1Y3NQdERlcGlJbG1KRV9ER1BUamtPZXVNVWE1VWIwMXBLTWJSVGZESmhCdW80X0diLWVScy1iVDNuanNhMXV5V3Z5eEtEU185aHFWVFh2a3pEWjVXR2RseGNxZDlpQUFjMGQ4a2J0LWw5aUExamk3VmxPS1Zfb1JWRFlRcFBVOElfODZRbzMyMmY4UUl2LUZTUWZNb1ZtVlZvcTliMXBHWFQ?oc=5) ⭐️ 5.0/10

上海自贸区临港新片区宣布其目标，即成为具有全球影响力的代币服务出口中心。该举措是该地区在中国数字贸易中作用日益增强的一部分。 此举表明，尽管此前对加密货币进行过打击，中国仍对区块链和代币化保持兴趣，可能为代币服务开辟一条受监管的路径。这可能使上海成为全球数字资产生态系统的关键参与者，吸引国际企业和人才。 临港新片区是上海自贸区内指定的经贸政策试验田，于 2019 年 8 月扩展至包括南汇新城和临港装备产业区等区域。该政策旨在促进资金流动和开放运输，以支持代币服务出口计划。

google_news · 一财全球Yicai Global · 8月20日 07:08

**背景**: 上海自贸区成立于 2013 年，一直是中国经济改革的先驱，2019 年新增临港新片区以进一步测试创新政策。代币服务指基于区块链的数字资产及相关服务，与比特币等加密货币不同，被视为数字化现实世界资产的一种方式。该举措与中国推动数字贸易和金融创新的更广泛努力一致，但在严格的监管框架内运作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Shanghai_Free-Trade_Zone">Shanghai Free-Trade Zone - Wikipedia</a></li>
<li><a href="https://digitalphablet.com/business/lingang-in-shanghai-ftz-to-emerge-as-global-token-services-hub/">Lingang in Shanghai FTZ to Emerge as Global Token Services Hub</a></li>
<li><a href="https://english.pudong.gov.cn/2025-06/03/c_88754.htm">Lin-gang Special Area</a></li>

</ul>
</details>

**标签**: `#blockchain`, `#tokenization`, `#policy`, `#Shanghai`, `#fintech`

---