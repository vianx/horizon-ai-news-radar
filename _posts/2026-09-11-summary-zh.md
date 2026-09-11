---
layout: default
title: "Horizon Summary: 2026-09-11 (ZH)"
date: 2026-09-11
lang: zh
---

> 从 41 条内容中筛选出 11 条重要资讯。

---

1. [OpenAI 的纳维-斯托克斯结果据称包含 Lean 4 形式化证明](#item-1) ⭐️ 9.0/10
2. [Shopify 放弃 React Native，回归原生 Swift 与 Kotlin](#item-2) ⭐️ 8.0/10
3. [研究者质疑能否将未发表的数学想法托付给 OpenAI](#item-3) ⭐️ 8.0/10
4. [OpenAI 推出托管式 Agents API，支持自托管沙箱](#item-4) ⭐️ 8.0/10
5. [Forgejo 16.0.4 修复模板展开导致的严重 RCE 漏洞](#item-5) ⭐️ 8.0/10
6. [微软将 Rust 提升为一级语言](#item-6) ⭐️ 8.0/10
7. [OpenAI 推出搭载 GPT-6 Astra 的金融版 ChatGPT](#item-7) ⭐️ 8.0/10
8. [trynix.dev 让任意 Nix 包在浏览器虚拟机中运行](#item-8) ⭐️ 8.0/10
9. [研究人员利用 Codex 和 ChatGPT 寻找新型抗菌分子](#item-9) ⭐️ 7.0/10
10. [OpenAI 在 ChatGPT Work 中推出 Data agent，面向企业数据分析](#item-10) ⭐️ 7.0/10
11. [OpenAI 与 GSA 为美国政府扩大免费 AI 访问](#item-11) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 的纳维-斯托克斯结果据称包含 Lean 4 形式化证明](https://www.johndcook.com/blog/2026/09/09/formal-method-revolution/) ⭐️ 9.0/10

据 johndcook.com 的一篇博客文章称，OpenAI 于 2026 年 9 月 8 日宣布的纳维-斯托克斯方程存在性与光滑性问题的一个无界反例，据称包含了 Lean 4 形式化证明。该发布声称 AI 在给出数学结果的同时还产出了可被机器检验的证明文件，但该结果尚未经过外部数学家的验证。 如果该 Lean 4 证明成立，这将是 AI 驱动数学发现的一个重要里程碑，因为形式化证明原则上可以通过机器检验，而不必依赖人工同行评审。这也加剧了关于 AI 能否真正解决千禧年大奖难题级别问题的争论，以及 Lean 这类形式化验证工具将如何重塑数学实践。 该结果涉及纳维-斯托克斯方程的存在性与光滑性问题，这是七个千禧年大奖难题之一；据称该反例是使用公开可用的 OpenAI 模型和未发布的 Anthropic 模型，在 Levent Alpöge 和 Tristan Buckmaster 此前工作的基础上得出的。Alpöge 和 Buckmaster 担心 OpenAI 可能将他们的对话纳入了训练数据，OpenAI 对此予以否认，而该解答仍有待外部验证。

hackernews · ibobev · 9月10日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=49650326)

**背景**: 纳维-斯托克斯方程描述粘性流体的运动，是空气动力学、血流建模等领域的核心方程。存在性与光滑性问题问的是这些方程在三维空间中是否总有光滑解，它是克雷数学研究所的千禧年大奖难题之一，正确解答可获 100 万美元奖金。Lean 4 是一个开源交互式定理证明器和函数式编程语言，基于归纳构造演算，用于编写可被计算机机械验证的证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_equations">Navier-Stokes equations</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier–Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者们在惊叹这一成就规模的同时，也对宣传口径持怀疑态度：有人指出，据称费马大定理的 Lean 验证耗时 15 小时、占用 230GB 内存，而智能体生成代码用了 11 天；也有人质疑成本对比，估算人类等效成本约为 1.32 亿美元，而非所称的四个数量级差距。一些评论者担心未来会出现 AI 解决人类无法独立验证的问题，另一些人则希望讨论能更多聚焦于实际数学结果。

**标签**: `#AI`, `#formal-verification`, `#Lean4`, `#Navier-Stokes`, `#mathematics`

---

<a id="item-2"></a>
## [Shopify 放弃 React Native，回归原生 Swift 与 Kotlin](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify 宣布将其移动应用从 React Native 迁移回完全原生的 Swift（iOS）和 Kotlin（Android），推翻了 2020 年采用跨平台框架的决定。公司表示，LLM 改变了当年决策背后的一个核心假设，因此重新进行了评估。 Shopify 的这一逆转是一个高调信号，表明围绕跨平台框架的权衡正在发生变化，尤其是 LLM 辅助代码生成降低了维护独立原生代码库的成本。这可能影响其他大型消费级应用在 React Native 与原生开发之间的取舍，并重新点燃关于共享代码库的长期争论。 此次迁移涉及用 Swift 和 Kotlin 重写应用，社区成员报告称 Codex 等 LLM 工具如今能快速为 React Native 屏幕生成原生版本，但打磨细节和边界情况仍需人工投入。Shopify 将此举定位为在核心假设改变时重新审视决策，而非否定 React Native 过去的成功。

hackernews · fnthawar2 · 9月10日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49643982)

**背景**: React Native 是一个跨平台框架，允许开发者用 JavaScript/React 编写移动应用，并在 iOS 和 Android 之间共享大量代码，这对于利用 Web 开发者很有吸引力。原生开发则分别使用 Swift（iOS）和 Kotlin（Android），为每个平台提供各自优化的代码库，但成本更高。Shopify 于 2020 年采用 React Native，此次回归反映了业界关于共享代码库何时值得权衡的更广泛争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reactnative.dev/architecture/xplat-implementation">Cross Platform Implementation · React Native</a></li>
<li><a href="https://www.aviator.co/blog/llm-agents-for-code-migration-a-real-world-case-study/">LLM Agents for Code Migration: A Real-World Case Study - Aviator Blog</a></li>
<li><a href="https://www.developers.dev/tech-talk/kotlin-vs-swift-which-is-best-for-app-development.html">Kotlin vs Swift : Which is Best for Native App Development ?</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多认可这一举措，一些 iOS 工程师表示这印证了他们长期以来对共享代码库的怀疑；但也有人反驳“LLM 使迁移变得可行”的说法，指出类似的迁移在 LLM 辅助出现之前就已完成。多位评论者认为，随着 LLM 生成原生代码的能力提升，React Native 最初让 Web 开发者构建移动应用的理由正在减弱。

**标签**: `#React Native`, `#Mobile Development`, `#Swift`, `#Kotlin`, `#Cross-Platform`

---

<a id="item-3"></a>
## [研究者质疑能否将未发表的数学想法托付给 OpenAI](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

在 OpenAI 宣称其未发布的模型解决了纳维-斯托克斯千禧年大奖难题之后，数学家们提出质疑，认为其成果与他们在与该公司的模型协作对话中分享的想法相似，却未给予应有的署名。争议的核心在于 OpenAI 是否使用了合作数学家未发表的研究成果来训练或启发其模型。 这场争议触及 AI 辅助科学的核心信任问题：研究者能否安全地使用前沿实验室的工具来研究未发表的发现，而不必担心自己的想法被吸收并在未获署名的情况下被发表。它可能重塑学术界与商业 AI 公司的合作方式，以及 AI 驱动研究中署名规范的演变。 OpenAI 坚称用于生成该结果的模型并未在这些协作对话上训练，且其内部模型正以惊人的速度解决开放问题。批评者指出，OpenAI 在得知一项重大数学证明可能存在于其训练数据中后不久，便从一个仍在训练中的模型生成了约 3000 亿个输出 token，一些人认为这颇为可疑。

hackernews · pred_ · 9月10日 06:49 · [社区讨论](https://news.ycombinator.com/item?id=49639408)

**背景**: 纳维-斯托克斯方程的存在性与光滑性问题是克雷数学研究所提出的千禧年大奖难题之一，这七个未解数学难题各设有 100 万美元奖金。像 OpenAI 这样的 AI 公司向研究者提供前沿模型的使用权限，而这些互动可能产生宝贵的训练数据和洞见。随着 AI 系统日益参与科学发现，署名和训练数据伦理已成为核心关切。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.axios.com/2026/09/08/openai-math-solution-navier-stokes-credit">OpenAI's historic math solution overshadowed by credit controversy</a></li>
<li><a href="https://www.stork.ai/blog/openais-stolen-math-proof">OpenAI Navier-Stokes Controversy: AI Authorship & Ethics | Stork.AI</a></li>
<li><a href="https://thearabianpost.com/openai-publishes-ai-proof-as-credit-dispute-grows/">OpenAI publishes AI proof as credit dispute grows — Arabian Post</a></li>

</ul>
</details>

**社区讨论**: 评论者将其类比为人类合作者：如果一位人类研究者基于合作成果发表论文却不署名，那将是极不道德的。一些人认为两件事可能同时成立——OpenAI 的模型可能从对话中提升直觉，同时也通过强化学习发现了真正新颖的技术；而另一些人则对 OpenAI 在得知一项重大证明可能存在于其训练数据中后立即生成 3000 亿个输出 token 感到可疑。

**标签**: `#AI ethics`, `#OpenAI`, `#research integrity`, `#mathematics`, `#attribution`

---

<a id="item-4"></a>
## [OpenAI 推出托管式 Agents API，支持自托管沙箱](https://developers.openai.com/api/docs/guides/agents-api/overview) ⭐️ 8.0/10

OpenAI 推出了托管式 Agents API，让开发者通过 OpenAI 托管服务访问 Codex harness，由 OpenAI 负责会话管理、编排和上下文压缩。该 API 支持可插拔工具以及可选的 自托管沙箱，并已在 openai-python 库的 3.13.0 版本中加入。 这标志着行业向 智能体即服务（agent-as-a-service）抽象层转变，开发者无需自行构建和维护 harness 即可部署智能体。这可能重塑智能体产品的构建方式，并加剧与 Anthropic 等提供类似托管智能体基础设施的厂商之间的竞争。 该 API 基于 Codex harness 构建，由 OpenAI 负责会话管理、编排和上下文压缩，开发者可以接入自定义工具，并可选地自托管沙箱。自托管选项值得关注，因为它可能降低供应商切换成本并缓解锁定顾虑。

hackernews · aquir · 9月10日 19:43 · [社区讨论](https://news.ycombinator.com/item?id=49649213)

**背景**: 智能体 harness 是围绕大语言模型的脚手架，负责处理工具调用、状态持久化和编排循环，从零构建它是一项巨大的工程投入。OpenAI 此前发布了开源的 Agents SDK，作为构建多智能体工作流的轻量级框架，而这次新的托管 API 采取了不同路线，将 harness 作为托管服务运行。自托管沙箱则允许客户在自有计算环境中运行智能体的工具调用，而非在厂商的云上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.openai.com/api/docs/guides/agents-api/overview">Agents API | OpenAI API</a></li>
<li><a href="https://openai.github.io/openai-agents-python/">OpenAI Agents SDK</a></li>
<li><a href="https://github.com/openai/openai-agents-python">GitHub - openai / openai - agents -python: A lightweight, powerful...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为行业仍在探索智能体的正确抽象方式，有人指出自建 harness 是一个深坑，而托管智能体解决了状态持久化问题，例如在没有文件系统的 Cloudflare worker 上运行。多位从业者强调自托管沙箱选项是重要吸引力，可降低供应商切换成本并缓解锁定顾虑，也有人分享了自己的自托管替代方案，并指出在个人虚拟机中运行 Codex 已经效果很好。

**标签**: `#AI Agents`, `#OpenAI`, `#API`, `#LLM`, `#Developer Tools`

---

<a id="item-5"></a>
## [Forgejo 16.0.4 修复模板展开导致的严重 RCE 漏洞](https://codeberg.org/forgejo/forgejo/src/branch/forgejo/release-notes-published/16.0.4.md) ⭐️ 8.0/10

Forgejo 发布了 16.0.4 和 15.0.8 版本，修复了一个严重的远程代码执行漏洞（CVE-2026-89094），该漏洞影响 16.0.4 之前的所有版本。攻击者可以通过构造恶意的模板仓库，在仓库初始化过程中滥用变量模板展开，从而在 Forgejo 主机上执行任意代码。 对于任何自托管 Forgejo 的组织来说，这是一个严重的安全问题，可能导致服务器完全被攻陷、数据被窃取或在网络内横向移动。由于 Forgejo 是广泛使用的自托管 Git 服务，管理员被敦促立即升级到 16.0.4 或 15.0.8。 该漏洞源于 Forgejo 在从模板仓库生成新仓库时，会克隆模板仓库、删除 .git 文件夹、对 .forgejo/template 中列出的文件进行变量模板展开，然后初始化新的 git 仓库；展开步骤对输入处理不当，导致代码注入。修复措施确保在变量展开后，删除或清理任何可能导致代码执行的现有文件或符号链接。

hackernews · weierstass · 9月10日 15:57 · [社区讨论](https://news.ycombinator.com/item?id=49645907)

**背景**: Forgejo 是 Gitea（一个流行的自托管 Git 服务）的社区驱动分支。模板仓库允许用户基于现有仓库创建预填充文件和配置的新仓库。变量模板展开会用动态值替换文件中的占位符，但如果未正确清理，就可能被利用在服务器上运行任意命令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lwn.net/Articles/1093671/">Forgejo 16.0.4 and 15.0.8 address critical security vulnerability</a></li>
<li><a href="https://www.rapid7.com/db/vulnerabilities/cve-2026-89094/">CVE-2026-89094: Forgejo : Forgejo ... | Rapid7 Vulnerability Database</a></li>
<li><a href="https://vuldb.com/vuln/402227">CVE-2026-89094 Forgejo Template Expansion code injection</a></li>

</ul>
</details>

**社区讨论**: 评论者强调了该 RCE 的严重性，并指出 Gitea 不受这些特定问题的影响。一些人就 Forgejo 最近禁止 LLM 贡献的安全影响展开辩论，认为攻击者仍可能利用 AI 寻找漏洞，从而使项目处于劣势。

**标签**: `#security`, `#vulnerability`, `#forgejo`, `#git`, `#rce`

---

<a id="item-6"></a>
## [微软将 Rust 提升为一级语言](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 8.0/10

微软已正式将 Rust 列为一级语言，使其与 C++、C# 和 TypeScript 并列，成为内部开发中支持最完善的语言之一。这一工程地位表明 Rust 现已全面融入微软的工具链、构建系统和开发者工作流。 此举验证了 Rust 的成熟度，并将其定位为 C++ 和 C# 等成熟系统语言的有力竞争者。这可能加速 Rust 在整个行业的采用，尤其是在内存安全的系统编程和全新项目中。 微软的一级语言地位意味着 Rust 在 Visual Studio 和 MSVC 工具链中获得一流支持，但社区成员指出，一级调试支持仍有待完善。这一认定也与微软更宏大的目标一致：到 2030 年利用自动化工具将 10 亿行代码转换为 Rust。

hackernews · mmastrac · 9月10日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=49643546)

**背景**: Rust 是 Mozilla 于 2010 年推出的系统编程语言，旨在不依赖垃圾回收器的情况下保证内存安全和线程安全。微软越来越多地采用 Rust 来减少与内存相关的安全漏洞，这类漏洞约占其产品 CVE 的 70%。一级语言地位是一项内部工程认定，表明该语言在全公司范围内得到生产环境的全面支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier - 1 Language at Microsoft</a></li>
<li><a href="https://news.ycombinator.com/item?id=49643546">Rust Is Tier - 1 Language at Microsoft | Hacker News</a></li>
<li><a href="https://rust-lang.org/">Rust Programming Language</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（593 分，338 条评论）总体积极，专业 Rust 开发者称这标志着 Rust 不再是初出茅庐的语言，而是 C++ 和 C# 的成熟竞争者。一些评论者强调了微软到 2030 年将 10 亿行代码转换为 Rust 的宏大目标，另一些人则询问 Visual Studio 何时能提供一级调试支持。

**标签**: `#Rust`, `#Microsoft`, `#Programming Languages`, `#Systems Programming`, `#Industry Adoption`

---

<a id="item-7"></a>
## [OpenAI 推出搭载 GPT-6 Astra 的金融版 ChatGPT](https://openai.com/index/introducing-chatgpt-financial-services) ⭐️ 8.0/10

OpenAI 正式推出 ChatGPT for Financial Services，这是一款将 Daloopa、PitchBook 和 LSEG News 等提供商的内置金融数据集与全新 GPT-6 Astra 模型相结合的专用产品。该产品面向研究、财务建模以及生成可直接交付客户的材料等场景。 这标志着 OpenAI 正从通用聊天机器人向垂直行业的企业级 AI 发力，切入受监管且数据密集的金融领域。此举可能加速银行、资产管理公司和金融科技企业对 AI 的采用，同时迫使竞争对手推出类似的金融专用 AI 产品。 该产品整合了涵盖财报电话会议记录、财务报表、公司基本面以及私营公司数据的数据集，并搭配 GPT-6 Astra——OpenAI 面向复杂推理、编程和长链条多步骤专业工作流的旗舰模型。GPT-6 Astra 目前在公开的 BenchAlign 排行榜上以 81.05/100 的成绩位列 232 个模型中的第 2 名，但其证据状态被标注为“估算”。

rss · OpenAI Blog · 9月10日 07:00

**背景**: ChatGPT 是 OpenAI 的对话式 AI 产品，而 GPT-6 Astra 是其最新的旗舰大语言模型，旨在跨软件、浏览器、代码、文档和外部工具执行长链条、多步骤任务，而不仅仅是生成文本。金融服务机构近年来越来越多地尝试将生成式 AI 用于研究、合规和客户服务，但往往缺乏对权威市场与公司数据的可靠、集成化访问。通过将授权数据集直接嵌入 ChatGPT，OpenAI 希望减少用户手动将金融数据输入通用聊天机器人的麻烦。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-chatgpt-financial-services/">Introducing ChatGPT for Financial Services | OpenAI</a></li>
<li><a href="https://www.cometapi.com/models/openai/gpt-6-astra/">GPT - 6 Astra API - Access OpenAI GPT - 6 Astra at Best... | CometAPI</a></li>
<li><a href="https://benchlm.ai/models/gpt-6-astra">GPT - 6 Astra Benchmarks & Pricing (September 2026)</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#Financial Services`, `#GPT-6`, `#Enterprise AI`

---

<a id="item-8"></a>
## [trynix.dev 让任意 Nix 包在浏览器虚拟机中运行](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

Farid Zakaria 发布了 trynix.dev，这是一个由 qemu-wasm 驱动的 x86_64 Linux 虚拟机，完全在浏览器中运行，并能启动过去 13 年间的任意 Nix 包。这些包可通过 URL 直接寻址，例如访问 trynix.dev/?pkg=python3%403.6.2 并点击“Load”，即可获得一个运行 2017 年 Python 3.6.2 的交互式 shell。 该项目让可复现的历史软件环境可以通过一个 URL 即时分享，且无需任何服务器端基础设施，这可能改变开发者审查代码和复现缺陷的方式。它也展示了基于浏览器的 WebAssembly 虚拟化已经发展到何种程度，降低了不想在本地安装 Nix 的用户尝试 Nix 的门槛。 该虚拟机基于 ktock 的 qemu-wasm 项目构建，后者将 QEMU 编译为 WebAssembly，使完整的 x86_64 Linux 系统能够在浏览器沙箱内运行。Farid 还发布了 trynix-preview，这是一个 GitHub Action，会在 pull request 上评论一条 trynix.dev 链接，让审查者能直接在浏览器中启动该 PR 的构建。

rss · Simon Willison · 9月10日 23:44

**背景**: Nix 是 Eelco Dolstra 于 2003 年创建的纯函数式包管理器，它将软件包视为不可变的值，从而实现可复现、声明式的构建。WebAssembly 是一种面向栈式虚拟机的二进制指令格式，可在所有现代浏览器中运行，而 qemu-wasm 利用它在客户端运行 QEMU 模拟器。这些技术结合在一起，使得完整的 Linux 虚拟机无需任何后端服务器即可在浏览器标签页中启动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/ qemu - wasm : QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_(package_manager)">Nix (package manager)</a></li>
<li><a href="https://webassembly.org/">WebAssembly</a></li>

</ul>
</details>

**标签**: `#Nix`, `#WebAssembly`, `#qemu`, `#reproducible-builds`, `#browser-VM`

---

<a id="item-9"></a>
## [研究人员利用 Codex 和 ChatGPT 寻找新型抗菌分子](https://openai.com/index/using-codex-chatgpt-to-search-for-new-antimicrobials) ⭐️ 7.0/10

根据 OpenAI 发布的一则案例研究，César de la Fuente 的实验室正在使用 OpenAI 的 Codex 和 ChatGPT，从现存及已灭绝生物的基因组中挖掘抗菌候选分子，以对抗耐药性感染。这项工作将 AI 编程与语言工具应用于基因组数据，用于寻找新的抗生素分子。 抗菌素耐药性是一场日益严峻的全球健康危机，而传统药物研发流程难以跟上其发展速度。展示 Codex 和 ChatGPT 这类通用 AI 工具能够加速新型抗菌药物的寻找，可能为整个制药行业指明更快、更廉价的药物发现路径。 该实验室的方法涉及对基因组序列（包括来自已灭绝生物的序列）进行计算机筛选，以寻找潜在的抗菌肽——这是一类由细菌和其他生物天然产生的小分子。Codex 协助完成筛选大规模基因组数据集所需的编程和数据处理任务，而 ChatGPT 则支持研究工作流程。

rss · OpenAI Blog · 9月10日 16:00

**背景**: 抗菌肽（AMP）是许多生物作为免疫防御的一部分而产生的短小类蛋白质分子，由于它们能通过病原体较难逃避的机制杀死细菌，因此被视为新型抗生素的有前景候选物。基因组挖掘是指通过计算机搜索 DNA 序列，寻找可能编码抗菌肽等有用分子的基因的过程。Codex 是 OpenAI 的 AI 编程工具，ChatGPT 是其对话式 AI 助手；在这里，两者都被重新用作科学研究辅助工具，而非通用的聊天或编程工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/openai-on-aws/">OpenAI models , Codex , and Managed Agents come to AWS | OpenAI</a></li>
<li><a href="https://link.springer.com/article/10.1007/s12602-026-11205-5">Integrated Genome Mining and Bioactivity-Guided Isolation of...</a></li>
<li><a href="https://camp.bicnirrh.res.in/">CAMPR4: a database of natural and synthetic antimicrobial peptides</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#drug discovery`, `#antimicrobial resistance`, `#Codex`, `#ChatGPT`

---

<a id="item-10"></a>
## [OpenAI 在 ChatGPT Work 中推出 Data agent，面向企业数据分析](https://openai.com/index/put-data-to-work) ⭐️ 7.0/10

OpenAI 在 ChatGPT Work 中推出了全新的 Data agent，用户可以用自然语言连接公司数据、挖掘洞察并构建交互式仪表盘。用户只需在 ChatGPT Work 中添加 Data Plugin，连接已有的数据源和上下文，即可开始对话。 此举让 OpenAI 更深入地进入企业分析领域，而自然语言生成仪表盘正是快速增长的赛道，可能让非技术员工无需 SQL 或 BI 专业知识即可查询公司数据。通过将数据工作流直接嵌入 ChatGPT Work，这可能对传统 BI 厂商和其他 AI 分析初创公司形成压力。 用户需在 ChatGPT Work 中添加 Data Plugin 并连接已有的数据源和上下文，之后即可通过提问获得答案、仪表盘和行动建议。该功能建立在 ChatGPT 现有的生成式 AI 能力之上，延续了此前面向企业的 Advanced Data Analysis 等文件清洗与分析功能。

rss · OpenAI Blog · 9月10日 15:00

**背景**: ChatGPT 是 OpenAI 开发的生成式 AI 聊天机器人，最初于 2022 年 11 月 30 日发布，使用大语言模型根据提示生成文本、语音和图像。ChatGPT Work 是 OpenAI 面向企业的产品，而新的 Data agent 在此基础上增加了专门的数据分析能力。自然语言生成仪表盘是一类新兴工具，让用户描述想要的可视化效果，而无需手动搭建。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/put-data-to-work/">Now everyone can put data to work | OpenAI</a></li>
<li><a href="https://community.openai.com/t/introducing-the-data-agent-for-chatgpt-work/1396488">Introducing the Data Agent for ChatGPT Work - ChatGPT - OpenAI...</a></li>
<li><a href="https://en.wikipedia.org/wiki/ChatGPT">ChatGPT - Wikipedia</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#Data Agent`, `#Enterprise AI`, `#Natural Language Interfaces`

---

<a id="item-11"></a>
## [OpenAI 与 GSA 为美国政府扩大免费 AI 访问](https://openai.com/index/expanding-ai-access-us-government) ⭐️ 7.0/10

OpenAI 与美国总务管理局（GSA）宣布合作，为符合条件的联邦、州、地方和部落政府提供零许可费、五折使用费以及扩展的网络防御支持。该计划建立在 OpenAI 现有的政府产品（如 ChatGPT Gov）之上，旨在简化公共部门对前沿 AI 模型的访问。 这一合作通过消除成本障碍，可能显著加速美国各级政府采用 AI，有望改善公共服务并加强关键基础设施的网络防御。这也标志着 AI 供应商争夺公共部门合同并影响政府 AI 政策的更广泛趋势。 该优惠包括零许可费和五折使用费，但公告中未完全详细说明资格标准和网络防御支持的具体范围。该计划可能利用 OpenAI 现有的政府专用工具，如 ChatGPT Gov 和 Codex Security。

rss · OpenAI Blog · 9月10日 07:00

**背景**: GSA 是美国政府的中央采购机构，负责管理联邦合同和共享服务。ChatGPT Gov 是 OpenAI 专为政府机构设计的聊天机器人版本，提供增强的安全性和合规性。网络防御支持指利用 AI 识别威胁、生成补丁并验证政府系统修复情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/global-affairs/introducing-chatgpt-gov/">Introducing ChatGPT Gov | OpenAI</a></li>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity | OpenAI</a></li>
<li><a href="https://dev.to/jay_all_day/openais-1-government-access-what-every-enterprise-must-know-about-the-partnership-24fg">OpenAI 's $1 Government Access : What Every... - DEV Community</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Government`, `#AI Access`, `#Cybersecurity`, `#Public Sector`

---