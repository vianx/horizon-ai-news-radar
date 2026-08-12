---
layout: default
title: "Horizon Summary: 2026-08-12 (EN)"
date: 2026-08-12
lang: en
---

> From 43 items, 11 important content pieces were selected

---

1. [Researchers Steal Hidden Reasoning from LLM APIs](#item-1) ⭐️ 9.0/10
2. [Compression Is Prediction: A Fundamental Equivalence](#item-2) ⭐️ 8.0/10
3. [Mojo 1.0 Released, But Closed-Source Compiler and Python Compatibility Questions Linger](#item-3) ⭐️ 8.0/10
4. [Decoupled Descent: Exact Train-Test Error Tracking via AMP](#item-4) ⭐️ 8.0/10
5. [Nvidia Unveils Nemotron 3.5 Lightning and NeMo Switchyard](#item-5) ⭐️ 7.0/10
6. [Go's Simplicity Makes It Ideal for AI-Assisted Development](#item-6) ⭐️ 7.0/10
7. [OpenAI Daybreak Models Now Available on AWS Bedrock](#item-7) ⭐️ 7.0/10
8. [No Lossless Transformations of Natural-Language Text](#item-8) ⭐️ 7.0/10
9. [ChatGPT Ads Expand to Five More Countries for Free and Go Users](#item-9) ⭐️ 6.0/10
10. [ByteDance CEO Rejects Model Distillation as Shortcut in AI Strategy](#item-10) ⭐️ 6.0/10
11. [TVB Stock Surges on AI Computing Joint Venture with Gaw Capital](#item-11) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Researchers Steal Hidden Reasoning from LLM APIs](https://stolen-thoughts.com/) ⭐️ 9.0/10

Researchers demonstrated a method to extract hidden chain-of-thought reasoning from proprietary LLM APIs by replaying traces into weaker models. The technique recovers the stronger model's reasoning without direct access, as detailed on stolen-thoughts.com. This raises serious concerns about model alignment and intellectual property, as proprietary models' internal reasoning can be exposed. It could impact AI security policies and the competitive advantage of API providers. The attack involves replaying a trace from a frontier model into a weaker sibling model and jailbreaking it to recover the reasoning. The paper notes that API summaries may not preserve distinctions like when a model states an answer before deriving it.

hackernews · quantumgarbage · Aug 11, 13:22 · [Discussion](https://news.ycombinator.com/item?id=49257876)

**Background**: Chain-of-thought (CoT) reasoning is a technique where LLMs generate step-by-step reasoning before answering, improving performance on complex tasks. Proprietary APIs often encrypt or hide these traces to protect intellectual property and alignment. Model extraction attacks typically use observable outputs to train a student model, but this method exploits replay across models to access hidden reasoning.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2505.15634">[2505.15634] Feature Extraction and Steering for Enhanced ... Feature Extraction and Steering for Enhanced Chain-of-Thought ... Think Faster Than Words: Efficient LLM Chain-of-Thought ... Chain-of-Thought Prompting: Step-by-Step Reasoning with LLMs Chain of Thought Prompting Explained (with examples) Stealing Reasoning Traces from Proprietary LLM APIs Thinking to recall: How reasoning unlocks parametric ...</a></li>
<li><a href="https://ai-alert.org/posts/model-extraction-attacks-explained/">Model Extraction Attacks : How Adversaries Steal AI via the API</a></li>
<li><a href="https://arxiv.org/pdf/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>

</ul>
</details>

**Discussion**: Commenters debated the ethics of 'stealing' reasoning, with some arguing it's fair use since users pay for tokens. Others noted alternative methods, such as using a 'deep_think' tool to bypass thinking restrictions, and shared experiences with similar extraction techniques.

**Tags**: `#LLM security`, `#chain-of-thought`, `#model extraction`, `#AI alignment`, `#proprietary APIs`

---

<a id="item-2"></a>
## [Compression Is Prediction: A Fundamental Equivalence](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

The ngrok blog published an article arguing that compression and prediction are fundamentally equivalent, drawing on information theory and machine learning principles. The post has gained significant traction with 199 points and 92 comments on Hacker News. This perspective unifies two major fields and has deep implications for understanding why large language models work, potentially influencing future AI research and model design. It resonates with the community, sparking discussions about generalization and the nature of intelligence. The article likely explains that a system predicting posterior probabilities can be used for optimal compression via arithmetic coding, and vice versa. Community comments highlight nuances, such as the distinction between compression and prediction when the test distribution differs from training data, and reference related resources like Grant Sanderson's video series.

hackernews · nikolay · Aug 11, 19:49 · [Discussion](https://news.ycombinator.com/item?id=49263497)

**Background**: In information theory, compression reduces data size by exploiting statistical regularities, while prediction estimates future data based on past data. The equivalence arises because both rely on modeling the underlying probability distribution: better prediction leads to better compression, and vice versa. This concept is central to understanding modern machine learning, where models like LLMs are trained to predict next tokens, effectively compressing training data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Data_compression">Data compression - Wikipedia</a></li>
<li><a href="https://dev.to/trismegistus/compression-is-prediction-and-it-explains-why-llms-actually-work-209e">Compression Is Prediction — and It Explains Why LLMs Actually ...</a></li>
<li><a href="https://medium.com/@EleventhHourEnthusiast/compression-and-prediction-why-language-models-are-really-compression-engines-317c97babe04">Compression and Prediction. Why Language Models Are Really Compression Engines | by Eleventh Hour Enthusiast | Medium</a></li>

</ul>
</details>

**Discussion**: Community comments generally agree with the core idea, with some pointing to academic courses and videos that explore the same theme. However, a notable comment by ssivark argues that compression is only functionally equivalent to prediction when the data distribution exactly represents all future problems, emphasizing the importance of generalization. Others humorously note ngrok's blog quality, and one comment extends the analogy to evolution as compression.

**Tags**: `#compression`, `#prediction`, `#information theory`, `#machine learning`, `#AI`

---

<a id="item-3"></a>
## [Mojo 1.0 Released, But Closed-Source Compiler and Python Compatibility Questions Linger](https://www.modular.com/blog/modular-26-5-mojo-1-0-is-here) ⭐️ 8.0/10

Modular announced the release of Mojo 1.0, marking a major milestone for the Python-superset language designed for high-performance AI applications. The release includes a fully open-sourced standard library, with plans to open-source the compiler and toolchain in 2026. Mojo 1.0 is significant because it aims to combine Python's ease of use with C-like performance, potentially impacting AI and systems programming. However, the closed-source compiler and uncertainty about full Python compatibility could affect its adoption and community trust. The Mojo standard library is fully open-source on GitHub, but the compiler remains closed-source until 2026. The roadmap indicates that Mojo may or may not become a full superset of Python, and the current Python interoperability relies on the CPython runtime for calling Python from Mojo.

hackernews · dayanruben · Aug 11, 16:56 · [Discussion](https://news.ycombinator.com/item?id=49261128)

**Background**: Mojo is a programming language created by Modular Inc., founded by Chris Lattner (creator of Swift and LLVM) and Tim Davis. It aims to bridge the gap between Python's ease of use and the performance needed for AI applications. The language uses Pythonic syntax and supports calling Python modules, but its full compatibility with Python is still evolving.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_(programming_language)">Mojo (programming language) - Wikipedia</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>
<li><a href="https://mojolang.org/docs/manual/python/">Python interoperability | Mojo - Modular</a></li>

</ul>
</details>

**Discussion**: Community comments express mixed feelings: some question the value of a closed-source compiler, while others note the lack of a clear overview of the language's purpose. There is also concern about the delay in open-sourcing the compiler and the potential walking back of the Python superset goal.

**Tags**: `#programming-languages`, `#mojo`, `#compiler`, `#python`, `#performance`

---

<a id="item-4"></a>
## [Decoupled Descent: Exact Train-Test Error Tracking via AMP](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

The paper introduces Decoupled Descent (DD), a novel training method that uses Approximate Message Passing (AMP) Onsager corrections to enforce exact train-test error tracking in neural networks. This ensures that the training error asymptotically equals the test error at each parameter iterate, as demonstrated on a stylized Gaussian mixture model. This work addresses the fundamental generalization gap in neural network training, where training error can drop to zero while test error stagnates or worsens. By providing a theoretical guarantee of train-test error alignment, it opens new avenues for optimal stopping and hyperparameter tuning, potentially improving model reliability and efficiency. The method is based on full-batch gradient descent on a stylized Gaussian mixture model, where data reuse bias is identified as the cause of the generalization gap. The paper is theoretical and uses high-dimensional statistical theory, specifically AMP, to derive the algorithm; a PyTorch-compatible package is planned for future release.

reddit · r/MachineLearning · /u/mlovik1 · Aug 11, 21:06

**Background**: Approximate Message Passing (AMP) is an iterative algorithm from high-dimensional statistics that uses Onsager corrections to account for self-interference, enabling accurate inference in linear inverse problems. In machine learning, AMP-inspired techniques have been used to construct deep networks with improved accuracy and efficiency. The generalization gap refers to the discrepancy between training and test performance, often caused by overfitting to training data.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.27883v1">Decoupled Descent : Exact Test Error Tracking Via Approximate...</a></li>
<li><a href="https://www.emergentmind.com/topics/onsager-correction-in-goamp">Onsager Correction in GOAMP - emergentmind.com</a></li>
<li><a href="https://arxiv.org/pdf/1612.01183">AMP-Inspired Deep Networks for Sparse Linear Inverse Problems</a></li>

</ul>
</details>

**Discussion**: The author actively seeks community feedback and suggestions for future features, indicating an open and collaborative approach. The discussion likely focuses on the theoretical contributions and potential practical applications, with some skepticism about scalability to large models.

**Tags**: `#machine learning`, `#optimization`, `#approximate message passing`, `#generalization`, `#theory`

---

<a id="item-5"></a>
## [Nvidia Unveils Nemotron 3.5 Lightning and NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 7.0/10

Nvidia has released the Nemotron 3.5 Lightning models, a 30B-parameter Mixture-of-Experts (MoE) model with 3B active parameters, and NeMo Switchyard, an open-source model routing library. These tools are designed to enhance efficiency and intelligence in agentic AI workflows. This announcement signals a shift toward smaller, more efficient models for agentic AI, potentially reducing costs and latency while maintaining high performance. The open-source routing library could enable more flexible and cost-effective deployment of AI systems across various providers. Nemotron 3.5 Lightning uses a hybrid architecture with interleaved Mamba-2 and MoE layers, along with selected attention layers, and is available in NVFP4 format. NeMo Switchyard is a Rust-based proxy and library that routes requests across providers, translates between OpenAI and Anthropic APIs, and provides composable routing algorithms.

hackernews · droidjj · Aug 11, 19:35 · [Discussion](https://news.ycombinator.com/item?id=49263340)

**Background**: Agentic AI refers to systems that operate autonomously to complete tasks, often using multiple models in an ensemble. Model routing is a technique that dynamically selects the most appropriate model for each request or step, balancing accuracy, cost, and latency. Nvidia's new offerings aim to streamline this process for developers building always-on agents.

<details><summary>References</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4">nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4 · Hugging Face</a></li>
<li><a href="https://github.com/NVIDIA-NeMo/Switchyard">GitHub - NVIDIA-NeMo/Switchyard · GitHub</a></li>

</ul>
</details>

**Discussion**: Community comments highlight a debate on the trend toward smaller, efficient models, with some believing it will drive structural improvements. Others raise practical concerns about routing, such as prompt caching and session consistency, and question the omission of Qwen models in benchmark comparisons.

**Tags**: `#Nvidia`, `#LLM`, `#AI infrastructure`, `#model routing`, `#open source`

---

<a id="item-6"></a>
## [Go's Simplicity Makes It Ideal for AI-Assisted Development](https://developers.googleblog.com/why-go-is-an-ideal-language-for-ai-assisted-software-engineering/) ⭐️ 7.0/10

Google's blog post argues that Go's simplicity, strong tooling, and clear conventions make it particularly well-suited for AI-assisted software engineering. The post sparked a lively debate on Hacker News, with 218 points and 270 comments. This perspective is significant because AI-assisted development is rapidly transforming software engineering, and the choice of programming language may affect how effectively AI tools can assist developers. If Go indeed offers advantages, it could influence language adoption trends and tooling investments. The article highlights Go's simple syntax, built-in concurrency, robust standard library, and strong tooling (e.g., gofmt, go vet) as factors that reduce ambiguity for AI models. However, critics argue that the argument is biased because it comes from a Go creator, and some prefer languages like Rust for their strict compilers that catch errors at compile time.

hackernews · 0xedb · Aug 11, 16:57 · [Discussion](https://news.ycombinator.com/item?id=49261133)

**Background**: Go is a statically typed, compiled programming language designed at Google in 2007 by Robert Griesemer, Rob Pike, and Ken Thompson. It is known for its simplicity, efficiency, and built-in concurrency, making it popular for cloud and backend services. AI-assisted software engineering involves using AI tools, such as large language models, to help developers write, review, and maintain code.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Go_(programming_language)">Go (programming language) - Wikipedia</a></li>
<li><a href="https://go.dev/">The Go Programming Language</a></li>
<li><a href="https://en.wikipedia.org/wiki/AI-assisted_software_development">AI-assisted software development - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments show mixed but substantive viewpoints. Some agree, like a Netflix Go guild lead who reports better AI-generated Go code, while others criticize the argument's bias and suggest Rust's strict compiler is more suitable for AI assistance. There is also debate about Go's concurrency model and the role of tooling in raising code confidence.

**Tags**: `#Go`, `#AI-assisted development`, `#software engineering`, `#programming languages`

---

<a id="item-7"></a>
## [OpenAI Daybreak Models Now Available on AWS Bedrock](https://openai.com/index/daybreak-models-are-now-available-on-aws) ⭐️ 7.0/10

OpenAI's Daybreak cybersecurity models are now available on Amazon Bedrock, enabling enterprise security workflows. This integration brings OpenAI's frontier cyber capabilities to AWS customers. This partnership makes advanced AI-driven cybersecurity tools accessible to a broader enterprise audience, potentially improving vulnerability detection and response. It also strengthens OpenAI's presence in the enterprise cloud market and highlights the growing trend of AI-powered security solutions. The Daybreak models are integrated via Amazon Bedrock, allowing enterprises to use them within existing security and development workflows. The models are designed to help defenders find, validate, and fix vulnerabilities before attackers can exploit them.

rss · OpenAI Blog · Aug 11, 10:00

**Background**: Amazon Bedrock is a managed service that provides access to foundation models from various providers via a unified API. OpenAI's Daybreak initiative combines frontier cyber models, Codex Security, and trusted workflows to assist security teams. This integration allows enterprises to leverage these capabilities without managing underlying infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://openai.com/index/daybreak-securing-the-world/">Daybreak: Tools for securing every organization in the world</a></li>
<li><a href="https://aws.amazon.com/bedrock/">Amazon Bedrock – Build genAI applications and agents at production...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AWS`, `#Cybersecurity`, `#AI`, `#Enterprise`

---

<a id="item-8"></a>
## [No Lossless Transformations of Natural-Language Text](https://simonwillison.net/2026/Aug/11/there-are-no-lossless-transformations-of-natural-language-text/#atom-everything) ⭐️ 7.0/10

Sophie Alpert published an internal policy on acceptable use of AI writing by engineers, arguing that there are no lossless transformations of natural-language text. The policy emphasizes that engineers must stand behind every idea and sentence in their documentation. This policy provides practical guidance for engineers using LLMs, promoting accountability and clarity in AI-assisted writing. It could influence how teams adopt AI tools, encouraging them to avoid blindly accepting AI-generated text and to ensure documents accurately reflect the author's intent. The policy states that every rewrite or rephrase changes the meaning of writing, and if done by an entity without the author's detailed mental model, information will be lost. It also asserts that it is unacceptable to dismiss AI-generated lines with 'Oh sorry, AI wrote that, just ignore it.'

rss · Simon Willison · Aug 11, 23:48

**Background**: Large language models (LLMs) are increasingly used to assist with writing, including technical documentation. However, LLMs do not have access to the author's private thoughts and intentions, so any transformation they perform may introduce subtle changes in meaning. This policy addresses the risk of information loss and emphasizes the importance of human oversight in AI-assisted writing.

<details><summary>References</summary>
<ul>
<li><a href="https://sophiebits.com/2026/06/25/there-are-no-lossless-transformations-of-natural-language-text">There are no lossless transformations of natural-language text – Sophie Alpert</a></li>
<li><a href="https://news.ycombinator.com/item?id=48980425">There are no lossless transformations of natural - language text</a></li>

</ul>
</details>

**Tags**: `#AI`, `#writing`, `#LLM`, `#engineering-practices`, `#documentation`

---

<a id="item-9"></a>
## [ChatGPT Ads Expand to Five More Countries for Free and Go Users](https://openai.com/index/testing-ads-in-chatgpt/) ⭐️ 6.0/10

On August 11, OpenAI announced that ChatGPT ads are now live in the UK, Mexico, Brazil, Japan, and South Korea, expanding the ad test that began in the US in February. The ads are shown only to logged-in adult users on the free and Go tiers, with higher tiers like Plus and Pro remaining ad-free. This expansion signals OpenAI's growing reliance on advertising to sustain free access to ChatGPT, a significant shift in its business model. It could set a precedent for how AI assistants integrate ads while balancing user trust and privacy, affecting millions of users globally. OpenAI states that ads will not affect answers and will be clearly labeled as sponsored. Advertisers only see aggregated data like impressions and clicks, and ads are not shown to minors or near sensitive topics such as health and politics.

telegram · OpenAI Blog · Aug 12, 00:00

**Background**: ChatGPT Go is a lower-cost subscription tier introduced in January 2026, offering expanded access to GPT-5.2 Instant with higher usage limits and longer memory. OpenAI's ad policies emphasize brand safety and user trust, with safeguards to prevent ads in sensitive contexts. The company updated its privacy policy in February 2026 to formalize how ads work and what data advertisers can access.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/testing-ads-in-chatgpt/">Testing ads in ChatGPT - OpenAI</a></li>
<li><a href="https://openai.com/policies/ad-policies/">Ad policies - OpenAI</a></li>
<li><a href="https://help.openai.com/en/articles/11989085-what-is-chatgpt-go">What is ChatGPT Go? - OpenAI Help Center</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#ChatGPT`, `#advertising`, `#business model`, `#privacy`

---

<a id="item-10"></a>
## [ByteDance CEO Rejects Model Distillation as Shortcut in AI Strategy](https://news.google.com/rss/articles/CBMirgFBVV95cUxNUERWZDVySDZuLUJYR3VFTGk5a0RlODVYTUNDRTVSekZESVdTOFRUZHk2dGpqamNudzdsMC01V0NmeXJHZkZOY3lKaXlDX2JLUnNxTFpWdDRBVTJ5d3hyOFg1aUp4M1pmak9FRmJ0dGZvSUFkcm1IUGoyeE1SU0JVNG0ybVJNbHBZSzBfNGhFZDZYMHdXNWduX2FYakdUR18tM0NPYmRpOU1VZUtzY0E?oc=5) ⭐️ 6.0/10

ByteDance's CEO Zhang Yiming publicly rejected model distillation as a shortcut in the company's long-term AI development strategy, emphasizing sustainable growth over quick wins. This stance signals ByteDance's commitment to building proprietary AI capabilities from scratch, which could influence industry practices and set a precedent for other tech giants. It also highlights the growing importance of long-term AI research over short-term optimization. Model distillation involves training a smaller 'student' model to mimic a larger 'teacher' model, reducing computational costs but potentially limiting innovation. Zhang's rejection suggests ByteDance will prioritize original research and development, possibly increasing investment in foundational AI technologies.

google_news · 一财全球Yicai Global · Aug 11, 19:59

**Background**: Model distillation is a common technique in AI to compress large models into smaller, more efficient ones, often used to deploy AI on edge devices. ByteDance, known for apps like TikTok and Douyin, has been aggressively expanding its AI capabilities, with reported plans for massive investments in AI infrastructure. The company's strategy appears to focus on long-term competitiveness rather than immediate cost savings.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://www.openxcell.com/blog/model-distillation">Model Distillation — How It Works & Why It Matters</a></li>
<li><a href="https://intellibytes.substack.com/p/ai-distillation-explained-what-it">AI Distillation Explained: What It Is, How It Works, Legality ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#ByteDance`, `#model distillation`, `#industry strategy`

---

<a id="item-11"></a>
## [TVB Stock Surges on AI Computing Joint Venture with Gaw Capital](https://news.google.com/rss/articles/CBMivgFBVV95cUxQR3lLdEkxUFVGOGx4ZGJfWlUwWUZid1lBMTVmVzZCV3hLWEZxaHpuQmxkWWdtQTVCclZWYWVZRjBjWVNjVGk0bDlJMXFtWkRKM3pRc2c3bFlIY2ttWHh2b1NZTHlqT2RobFhObUJid0JJaHFoVFE5dl84N0JpVktGRnE3aHB0bl8yakJiRXFJakc4ODdjMWpaSHp2bGExODlMWWZZWWkxUWowUDduZWo3MHRoRGEybUpSQi1TNm13?oc=5) ⭐️ 5.0/10

TVB, Hong Kong's main terrestrial broadcaster, announced a joint venture with a Gaw Capital affiliate to build a subscription-based AI computing business, causing its shares to jump. The venture will develop AI computing facilities, including a data center at TVB's Tseung Kwan O campus, and procure GPUs and CPUs. This move marks a significant diversification for TVB, whose core broadcasting business has been under pressure, and signals growing interest from traditional media companies in the AI infrastructure market. It could provide a new revenue stream and contribute to Hong Kong's AI ecosystem development. The joint venture plans to build a data center within TVB's corporate campus at the Tseung Kwan O Industrial Estate, and has signed a Letter of Interest with a 'leading global technology group' for a sizeable subscription of AI computing services. TVB's broadcasting revenue fell 2% year-on-year to HK$3.2 billion in 2025, though the company returned to profitability.

google_news · 一财全球Yicai Global · Aug 11, 13:12

**Background**: AI computing involves providing computational resources, such as GPUs and CPUs, to run AI models and applications. Hong Kong is actively developing its AI ecosystem, with over 300 AI companies operating in the region. TVB, as a traditional broadcaster, is seeking new growth areas amid declining broadcast revenue.

<details><summary>References</summary>
<ul>
<li><a href="https://www.yicaiglobal.com/news/tvb-jumps-after-hong-kong-broadcaster-targets-ai-computing-market-with-new-joint-venture">TVB Jumps After Hong Kong Broadcaster Targets AI Computing ...</a></li>
<li><a href="https://www.minichart.com.sg/2026/08/11/tvb-plans-ai-advanced-computing-joint-venture-with-gaw-capital-and-signs-loi-with-global-tech-group/">TVB Plans AI Advanced Computing Joint Venture With Gaw ...</a></li>
<li><a href="https://www.mingtiandi.com/real-estate/data-centres/gaw-expanding-links-with-hong-kongs-tvb-in-ai-computing-plan/">Gaw Expanding Links with Hong Kong's TVB in AI Computing Plan - Mingtiandi</a></li>

</ul>
</details>

**Tags**: `#AI computing`, `#Hong Kong`, `#joint venture`, `#business news`

---