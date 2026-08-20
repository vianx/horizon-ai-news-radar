---
layout: default
title: "Horizon Summary: 2026-08-20 (ZH)"
date: 2026-08-20
lang: zh
---

> 从 41 条内容中筛选出 11 条重要资讯。

---

1. [恶意 Rust crate arrayref 在构建时执行载荷](#item-1) ⭐️ 9.0/10
2. [GitHub 8 月 17 日宕机：重试循环与 AI 流量激增](#item-2) ⭐️ 8.0/10
3. [AliExpress 静默 WebAudio 指纹识别干扰蓝牙多点连接](#item-3) ⭐️ 8.0/10
4. [文章反思教育如何扼杀生物学的奇妙](#item-4) ⭐️ 8.0/10
5. [用 1.25 亿参数 Transformer 实现设备端钢琴自动补全](#item-5) ⭐️ 8.0/10
6. [Linux 7.2 发布，支持 HDMI 2.1](#item-6) ⭐️ 8.0/10
7. [Bun 1.4 的 Bun.WebView 驱动类似 shot-scraper 的 JSON API](#item-7) ⭐️ 8.0/10
8. [OpenAI 推出 AI Futures 博客，探讨社会影响](#item-8) ⭐️ 7.0/10
9. [阿里巴巴 2026 财年第一季度销售额增长 9%，AI 投入拖累利润](#item-9) ⭐️ 6.0/10
10. [临港新片区将成代币服务出口全球枢纽](#item-10) ⭐️ 6.0/10
11. [Stampli 使用 ChatGPT Work 将发布工时减少 68%](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [恶意 Rust crate arrayref 在构建时执行载荷](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

流行的 Rust crate 'arrayref' 的一个恶意版本被发布到 crates.io，其中包含一个 proc-macro1 构建脚本，在编译期间下载并执行远程载荷。恶意版本随后已从 crates.io 移除，Rust 团队发布了安全公告。 此次攻击凸显了 Rust 生态系统中严重的供应链漏洞，一个广泛使用的 crate 被攻破并在构建时执行恶意软件。这强调了 crates.io 需要改进安全措施，并引发了关于标准库设计和构建脚本沙箱化的讨论。 恶意载荷通过 proc-macro1 构建脚本传递，这很不寻常，因为大多数攻击使用 build.rs 脚本。该活动与朝鲜相关的供应链攻击有重叠，crates.io 的回应因缺乏透明度而受到批评，因为恶意版本被移除时没有明确的 yank 通知或安全公告。

hackernews · abhisek · 8月20日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=49374269)

**背景**: Rust 的包注册表 crates.io 是库和工具的中心存储库，Cargo 是下载和编译依赖项的构建系统。构建脚本（build.rs）和过程宏在编译期间执行，使其成为供应链攻击的主要目标。Rust 标准库有意保持精简，鼓励使用第三方 crate，这增加了攻击面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build-Time Malware in Crates ...</a></li>
<li><a href="https://www.wiz.io/blog/rust-supply-chain-attack-on-arrayref-significant-overlap-with-dprk-campaigns">Rust Supply Chain Attack on arrayref: Significant Overlap ...</a></li>
<li><a href="https://socket.dev/blog/popular-rust-crates-compromised">Popular Rust Crates Compromised in Build-Time Supply Chain Attack</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 crates.io 处理此次事件表示不满，指出缺乏 yank 通知或公告。一些用户主张采用“电池包含”的方法来扩展标准库，以减少对第三方 crate 的依赖，而另一些用户则呼吁 Cargo 对构建脚本进行沙箱化。还有人讽刺地说，至少这个漏洞是内存安全的。

**标签**: `#security`, `#supply-chain`, `#rust`, `#malware`, `#crates.io`

---

<a id="item-2"></a>
## [GitHub 8 月 17 日宕机：重试循环与 AI 流量激增](https://github.blog/news-insights/company-news/the-august-17-outage-and-the-work-ahead/) ⭐️ 8.0/10

GitHub 发布了 8 月 17 日宕机的复盘报告，揭示基础设施故障、客户端重试循环以及 AI 驱动流量激增（自 4 月以来月度提交量从 14 亿翻倍至 29 亿）共同导致了长达 7 小时 47 分钟的长时间服务中断。 此次宕机凸显了为满足 AI 驱动需求而扩展基础设施的系统性挑战，影响了数百万开发者和 Copilot 用户。它强调了在 AI 编码工具成为主流之际，健壮的重试管理和容量规划的必要性。 宕机始于美国中部地区的网络饱和，触发了客户端重试循环，将流量放大约 10 倍，延迟了认证路径和 Copilot 令牌服务的恢复。GitHub 工程师不得不限制重试以使认证层得以恢复。

hackernews · 0xedb · 8月20日 19:22 · [社区讨论](https://news.ycombinator.com/item?id=49378957)

**背景**: GitHub 是微软旗下广泛使用的代码托管平台，服务超过 1.8 亿开发者。像 GitHub Copilot 这样的 AI 辅助编码工具推动了流量激增，自 4 月以来月度提交量从 14 亿增长到 29 亿。重试循环是指客户端自动重试失败的请求，这可能会使本已处于压力下的系统不堪重负，形成反馈循环，延长宕机时间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xenospectrum.com/en/github-outage-retry-storm/">Why Did the GitHub Outage Last 7 Hours 47 Minutes? | XenoSpectrum</a></li>
<li><a href="https://dev.to/prasadmk/what-the-github-outage-taught-us-about-authentication-retries-1lbn">What the GitHub Outage Taught Us About Authentication Retries</a></li>
<li><a href="https://www.theregister.com/software/2026/06/12/github-outages-persist-as-ai-coding-drives-traffic-surge/5255125">GitHub outages persist as AI coding drives traffic surge</a></li>

</ul>
</details>

**社区讨论**: 社区评论对重试循环设计表示不满，一位用户指出，不惜一切代价隐藏错误会导致用户长时间盯着加载动画。其他人对流量增长感到惊叹，称其“疯狂”，并认为是“生产力恐慌”的证据。一些人建议通过收费来减少 AI 重度用户，但认为微软不太可能这样做，因为它从 AI 采用中获益；还有用户质疑在连接良好的桌面环境中激进重试的合理性。

**标签**: `#outage`, `#post-mortem`, `#GitHub`, `#reliability`, `#AI`

---

<a id="item-3"></a>
## [AliExpress 静默 WebAudio 指纹识别干扰蓝牙多点连接](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

AliExpress 被发现其网站使用静默 WebAudio 指纹识别技术，该技术会干扰用户设备上的蓝牙多点连接功能。此技术通过播放听不见的音频来生成独特的设备指纹，无意中破坏了同时进行的蓝牙连接。 这引发了重大的隐私担忧，因为它可以在未经同意的情况下跟踪用户，并且通过破坏蓝牙多点连接降低了用户体验，影响了众多依赖此功能的用户。这凸显了浏览器需要更好的防护措施来应对此类隐蔽的指纹识别技术。 该指纹识别技术通过 Web Audio API 播放静音音频，根据设备的硬件和软件产生独特的特征。这可能导致浏览器被视为活跃的音频源，从而使蓝牙多点连接被中断或切换。该问题在桌面和移动浏览器上均有出现，AliExpress 移动应用也被指涉及类似的蓝牙干扰。

hackernews · emctech · 8月20日 10:08 · [社区讨论](https://news.ycombinator.com/item?id=49372583)

**背景**: WebAudio 指纹识别是一种跟踪技术，利用 Web Audio API 测量设备处理音频信号时的细微差异，从而在无需权限的情况下创建唯一标识符。蓝牙多点连接允许单个耳机同时连接多个设备（如手机和笔记本电脑），并在它们之间自动切换音频。当网站播放静音音频时，可能会欺骗设备以为正在播放音频，从而干扰多点切换逻辑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fingerprint.com/blog/audio-fingerprinting/">Audio Fingerprinting: What It Is + How It Works with Web API</a></li>
<li><a href="https://browserinsight.net/blog/audio-fingerprinting">Audio Fingerprinting: How AudioContext Identifies Your Device</a></li>
<li><a href="https://www.soundguys.com/bluetooth-multipoint-explained-28601/">What is Bluetooth multipoint? - SoundGuys</a></li>

</ul>
</details>

**社区讨论**: 社区成员分享了在访问某些网站或使用 AliExpress 应用时遇到蓝牙中断的个人经历，有些人指出关闭应用即可解决问题。其他人讨论了 WebAudio 指纹识别的技术细节及其在浏览器中的缓解措施，而一些人则对苹果执行隐私政策表示怀疑。总体而言，大家对 AliExpress 的做法持批评态度，并对隐私影响表示担忧。

**标签**: `#privacy`, `#fingerprinting`, `#WebAudio`, `#security`, `#Bluetooth`

---

<a id="item-4"></a>
## [文章反思教育如何扼杀生物学的奇妙](https://jsomers.net/i-should-have-loved-biology/) ⭐️ 8.0/10

文章《我本应热爱生物学》（2020 年）由 jsomers.net 发布，反思传统教育如何削弱生物学的天然奇妙感，倡导更以发现为导向的学习方法。该文获得 8.0/10 的高分，并引发了关于教学法和科学发现的深入讨论。 这篇文章引起了许多读者（尤其是 STEM 领域人士）的共鸣，指出了教育中死记硬背的普遍问题。它将个人反思与更广泛的教育批评相结合，可能影响教育者和学生对待科学学习的方式。 这篇文章是一篇反思性文章，而非技术报告，基于作者在生物学教育中的个人经历。它强调发现和惊奇的重要性，与通常优先记忆而非探索的传统课程形成对比。

hackernews · tyre · 8月20日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=49377853)

**背景**: 传统科学教育往往侧重于记忆事实和公式，这可能会掩盖最初吸引人们学习生物学等学科的好奇心和惊奇感。这篇文章呼应了关于教学改革的更广泛讨论，与 Seymour Papert 和 Jean Piaget 等思想家的理念相呼应，他们主张通过互动和发现来学习。

**社区讨论**: 社区评论既有赞同也有个人轶事。一些读者分享了自己尽管教学不佳却热爱生物学的经历，而另一些人则指出生命科学被浪漫化的观点以及研究工作的现实。还有人将其与 Papert 和 Piaget 的教学哲学联系起来，强调了对传统教育的共同批评。

**标签**: `#biology`, `#education`, `#pedagogy`, `#science`, `#reflection`

---

<a id="item-5"></a>
## [用 1.25 亿参数 Transformer 实现设备端钢琴自动补全](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

一位开发者训练了一个 1.25 亿参数的 Transformer 模型，在 iPhone 15 上实时自动补全钢琴演奏，推理速度约每秒 108 个音符。该应用免费，并完全在设备端通过 Core ML 运行。 这展示了设备端 AI 在创意领域的新应用，可能激发新的音乐创作工具。同时，它也凸显了在消费级硬件上高效运行小型 Transformer 模型的可行性，这可能降低类似创意 AI 项目的门槛。 该模型使用 MIDI 表示，并通过积极的数据清洗和 DPO 后训练得到改进。开发者指出，找到合适的 MIDI 表示是性能的关键，项目开发耗时约一年。

hackernews · simedw · 8月20日 12:04 · [社区讨论](https://news.ycombinator.com/item?id=49373456)

**背景**: Transformer 模型通常用于文本生成，但也可应用于音乐等序列数据。Core ML 是苹果的设备端推理引擎，可将模型优化以在神经引擎、GPU 或 CPU 上运行。该项目将代码自动补全（如 GitHub Copilot）的概念应用于音乐，用户弹奏几个音符，模型便续写旋律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simedw.com/2026/08/20/midi-autocomplete/">Training a 125M-parameter Model to Autocomplete Piano</a></li>
<li><a href="https://blakecrosley.com/blog/core-ml-on-device-inference">Core ML On-Device Inference: The Patterns That Actually Ship</a></li>
<li><a href="https://developer.apple.com/videos/play/wwdc2024/10161/">Deploy machine learning and AI models on-device with Core ML - WWDC24 - Videos - Apple Developer</a></li>

</ul>
</details>

**社区讨论**: 评论者将其与古典作曲家的训练方法及 AI 设计工具相提并论，指出生成成本已趋近于零，品味成为关键差异。有人询问训练数据规模，也有人觉得模型产生的意外音乐方向令人不安但有趣。

**标签**: `#AI/ML`, `#Music Generation`, `#On-device AI`, `#Transformer`, `#Core ML`

---

<a id="item-6"></a>
## [Linux 7.2 发布，支持 HDMI 2.1](https://www.igalia.com/2026/08/19/Linux-72-Released.html) ⭐️ 8.0/10

Linux 内核 7.2 已发布，其中包含 HDMI 2.1 支持等改进。该版本还引入了缓存感知调度，并回滚了导致 GPU 性能回退的 DRM 调度器更改。 此版本对开源社区意义重大，因为它为 Linux 带来了现代显示连接技术，可能改善游戏玩家和专业用户的体验。HDMI 2.1 支持也可能影响硬件采用和驱动程序开发。 内核中的 HDMI 2.1 支持此前曾受到 HDMI 论坛的阻碍，但此版本表明情况已发生变化。此外，Linux 7.2 预计将成为 Ubuntu 26.10 及其他即将发布的发行版的默认内核。

hackernews · mariuz · 8月20日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=49376265)

**背景**: HDMI 2.1 支持更高的带宽和可变刷新率等功能，对现代显示器很重要。DisplayPort 是常见的替代方案，两者之间的选择取决于设备兼容性和具体需求。Linux 内核是许多操作系统的核心，其更新带来新的硬件支持和性能改进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://itsfoss.com/news/linux-kernel-7-2-release/">Linux 7 . 2 Arrives With Cache Aware Scheduling After More Than...</a></li>
<li><a href="https://www.linuxjournal.com/content/linux-72-reverts-drm-scheduler-change-after-serious-gpu-regressions">Linux 7 . 2 Reverts DRM Scheduler Change After... | Linux Journal</a></li>
<li><a href="https://www.phoronix.com/news/Linux-7.2-rc7-Released">Linux 7 . 2 -rc7 Released Following Another Exhausting... - Phoronix</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 HDMI 2.1 支持如何在先前受阻的情况下成为可能表示好奇，也有人质疑此类新闻的目标受众。其他人则将 HDMI 与 DisplayPort 进行比较，想知道实际好处，而一位用户则对更新其树莓派 4 感到兴奋。

**标签**: `#Linux`, `#kernel`, `#HDMI`, `#open-source`, `#release`

---

<a id="item-7"></a>
## [Bun 1.4 的 Bun.WebView 驱动类似 shot-scraper 的 JSON API](https://simonwillison.net/2026/Aug/20/bun-webview-json-api/) ⭐️ 8.0/10

Simon Willison 发布了一个研究原型，展示了基于 Bun 1.4 新 Bun.WebView 的类似 shot-scraper 的 JSON API。该原型加载网页并对其执行 JavaScript，利用了 Bun.WebView 内置的浏览器自动化功能。 这展示了 Bun.WebView 的新颖用途，通过消除对外部工具（如 Puppeteer 或 Playwright）的需求，可能简化浏览器自动化。同时，它也凸显了 Bun 1.4 的性能改进和新特性，对 JavaScript 生态系统意义重大。 该原型是一个 TypeScript 服务器，需要 192MB-256MB 的容器才能针对复杂网页运行完整的 Chrome，并使用 cgroups 进行了测试。Bun.WebView 支持 macOS WebKit 和通过 Chrome DevTools 协议（CDP）控制的本地 Chromium。

rss · Simon Willison · 8月20日 15:37

**背景**: Bun 1.4 是一个重要版本，包含从 Zig 到 Rust 的重写，以及 Bun.Image、Bun.WebView、Bun.markdown 和 Bun.cron() 等新功能。Bun.WebView 是运行时内置的无头浏览器，允许开发者加载页面、运行 JavaScript、模拟用户输入和捕获截图，而无需外部依赖。shot-scraper 是 Simon Willison 开发的一个 CLI 工具，使用 Playwright 自动化截图和抓取。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bun.com/docs/runtime/webview">WebView | Bun Docs</a></li>
<li><a href="https://bun.com/reference/bun/WebView">Bun.WebView object | API Reference | Bun</a></li>
<li><a href="https://shot-scraper.datasette.io/">shot-scraper</a></li>

</ul>
</details>

**标签**: `#Bun`, `#WebView`, `#JSON API`, `#JavaScript`, `#Web Development`

---

<a id="item-8"></a>
## [OpenAI 推出 AI Futures 博客，探讨社会影响](https://openai.com/index/introducing-ai-futures) ⭐️ 7.0/10

OpenAI 宣布推出 AI Futures，这是一个新的博客系列，旨在探讨变革性 AI 如何重塑权力、治理、经济和个体自由。该公告通过 OpenAI 官方网站发布。 这一举措表明 OpenAI 致力于参与 AI 更广泛的社会和政策影响讨论，而不仅仅是技术发展。随着 AI 的快速发展，它可能会影响公众讨论和政策制定。 该博客系列将涵盖权力、治理、经济和个体自由等主题，表明其关注点在于高层次的社会影响而非技术细节。公告内容简短，未指定发布时间表或作者名单。

rss · OpenAI Blog · 8月20日 07:00

**背景**: OpenAI 是一家领先的 AI 研究机构，以开发 GPT-4 和 ChatGPT 等先进模型而闻名。随着 AI 能力的增强，人们越来越关注其社会影响，包括经济颠覆、治理挑战以及对个体自由的影响。AI Futures 似乎是 OpenAI 分享其对这些问题的看法的平台。

**标签**: `#OpenAI`, `#AI policy`, `#AI governance`, `#AI impact`, `#blog`

---

<a id="item-9"></a>
## [阿里巴巴 2026 财年第一季度销售额增长 9%，AI 投入拖累利润](https://news.google.com/rss/articles/CBMi4wFBVV95cUxOS3J2dThHdVdSVV92ZHF0bGxxZHVuYlpkb2QtX3BRVWtYeVhiQzZkaGNJalNYQVBPUU1UMmpQOGctcDRzNE9PYWxSTVJQcFFONTYxRFFFZFhBa1cyODNKVDNQUUtfS3ZiQXY0ZGdoTUh5UG9NTFk0X3hTZnhNN3ZKckI5Wldla3ZYeTlrNk8tS2xyOXpaM25ENm9hSE1ibzJ3VDhRei1fWVhvMnBlSG53REVzVms4NVpON0xZbW1oRTlXbWF0SktYMk9SbElHQWhXalhsN0o1MTdrTVFQNk1GR3VOQQ?oc=5) ⭐️ 6.0/10

阿里巴巴公布 2026 财年第一季度销售额同比增长 9%，但对人工智能的大规模投入拖累了盈利能力。Investing.com 南非站发布的财报电话会议记录凸显了增长与 AI 投资之间的张力。 这份财报意义重大，因为它展示了大型科技公司如何平衡 AI 投资与财务表现。阿里巴巴的业绩可能影响投资者对整个行业重金投入 AI 策略的看法。 报告显示，尽管销售额增长了 9%，但利润因 AI 相关支出增加而受到负面影响。摘要中未提供净利润或 AI 支出的具体数字，但趋势明确。

google_news · Investing.com South Africa · 8月20日 02:26

**背景**: 阿里巴巴是中国最大的电子商务和云计算公司之一，一直在大力投资 AI 以与全球竞争对手抗衡。财报电话会议是常规的财务更新，但能揭示公司的战略重点。9%的销售增长表明业务持续扩张，而利润压力则反映了 AI 开发的成本。

**标签**: `#Alibaba`, `#earnings`, `#AI investment`, `#financial results`, `#tech industry`

---

<a id="item-10"></a>
## [临港新片区将成代币服务出口全球枢纽](https://news.google.com/rss/articles/CBMitAFBVV95cUxQd3NmbXppeDV1cUJ1Y3NQdERlcGlJbG1KRV9ER1BUamtPZXVNVWE1VWIwMXBLTWJSVGZESmhCdW80X0diLWVScy1iVDNuanNhMXV5V3Z5eEtEU185aHFWVFh2a3pEWjVXR2RseGNxZDlpQUFjMGQ4a2J0LWw5aUExamk3VmxPS1Zfb1JWRFlRcFBVOElfODZRbzMyMmY4UUl2LUZTUWZNb1ZtVlZvcTliMXBHWFQ?oc=5) ⭐️ 6.0/10

上海自贸区临港新片区宣布计划成为具有全球影响力的代币服务外贸枢纽。该区域将建立一站式合规服务平台，提供数据安全评估、标准合同生成、跨境规则查询和自动适配等服务。 此举标志着中国在区块链和加密货币监管方面迈出重要一步，可能使临港成为国际代币服务的关键参与者。它可能吸引全球企业，并影响全球代币服务的监管和出口方式。 该公告由一位姓陈的官员发布，平台旨在促进跨境代币服务。临港新片区于 2019 年作为上海自贸区扩区的一部分成立，专注于制度创新和全球竞争力。

google_news · 一财全球Yicai Global · 8月20日 07:08

**背景**: 临港新片区是上海自贸区内的特殊经济功能区，以制度创新和聚焦国际贸易与先进制造业著称。代币服务指与数字代币相关的服务，如发行、交易和合规，属于更广泛的区块链和加密货币生态系统的一部分。这一举措与中国探索受监管的区块链应用，同时严格控制加密货币交易的方针一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.yicaiglobal.com/news/shanghai-ftzs-lingang-special-area-to-become-global-hub-for-token-services-export">Shanghai FTZ's Lingang Special Area to Become Global Hub for Token ...</a></li>
<li><a href="https://en.lingang.gov.cn/">Lin-gang Special Area</a></li>
<li><a href="https://en.wikipedia.org/wiki/Shanghai_Free-Trade_Zone">Shanghai Free-Trade Zone - Wikipedia</a></li>

</ul>
</details>

**标签**: `#blockchain`, `#cryptocurrency`, `#regulation`, `#Shanghai`, `#token services`

---

<a id="item-11"></a>
## [Stampli 使用 ChatGPT Work 将发布工时减少 68%](https://openai.com/index/stampli) ⭐️ 5.0/10

金融自动化公司 Stampli 通过使用 OpenAI 的 Codex 和 ChatGPT Work，将发布生产时间减少了 68%，将数周的工作压缩到几天内完成。OpenAI 发布此案例研究，以展示其 AI 工具的实际影响。 该案例研究凸显了 AI 编码代理和工作场所 AI 工具如何显著加速软件开发和发布流程，可能重塑科技行业的生产力基准。它为 AI 辅助工作流程的价值提供了具体证据，可能影响其他公司的采用决策。 Stampli 面临固定截止日期，且设计资源已投入其他项目，因此他们利用 Codex 和 ChatGPT Work 来简化发布生产。工时减少 68% 表明效率大幅提升，但案例研究未披露具体项目细节或指标。

rss · OpenAI Blog · 8月20日 00:00

**背景**: OpenAI Codex 是一款 AI 编码代理，于 2025 年 4 月发布，可通过 ChatGPT、CLI、桌面应用和 IDE 集成使用，旨在处理编写代码和修复错误等软件工程任务。ChatGPT Work 由 GPT-5.6 驱动，是一款工作场所工具，可与团队工具集成，将笔记和草稿转化为成品，保持项目推进。这些工具代表了工作场所中 AI 辅助开发和生产力提升的更广泛趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/chatgpt-work/">ChatGPT Work for every team | OpenAI</a></li>
<li><a href="https://openai.com/index/chatgpt-for-your-most-ambitious-work/">ChatGPT is now a partner for your most ambitious work</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#productivity`, `#case study`, `#AI tools`

---