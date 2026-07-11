---
layout: default
title: "Horizon Summary: 2026-07-11 (EN)"
date: 2026-07-11
lang: en
---

> From 11 items, 6 important content pieces were selected

---

1. [GPT-5.6 Sol Ultra Claims Proof of Cycle Double Cover Conjecture](#item-1) ⭐️ 9.0/10
2. [Apple Sues OpenAI Over Trade Secret Theft](#item-2) ⭐️ 8.0/10
3. [QuadRF: Open-Source RF Sensor Sees Drones and WiFi Through Walls](#item-3) ⭐️ 8.0/10
4. [SGLang v0.5.15 Boosts GLM-5.2 Inference on Blackwell GPUs](#item-4) ⭐️ 7.0/10
5. [Nilay Patel: AR Glasses Require Always-On Cameras, Cloud Processing](#item-5) ⭐️ 7.0/10
6. [Deutsche Telekom rewires telecom with OpenAI](#item-6) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Sol Ultra Claims Proof of Cycle Double Cover Conjecture](https://cdn.openai.com/pdf/04d1d1e4-bc75-476a-97cf-49055cd98d31/cdc_proof.pdf) ⭐️ 9.0/10

OpenAI released a preprint claiming that its GPT-5.6 Sol Ultra model produced a proof of the Cycle Double Cover Conjecture, a long-standing open problem in graph theory. If verified, this would mark a major milestone in AI's ability to autonomously solve deep mathematical problems, potentially transforming how research is conducted in mathematics and theoretical computer science. The proof is extremely concise, suggesting a clever trick that experts may have missed, but the claim has not been peer-reviewed and the community is skeptical due to prompt engineering concerns and low prior interest in the conjecture.

hackernews · scrlk · Jul 10, 18:29 · [Discussion](https://news.ycombinator.com/item?id=48863490)

**Background**: The Cycle Double Cover Conjecture asks whether every bridgeless undirected graph has a collection of cycles such that each edge appears exactly twice. It was posed by Tutte, Itai, Rodeh, Szekeres, and Seymour, and has been open for decades. GPT-5.6 Sol Ultra is OpenAI's latest model, featuring a new 'ultra' mode that coordinates multiple agents for complex tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>

</ul>
</details>

**Discussion**: Community comments are skeptical: one user notes that the conjecture was only mentioned once on the site 14 years ago with zero upvotes, implying low interest. Another points out that much of the prompt is spent instructing the model to actually solve the problem, raising concerns about prompt engineering rather than autonomous reasoning.

**Tags**: `#AI`, `#mathematics`, `#conjecture`, `#GPT-5.6`, `#proof`

---

<a id="item-2"></a>
## [Apple Sues OpenAI Over Trade Secret Theft](https://9to5mac.com/2026/07/10/apple-sues-openai-trade-secret-theft/) ⭐️ 8.0/10

Apple has filed a lawsuit against OpenAI, accusing the company of orchestrating a scheme to steal trade secrets through former Apple employees, with evidence of systematic misconduct including emailing confidential information and using Apple hardware data to approach suppliers. This high-profile legal battle could set a precedent for trade secret protection in the AI industry and significantly impact OpenAI's reputation and business relationships, especially as it prepares for an IPO. The lawsuit alleges that OpenAI instructed new hires to avoid scrutiny when leaving Apple, and that one ex-Apple employee, Tang Yew Tan, who worked at Apple for 25 years, emailed himself confidential information before joining OpenAI.

hackernews · stock_toaster · Jul 10, 20:47 · [Discussion](https://news.ycombinator.com/item?id=48865019)

**Background**: Trade secrets are confidential business information that provides a competitive edge. Apple has a history of aggressively protecting its intellectual property, and this lawsuit reflects growing tensions in the AI sector over talent poaching and data theft.

**Discussion**: Community comments express strong support for Apple's case, with many believing the evidence is damning and that OpenAI will face severe consequences. Some commenters question OpenAI's trustworthiness and note that discovery will be favorable for Apple.

**Tags**: `#Apple`, `#OpenAI`, `#trade secrets`, `#lawsuit`, `#AI`

---

<a id="item-3"></a>
## [QuadRF: Open-Source RF Sensor Sees Drones and WiFi Through Walls](https://www.jeffgeerling.com/blog/2026/quadrf-can-spot-drones-and-see-wifi-through-my-wall/) ⭐️ 8.0/10

QuadRF, an open-source RF imaging platform, has been released that turns a Raspberry Pi 5 into a real-time RF camera capable of visualizing wireless signals through walls and detecting drones. This democratizes RF sensing technology, enabling hobbyists and researchers to explore spatial RF environments affordably, with applications in security, drone detection, and wireless diagnostics. The system uses a 4x4 MIMO SDR tile with phased-array antennas and runs on a Raspberry Pi 5, providing augmented reality visualization of RF signals in real time.

hackernews · speckx · Jul 10, 15:59 · [Discussion](https://news.ycombinator.com/item?id=48861717)

**Background**: Software-defined radio (SDR) allows flexible signal processing using software instead of dedicated hardware. RF sensing uses radio waves to detect objects or movements, and through-wall capabilities exploit the ability of certain frequencies to penetrate building materials. QuadRF combines these concepts into an accessible open-source hardware platform.

<details><summary>References</summary>
<ul>
<li><a href="https://www.opensourceforu.com/2026/07/rf-imaging-platform-visualises-wi-fi-signals/">RF Imaging Platform Visualises Wi-Fi Signals - Open Source ...</a></li>
<li><a href="https://www.hackster.io/news/quadrf-the-open-source-rf-camera-that-lets-you-see-wi-fi-signals-141ad91f2a2d">QuadRF: The Open Source RF Camera That Lets You See Wi-Fi ...</a></li>
<li><a href="https://github.com/dustinbowers/QuadRF">GitHub - dustinbowers/QuadRF</a></li>

</ul>
</details>

**Discussion**: The creator actively engaged in the comments, answering questions and noting improvements to the UI based on feedback. Some commenters expressed curiosity about extending the concept to sound localization or covering more RF bands, while others questioned the novelty of 'seeing WiFi through walls' since WiFi already penetrates walls.

**Tags**: `#RF sensing`, `#open-source hardware`, `#drone detection`, `#WiFi`, `#SDR`

---

<a id="item-4"></a>
## [SGLang v0.5.15 Boosts GLM-5.2 Inference on Blackwell GPUs](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 7.0/10

SGLang v0.5.15 delivers optimized GLM-5.2 NVFP4 inference on Blackwell GPUs, achieving over 500 tokens per second per user on 8x B300 and 450 on 4x GB300. Key improvements include Spec V2 with zero-overhead scheduling, IndexShare MTP for up to 1.9x lower draft-step cost, and TopK V2 with fused top-k selection. This release significantly improves the efficiency of serving large language models, particularly GLM-5.2, on NVIDIA's latest Blackwell architecture. The performance gains enable faster and more cost-effective LLM inference, benefiting production deployments and real-time applications. Spec V2 uses CUDA-graphable DSA draft-extend and fused metadata ops to achieve an 11% end-to-end throughput gain. IndexShare MTP reuses the indexer top-k across draft steps, reducing draft-step cost by up to 1.9x at long context. TopK V2 fuses top-k selection with page-table transform, supporting runtime k up to 2048.

github · Fridge003 · Jul 10, 22:58

**Background**: NVFP4 is a 4-bit floating-point precision format introduced by NVIDIA for Blackwell GPUs, offering a 3.5x memory reduction over FP16 with minimal accuracy loss. SGLang is an open-source LLM serving framework that optimizes inference throughput and latency. Speculative decoding accelerates generation by using a draft model to predict multiple tokens, which are then verified by the target model.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://docs.sglang.ai/advanced_features/speculative_decoding.html">Speculative Decoding - SGLang Documentation</a></li>
<li><a href="https://sebastianraschka.com/blog/2026/glm-5-2-indexshare.html">GLM-5.2 IndexShare Architecture Note | Sebastian Raschka, PhD</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#GPU optimization`, `#speculative decoding`, `#SGLang`, `#Blackwell`

---

<a id="item-5"></a>
## [Nilay Patel: AR Glasses Require Always-On Cameras, Cloud Processing](https://simonwillison.net/2026/Jul/10/nilay-patel/#atom-everything) ⭐️ 7.0/10

Nilay Patel, editor-in-chief of The Verge, argued on The Vergecast that practical augmented reality glasses must have always-on cameras and cloud processing, making privacy invasion unavoidable and potentially not worth the trade-off. This commentary highlights a fundamental privacy dilemma for AR glasses, challenging the industry's pursuit of lightweight, always-on devices. It could influence public debate and regulatory scrutiny around AR products from companies like Meta and Apple. Patel stated that no chip small enough to fit in a glasses stem can be both powerful and power-efficient enough for real-time AR processing, necessitating cloud offloading. He noted the alternative is a bulky device like Apple Vision Pro with an external battery pack.

rss · Simon Willison · Jul 10, 17:05

**Background**: Augmented reality glasses overlay digital information onto the real world, requiring real-time processing of camera feeds. Current lightweight designs, like Meta's Ray-Ban Stories, already raise privacy concerns due to their cameras, but they are not always-on. Achieving a true AR experience demands continuous video analysis, which current mobile chips cannot perform locally without excessive power consumption.

<details><summary>References</summary>
<ul>
<li><a href="https://9to5google.com/2026/07/09/meta-smart-glasses-privacy-light-always-on/">Meta developing always-on glasses with less-active privacy light</a></li>
<li><a href="https://www.msn.com/en-us/news/technology/now-meta-wants-its-glasses-camera-to-be-always-on-sparking-new-privacy-concerns/ar-AA27FfGz">Now Meta wants its glasses camera to be always-on ... - MSN</a></li>
<li><a href="https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/cloud-ar-vr-whitepaper-2/">Cloud AR/VR Whitepaper - Networks</a></li>

</ul>
</details>

**Tags**: `#augmented reality`, `#privacy`, `#cloud computing`, `#hardware`

---

<a id="item-6"></a>
## [Deutsche Telekom rewires telecom with OpenAI](https://openai.com/index/deutsche-telekom) ⭐️ 6.0/10

Deutsche Telekom is adopting OpenAI's AI models to transform customer service, employee workflows, network operations, and voice services, aiming to become an AI-native telco. This partnership showcases how traditional telecom operators can leverage frontier AI to drive efficiency and innovation, potentially setting a precedent for the industry's shift toward AI-native operations. The transformation spans multiple areas including customer service chatbots, internal workflow automation, network optimization, and next-generation voice services, though specific technical implementations and metrics are not disclosed.

rss · OpenAI Blog · Jul 10, 07:00

**Background**: An AI-native telco is one where AI is embedded into the core architecture, processes, and products, rather than used in isolated pockets. This approach promises radical efficiency, faster innovation, and new revenue streams. Deutsche Telekom's move aligns with a broader trend of telecom operators partnering with AI leaders like OpenAI to stay competitive.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/reimagining-connectivity-ai-native-evolution-from-aerdts-ph-d--me6uc">Reimagining Connectivity: The AI - Native Evolution from Telco to Techco</a></li>
<li><a href="https://medium.com/@sniranjaniyer/the-rise-of-the-ai-native-telco-rethinking-telecom-for-the-intelligence-era-5909ab6d788c">The Rise of the AI Native Telco : Rethinking Telecom for the... | Medium</a></li>
<li><a href="https://dataforest.ai/blog/scaling-the-ai-native-telco">Scaling the AI - Native Telco : From Concept to Competitive Edge</a></li>

</ul>
</details>

**Tags**: `#AI`, `#telecommunications`, `#OpenAI`, `#enterprise AI`

---