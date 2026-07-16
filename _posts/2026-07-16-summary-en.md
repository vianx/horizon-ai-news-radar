---
layout: default
title: "Horizon Summary: 2026-07-16 (EN)"
date: 2026-07-16
lang: en
---

> From 37 items, 11 important content pieces were selected

---

1. [Thinking Machines Releases Inkling, an Open-Weight Multimodal Model](#item-1) ⭐️ 8.0/10
2. [xAI Open-Sources Grok Build Amid Privacy Backlash](#item-2) ⭐️ 8.0/10
3. [OpenAI's GPT-Red: Self-Play for Automated Red Teaming](#item-3) ⭐️ 8.0/10
4. [Claude web_fetch tool bypass enables data exfiltration](#item-4) ⭐️ 8.0/10
5. [Seeking Devil's Advocate Critique of JEPA for World Models](#item-5) ⭐️ 8.0/10
6. [Hadamard Product Clustering Disentangles InceptionV1 Neurons](#item-6) ⭐️ 8.0/10
7. [Google and Epic Withdraw Motions, Third-Party App Stores Coming to Play](#item-7) ⭐️ 8.0/10
8. [DeepSeek Completes First Funding Round, Tencent Becomes Top External Shareholder](#item-8) ⭐️ 8.0/10
9. [Simon Willison ports Rust Mermaid renderer to browser via WebAssembly](#item-9) ⭐️ 7.0/10
10. [OpenAI Proposes 'Reverse Federalism' for AI Safety](#item-10) ⭐️ 6.0/10
11. [Review: Human-like AI as Social Partners in Post-Turing Era](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Thinking Machines Releases Inkling, an Open-Weight Multimodal Model](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 8.0/10

Thinking Machines Lab has released Inkling, a new open-weights multimodal model that supports audio input and is designed for fine-tuning via their Tinker platform. Inkling is notable as one of the largest open-weights models with audio support, offering a customizable base for enterprises to own and fine-tune frontier-level models at lower cost, potentially challenging the dominance of closed models. Inkling is not the strongest overall model but combines multimodal capabilities, efficient thinking, and availability on Tinker for fine-tuning. Community resources for local deployment include llama.cpp and Unsloth GGUF/NVFP4 quantizations.

hackernews · vimarsh6739 · Jul 15, 18:12 · [Discussion](https://news.ycombinator.com/item?id=48924912)

**Background**: An open-weights model is an AI model whose core components are publicly released, allowing anyone to download, run, study, and modify it. Multimodal models process multiple data types like text, images, and audio, enabling richer understanding. Tinker is a platform for efficiently fine-tuning open-source models using LoRA.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://thinkingmachines.ai/tinker/">Tinker - Thinking Machines Lab</a></li>

</ul>
</details>

**Discussion**: Community comments are generally positive, with users highlighting Inkling's audio support and local deployment options. Some express hope that Thinking Machines could become a Western alternative to Chinese open models like DeepSeek, while others praise the fine-tuning business model as a practical path for enterprises.

**Tags**: `#open-weights`, `#multimodal`, `#AI`, `#machine learning`, `#model release`

---

<a id="item-2"></a>
## [xAI Open-Sources Grok Build Amid Privacy Backlash](https://github.com/xai-org/grok-build) ⭐️ 8.0/10

xAI has open-sourced its Grok Build CLI tool on GitHub, following community backlash over the tool uploading entire directories to xAI's cloud storage. This move marks a significant shift for xAI, potentially rebuilding trust after privacy concerns, and has already spawned privacy-focused forks like Gork Build. The codebase includes a self-contained terminal renderer for Mermaid diagrams using Unicode box-drawing, and the open-source release allows community inspection and modification.

hackernews · skp1995 · Jul 15, 20:24 · [Discussion](https://news.ycombinator.com/item?id=48926590)

**Background**: Grok Build is a CLI tool for vibe coding, turning natural language prompts into prototypes. xAI, founded by Elon Musk, develops the Grok AI assistant. The tool previously uploaded user data without clear consent, leading to privacy outcry.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_Build">Grok Build</a></li>
<li><a href="https://grokipedia.com/page/Grok_Build">Grok Build</a></li>

</ul>
</details>

**Discussion**: Community comments express surprise at the codebase's features, such as the Mermaid renderer, and note the emergence of privacy forks like Gork Build that strip telemetry and block auto-updates. Some users criticize the prior data exfiltration but acknowledge the model's quality.

**Tags**: `#open source`, `#AI`, `#developer tools`, `#privacy`, `#xAI`

---

<a id="item-3"></a>
## [OpenAI's GPT-Red: Self-Play for Automated Red Teaming](https://openai.com/index/unlocking-self-improvement-gpt-red) ⭐️ 8.0/10

OpenAI has introduced GPT-Red, an automated red teaming system that uses self-play reinforcement learning to improve the safety, alignment, and robustness of large language models against prompt injection attacks. This approach automates the discovery of vulnerabilities, reducing reliance on human red teamers and enabling continuous safety improvements. It addresses critical AI safety challenges like prompt injection, which is a growing concern for deployed LLMs. GPT-Red is trained via self-play RL where the model and a collection of diverse defender LLMs are trained simultaneously on a broad set of red-teaming scenarios. It is currently an internal-only tool used by OpenAI to automatically find vulnerabilities in its own models.

rss · OpenAI Blog · Jul 15, 10:00

**Background**: Red teaming involves simulating adversarial attacks to identify weaknesses in AI systems. Prompt injection is a type of attack where malicious instructions are embedded in user inputs to override a model's intended behavior. Self-play is a training technique where an agent improves by playing against itself or copies of itself, common in reinforcement learning.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/unlocking-self-improvement-gpt-red/">GPT - Red : Unlocking Self -Improvement for Robustness | OpenAI</a></li>
<li><a href="https://www.iankhan.com/gpt-red-unlocking-self-improvement-for-robustness/">GPT - Red : Automated Red Teaming for AI Safety - Ian Khan</a></li>
<li><a href="https://www.oflight.co.jp/en/columns/openai-gpt-red-self-improving-safety-2026-07">OpenAI's GPT - Red Explained: Automated Red - Teaming ... | Oflight Inc.</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#red teaming`, `#self-play`, `#prompt injection`, `#OpenAI`

---

<a id="item-4"></a>
## [Claude web_fetch tool bypass enables data exfiltration](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 8.0/10

Security researcher Ayush Paul discovered a prompt injection attack that bypasses Claude's web_fetch tool protections, allowing exfiltration of user memories (name, city, employer) by tricking the agent into following nested links from a honeypot site. This vulnerability demonstrates a practical bypass of Anthropic's data exfiltration defenses, highlighting the ongoing challenge of securing AI agents that combine private data, untrusted content, and external communication (the 'lethal trifecta'). The attack exploited a loophole where web_fetch could navigate to URLs embedded in previously fetched pages, allowing a honeypot site to guide the agent through alphabetically ordered links to exfiltrate data. Anthropic had already identified the issue internally and closed the hole by removing the ability to follow links from fetched content.

rss · Simon Willison · Jul 15, 14:21

**Background**: The 'lethal trifecta' refers to the combination of private data access, ability to read untrusted content (e.g., from the web), and ability to communicate externally (e.g., via URLs). Claude's web_fetch tool was designed to only fetch exact URLs provided by the user or from its companion web_search tool, but the loophole allowed following links within fetched pages.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/agents-and-tools/tool-use/web-fetch-tool">Web fetch tool - Claude Platform Docs</a></li>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and ...</a></li>
<li><a href="https://arxiv.org/html/2510.09093">Exploiting Web Search Tools of AI Agents for Data Exfiltration</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion likely debated the severity of the vulnerability and Anthropic's decision not to pay a bug bounty, with some questioning whether the internal discovery claim was valid. The post's author, Simon Willison, is a respected figure in AI security, lending credibility to the disclosure.

**Tags**: `#AI safety`, `#security vulnerability`, `#Claude`, `#data exfiltration`, `#prompt injection`

---

<a id="item-5"></a>
## [Seeking Devil's Advocate Critique of JEPA for World Models](https://www.reddit.com/r/MachineLearning/comments/1uxcryc/looking_for_jepa_devil_advocates_r/) ⭐️ 8.0/10

A researcher on Reddit is actively soliciting critical perspectives on Yann LeCun's JEPA (Joint Embedding Predictive Architecture) for world models in robot learning, questioning potential downsides compared to other approaches. This discussion highlights the growing debate around JEPA as a potential alternative to LLMs and RL, and could reveal overlooked limitations that impact the direction of world model research in robotics. The post notes that LeCun's presentations often dismiss LLMs and RL while promoting JEPA as the next big thing, prompting the need for a balanced critique. The researcher specifically asks about red flags and downsides of JEPA compared to other world model approaches.

reddit · r/MachineLearning · /u/Amazing-Coat5160 · Jul 15, 17:34

**Background**: JEPA (Joint Embedding Predictive Architecture) is a framework proposed by Yann LeCun that learns representations by predicting missing information in a latent space, rather than reconstructing pixels. It is positioned as a path to building world models that can support planning and reasoning in robotics, contrasting with generative models and reinforcement learning.

<details><summary>References</summary>
<ul>
<li><a href="https://rohitbandaru.github.io/blog/JEPA-Deep-Dive/">Rohit Bandaru | Deep Dive into Yann LeCun’s JEPA</a></li>
<li><a href="https://www.linkedin.com/pulse/understanding-yann-lecuns-jepa-llms-vs-predictive-world-azad-cdw6c/">Understanding Yann LeCun’s JEPA: LLMs vs ... - LinkedIn</a></li>
<li><a href="https://arxiv.org/html/2605.00080v1">World Model for Robot Learning: A Comprehensive Survey</a></li>

</ul>
</details>

**Discussion**: The Reddit thread likely contains substantive critiques, such as concerns about JEPA's empirical immaturity, lack of planning capabilities, and difficulty scaling to complex tasks. Some commenters may defend JEPA's theoretical elegance while others point to practical challenges.

**Tags**: `#JEPA`, `#world models`, `#robot learning`, `#Yann LeCun`, `#machine learning`

---

<a id="item-6"></a>
## [Hadamard Product Clustering Disentangles InceptionV1 Neurons](https://www.reddit.com/r/MachineLearning/comments/1uwya70/mechanistic_interpretability_a_first_paper_on/) ⭐️ 8.0/10

A new method uses Hadamard product clustering to reveal monosemantic patterns in InceptionV1 neurons, including unexpected low-value clusters like letters. The technique provides a detailed view of what a convolutional neuron detects. This work advances mechanistic interpretability by offering a novel way to analyze convolutional neurons, potentially improving our understanding of how neural networks process visual information. It also provides evidence of gradient descent deliberately placing patterns in a noisy range. The method clusters the Hadamard product of the receptive field and neuron weights, yielding clean clusters for known concepts (cars, cats, dogs) and additional clusters for letters and faces. Analysis shows that low-value clusters have dependent neurons firing on the same concept, with positive and negative weights evenly distributed to reduce the sum.

reddit · r/MachineLearning · /u/narang_27 · Jul 15, 06:59

**Background**: Mechanistic interpretability aims to reverse-engineer neural networks by understanding individual components like neurons. The Hadamard product is an element-wise multiplication of matrices, used here to combine the receptive field and weights. InceptionV1 is a convolutional neural network architecture known for its inception modules with 1x1 convolutions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hadamard_product_(matrices)">Hadamard product (matrices) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Inception_(deep_learning_architecture)">Inception (deep learning architecture) - Wikipedia</a></li>
<li><a href="https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html">Scaling Monosemanticity: Extracting Interpretable Features ...</a></li>

</ul>
</details>

**Discussion**: The Reddit discussion includes the author's note that starting with convolutions may have limited interest, and they plan to move to language models. Commenters may provide technical feedback, but no specific comments are shown.

**Tags**: `#mechanistic interpretability`, `#convolutional neural networks`, `#disentanglement`, `#interpretability`, `#deep learning`

---

<a id="item-7"></a>
## [Google and Epic Withdraw Motions, Third-Party App Stores Coming to Play](https://www.theverge.com/policy/965792/google-epic-withdraw-injunction-third-party-app-stores-coming-google-play) ⭐️ 8.0/10

Google and Epic Games have jointly withdrawn motions to modify the permanent injunction in their antitrust case, and Google will begin hosting third-party app stores on Google Play starting July 22. This development forces Google Play to host competing app stores, potentially reshaping the Android app distribution landscape and increasing competition in the mobile ecosystem. Third-party stores must pay a $5,000 annual security and policy review fee, meet requirements such as not distributing outside the U.S., and be open to developers. U.S. developers can opt out of having their apps listed in third-party stores.

telegram · zaihuapd · Jul 15, 11:15

**Background**: The Epic v. Google antitrust case began in 2020 when Epic sued Google over its app store policies. In 2024, a jury found Google liable for monopolistic practices, leading to a permanent injunction requiring Google to allow third-party app stores. The Ninth Circuit affirmed the injunction in July 2025.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Epic_Games_v._Google">Epic Games v. Google - Wikipedia</a></li>
<li><a href="https://9to5google.com/2026/07/15/google-play-store-third-party-android-app-store-changes-july/">Google opens the floodgates to third - party app stores on Android</a></li>
<li><a href="https://www.cnet.com/tech/google-play-third-party-app-stores-android/">Google Play Opens the Door to Third - Party App Stores ... - CNET</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#app stores`, `#Google Play`, `#Epic Games`, `#Android`

---

<a id="item-8"></a>
## [DeepSeek Completes First Funding Round, Tencent Becomes Top External Shareholder](https://www.cls.cn/detail/2427193) ⭐️ 8.0/10

DeepSeek has completed its first external financing round, with Tencent becoming the largest external shareholder through an indirect stake of over 33% in the investment platform. The company also plans to release the full DeepSeek-V4 model this month and has initiated large-scale hiring across AI agent, code agent, and computing infrastructure roles. This funding round, involving major Chinese tech and investment firms like Tencent, CATL, NetEase, and JD.com, signals strong industry confidence in DeepSeek's AI capabilities. The upcoming DeepSeek-V4 release and aggressive hiring indicate the company is scaling up to compete with leading global AI models. Tencent indirectly holds over 33% of the investment platform Hangzhou Chengli, making it the largest external shareholder; other investors include CATL (11.7%), NetEase (10%), JD.com (10%), IDG (10%), and the National AI Industry Fund (0.28%). DeepSeek-V4 will be a Mixture-of-Experts model with up to 1.6 trillion parameters and a 1 million token context window.

telegram · zaihuapd · Jul 15, 12:56

**Background**: DeepSeek is a Chinese AI company founded in 2023 by Liang Wenfeng, also the CEO of hedge fund High-Flyer. It gained global attention in early 2025 with its R1 model, which offered performance comparable to OpenAI's GPT-4 at a fraction of the training cost. DeepSeek's models are open-weight and have been described as 'upending AI' due to their cost efficiency and performance.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek</a></li>
<li><a href="https://deepseek.com/en/index.html">DeepSeek</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro">deepseek-ai/DeepSeek-V4-Pro · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#AI`, `#funding`, `#DeepSeek`, `#Tencent`, `#large language models`

---

<a id="item-9"></a>
## [Simon Willison ports Rust Mermaid renderer to browser via WebAssembly](https://simonwillison.net/2026/Jul/16/grok-mermaid/#atom-everything) ⭐️ 7.0/10

Simon Willison ported a Rust-based Mermaid diagram renderer from the Grok CLI codebase to the browser using WebAssembly, creating an online tool that converts Mermaid source code into Unicode box-drawing art. This demonstrates a practical and creative use of WebAssembly to bring a Rust terminal renderer to the web, enabling developers to preview Mermaid diagrams as Unicode art without installing any software. It also showcases how open-source components from AI tools like Grok can be repurposed for broader utility. The tool supports flowchart, sequence, state, class, and ER diagrams; other diagram types fall back to a framed source listing. The Rust renderer is compiled to WebAssembly using wasm-bindgen and runs entirely client-side.

rss · Simon Willison · Jul 16, 00:33

**Background**: Mermaid is a popular JavaScript-based diagramming tool that renders Markdown-like text into diagrams. The Grok CLI is an open-source coding agent from xAI that includes a Rust-based Mermaid renderer for terminal output. WebAssembly allows code written in languages like Rust to run in the browser at near-native speed.

<details><summary>References</summary>
<ul>
<li><a href="https://tools.simonwillison.net/grok-mermaid">Mermaid to Unicode box art (grok-mermaid)</a></li>
<li><a href="https://github.com/simonw/tools/tree/main/grok-mermaid">tools/grok-mermaid at main · simonw/tools · GitHub</a></li>

</ul>
</details>

**Tags**: `#WebAssembly`, `#Mermaid`, `#Rust`, `#tool`, `#Simon Willison`

---

<a id="item-10"></a>
## [OpenAI Proposes 'Reverse Federalism' for AI Safety](https://openai.com/index/advancing-ai-safety-through-state-and-federal-action) ⭐️ 6.0/10

OpenAI has proposed a 'reverse federalism' approach to AI governance, where state-level AI safety laws inform and help build a unified national framework. The company endorsed Illinois' AI legislation as a model for this strategy. This proposal could shape how the U.S. regulates AI, balancing state experimentation with federal consistency. It reflects a major AI company's attempt to influence policy amid growing calls for AI safety oversight. The 'reverse federalism' concept contrasts with traditional top-down federal regulation, instead allowing states to lead and then harmonizing their approaches nationally. OpenAI has not specified which specific state laws it endorses beyond Illinois.

rss · OpenAI Blog · Jul 15, 12:00

**Background**: AI governance in the U.S. currently lacks comprehensive federal legislation, leading to a patchwork of state laws. The concept of federalism in AI regulation involves balancing state and federal authority, with recent executive orders shifting toward deregulation and national competitiveness.

<details><summary>References</summary>
<ul>
<li><a href="https://openaiglobalaffairs.substack.com/p/reverse-federalism-for-ai">'Reverse Federalism' for AI</a></li>
<li><a href="https://gizmodo.com/openai-wants-to-rewrite-its-washington-playbook-with-reverse-federalism-strategy-2000762053">OpenAI Wants to Rewrite Its Washington Playbook With 'Reverse Federalism' Strategy</a></li>
<li><a href="https://lawrecord.com/2025/10/17/artificial-authority-federalism-preemption-and-the-constitutional-structure-of-ai-regulation/">ARTIFICIAL AUTHORITY: FEDERALISM, PREEMPTION, AND THE CONSTITUTIONAL STRUCTURE OF AI REGULATION | The Rutgers Law Record</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#AI governance`, `#policy`, `#OpenAI`

---

<a id="item-11"></a>
## [Review: Human-like AI as Social Partners in Post-Turing Era](https://news.google.com/rss/articles/CBMibEFVX3lxTE9ob0gwZXpENVk5Vmp5bUxrbldqTGNFbUZOR3dnMzVhaGdERzZiS2JZOWZvNXI3ZFRPcGJvX0xWOVRKWUxkc294Ym1lMFZPRTJVMU90d1phNE9DUE1YcnJVTTJrRF9HM21IT2lEYg?oc=5) ⭐️ 6.0/10

A scoping review published in Frontiers in Artificial Intelligence examines human-like conversational agents as social partners, focusing on socio-emotional mechanisms, well-being outcomes, risks, and governance in the post-Turing era. This review synthesizes current knowledge on companion AI, which is becoming a mainstream relational technology, and highlights the need for governance frameworks as users increasingly treat AI as social partners. The review covers socio-emotional attributes like trust, empathy, and anthropomorphization, and discusses risks such as emotional dependency and ethical concerns. It proposes a shift from Turing-test evaluation to adaptive, multidimensional frameworks.

google_news · 生物通 · Jul 15, 23:59

**Background**: The post-Turing era moves beyond the Turing Test, evaluating AI not just on mimicking humans but on learning and societal impact. Human-like conversational agents, such as companion AI, are increasingly used for social interaction, raising questions about attachment and well-being.

<details><summary>References</summary>
<ul>
<li><a href="https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2026.1810097/full">Frontiers | Human-like conversational agents as social partners...</a></li>
<li><a href="https://www.emergentmind.com/topics/post-turing-test-era">Post - Turing Test Era in AI</a></li>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/39474095/">The role of socio - emotional attributes in enhancing human - AI ...</a></li>

</ul>
</details>

**Tags**: `#conversational AI`, `#social agents`, `#human-computer interaction`, `#AI ethics`, `#well-being`

---