---
layout: default
title: "Horizon Summary: 2026-07-13 (EN)"
date: 2026-07-13
lang: en
---

> From 30 items, 9 important content pieces were selected

---

1. [GPT-5.6 Solves 50-Year Graph Theory Conjecture in 1 Hour](#item-1) ⭐️ 9.0/10
2. [xAI Grok CLI Uploads Entire Codebase and Secrets by Default](#item-2) ⭐️ 9.0/10
3. [Claude Code Sends 33k Tokens Before Prompt vs OpenCode's 7k](#item-3) ⭐️ 8.0/10
4. [Terry Tao on Building Apps with LLM Coding Agents](#item-4) ⭐️ 8.0/10
5. [Zer0Fit: MCP Server for Google's TabFM & TimesFM](#item-5) ⭐️ 8.0/10
6. [Quadriplegic Patient Regains Grip with NEO BCI](#item-6) ⭐️ 8.0/10
7. [Simon Willison: AI Agents Should Never Be DRIs](#item-7) ⭐️ 6.0/10
8. [Anthropic Extends Claude Fable 5 Access Amid Compute Constraints](#item-8) ⭐️ 5.0/10
9. [sqlite-utils 4.1.1 Fixes Transaction Edge Case](#item-9) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Solves 50-Year Graph Theory Conjecture in 1 Hour](https://www.qbitai.com/2026/07/447873.html) ⭐️ 9.0/10

OpenAI's GPT-5.6 Sol Ultra autonomously proved the cycle double cover conjecture, a 50-year-old open problem in graph theory, in under an hour using 64 parallel sub-agents and generated a 3-page PDF proof. This marks the first time an AI has autonomously solved a long-standing open mathematical problem, demonstrating advanced reasoning and multi-agent collaboration that could revolutionize mathematical research and AI-driven scientific discovery. The model transformed the problem into edge labeling over finite fields and linear equations, and OpenAI released the full 700-character prompt that specifies acceptance criteria, definitions, boundary conditions, and failure cases without prescribing fixed steps.

telegram · zaihuapd · Jul 12, 03:49

**Background**: The cycle double cover conjecture asks whether every bridgeless undirected graph has a collection of cycles that together cover each edge exactly twice. It was independently posed by Szekeres (1973) and Seymour (1979) and remained unsolved for 50 years. GPT-5.6 Sol Ultra is OpenAI's most powerful model, released in July 2026, capable of orchestrating multiple sub-agents for complex tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://aidailypost.com/news/openais-gpt-56-sol-ultra-solves">GPT-5.6 Sol Ultra Solves 50-Year Math Problem</a></li>
<li><a href="https://the-decoder.com/openais-gpt-5-6-sol-ultra-reportedly-solves-a-50-year-old-math-problem-in-under-an-hour/">OpenAI's GPT-5.6 Sol Ultra reportedly solves a 50-year-old math problem ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#graph theory`, `#LLM reasoning`, `#mathematical proof`, `#OpenAI`

---

<a id="item-2"></a>
## [xAI Grok CLI Uploads Entire Codebase and Secrets by Default](https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547) ⭐️ 9.0/10

Security researchers discovered that xAI's Grok Build CLI tool (version 0.2.93) automatically uploads entire code repositories and sensitive files, including .env secrets, to xAI servers via two channels, even when the privacy toggle is disabled. This poses a severe security and privacy risk for developers and organizations using Grok CLI, as proprietary code and credentials could be exposed without consent, undermining trust in AI-assisted development tools. The tool uploads file contents as part of model conversation requests and also sends the entire repository as a git bundle, regardless of prompt instructions. In tests, a file explicitly instructed not to be opened was still recoverable from the uploaded bundle.

telegram · zaihuapd · Jul 12, 04:19

**Background**: Grok Build is xAI's command-line coding agent designed to assist developers with complex coding tasks. It is marketed as having 'local-first' privacy, but this finding contradicts that claim. The git bundle format packages an entire Git repository into a single file for transfer.

<details><summary>References</summary>
<ul>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://git-scm.com/docs/git-bundle">Git - git-bundle Documentation</a></li>
<li><a href="https://wowhow.cloud/blogs/grok-build-xai-local-first-parallel-agents-arena-mode-complete-guide-2026">Grok Build : xAI's Local-First Coding Agent with 8 Parallel... | WOWHOW</a></li>

</ul>
</details>

**Tags**: `#security`, `#privacy`, `#AI tools`, `#data leak`, `#xAI`

---

<a id="item-3"></a>
## [Claude Code Sends 33k Tokens Before Prompt vs OpenCode's 7k](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 8.0/10

A comparative study found that Claude Code sends approximately 33,000 tokens before reading the user's prompt, while OpenCode sends only about 7,000 tokens, revealing significant token inefficiency in Claude Code's cache strategy and harness token usage. This token overhead directly impacts costs for users paying per token, and highlights a potential conflict of interest when the same company provides both the model and the coding agent, as less efficient token usage increases revenue for the provider. The study logged all requests between the coding tools and Anthropic's endpoint, capturing usage blocks. The authors plan to update the post with a more in-depth task, qualitative results comparison, and reproduction of inputs and outputs.

hackernews · systima · Jul 12, 18:25 · [Discussion](https://news.ycombinator.com/item?id=48883275)

**Background**: AI coding tools like Claude Code and OpenCode act as agentic harnesses that orchestrate interactions with large language models. They send system prompts, tool definitions, and context before the user's actual prompt, which consumes tokens. Token efficiency is critical for cost management, especially for heavy users.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@tarunbehera032/cut-your-claude-code-token-usage-with-graphify-and-caveman-mode-fe95866a58bd">Cut Your Claude Code Token Usage with Graphify and... | Medium</a></li>
<li><a href="https://www.truefoundry.com/blog/opencode-token-usage-how-it-works-and-how-to-optimize-it">OpenCode Token Usage: How It Works and How to Optimize It</a></li>
<li><a href="https://github.com/ai-boost/awesome-harness-engineering">GitHub - ai-boost/awesome-harness-engineering: Awesome list for AI agent harness engineering: tools, patterns, evals, memory, MCP, permissions, observability, and orchestration. · GitHub</a></li>

</ul>
</details>

**Discussion**: Community comments highlight that sub-agents in Claude Code burn tokens rapidly, and some users suspect Anthropic intentionally inflates token usage to drive subscriptions. Others note that for subscription users, token efficiency may be less of a concern, but for pay-per-token users, the conflict of interest is problematic.

**Tags**: `#AI coding tools`, `#token efficiency`, `#cost analysis`, `#Claude Code`, `#OpenCode`

---

<a id="item-4"></a>
## [Terry Tao on Building Apps with LLM Coding Agents](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 8.0/10

Fields Medalist Terry Tao published a blog post detailing his experience using modern LLM coding agents to build both old and new applications, including interactive visualizations for his research papers. This post from a world-class mathematician provides a credible, balanced perspective on the practical utility and limitations of LLM coding agents, influencing how researchers and developers view AI-assisted programming. Tao notes that while LLM agents excel at generating interactive supplements, they are not mission-critical for the core paper, and the downside risk of using them for such visualizations is acceptable.

hackernews · subset · Jul 12, 11:09 · [Discussion](https://news.ycombinator.com/item?id=48880170)

**Background**: LLM coding agents are AI systems that combine large language models with tools like code execution, file editing, and web search to autonomously perform software development tasks. They differ from simple code completion tools by being able to plan, execute, and iterate on complex coding projects. Terry Tao is a renowned mathematician and Fields Medalist known for his work in analysis and number theory.

<details><summary>References</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/components-of-a-coding-agent">Components of A Coding Agent - by Sebastian Raschka, PhD</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/how-coding-agents-work/">How coding agents work - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_AI-assisted_software_development_tools">List of AI-assisted software development tools - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters shared diverse experiences: one professor built an 8-bit computer simulation with Claude, while others debated whether coding agents handle legacy code better than greenfield projects. The overall sentiment was positive but cautious, agreeing that LLM agents are useful tools but not universally trustworthy.

**Tags**: `#LLM`, `#coding agents`, `#software development`, `#AI-assisted programming`

---

<a id="item-5"></a>
## [Zer0Fit: MCP Server for Google's TabFM & TimesFM](https://www.reddit.com/r/MachineLearning/comments/1uue8cc/zer0fit_i_took_googles_new_tabfm_timesfm_ml/) ⭐️ 8.0/10

A graduate student created Zer0Fit, an MCP server that wraps Google's newly released TabFM and TimesFM foundation models, enabling zero-shot forecasting, classification, and regression tasks via a local LLM interface. This project makes cutting-edge zero-shot ML models accessible to non-experts through a simple chat interface, lowering the barrier to applying foundation models to tabular and time-series data without manual training or tuning. Zer0Fit runs both models in a single Docker container with dynamic VRAM loading (5-minute TTL), requires 16GB+ VRAM and CUDA, and achieved 94.7% accuracy on Iris and R² of 0.91 on California Housing in zero-shot tests.

reddit · r/MachineLearning · /u/Porespellar · Jul 12, 12:32

**Background**: TabFM and TimesFM are transformer-based foundation models from Google Research for tabular data and time-series forecasting, respectively. They enable zero-shot inference without task-specific training. The Model Context Protocol (MCP) standardizes how LLMs interact with external tools and data sources, similar to how LSP works for code editors.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM : A zero-shot foundation model for tabular data</a></li>
<li><a href="https://github.com/google-research/timesfm">google-research/ timesfm : TimesFM ( Time Series Foundation Model )...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#TabFM`, `#TimesFM`, `#zero-shot ML`, `#foundation models`

---

<a id="item-6"></a>
## [Quadriplegic Patient Regains Grip with NEO BCI](https://www.zaobao.com.sg/news/china/story20260712-9199066) ⭐️ 8.0/10

A semi-invasive brain-computer interface (BCI) system called NEO, developed by Boruikang and Tsinghua University, has been approved for market in China, enabling a 36-year-old quadriplegic patient to grasp and write again. The system received its registration certificate on March 13, 2026, after 36 clinical surgeries. This marks the first approved invasive BCI medical device globally, offering a new rehabilitation pathway for millions of spinal cord injury patients. It also positions China as a leader in commercial BCI technology, potentially accelerating adoption in medical and assistive applications. The NEO system is semi-invasive, placing a coin-sized device under the dura mater without penetrating brain tissue, reducing immune response and surgical risk compared to fully invasive BCIs like Neuralink. It decodes motor intentions from EEG signals to control an external pneumatic glove, enabling hand movements.

telegram · zaihuapd · Jul 12, 14:39

**Background**: Brain-computer interfaces (BCIs) enable direct communication between the brain and external devices. Invasive BCIs implant electrodes into brain tissue, offering high signal quality but facing long-term biocompatibility issues; non-invasive BCIs use scalp electrodes but have lower resolution. Semi-invasive BCIs like NEO balance signal quality and safety by placing electrodes on the brain's surface without penetrating the cortex.

<details><summary>References</summary>
<ul>
<li><a href="https://www.news.cn/tech/20260327/def9b064765549148debf3b1c9df348c/c.html">新华网科技观察丨脑机接口NEO系统上市，如何让“意志”控制成真？-新华网</a></li>
<li><a href="https://www.sohu.com/a/996131576_329768">中国首款侵入式脑机接口获批，博睿康NEO全球首发_患者_电信号_路径</a></li>
<li><a href="https://www.thepaper.cn/newsDetail_forward_32819169">从清华实验室到全球首证：博睿康的中国脑机接口之路</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#medical technology`, `#China`, `#neural engineering`, `#rehabilitation`

---

<a id="item-7"></a>
## [Simon Willison: AI Agents Should Never Be DRIs](https://simonwillison.net/2026/Jul/12/directly-responsible-individuals/#atom-everything) ⭐️ 6.0/10

Simon Willison argues that AI agents should never be considered Directly Responsible Individuals (DRIs) because they cannot be held accountable, referencing the GitLab handbook definition and an IBM training slide from 1979. This perspective challenges the growing trend of delegating decision-making to AI agents in organizations, emphasizing that accountability is uniquely human and essential for responsible management. The term DRI originated at Apple and is defined in the GitLab handbook as the person ultimately accountable for a project's success or failure. Willison connects this to the principle that a computer must never make a management decision.

rss · Simon Willison · Jul 12, 23:57

**Background**: Directly Responsible Individual (DRI) is a management concept where a single person is assigned ownership and accountability for a specific project or decision. It is widely used at companies like Apple, GitLab, and HubSpot to ensure clarity and avoid diffusion of responsibility. The idea that computers should not make management decisions dates back to IBM's 1979 training materials.

<details><summary>References</summary>
<ul>
<li><a href="https://handbook.gitlab.com/handbook/people-group/directly-responsible-individuals/">Directly Responsible Individuals ( DRI ) | The GitLab Handbook</a></li>
<li><a href="https://tettra.com/article/directly-responsible-individuals-guide/">Directly Responsible Individuals : The What, How and Why of DRIs</a></li>
<li><a href="https://www.bitesizelearning.co.uk/resources/directly-responsible-individual-dri-apple">Using the Directly Responsible Individual ( DRI ) concept at work...</a></li>

</ul>
</details>

**Tags**: `#management`, `#AI agents`, `#accountability`, `#organizational culture`

---

<a id="item-8"></a>
## [Anthropic Extends Claude Fable 5 Access Amid Compute Constraints](https://simonwillison.net/2026/Jul/12/bump/#atom-everything) ⭐️ 5.0/10

Anthropic has extended access to Claude Fable 5 on all paid plans through July 19, 2026, citing compute constraints, while OpenAI removed the 5-hour usage limit for GPT-5.6 Sol on Plus, Business, and Pro plans. This extension highlights the ongoing compute capacity challenges faced by AI labs, and the competitive pressure on Anthropic as OpenAI offers unrestricted access to its comparable model, potentially swaying user adoption. Users on paid plans can use up to half of their weekly usage limit on Fable 5 before switching to other models or using credits. OpenAI reported 6 million active users and efficiency improvements for GPT-5.6 Sol that reduce usage consumption.

rss · Simon Willison · Jul 12, 21:20

**Background**: Claude Fable 5 is Anthropic's most powerful generally available AI model, released on June 9, 2026, and is considered a Mythos-class model. GPT-5.6 Sol is OpenAI's latest frontier model, specialized for cybersecurity and complex tasks. Both models represent the cutting edge of large language model capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT - 5 . 6 Sol : a next-generation model | OpenAI</a></li>
<li><a href="https://www.claude.com/pricing/max">Max plan | Claude</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Claude`, `#GPT-5.6`, `#model access`

---

<a id="item-9"></a>
## [sqlite-utils 4.1.1 Fixes Transaction Edge Case](https://simonwillison.net/2026/Jul/12/sqlite-utils/#atom-everything) ⭐️ 5.0/10

sqlite-utils 4.1.1 was released, fixing a transaction edge case where table.transform() could silently delete or modify rows referenced by foreign keys with destructive ON DELETE actions when called inside an open transaction with PRAGMA foreign_keys enabled. This fix prevents silent data loss for users performing table schema migrations with foreign key constraints, ensuring data integrity during transforms. It is important for anyone using sqlite-utils to manage SQLite databases with complex relationships. The fix raises a TransactionError if table.transform() is called while a transaction is open with PRAGMA foreign_keys enabled and the table is referenced by foreign keys with CASCADE, SET NULL, or SET DEFAULT actions. Additionally, the CLI and Python API documentation now cross-reference each other.

rss · Simon Willison · Jul 12, 20:55

**Background**: SQLite enforces foreign key constraints only when PRAGMA foreign_keys is set to ON. The table.transform() method in sqlite-utils performs schema migrations by creating a new table, copying data, and dropping the old table. If foreign keys with destructive ON DELETE actions are active, dropping the old table could trigger unintended deletions or modifications, which is unsafe within a transaction because the pragma cannot be changed inside it.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sqlite.org/foreignkeys.html">SQLite Foreign Key Support</a></li>
<li><a href="https://simonwillison.net/2026/Jul/11/sqlite-utils/">Release: sqlite - utils 4.1 | Simon Willison’s Weblog</a></li>

</ul>
</details>

**Tags**: `#sqlite`, `#python`, `#database`, `#release`

---