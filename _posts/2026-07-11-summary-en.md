---
layout: default
title: "Horizon Summary: 2026-07-11 (EN)"
date: 2026-07-11
lang: en
---

> From 30 items, 15 important content pieces were selected

---

1. [OpenAI launches GPT-5.6 in three sizes](#item-1) ⭐️ 9.0/10
2. [Apple Sues OpenAI Over Trade Secret Theft Claims](#item-2) ⭐️ 8.0/10
3. [OpenAI Claims GPT-5.6 Sol Ultra Proved CDC Conjecture](#item-3) ⭐️ 8.0/10
4. [How Terminator 2’s VFX Were Built](#item-4) ⭐️ 8.0/10
5. [AI 2040: Speculative Long-Range Forecast](#item-5) ⭐️ 8.0/10
6. [QuadRF Spots Drones and Visualizes WiFi Through Walls](#item-6) ⭐️ 7.0/10
7. [NYC Targets Deceptive Subscription Tactics](#item-7) ⭐️ 7.0/10
8. [Nilay Patel on AR Glasses’ Privacy Trade-offs](#item-8) ⭐️ 7.0/10
9. [Meta Launches Muse Spark 1.1 API](#item-9) ⭐️ 7.0/10
10. [Good Tools Should Fade Into the Background](#item-10) ⭐️ 6.0/10
11. [Late Bronze Age Collapse overview](#item-11) ⭐️ 6.0/10
12. [ML Submission Caps Debate](#item-12) ⭐️ 6.0/10
13. [Critic-Based Attacks Beat Actor-Based in Multi-Agent PPO](#item-13) ⭐️ 6.0/10
14. [Talos-XII Rust Gacha Simulator](#item-14) ⭐️ 6.0/10
15. [IMGNet swaps cosine for sign-pattern face matching](#item-15) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI launches GPT-5.6 in three sizes](https://simonwillison.net/2026/Jul/9/gpt-5-6/#atom-everything) ⭐️ 9.0/10

OpenAI has released GPT-5.6 to general availability in three sizes: Luna, Terra, and Sol. The family ships with a February 16, 2026 knowledge cutoff, a 1 million token context window, and up to 128,000 output tokens. A 1 million token context window and very large output limits make GPT-5.6 useful for longer, more stateful workflows, especially agentic tasks that need to carry a lot of context. OpenAI is also positioning the family competitively on benchmarked long-horizon work against Anthropic's Claude Fable 5. OpenAI says GPT-5.6 Sol reached 53.6 on Agents' Last Exam, beating Claude Fable 5's adaptive reasoning score by 13.1 points, while Terra and Luna were also reported to outperform Fable 5 at lower cost. The post also notes that SWE-Bench Pro may be unreliable, citing OpenAI's claim that about 30% of its tasks are broken.

rss · Simon Willison · Jul 9, 19:46

**Background**: A context window is how much text a model can consider at once, so larger windows help with long documents, multi-step reasoning, and agent workflows. Agents' Last Exam is a benchmark designed to measure long-horizon, economically valuable real-world tasks with verifiable outcomes. SWE-Bench Pro is a coding benchmark, but the article argues its results may be distorted by broken tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sciencetimes.com/articles/51540/20241101/pushing-the-boundaries-of-contextual-understanding.htm">Pushing the Boundaries of Contextual Understanding</a></li>
<li><a href="https://www.ibm.com/think/topics/context-window">What is a context window ? | IBM</a></li>
<li><a href="https://arxiv.org/abs/2606.05405">[2606.05405] Agents' Last Exam - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#LLMs`, `#model release`, `#AI benchmarks`, `#agentic AI`

---

<a id="item-2"></a>
## [Apple Sues OpenAI Over Trade Secret Theft Claims](https://9to5mac.com/2026/07/10/apple-sues-openai-trade-secret-theft/) ⭐️ 8.0/10

Apple has filed a lawsuit against OpenAI, alleging that former Apple employees stole trade secrets and that OpenAI improperly used confidential Apple information in recruiting and supplier outreach. The complaint, reported by MacRumors and 9to5Mac on July 10, 2026, centers on alleged misuse of sensitive internal information. This is a high-stakes dispute between one of the world's largest device makers and a leading AI company, so it could influence how AI firms recruit talent and interact with suppliers. If Apple’s claims gain traction, the case may reinforce stricter expectations around confidentiality, employee transitions, and enterprise trust in AI vendors. The community discussion highlighted allegations that OpenAI allegedly told new hires how to avoid scrutiny when leaving Apple, and that some recruits may have emailed confidential information to themselves before departing. The comments also referenced claims that OpenAI used Apple hardware information when approaching suppliers, which would be especially relevant in a trade secret misappropriation case.

hackernews · stock_toaster · Jul 10, 20:47 · [Discussion](https://news.ycombinator.com/item?id=48865019)

**Background**: Trade secret misappropriation is a legal claim that typically alleges someone improperly acquired, disclosed, or used confidential business information. In the U.S., such disputes are often pursued in civil court and can seek injunctions and damages. Recruiting disputes and supplier outreach can become legally sensitive when confidential internal data is carried into a new employer’s hiring or procurement process.

<details><summary>References</summary>
<ul>
<li><a href="https://www.justia.com/intellectual-property/trade-secrets/infringement/">Trade Secret Infringement & Potential Legal Defenses - Justia</a></li>
<li><a href="https://www.americanbar.org/groups/business_law/resources/business-law-today/2025-december/understanding-ip-damages-part-4-trade-secret-law/">Understanding IP Damages, Part 4: Trade Secret Law</a></li>

</ul>
</details>

**Discussion**: Commenters reacted strongly, with several treating the allegations as severe and potentially damaging to OpenAI’s credibility. Others focused on the discovery process and the legal firepower Apple could bring, while one comment framed the issue as a serious enterprise risk for any company using OpenAI products.

**Tags**: `#Apple`, `#OpenAI`, `#trade secrets`, `#lawsuit`, `#AI industry`

---

<a id="item-3"></a>
## [OpenAI Claims GPT-5.6 Sol Ultra Proved CDC Conjecture](https://cdn.openai.com/pdf/04d1d1e4-bc75-476a-97cf-49055cd98d31/cdc_proof.pdf) ⭐️ 8.0/10

OpenAI published a PDF claiming that GPT-5.6 Sol Ultra produced a proof of the Cycle Double Cover Conjecture. The proof and a separate prompt document were shared through OpenAI-hosted PDFs. The Cycle Double Cover Conjecture is a long-standing open problem in graph theory, so a claimed proof would be a notable milestone for automated theorem proving and AI-assisted mathematics. If the result holds up, it suggests frontier models may be able to tackle more than routine symbolic tasks and contribute to original mathematical research. The conjecture states that every bridgeless graph has a collection of cycles that covers every edge exactly twice. The search results note that the problem remains open in the mathematical literature and that the classic difficult cases are snarks, so any proof claim will need careful verification.

hackernews · scrlk · Jul 10, 18:29 · [Discussion](https://news.ycombinator.com/item?id=48863490)

**Background**: A cycle double cover is a graph-theory object in which cycles are chosen so that each edge appears exactly twice across the set. The conjecture was independently formulated by Szekeres and Seymour, and it has been studied for decades as one of the central open questions in the area. In AI theorem proving, models are often evaluated by whether they can generate machine-checkable proofs rather than just plausible explanations.

<details><summary>References</summary>
<ul>
<li><a href="https://mathworld.wolfram.com/CycleDoubleCoverConjecture.html">Cycle Double Cover Conjecture -- from Wolfram MathWorld</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover">Cycle double cover - Wikipedia</a></li>
<li><a href="https://cdn.openai.com/pdf/04d1d1e4-bc75-476a-97cf-49055cd98d31/cdc_proof.pdf">Introduction A PROOF OF THE CYCLE DOUBLE COV</a></li>

</ul>
</details>

**Discussion**: Commenters focused less on the conjecture itself and more on what the prompt reveals about current model limitations, especially how much instruction is needed to push the model into actually solving the problem. Others argued this is a strong indicator of what kinds of work are easiest to automate, while one commenter noted the proof appears unusually concise, suggesting a clever trick may be doing most of the work.

**Tags**: `#AI research`, `#theorem proving`, `#graph theory`, `#large language models`, `#Hacker News`

---

<a id="item-4"></a>
## [How Terminator 2’s VFX Were Built](https://vfxblog.com/2017/08/23/the-tech-of-terminator-2-an-oral-history/) ⭐️ 8.0/10

This oral history revisits the technical work behind 1991’s Terminator 2: Judgment Day, focusing on how ILM teams built the T-1000’s morphing and reflective effects. It highlights that the production split the work into multiple shot categories, including reusing pseudopod data from The Abyss and developing separate morphing workflows. Terminator 2 is a landmark in VFX history because it helped prove that CGI could support a major character, not just a brief effect shot. The techniques discussed here influenced later visual effects pipelines and remain important for anyone studying the transition from practical effects to modern digital filmmaking. Steve “Spaz” Williams describes five separate categories of shots for the film, including a pseudopod team and a morph team, which shows how specialized the production pipeline had to be. The article also underscores that the T-1000’s challenge was not just creating a chrome-like surface, but making that surface move convincingly while still reflecting the environment.

hackernews · markus_zhang · Jul 10, 16:48 · [Discussion](https://news.ycombinator.com/item?id=48862365)

**Background**: Terminator 2 combined practical effects, motion-control techniques, compositing, and early CGI to create shots that were difficult or impossible to film normally. The T-1000 became famous because it could appear human, then liquefy, split, and reform, which required a mix of animation and live-action integration. Industrial Light & Magic was the main VFX house behind these breakthroughs, and the film is still often cited as a turning point for digital characters.

<details><summary>References</summary>
<ul>
<li><a href="https://vfxblog.com/2017/08/23/the-tech-of-terminator-2-an-oral-history/">The tech of 'Terminator 2' – an oral history</a></li>
<li><a href="https://en.wikipedia.org/wiki/Special_effects_of_Terminator_2:_Judgment_Day">Special effects of Terminator 2: Judgment Day - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly enthusiastic and treated the article as a valuable deep dive into how much of the film had to be invented from scratch. Several noted related points, including the use of Softimage, the quality of the practical squib effects, and recommendations for the documentary Jurassic Punk and the film’s 4K rerelease.

**Tags**: `#VFX`, `#film history`, `#computer graphics`, `#practical effects`, `#digital animation`

---

<a id="item-5"></a>
## [AI 2040: Speculative Long-Range Forecast](https://ai-2040.com/) ⭐️ 8.0/10

The Hacker News discussion highlights "AI 2040: Plan A," a speculative forecast about where AI may be headed and how it could affect society. The thread focuses on claims about timelines, capability growth, and possible economic disruption rather than a concrete product launch or model release. Forecasts like this shape how people think about AI strategy, regulation, labor markets, and infrastructure investment. Even when speculative, they influence whether readers expect gradual change or rapid disruption across the economy. Several commenters challenged the forecast's assumptions, including claims such as robots being capable of 95% of cognitive and physical tasks by 2035 and a 74% unemployment rate. Others argued current LLM progress may be nearing a plateau rather than an exponential curve, which would imply slower capability gains.

hackernews · kschaul · Jul 9, 16:21 · [Discussion](https://news.ycombinator.com/item?id=48848425)

**Background**: AI forecasting is the practice of using patterns, trends, and assumptions to estimate how AI may evolve over time. Scenario planning goes a step further by exploring multiple possible futures rather than making a single prediction. Discussions about AI often connect technical progress to broader questions about labor, productivity, and the economy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cbo.gov/publication/61147">Artificial Intelligence and Its Potential Effects on the Economy and the Federal Budget | Congressional Budget Office</a></li>
<li><a href="https://www.congress.gov/crs-product/IF12762">The Macroeconomic Effects of Artificial Intelligence | Congress.gov | Library of Congress</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-forecasting">What is AI forecasting? - IBM</a></li>

</ul>
</details>

**Discussion**: The discussion was broadly skeptical, with commenters questioning both the plausibility of the timelines and the scale of economic disruption described. Some saw the piece as overly speculative, while others argued that AI progress may already be slowing from an exponential trajectory to a more incremental one.

**Tags**: `#AI forecasting`, `#artificial intelligence`, `#future of work`, `#long-term strategy`, `#Hacker News`

---

<a id="item-6"></a>
## [QuadRF Spots Drones and Visualizes WiFi Through Walls](https://www.jeffgeerling.com/blog/2026/quadrf-can-spot-drones-and-see-wifi-through-my-wall/) ⭐️ 7.0/10

QuadRF is an open-source RF sensing system that can detect drones and visualize WiFi signals through walls. The project drew major attention on Hacker News, with the creator joining the discussion and sharing demo and deeper-dive videos. This matters because RF sensing can turn ordinary wireless emissions into a source of environmental information, with potential uses in security, monitoring, and research. It also highlights how open-source hardware and signal processing are making advanced sensing tools more accessible to hobbyists and engineers. The project is framed as an RF sensing system, which means it infers objects or activity by analyzing properties of radio signals rather than using cameras or visible light. Community comments suggest the interface and calibration details, such as camera alignment and radio gain, matter for getting good results, and that the system is open source and customizable.

hackernews · speckx · Jul 10, 15:59 · [Discussion](https://news.ycombinator.com/item?id=48861717)

**Background**: RF sensing refers to using changes in radio signals, such as amplitude, phase, and frequency, to detect objects or movement in an environment. WiFi-based through-wall sensing has been demonstrated in prior research by using off-the-shelf WiFi transceivers to observe reflections and motion behind walls. Drone detection is another common RF sensing application because drones can emit distinctive radio signatures or be identified through signal analysis.

<details><summary>References</summary>
<ul>
<li><a href="https://web.ece.ucsb.edu/~ymostofi/WiFiReadingThroughWall">Reading Through Walls With WiFi</a></li>
<li><a href="https://people.csail.mit.edu/fadel/wivi/">See Through Walls with WiFi</a></li>

</ul>
</details>

**Discussion**: The creator responded directly, offering help and noting that the team is improving the UI based on feedback. Commenters were intrigued by the idea of through-wall RF visualization, though one user questioned the headline wording because WiFi already penetrates walls in everyday use.

**Tags**: `#RF sensing`, `#wireless`, `#open source hardware`, `#drone detection`, `#signal processing`

---

<a id="item-7"></a>
## [NYC Targets Deceptive Subscription Tactics](https://www.theguardian.com/us-news/2026/jul/10/new-york-city-deceptive-subscriptions-ban) ⭐️ 7.0/10

New York City announced a new consumer-protection rule aimed at banning deceptive subscription cancellation tactics and hidden fee practices. The policy is being framed as a “click to cancel” style requirement and was announced by Mayor Mamdani on July 10, 2026. The rule could affect how companies across media, SaaS, hospitality, and other subscription-heavy businesses present recurring charges and cancellation flows. If enforced strongly, it may reduce dark patterns that make it harder for customers to leave services or understand the real price. The discussion around the rule centers on whether it will have real teeth and whether any industry carve-outs will weaken it. Commenters pointed to examples such as restaurant service charges, hotel resort fees, and failed cancellations from services like Evernote and The New York Times as evidence that hidden-fee and cancellation problems remain widespread.

hackernews · randycupertino · Jul 10, 18:26 · [Discussion](https://news.ycombinator.com/item?id=48863464)

**Background**: “Click to cancel” rules are designed to make subscription cancellation as straightforward as signup, so customers can end recurring charges without being forced through confusing steps. The broader regulatory target is often called dark patterns, which are interface or billing tactics that steer users into paying more, staying subscribed, or missing important fee disclosures. Consumer-protection agencies have increasingly focused on these practices because subscriptions are now common across software, media, travel, and retail.

<details><summary>References</summary>
<ul>
<li><a href="https://prosperstack.com/blog/ftc-click-to-cancel/">How to Comply - FTC “ Click to Cancel ” Negative Option Rule</a></li>
<li><a href="https://natlawreview.com/article/new-click-cancel-requirements-welcomenot-welcome">Federal Trade Commission Announces Final Negative Option Rule</a></li>
<li><a href="https://www.ftc.gov/news-events/news/press-releases/2022/09/ftc-report-shows-rise-sophisticated-dark-patterns-designed-trick-trap-consumers">FTC Report Shows Rise in Sophisticated Dark Patterns Designed to Trick and Trap Consumers | Federal Trade Commission</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly supportive of stronger consumer protection, but several questioned whether the rule would be meaningful in practice without clear enforcement and no major carve-outs. Others noted that similar rules already exist in places like California, while sharing real-world complaints about hidden hotel fees and subscriptions that are surprisingly hard to cancel.

**Tags**: `#consumer protection`, `#subscriptions`, `#regulation`, `#dark patterns`, `#policy`

---

<a id="item-8"></a>
## [Nilay Patel on AR Glasses’ Privacy Trade-offs](https://simonwillison.net/2026/Jul/10/nilay-patel/#atom-everything) ⭐️ 7.0/10

Nilay Patel argued on The Vergecast that practical augmented reality glasses require a camera continuously recording what the wearer sees, with data processed in real time to overlay information. He said current hardware cannot fit enough compute into a glasses stem, so the choice is either cloud processing or a bulkier device closer to the size of Vision Pro. The argument highlights a central barrier for AR wearables: the technical path to useful always-on AR may conflict with privacy expectations. That trade-off affects product design, public acceptance, and how companies position future AI-powered glasses in the broader wearables market. Patel framed the issue as a hardware and systems constraint, not just a policy choice: local real-time AR would need compute and power budgets that current glasses-size devices cannot yet provide. The practical alternatives he described are cloud processing or moving the battery and compute elsewhere, both of which raise size, latency, or privacy costs.

rss · Simon Willison · Jul 10, 17:05

**Background**: Augmented reality overlays digital content onto the real world through a display such as a head-mounted device or glasses. For AR glasses to recognize what the wearer is seeing and place information correctly, the device typically needs sensors like cameras and software that can analyze video quickly. Edge AI refers to doing that processing locally on the device, while cloud processing sends data to remote servers; the choice between them matters for speed, battery life, and privacy.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Augmented_reality">Augmented reality - Wikipedia</a></li>
<li><a href="https://www.iotforall.com/edge-ai-wearables">How Edge AI Is Transforming Wearable Devices - IoT For All</a></li>

</ul>
</details>

**Tags**: `#augmented reality`, `#privacy`, `#wearables`, `#edge computing`, `#AI`

---

<a id="item-9"></a>
## [Meta Launches Muse Spark 1.1 API](https://simonwillison.net/2026/Jul/9/muse-spark-1-1/#atom-everything) ⭐️ 7.0/10

Meta released Muse Spark 1.1, the first Spark model available through the new Meta Model API in public preview. The launch includes an evaluation report and claims improvements in agentic tool calling and computer use. This gives developers a new API-accessible model aimed at agentic workflows, which are increasingly important for coding assistants, tool-using agents, and computer-interaction tasks. It also signals that Meta is turning Muse Spark from a showcased model into something builders can actually integrate into products. The announcement says Muse Spark 1.1 is available through the Meta Model API, and the linked evaluation report is where Meta provides more technical detail. Simon Willison also published a CLI and Python access path via the llm-meta-ai plugin, showing that the model can already be used from developer tooling.

rss · Simon Willison · Jul 9, 16:24

**Background**: Muse Spark is Meta's model line for agentic use cases, meaning models that can decide when to call tools or interact with software rather than only generating text. An API release matters because it lets developers build real applications on top of the model instead of only reading about benchmarks or demos. The post also references a playful “self-conversation” experiment from the evaluation report, which highlights how the model behaves when two copies of it interact with each other.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/">Introducing Muse Spark 1.1 - ai.meta.com</a></li>

</ul>
</details>

**Tags**: `#AI models`, `#Meta`, `#agentic tooling`, `#computer use`, `#API release`

---

<a id="item-10"></a>
## [Good Tools Should Fade Into the Background](https://www.gingerbill.org/article/2026/07/10/good-tools-are-invisible/) ⭐️ 6.0/10

The essay "Good Tools Are Invisible" argues that software tools should minimize friction and get out of the way so users can focus on their actual work. It frames "invisible" tools as those that become natural to use, rather than drawing attention to the interface itself. This is relevant to developer tools and UX design because it challenges the idea that exposing more controls or internals is always better. If teams build tools that are easier to use under pressure, they can reduce wasted time, confusion, and workflow interruptions. The piece focuses on friction, muscle memory, and the difference between necessary complexity and unnecessary complexity. It also suggests that what feels "invisible" often comes from repeated use over time, not from removing every advanced feature.

hackernews · theanonymousone · Jul 10, 10:32 · [Discussion](https://news.ycombinator.com/item?id=48858121)

**Background**: In software design, "UX" refers to how easy and efficient a tool is to use, especially for accomplishing real tasks without unnecessary steps. Developer tools are programs used by engineers, such as editors, terminals, and internal systems for teams. The idea behind invisible tools is that good interfaces should support the work so smoothly that the interface itself stops being the user's focus.

**Discussion**: Commenters largely agreed with the essay's core point, especially those who build internal tools or work heavily in terminals and editors. A few added nuance: some friction is necessary for certain tasks, and some features only become "invisible" after enough practice and muscle memory.

**Tags**: `#developer-tools`, `#user-experience`, `#productivity`, `#software-design`, `#hacker-news`

---

<a id="item-11"></a>
## [Late Bronze Age Collapse overview](https://acoup.blog/2026/01/30/collections-the-late-bronze-age-collapse-a-very-brief-introduction/) ⭐️ 6.0/10

A Hacker News discussion highlighted a brief introduction to the Late Bronze Age Collapse, drawing in a large comment thread of 225 replies. The conversation centered on historians’ interpretations of the collapse and on modern systems-collapse analogies. The Late Bronze Age Collapse is a widely used historical case study for how interconnected societies can fail under combined pressures. Its popularity in the discussion shows that it still resonates with readers interested in civilization fragility, trade dependence, and collapse dynamics. Web references place the collapse in the late 13th to early 12th century BC and note that it affected much of the Eastern Mediterranean and Near East, including Egypt, Anatolia, the Aegean, and the Levant. Commenters also pointed to historian Eric H. Cline’s view that the crisis was driven by interconnected failures rather than a single cause, with trade-route disruption playing a major role.

hackernews · dmonay · Jul 10, 11:59 · [Discussion](https://news.ycombinator.com/item?id=48858737)

**Background**: The Late Bronze Age was a period when major powers around the Mediterranean were tightly linked by diplomacy, trade, and shared materials such as bronze. Bronze production depended on copper and the scarcer tin, so long-distance exchange networks mattered a great deal. Historians debate the collapse because it did not look like one clean event; instead, multiple kingdoms and cities declined or fell over a relatively short period. That uncertainty is part of why the topic is often discussed in terms of 'systems collapse.'

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Late_Bronze_Age_collapse">Late Bronze Age collapse - Wikipedia</a></li>
<li><a href="https://www.worldhistory.org/Bronze_Age_Collapse/">Bronze Age Collapse - World History Encyclopedia</a></li>
<li><a href="https://www.jstor.org/stable/10.3764/aja.120.1.0099">Crisis in Context: The End of the Late Bronze Age in ... - JSTOR</a></li>

</ul>
</details>

**Discussion**: The comments were broadly fascinated and speculative, with several users connecting the collapse to modern analogies like AI risk, oil dependence, and fragile supply networks. Others added historical context, citing Eric H. Cline and Patrick Wyman, while one commenter joked about divine causes, reflecting the thread’s mix of seriousness and humor.

**Tags**: `#history`, `#civilization collapse`, `#archaeology`, `#Hacker News`, `#systems thinking`

---

<a id="item-12"></a>
## [ML Submission Caps Debate](https://www.reddit.com/r/MachineLearning/comments/1usq43t/why_doesnt_the_ml_research_community_limit_the/) ⭐️ 6.0/10

A Reddit post in r/MachineLearning asks why the ML research community does not cap the number of submissions per author, arguing that high submission volume is hurting review quality. The poster points to ARR cycles and compares ML with fields like Security and Computer Architecture, where submission limits are sometimes used to manage reviewer workload. This is a process and policy issue rather than a technical breakthrough, but it touches the quality and scalability of peer review across ML conferences. If submission pressure keeps rising, it can affect authors, reviewers, and the credibility of conference decisions. The post specifically references ARR, which runs peer review in two-month cycles and can send revised papers into later cycles with the same or different reviewers. The comparison examples include DAC's limit of five submissions for technical program committee members and CCS's rule that an individual may not be an author on more than 20 research manuscripts.

reddit · r/MachineLearning · /u/alafaya101 · Jul 10, 14:59

**Background**: In machine learning, conferences often function as the main publication venue, so submission volume can become very large. ARR, or ACL Rolling Review, is a review platform used in the ACL ecosystem and adopted by some conferences as part of a two-stage process: papers are reviewed in ARR first, then committed to a specific conference for final decision. Submission limits in other fields are sometimes used to reduce reviewer overload and keep the process manageable.

<details><summary>References</summary>
<ul>
<li><a href="https://aclrollingreview.org/">ACL Rolling Review – A peer review platform for the Association for...</a></li>
<li><a href="https://ccspub.org/sub.html">Submission Guidelines | CCS Publishing</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#peer review`, `#research policy`, `#conference submissions`, `#academic publishing`

---

<a id="item-13"></a>
## [Critic-Based Attacks Beat Actor-Based in Multi-Agent PPO](https://www.reddit.com/r/MachineLearning/comments/1usx96p/on_adversarial_rl_r/) ⭐️ 6.0/10

A Reddit user reports that, in their multi-agent PPO experiments on VMAS scenarios, critic-based adversarial perturbations are consistently stronger than actor-based ones, which appears opposite to the expectation described by Zhang et al.'s 2020 SA-MDP framework. They ask whether this is a bug, a consequence of adapting PGD to continuous policies with KL divergence, or simply a difference between single-agent and multi-agent settings. This matters because the answer affects how researchers evaluate robustness in multi-agent reinforcement learning and which network is the more effective target for adversarial attacks. If critic-based attacks can be stronger in practice, then assumptions from single-agent SA-MDP analyses may not transfer cleanly to multi-agent PPO systems. The post specifically mentions IPPO and GPPO, including heterogeneous variants, and says the attack is a PGD-style method adapted to continuous policies via the closed-form KL divergence. The claim is not a published result, but a comparison based on experiments by a single user, so it should be treated as an open technical question rather than a settled conclusion.

reddit · r/MachineLearning · /u/ham_bam0 · Jul 10, 19:15

**Background**: SA-MDP stands for state-adversarial Markov decision process, a framework for reasoning about adversarial perturbations to observations in reinforcement learning. In this context, the actor network outputs the policy c0(s), while the critic network estimates value with V(s), and the question is which one provides a more effective signal for constructing observation attacks. PPO is a common policy-gradient algorithm, and in multi-agent variants such as IPPO and GPPO, each agent may be trained independently or with graph-based structure, which can change how perturbations propagate across agents.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.stackexchange.com/questions/50666/critic-based-adversarial-attacks-unexpectedly-outperform-actor-based-attacks-in">Critic-based adversarial attacks unexpectedly outperform actor-based...</a></li>
<li><a href="https://learn.arena.education/chapter2_rl/03_ppo/bonus/">Chapter 2: Reinforcement Learning - ARENA</a></li>

</ul>
</details>

**Tags**: `#adversarial-rl`, `#reinforcement-learning`, `#multi-agent-rl`, `#ppo`, `#robustness`

---

<a id="item-14"></a>
## [Talos-XII Rust Gacha Simulator](https://www.reddit.com/r/MachineLearning/comments/1urvxgb/talosxii_handwritten_autograd_small_rlmlp_stack/) ⭐️ 6.0/10

Talos-XII is a Rust CLI simulator for Arknights: Endfield gacha probability modeling that uses a hand-written autograd engine and small neural models instead of PyTorch, tch-rs, or ndarray. It trains on first run, caches the models locally, and also includes benchmark tooling for different CPU and GPU setups. The project is notable because it combines systems programming, custom ML infrastructure, and a niche simulation problem in a single static Rust binary. It may be useful to developers who want to study lightweight on-device inference, custom autograd design, or performance tradeoffs across CPU architectures. The codebase includes an EnvNet MLP, a Luck Optimizer over a 32-dimensional feature vector, a Dueling DQN, and a PPO actor-critic with an MLA transformer for strategy selection. It also reports runtime SIMD dispatch from scalar up to AVX-512 and NEON, Rayon-parallelized simulations, BF16 inference caches, and an optional PyO3 bridge for Python scripting.

reddit · r/MachineLearning · /u/zay0kami · Jul 9, 16:52

**Background**: Autograd, short for automatic differentiation, is a technique that computes gradients needed for training neural networks without manually deriving derivatives. Rust projects sometimes implement these pieces from scratch when they want tighter control over memory layout, performance, or binary deployment than mainstream ML frameworks provide. The gacha problem here refers to estimating probabilities and decision policies in a randomized pull system, where concepts like pity count and rate-up units affect expected outcomes.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/hodulabs/kurumi">GitHub - hodulabs/kurumi: Tensor and autograd engine in Rust ...</a></li>
<li><a href="https://github.com/ThalesMMS/Rust-Neural-Networks/blob/main/docs/tutorials/05_autograd_engine.md">Rust-Neural-Networks/docs/tutorials/05_autograd_engine.md at ...</a></li>

</ul>
</details>

**Tags**: `#Rust`, `#autograd`, `#reinforcement learning`, `#machine learning infrastructure`, `#simulation`

---

<a id="item-15"></a>
## [IMGNet swaps cosine for sign-pattern face matching](https://www.reddit.com/r/MachineLearning/comments/1urxvxh/i_built_imgnet_a_face_verification_model_that/) ⭐️ 6.0/10

An independent researcher introduced IMGNet, a compact face verification model that compares embeddings with sliding-window sign pattern matching instead of cosine similarity. The post reports 96.27% on LFW with a 10.58 MB model trained on CASIA-WebFace, and 99.58% on LFW when IMG Sign Score is applied to ArcFace embeddings without retraining. Face verification systems typically rely on embedding comparisons, and cosine similarity is a common default metric for that task. If sign-pattern matching proves robust, it could offer an alternative way to align training objectives and inference metrics for compact vision models. IMGNet's SW Block replaces a standard convolution with multi-scale relational processing over prime window sizes {3, 5, 7}, and the author says the sign-based loss is designed to ignore amplitude. The post also introduces three scores that share one threshold and a 2/3-or-3/3 voting scheme, while noting that the occlusion-based spatial-organization observation is still preliminary and not formally validated.

reddit · r/MachineLearning · /u/img-_- · Jul 9, 18:00

**Background**: Face verification asks whether two face images belong to the same person, while face recognition identifies who someone is. In modern systems, a neural network first turns each face into an embedding, then a similarity metric such as cosine similarity decides whether the embeddings match. The idea in this post is to replace that final comparison rule with a pattern-based score over local windows of the embedding.

<details><summary>References</summary>
<ul>
<li><a href="https://hackernoon.com/id-verification-with-deep-learning-7bae0a5dffd8">ID verification pipeline with deep learning | HackerNoon</a></li>
<li><a href="https://www.iproov.com/blog/face-recognition-face-verification-whats-the-difference">Face Verification vs Facial Recognition Difference [2026]</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#face-verification`, `#computer-vision`, `#embeddings`, `#research`

---