---
layout: default
title: "Horizon Summary: 2026-07-11 (EN)"
date: 2026-07-11
lang: en
---

> From 40 items, 9 important content pieces were selected

---

1. [GPT-5.6 Sol Ultra Proves Cycle Double Cover Conjecture](#item-1) ⭐️ 9.0/10
2. [China's Long March 10B achieves world's first net-based sea recovery](#item-2) ⭐️ 9.0/10
3. [SGLang v0.5.15 Boosts GLM-5.2 on Blackwell GPUs](#item-3) ⭐️ 8.0/10
4. [QuadRF Open-Source RF Sensor Detects Drones, Visualizes WiFi Through Walls](#item-4) ⭐️ 8.0/10
5. [Apple sues OpenAI over trade secret theft](#item-5) ⭐️ 8.0/10
6. [Why No Submission Limits Per Author in ML?](#item-6) ⭐️ 8.0/10
7. [Nilay Patel: AR glasses force privacy trade-off](#item-7) ⭐️ 7.0/10
8. [Deutsche Telekom rewires telecom with OpenAI](#item-8) ⭐️ 6.0/10
9. [MiniMax Plans $2 Billion Fundraising Amid Stock Decline](#item-9) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Sol Ultra Proves Cycle Double Cover Conjecture](https://cdn.openai.com/pdf/04d1d1e4-bc75-476a-97cf-49055cd98d31/cdc_proof.pdf) ⭐️ 9.0/10

OpenAI's GPT-5.6 Sol Ultra model has generated a proof of the Cycle Double Cover Conjecture, a long-standing open problem in graph theory, and released it as a preprint on July 10, 2026. This marks the first time an AI has produced a proof of a major open conjecture in mathematics, demonstrating the potential of large language models to contribute to theoretical research. It could accelerate discovery in graph theory and related fields. The proof is notably concise, suggesting it exploits a clever trick that experts had missed. The prompt used to guide the model was also released, revealing extensive instructions to reject vague optimism and focus on solving the problem.

hackernews · scrlk · Jul 10, 18:29 · [Discussion](https://news.ycombinator.com/item?id=48863490)

**Background**: The Cycle Double Cover Conjecture, posed by Tutte, Itai, Rodeh, Szekeres, and Seymour, states that every bridgeless undirected graph has a collection of cycles covering each edge exactly twice. It is a central open problem in graph theory with connections to graph embeddings. GPT-5.6 Sol Ultra is OpenAI's most advanced model, featuring an 'ultra' mode that coordinates multiple sub-agents for complex reasoning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>

</ul>
</details>

**Discussion**: The community is impressed but skeptical: some note the proof's conciseness suggests a clever trick, while others discuss the extensive prompt engineering required. There is debate about whether this constitutes true autonomous mathematical discovery.

**Tags**: `#AI`, `#mathematics`, `#graph theory`, `#proof`, `#OpenAI`

---

<a id="item-2"></a>
## [China's Long March 10B achieves world's first net-based sea recovery](https://weibo.com/7340734455/R814of1Ki) ⭐️ 9.0/10

On July 10, 2026, China's Long March 10B rocket launched from Hainan Commercial Space Launch Site and successfully recovered its first stage at sea using a net-based system, marking the world's first net-based recovery and China's first controlled recovery of a rocket first stage. This breakthrough demonstrates China's rapid progress in reusable rocket technology, potentially reducing launch costs and increasing payload capacity. It also introduces a novel net-based recovery method that differs from SpaceX's propulsive landing, offering an alternative approach to rocket reusability. The Long March 10B is a two-stage, medium-lift partially reusable rocket using kerosene/LOX for the first stage and methane/LOX for the second stage. The net-based recovery system uses pulley-driven cables to capture the first stage, simplifying onboard structure and reducing vehicle mass.

telegram · zaihuapd · Jul 10, 04:36

**Background**: Reusable rocket technology aims to recover and reuse rocket stages to lower launch costs. SpaceX's Falcon 9 first achieved propulsive landing in 2015. China's Long March 10B is under development for crewed lunar missions and commercial launches. The net-based recovery method is a novel alternative that avoids the need for landing legs and extra fuel for landing burns.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Long_March_10B">Long March 10B - Wikipedia</a></li>
<li><a href="https://www.globaltimes.cn/page/202607/1365624.shtml?id=12">China enters rocket recovery era as experts highlight... - Global Times</a></li>
<li><a href="https://www.newindianexpress.com/world/2026/Jul/10/china-achieves-first-controlled-recovery-of-reusable-rocket-booster-after-spacex-2">China achieves first controlled recovery of reusable rocket booster after SpaceX</a></li>

</ul>
</details>

**Tags**: `#aerospace`, `#reusable rocket`, `#Long March 10B`, `#net recovery`, `#China space`

---

<a id="item-3"></a>
## [SGLang v0.5.15 Boosts GLM-5.2 on Blackwell GPUs](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 8.0/10

SGLang v0.5.15 delivers optimized GLM-5.2 NVFP4 serving on Blackwell GPUs, achieving over 500 tokens/second/user on 8x B300 and 450 tokens/second/user on 4x GB300 at batch size 1. It also introduces Spec V2 by default, IndexShare MTP, TopK V2, and other performance enhancements. This release significantly improves inference throughput for large language models on NVIDIA's latest Blackwell architecture, making production deployment more efficient. The optimizations in speculative decoding and attention mechanisms benefit a wide range of LLM serving scenarios, especially for long-context tasks. Spec V2 achieves +11% end-to-end TPS by zero-overhead scheduling and fused metadata ops. IndexShare MTP reduces draft-step cost by up to 1.9x at long context by reusing the indexer top-k across draft steps. TopK V2 fuses top-k selection with page-table transform, supporting runtime k up to 2048.

github · Fridge003 · Jul 10, 22:58

**Background**: NVFP4 is a 4-bit floating-point format introduced with NVIDIA's Blackwell GPU architecture, designed for efficient low-precision inference with minimal accuracy loss. SGLang is an open-source LLM serving framework that supports various optimization techniques like speculative decoding, which uses a draft model to predict multiple tokens in parallel to speed up generation. Multi-Token Prediction (MTP) is a speculative decoding method where the target model itself predicts multiple future tokens.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference</a></li>
<li><a href="https://docs.sglang.io/docs/advanced_features/speculative_decoding">Speculative Decoding - SGLang Documentation</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**Tags**: `#AI inference`, `#GPU optimization`, `#speculative decoding`, `#LLM serving`, `#SGLang`

---

<a id="item-4"></a>
## [QuadRF Open-Source RF Sensor Detects Drones, Visualizes WiFi Through Walls](https://www.jeffgeerling.com/blog/2026/quadrf-can-spot-drones-and-see-wifi-through-my-wall/) ⭐️ 8.0/10

QuadRF, an open-source RF sensor combining a 4x4 MIMO SDR, phased-array antenna, and Raspberry Pi 5, can detect drones and visualize WiFi signals through walls in real-time as augmented reality overlays. This democratizes advanced RF sensing—previously limited to expensive military or research equipment—making it accessible to hobbyists, security researchers, and wireless engineers for drone detection, beamforming, and wireless research. The system uses a hybrid open model: the RF-core implementation is protected, while user-customizable elements like UI and software are fully open-source. It can also decode NTSC video transmissions from drones.

hackernews · speckx · Jul 10, 15:59 · [Discussion](https://news.ycombinator.com/item?id=48861717)

**Background**: RF sensing uses radio waves to detect objects and movement through walls, a technique long used by military and law enforcement. Software-defined radios (SDRs) have made such capabilities more accessible, but QuadRF packages a complete phased-array system in a single kit for real-time visualization.

<details><summary>References</summary>
<ul>
<li><a href="https://www.hackster.io/news/quadrf-the-open-source-rf-camera-that-lets-you-see-wi-fi-signals-141ad91f2a2d">QuadRF: The Open Source RF Camera That Lets You See Wi-Fi Signals - Hackster.io</a></li>
<li><a href="https://www.crowdsupply.com/scale-rf/quadrf">QuadRF | Crowd Supply</a></li>
<li><a href="https://scalerf.com/updates/">QuadRF Updates</a></li>

</ul>
</details>

**Discussion**: The creator engaged actively, addressing questions and noting UI improvements based on feedback. Some commenters questioned the novelty of 'seeing WiFi through walls,' while others expressed interest in extending the concept to sound localization or checking for hidden RF transmitters.

**Tags**: `#RF sensing`, `#open-source hardware`, `#drone detection`, `#WiFi visualization`, `#SDR`

---

<a id="item-5"></a>
## [Apple sues OpenAI over trade secret theft](https://9to5mac.com/2026/07/10/apple-sues-openai-trade-secret-theft/) ⭐️ 8.0/10

Apple has filed a lawsuit against OpenAI, alleging that the company systematically recruited ex-Apple employees who stole trade secrets, including confidential hardware information and supplier contacts. This high-profile case could set a precedent for how AI companies compete for talent and protect intellectual property, potentially reshaping hiring practices and trade secret enforcement in the tech industry. Apple claims OpenAI instructed new hires to avoid scrutiny when leaving Apple, and that employees like Tang Yew Tan, who worked at Apple for 25 years, emailed themselves confidential information before joining OpenAI.

hackernews · stock_toaster · Jul 10, 20:47 · [Discussion](https://news.ycombinator.com/item?id=48865019)

**Background**: Trade secret theft occurs when confidential business information is taken without authorization. Apple and OpenAI are major players in AI, with Apple focusing on on-device AI and OpenAI on cloud-based models. The lawsuit highlights tensions as AI talent moves between companies.

**Discussion**: Commenters largely side with Apple, calling the evidence damning and predicting OpenAI will face severe consequences. Some note the irony of a 25-year Apple veteran risking his career, while others warn that enterprises using OpenAI products may be taking a risk.

**Tags**: `#Apple`, `#OpenAI`, `#trade secrets`, `#lawsuit`, `#AI`

---

<a id="item-6"></a>
## [Why No Submission Limits Per Author in ML?](https://www.reddit.com/r/MachineLearning/comments/1usq43t/why_doesnt_the_ml_research_community_limit_the/) ⭐️ 8.0/10

A researcher on Reddit questions why the ML community does not limit the number of submissions per author to alleviate the burden on reviewers, citing successful practices in security (CCS) and computer architecture (DAC) conferences. This discussion highlights a systemic issue affecting peer review quality in ML, where high submission volumes strain reviewers and potentially degrade the rigor of top conferences. The post references ARR (ACL Rolling Review) cycles as an example of current struggles, and compares to CCS and DAC which have per-author limits to keep workloads manageable.

reddit · r/MachineLearning · /u/alafaya101 · Jul 10, 14:59

**Background**: ML conferences like NeurIPS and ICML have seen explosive growth in submissions, often exceeding 10,000 papers per cycle. Unlike some other fields, ML venues typically do not cap the number of papers an author can submit, leading to reviewer overload and concerns about review quality. ARR is a centralized reviewing platform for NLP conferences that has faced similar capacity issues.

<details><summary>References</summary>
<ul>
<li><a href="https://aclrollingreview.org/">ACL Rolling Review – A peer review platform for the Association for...</a></li>
<li><a href="https://www.sigsac.org/ccs/CCS2026/call-for/call-for-papers.html">ACM CCS 2026</a></li>
<li><a href="https://conferenceinc.net/post/dac-2026/">DAC 2026 in California: Dates, Registration Fees, Paper Submission & How to Register - Conference Inc.</a></li>

</ul>
</details>

**Discussion**: The Reddit thread likely includes debate on cultural factors, such as the ML community's emphasis on rapid iteration and the difficulty of defining authorship limits fairly. Some commenters may argue that limits could hinder collaboration or disproportionately affect junior researchers.

**Tags**: `#ML research`, `#peer review`, `#conference submissions`, `#academic culture`

---

<a id="item-7"></a>
## [Nilay Patel: AR glasses force privacy trade-off](https://simonwillison.net/2026/Jul/10/nilay-patel/#atom-everything) ⭐️ 7.0/10

Nilay Patel, editor-in-chief of The Verge, argued on The Vergecast that practical augmented reality glasses require always-on cameras and cloud processing, inevitably invading privacy, and suggested the product category may need to be abandoned. This commentary highlights a fundamental tension in AR development: the hardware limitations force a choice between privacy invasion or abandoning the form factor, affecting companies like Meta, Apple, and Google who are investing heavily in AR glasses. Patel noted that no chip small enough to fit in glasses stems can process real-time AR data locally; data must be sent to the cloud, making always-on cameras a necessity. He contrasted this with Apple Vision Pro's larger form factor with a separate battery pack.

rss · Simon Willison · Jul 10, 17:05

**Background**: Augmented reality glasses overlay digital information onto the real world, requiring real-time understanding of the user's environment via cameras. Current technology cannot achieve the necessary processing power and battery life in a glasses-sized device, forcing reliance on cloud computing. This raises significant privacy concerns because always-on cameras can record everything the user sees, potentially capturing bystanders without consent.

<details><summary>References</summary>
<ul>
<li><a href="https://digitechbytes.com/digital-lifestyle-productivity/always-on-ar-camera-ethics/">Ethical Implications of Always‑On Cameras in AR Glasses</a></li>
<li><a href="https://9to5google.com/2026/07/09/meta-smart-glasses-privacy-light-always-on/">Meta developing always-on glasses with less-active privacy light</a></li>
<li><a href="https://en.wikipedia.org/wiki/Augmented_reality">Augmented reality - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#augmented reality`, `#privacy`, `#technology ethics`, `#AR glasses`

---

<a id="item-8"></a>
## [Deutsche Telekom rewires telecom with OpenAI](https://openai.com/index/deutsche-telekom) ⭐️ 6.0/10

Deutsche Telekom announced a collaboration with OpenAI to integrate AI across customer service, employee workflows, network operations, and voice services, aiming to become an AI-native telco. This partnership signals a major shift in the telecom industry toward AI-native operations, potentially improving efficiency and customer experience while setting a precedent for other carriers. Deutsche Telekom is one of the first companies to gain early access to an alpha-phase OpenAI model, and the collaboration includes developing advanced AI applications for telecom-specific use cases.

rss · OpenAI Blog · Jul 10, 07:00

**Background**: Telecom operators have been investing in AI for over a decade, but recent advances in generative AI are accelerating adoption. An AI-native telco leverages AI to optimize network lifecycle stages from planning to operations, and about 50% of telco executives now report capturing impact from AI/gen AI.

<details><summary>References</summary>
<ul>
<li><a href="https://www.telekom.com/en/media/media-information/archive/openai-and-telekom-collaborate-1100164">OpenAI and Deutsche Telekom launch collaboration to deliver ...</a></li>
<li><a href="https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/scaling-the-ai-native-telco">Scaling the AI-native telco | McKinsey</a></li>
<li><a href="https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/the-ai-native-telco-radical-transformation-to-thrive-in-turbulent-times">The AI-native telco: Radical transformation to thrive in turbulent times | McKinsey</a></li>

</ul>
</details>

**Tags**: `#AI`, `#telecommunications`, `#OpenAI`, `#industry case study`

---

<a id="item-9"></a>
## [MiniMax Plans $2 Billion Fundraising Amid Stock Decline](https://news.google.com/rss/articles/CBMivwFBVV95cUxQLXF5NjVNZllua2lhMVV5aVN4SUJFN1drWE01NUFwM3RjY1lxa3JYX2JadjJEZVpPckV5UUpPdHF4b1VOeTZ1VVR6Q2NjUmxUbVd0cjdmREFNVC0tWHZ4VHQ3bVJ5dEo0X0FXLWtreDJYSHFXYUxyaXdCLU43ZU5XdUMzTDA0WXVSeGEzYmhEWGY2Ty1xNzJDaXlpWm93Tk03bzU1LUxfTnhaTkhwUTlmLWMwUHhNYzR1d21rVWxOdw?oc=5) ⭐️ 6.0/10

Chinese AI firm MiniMax announced a $2 billion fundraising plan, while its stock fell for a second consecutive day on the Hong Kong Stock Exchange. This large fundraising round signals continued investor interest in Chinese AI startups despite market volatility, and could fuel MiniMax's expansion in multimodal AI and consumer applications. MiniMax, listed on the Hong Kong Stock Exchange in January 2026, develops multimodal AI models and consumer apps like Talkie and Hailuo AI. The stock decline suggests market skepticism about the fundraising terms or valuation.

google_news · 一财全球Yicai Global · Jul 10, 10:59

**Background**: MiniMax is a Shanghai-based AI company known for its multimodal AI models and consumer-facing apps. The Chinese AI sector has seen massive fundraising rounds recently, with Moonshot AI raising $2 billion and DeepSeek reportedly seeking $7.4 billion, reflecting intense competition and high capital requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MiniMax_(company)">MiniMax (company)</a></li>
<li><a href="https://www.deepseekimagegenerator.com/moonshot-ai-raises-2-billion-china-open-weight-model-race/">Moonshot AI raises $ 2 billion in China AI funding push</a></li>
<li><a href="https://economictimes.indiatimes.com/tech/artificial-intelligence/deepseek-slated-to-draw-7-billion-in-maiden-fundraising-sources-say/articleshow/131475552.cms">DeepSeek slated to draw $7 billion in maiden fundraising , sources...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#fundraising`, `#Chinese tech`, `#MiniMax`

---