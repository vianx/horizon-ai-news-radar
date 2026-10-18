---
layout: default
title: "Horizon Summary: 2026-10-18 (ZH)"
date: 2026-10-18
lang: zh
---

> 从 37 条内容中筛选出 7 条重要资讯。

---

1. [DeepSeek 发布 v4.1-Flash-1017，在 11 项编码基准中 10 项超越 Sol 5.6](#item-1) ⭐️ 9.0/10
2. [爱沙尼亚开源网络投票系统代码，引发安全辩论](#item-2) ⭐️ 8.0/10
3. [全球太阳能发电量首次超过核能](#item-3) ⭐️ 8.0/10
4. [OpenAI 为 ChatGPT 新增多智能体并行处理与幻灯片功能](#item-4) ⭐️ 8.0/10
5. [iPhone 18 Pro 实现自 iOS 9 以来首个公开完整越狱](#item-5) ⭐️ 8.0/10
6. [开源 ESP32 模拟器让固件在浏览器中运行](#item-6) ⭐️ 7.0/10
7. [Vitalik Buterin 称 Tor 在其 AI 隐私方案中仍显不足](#item-7) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 v4.1-Flash-1017，在 11 项编码基准中 10 项超越 Sol 5.6](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 9.0/10

DeepSeek 于 2026 年 10 月 17 日发布了 DeepSeek-V4.1-Flash-1017，这是对 V4.1-Flash 的一次小版本更新，但在推理、编码和智能体任务上带来了显著提升，在 11 项编码基准测试中有 10 项得分超过 Sol 5.6。该模型现已在 DeepSeek 官网、应用和 API 上线，同时也可通过 OpenRouter 和 Ollama 获取。 此次发布巩固了 DeepSeek 作为 Sol 和 Gemini 等专有模型之外快速、开放替代方案的地位，尤其在编码和智能体工作流方面。其强劲的基准测试成绩和社区高度参与（Hacker News 上 688 分、579 条评论）表明市场对多样化、透明模型生态的需求日益增长。 DeepSeek-V4.1-Flash-1017 是一个多模态混合专家（MoE）模型，拥有 5520 亿骨干参数，支持高达 100 万 token 的上下文，以 deepseek-flash 的 API 模型名提供服务。尽管被称为“小版本更新”，它在性能和成本上实现了帕累托改进，任务完成更快，输出比上一版本更短。

hackernews · theykk · 10月17日 08:21 · [社区讨论](https://news.ycombinator.com/item?id=50129045)

**背景**: DeepSeek 是一家中国 AI 公司，以发布性能具有竞争力的开放权重模型而闻名。Sol 指的是 OpenAI 的 GPT-6 Sol 模型系列，Gemini 是谷歌的模型系列，两者都是专有竞争对手。OpenRouter 是一个统一的 API 平台，让开发者通过单一端点访问多种模型；Ollama 则是一个用于本地或云端运行模型的工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/news/news261017/">DeepSeek - V 4 . 1 - Flash - 1017 : Wish-Driven Programming Made Real</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V 4 . 1 Flash 1017 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://ollama.com/library/deepseek-v4.1-flash:1017-cloud">deepseek - v 4 . 1 - flash : 1017 -cloud</a></li>

</ul>
</details>

**社区讨论**: 评论者强调 DeepSeek 的速度（每秒 token 数和首 token 时间）和开放性——例如可见的思维链和更少的内容拦截——是它尽管不总是领跑基准却“感觉”更好的原因。一些人分享了真实智能体测试，显示 Sol 模型更快发现问题，而另一些人则认为像 DeepSeek 这样的生态多样性对于应对监管障碍至关重要。

**标签**: `#AI/ML`, `#LLM`, `#DeepSeek`, `#benchmarks`, `#model release`

---

<a id="item-2"></a>
## [爱沙尼亚开源网络投票系统代码，引发安全辩论](https://github.com/valimised/ivxv) ⭐️ 8.0/10

爱沙尼亚在 GitHub 上以 valimised/ivxv 仓库发布了其国家网络投票系统的源代码，使完整实现可供公众审查。此次发布在 Hacker News 上引发广泛关注，获得 154 分和 133 条评论，讨论电子选举的安全性和信任假设。 将国家选举系统开源是一个重要的透明度里程碑，使独立专家能够审计代码中的漏洞和设计缺陷。这也引发了关于基于软件的投票是否足够安全用于公共选举的更广泛辩论，影响其他国家对待电子投票的方式。 该网络投票系统在计票前使用加密将选民身份与选票分离，自 2005 年以来已在爱沙尼亚选举中使用。然而，专家指出仅靠软件无法保证选举安全；需要在选举后进行验证和统计抽样以检测故障或篡改。

hackernews · theanonymousone · 10月17日 03:18 · [社区讨论](https://news.ycombinator.com/item?id=50127586)

**背景**: 爱沙尼亚是网络投票的先驱，自 2005 年起向所有选民提供网络投票，并自 2007 年起在议会选举中广泛使用。该系统允许选民在线提交加密选票，在确认选民资格后进行解密和计票。端到端可验证（E2E）投票系统旨在提供选票被正确计票的密码学证明，但对当局的信任仍然是任何选举系统的关键组成部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jhalderm.com/pub/papers/ivoting-ccs14.pdf">Security Analysis of the Estonian Internet Voting System</a></li>
<li><a href="https://www.valimised.ee/en/internet-voting/frequently-asked-questions/questions-about-reliability-i-voting">Questions about the reliability of i - voting | Elections in Estonia</a></li>
<li><a href="https://en.wikipedia.org/wiki/End-to-end_auditable_voting">End-to-end auditable voting - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者意见不一：一些人认为仅靠软件无法保障选举安全，选举后验证至关重要；另一些人则强调爱沙尼亚长期成功的使用和对系统的信任。有人对信任的脆弱性和复杂攻击的可能性表示担忧，并提到了 ElectionGuard 等现有的可验证系统。

**标签**: `#e-voting`, `#open-source`, `#security`, `#elections`, `#trust`

---

<a id="item-3"></a>
## [全球太阳能发电量首次超过核能](https://www.pv-magazine.com/2026/09/29/solar-surpasses-nuclear-power-globally-for-first-time/) ⭐️ 8.0/10

全球太阳能发电量首次超过核能发电量，风能发电量也即将超过核能。这一里程碑得益于可再生能源装机容量的快速增长：太阳能装机容量同比增长 27%至 2383 吉瓦，而核能装机容量仅增长 1.5 吉瓦至 399.5 吉瓦。 这标志着全球能源结构的重大转变，凸显了可快速扩展的可再生能源如何超越增长缓慢的核能。它表明太阳能和风能正成为电力供应的主要支柱，对电网基础设施、能源政策和脱碳努力具有深远影响。 太阳能的领先值得注意，因为核能的容量系数要高得多（通常超过 90%，而太阳能光伏仅为 10-20%），这意味着太阳能需要远更多的装机容量才能匹配核能的发电量。下一个重要里程碑将是太阳能发电量超过水力发电，按当前增长率预计还需数年时间。

hackernews · xbmcuser · 10月17日 14:01 · [社区讨论](https://news.ycombinator.com/item?id=50131256)

**背景**: 容量系数是指一段时间内实际发电量与电厂连续满功率运行时的最大可能发电量之比。核电厂通常以高容量系数运行，因为其稳定运转，而太阳能和风能由于日照和风力的间歇性，容量系数较低。尽管如此，太阳能装机容量的巨大增长使其总发电量超过了核能。核能装机容量近四分之一世纪以来基本停滞，近期仅有小幅增长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Capacity_factor">Capacity factor - Wikipedia Renewable Energy Power Output: Capacity Factors, Wind vs ... Comparison of Photovoltaics and Nuclear Power Plants</a></li>
<li><a href="https://www.worldnuclearreport.org/Nuclear-Power-s-Quarter-century-of-Stagnation-Has-No-End-in-Sight-and-Has-Been">Nuclear Power’s Quarter-century of Stagnation Has No End in ...</a></li>

</ul>
</details>

**社区讨论**: 评论者强调，太阳能的成就是基于实际发电的太瓦时数，而不仅仅是装机容量，并指出核能的高容量系数意味着太阳能需要巨大增长才能超越。一些人对核能停滞导致无化石燃料电网推迟数十年表示遗憾，而另一些人则强调需要进一步加速清洁能源以替代所有化石能源用途，包括化工原料。

**标签**: `#energy`, `#solar-power`, `#nuclear-power`, `#renewables`, `#infrastructure`

---

<a id="item-4"></a>
## [OpenAI 为 ChatGPT 新增多智能体并行处理与幻灯片功能](https://x.com/OpenAI/status/2111192259073094035) ⭐️ 8.0/10

OpenAI 在连续 28 天更新的第 12 天宣布，GPT-6 Astra Pro 在 ChatGPT 中迎来升级，响应速度更快，插件与工具调用能力也得到改善。现在多个智能体可以并行处理同一任务的不同部分，用户可查看各项任务的进度，并打开已完成的子任务查看详情，该功能正逐步向 Pro 用户开放，可在对话标签页中使用。 此次更新标志着 ChatGPT 从单轮对话转向并行的多智能体任务执行，有望大幅提升复杂工作流的生产力，并为 AI 助手树立新的竞争标杆。同时，它还将 ChatGPT 从对话工具扩展为演示文稿创作平台，直接挑战现有的 AI 幻灯片生成器和办公套件。 Codex 与 Work 通过跨子智能体复用上下文、延长上下文缓存时间和改进请求路由以提高缓存命中率，进而提升有效用量。ChatGPT Slides 正逐步面向具备 Space 访问权限的 Pro、Business 和 Enterprise 用户开放，演示文稿可导出至 PowerPoint 或 Google Slides。

telegram · zaihuapd · 10月17日 02:05

**背景**: GPT-6 Astra 是 OpenAI 的最新一代模型，面向 ChatGPT Plus、Pro、Business 和 Enterprise 用户开放，也可通过 API、Azure 和 AWS Bedrock 使用。GPT-6 Astra Pro 与 GPT-6 Astra 共享相同权重，但推理设置不同，Pro 提供更高的推理预算。多智能体系统允许多个 AI 智能体协调和委派工作，OpenAI 的 Agents SDK 已支持智能体即工具和交接等模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-astra/">GPT-6 Astra: A new generation of intelligence | OpenAI</a></li>
<li><a href="https://www.orcarouter.ai/blog/gpt-6-astra-pro-vs-gpt-6-astra">GPT-6 Astra Pro vs GPT-6 Astra: Same Weights, Two Dials</a></li>
<li><a href="https://openai.github.io/openai-agents-python/">OpenAI Agents SDK</a></li>
<li><a href="https://chatgpt.com/features/slides/">ChatGPT Slides | Create, edit, and chat with presentations</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#multi-agent`, `#AI`, `#product update`

---

<a id="item-5"></a>
## [iPhone 18 Pro 实现自 iOS 9 以来首个公开完整越狱](https://x.com/calif_io/status/2111080240978223545?s=20) ⭐️ 8.0/10

安全研究员 Calif 公开展示了针对 iPhone 18 Pro 的 untethered 越狱，这是自 iOS 9 以来首个此类越狱。该越狱在设备重启后仍保持越狱状态，且无需连接电脑，利用了涉及 cryptex 子系统、TSS 票签欺骗和 PAC 绕过的三层攻击链。 这是一个重要的安全里程碑，因为它表明即使 Apple 在 9 月 14 日修补了 273 个漏洞，针对最新硬件的未公开攻击链仍然存在。这凸显了 iOS 安全面临的持续挑战，并将影响安全研究员、越狱开发者和 Apple 的漏洞管理。 该攻击链结合了三层：滥用 cryptex 子系统（用于密封系统组件）、欺骗 TSS（票签签名服务器）票签以绕过签名检查，以及绕过 PAC（指针认证码）以破坏 ARM 硬件指针完整性。该演示由 @calif_io 展示，并显示设备重启后可通过 SSH 获得完整 root 访问权限。

telegram · zaihuapd · 10月17日 10:34

**背景**: Untethered 越狱是指设备重启后仍保持越狱状态，无需重新连接电脑，这与 tethered 或 semi-tethered 越狱不同。Cryptex 子系统是现代 iOS 中用于挂载密封系统卷的组件，而 TSS 票签被 Apple 用于授权固件签名。PAC 是 ARMv8.3-A 引入的硬件安全特性，在 Apple 的 A12 及后续芯片中实现，通过对指针进行加密签名来增加内存破坏漏洞利用的难度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/ios-27-0-1-jailbreak-demonstrated/">iOS 27.0.1 Untethered Jailbreak Demonstrated on iPhone 18 Pro</a></li>
<li><a href="https://www.idownloadblog.com/2024/10/14/alfiecg_dev-pac-bypass-0-day/">Security researcher alfiecg_dev discovers 0-day PAC bypass ... Bypassing Pointer Authentication on iPhone | Infosec CVE-2026-20700 How DarkSword Defeated Apple's Hardware ... What is PAC and why is it helpful to be bypassed? : r/jailbreak</a></li>
<li><a href="https://eclecticlight.co/2022/11/16/cryptex-how-a-custom-iphone-is-changing-macos-updates/">Cryptex : how a custom iPhone is changing macOS updates</a></li>

</ul>
</details>

**标签**: `#iOS security`, `#jailbreak`, `#exploit chain`, `#PAC bypass`, `#Apple`

---

<a id="item-6"></a>
## [开源 ESP32 模拟器让固件在浏览器中运行](https://github.com/mikroverk/esp32sim) ⭐️ 7.0/10

一位开发者发布了 esp32sim，这是一个开源的 ESP32 模拟器，通过 WebAssembly 在浏览器中运行真实固件，并附有一段演示视频，展示无需任何物理 ESP32 硬件即可执行固件。 这降低了嵌入式开发者无需硬件即可实验、测试和模拟 ESP32 软件的门槛，有望为物联网项目实现 CI/CD 流水线和更快的迭代。 该模拟器托管在 GitHub 的 mikroverk/esp32sim 下，至少支持 ESP32-S3 开发板，但社区反馈指出文档密集且格式不佳，可能会阻碍采用。

hackernews · joakimeriksson · 10月17日 13:51 · [社区讨论](https://news.ycombinator.com/item?id=50131189)

**背景**: ESP32 是一款广受欢迎的低成本微控制器，内置 Wi-Fi 和蓝牙，广泛用于物联网和爱好者项目。此类模拟器使用 WebAssembly 在浏览器沙箱中运行编译后的固件，模拟微控制器的 CPU 和外设，使开发者无需物理板即可测试代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/mikroverk/esp32sim">GitHub - mikroverk/esp32sim: Open-source ESP32 emulator. Run ...</a></li>
<li><a href="https://espressif.github.io/esp-emulator/">ESP-EMU — ESP32 emulator in the browser</a></li>
<li><a href="https://www.cirkitdesigner.com/esp32-simulator">ESP32 Simulator Online - Cirkit Designer</a></li>

</ul>
</details>

**社区讨论**: 评论者认为该项目很酷，并分享了相关工作，例如一个以 WebAssembly 运行 ESP32 飞控代码的无人机模拟器，还讨论了 CI/CD 测试和功能模拟等用例。一些人批评文档的 AI 生成风格难以阅读，还有人询问它与成熟的在线模拟器 Wokwi 有何不同。

**标签**: `#ESP32`, `#emulator`, `#embedded-systems`, `#WebAssembly`, `#open-source`

---

<a id="item-7"></a>
## [Vitalik Buterin 称 Tor 在其 AI 隐私方案中仍显不足](https://news.google.com/rss/articles/CBMitwFBVV95cUxPTzBYcGJsTW1NTm5XbjdFRVpJVElwT2lJVk15NTV1dEhBclRoOGpSSUYzZjNWMEdUejdhbXZYb083OGpydXZkZTFkeldNZkdIWkE4V1VjVkhScnBvU1Z3LV9qbWVCZlJGTFl2VVZUMzhBR3JyVlBUU2hsQXJ1ZDBCcXZaSzRCb0xzbmlJVmItTDM5dmZRcm1SZmR1dU9ORVR5Q0Nrc1Q5Y2dhTFJmcnNBd1hidFk0bUE?oc=5) ⭐️ 5.0/10

据 CryptoRank 新闻摘要报道，以太坊联合创始人 Vitalik Buterin 警告称，Tor 匿名网络在他个人的 AI 隐私方案中仍显不足。他描述了自己用个人健康和旅行数据测试 AI 建议的过程：先由本地模型处理查询，再通过 zkAPI 向远程前沿模型发送有限请求。 这凸显了 Tor 等传统网络层匿名工具与现代 AI 工作流隐私需求之间日益扩大的差距——提示词本身就可能泄露敏感数据。Buterin 的公开实验可能会推动开发者转向本地优先与零知识证明相结合的混合 AI 隐私架构。 据报道，该方案结合了本地模型处理、Tor 路由、zkAPI 支付和提示词重写，以限制远程前沿模型可见的内容。但消息来源仅为简短标题，缺乏技术细节，因此 Buterin 所指出的 Tor 具体缺陷仍不明确。

google_news · CryptoRank · 10月17日 05:44

**背景**: Tor 是一个由志愿者运营的匿名网络，通过多跳中继路由流量以隐藏用户 IP 地址并抵抗审查。随着 AI 助手越来越多地处理个人数据，研究人员正在探索本地模型、可信执行环境和零知识证明等替代方案，以使提示词对云服务商保持私密。Tor 浏览器开发者自己也因隐私和可审计性问题而拒绝了 AI 功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.cryptonomist.ch/2026/10/16/privacy-ai-agent-vitalik/">Privacy AI Agent Enhancements by Vitalik Buterin</a></li>
<li><a href="https://cryptopanic.com/news/33496497/Vitalik-Puts-AI-Privacy-to-The-Test-Ethereum-co-founder-Vitalik-Buterin-VitalikButerin-says-he-tested-AI-recommendations-using-personal-health-and-travel-data-A-local-model-handled-queries-before-sending-limited-requests-to-remote-frontier-models-The-setup">Vitalik Puts AI Privacy to The Test Ethereum co-founder Vitalik ...</a></li>
<li><a href="https://support.torproject.org/about-tor/how-tor-works/overview/">Overview - How Tor works - About Tor — Tor</a></li>

</ul>
</details>

**标签**: `#privacy`, `#Tor`, `#AI`, `#Vitalik Buterin`, `#security`

---