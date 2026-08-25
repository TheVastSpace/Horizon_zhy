---
layout: default
title: "Horizon Summary: 2026-08-25 (EN)"
date: 2026-08-25
lang: en
---

> From 35 items, 19 important content pieces were selected

---

1. [Paint and Photos May Embed Invisible GUID Watermarks in Local AI Images](#item-1) ⭐️ 8.0/10
2. [seL4 completes AArch64 security proofs](#item-2) ⭐️ 8.0/10
3. [AI Generates Programmable 3D Spatial Software](#item-3) ⭐️ 8.0/10
4. [Xiaomi’s Xring O3 Reaches Apple-Level Single-Core Performance](#item-4) ⭐️ 7.0/10
5. [San Francisco Recreated as a Playable 3D Web World](#item-5) ⭐️ 7.0/10
6. [EU Packaging Rules Put Makers and Micro-Entrepreneurs Under Pressure](#item-6) ⭐️ 7.0/10
7. [Oceans Reach Their Highest Recorded Temperatures](#item-7) ⭐️ 7.0/10
8. [XMPP at 25: A Case for Digital Independence](#item-8) ⭐️ 7.0/10
9. [IPFS Shipyard Winds Down Centralized Maintainer Support](#item-9) ⭐️ 7.0/10
10. [Your Executable Is a SQLite Database](#item-10) ⭐️ 7.0/10
11. [Unbounded Labs Releases Bart, a Vintage 2.82B-Parameter LLM](#item-11) ⭐️ 7.0/10
12. [Hide My Email Stays on icloud.com](#item-12) ⭐️ 6.0/10
13. [Online Claim Denies the Tang Dynasty Existed](#item-13) ⭐️ 6.0/10
14. [Why Public Bathrooms Are Disappearing](#item-14) ⭐️ 6.0/10
15. [Anthropic’s Revenue Surges as Cheaper AI Tools Gain Adoption](#item-15) ⭐️ 6.0/10
16. [Expensive Fable Model Prompts Smarter Coding Task Allocation](#item-16) ⭐️ 6.0/10
17. [Hyperparameter Tuning for Fair MARL Comparisons](#item-17) ⭐️ 6.0/10
18. [CCPL tackles delayed penalties in constrained RL](#item-18) ⭐️ 6.0/10
19. [Minimal Open-Source Demo of LLM Watermarking](#item-19) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Paint and Photos May Embed Invisible GUID Watermarks in Local AI Images](https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/) ⭐️ 8.0/10

A reverse-engineering report found that Microsoft Paint and Photos can embed an invisible, server-issued 16-byte GUID watermark into images produced through their local AI-generation workflows. The workflow reportedly obtains the GUID through a remote moderation request before local generation, even though the image processing itself occurs on the device. This blurs the distinction between local processing and cloud-mediated services, while raising privacy, provenance, and anonymity concerns for users who expect local tools not to contact a remote service. Because the identifier is embedded in the pixels, it may remain attached to exported or shared images and could support later attribution if Microsoft can associate it with account or device records. The reported mechanism concerns invisible pixel-level watermarking and is separate from a visible AI label that users may be able to disable; the report says the invisible watermark has no apparent opt-out. The findings do not by themselves prove that any recipient can directly recover a user’s name or address, and the scope of affected features, including non-generative AI edits, remains uncertain.

hackernews · ComputerGuru · Aug 24, 15:28 · [Discussion](https://news.ycombinator.com/item?id=49421158)

**Background**: A digital watermark is information covertly embedded in image, audio, or video data so that it can survive ordinary handling and later be detected. A GUID is a long identifier designed to be highly unlikely to collide with another identifier; in this case, the reported GUID is issued remotely and then embedded into locally generated image pixels. The report also distinguishes local image generation from remote moderation, meaning that local execution does not necessarily mean the entire workflow is offline.

<details><summary>References</summary>
<ul>
<li><a href="https://xusheng.dev/posts/reversing/mspaint_invisible_watermark/main/">Microsoft Paint and Photos Embed Server-Issued GUIDs as Invisible Watermarks in Locally-Generated Images :: Xusheng Li</a></li>
<li><a href="https://en.wikipedia.org/wiki/Digital_watermarking">Digital watermarking - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Discussion largely focused on the silent, non-disableable identifier rather than the AI feature itself, with commenters warning that it could undermine online anonymity and criticizing Microsoft’s implementation quality. Some claims about subpoenas and automatic access to personal data were speculative, while others questioned whether every AI-assisted editing feature is affected.

**Tags**: `#Reverse Engineering`, `#Privacy`, `#Digital Watermarking`, `#Microsoft`, `#AI Image Editing`

---

<a id="item-2"></a>
## [seL4 completes AArch64 security proofs](https://proofcraft.systems/news-2026/#2026-08-21) ⭐️ 8.0/10

seL4 has completed its security proofs for non-MCS, unicore AArch64 systems. This extends the microkernel’s formal assurance to a widely used ARM 64-bit architecture. This is an important milestone for formally verified systems software because it strengthens the case for using seL4 on modern ARM hardware. It can increase confidence for deployments that depend on strong isolation and high-assurance kernel behavior. The result applies only to non-MCS configurations and unicore systems, so it does not cover the mixed-criticality scheduler variant or multiprocessor setups. The seL4 proof stack is built in Isabelle/HOL, and the security theorem still depends on setting up the system correctly, including access-control configuration.

hackernews · snvzz · Aug 24, 11:32 · [Discussion](https://news.ycombinator.com/item?id=49418255)

**Background**: seL4 is a formally verified microkernel, meaning key correctness and security properties are proven mathematically rather than only tested. Its proofs are used to argue that the kernel enforces isolation and confidentiality when the system is configured according to the proof assumptions. AArch64 is ARM’s 64-bit architecture, which is common in phones, servers, embedded devices, and automotive systems.

<details><summary>References</summary>
<ul>
<li><a href="https://sel4.systems/Verification/proofs.html">seL4 Proofs | seL4</a></li>
<li><a href="https://sel4.systems/">The seL4 Microkernel | seL4</a></li>
<li><a href="https://docs.sel4.systems/projects/sel4/verified-configurations.html">Verified Configurations | seL4 docs</a></li>

</ul>
</details>

**Discussion**: The comments are skeptical but engaged. Some readers immediately raised side-channel and timing-attack concerns, while others highlighted the limited scope of the result by pointing out the non-MCS and unicore fine print; another thread questioned real-world adoption and whether seL4 needs tighter Linux integration to make broader security claims.

**Tags**: `#seL4`, `#Formal Verification`, `#AArch64`, `#Operating Systems`, `#Systems Security`

---

<a id="item-3"></a>
## [AI Generates Programmable 3D Spatial Software](https://www.reddit.com/r/MachineLearning/comments/1vxcc1h/r_using_ai_as_a_spatial_software_generator_to/) ⭐️ 8.0/10

The paper and Nova3D demo present an approach in which LLMs generate 3D objects as hierarchical spatial software rather than monolithic mesh blobs. The resulting objects support built-in articulation, animation, and environment-dependent behavior from the time they are authored. This could make AI-generated assets more immediately usable in game development, industrial design, simulation, and AR/VR/XR workflows. Treating geometry as executable, editable logic may also enable more efficient adaptation across mobile devices and high-end game engines. The objects can be organized into explicit hierarchies with hinge or socket articulation and can contain logic for different compute environments. The approach currently trails conventional AI 3D generators on complex organic shapes, so its strongest near-term fit may be structured or mechanical objects.

reddit · r/MachineLearning · /u/mhb_11 · Aug 24, 19:10

**Background**: A monolithic mesh is a largely fixed surface representation, whereas programmable 3D represents parts, relationships, parameters, and behavior as editable logic. Related LLM-based systems such as Proc3D translate natural-language instructions into procedural representations and executable code, illustrating the broader shift from static meshes toward software-defined geometry. Hierarchies and joints are important because they let connected parts move in constrained ways instead of requiring an entirely new mesh for each pose.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2601.12234v1">Proc3D: Procedural 3D Generation and Parametric Editing of 3D Shapes with Large Language Models</a></li>

</ul>
</details>

**Tags**: `#3D generation`, `#LLMs`, `#computer graphics`, `#AI research`, `#procedural content`

---

<a id="item-4"></a>
## [Xiaomi’s Xring O3 Reaches Apple-Level Single-Core Performance](https://twitter.com/lemire/status/2091894299289874926) ⭐️ 7.0/10

Xiaomi’s Xring O3 reportedly matches Apple CPU performance in single-threaded benchmarks and exceeds it in multi-threaded tests. Reported figures include about 3,945 Geekbench single-core points and 15,221 multi-core points, although the comparison context remains incomplete. The results suggest Xiaomi is becoming a more credible smartphone silicon competitor, potentially increasing pressure on Qualcomm and MediaTek. Strong multi-threaded performance could benefit demanding mobile workloads, but real-world competitiveness will depend heavily on efficiency, sustained performance, and device thermals. Community comparisons note that the multi-threaded result may benefit from Xring O3 using 10 cores versus six in the Apple comparison, while some commenters identify its CPU cores as ARM C1-Ultra designs also used by MediaTek’s Dimensity 9500. The most important missing metric is performance per watt: reported laboratory scores may fall substantially under smartphone cooling and power limits.

hackernews · tosh · Aug 24, 15:08 · [Discussion](https://news.ycombinator.com/item?id=49420873)

**Background**: Single-threaded benchmarks measure how quickly one CPU core handles a task, while multi-threaded benchmarks use several cores at once. Xring O3 is described as a three-cluster mobile processor with Prime, Titanium, and Little cores, and search results report a 3-nanometer manufacturing process. These architectural and manufacturing details help explain why peak benchmark performance can be high, but they do not by themselves establish battery life or sustained performance.

<details><summary>References</summary>
<ul>
<li><a href="https://memeburn.com/xiaomi-xring-o3-chip-4ghz-mix-fold-5/">Xiaomi 's XRING O 3 Chip Just Broke the 4GHz Barrier... - Memeburn</a></li>
<li><a href="https://www.cpubenchmark.net/singleThread.html">PassMark CPU Benchmarks - Single Thread Performance</a></li>

</ul>
</details>

**Discussion**: The discussion was engaged but skeptical. Commenters agreed that Xiaomi’s ability to produce a competitive chip could pressure MediaTek and Qualcomm, while emphasizing that the comparison is affected by different core counts, possible reliance on ARM-designed cores, and the absence of performance-per-watt data; some also argued that matching Apple’s current result would not necessarily mean surpassing Apple’s latest designs.

**Tags**: `#CPU Architecture`, `#Smartphone SoCs`, `#ARM`, `#Benchmarking`, `#Semiconductor Competition`

---

<a id="item-5"></a>
## [San Francisco Recreated as a Playable 3D Web World](https://sf.thijs.gg/) ⭐️ 7.0/10

A browser-based project turns the entire city of San Francisco into a game-like 3D environment that users can explore, including vehicle driving and collectible coins. It demonstrates an interactive combination of WebGL-style graphics, geospatial mapping, and world-building. The project shows how web graphics and mapping technologies can make a city-scale environment immediately accessible without a dedicated game installation. It could inspire richer digital twins, urban visualizations, location-based games, and procedurally generated game worlds. The current experience is more of an interactive simulation than a full game, with the main game-like feature mentioned being coins collected while driving. Community reports also identify collision or navigation limitations, such as being unable to pass underneath some walkways in Japantown.

hackernews · centrosphere · Aug 24, 17:05 · [Discussion](https://news.ycombinator.com/item?id=49422784)

**Background**: WebGL is a JavaScript API that lets compatible browsers render interactive 2D and 3D graphics without plug-ins. City-scale 3D map systems commonly use hierarchical streaming techniques, such as the 3D Tiles standard, to load large geospatial datasets progressively while balancing visual quality and performance. Procedural generation refers to creating environments or their components through rules and algorithms rather than manually building every object.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API">WebGL: 2D and 3D graphics for the web - Web APIs | MDN</a></li>
<li><a href="https://github.com/CesiumGS/3d-tiles">GitHub - CesiumGS/3d-tiles: Specification for streaming massive heterogeneous 3D geospatial datasets :earth_americas: · GitHub</a></li>
<li><a href="https://www.autodesk.com/solutions/proceduralism">Proceduralism | What is Proceduralism? | Autodesk</a></li>

</ul>
</details>

**Discussion**: The discussion is strongly positive, with users praising the experience and one former San Francisco resident describing an emotional reaction to revisiting familiar places. Suggestions include higher-resolution local downloads, street names and landmarks, address-based teleportation, more life or MMO features, and pipelines combining elevation, building, map, and Street View data; commenters also reported minor geometry bugs and shared a similarly styled Seattle project.

**Tags**: `#WebGL`, `#3D visualization`, `#Game development`, `#Geospatial mapping`, `#Procedural generation`

---

<a id="item-6"></a>
## [EU Packaging Rules Put Makers and Micro-Entrepreneurs Under Pressure](https://lectronz.com/u/lectronz/articles/how-europe-is-killing-makers-and-micro-entrepreneurs) ⭐️ 7.0/10

The article argues that EU packaging and compliance rules could impose disproportionate costs and administrative burdens on makers and micro-entrepreneurs selling physical products. Community commenters challenge that interpretation, saying some rules may exempt micro-enterprises or businesses using generic packaging, while implementation remains unsettled across member states. Packaging compliance can affect whether small hardware businesses can afford to sell across EU markets, particularly when they lack dedicated legal, logistics, or reporting staff. The debate also highlights a broader tension between EU-wide environmental goals and the practical difficulties of regulating small sellers through systems designed for larger companies. The discussion disputes the article’s worst-case reading: one commenter cites an EU FAQ as indicating that some micro-enterprises and sellers using generic rather than branded packaging may be outside certain requirements, while another argues that member-state implementation creates divergent obligations. More generally, the company that first places packaged products on an EU market may carry Extended Producer Responsibility obligations, including registration and waste-financing duties, depending on the applicable national system.

hackernews · l-one-lone · Aug 24, 13:05 · [Discussion](https://news.ycombinator.com/item?id=49419237)

**Background**: The Packaging and Packaging Waste Regulation, commonly abbreviated as PPWR, is intended to reduce packaging waste and promote recyclable packaging across the EU. Extended Producer Responsibility, or EPR, makes businesses help organize or finance the collection and recycling of packaging they place on the market. The first company placing packaging on a national market is therefore often the relevant party for registration and reporting, although the detailed rules and exemptions can vary by country and business type.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kauflandglobalmarketplace.com/en/seller-university/formal-framework/the-new-eu-packaging-and-packaging-waste-regulation-ppwr/">The new EU Packaging and... - Kaufland Global Marketplace</a></li>
<li><a href="https://smallbusiness.co.uk/what-is-the-packaging-and-packaging-waste-regulation-ppwr/">What is the Packaging and Packaging Waste... - Small Business UK</a></li>
<li><a href="https://www.sgs.com/en-za/news/2026/08/cc2026q2-faq-what-you-need-to-know-about-the-eu-packaging-and-packaging-waste-regulation-ppwr">FAQ: What You Need to Know About the EU Packaging and...</a></li>

</ul>
</details>

**Discussion**: The discussion is highly skeptical of the article’s accuracy, with commenters arguing that it may misunderstand or exaggerate the EU rules and pointing to official guidance. Other participants emphasize the fragmentation of national implementation, the failure to establish a single central registry, and the difficulty of applying large-company compliance models to small entrepreneurs; one commenter also compares the EU approach with China’s more centralized e-commerce and logistics “choke points.”

**Tags**: `#EU regulation`, `#makers`, `#micro-entrepreneurs`, `#e-commerce`, `#packaging compliance`

---

<a id="item-7"></a>
## [Oceans Reach Their Highest Recorded Temperatures](https://www.bbc.com/news/articles/c62m4gpnp78o) ⭐️ 7.0/10

Global ocean temperatures have reached their highest recorded levels, according to the reported climate-science findings. The record highlights continued ocean warming amid accelerating climate change, with El Niño contributing to recent temperature patterns. Warmer oceans can intensify marine heatwaves, disrupt ecosystems, influence weather and rainfall, and contribute to sea-level rise through thermal expansion. These effects can threaten fisheries, coastal communities, infrastructure, and regions exposed to changing climate extremes. Ocean heat is not distributed evenly: regional marine heatwaves can develop, move, and produce different local effects on weather and marine life. El Niño helps explain some short-term global temperature patterns, but the record should be understood within the longer-term trend of human-driven ocean warming.

hackernews · tcp_handshaker · Aug 24, 19:19 · [Discussion](https://news.ycombinator.com/item?id=49424606)

**Background**: Ocean heat content refers to the amount of heat stored in seawater, while ocean temperature describes how warm the water is in a particular place and depth. Warmer seawater expands, making thermal expansion an important contributor to sea-level rise alongside melting glaciers and ice sheets. El Niño is a climate pattern that changes tropical Pacific ocean temperatures and also affects atmospheric circulation, clouds, and weather around the world.

<details><summary>References</summary>
<ul>
<li><a href="https://theconversation.com/nz-is-again-being-soaked-this-summer-record-ocean-heat-helps-explain-it-274013">NZ is again being soaked this summer – record ocean heat helps...</a></li>
<li><a href="https://theblueplanetpost.beehiiv.com/p/ocean-heat-content-hits-a-new-record-here-s-why-it-matters">Ocean Heat Content Hits a New Record — Here’s Why It Matters</a></li>
<li><a href="https://science.nasa.gov/earth/explore/el-nino/">El Niño - NASA Science</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agreed that the record is serious and reflects inadequate government action, while sharing links to explanatory science coverage. Some comments emphasized risks from El Niño and marine warming, but others made speculative or oversimplified claims about temperature effects and melting ice, so the discussion was not uniformly rigorous.

**Tags**: `#Climate Change`, `#Oceanography`, `#Environmental Science`, `#El Niño`, `#Energy Policy`

---

<a id="item-8"></a>
## [XMPP at 25: A Case for Digital Independence](https://gultsch.de/posts/25-years-of-digital-independence/) ⭐️ 7.0/10

A retrospective marks 25 years of XMPP, examining how the open, decentralized messaging standard has evolved and where it could be used next. It also considers the modern ecosystem surrounding XMPP rather than presenting a new protocol release. XMPP remains an example of federated, interoperable messaging that can reduce dependence on a single platform or provider. Its continued development could support modern messaging, telephony bridges, and communication between software agents. XMPP federation allows users on different servers to exchange messages and presence information, while XMPP Extension Protocols add features without changing the core protocol. The ecosystem still depends on the availability and quality of clients and servers, and the discussion highlights uneven Android notifications and the need for custom changes in agent-oriented use.

hackernews · inputmice · Aug 24, 15:51 · [Discussion](https://news.ycombinator.com/item?id=49421536)

**Background**: XMPP is a messaging protocol in which independently operated servers communicate with one another, much like an email federation. Its core specifications include mechanisms such as TLS and SASL for securing connections and authentication. The XMPP Standards Foundation develops additional capabilities through XMPP Extension Protocols, or XEPs.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XMPP">XMPP - Wikipedia</a></li>
<li><a href="https://xmpp.org/extensions/">Specifications | XMPP - The universal messaging standard</a></li>
<li><a href="https://www.process-one.net/blog/xmpp-matrix/">Understanding messaging protocols : XMPP and Matrix</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly positive about XMPP and cited Movim, Fluux, ejabberd, Dino, Cheogram, and the jmp.chat telephony bridge as evidence of a practical ecosystem. They also described using XMPP for AI-agent communication, regretted that Matrix did not build more directly on XMPP, recalled the period when major platforms supported it, and raised concerns about Android client notifications and ecosystem polish.

**Tags**: `#XMPP`, `#Decentralized Systems`, `#Open Standards`, `#Messaging`, `#Interoperability`

---

<a id="item-9"></a>
## [IPFS Shipyard Winds Down Centralized Maintainer Support](https://ipshipyard.com/blog/2026-the-end-of-ipfs-at-shipyard/) ⭐️ 7.0/10

IPFS Shipyard is winding down its centralized support for IPFS implementations and plans to shift toward grants for individual maintainers. The broader IPFS project is continuing rather than shutting down. The change alters how important open-source components in the IPFS ecosystem may be funded, coordinated, and maintained. It highlights the sustainability and governance challenges facing decentralized infrastructure projects that rely on a central organization for implementation support. The announcement concerns Shipyard, one maintainer organization supporting IPFS implementations, not the entire IPFS project. IPFS has multiple implementations for different languages and use cases, including implementations that integrate blockstores and libp2p for content discovery and pubsub.

hackernews · iand · Aug 24, 15:48 · [Discussion](https://news.ycombinator.com/item?id=49421489)

**Background**: IPFS is a decentralized, peer-to-peer system for storing and sharing distributed files. Its content-addressing model identifies data by cryptographic content identifiers rather than by the location of a conventional server. Multiple implementations can provide the protocol in different programming languages or for different deployment needs, so reducing support from one maintainer group does not automatically terminate the protocol.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.ipfs.tech/concepts/ipfs-implementations/">IPFS implementations | IPFS Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/InterPlanetary_File_System">InterPlanetary File System - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely clarified that the announcement is about Shipyard rather than IPFS itself, while criticizing its potentially misleading framing. Others expressed concern about project sustainability and strategic direction, suggested Iroh as an alternative peer-to-peer technology, questioned IPFS’s approach to web applications and privacy, and recalled prior ecosystem changes such as Cloudflare’s gateway transition.

**Tags**: `#IPFS`, `#Decentralized Systems`, `#Open Source Sustainability`, `#Peer-to-Peer Networking`, `#Project Governance`

---

<a id="item-10"></a>
## [Your Executable Is a SQLite Database](https://simonwillison.net/2026/Aug/24/your-executable-is-a-sqlite-database/) ⭐️ 7.0/10

Farid Zakaria demonstrated a Linux executable format that is also a SQLite database, storing ELF components across SQLite tables. A custom `self-exec` loader extracts the required components, while the SQLite application ID at byte offset 68 is set to `SELF` to identify the format. The technique shows that Linux can support unconventional executable formats by combining a structured, queryable SQLite container with a user-space loader. It is mainly useful for niche systems tooling and experimentation, rather than representing a broad replacement for ELF. The SQLite schema organizes the executable’s ELF-related parts into tables, and `binfmt_misc` can be registered to recognize the `SELF` marker at offset 68 and invoke `/usr/local/bin/self-exec`. Execution therefore depends on the custom loader and the relevant Linux `binfmt_misc` registration being available.

rss · Simon Willison · Aug 24, 11:38

**Background**: ELF is the executable and linkable file format commonly used for Linux binaries. SQLite databases have a 32-bit application ID stored at byte offset 68 in their file header, which can help identify application-specific file formats. Linux `binfmt_misc` allows the kernel to recognize custom executable patterns and pass matching files to a specified user-space interpreter.

<details><summary>References</summary>
<ul>
<li><a href="https://fzakaria.com/2026/08/23/your-executable-is-a-sqlite-database">Your executable is a SQLite database | Farid Zakaria’s Blog</a></li>
<li><a href="https://sqlite.work/sqlite-application-id-and-magic-number-registration-for-file-type-recognition/">SQLite Application ID and Magic Number Registration for File Type...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Binfmt_misc">binfmt _ misc - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#SQLite`, `#Linux`, `#ELF`, `#systems programming`, `#binfmt_misc`

---

<a id="item-11"></a>
## [Unbounded Labs Releases Bart, a Vintage 2.82B-Parameter LLM](https://www.reddit.com/r/MachineLearning/comments/1vx94er/bart_a_vintage_llm_r/) ⭐️ 7.0/10

Unbounded Labs released Bart, a 2.82-billion-parameter language model trained from scratch on 20.1 billion English tokens published before 1931. The project also provides a chat demo, an SFT model, open datasets, training code, evaluations, and documented experiments. Bart offers an open test case for studying whether language models trained on historically bounded data can reproduce historical knowledge, support reasoning, and generate original ideas. Its openly released corpus work and evaluations may help researchers investigate how data curation and efficient training affect smaller language models. The team says it cleaned Harvard's Institutional Books from 242 billion to 23 billion tokens, created the 20-task Vintage CORE benchmark suite, and used 100 autonomous experiments on one H100 to identify 26 improvements. The final model was trained for five days at 60% MFU, while the released SFT dataset contains 416,000 graded question-and-answer pairs grounded in pre-1930s text.

reddit · r/MachineLearning · /u/soggydoggy8 · Aug 24, 17:20

**Background**: Pretraining from scratch means that a model learns its language patterns from an initial token corpus rather than adapting an already trained model. Supervised fine-tuning, or SFT, further trains a model on labeled question-and-answer examples so that it better follows the intended interaction format. An ablation study removes or changes components of a system to estimate how much each component contributes to performance.

<details><summary>References</summary>
<ul>
<li><a href="https://datawhalechina.github.io/diy-llm/en/chapter13/chapter13_Training_Pipeline.html">Chapter 13: Basic Training Pipeline for Large Language Models</a></li>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/supervised-fine-tuning-sft-for-llms/">Supervised Fine - Tuning ( SFT ) for LLMs - GeeksforGeeks</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ablation_(artificial_intelligence)">Ablation (artificial intelligence) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Large Language Models`, `#AI Research`, `#Training Data`, `#Historical NLP`, `#Open Models`

---

<a id="item-12"></a>
## [Hide My Email Stays on icloud.com](https://developer.apple.com/news/?id=1ptvdtcm) ⭐️ 6.0/10

Apple confirmed that iCloud+ Hide My Email addresses will remain under the icloud.com domain instead of moving to a separate private domain. The update clarifies the address format for users who rely on Apple’s email relay feature. This matters because Hide My Email is a core iCloud+ privacy feature used to mask a user’s real address when signing up for websites, apps, and newsletters. Keeping it on icloud.com also avoids breaking existing expectations around deliverability and account management. Apple Support says iCloud+ subscribers can manage Hide My Email addresses and forward mail to the verified address on their Apple Account. Community discussion also noted that random icloud.com relay addresses are treated as ordinary email addresses for sending, but may still interact with spam filtering like other mail services.

hackernews · K7PJP · Aug 24, 22:13 · [Discussion](https://news.ycombinator.com/item?id=49426564)

**Background**: Hide My Email is part of iCloud+, Apple’s paid subscription tier that provides privacy-focused features. It generates random forwarding addresses so users can share an alias instead of their real inbox address. Those messages are then forwarded to the user’s verified Apple Account email address. The feature is commonly used for signups, shopping, and services where users want to limit spam or tracking.

<details><summary>References</summary>
<ul>
<li><a href="https://support.apple.com/en-us/105078">How to use Hide My Email with Sign in with Apple - Apple Support</a></li>
<li><a href="https://www.suped.com/learn/email-deliverability/can-i-email-users-who-have-apples-private-relay-email-addresses">Can I email users who have Apple 's private relay email addresses ?</a></li>
<li><a href="https://applemagazine.com/private-icloud-domain-sign-in-with-apple/">Apple Unifies Hide My Email and Sign in With Apple ... - AppleMagazine</a></li>

</ul>
</details>

**Discussion**: Commenters were mostly positive, with several users saying they were glad Apple kept the feature as-is because they use it heavily. Some also noted that Gmail may still mark mail from iCloud addresses as spam, while others questioned whether a private domain would have changed the underlying targeting problem.

**Tags**: `#Apple`, `#iCloud+`, `#Privacy`, `#Email`, `#Identity Management`

---

<a id="item-13"></a>
## [Online Claim Denies the Tang Dynasty Existed](https://www.cnn.com/2026/08/19/style/china-tang-dynasty-never-existed-hoax-intl-hnk) ⭐️ 6.0/10

A CNN article reports that part of China’s internet is circulating a conspiracy claim that the Tang Dynasty never existed. The discussion has spread enough to draw comparisons with other historical denial theories and misinformation campaigns. The claim matters because it targets one of the best-documented periods in Chinese history, making it a clear example of how misinformation can attack even well-established historical facts. It also reflects a broader pattern of online revisionism, where conspiracy narratives compete with scholarship for attention. The Tang Dynasty is generally dated to 618–907 CE, and the web results point to multiple lines of evidence, including archaeological sites and historical texts such as the Old Book of Tang and New Book of Tang. Commenters also compared the claim to the “phantom time” conspiracy theory, arguing that the Tang-denial narrative is similarly implausible.

hackernews · related · Aug 24, 21:03 · [Discussion](https://news.ycombinator.com/item?id=49425819)

**Background**: The Tang Dynasty was an imperial Chinese dynasty that followed the Sui and preceded the Five Dynasties and Ten Kingdoms period. It is widely regarded as a major era in Chinese history, and historians rely on both Chinese court histories and archaeological evidence to reconstruct it. Historical denialism is different from normal historical revision, because it rejects well-supported events rather than reinterpreting them with new evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tang_dynasty">Tang dynasty - Wikipedia</a></li>
<li><a href="https://www.worldhistory.org/Tang_Dynasty/">Tang Dynasty - World History Encyclopedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Historical_negationism">Historical negationism - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters overwhelmingly rejected the claim and pointed to primary sources, archaeology, and foreign records as strong evidence that the Tang Dynasty existed. Several compared it to other conspiracy theories, including phantom time and broader historical revisionism, while one commenter noted the phenomenon feels like narrative warfare rather than scholarship.

**Tags**: `#history`, `#misinformation`, `#china`, `#hacker-news`, `#conspiracy-theory`

---

<a id="item-14"></a>
## [Why Public Bathrooms Are Disappearing](https://daily.jstor.org/where-did-all-the-public-bathrooms-go/) ⭐️ 6.0/10

The JSTOR Daily article examines the decline of public bathrooms and the social, policy, and accessibility consequences of their disappearance. It treats restroom availability as an urban infrastructure and public-space issue rather than merely a matter of personal convenience. Reliable public bathrooms affect whether people with medical conditions, disabilities, or limited access to private facilities can safely participate in public life. Their decline also reveals how cities balance maintenance costs, public order, accessibility, and responsibility for shared spaces. The discussion highlights competing explanations and responsibilities: bathrooms may be closed because of vandalism, drug use, public sex, maintenance burdens, or limited enforcement, while their absence shifts the costs onto people who urgently need them. Experiences vary substantially by place, with commenters contrasting restroom access in parts of Europe, China, Thailand, and the United States.

hackernews · herbertl · Aug 24, 17:07 · [Discussion](https://news.ycombinator.com/item?id=49422800)

**Background**: Public bathrooms are shared facilities located in public or publicly accessible places, such as streets, parks, stations, and commercial areas. Because they must provide privacy while remaining available to strangers, they are difficult to manage: cities must address cleaning, safety, accessibility, and acceptable behavior at the same time. When facilities disappear, people who cannot easily wait or use private businesses face a disproportionate burden.

**Discussion**: The 277-comment discussion is broadly sympathetic to the need for public bathrooms, especially for people with IBS and others who cannot postpone using the toilet. Commenters disagree about whether the core problem is a failure of the commons or the behavior of a small minority, and they debate whether better staffing, enforcement, and public investment could preserve facilities; several also report that access is much better in particular regions.

**Tags**: `#urban infrastructure`, `#public policy`, `#accessibility`, `#urban planning`, `#hacker news discussion`

---

<a id="item-15"></a>
## [Anthropic’s Revenue Surges as Cheaper AI Tools Gain Adoption](https://simonwillison.net/2026/Aug/23/anthropics-best-ai-model-struggles-to-attract-users-as-cheaper-t/) ⭐️ 6.0/10

Anthropic’s reported annualized revenue rose from $47 billion in May to as much as $65 billion in July 2026, and the company expected its third quarter to be profitable. OpenAI’s annualized revenue reportedly exceeded $40 billion after growing 35% during the quarter, while Ramp’s July spending data showed Anthropic’s newer premium models attracting relatively limited usage. The figures suggest that rapid revenue growth does not necessarily mean a company’s most capable or expensive model has the broadest adoption. For enterprises, model pricing and cost efficiency may be becoming as important as capability as they choose among Anthropic, OpenAI, and cheaper alternatives. Ramp’s July Anthropic spending shares were led by Opus 4.8 at 28.0%, while Fable 5 accounted for 8.0% and Opus 5 for 3.5%; Opus 5 was released only on July 24. Annualized revenue is a projection based on a recent month or period rather than realized full-year revenue, and Ramp’s data measures company payments rather than the depth or scale of actual usage.

rss · Simon Willison · Aug 23, 20:24

**Background**: Annualized revenue run rate takes revenue from a recent month or period and projects it over a full year, which can magnify apparent growth when sales are accelerating. Ramp’s AI Index uses billing data from companies using Ramp corporate cards or invoicing to estimate business spending on AI tools. This can provide a directional view of adoption, but a payment from one company or employee does not necessarily represent widespread organizational use.

<details><summary>References</summary>
<ul>
<li><a href="https://overcentral.com/en/anthropic-revenue-run-rate/">Anthropic's Annualized Revenue Run Rate Surges to $65B</a></li>
<li><a href="https://ramp.com/data/ai-index-may-2026">Anthropic beats OpenAI on business adoption</a></li>
<li><a href="https://pod.wave.co/podcast/everyday-ai-podcast-an-ai-and-chatgpt-podcast/ep-777-no-anthropic-isnt-leading-in-enterprise-ai-adoption-separating-ai-facts-from-fiction-and-how-">Ep 777: No, Anthropic isn’t leading In Enterprise AI Adoption .</a></li>

</ul>
</details>

**Tags**: `#AI industry`, `#Anthropic`, `#OpenAI`, `#AI economics`, `#Enterprise adoption`

---

<a id="item-16"></a>
## [Expensive Fable Model Prompts Smarter Coding Task Allocation](https://simonwillison.net/2026/Aug/23/drew-breunig/) ⭐️ 6.0/10

Drew Breunig says the arrival of the highly capable but expensive Fable model changed how his team approaches AI-assisted coding. Instead of sending every task to the strongest model, the team began deciding which work should go to Fable, Opus, 5.6, K3, or GLM. The observation suggests that AI coding productivity is shifting from simply waiting for cheaper and stronger models toward optimizing model routing, coding harnesses, and context strategies. This could reduce costs while preserving quality for engineering teams that use multiple language models. Breunig describes Fable as incredible but says Opus and several other models were good enough for most of the team’s code, making task-to-model allocation important. The quote also cautions that a very capable model may not be the most economical choice for routine work.

rss · Simon Willison · Aug 23, 19:55

**Background**: A coding harness is the surrounding system that gives an AI coding agent tools, prompts, tests, and workflow rules. Context strategies determine which project information is included in a model’s input, while model routing selects different models according to task difficulty, cost, or required quality. Anthropic describes Claude Fable 5 as a model for ambitious coding projects such as large migrations, complex implementations, and multi-day autonomous sessions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://www.notdiamond.ai/?ref=taaft">Not Diamond - Model Routing for Coding Agents</a></li>

</ul>
</details>

**Tags**: `#AI coding agents`, `#LLMs`, `#model routing`, `#prompt engineering`, `#Anthropic Claude`

---

<a id="item-17"></a>
## [Hyperparameter Tuning for Fair MARL Comparisons](https://www.reddit.com/r/MachineLearning/comments/1vxfmms/hyperparameters_fine_tuning_for_marl_comparative/) ⭐️ 6.0/10

A researcher asks whether PPO variants in VMAS multi-agent tasks should share identical hyperparameters or be tuned separately for each architecture and scenario. The question is motivated by differences in learning rate, entropy coefficient, KL coefficient, and SGD batch size, with shared settings sometimes causing non-convergence. The choice directly affects whether an architectural comparison is fair, because a single shared configuration may disadvantage some methods while separate tuning may give each method unequal optimization effort. It is especially important here because the final goal is to compare test-time adversarial robustness of frozen policies, not merely training reward. The post discusses Independent PPO and Graph PPO, including HetGPPO, across multiple VMAS scenarios, and reports no established methodological answer or experimental result. A credible study would need to document the tuning protocol and distinguish failures caused by unsuitable optimization settings from genuine architectural weaknesses.

reddit · r/MachineLearning · /u/ham_bam0 · Aug 24, 21:10

**Background**: VMAS is a vectorized differentiable simulator intended for efficient multi-agent reinforcement learning benchmarking, and it can be used with TorchRL and BenchMARL. PPO is a policy-optimization method whose behavior depends on settings such as learning rate, entropy coefficient, KL-related controls, and batch size. In the proposed evaluation, policies are trained first and then frozen while adversarial attacks are applied at test time, so training choices can influence the robustness results indirectly.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/proroklab/VectorizedMultiAgentSimulator">GitHub - proroklab/VectorizedMultiAgentSimulator: VMAS is...</a></li>
<li><a href="https://medium.com/aureliantactics/ppo-hyperparameters-and-ranges-6fc2d29bccbe">PPO Hyperparameters and Ranges. Proximal Policy... | Medium</a></li>

</ul>
</details>

**Tags**: `#multi-agent reinforcement learning`, `#hyperparameter tuning`, `#PPO`, `#benchmarking`, `#adversarial robustness`

---

<a id="item-18"></a>
## [CCPL tackles delayed penalties in constrained RL](https://www.reddit.com/r/MachineLearning/comments/1vx11hz/delaycorrected_bellman_operator_causal/) ⭐️ 6.0/10

The post introduces CCPL (Causal Consequence-Penalized Learning), a constrained RL framework that tries to correct for stochastic consequence delays instead of assuming violations happen immediately. It combines a delay-corrected Bellman operator with an Interventional Consequence Net (ICN) that attributes penalties by estimated causal contribution rather than simple temporal proximity. Delayed and stochastic violations are common in real-world constrained RL, so penalizing the most recent action can misassign blame and distort learning. If the approach holds up, it could improve safety-critical RL systems by making constraint learning more faithful to actual causality. The author claims the delay-corrected Bellman operator uses an adaptive effective discount learned from the consequence-delay distribution, and that the contraction proof still works under unknown stochastic delay. A major limitation is that the ICN currently needs structural-causal-model labels for pretraining, so it is not yet learned end-to-end from observational or interventional data alone.

reddit · r/MachineLearning · /u/No_Cauliflower7923 · Aug 24, 12:11

**Background**: Constrained RL is a form of reinforcement learning where an agent must maximize reward while also respecting safety or cost constraints. Bellman operators are the update rules behind dynamic programming and value iteration, and contraction is the property that helps guarantee stable convergence to a fixed point. Causal attribution matters here because delayed penalties can make it hard to tell which action actually caused a later violation.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.stackexchange.com/questions/37412/are-my-proofs-that-the-bellman-operators-are-contractions-correct">reinforcement learning - Are my proofs that the Bellman operators ...</a></li>
<li><a href="https://web.stanford.edu/class/cme241/lecture_slides/BellmanOperators.pdf">Understanding (Exact) Dynamic Programming through Bellman ...</a></li>
<li><a href="https://pypi.org/project/ccpl-rl/">Causal Consequence -Penalized Learning for delayed constrained ...</a></li>

</ul>
</details>

**Tags**: `#constrained reinforcement learning`, `#causal inference`, `#delayed credit assignment`, `#Bellman operators`, `#theoretical analysis`

---

<a id="item-19"></a>
## [Minimal Open-Source Demo of LLM Watermarking](https://www.reddit.com/r/MachineLearning/comments/1vw18ys/implementing_watermarking_for_language_models_p/) ⭐️ 6.0/10

A Reddit post shares a minimal, educational open-source implementation of SynthID-Text-style watermarking for language models. The author says the project is not an exact reproduction of SynthID-Text, but a simplified version that shows how subtle statistical patterns can be embedded during token selection. This helps make an emerging AI safety and provenance technique easier to understand for developers and researchers. As more model providers explore watermarking, educational implementations can clarify how AI-generated text may be identified without visibly altering the output. The watermark described here is not a visible message or inserted ad; it is a statistical pattern introduced as the model chooses tokens. The post explicitly notes that the implementation simplifies some parts of the original SynthID-Text system to keep it understandable.

reddit · r/MachineLearning · /u/Saad_ahmed04 · Aug 23, 08:09

**Background**: Language models generate text one token at a time by predicting what token is most likely to follow the previous ones. Watermarking methods like SynthID-Text try to bias that generation process so the output carries an invisible signature that can later be detected. The goal is to identify AI-generated text while preserving generation quality and without changing how the underlying model works.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.google.dev/responsible/docs/safeguards/synthid">SynthID : Tools for watermarking and detecting LLM-generated Text</a></li>
<li><a href="https://huggingface.co/blog/synthid-text">Introducing SynthID Text</a></li>
<li><a href="https://deepmind.google/blog/watermarking-ai-generated-text-and-video-with-synthid/">Watermarking AI-generated text and video with SynthID</a></li>

</ul>
</details>

**Tags**: `#LLM watermarking`, `#AI-generated text`, `#SynthID`, `#Machine learning`, `#Open source`

---