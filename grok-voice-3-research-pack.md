# Research Pack: "Grok Voice 3.0 Is Answering Customer Calls—Would You Trust It?"
Prepared 2026-10-15 (Asia/Taipei). For a 3–5 min English explainer with a 2D illustrated presenter. **No original product recordings, customer-call audio, or hands-on tests exist for this project, and none are implied below.**

> Naming note: the company now calls itself **SpaceXSI** (formerly xAI; SpaceX absorbed xAI in Feb 2026 per PCMag). Official pages still live at x.ai / docs.x.ai. In this pack, "xAI" = SpaceXSI.

---
## A. Executive brief: what a customer most needs to understand

1. **The 70% figure is the company's own number, and the other 30% is what you should care about.** xAI says Starlink's Grok Voice line takes about 20,000 calls a day and settles about 70% "with no human in the loop" ([x.ai/news/grok-voice-3](https://x.ai/news/grok-voice-3)). Nobody outside the company has audited that. xAI also published the same ~70% back in April 2026 for Grok Voice 1.0 ([x.ai/news/grok-voice-think-fast-1](https://x.ai/news/grok-voice-think-fast-1)), so it isn't a new result tied to 3.0. Independent benchmarks (Artificial Analysis) do rank Grok Voice 3.0 #1 on their composite speech index. But those are **simulated** support calls, and on the hardest simulated-support test (τ-Voice) it gets 71.6%: roughly 3 in 10 simulated tasks still fail. On that test it is *not* first (OpenAI's GPT-Live-1 Astra scores 74.5%) ([artificialanalysis.ai/speech-to-speech](https://artificialanalysis.ai/speech-to-speech)).
2. **Whether you can reach a human isn't set by the model. Each company that deploys it decides.** xAI's tools *let* businesses add a "transfer_to_human" action or a SIP call transfer ([x.ai/voice](https://x.ai/voice); [docs.x.ai voice REST reference](https://docs.x.ai/developers/rest-api-reference/inference/voice)). In tutorials it's a checkbox the builder can switch off (Tech Tomlet answered "No" to the transfer question on camera; item V11). At Starlink, a PCMag reporter in April 2026, before 3.0, found the AI offered a **scheduled human callback**, not a live transfer, and a human rang back in 5 minutes ([PCMag](https://www.pcmag.com/news/hi-this-is-ai-starlinks-customer-support-now-features-grok-voice-chatbot)). The practical advice to customers: ask for a human clearly and early. Whether you get one depends on the company, not on "Grok."

---
## B. Research inventory

### Honest counts
| Type | Analyzed | How accessed |
|---|---|---|
| Videos | **27** | **Transcript read** (YouTube caption tracks pulled with `youtube-transcript-api`). I didn't *watch* any of the videos, so visual-only content (charts, UI) is not verified. For videos over 15 min I read the transcript **in part**: opening sections, plus keyword search for human/handoff/escalate/frustration/trust. |
| X posts/threads | **12** | Post read (X API full text; some long posts truncated by the API, noted) |
| Reddit | **0** | Reddit blocked every route I tried (WebFetch: "blocked by network security"; curl JSON and old.reddit: blocked or redirected). The thread titles I saw in search results are listed in Gaps and **not counted**. |
| **Total** | **39** | |

**Not counted:** 4 videos found but excluded.
- OPtmFcHNyOs (IBM): no transcript available.
- gl7kpICvExE (Tech2Fast): YouTube IP-blocked the transcript request.
- 0JLPp_ax15Q (DennisCW): Tesla custom connectors, not about customer support.
- XcI5IMLEAaE (YC/Pylon): founder story, off-topic.

The x.ai launch post, the docs, Artificial Analysis, PCMag, SiliconANGLE and Gartner are **fact-check sources**. They are in the Claim Ledger (D), not in this inventory.

Column key: **Verify?** = do its claims need independent verification? (Y/N/Partly)

### B1. Videos (27)
| # | Title / URL | Creator | Date | Access | Summary (original) | Most relevant viewer question | Useful timestamp | Verify? |
|---|---|---|---|---|---|---|---|---|
|V1|[Grok Voice 3: how fast can an AI voice agent answer a support call?](https://www.youtube.com/watch?v=Kj-kyXOEkek)|Stepwise|2026-10-14|Transcript read (full)|Narrates an illustrated router-outage call and walks through barge-in, tool use and the ~0.81 s first-audio figure. Flags that 2.0 was actually slightly faster (~0.7 s) and that xAI's "record for resolving support calls" names no test.|Is it actually faster than before?|1:26 (speed vs 2.0); 2:06 (unnamed "record")|Partly (cites AA; matches AA table)|
|V2|[How to Access SpaceXSI AI Frontier Grok Voice 3.0 Model](https://www.youtube.com/watch?v=ki3MfDmA-Tw)|Reality PC|2026-10-15|Transcript read (full)|Reads through the launch post with skeptical commentary. Interprets "70% no human" as no escalation to a supervisor and raises job-replacement worries about $4.80/hr pricing.|Will this replace human agents?|3:23 (70% interpretation); 4:45 (jobs)|Y (opinion)|
|V3|[Grok Voice 3.0 Is #1 on Tests. So Why Do People Prefer Google's?](https://www.youtube.com/watch?v=Os80lGvR3AA)|Simply AI|2026-10-14|Transcript read (full)|Explains speech-to-speech vs cascaded pipelines. Points out that in AA's blind listener vote Google voices edge out Grok, and that xAI's chart compares against a less-preferred Gemini variant. Notes the 70% Starlink figure was reported two versions ago, nobody outside has checked it, and the regular Grok app isn't on xAI's availability list.|Do people actually *prefer* talking to it?|0:42 (app availability); 3:28–4:49 (arena vote); 5:30 (70% not new)|Partly (arena claim confirmed vs AA table)|
|V4|[Grok Voice 3.0: Elon Musk presenta la IA de voz más inteligente](https://www.youtube.com/watch?v=SUsi0csSUzw)|LLM Master|2026-10-14|Transcript read (English caption track of a Spanish video; may be auto-translated)|Spanish-language walkthrough of the launch post followed by a console test call. In the test, the agent declines to take card details and points the caller to the website.|Will it handle payments or send me elsewhere?|7:34–8:55 (test call)|Y|
|V5|[Grok Voice ThinkFast 1 Explained](https://www.youtube.com/watch?v=YgKZKnzASvg)|Alex Hitt|2026-04-24|Transcript read (full)|Explains why delays over ~500 ms break the feel of a conversation and how xAI says it masks tool calls behind speech. Treats the Starlink deployment uncritically.|Why do AI calls feel awkward and slow?|0:00–0:42 (latency threshold); 8:11 (Starlink)|Y (promotional tone)|
|V6|[Introducing Grok Voice Agent Builder](https://www.youtube.com/watch?v=W34FDMm1nCk)|Grok (official)|2026-07-02|Transcript read (full)|46-second official promo: build an agent in about 2 minutes, clone voices, get a free number, 25 languages, "5 cents per minute."|How easy is it for any business to deploy?|0:00–0:46|Y (vendor; price differs from API's $0.08/min)|
|V7|[Grok Voice API Demo: Build Voice Agents with xAI & LiveKit](https://www.youtube.com/watch?v=4IGnr08CkB4)|LiveKit|2025-12-17|Transcript read (full)|Partner demo of the earlier Grok voice API: emotional range, 100+ languages, function calling, and a 4-line integration. Suggests healthcare and therapy as uses.|Can it sense my tone?|2:01; 2:42 (empathy claims)|Y (vendor/partner)|
|V8|[Grok Voice Agent API Review](https://www.youtube.com/watch?v=3LGPw4gLwwY)|The West Reviews|2025-12-22|Transcript read (full)|Short, generic overview of the 2025 API: about 5¢/min connection pricing and OpenAI Realtime compatibility. Mentions "occasional context or personalization quirks."|Is it reliable?|1:20|Y|
|V9|[Grok Voice Agents Are INSANE!](https://www.youtube.com/watch?v=0g5X6T0CpLg)|Brendan Jowett|2026-04-28|Transcript read (partial + keyword)|Builds a shopping voice agent with Replit that navigates a mock store by voice. Admits openly that the first build didn't work.|Does it work first time?|~7:24 (first build fails)|Partly|
|V10|[How to create AI receptionist with phone number in 2 minutes (grok platform)](https://www.youtube.com/watch?v=JtF2IhTNiOk)|CloudYeti|2026-08-31|Transcript read (full)|Builds a Grok voice agent with web search and a "transfer to human" option in the xAI console. On the live call, asking for a human produced an odd "please enter your password" prompt, which the creator blames on his test setup.|When I ask for a human, what actually happens?|1:20–2:02 (transfer setup); 4:45–5:26 (transfer attempt)|Y|
|V11|[Grok Voice: The Complete Guide](https://www.youtube.com/watch?v=y6DensdKvFQ)|Tech Tomlet|2026-07-19|Transcript read (partial + keyword)|Long builder tutorial. In setup, the "transfer calls to a human?" question is answered "No," showing that handoff is optional. Concludes the platform is "nowhere near production ready" because testing tools are limited.|Can businesses skip the human option?|setup section (transfer = No); 22:26 (not production ready)|N (first-hand opinion)|
|V12|[Best AI Voice Agents for Customer Service 2026: 10 Ranked by Handoff](https://www.youtube.com/watch?v=2FvjcSwogvw)|JustCall|2026-10-14|Transcript read (full)|Ranks vendors by how they hand callers to humans, opening with Gartner's 64% / 53% survey stats. Explains warm handoff with a summary versus a cold transfer. Vendor-made and self-ranked #1.|Will the human know what I already said?|0:00–0:41 (Gartner); throughout (warm transfer)|Partly (Gartner verified; rankings are vendor opinion)|
|V13|[Escalating Voice AI Calls Properly](https://www.youtube.com/watch?v=vOlxHgaFFpU)|Voice AI with Tim|2026-02-16|Transcript read (partial + keyword)|Proposes a "HELP" checklist for when to escalate: explicit request, emotional change, legal limits, permission limits. Argues that ignoring a request for a human "destroys trust."|When *should* the AI hand me to a person?|0:40–2:42|N (framework/opinion)|
|V14|[Give Your Amazon Connect AI Agent a Human Handoff (With Full Context)](https://www.youtube.com/watch?v=gwj0Wcgd9o0)|Tech With Kobina|2026-08-20|Transcript read (partial + keyword)|Configures an escalation tool that passes a summary to the human agent, triggered by explicit requests, repeated tool failures or frustration.|Will I have to repeat myself?|2:04 (triggers)|N|
|V15|[AI Voice Agent to Live Agent Transfer](https://www.youtube.com/watch?v=jATOzux_wwc)|ICTContact|2026-09-02|Transcript read (full)|Vendor demo: the AI takes the routine part, the caller asks for a person, and the call moves to a live agent in the same workflow.|What does a smooth handoff sound like?|0:41–1:22|Y (vendor demo)|
|V16|[How Assembled's AI voice agent handles support calls](https://www.youtube.com/watch?v=sV1uKTyUO2s)|Assembled|2026-02-10|Transcript read (full)|Live demo of identity verification, a subscription change and then a request for a person. Shows the call summary handed to the human team in Zendesk.|Does the AI verify me safely?|0:40 (ID check); 2:00–3:20 (handoff + summary)|Y (vendor)|
|V17|[Warm Transfer Setup Tutorial (Cold vs Warm)](https://www.youtube.com/watch?v=VaUipyej8Zw)|SigmaMind AI|2026-02-06|Transcript read (full)|Defines a cold transfer (no context, AI drops off) versus a warm transfer (whisper briefing to the agent, then a three-way intro), with automatic retry if the transfer fails.|What's the difference between a good and bad transfer?|0:00–2:43|N|
|V18|[The Right Way to Handoff Calls in Voice Agents](https://www.youtube.com/watch?v=HEhNvsn8CxQ)|Martí Blanes|2026-03-31|Transcript read (full)|Argues the best agent knows when to stop, and that handoff should be treated as a feature, not a failure. Lists triggers: frustration, repetition, out-of-scope requests, low confidence, failed tools.|Is it a failure when the AI passes me on?|0:00–2:01|N|
|V19|[AI phone support that actually sounds human: Meet Fin Voice](https://www.youtube.com/watch?v=XneynoZTFyk)|Fin (Intercom)|2025-04-01|Transcript read (full)|Competitor demo of an order change with an interruption and a language switch. Names latency, interruptions and hallucinations as the hard problems on the phone.|Can it handle me interrupting?|0:00–0:41 (problems); 1:22–2:05 (interruption)|Y (vendor)|
|V20|[The AI Customer Service Boom](https://www.youtube.com/watch?v=-6EiO5_Ixdg)|Fortune Magazine|2026-06-25|Transcript read (auto captions fragmentary)|Journalistic look at AI call centers, including a Hertz voice agent that routes risky situations (a flat tire on the road) to humans. Cites consumer surveys showing a strong preference for humans. Covers hallucination guardrails and the Air Canada chatbot case.|What happens in an emergency?|6:56–7:38 (Hertz safety handoff); 8:20 (Air Canada)|Partly (survey stats not traced)|
|V21|[fire your AI customer service bot](https://www.youtube.com/watch?v=cG-5xp5pxGk)|Swell Entertainment|2026-05-12|Transcript read (partial + keyword)|Former customer-service lead's commentary: bots loop, repeat themselves, and turn 5-minute issues into long ordeals. Argues humans make intuitive leaps that bots can't.|Why do bots make simple things harder?|~4:46|N (opinion)|
|V22|[Top AI use cases in the contact centre](https://www.youtube.com/watch?v=xjVa_YMTqLU)|VUX World|2024-02-09|Transcript read (full)|Industry overview: self-service, post-call summaries, conversation analytics and agent assist. Positions AI as a helper to human agents, not only a replacement.|Is the AI replacing the agent or helping them?|2:42–4:43|N|
|V23|[Will AI REPLACE customer support teams?](https://www.youtube.com/watch?v=kDhdUEHvaFA)|Customer Success Collective|2025-02-26|Transcript read (full)|Traces the path from phone menus to chatbots to language-understanding AI. Raises privacy, the right to know you're talking to AI, and job displacement.|Do I have a right to know it's AI?|3:21–4:01|N|
|V24|[AI Agents for Customer Service with Latane Conant](https://www.youtube.com/watch?v=pBrCB-BC2dU)|Business Intelligence Group|2026-05-14|Transcript read (partial + keyword)|Parloa executive cites the company's mystery-shopper research: chatbots resolved 8% of issues and handed off correctly 8% of the time, 96% of enterprises still use phone menus, and wait times reached 90 minutes. Criticizes "contain, contain, contain" thinking.|Why is phone support so bad today?|8:10–9:32; 28:29|Y (company research, not public)|
|V25|[What If Your Customer Service Never Needed a Human?](https://www.youtube.com/watch?v=15VjN3taUJI)|Everdial AI (titled Celestris)|2026-10-06|Transcript read (full)|A 1:44 promo promising zero wait times and 24/7 answers. Useful as an example of the "no human needed" sales pitch.|Is "never needs a human" realistic?|0:00–0:42|Y (marketing)|
|V26|[How to Make an AI Customer Support Phone Line in 3 Minutes](https://www.youtube.com/watch?v=8K1z-5-74w8)|Liam Ottley|2024-03-30|Transcript read (full)|Builds a knowledge-base phone agent with a fallback line for unknown answers. Shows how little setup a basic support line needs.|Who builds these bots, and how carefully?|1:22 (fallback); 2:42 (demo call)|N|
|V27|[5 AI Tools That Will Separate Winners From Losers in Customer Support](https://www.youtube.com/watch?v=Dkio6U4k2PY)|Edwin Chen|2026-01-07|Transcript read (partial)|Agency owner compares support-AI vendors on pricing and resolution claims, and warns that generic AI voices can hurt brands.|Will every company's bot sound the same?|1:20–2:41|Y (vendor claims repeated)|

### B2. X posts/threads (12)
| # | URL | Author | Date (UTC) | Access | Summary (original) | Viewer question | Location | Verify? |
|---|---|---|---|---|---|---|---|---|
|X1|https://x.com/malkorex/status/2110435918834479293|@malkorex|2026-10-14|Post read|Reply to @spacexai pointing out that the launch chart omits τ-Voice, where GPT-Live-1 Astra (74.5%) beats Grok (71.6%), and that 94.8% "task success" comes from a different test, so it doesn't mean 95% of real calls are solved.|Does "94.8%" mean 95% of my calls get fixed?|reply to launch post|Verified against AA table|
|X2|https://x.com/AIRoboticsInt/status/2110505612450902156 (+ [2110492610439835914](https://x.com/AIRoboticsInt/status/2110492610439835914))|@AIRoboticsInt (Josh Marino)|2026-10-14|Post read (2-post self-thread, counted once)|Individual set up a Grok Voice 3 agent to screen his personal calls. Urgent and family calls get transferred; a caller probing for his home address was refused. Notes there is no transcript API.|Can it tell an urgent call from a routine one?|both posts|Y (anecdote)|
|X3|https://x.com/david04652302/status/2110563598946664834|@david04652302|2026-10-15|Post read|Wonders whether the new model will stop an older widow from hanging up because she doesn't want to deal with AI at all.|What about people who won't talk to a bot?|reply to @spacexai|N (opinion)|
|X4|https://x.com/DavidTranAI/status/2110488985722368160|@DavidTranAI|2026-10-14|Post read|Early user says ElevenLabs still sounds most human to him, but Grok Voice 3 might become his daily driver.|Does it sound human?|reply to @elonmusk|N (opinion)|
|X5|https://x.com/mellmango/status/2110557041307595209|@mellmango|2026-10-15|Post read (truncated by API)|Developer argues GPT-Live-1's sticker price hides a second "delegated" model cost, so the real gap with Grok is bigger than charts show.|Is the cheap price real?|reply|Y|
|X6|https://x.com/thecsguy/status/2110499106041053345 (+ replies from [@yesadok](https://x.com/yesadok/status/2110522821571129733) and [@joshdbirdwell](https://x.com/joshdbirdwell/status/2110500508796408209))|@thecsguy + repliers|2026-10-14|Post read (thread)|Asks: a really good AI agent now, or a 20-minute wait for a person? Repliers prefer the AI; one jokes he'd rather his own bot talk to theirs.|AI now vs human later: which would I pick?|thread|N (opinion)|
|X7|https://x.com/antiviral_mktng/status/2099612757528133906|@antiviral_mktng|2026-09-14|Post read|Customer story (company not named): the voice agent was useless, a human was a 30-minute wait, then chat was another bot with a 60-minute human queue.|What if the human queue is still long?|post|N (anecdote)|
|X8|https://x.com/jayjonsun/status/2104356412226744703|@jayjonsun|2026-09-27|Post read|Tells @Xfinity its AI agent is fine for simple questions but weak at troubleshooting, and complains there's no way to reach a human.|Is it OK for simple vs complex problems?|reply to @Xfinity|N|
|X9|https://x.com/beecheorii/status/2101057148897612174|@beecheorii|2026-09-18|Post read|Cash App caller found the AI agent so lifelike, with background sounds, that it felt creepy, and hung up.|Should it tell me it's AI?|post|N|
|X10|https://x.com/Bas3dPhilosophy/status/2105709854405087577|@Bas3dPhilosophy|2026-10-01|Post read (truncated)|Opposing view: says fully AI support beats human agents, who often misunderstand the problem.|Can AI be *better* than a person?|reply|N|
|X11|https://x.com/Dat_von_guy/status/2094849262177894807|@Dat_von_guy|2026-09-01|Post read|Tells @Rogers its AI phone assistant doesn't help and can't be skipped to reach a person.|Can I skip the bot?|reply to @Rogers|N|
|X12|https://x.com/shawnchauhan1/status/2092590409742717384|@shawnchauhan1|2026-08-26|Post read (truncated by API)|Notes Starlink routes about 15,000 calls a day through one AI agent with "no human in the loop," calling it impressive but "a single point of…" (failure; the text is cut off).|What if the one AI system fails?|post|Y (15k figure differs from the current 20k)|

---
## C. Audience-insight synthesis
| Insight | Supporting items |
|---|---|
|**Hope: no hold queue.** Speed and 24/7 answers are the main pull. Some would rather take a good AI now than a human in 20 minutes.|V1, V5, V25, X6, X10, V24 (90-min waits)|
|**Fear #1: being trapped with no exit to a human.** This is the most repeated complaint.|X7, X8, X11, V21, V13 ("destroys trust"), V12 (Gartner: top concern is reaching a person)|
|**Fear #2: having to repeat my story after the transfer.** Experts answer with warm handoffs and summaries.|V24 (context lost), V14, V16, V17, V12|
|**Fear #3: confident wrong answers.**|V20 (Air Canada case), V11 ("I don't know" fallback), V26, V19|
|**Fear #4: it's creepy or deceptive if I can't tell it's AI.** Disclosure matters.|X9, V23, PCMag (AI disclosed itself when asked)|
|**Fear #5: jobs and companies just cutting costs.**|V2, V24 ("contain, contain"), V21, V20|
|**Disagreement: do benchmarks = good calls?** Lab #1 rank vs listener preference and the τ-Voice gap.|V3, X1, V1, X4|
|**Disagreement: is AI better or worse than human agents?**|X10, X6 vs X7, X8, V21|
|**Nuance: AI is OK for simple tasks, weaker at messy troubleshooting.**|X8, V18, V13, V20 (Hertz routes safety issues to humans)|
|**Nuance: some people won't engage with a bot at all** (older or less tech-comfortable callers). Notably, xAI's own Starlink story says many callers are "older, rural, and phone-native."|X3, [x.ai/stories/starlink](https://x.ai/stories/starlink)|
|**Builder reality: the handoff is a setting, not a guarantee.**|V10, V11, V6, V13|

**Likely viewer questions:** Is that a real person? How do I get a human? Will the human know what I already said? Can it give me a refund or credit? What if it gets it wrong? Is my call recorded or used for training? Does the Grok app on my phone use this?

The search phrasing comes from consumer guides (e.g., ConsumerAffairs "Stuck with an AI bot? Clever ways to reach a human") and Reddit thread titles seen in search. **Autocomplete was not checked for this pack.**

---
## D. Claim ledger
| # | Claim | Class | Primary source | Date | Evidence | Uncertainty | Script-safe wording |
|---|---|---|---|---|---|---|---|
|1|Grok Voice 3.0 released|Verifiable fact|[x.ai/news/grok-voice-3](https://x.ai/news/grok-voice-3); [SiliconANGLE](https://siliconangle.com/2026/10/14/grok-voice-3-0-from-spacexsi-outscores-openai-and-google-on-speech-to-speech-index/)|Oct 14, 2026 (US); Oct 15 Taipei|SiliconANGLE dated Oct 14 EDT; AA data dated Oct 13|The fetched launch page shows no dateline|"Announced October 14, 2026."|
|2|Available in the Voice Agent API at $0.08/min ($4.80/hr), same as 2.0; `grok-voice-latest` auto-switched|xAI claim (pricing; reliable)|launch post|Oct 14|Launch post text; AA lists 4.80/hr|Docs page didn't render the price; the Builder promo (V6, Jul 2026) said 5¢/min, so a different product or tier is possible|"xAI lists it at 8 cents a minute for developers."|
|3|Who has it: Voice Agent API customers, Tesla in-car voice, Grok Bot voice mode|xAI claim|launch post|Oct 14|Launch post names only these|The regular Grok app isn't named; don't assume every Grok user has 3.0|"xAI says it powers Tesla's in-car voice, Grok Bot voice mode, and businesses using its API."|
|4|#1 on AA Speech-to-Speech Index, 86.9 (GPT-Live-1 Astra 83.2; Gemini 3.8 Live Ext. Thinking 82.6)|Independently verifiable|[AA speech-to-speech](https://artificialanalysis.ai/speech-to-speech); [methodology](https://artificialanalysis.ai/methodology/speech-to-speech-benchmarking)|AA table fetched Oct 15|AA table matches|Index is a composite of simulated tests plus listener votes|"An independent lab, Artificial Analysis, currently ranks it first on its combined voice-AI score."|
|5|τ-Voice (simulated support calls) 71.6%; GPT-Live-1 Astra 74.5%; Grok 2.0 56.5%|Verifiable|AA table|Oct 15|AA table|Simulated callers; AA notes GPT-Live-1 is based on 1 trial|"In simulated support calls, it solved about 7 in 10, a big jump from the last version, but not the top score."|
|6|Arena preference Elo 1070, tied with Gemini 3.1 Flash Live High and below Gemini 3.8 Live (1088) and Gemini 3.1 Flash Live Minimal (1100)|Verifiable|AA table|Oct 15|AA table; xAI's own chart shows only weaker comparisons (Gemini Ext. Thinking 990)|xAI's chart values (1048, 990) differ slightly from the AA live table; AA freezes Elo for the index|"In blind listening votes, some Google voices were preferred."|
|7|Time to first audio 0.81 s (2.0: 0.70 s)|Verifiable|AA table|Oct 15|AA|Lab measurement, not over phone lines|"It starts answering in under a second in lab tests."|
|8|"Sets a new record for resolving customer support calls"|xAI claim, unsupported|launch post|Oct 14|No test named (also flagged by V1)|Unclear basis|**Avoid** or attribute: "xAI claims a record, without saying which test."|
|9|EVA-Bench (ServiceNow) top accuracy 74%; best combined accuracy + experience|xAI claim + partner quote|launch post; [ServiceNow/eva GitHub](https://github.com/ServiceNow/eva); [arXiv](https://arxiv.org/pdf/2605.13841v3)|Oct 14|The benchmark is real and open source (213 scenarios). I found no public ServiceNow leaderboard entry for Grok 3.0.|Result not independently published|"xAI says it led ServiceNow's voice-agent test."|
|10|Starlink: ~20,000 calls/day; ~70% resolved without a human; 1 in 4 sales calls buy|xAI case study (company-reported)|launch post; [x.ai/stories/starlink](https://x.ai/stories/starlink)|Oct 14 (story Aug)|Story: "Voice containment sits around 70%"; English sales conversion ~24.5%|Not audited. "Containment" may mean the call didn't reach a human, not that the problem was solved. Same 70% claimed in April for v1.0.|"xAI *says* about 70% of Starlink's support calls end without a human. That's the company's own figure."|
|11|70% figure predates 3.0|Verifiable (xAI's own archive)|[x.ai/news/grok-voice-think-fast-1](https://x.ai/news/grok-voice-think-fast-1)|Apr 23, 2026|v1.0 post: "70% resolution rate," 20% conversion|—|"xAI reported that same 70% back in April, two versions ago."|
|12|The Starlink agent verifies customers, troubleshoots hardware, issues credits, ships replacements|xAI case study|launch post; Starlink story|Oct 14|Company description|Not observed by us|"According to xAI, the Starlink agent can…"|
|13|Starlink AI offers a human **callback**; a reporter got a human call in 5 min|Independent reporting (single test, pre-3.0)|[PCMag, Michael Kan](https://www.pcmag.com/news/hi-this-is-ai-starlinks-customer-support-now-features-grok-voice-chatbot)|Apr 13, 2026|Reporter's own call; the AI disclosed it was AI when asked|One call, older model version; current behavior unknown|"In April, a PCMag reporter asked for a human and was offered a callback."|
|14|Businesses can add human transfer (transfer_to_human tool; SIP REFER endpoint)|Verifiable (docs)|[x.ai/voice](https://x.ai/voice); [docs REST voice](https://docs.x.ai/developers/rest-api-reference/inference/voice)|accessed Oct 15|Docs/marketing|Optional per business (V10, V11)|"The tools let a company send you to a person, if the company sets it up."|
|15|"Millions of conversations a day" in Tesla vehicles|xAI claim|launch post|Oct 14|None independent|Unverified|"xAI says…"|
|16|Audio "processed in real time and never stored or used for training"; SOC 2 / HIPAA-eligible|xAI claim (API docs)|[docs.x.ai voice guide](https://docs.x.ai/docs/guides/voice)|accessed Oct 15|Docs text|Applies to xAI's API processing; the deploying company (e.g., Starlink) may record calls under its own policy|Avoid broad privacy promises; "xAI says its API doesn't store audio; the company you call may still record."|
|17|64% of customers would prefer companies not use AI for service; 53% would consider switching; 60% fear it's harder to reach a human|Independent survey|[Gartner press release](https://www.gartner.com/en/newsroom/press-releases/2024-07-09-gartner-survey-finds-64-percent-of-customers-would-prefer-that-companies-didnt-use-ai-for-customer-service); [The Register](https://www.theregister.com/on-prem/2024/07/09/64-of-customers-not-keen-on-ai-powered-customer-service/620370)|Survey Dec 2023, published Jul 2024|n=5,728|Pre-dates current voice models|"In a 2023 Gartner survey, nearly two-thirds of customers said they'd rather companies didn't use AI for service."|
|18|Chatbots resolved 8% and handed off correctly 8% (mystery shop)|Company-reported (Parloa, a vendor)|V24|May 2026|Spoken claim; no public study found|Unverified, vendor bias|Don't use, or attribute clearly as a vendor's own research.|
|19|Opinions: "nowhere near production ready" (V11); "creepy" (X9); "AI beats humans" (X10)|Opinion|items cited|—|—|Individual views|Attribute as "one builder said…" / "some customers say…"|
|20|Unanswered: how the 70% is measured; failure and repeat-call rates; transfer wait times; whether 3.0 is live on Starlink today; customer satisfaction scores|Open question|—|—|Not published|—|Present as questions to ask.|

---
## E. Image/video asset manifest (UPDATED 2026-10-15: files now in `assets/`)
Amy approved including third-party assets with clear attribution. **The full table, with owner, source URL, direct URL, what each file shows, proposed use and credit text, is in `assets/ATTRIBUTION.md`.** Attribution is not a license: only the Wikimedia logos carry a license, and every other file is included on Amy's instruction.

| Local path | Owner | Proposed use | On-screen credit | Status |
|---|---|---|---|---|
|assets/xai_og_grok_voice_3.webp|SpaceXSI|Title card|Image: SpaceXSI (xAI), x.ai/news/grok-voice-3|Included w/ attribution (no license)|
|assets/xai_launch_page.jpg|SpaceXSI|Announcement date (Oct 14, 2026)|Screenshot: x.ai/news/grok-voice-3 (SpaceXSI)|Included w/ attribution|
|assets/xai_launch_benchmark_table.jpg|SpaceXSI / data AA|"What xAI shows"|xAI launch post; data: Artificial Analysis, Oct 13 2026|Included w/ attribution|
|assets/xai_launch_tauvoice_chart.jpg|SpaceXSI / data AA|Speed vs accuracy|Chart: SpaceXSI; data: Artificial Analysis|Included w/ attribution|
|assets/xai_launch_cost_chart.jpg|SpaceXSI / data AA|Optional cost note|Chart: SpaceXSI; data: Artificial Analysis|Included w/ attribution|
|assets/aa_speech_to_speech_leaderboard.jpg|Artificial Analysis|Independent source|Source: Artificial Analysis, Oct 15 2026|Included w/ attribution|
|assets/aa_s2s_index_chart.jpg|Artificial Analysis|#1 composite|same|Included w/ attribution|
|assets/aa_tauvoice_chart.jpg|Artificial Analysis|~7 in 10, not first|same|Included w/ attribution|
|assets/aa_arena_preference_chart.jpg|Artificial Analysis|Listeners preferred Google voices|same|Included w/ attribution|
|assets/xai_voice_agent_builder_page.jpg|SpaceXSI|Businesses build agents|Screenshot: x.ai/voice (SpaceXSI)|Included w/ attribution|
|assets/xai_starlink_story_page.jpg|SpaceXSI|70% company-reported|Screenshot: x.ai/stories/starlink; company-reported figures|Included w/ attribution|
|assets/xai_starlink_story.webp|SpaceXSI/Starlink|Starlink B-roll|Image: SpaceXSI / Starlink|Included w/ attribution|
|assets/xai_tesla_story.webp|SpaceXSI/Tesla|Where it runs|Image: SpaceXSI / Tesla|Included w/ attribution|
|assets/xai_docs_refer_call.jpg|SpaceXSI|Transfer tool exists (check the crop shows the Refer section)|Screenshot: docs.x.ai (SpaceXSI)|Included w/ attribution|
|assets/clips/xai_tesla_grok_voice_promo_0-15s.mp4|SpaceXSI/Tesla|Tesla beat (15 s, 720p)|Video: SpaceXSI / Tesla, via x.ai|Included w/ attribution|
|assets/clips/grok_official_builder_V6_0m00-0m15.mp4|Grok (YouTube)|Builder beat|Video: Grok / SpaceXSI, YouTube|Included w/ attribution|
|assets/clips/stepwise_V1_0m00-0m15.mp4|Stepwise|Minimal cutaway only|Clip: Stepwise, YouTube|Included w/ attribution (higher risk: competing explainer)|
|assets/clips/simplyai_V3_3m50-4m05.mp4|Simply AI|Listener-vote point|Clip: Simply AI, YouTube|Included w/ attribution (higher risk)|
|assets/clips/cloudyeti_V10_4m45-5m00.mp4|CloudYeti|Handoff depends on setup|Clip: CloudYeti, YouTube|Included w/ attribution|
|assets/clips/assembled_V16_2m10-2m25.mp4|Assembled|Good-handoff example; label "not Grok"|Clip: Assembled demo (not Grok), YouTube|Included w/ attribution|
|assets/logos/starlink_logo.png|SpaceX ™|Case-study label|Starlink is a trademark of SpaceX|Commons public domain; trademark applies|
|assets/logos/xai_logo.png|SpaceXSI ™|Company label (pre-rebrand mark)|xAI logo via Wikimedia Commons, CC BY-SA 4.0|Licensed CC BY-SA; trademark applies|
|assets/logos/grok_logo_2023-2025.png|SpaceXSI ™|Outdated mark; avoid if possible|Grok logo via Wikimedia Commons (PD)|PD; outdated|
|PCMag/Getty photo|Getty|Not used|—|Excluded (licensed stock)|

Rules for Claude Code: show each credit on screen for the whole time the asset is visible. Never present a vendor clip (Assembled) as Grok. Never present xAI's chart as an independent result without the "data: Artificial Analysis" line. Original 2D diagrams remain the primary visuals (section F).

---
## F. Original 2D visual concepts (no fake UI, no real calls)
1. **"Two doors" opener:** presenter at a phone-shaped building with two doors labeled "AI" and "Human"; the AI door opens instantly, the Human door has a clock. *(illustrative)*
2. **Pipeline vs one brain:** three boxes (ears → brain → mouth) passing notes vs a single box that listens and talks at once. Explains speech-to-speech.
3. **Stopwatch strip:** "under 1 second to start replying (lab test)" against a typical pause in human conversation. Label: "Lab measurement."
4. **Scoreboard with an asterisk:** original bar chart of AA composite (86.9 / 83.2 / 82.6), then flips to τ-Voice where GPT-Live-1 leads (74.5 vs 71.6). Source line: AA, Oct 2026.
5. **10 simulated callers:** a row of 10 cartoon callers; 7 get a green check, 3 a question mark. "Simulated test, not real customers."
6. **The 70% pie, stamped "company-reported":** pie chart drawn as a cartoon with a "xAI's figure, not independently audited" stamp, and a calendar showing "same claim in April."
7. **"Where does the 30% go?" flowchart:** caller → AI → (solved) or (needs human → live transfer / callback / ticket / stuck?). Dotted lines for unknowns.
8. **Cold vs warm transfer:** two illustrative relay-race panels. In one the baton drops (you repeat your story); in the other the baton is handed over (summary passed).
9. **Settings switch:** an abstract toggle labeled "Offer human?", explicitly *not* Grok's UI, showing it's the business's choice. Label "illustrative."
10. **"Ask these 3 things" card:** Am I talking to AI? Can you transfer me to a person? Will they see what I've said?
11. **Disclosure moment:** illustrative caller asking "Are you a person?" and the AI answering honestly. Clearly labeled "illustrative scene."
12. **Verdict scale:** "Simple fix" side (password reset, order status) vs "Messy/high-stakes" side (billing disputes, safety). Presenter places the trust marker.

---
## G. Narrative outline (target ~550–650 spoken words, about 4:00)
1. **Hook (0:00–0:20, ~50 words):** You call support and a voice answers instantly, and it isn't a person. xAI says that's already happening at Starlink thousands of times a day. Question: should you trust it, and how do you get a human when you need one?
2. **What it is (0:20–0:55, ~90):** Grok Voice 3.0 was announced Oct 14 as a speech-to-speech model for businesses' phone agents. Uses concept 2. Where it is per xAI: API customers, Tesla, Grok Bot voice mode; don't assume your Grok app has it.
3. **The promise (0:55–1:35, ~100):** speed under a second (lab), and an independent #1 composite score. Concepts 3 and 4.
4. **The fine print (1:35–2:25, ~130):** simulated support tasks ~7/10, not the top score; listeners preferred some Google voices; the "record" is unnamed. Starlink's 70% is company-reported and not new. Concepts 4, 5, 6.
5. **The real question: the other 30% (2:25–3:20, ~130):** human handoff is a business decision; the tools allow it, builders can skip it. PCMag's callback experience (April, earlier version). Why warm transfer matters. The Gartner fear stat. Concepts 7, 8, 9.
6. **Customer decision (3:20–3:55, ~90):** good fit for simple, well-defined tasks; ask for a human early for billing disputes, safety, or anything confusing. The three questions. Concepts 10, 12.
7. **Close (3:55–4:15, ~50):** trust the process, not the leaderboard; judge companies by how easy they make the exit. CTA question to viewers.

---
## H. Do not claim
- That we tested, called, or heard Grok Voice 3.0 (we didn't), or show any "real" Grok UI or call audio.
- That **70% of callers get their problem solved**: xAI reports ~70% "no human in the loop" / "containment." It is company-reported, unaudited, and may not mean solved.
- That 3.0 caused the 70% (the figure was published in April for v1.0).
- That Grok Voice 3.0 is "the best voice AI" without qualification. It's #1 on AA's composite, but not on τ-Voice and not in listener preference.
- That 94.8% task success = 94.8% of real calls resolved.
- That xAI holds a support-call "record" (no named test).
- That EVA-Bench results were published by ServiceNow independently (only xAI's post and a quote).
- That every Grok app user, or every Grok-powered business, uses 3.0.
- That every company using Grok Voice offers a human or a live transfer, or that Starlink currently offers live transfer (only an April callback report exists).
- That your calls are never recorded (xAI's API claim doesn't bind the company you call).
- That it understands emotions or is "empathetic" as a fact (vendor claims, V7).
- That it will eliminate hold times or jobs.
- Gartner stats as current 2026 opinion (the survey is from Dec 2023).
- Parloa's 8% / 96% figures as independent facts.
- Any invented customer story, quote, or call.

---
## Gaps & limitations
- **Reddit: 0 analyzed.** Every access route was blocked. Titles seen in search only, **not read and not counted**: r/Starlink "How to get human support by bypassing grok" (/comments/1v37gb1), "How to get past Grok to make a support ticket" (/1rd6isn), "Getting a human agent on support" (/1pzvntt), "How can I get to actual human support?" (/1tyz2w2); r/NoStupidQuestions /1sny2hb; r/automation "Walmart's AI phone got bypassed with one sentence" (/1rcgtr9). These titles suggest real Starlink callers look for ways around Grok. Worth reading with a logged-in or official API route.
- **Videos were read via transcripts, not watched.** Visual content is unverified. 7 long videos were only partly read (marked). V4 uses an English caption track of a Spanish video (possibly auto-translated). The V20 Fortune captions were fragmentary.
- **Only a few videos are Grok-Voice-3-specific** (V1–V4 posted Oct 14–15, from small channels). The rest cover earlier Grok voice versions or AI phone support in general.
- No public recording of a Grok Voice 3.0 support call. No independent audit of the Starlink numbers. No public data on transfer wait times or repeat-call rates.
- The YouTube transcript endpoint started IP-blocking near the end of collection; 1 candidate was lost to this.
- The pricing discrepancy (Builder promo 5¢/min vs API 8¢/min) is unresolved.
