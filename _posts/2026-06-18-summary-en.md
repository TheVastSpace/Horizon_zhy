---
layout: default
title: "Horizon Summary: 2026-06-18 (EN)"
date: 2026-06-18
lang: en
---

> From 50 items, 26 important content pieces were selected

---

1. [Firecracker VMs Accelerate Browser Startup](#item-1) ⭐️ 8.0/10
2. [RFC 10008 Introduces HTTP QUERY Method](#item-2) ⭐️ 8.0/10
3. [Tesco Shifts 40k Server Workloads from VMware](#item-3) ⭐️ 8.0/10
4. [GLM-5.2: Powerful 753B Parameter Text-Only LLM](#item-4) ⭐️ 8.0/10
5. [Charity Majors: AI Transforms Code Production](#item-5) ⭐️ 8.0/10
6. [NextLat: Self-Supervised Latent Prediction in Transformers](#item-6) ⭐️ 8.0/10
7. [Speculative Decoding Accelerates LLM Token Generation](#item-7) ⭐️ 8.0/10
8. [Contrastive targeted SFT as a mechinterp method - has anyone mapped causal dependency interactions this way? (D)](#item-8) ⭐️ 8.0/10
9. [Lore – Open source version control system designed for scalability](#item-9) ⭐️ 7.0/10
10. [US holds off blacklisting DeepSeek, more than 100 firms deemed security risks](#item-10) ⭐️ 7.0/10
11. [Leaked financial docs show OpenAI is losing billions of dollars a year](#item-11) ⭐️ 7.0/10
12. [U.S. science is in chaos](#item-12) ⭐️ 7.0/10
13. [Launch HN: Adam (YC W25) – Open-Source AI CAD](#item-13) ⭐️ 7.0/10
14. [A robot is sprinting towards you. Do you want it running on Claude or Grok?](#item-14) ⭐️ 7.0/10
15. [Volkswagen started blocking GrapheneOS users](#item-15) ⭐️ 7.0/10
16. [datasette 1.0a34](#item-16) ⭐️ 7.0/10
17. [The Fable 5 Export Controls Harm US Cyber Defense](#item-17) ⭐️ 7.0/10
18. [Is foundational AI research still something that can be done without access to HPC? (D)](#item-18) ⭐️ 7.0/10
19. [How do you analyze the relative "strength" of probes? (R)](#item-19) ⭐️ 7.0/10
20. [I deployed a GAN on a Raspberry Pi 4 and built a physical NFT minting device (P)](#item-20) ⭐️ 7.0/10
21. [I built a leakage-clean verifier for robot manipulation, is this useful? Am I solving a non-problem? (D)](#item-21) ⭐️ 7.0/10
22. [<click-to-play> — a still that plays](#item-22) ⭐️ 6.0/10
23. [datasette-tailscale 0.1a0 Alpha Release](#item-23) ⭐️ 6.0/10
24. [Quoting Georgi Gerganov](#item-24) ⭐️ 6.0/10
25. [Quoting Matteo Wong, The Atlantic](#item-25) ⭐️ 6.0/10
26. [Open-Source Hong Kong Horse Racing ML Pipeline — Feedback Welcome (P)](#item-26) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Firecracker VMs Accelerate Browser Startup](https://browser-use.com/posts/firecracker-browser-infra) ⭐️ 8.0/10

The post explains how running Firecracker VMs inside EC2 enables browser instances to start in less than one second. The approach has sparked robust technical debates on virtualization techniques and browser performance. This innovation is significant because it offers a novel method to drastically reduce browser startup times, which can enhance user experience and efficiency in performance-critical environments. It also contributes to ongoing discussions about optimizing virtualization in cloud infrastructures. The method uses AWS EC2 in combination with Firecracker microVMs to achieve sub-second browser launches, but it raises concerns regarding detection by anti-bot measures and ethical considerations in bypassing such defenses. Alternative approaches, such as using AWS Lambda or switching to lighter browser variants, were noted by community members.

hackernews · gregpr07 · Jun 16, 15:15 · [Discussion](https://news.ycombinator.com/item?id=48556561)

**Background**: Firecracker is an open source virtualization technology developed by AWS to run workloads in lightweight microVMs, providing enhanced security and performance. It is designed to bring the speed and resource efficiency of containers to virtual machines, making it valuable for serverless computing and performance-intensive applications. EC2 is Amazon's widely used cloud computing platform that supports various deployment models.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker-microvm/firecracker: Secure and fast ...</a></li>
<li><a href="https://firecracker-microvm.github.io/">GitHub Pages - Firecracker</a></li>

</ul>
</details>

**Discussion**: Community comments reflect mixed sentiments, with some expressing concerns over the ethical implications of avoiding anti-bot measures, while others discuss the technical benefits and potential alternatives such as using AWS Lambda or lighter browsers. Additionally, debates about the choice of Chromium versus more efficient browser implementations were also brought up.

**Tags**: `#Firecracker`, `#EC2`, `#virtualization`, `#performance`, `#AWS`

---

<a id="item-2"></a>
## [RFC 10008 Introduces HTTP QUERY Method](https://www.rfc-editor.org/info/rfc10008/) ⭐️ 8.0/10

RFC 10008 proposes a new HTTP QUERY method that allows a request to carry a body while ensuring safety and idempotency, addressing the limitations of GET requests with bodies. This update generates active debate over design choices and caching strategies in web protocols. This development is significant because it provides a standardized, safe alternative for including a body in HTTP requests, which can lead to more robust API designs and caching mechanisms. It is expected to impact web developers and architects by improving protocol reliability and interoperability. The specification emphasizes that QUERY is safe and idempotent, making it suitable for repeated requests without unintended state changes, and it addresses historical interoperability issues associated with GET requests carrying a body. Additionally, it raises important considerations regarding caching strategies, especially the challenge of incorporating the request body into cache keys.

hackernews · schappim · Jun 17, 10:51 · [Discussion](https://news.ycombinator.com/item?id=48568502)

**Background**: HTTP methods such as GET and POST have long been used with well-defined roles: GET for retrieving data without a body and POST for submitting data non-idempotently. However, the inability of GET to carry a body has been a consistent limitation in API design, prompting the need for a new method. RFC 10008 builds on decades of HTTP evolution by introducing QUERY as a safe, idempotent alternative. This change reflects ongoing efforts to align historical practices with modern web requirements.

<details><summary>References</summary>
<ul>
<li><a href="https://www.rfc-editor.org/info/rfc10008/">RFC 10008: The HTTP QUERY Method | RFC Editor</a></li>
<li><a href="https://httpwg.org/http-extensions/draft-ietf-httpbis-safe-method-w-body.html">The HTTP QUERY Method</a></li>

</ul>
</details>

**Discussion**: Community discussion reflects mixed opinions; some developers express concerns about caching complexities and the potential for oversized cache keys due to large request bodies, while others appreciate the move towards clarifying the roles of HTTP methods. There is also curiosity about integrating QUERY with HTML forms to avoid common POST pitfalls.

**Tags**: `#HTTP`, `#RFC`, `#Web Protocols`, `#Networking`, `#Standards`

---

<a id="item-3"></a>
## [Tesco Shifts 40k Server Workloads from VMware](https://arstechnica.com/information-technology/2026/06/tesco-moving-40000-server-workloads-off-vmware-amid-broadcoms-abusive-conduct/) ⭐️ 8.0/10

Tesco is moving 40,000 server workloads off VMware in response to Broadcom’s aggressive pricing strategies. This marks a significant change in its enterprise IT operations as the company seeks more cost-effective solutions. This decision is significant because it highlights the growing pressure on traditional virtualization vendors due to abusive pricing tactics, prompting enterprises to reconsider their vendor relationships. It also underscores the critical need for cost management in large-scale IT infrastructure. Tesco’s move involves transferring 40,000 server workloads away from VMware, driven by Broadcom’s reported abusive pricing practices. Additionally, Tesco faces migration challenges including potential incompatibility with existing backup solutions such as Veeam and Zerto.

hackernews · Bender · Jun 17, 21:00 · [Discussion](https://news.ycombinator.com/item?id=48576838)

**Background**: VMware is a leading provider of virtualization technology that many enterprises rely on for managing server workloads, while Broadcom is known for its aggressive pricing and business practices in various sectors. Tesco, one of the largest retailers in the United Kingdom, is adapting its IT strategy to better control costs and mitigate vendor-related risks.

**Discussion**: Community comments reflect strong criticism of Broadcom’s pricing strategy, with several contributors supporting Tesco's decision as a necessary step towards more reasonable IT spending. Some users also raised concerns about migration challenges and the impact on compatibility with backup software.

**Tags**: `#enterprise technology`, `#server workloads`, `#VMware`, `#pricing strategy`, `#Broadcom`

---

<a id="item-4"></a>
## [GLM-5.2: Powerful 753B Parameter Text-Only LLM](https://simonwillison.net/2026/Jun/17/glm-52/#atom-everything) ⭐️ 8.0/10

Chinese AI lab Z.ai released GLM-5.2, a 753 billion parameter text-only LLM with a 1-million token context window and open weights under an MIT license; it was first available to coding plan subscribers on June 13th and fully released on June 16th. The model builds on previous releases while substantially increasing both size and context length. This release marks a significant milestone in the development of open weights LLMs, potentially reshaping benchmarks in natural language processing and front-end coding tasks. Its unprecedented scale and extended context window could influence competitive dynamics among AI models. GLM-5.2 employs a Mixture of Experts strategy with 40 active parameters, resulting in a 753B parameter model and a substantial 1-million token context window. Despite its impressive performance on benchmarks like the Artificial Analysis Intelligence Index and Code Arena WebDev leaderboard, the model is notably token-hungry compared to previous versions and competitors.

rss · Simon Willison · Jun 17, 23:58

**Background**: Large language models (LLMs) are neural networks trained on massive amounts of text data to perform various natural language processing tasks. The Mixture of Experts technique involves using several specialized sub-models to improve efficiency and performance. Moreover, a 1-million token context window allows the model to consider extensive input data in a single operation, a substantial upgrade from previous token limits.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://hammadhaqqani.com/blog/llm-token-limits-context-windows-explained">LLM Context Windows and Token Limits: The Complete Guide ...</a></li>

</ul>
</details>

**Discussion**: The community response has been enthusiastic, with many praising the model's advanced output quality and benchmark performance despite its high token consumption. Overall, opinions are cautiously optimistic, highlighting both its breakthroughs and some practical limitations.

**Tags**: `#LLM`, `#Open Weights`, `#AI`, `#Model Release`, `#Chinese AI`

---

<a id="item-5"></a>
## [Charity Majors: AI Transforms Code Production](https://simonwillison.net/2026/Jun/17/charity-majors/#atom-everything) ⭐️ 8.0/10

A recent commentary by Charity Majors explains that generative AI has turned the economics of code production upside down by making code generation nearly free and instantaneous. This shift has transformed code from a valuable, curated asset into a disposable commodity. This paradigm shift is significant as it challenges traditional views on code value and curation, potentially reshaping software engineering practices. The change could impact how resources are allocated and managed in development teams. The commentary highlights that with generative AI, code that once required substantial time and expense to produce is now generated almost instantly, reducing its perceived value and necessitating new engineering discipline. It underlines the need for adapting to a new era where code is easily replaceable.

rss · Simon Willison · Jun 17, 17:12

**Background**: Generative AI refers to technologies that can produce content, including code, with minimal human intervention. Previously, writing code was a time-intensive process that required careful design and maintenance. With this shift, the economics that once made code production costly have been upended, leading to fresh challenges in quality control and best practices.

**Tags**: `#generative-ai`, `#ai-assisted-programming`, `#charity-majors`, `#software-engineering`

---

<a id="item-6"></a>
## [NextLat: Self-Supervised Latent Prediction in Transformers](https://www.reddit.com/r/MachineLearning/comments/1u84mio/nextlatent_prediction_transformers_r/) ⭐️ 8.0/10

Microsoft Research has introduced NextLat, a self-supervised learning method that trains transformers to predict their next latent state using both current states and the next token. The approach promises denser supervision and up to 3.3x faster inference via self-speculative decoding. This development is significant because it improves data efficiency and inference speed, addressing key limitations of traditional next-token prediction methods in transformers. Its potential to build compact world models could enhance reasoning and planning tasks across various machine learning applications. NextLat combines conventional next-token prediction with latent state prediction, enabling transformers to compress history into compact belief states. Additionally, it utilizes recursive multi-step lookahead and self-speculative decoding to bypass redundant computations and accelerate inference.

reddit · r/MachineLearning · /u/jayden_teoh_ · Jun 17, 08:44

**Background**: Self-supervised learning is a technique that leverages unlabeled data to learn useful representations, and transformers are a cornerstone in modern sequence modeling tasks. Traditional next-token prediction can be limited by a narrow focus on sequential data, which NextLat overcomes by predicting latent states. Self-speculative decoding offers a means to accelerate inference by processing multiple steps in parallel. These advancements are part of ongoing efforts to enhance efficiency in machine learning models.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/layerskip">Faster Text Generation with Self-Speculative Decoding</a></li>

</ul>
</details>

**Discussion**: Community reactions have been positive, with many expressing enthusiasm about the potential improvements in inference speed and data efficiency. Some participants, however, have discussed possible limitations and raised questions regarding the method's versatility across different transformer architectures.

**Tags**: `#transformers`, `#self-supervised-learning`, `#inference`, `#machine-learning`

---

<a id="item-7"></a>
## [Speculative Decoding Accelerates LLM Token Generation](https://www.reddit.com/r/MachineLearning/comments/1u83kzt/what_is_speculative_decoding_trending_on/) ⭐️ 8.0/10

A trending post on Papers with Code explains speculative decoding, a method where a fast draft model proposes multiple tokens that are then verified in parallel by a larger target model. SGLang recently detailed how they utilize DFlash speculative decoding to achieve state-of-the-art latencies in LLM inference serving. This technique is significant because it reduces the inherent latency in autoregressive token generation without compromising output quality. It aligns with current trends in optimizing the efficiency and performance of large-scale language models. Speculative decoding uses a fast draft model to propose several tokens simultaneously, which are then verified by a slower but more accurate target model in parallel. This approach has been integrated into frameworks such as SGLang and leverages tools like Modal and Z.ai's DFlash models to enhance performance.

reddit · r/MachineLearning · /u/NielsRogge · Jun 17, 07:41

**Background**: Large language models typically generate tokens sequentially using autoregressive decoding, which can lead to slow inference speeds. Speculative decoding introduces a draft-target method that predicts multiple tokens in a single forward pass, reducing latency. This technique is part of the broader efforts to optimize LLM inference in real-world applications.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency ...</a></li>
<li><a href="https://github.com/vllm-project/speculators">GitHub - vllm-project/speculators: A unified library for ...</a></li>

</ul>
</details>

**Discussion**: Reddit discussions reveal a mix of curiosity and positive feedback from the machine learning community, with many interested in comparing speculative decoding to other methods. Some users have also raised technical questions regarding its integration with existing inference systems.

**Tags**: `#LLM`, `#Inference Optimization`, `#Machine Learning`, `#Speculative Decoding`

---

<a id="item-8"></a>
## [Contrastive targeted SFT as a mechinterp method - has anyone mapped causal dependency interactions this way? (D)](https://www.reddit.com/r/MachineLearning/comments/1u8if6l/contrastive_targeted_sft_as_a_mechinterp_method/) ⭐️ 8.0/10

The post outlines an experimental method to map causal dependencies in large language models by using contrastive targeted SFT and ablation of specific network circuits.

reddit · r/MachineLearning · /u/Substantial_Diver469 · Jun 17, 18:31

**Tags**: `#machine learning`, `#mechanistic interpretability`, `#SFT`, `#causal analysis`, `#Large Language Models`

---

<a id="item-9"></a>
## [Lore – Open source version control system designed for scalability](https://lore.org/) ⭐️ 7.0/10

Lore is an open source version control system designed to improve game development workflows by efficiently managing non-text assets.

hackernews · regnerba · Jun 17, 14:30 · [Discussion](https://news.ycombinator.com/item?id=48571081)

**Tags**: `#version-control`, `#game-development`, `#opensource`, `#Perforce`, `#Git`

---

<a id="item-10"></a>
## [US holds off blacklisting DeepSeek, more than 100 firms deemed security risks](https://www.reuters.com/world/china/us-holds-off-blacklisting-chinas-deepseek-more-than-100-firms-deemed-security-2026-06-17/) ⭐️ 7.0/10

The US has decided not to blacklist DeepSeek for now, even as over 100 firms are labeled as security risks, stirring active debate within tech communities.

hackernews · giuliomagnifico · Jun 17, 03:55 · [Discussion](https://news.ycombinator.com/item?id=48565498)

**Tags**: `#tech policy`, `#security`, `#geopolitics`, `#AI regulation`, `#industry news`

---

<a id="item-11"></a>
## [Leaked financial docs show OpenAI is losing billions of dollars a year](https://arstechnica.com/ai/2026/06/leaked-financial-docs-show-openai-is-losing-billions-of-dollars-a-year/) ⭐️ 7.0/10

Leaked financial data reveal that OpenAI is losing billions annually due to high overhead costs, prompting a robust community debate on its long-term sustainability.

hackernews · greenchair · Jun 17, 21:31 · [Discussion](https://news.ycombinator.com/item?id=48577208)

**Tags**: `#OpenAI`, `#financials`, `#tech industry`, `#sustainability`, `#AI economics`

---

<a id="item-12"></a>
## [U.S. science is in chaos](https://www.scientificamerican.com/article/americas-compact-between-science-and-politics-is-broken/) ⭐️ 7.0/10

The content examines the growing crisis in U.S. science research driven by funding deficits, restrictive policies, and institutional neglect.

hackernews · presspot · Jun 17, 09:54 · [Discussion](https://news.ycombinator.com/item?id=48568058)

**Tags**: `#science policy`, `#research funding`, `#academic crisis`, `#US science`, `#institutional support`

---

<a id="item-13"></a>
## [Launch HN: Adam (YC W25) – Open-Source AI CAD](https://github.com/Adam-CAD/CADAM) ⭐️ 7.0/10

An open-source project aiming to transform mechanical CAD design by converting text prompts into code-generated CAD models.

hackernews · zachdive · Jun 17, 16:14 · [Discussion](https://news.ycombinator.com/item?id=48572553)

**Tags**: `#AI`, `#CAD`, `#Open-Source`, `#Mechanical Design`, `#Startup`

---

<a id="item-14"></a>
## [A robot is sprinting towards you. Do you want it running on Claude or Grok?](https://openrouter.ai/blog/insights/royale-last-agent-standing/) ⭐️ 7.0/10

The article contrasts the operational tradeoffs between AI models like Claude and Grok in a playful, cost-sensitive robot performance experiment.

hackernews · Usu · Jun 17, 21:00 · [Discussion](https://news.ycombinator.com/item?id=48576824)

**Tags**: `#AI`, `#LLM`, `#cost analysis`, `#robotics`, `#tech debate`

---

<a id="item-15"></a>
## [Volkswagen started blocking GrapheneOS users](https://discuss.grapheneos.org/d/35949-volkswagen-app?page=3) ⭐️ 7.0/10

Volkswagen has blocked GrapheneOS users from accessing its car integration API, leading to community dissatisfaction.

hackernews · microtonal · Jun 17, 15:04 · [Discussion](https://news.ycombinator.com/item?id=48571526)

**Tags**: `#automotive`, `#GrapheneOS`, `#Volkswagen`, `#API`, `#community`

---

<a id="item-16"></a>
## [datasette 1.0a34](https://simonwillison.net/2026/Jun/16/datasette/#atom-everything) ⭐️ 7.0/10

Datasette 1.0a34 adds tools for inserting, editing, and deleting rows directly through its interface.

rss · Simon Willison · Jun 16, 21:31

**Tags**: `#datasette`, `#release`, `#UI`, `#database`, `#SQL`

---

<a id="item-17"></a>
## [The Fable 5 Export Controls Harm US Cyber Defense](https://simonwillison.net/2026/Jun/16/fable-5-export-controls/#atom-everything) ⭐️ 7.0/10

The article critiques export controls that hinder effective cybersecurity by limiting how coding models address known vulnerabilities.

rss · Simon Willison · Jun 16, 05:20

**Tags**: `#cybersecurity`, `#export controls`, `#code analysis`, `#AI in coding`

---

<a id="item-18"></a>
## [Is foundational AI research still something that can be done without access to HPC? (D)](https://www.reddit.com/r/MachineLearning/comments/1u8jyat/is_foundational_ai_research_still_something_that/) ⭐️ 7.0/10

A discussion on whether foundational AI research can be pursued without access to high-performance computing infrastructure.

reddit · r/MachineLearning · /u/Proof-Bed-6928 · Jun 17, 19:26

**Tags**: `#AI`, `#machine learning`, `#hardware`, `#research`

---

<a id="item-19"></a>
## [How do you analyze the relative "strength" of probes? (R)](https://www.reddit.com/r/MachineLearning/comments/1u8lo60/how_do_you_analyze_the_relative_strength_of/) ⭐️ 7.0/10

A Reddit user inquires about methods to assess and balance the capacity of probes in language models, seeking theoretical guarantees and practical insights to address potential overfitting issues.

reddit · r/MachineLearning · /u/RepresentativeBee600 · Jun 17, 20:29

**Tags**: `#machine learning`, `#language models`, `#model interpretability`, `#circuit analysis`

---

<a id="item-20"></a>
## [I deployed a GAN on a Raspberry Pi 4 and built a physical NFT minting device (P)](https://www.reddit.com/r/MachineLearning/comments/1u8cqan/i_deployed_a_gan_on_a_raspberry_pi_4_and_built_a/) ⭐️ 7.0/10

A DCGAN is deployed on a Raspberry Pi to generate hybrid face images that are physically minted as NFTs using an ESP32 display.

reddit · r/MachineLearning · /u/Numerous-Dentist-882 · Jun 17, 15:05

**Tags**: `#GAN`, `#Raspberry Pi`, `#NFT`, `#Deep Learning`, `#ONNX`

---

<a id="item-21"></a>
## [I built a leakage-clean verifier for robot manipulation, is this useful? Am I solving a non-problem? (D)](https://www.reddit.com/r/MachineLearning/comments/1u7hxem/i_built_a_leakageclean_verifier_for_robot/) ⭐️ 7.0/10

The content presents a leakage-clean verification method for robot manipulation that uses object-centric graphs to independently validate task success, aiming to eliminate evaluation bias.

reddit · r/MachineLearning · /u/Alexpplay · Jun 16, 16:10

**Tags**: `#robotics`, `#machine learning`, `#verification`, `#benchmark`, `#manipulation`

---

<a id="item-22"></a>
## [<click-to-play> — a still that plays](https://simonwillison.net/2026/Jun/17/click-to-play-component/#atom-everything) ⭐️ 6.0/10

Simon Willison presents a Web Component that delays loading animated GIFs until they are clicked, enhancing page performance through progressive enhancement.

rss · Simon Willison · Jun 17, 03:56

**Tags**: `#javascript`, `#web-component`, `#progressive-enhancement`, `#gif`

---

<a id="item-23"></a>
## [datasette-tailscale 0.1a0 Alpha Release](https://simonwillison.net/2026/Jun/16/datasette-tailscale/#atom-everything) ⭐️ 6.0/10

The datasette-tailscale plugin has been released experimentally in its alpha version (0.1a0), integrating Datasette with Tailscale to enable secure local serving. The release introduces a new command that sets up a Datasette server with a Tailscale sidecar attached to your Tailnet. This release is significant because it offers a novel approach to securely serving data with minimal exposure by using Tailscale, reducing the risk of unintended public access. It reflects an ongoing trend in combining data serving with secure networking for private deployments. The plugin employs experimental Python bindings for the tailscale-rs library, which means it currently comes without full production guarantees and may have security limitations. It operates by launching a Datasette instance on localhost (127.0.0.1) and routing it through a Tailscale-provided proxy using a specific command-line invocation.

rss · Simon Willison · Jun 16, 16:18

**Background**: Datasette is a platform that allows users to publish and explore data interactively, typically by creating web interfaces for databases. Tailscale is a networking tool that creates a secure mesh VPN, enabling safe remote access without complex network configurations. The underlying tailscale-rs library, written in Rust, is experimental and provides multi-language bindings, including Python, which facilitates this integration. This development is part of a broader movement toward securing local data services through modern network tools.

<details><summary>References</summary>
<ul>
<li><a href="https://pypi.org/project/datasette-tailscale/">datasette-tailscale · PyPI</a></li>
<li><a href="https://github.com/datasette/datasette-tailscale/blob/main/README.md">datasette-tailscale/README.md at main - GitHub</a></li>
<li><a href="https://github.com/tailscale/tailscale-rs">GitHub - tailscale/tailscale-rs: Rust implementation of Tailscale (preview, experimental) · GitHub</a></li>

</ul>
</details>

**Tags**: `#datasette`, `#tailscale`, `#plugin`, `#experimental`, `#integration`

---

<a id="item-24"></a>
## [Quoting Georgi Gerganov](https://simonwillison.net/2026/Jun/16/georgi-gerganov/#atom-everything) ⭐️ 6.0/10

Georgi Gerganov shares his experience using the Qwen3.6-27B local model for coding tasks with his custom lightweight harness.

rss · Simon Willison · Jun 16, 16:04

**Tags**: `#AI/ML`, `#Local Models`, `#Coding`, `#LLMs`

---

<a id="item-25"></a>
## [Quoting Matteo Wong, The Atlantic](https://simonwillison.net/2026/Jun/16/matteo-wong-the-atlantic/#atom-everything) ⭐️ 6.0/10

Cybersecurity expert Katie Moussouris explains Anthropic's approach where the model differentiates between reviewing and fixing insecure code as part of a security evaluation.

rss · Simon Willison · Jun 16, 03:07

**Tags**: `#cybersecurity`, `#AI`, `#prompt engineering`, `#Anthropic`

---

<a id="item-26"></a>
## [Open-Source Hong Kong Horse Racing ML Pipeline — Feedback Welcome (P)](https://www.reddit.com/r/MachineLearning/comments/1u8twkz/opensource_hong_kong_horse_racing_ml_pipeline/) ⭐️ 6.0/10

An open-source ML pipeline for Hong Kong horse racing predictions that evaluates with-odds vs. no-odds models and includes various simulation techniques.

reddit · r/MachineLearning · /u/Marshallmatta · Jun 18, 02:21

**Tags**: `#machine-learning`, `#open-source`, `#horse racing`, `#predictive modeling`, `#simulation`

---