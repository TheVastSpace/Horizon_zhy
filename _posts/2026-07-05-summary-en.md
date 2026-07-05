---
layout: default
title: "Horizon Summary: 2026-07-05 (EN)"
date: 2026-07-05
lang: en
---

> From 27 items, 13 important content pieces were selected

---

1. [CDD Recovers Finetuning Data from Logits](#item-1) ⭐️ 9.0/10
2. [Current AI launches Open Source AI Gap Map](#item-2) ⭐️ 8.0/10
3. [Competence Gate Uses Internal Confidence for Tool Routing](#item-3) ⭐️ 8.0/10
4. [shadcn/ui switches default foundation to Base UI](#item-4) ⭐️ 7.0/10
5. [Command & Conquer Generals Gets Native Apple Port](#item-5) ⭐️ 7.0/10
6. [sqlite-utils 4.0rc2 reviewed with Claude Fable](#item-6) ⭐️ 7.0/10
7. [New Claude Models Weaken Tool Calls](#item-7) ⭐️ 7.0/10
8. [USAF Sparse Fine-Tuning for MoE Models](#item-8) ⭐️ 7.0/10
9. [H64LM: A from-scratch 249M-parameter MoE Transformer](#item-9) ⭐️ 7.0/10
10. [Buttons Should Do One Thing Reliably](#item-10) ⭐️ 6.0/10
11. [Josh W. Comeau Says AI Is Hitting Course Sales](#item-11) ⭐️ 6.0/10
12. [Let Claude Decide When to Delegate](#item-12) ⭐️ 6.0/10
13. [Open-source neural network shape validator](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [CDD Recovers Finetuning Data from Logits](https://www.reddit.com/r/MachineLearning/comments/1umn2dk/contrastive_decoding_diffing_cdd_recovering/) ⭐️ 9.0/10

Researchers introduced Contrastive Decoding Diffing (CDD), a grey-box model-diffing method that can recover verbatim content from narrowly finetuned LLMs using only base and finetuned model logit outputs. According to the report, CDD achieved 4+/5 verbatim recovery on 19 of 20 organism-model pairs across four model families, while the earlier white-box Activation Difference Lens (ADL) did not exceed 3/5 on the same benchmark. This raises the bar for model privacy and memorization audits because sensitive or proprietary finetuning data may be extractable even when model weights and activations are hidden. It also suggests that output logits alone can expose more about training and finetuning data than many practitioners may expect, which matters for deployers of custom LLMs and synthetic-data pipelines. CDD is described as the output-level analog of ADL: instead of steering with activation differences, it contrasts the base and finetuned models' logits directly, with no weight access, no layer selection, and no per-model calibration. The post also notes one unexpected artifact: the fictional scientist name "Dr. Elena Rodriguez" reappeared across multiple unrelated finetuning domains because it was favored by Claude Sonnet 3.6 during synthetic-data generation.

reddit · r/MachineLearning · /u/CebulkaZapiekana · Jul 3, 19:01

**Background**: Large language models can memorize portions of their training or finetuning data, sometimes reproducing them nearly verbatim during generation. Model diffing methods try to infer what changed between a base model and its finetuned version, which can reveal the effect of the fine-tuning process. ADL was a prior white-box approach that used activation differences, while CDD attempts a similar goal using only output logits, which are easier to access in restricted settings.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2605.25902">Reading the Finetuning Prior: Verbatim Content Recovery via Contrastive ...</a></li>
<li><a href="https://arxiv.org/pdf/2605.25902">Reading the Finetuning Prior: Verbatim Content Recovery via Contrastive ...</a></li>
<li><a href="https://www.machinebrief.com/news/unlocking-ais-hidden-memories-with-contrastive-decoding-9a3m">Unlocking AI's Hidden Memories with Contrastive Decoding</a></li>

</ul>
</details>

**Tags**: `#LLM security`, `#model memorization`, `#logit analysis`, `#finetuning`, `#machine learning research`

---

<a id="item-2"></a>
## [Current AI launches Open Source AI Gap Map](https://simonwillison.net/2026/Jul/3/open-source-ai-gap-map/#atom-everything) ⭐️ 8.0/10

Current AI launched the Open Source AI Gap Map v0.1, a public index of the open source AI ecosystem. The map details 421 products in depth, including 266 software tools and libraries, 85 models, 50 datasets, and 20 hardware projects from 228 organizations. The project gives researchers, builders, and investors a structured way to understand where the open source AI stack is crowded and where it still lacks coverage. Because Current AI says the effort is aimed at identifying high-leverage gaps, it could influence what new tools get built and where funding flows next. Current AI says the map organizes products into 14 categories across three stack layers: model components, product/UX, and infrastructure. The underlying data was released under an MIT license in a GitHub repository, including 1,184 YAML files plus notebooks, schemas, and scripts used to assemble the dataset.

rss · Simon Willison · Jul 3, 22:04

**Background**: Open source AI refers to models, tools, datasets, and infrastructure that are publicly available for others to inspect, reuse, and build on. Ecosystem maps like this try to show the shape of the stack, from core model pieces to the developer tools and hardware that support them. In this case, Current AI says the map is meant to highlight what is missing, not just what already exists.

<details><summary>References</summary>
<ul>
<li><a href="https://www.currentai.org/blogs/introducing-the-gap-map-v0-1">Introducing the Gap Map v0.1</a></li>
<li><a href="https://simonwillison.net/2026/Jul/3/open-source-ai-gap-map/">Open Source AI Gap Map</a></li>
<li><a href="https://map.currentai.org/">Current AI – Open Source AI Gap Map</a></li>

</ul>
</details>

**Tags**: `#open source AI`, `#ecosystem mapping`, `#AI tools`, `#models`, `#datasets`

---

<a id="item-3"></a>
## [Competence Gate Uses Internal Confidence for Tool Routing](https://www.reddit.com/r/MachineLearning/comments/1unw5un/competence_gate_gating_tooluse_on_a_small_models/) ⭐️ 8.0/10

A researcher released an open research prototype: a 10MB LoRA adapter for Qwen3.5-4B plus a small orchestration layer that decides whether to answer directly, search the web, or retrieve from local documents. The system reads internal confidence signals from the model rather than relying on its verbalized self-assessment, and it runs locally on Apple Silicon/MLX with a GGUF build for llama.cpp/Ollama. This matters because small instruct models often overstate confidence, which can lead to hallucinated answers or unnecessary exposure of private queries to public search engines. If the gate reliably routes uncertain or sensitive questions to retrieval instead of guessing, it could improve agent reliability and privacy for local, document-heavy workflows. The author reports that the gate improved error detection over the base model's tool calling, with a d′ gain of 0.46 and 87% of newly flagged cases being genuinely wrong answers. A two-signal version also reduced private questions sent to public search from 22% to 10%, but the author notes the privacy result is based on n=60 and the retrieval/competence dissociation on n=126 hand-authored items, so the evidence is still limited.

reddit · r/MachineLearning · /u/Synthium- · Jul 5, 07:49

**Background**: LoRA, or Low-Rank Adaptation, is a parameter-efficient fine-tuning method that adds small trainable matrices to a base model instead of updating all of its weights. In this project, LoRA is used to teach Qwen3.5-4B when to answer, when to search, and when to retrieve local passages. The broader idea is confidence estimation: if a model can tell when it is uncertain, an orchestrator can choose safer tools or decline to answer. The release also mentions local inference stacks such as MLX, llama.cpp, and Ollama, which are commonly used to run models on personal hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2106.09685">[2106.09685] LoRA: Low-Rank Adaptation of Large Language Models</a></li>
<li><a href="https://huggingface.co/learn/llm-course/chapter11/4">LoRA (Low-Rank Adaptation) · Hugging Face</a></li>
<li><a href="https://ollama.com/library/qwen3.5:4b">qwen3.5:4b - ollama.com</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#tool use`, `#confidence estimation`, `#retrieval`, `#local inference`

---

<a id="item-4"></a>
## [shadcn/ui switches default foundation to Base UI](https://ui.shadcn.com/docs/changelog) ⭐️ 7.0/10

shadcn/ui has changed its default component foundation from Radix to Base UI. The changelog announcement signals that future defaults and migration paths will now center on Base UI instead of Radix primitives. shadcn/ui is widely used in frontend projects, so a default foundation switch can influence how many teams build and maintain accessible UI components. It also reflects a broader shift in the React UI ecosystem toward headless, customizable component layers and migration tooling. Radix Primitives is a low-level, accessibility-focused UI component library, while Base UI is described as a headless React component library and low-level hooks system for accessible interfaces. Community discussion also suggests shadcn’s migration approach is drawing attention because it appears to lean more on LLM-assisted workflows than traditional codemods.

hackernews · dabinat · Jul 5, 04:46 · [Discussion](https://news.ycombinator.com/item?id=48791328)

**Background**: shadcn/ui is a popular way to assemble React user interfaces by copying components into a project rather than consuming a closed component package. Radix Primitives provides unstyled, accessible building blocks that developers can customize, which is why many UI systems use it as an underlying layer. Base UI is another headless component foundation, created by the makers of Radix, Floating UI, and Material UI. Because both libraries focus on accessibility and customization, changing the default foundation is more about ecosystem preference and maintenance strategy than about a simple visual redesign.

<details><summary>References</summary>
<ul>
<li><a href="https://www.radix-ui.com/primitives">Radix Primitives</a></li>
<li><a href="https://www.radix-ui.com/primitives/docs/overview/introduction">Introduction - Radix Primitives</a></li>
<li><a href="https://base-ui.com/">Unstyled UI components for accessible design systems · Base UI</a></li>

</ul>
</details>

**Discussion**: The discussion is broadly interested but mixed. Some commenters criticize the post’s tone and worry about increased reliance on AI for important release work, while others debate whether shadcn’s copy-paste model is preferable to a traditional UI library and whether LLM-driven migration tools are replacing codemods. A few also used the thread to ask for alternatives in other ecosystems, such as Angular.

**Tags**: `#frontend`, `#UI libraries`, `#shadcn/ui`, `#Radix`, `#Base UI`

---

<a id="item-5"></a>
## [Command & Conquer Generals Gets Native Apple Port](https://github.com/ammaarreshi/Generals-Mac-iOS-iPad/tree/main) ⭐️ 7.0/10

A community project has ported Command & Conquer: Generals to run natively on macOS, iPhone, and iPad using the Fable game-porting framework. The project is hosted on GitHub and has sparked discussion about how much of the work was done by Fable versus earlier reverse-engineering efforts. This shows how classic PC games can be revived across Apple platforms through community reverse engineering and modern tooling. It also highlights growing interest in LLM-assisted porting workflows, which could speed up future game preservation projects. The HN discussion suggests the port is not a simple one-step conversion: earlier work already handled much of the heavy lifting, and Fable appears to have added the final iOS and iPadOS support. One commenter also noted an indirect graphics path, described as DirectX 8 to DXVK to Vulkan to MoltenVK to Metal, which implies a layered compatibility stack rather than a direct rewrite.

hackernews · asronline · Jul 4, 19:41 · [Discussion](https://news.ycombinator.com/item?id=48788283)

**Background**: Command & Conquer: Generals is a classic real-time strategy game originally built for Windows-era PCs, so running it on Apple devices usually requires significant compatibility work. Reverse engineering is the process of studying compiled software to understand how it works so it can be fixed, modified, or ported without the original source code. Fable refers to the tooling used here to help with the porting workflow, and the discussion suggests LLMs may be useful for converting low-level code during this kind of work.

<details><summary>References</summary>
<ul>
<li><a href="https://explainx.ai/blog/command-conquer-generals-fable-5-macos-ios-port-2026">C&C Generals Ported to iPad with Claude Fable 5 — What Actually ...</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly enthusiastic about LLM-assisted reverse engineering, with several arguing that Ghidra plus an LLM can save a large amount of time when reviving old games. Others were more skeptical about the framing, saying the headline overstates Fable's role and that the project's documentation and credit assignment could have been clearer.

**Tags**: `#game-porting`, `#reverse-engineering`, `#macOS`, `#iOS`, `#LLM-assisted-development`

---

<a id="item-6"></a>
## [sqlite-utils 4.0rc2 reviewed with Claude Fable](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/#atom-everything) ⭐️ 7.0/10

Simon Willison used Claude Fable to do a final pre-release review of sqlite-utils 4.0rc2 before moving toward a stable 4.0 release. The agent found five release blockers, including a serious `delete_where()` bug that could leave transactions uncommitted and cause data loss. sqlite-utils is a widely used Python tool for working with SQLite, so catching a bug like this before a major release helps prevent real-world data corruption. The post also shows a practical AI-assisted release workflow where an agent can surface issues that human review may miss, especially under time pressure. Willison says the review took 37 prompts, 34 commits, and more than 1,300 lines of additions across 30 files. He also notes that although the bug was severe, it looked fixable in a 4.0.1 point release rather than requiring a 5.0 redesign.

rss · Simon Willison · Jul 5, 01:00

**Background**: sqlite-utils is a Python library that helps developers create, query, and manipulate SQLite databases with less boilerplate. A release candidate, or RC, is a near-final pre-release version used to catch remaining bugs before a stable launch. SemVer, short for semantic versioning, is a release convention where incompatible changes are typically reserved for major version bumps.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://sqlite-utils.datasette.io/en/stable/python-api.html">sqlite _ utils Python library - sqlite - utils</a></li>

</ul>
</details>

**Tags**: `#sqlite-utils`, `#Python`, `#AI-assisted development`, `#release engineering`, `#Claude Fable`

---

<a id="item-7"></a>
## [New Claude Models Weaken Tool Calls](https://simonwillison.net/2026/Jul/4/better-models-worse-tools/#atom-everything) ⭐️ 7.0/10

Armin Ronacher reported that newer Claude models, including Claude Opus 4.8 and Claude Sonnet 5, sometimes generate malformed arguments for Pi’s edit tool. In his case, the edit content was often correct, but the nested `edits[]` arguments contained invented fields, causing Pi to reject the tool call and ask the model to retry. This is a concrete regression in tool-calling reliability, which matters because many AI coding systems depend on strict schema compliance to work at all. It suggests that model quality improvements in one area can come with worse behavior in third-party agent frameworks, especially for developers integrating Claude into custom tooling. The failure appears to be specific to Pi’s edit schema and was observed on newer Anthropic models rather than older ones. Armin speculates that recent training for Claude Code’s built-in edit tools may have overfit the models to a particular tool shape, making custom edit tools more error-prone.

rss · Simon Willison · Jul 4, 22:53

**Background**: Tool use, also called function calling, lets a model emit structured arguments for an external action instead of plain text. In coding agents, the model’s output must match a tool schema exactly, or the harness may reject the call even if the underlying intent is correct. Claude and OpenAI use different edit-tool designs, with Claude using search-and-replace style edits and OpenAI’s Codex using an `apply_patch` mechanism.

**Tags**: `#LLMs`, `#tool calling`, `#Anthropic Claude`, `#AI engineering`, `#model reliability`

---

<a id="item-8"></a>
## [USAF Sparse Fine-Tuning for MoE Models](https://www.reddit.com/r/MachineLearning/comments/1unl62q/if_your_gpu_can_run_inference_it_should_be_able/) ⭐️ 7.0/10

A project called USAF, short for Ultra Sparse Adaptive Fine-Tuning, was announced as an open-source way to fine-tune MoE models on consumer GPUs. The author says it can fine-tune Qwen3-30B-A3B on an AMD RX 6750 XT with 12 GB of VRAM by training sparse expert weights and the router instead of adapters. If validated, this could lower the hardware barrier for adapting large MoE models, especially for users with consumer GPUs and AMD cards. It also explores an alternative to adapter-based fine-tuning, which is relevant as MoE models become more common in efficient large-model deployment. The post claims USAF trains only about 26 million of 4.8 billion parameters on a 12 GB GPU, and says it is the only method that works on AMD while updating both expert weights and the router. The announcement is a release-style post rather than a full technical paper, so the main claims should be treated as promising but not independently validated from this source alone.

reddit · r/MachineLearning · /u/tsuyu122 · Jul 4, 21:56

**Background**: Mixture-of-Experts, or MoE, models route each input through only a subset of specialized experts instead of activating every parameter at once. That sparse activation can make very large models cheaper to run at inference time, which is why models like Qwen3-30B-A3B can have 30B total parameters but only activate 3B per forward pass. Fine-tuning usually requires much more memory than inference, so methods that can update only a small subset of weights are important for making large models more accessible.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/tsuyu122/usaf/blob/master/README.md">usaf/README.md at master · tsuyu122/usaf · GitHub</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://langmart.ai/model-docs/models/openrouter_qwen_qwen3-30b-a3b.html">LangMart: Qwen: Qwen 3 30 B A 3 B - Openrouter | Model Documentation</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#mixture of experts`, `#fine-tuning`, `#GPU training`, `#open source`

---

<a id="item-9"></a>
## [H64LM: A from-scratch 249M-parameter MoE Transformer](https://www.reddit.com/r/MachineLearning/comments/1umqfd2/h64lm_a_249mparameter_mixtureofexperts/) ⭐️ 7.0/10

A developer released H64LM, a 249M-parameter Mixture-of-Experts Transformer implemented from scratch in PyTorch. The project includes GQA, Top-2 MoE routing with three auxiliary routing losses, RoPE, RMSNorm, SwiGLU, sliding-window attention, mixed-precision training, checkpointing, and resume support. The project is useful as a hands-on reference for how modern LLM building blocks fit together in a full training pipeline. It is especially relevant for practitioners who want to understand MoE routing and other architecture choices without relying on high-level training frameworks. The included checkpoint was trained on a subset of WikiText-103 to validate the end-to-end pipeline, not to produce a strong model, and the author notes it overfits after about epoch 10 with best validation perplexity around 40.5. Known limitations include batch-size-1-only generation and no true DDP support, with DataParallel used as a fallback.

reddit · r/MachineLearning · /u/Loose_Literature6090 · Jul 3, 21:18

**Background**: Mixture-of-Experts models route each token to a small subset of specialized experts, which can increase capacity without activating every parameter for every token. The cited web material also notes that router quality matters because poor routing can cause load imbalance and hurt accuracy. GQA, RoPE, RMSNorm, and SwiGLU are all common components in modern Transformer blocks, and GQA in particular helps reduce KV-cache memory during attention.

<details><summary>References</summary>
<ul>
<li><a href="https://simulations4all.com/simulations/mixture-of-experts-moe-visualizer">Free Mixture of Experts (MoE) Visualizer | Simulations4All</a></li>
<li><a href="https://www.allisone.co.jp/note/machine-learning/advanced/12_llm_en.html">Large Language Models ( LLMs ) - Advanced Machine Learning</a></li>
<li><a href="https://dev.to/zeromathai/how-modern-transformer-blocks-work-from-rmsnorm-to-moe-44cc">How Modern Transformer Blocks Work — From RMSNorm to MoE</a></li>

</ul>
</details>

**Tags**: `#PyTorch`, `#Mixture-of-Experts`, `#LLM architecture`, `#Transformer`, `#machine learning`

---

<a id="item-10"></a>
## [Buttons Should Do One Thing Reliably](https://unsung.aresluna.org/if-youre-a-button-you-have-one-job/) ⭐️ 6.0/10

The essay argues that a button or UI control should have one clear, visible job and should reliably do exactly that job every time. It uses examples of broken feedback loops and “cargo cult” animation patterns to show how interfaces can look active while failing to communicate what actually happened. This matters because reliable feedback is a basic requirement for usable software: if users cannot tell whether an action succeeded, they will repeat it, hesitate, or lose trust. The critique applies broadly to product design and engineering teams building interactive systems, especially where animations or state changes can obscure the result of a click. The essay emphasizes that animations should support interaction by masking loading time or easing transitions, not become a second system that code must wait on. Community examples also point to UI elements disappearing and reappearing after actions, or controls that give inconsistent feedback like beeping without completing the underlying task.

hackernews · nozzlegear · Jul 5, 02:01 · [Discussion](https://news.ycombinator.com/item?id=48790689)

**Background**: In user interface design, feedback is the signal that tells a user whether an action was received and what changed as a result. A well-designed button usually maps one click to one obvious outcome, with clear visual or textual confirmation when the action starts and ends. The phrase “cargo cult” here refers to copying the appearance of good design practices without preserving their actual purpose.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@blessingokpala/feedback-loops-are-broken-heres-how-to-fix-them-9fbb751d61f4">Feedback Loops Are Broken — Here’s How to Fix Them | Medium</a></li>
<li><a href="https://lethain.com/feedback-loops-in-software-development/">Feedback Loops in Software Development | Irrational Exuberance</a></li>
<li><a href="https://www.andrewyao.me/Single-Responsibility/">Applying the Single Responsibility Principle – Andrew J. Yao...</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed that inconsistent feedback is frustrating and can make users retry actions unnecessarily. Several pointed to real-world examples, including physical devices and software buttons that behave as if the first click did not count, while others argued that animations are fine only when they remain strictly supportive and do not block the interaction.

**Tags**: `#UX design`, `#user interface`, `#software engineering`, `#animation`, `#product design`

---

<a id="item-11"></a>
## [Josh W. Comeau Says AI Is Hitting Course Sales](https://simonwillison.net/2026/Jul/3/josh-w-comeau/#atom-everything) ⭐️ 6.0/10

Josh W. Comeau said his newly launched course, Whimsical Animations, is on track to sell about one-third as many copies as a typical launch. He also said sales for his two existing courses are significantly down from last year and linked the decline largely to AI. The comment highlights how AI may be changing both the demand for paid developer education and the economics of the creator economy. If learners increasingly rely on LLMs for tutoring or question whether developer careers are stable, that could pressure independent course creators and other education businesses. Comeau described a "double whammy": fewer people may invest in new dev skills because of uncertainty about future developer jobs, and those who do want to learn can ask LLMs for personalized help instead of buying a course. He also said he has spoken with other course creators who are seeing similar revenue declines of 50% or more, but this is anecdotal rather than a formal study.

rss · Simon Willison · Jul 3, 21:25

**Background**: Large language models, or LLMs, are AI systems that are trained on large amounts of text and can generate human-like responses. In developer education, they can act like interactive tutors by answering questions, explaining concepts, and helping troubleshoot code. Online course creators sell structured lessons, projects, and guidance, so they can be affected when free or low-cost AI tools substitute for some of that value.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cloudflare.com/learning/ai/what-is-large-language-model/">What is a large language model (LLM)? | Learning Center</a></li>
<li><a href="https://www.ibm.com/think/topics/large-language-models">What Are Large Language Models ( LLMs )? | IBM</a></li>

</ul>
</details>

**Tags**: `#AI impact`, `#developer education`, `#online courses`, `#creator economy`, `#LLMs`

---

<a id="item-12"></a>
## [Let Claude Decide When to Delegate](https://simonwillison.net/2026/Jul/3/judgement/#atom-everything) ⭐️ 6.0/10

Simon Willison reports a practical prompting tip for Claude Code and Fable: instead of micromanaging when to run tests or which model to use, ask the model to use its own judgment. He says Claude Code stored that instruction as a project memory entry and that it is already reducing his Fable token usage. The tip reflects a broader shift toward more autonomous AI coding workflows, where the main model focuses on judgment while smaller subagents handle routine implementation. For teams using expensive or limited models, this can improve cost efficiency without sacrificing quality on tasks that need stronger reasoning. Willison’s example tells Fable to decide on its own whether a task should trigger automated testing, rather than following a rigid rule like “only test larger features.” He also suggests using lower-power models in subagents for smaller coding tasks, while keeping design, review, and synthesis in the main loop.

rss · Simon Willison · Jul 3, 18:51

**Background**: Claude Code is an agentic coding tool that can run models in a workflow with tools, memory, and subagents. Fable is described by Anthropic as a high-end model that can work through long-running tasks, delegate to sub-agents, and check its own work. Prompt engineering is the practice of shaping instructions so LLMs behave more effectively without changing the model itself.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://apidog.com/blog/claude-fable-5-claude-code/">How to Use Claude Fable 5 with Claude Code</a></li>

</ul>
</details>

**Tags**: `#AI coding assistants`, `#prompt engineering`, `#Claude Code`, `#developer tooling`, `#LLM workflows`

---

<a id="item-13"></a>
## [Open-source neural network shape validator](https://www.reddit.com/r/MachineLearning/comments/1unvbdb/i_built_a_open_source_neural_network_shape/) ⭐️ 6.0/10

A developer has released Tensey, an open-source visual neural network editor that validates tensor shapes while models are being designed. It also estimates parameter counts, FLOPs, and VRAM usage, and can export runnable PyTorch code. Shape errors are a common and time-consuming source of failure in deep learning workflows, especially when wiring residual connections or Linear layers. A tool that catches those issues before training can save GPU time and make model prototyping faster for PyTorch users. The project claims proper shape inference across 63 operations and says the exported PyTorch code actually runs. It is MIT licensed and available via the Tensey web app and its GitHub repository.

reddit · r/MachineLearning · /u/uselessfuh · Jul 5, 06:58

**Background**: Tensor shape inference is the process of determining how tensor dimensions change as data flows through layers in a neural network. PyTorch users often inspect these shapes with hooks or other debugging tools to find mismatches before a forward pass fails. Estimating FLOPs and VRAM is also useful because it helps developers judge whether a model is computationally and memory feasible on a given GPU.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.pytorch.org/tutorials/recipes/recipes/reasoning_about_shapes.html">Reasoning about Shapes in PyTorch</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/3639477.3639718">Dynamic Inference of Likely Symbolic Tensor Shapes in Python Machine ...</a></li>
<li><a href="https://research.google/pubs/dynamic-inference-of-likely-symbolic-tensor-shapes-in-python-machine-learning-programs/">Dynamic Inference of Likely Symbolic Tensor Shapes in Python Machine ...</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#deep learning tools`, `#PyTorch`, `#tensor shapes`, `#open source`

---