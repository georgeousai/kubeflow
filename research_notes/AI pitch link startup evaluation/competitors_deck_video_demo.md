# Competitor Map: AI Deck / Explainer-Video / Interactive-Demo Generation (as of Oct 9, 2026)

Method note: research was done on Oct 9, 2026. Direct page fetches (WebFetch and curl) were blocked in this environment by DNS failures and proxy 403s. Every finding below therefore comes from web-search result summaries of the cited URLs, not from reading the full pages. Most pricing figures come from third-party aggregators (Creatify, CostBench, eesel, Tavus/Supademo/Storylane comparison blogs), several of which are competitors of the vendor they describe. Treat prices as indicative and check them against vendor pricing pages before quoting them. Figures older than 2026 are dated inline.

## Q1. Which AI presentation/deck generators exist, how close are they to the idea, and do any offer a shareable link with embedded AI Q&A or voiceover narration?

### Takeaway
"Content in → AI deck out" is saturated and commoditized. Gamma leads among standalone tools ($100M+ ARR, $2.1B valuation), Microsoft and Google bundle the same capability into their suites, and roughly 8+ other tools sit at $7–$40/user/month. None of the major deck tools found ships both AI voice narration and a visitor-facing AI Q&A agent on the share link. Gamma users have repeatedly asked for narration, and Gamma replied "no current plans." That combination is covered only by small startups (DeckChat, InteractPitch, SendNow, Papermark AI) and, in a consumer-research framing, by Google NotebookLM.

### Cited Findings

**Gamma (category leader)**
- Nov 2025: $68M Series B led by Andreessen Horowitz at a $2.1B valuation, with Accel, Uncork Capital and others. CEO Grant Lee said Gamma had profitably reached $100M ARR, with ~70M users — [Pulse 2.0](https://pulse2.com/gamma-68-million-at-2-1-billion-valuation-raised-as-it-surpasses-100-million-in-arr/amp/); [CXO Digital Pulse](https://www.cxodigitalpulse.com/?p=40266); [The Outpost](https://theoutpost.ai/news-story/ai-presentation-startup-gamma-reaches-2-1-b-valuation-with-profitable-100-m-revenue-run-rate-21585/)
- Coverage of the round reported 600,000+ paying subscribers, profitability since 2023, and 52 full-time employees (the 52 figure is Bloomberg-sourced) — [The Outpost](https://theoutpost.ai/news-story/ai-presentation-startup-gamma-reaches-2-1-b-valuation-with-profitable-100-m-revenue-run-rate-21585/); [Pulse 2.0](https://pulse2.com/gamma-68-million-at-2-1-billion-valuation-raised-as-it-surpasses-100-million-in-arr/amp/)
- Sacra estimates ~$102M ARR in Oct 2025, up from $30.5M at end of 2024, which implies a ~21x revenue multiple. Sacra puts total funding at ~$80M — [Sacra](https://sacra.com/c/gamma/). Other trackers give ~$87M across 3 rounds — [Tracxn](https://tracxn.com/d/companies/gamma/__fU9G1eXiWu7iez1HO_-6ZN7vBNibrpNO-Q621b8JYqU); [Getlatka](https://getlatka.com/companies/gamma-app)
- Gamma's own account of reaching $100M with a small, profitable team — [Gamma blog](https://gamma.app/insights/how-we-built-a-usd100m-business-differently)
- Oct 6, 2026: Gamma launched "Gamma 5," a platform rebuild with a new conversational agent that keeps context through editing, a freeform editor and a wider style palette. The release repeats the >$100M ARR claim — [Business Wire press release](https://www.businesswire.com/news/home/20261006266441/en/Gamma-Launches-Gamma-5-to-Eliminate-the-AI-Smell-From-AI-Generated-Content)
- Pricing (2026, third-party, sources conflict): one guide lists Plus $9, Pro $18 and Ultra $90 per seat/month billed annually, with a one-time 400-credit free tier. Pro ($18) includes custom branding, analytics, API and custom domains — [eesel](https://www.eesel.ai/en/blog/gamma-pricing). Another lists Plus $10, Pro $20, Ultra $100 — [Dupple review, updated Jul 2026](https://dupple.com/reviews/gamma). CostBench lists Gamma at $10 vs Beautiful.ai at $12/mo — [CostBench](https://www.costbench.com/compare/gamma-vs-beautiful-ai/)
- Shared Gamma decks have analytics for views, time per card and engagement — [Dupple](https://dupple.com/reviews/gamma)
- **No narration.** Gamma's public feedback board has several user requests for "export with narration / automatic voiceovers (ElevenLabs, HeyGen)" and for timing a narrated script to slides. A Gamma staff reply to the ElevenLabs/HeyGen request said "No current plans but on our radar." The posts are undated — [Gamma ideas: narration export](https://ideas.gamma.app/ideas/p/videos); [Gamma ideas: auto voiceovers](https://ideas.gamma.app/ideas/p/export-gammas-as-videos-with-automatic-voiceovers-eg-for-social-media-posts); [Gamma ideas: voice overs & recording](https://ideas.gamma.app/ideas/p/add-automatic-voice-overs-and-recording-for-gammas)

**Pitch.com (struggled, pivoted)**
- Jan 2024 restructuring: co-founder/CEO Christian Reber stepped down and CTO Adam Renklint became CEO. TechCrunch estimated ~80 roles cut from a published headcount of ~120. Sifted reported 69 people laid off — [TechCrunch, Jan 8, 2024](https://techcrunch.com/2024/01/08/pitch-christian-reber-venture-funding); [Sifted](https://sifted.eu/articles/pitch-lays-off-two-third-of-staff)
- An earlier ~30% cut (~59 people) came in Sept 2022. Total raised was ~$136M, the last round being an $85M Series B in May 2021 — [Sifted](https://sifted.eu/articles/pitch-layoffs-news-tiger); [TechCrunch](https://techcrunch.com/2024/01/08/pitch-christian-reber-venture-funding)
- Per Sacra, Pitch returned most of its VC to investors, cut headcount ~78% (180 → 40), reached profitability by mid-2024 and pivoted toward sales enablement. Sacra estimated ~$10M ARR in Feb 2025; this is a third-party estimate — [Sacra](https://sacra.com/research/pitch); [Sacra chat: Pitch pivots to sales enablement](https://sacra.com/chat/h/a9bfec58-b329-472d-b860-0f7b52c5c915/)
- Pitch's 2025 recap says it has "25+ AI actions" — [Pitch.com](https://pitch.com/whats-new/a-look-back-at-pitch-in-2025). "Pitch Agent" (on-brand decks generated in seconds) launched on Product Hunt on May 28, 2026 — [Product Hunt](https://www.producthunt.com/products/pitch/launches/pitch-4)

**Tome (shut down its deck product)**
- Tome stopped taking new Slides users, cancelled Pro subscriptions, shut the presentation product on Apr 30, 2025 and deleted remaining content. Its email to users said it "failed to find a sustainable path" — [ChatSlide (competitor; commercial bias)](https://www.chatslide.ai/articles/tome-ai-shut-down-what-happened); [Deckary](https://deckary.com/blog/tome-review)
- Tome reportedly generated <$4M ARR despite 20M+ users, in a crowded category where Microsoft and Google were adding native AI slide generation — [Sacra chat: Tome favored growth over enterprise monetization](https://sacra.com/chat/h/5e9af049-ca7f-4b2a-924a-cf5df305fed9); [The Signal](https://signalhub.substack.com/p/tome-failed-in-ai-pptwhy-is-gamma)
- Tome first pivoted to sales personalization (CRM integrations, viewer analytics), and the founders then launched Lightfield, an AI-native CRM — [Sacra chat: Tome pivots to sales enablement](https://sacra.com/chat/h/86a38577-a643-49cd-95e5-8fb8429df303/)
- Sources conflict on whether AngelList acquired the Tome brand. ChatSlide calls the claim mistaken identity — [ChatSlide](https://www.chatslide.ai/articles/tome-ai-shut-down-what-happened)

**Other standalone deck generators (2026 pricing, third-party aggregator data, may conflict)**
- Beautiful.ai: Pro $12/mo, Teams $40/user/mo. Decktopus: Pro AI $14.99/user/mo (9,000 annual AI credits, ~300 decks/yr), top tier $34.99 — [CostBench Beautiful.ai vs Decktopus](https://www.costbench.com/compare/beautiful-ai-vs-decktopus/); [CostBench Decktopus alternatives](https://costbench.com/software/ai-presentations/decktopus/alternatives)
- Plus AI: trial only, Basic $15, Pro $25, Team $40/user/mo. Pro is required for PDF/DOCX uploads — [CostBench Plus AI vs Decktopus](https://costbench.com/compare/decktopus-vs-plus-ai/)
- Prezi: Standard $7/mo, Plus $15/mo, Teams $39/user/mo. Prezi AI generates from a prompt, PDF, PPT or Word file — [CostBench Beautiful.ai vs Prezi](https://costbench.com/compare/beautiful-ai-vs-prezi/); [Affine](https://affine.pro/blog/canva-ai-presentation-maker)
- CostBench's April 2026 benchmark of 7 AI presentation tools names Beautiful.ai the cheapest — [CostBench AI presentations pricing 2026](https://costbench.com/stats/ai-presentations-pricing-2026/)
- Canva: Magic Studio had been used 16B+ times as of 2025. Magic Design builds a deck from a text prompt. Free accounts get 200 Magic Studio credits, and Pro is listed at $15/mo — [Presentations.ai (competitor)](https://www.presentations.ai/blog/how-to-create-a-presentation-with-canva-ai-step-by-step); [Affine](https://affine.pro/blog/canva-ai-presentation-maker)

**Bundled incumbents**
- Microsoft Copilot in PowerPoint drafts a deck from a document you point it to. This needs a Microsoft 365 Copilot (work) license — [Microsoft Support](https://support.microsoft.com/article/57133c75-24c0-4519-8096-d0dadf25fb8d). A Microsoft tutorial covers turning templates, files or PDFs into branded decks with speaker notes. These are text notes, not voice narration — [Microsoft tutorial](https://support.microsoft.com/bg-bg/topic/copilot-tutorial-create-a-branded-presentation-from-a-file-7ed62b4e-4ed9-4762-b042-28b85321d173). April 2026 roadmap: start a Copilot presentation from PowerPoint Home, GA listed for May 2026 — [M365 roadmap mirror](https://mc.merill.net/message/RM560536)
- Google Slides (July 2026 feature drop): Gemini can build a deck using context from your Docs, Sheets, PDFs or earlier decks — [Google Workspace blog, July 2026](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)
- **Google NotebookLM is the closest big-tech analog to the full idea.** Users upload sources and generate "Video Overviews" (narrated explainer videos). A single video, or a whole notebook, can be shared by public link, but only from consumer accounts; public sharing is disabled for Workspace Enterprise/Education — [Google NotebookLM Help](https://support.google.com/notebooklm/answer/16454555). Public-notebook visitors can ask questions in chat and browse generated audio overviews, FAQs and briefing docs. Pro subscribers can share chat-only notebooks — [heise](https://www.heise.de/en/news/NotebookLM-makes-it-easier-to-share-content-with-public-links-10424873.html?view=print). Since Mar 2026, a visitor's chat in a shared notebook is private to them, and "Cinematic Video Overviews" were added — [Google Workspace Updates, Mar 20, 2026](https://workspaceupdates.googleblog.com/2026/03/new-ways-to-customize-and-interact-with-your-content-in-NotebookLM.html). Video Overviews first launched Jul 2025 — [9to5Google](https://9to5google.com/2025/07/29/notebooklm-video-overviews/)

**Small startups combining a share link with an AI Q&A layer (direct overlap with the "talk to the deck" half)**
- DeckChat ("Your Talking Pitch Deck"): founders add a deck and materials, and an AI answers investor questions around the clock from one shared link — [DeckChat](https://deckchat.io/)
- InteractPitch (launched ~Jan 2026): turns a PDF/PPTX deck into an interactive experience led by an AI avatar of the founder, built from a photo and voice sample. Investors ask by text or voice and get answers grounded in the slides plus a knowledge base. The viewer is mobile-first, and founders see analytics on who opened it, time spent, sections viewed and questions asked. Toolify shows 0 user reviews — [Product Hunt](https://www.producthunt.com/posts/interactpitch-3); [Toolify](https://www.toolify.ai/tool/interactpitch); [Feedbagel](https://feedbagel.com/post/interactpitch-interactive-pitch-decks-with-ai-avatars-and-real-time-investor-ana)
- SendNow: indexes an uploaded PDF/PPTX and answers visitor questions with page citations, using text chat only — [SendNow](https://sendnow.live/solutions/ai-chatbot-pitch-deck)
- Tars (hellotars): a "pitch deck AI agent" that turns a company story into a guided two-way conversation with lead capture, and claims 500+ brand customers — [Tars](https://hellotars.com/ai-agents/pitch-deck-ai-agent); [Tars sales deck agent](https://hellotars.com/ai-agents/sales-deck-ai-agent)
- Papermark (open-source DocSend alternative): AI chat with documents, link sharing with email verification, watermarks and NDA gates, and page analytics. It is now positioned mainly as a data room, from €99/mo — [Papermark AI](https://papermark.io/ai); [Papermark](https://www.papermark.com/index.md)
- DocSend (Dropbox) is reported to lack AI document chat. Both sources making this claim are competitors. DocSend Personal costs $10/user/mo — [Send.co](https://www.send.co/blog/top-alternatives-to-highspot); [Prospeo](https://prospeo.io/s/docsend-alternatives)

### Inferences
- Deck generation itself is not a differentiator. Gamma ($9–$20 a seat), Copilot and Gemini (bundled) and 8+ others all do "paste a doc → deck." A new entrant would have to build on this layer, or call it through an API, rather than compete on it.
- Gamma's public feedback board shows unmet demand for narration and voiceover export, and Gamma said it had no plans to build it at the time (undated). That is a signal of demand. It is also a risk: Gamma, with 600K+ paying subscribers and a new conversational agent in Gamma 5, could ship narration quickly.
- NotebookLM is a free or cheap substitute that already delivers "upload content → narrated video + chat Q&A on one public link." Its limits for this use case are Google branding, lack of company-branded pages, consumer-account-only public sharing, and no lead capture or LinkedIn-optimized landing page. It is not designed as a marketing or pitch asset. The founder's product would have to beat it on presentation polish, branding, analytics and lead capture.
- The "talking pitch deck" niche (DeckChat, InteractPitch, SendNow, Tars) is already populated, but by small, early players with no visible traction data. This suggests the idea is being tried by many but has not broken out yet.

### Gaps
- Gamma's 2026 ARR beyond ">$100M" and its 2026 paying-subscriber count were not found. A Gamma acquisition of design startup "Lica" (Aug 2026) appeared in one search summary and could not be verified.
- Beautiful.ai, Prezi, Decktopus and Plus AI funding/ARR were not found in this research.
- DeckChat, InteractPitch, SendNow and Tars pricing, user counts and funding were not found. Their feature claims are self-reported.
- Tome's total funding was not verified with a cited source here.
- Whether Copilot in PowerPoint can generate voice narration was not confirmed. Search found only speaker notes.
- Official vendor pricing pages could not be opened, so all prices are third-party.

## Q2. Which AI video tools turn text, docs, URLs or slides into explainer videos with avatars or voiceover, at what price, and do they support "URL or doc in → explainer video out"?

### Takeaway
"URL/doc in → avatar-narrated explainer video out" is already a mainstream, well-funded feature. HeyGen ($200M ARR, June 2026) and Synthesia ($4B valuation, Jan 2026) both accept URLs and files. Google Vids converts Slides to avatar-narrated video. Lumen5, Pictory and InVideo do URL-to-video at roughly $15–$20/month. Entry pricing works out to about $1.40–$2/min (Synthesia) or $29/mo plans (HeyGen). What these tools do not package is a hosted landing page that pairs the video with a live Q&A agent. HeyGen (LiveAvatar) and Synthesia (planned conversational agents) both own the components to do it.

### Cited Findings

**HeyGen**
- Jun 25, 2026: passed $200M ARR, doubling from $100M in ~8 months. It reports being cash-flow break-even in 2026 so far, having burned ~$25M of $74M raised, and serving 30M+ users in 196 countries, including 85% of the Fortune 100 — [HeyGen blog](https://www.heygen.com/blog/heygen-surpasses-200m-arr); [Upstarts Media](https://www.upstartsmedia.com/p/exclusive-heygen-200m-arr-without-burn)
- Pricing (2026, third-party): tiers at $0, $29, $49 and $149/mo, with 600 credits (Creator), 1,000 (Pro) and 1,500 shared (Business). The free plan allows up to 3 videos/mo of ~1 min each, watermarked. Video Agent costs reportedly rose from 20 to 30 credits/min on Jul 22, 2026, with 90 credits/min in "Seedance" mode — [Creatify](https://creatify.ai/blog/heygen-pricing-(2026)-plans-and-what-you-ll-actually-pay); [eesel](https://eesel.ai/blog/heygen-pricing)
- URL-in: HeyGen's AI Video Explainer reads a pasted webpage link, builds a scene-by-scene storyboard and narrates it — [HeyGen tool page](https://www.heygen.com/tool/ai-video-explainer)
- HeyGen also sells LiveAvatar, a real-time interactive avatar product with separate billing — [Tavus blog (competitor)](https://www.tavus.io/blog/heygen-pricing-breakdown-best-alternatives); [Neuronfeed](https://neuronfeed.com/reviews/tavus-review)

**Synthesia**
- Apr 15, 2025: passed $100M ARR and took an Adobe Ventures strategic investment — [Synthesia](https://www.synthesia.io/post/100-million-revenue-adobe-investment); [Tech.eu](https://tech.eu/2025/04/15/synthesia-scores-adobe-investment-as-hits-100m-in-arr/)
- Jan 2026: $200M Series E at a $4B valuation, led by GV, alongside an employee secondary run with Nasdaq. The prior round was a $180M Series D at $2.1B in early 2025. Total raised is ~$535–536M — [UCL News](https://www.ucl.ac.uk/news/2026/jan/ai-video-startup-co-founded-ucl-professor-valued-4-billion); [HLTH](https://hlth.com/insights/news/synthesia-raises-200m-with-4b-valuation-2026-01-27); [VKTR](https://www.vktr.com/ai-news/synthesia-hits-4b-valuation-in-series-e-adds-nasdaq-backed-employee-liquidity/)
- Sacra says Synthesia disclosed ~$140M ARR in a Feb 2026 engineering post — [Sacra](https://sacra.com/research/synthesia)
- Synthesia plans to move beyond "static, one-way content" toward conversational AI agents that answer questions, role-play and explain. No source confirmed that these have launched — [The Deep View](https://www.thedeepview.com/articles/synthesia-doubles-to-usd4b-preps-ai-video-agents); [Sifted](https://sifted.eu/articles/synthesia-100m-arr-ai-agents)
- URL/file-in: Synthesia's assistant drafts an explainer from a prompt, script, uploaded file or URL, producing an editable outline before generation — [Synthesia explainer tool](https://www.synthesia.io/tools/explainer-video-maker)
- Pricing (Aug 2026, third-party, conflicting): Starter ~$168/yr for ~120 min (≈$1.40/min). Creator $708/yr for ~360 min (≈$1.97/min). Lip-synced dubbing uses 2x the credits — [Creatify](https://creatify.ai/blog/synthesia-pricing-(2026)-plans-credits-and-what-you-ll-actually-pay). Arcade's roundup instead lists Starter $29/mo and Creator $89/mo (30 min/mo, 5 personal avatars) — [Arcade](https://www.arcade.software/post/synthesia-pricing)

**Other avatar/voiceover video tools (2026 third-party pricing)**
- Colossyan: Starter $27/mo (15 min), Business $88/mo (unlimited minutes, SCORM, 3 seats), Enterprise custom. Another source gives Starter $19/mo billed annually. It turns PDFs, PowerPoint and text documents into avatar-narrated video, mainly for training. Custom avatars cost ~$1,000/yr extra — [CostBench Colossyan vs D-ID](https://costbench.com/compare/colossyan-vs-d-id/); [Anam (competitor)](https://anam.ai/blog/d-id-vs-colossyan)
- D-ID: Lite ~$5.99/mo (10 min, watermarked), Pro ~$16–29/mo, Advanced ~$108–196/mo (~100 min) — [CostBench](https://costbench.com/compare/colossyan-vs-d-id/); [Anam](https://anam.ai/blog/d-id-vs-colossyan)
- Tavus (conversational video, CVI): entry pricing is reported anywhere from ~$22 to ~$59/mo. One source lists Hobby $39, Business $375/mo and custom Enterprise. Real-time minutes drive cost — [Neuronfeed](https://neuronfeed.com/reviews/tavus-review); [Sendspark](https://blog.sendspark.com/tavus-alternatives)
- VisionStory: an "AI Video Agent" that turns a prompt, URL or script into a video with avatar, voiceover and captions in one flow — [VisionStory](https://www.visionstory.ai/avatar)

**Faceless / stock-footage URL-to-video tools (2026 third-party pricing)**
- InVideo AI: Plus $17/mo billed annually ($200/yr); accepts a pasted URL or script — [Subclip](https://subclip.app/blogs/top-10-invideo-ai-alternatives)
- Pictory: entry $19/mo for 200 video min at 1080p. Fliki: Standard $21/mo for 120 min/mo. Both figures come from a Pictory-authored comparison dated May 1, 2026, so the source is vendor-biased — [Pictory](https://pictory.ai/blog/pictory-vs-fliki)
- Lumen5: from £15/mo billed annually. Pasting a blog URL splits it into scenes with key-sentence text and matched stock footage — [Marc Andrews](https://marcandrews.com/?p=3165); [Subclip](https://www.subclip.app/blogs/top-10-lumen5-alternatives)
- Fliki markets an "AI pitch video maker," and PortfolioVideo an "AI pitch deck generator" that produces narrated videos with share links but no live Q&A — [Fliki](https://fliki.ai/use-cases/business-and-corporate/pitch-maker); [PortfolioVideo](https://portfoliovideo.com/ai-pitch-deck-generator)
- ChatSlide converts presentations into videos with AI narration in 29 languages — [ChatSlide](https://www.chatslide.ai/pages/gamma-to-video)

**Google Vids**
- May 11, 2026: users can add AI avatars as spokespeople when converting Google Slides to Vids. Gemini already generated scripts, voiceovers and music. Per-user limits apply after a promotional period that ended Jul 1, 2026 — [Google Workspace Updates](https://workspaceupdates.googleblog.com/2026/05/add-avatars-when-you-convert-presentations-to-Vids.html)
- Jul 16, 2026: Gemini Omni in Vids lets users build personal avatars from a selfie and voice recording. This is limited to paid subscribers, English, users 18+, and is not available in the EEA, Switzerland or the UK — [Google Workspace Updates](https://workspaceupdates.googleblog.com/2026/07/cast-yourself-in-ai-video-clips-using-your-personal-avatar-with-Gemini-Omni-in-Vids.html); [PPC Land](https://ppc.land/google-vids-gains-gemini-omni-editing-and-avatars-for-paid-users-only/)
- The preset avatar library reportedly grew from 23 to 53. Language counts conflict: 24 languages in one source, 8 for AI voiceovers in Google's July drop — [Softprom](https://softprom.com/google-vids-gemini-omni-ai-avatars-update-overview); [Google Workspace blog](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)

### Inferences
- The founder should not plan to build video generation in-house. HeyGen, Synthesia and Google Vids cover "doc/URL → narrated avatar explainer," and at least HeyGen and Synthesia are well capitalized and fast-moving. The realistic architecture is to orchestrate one of these through an API, or to use slide + TTS narration instead of avatars.
- HeyGen ($29/mo entry; ~30 credits per Video Agent minute) and Synthesia (~$1.40–$2/min) set the price anchor. If the product renders one ~2-minute explainer per customer, the generation cost is likely a few dollars, so it will not be a cost barrier. This is an inference from the per-minute figures above.
- The incumbents' weak spot is that their output is a video file or player, not a "company page" with an attached Q&A agent. HeyGen already sells LiveAvatar and Synthesia is building conversational agents, so either could close this gap.

### Gaps
- Elai, Steve AI and Sora/Veo-based tools: no 2026 pricing or URL-to-video details were found in this research.
- Google Vids standalone pricing and plan eligibility in Oct 2026 were not found.
- Official HeyGen and Synthesia pricing pages could not be opened. The Synthesia figures conflict between Creatify and Arcade.
- Whether HeyGen LiveAvatar and a HeyGen explainer video can be combined on one hosted share page was not determined.

## Q3. Interactive demo and sharing platforms (Arcade, Storylane, Navattic, Supademo, Walnut, Consensus, DocSend, Qwilr, Loom): do any combine a narrated walkthrough with an AI Q&A layer?

### Takeaway
Yes. Storylane (Lily/RepX: AI voiceover, avatars, and a live AI agent across chat, voice and video) and Supademo (AI voiceover plus a self-serve AI Demo Agent as of Aug 2026) already combine narrated walkthroughs with AI Q&A, and Navattic has Agent Demos in beta. All three target B2B SaaS product demos built from screen captures of a software UI, not company or idea explainers built from pasted content. Arcade has AI voiceover but no live agent. DocSend and Qwilr reportedly have no native AI chat.

### Cited Findings
- **Storylane:** offers the Lily AI sales agent, AI voiceover, AI avatars and translation. RepX is a live AI sales agent that answers questions, runs discovery, qualifies visitors, shows demos and books meetings across chat, voice and video. Pricing: Demo Suite is free for 1 demo, then $40–$1,200/mo on yearly billing. RepX starts at $2,000/mo. These comparisons come from competitors — [Supademo blog](https://supademo.com/blog/storylane-alternatives); [Floe](https://floe.so/compare/storylane-alternatives); [Storylane vs Navattic (Storylane)](https://www.storylane.io/blog/storylane-vs-navattic)
- Storylane funding: a $1M angel round to integrate the Lily AI agent (date unconfirmed) and a YC seed of ~$125K in 2021. Totals conflict, with VCBacked listing $800K — [Signalbase](https://www.trysignalbase.com/news/funding/storylane-raises-1m-in-angel-funding-to-revolutionize-demo-automation-with-lily-ai); [Seedtable](https://seedtable.com/companies/storylane/funding-rounds/seed-2021-08); [VCBacked](https://www.vcbacked.co/company/storylane)
- **Navattic:** launched LaunchPad in Sep 2025 and announced "Agent Demos" in 2026, which are autonomous AI walkthroughs, in beta, that infer intent, navigate the product and produce transcripts. It has AI voiceovers but reportedly no in-app voice recording — [Naoma (competitor)](https://naoma.ai/blog/storylane-vs-navattic); [Naoma 2026](https://naoma.ai/articles/navattic-vs-storylane-2026)
- Navattic funding: a $4.25M growth seed in Mar 2022 led by Canvas Ventures, ~$5.5M total. No Series A was found — [Navattic blog](https://www.navattic.com/blog/building-the-future-of-plg); [Seedtable](https://seedtable.com/startups/Navattic-99XN49K)
- **Arcade:** AI voiceover, copy suggestions and auto chapters, with no live AI demo agent — [Arcade](https://www.arcade.software/post/best-interactive-demo-software-2026); [Supademo blog](https://supademo.com/blog/storylane-alternatives). Funding: $21.5M over 4 rounds, the latest a $14M Series A on Nov 19, 2024; VCBacked lists $14M total — [CB Insights](https://www.cbinsights.com/company/arcade-3/financials); [VCBacked](https://www.vcbacked.co/company/arcade-san-francisco)
- **Supademo:** AI voiceover uses OpenAI and ElevenLabs models, with the voice matched to the demo language — [Supademo docs](https://docs.supademo.com/customize/voiceovers/instant-ai-voiceover). May 2026 added a pronunciation dictionary shared by voiceovers and Demo Agent conversations — [Supademo May 2026](https://supademo.com/blog/product-update-may-recap). June 2026 added Voiceovers 2.0, with emotion and tone — [Supademo June 2026](https://supademo.com/blog/product-update-june-recap). In Aug 2026, Demo Agents became self-serve, with 1,500 free credits per workspace (~70 conversations) — [Supademo Aug 2026](https://supademo.com/blog/product-update-august-recap)
- A 2026 roundup lists Naoma, Storylane, Navattic, Arcade, Supademo, Consensus and Walnut as the main players in the category — [Naoma](https://naoma.ai/bs/articles)
- **DocSend:** reported to lack AI document chat, per competitor claims; Personal plan $10/user/mo — [Prospeo](https://prospeo.io/s/docsend-alternatives); [Send.co](https://www.send.co/blog/top-alternatives-to-highspot)
- **Qwilr:** no native AI chat feature found. The only AI material was a third-party agent-automation page — [Toolhouse](https://toolhouse.ai/integrations/automate-qwilr-with-ai-agents); [CheckThat](https://checkthat.ai/answers/what-is-the-best-proposal-software)

### Inferences
- "Narrated walkthrough + AI agent answering questions on one link" already exists in the demo-automation category, in at least Storylane, Supademo and Navattic (beta). The founder's idea is not new as a pattern. Its novelty would come from the input (pasted company content rather than a product UI capture) and the audience (LinkedIn viewers and investors rather than SaaS buyers).
- Storylane RepX at $2,000+/mo against Supademo's free 70 conversations shows the AI-agent layer moving quickly from premium to commodity in 2026.
- Demo platforms are a plausible adjacent entrant. They already have hosting, analytics, voiceover and agents, and would need only a "generate from docs/URL" mode to compete with the founder's product.

### Gaps
- Walnut and Consensus: no verified 2026 AI features, pricing or funding were found.
- Loom AI: no results on 2026 AI features or any viewer Q&A capability.
- Storylane and Navattic pricing comes from competitor comparisons. Navattic's pricing is not consistently published.
- Supademo funding and Storylane revenue were not found.

## Q4. Which players have strong revenue or funding, which have shut down, pivoted or struggled, and what lessons do the failures offer?

### Takeaway
The money has concentrated in a few capital-efficient, horizontal winners: HeyGen ($200M ARR, Jun 2026, cash-flow break-even), Gamma (>$100M ARR, profitable, ~52 staff in Nov 2025) and Synthesia ($4B valuation, ~$140M ARR disclosed Feb 2026). The failures (Tome, Pitch) show that viral free usage of AI deck generation does not convert to revenue, that bundling by Microsoft and Google compresses standalone pricing, and that over-funded deck tools retreat into sales enablement.

### Cited Findings
- **Winners**
  - HeyGen: $200M ARR (Jun 2026), doubled in ~8 months, ~$25M burned of $74M raised — [Upstarts Media](https://www.upstartsmedia.com/p/exclusive-heygen-200m-arr-without-burn); [HeyGen blog](https://www.heygen.com/blog/heygen-surpasses-200m-arr)
  - Gamma: $100M ARR, profitable, $2.1B valuation (Nov 2025); Sacra estimates ~3.3x ARR growth from $30.5M at end of 2024 to ~$102M in Oct 2025 — [Pulse 2.0](https://pulse2.com/gamma-68-million-at-2-1-billion-valuation-raised-as-it-surpasses-100-million-in-arr/amp/); [Sacra](https://sacra.com/c/gamma/)
  - Synthesia: $4B valuation (Jan 2026); $100M ARR (Apr 2025); ~$140M ARR per a Feb 2026 disclosure cited by Sacra — [UCL](https://www.ucl.ac.uk/news/2026/jan/ai-video-startup-co-founded-ucl-professor-valued-4-billion); [Synthesia](https://www.synthesia.io/post/100-million-revenue-adobe-investment); [Sacra](https://sacra.com/research/synthesia)
- **Mid/small players:** Arcade raised $21.5M total, with a Series A in Nov 2024 — [CB Insights](https://www.cbinsights.com/company/arcade-3/financials). Navattic ~$5.5M, last raised in 2022 — [Seedtable](https://seedtable.com/startups/Navattic-99XN49K). Storylane is lightly funded (YC plus a $1M angel round) — [Signalbase](https://www.trysignalbase.com/news/funding/storylane-raises-1m-in-angel-funding-to-revolutionize-demo-automation-with-lily-ai)
- **Tome:** 20M+ users but <$4M ARR. The Slides product was shut on Apr 30, 2025 and user content deleted. The company pivoted to sales, and the founders launched the Lightfield CRM — [Sacra chat](https://sacra.com/chat/h/5e9af049-ca7f-4b2a-924a-cf5df305fed9); [Sacra chat (pivot)](https://sacra.com/chat/h/86a38577-a643-49cd-95e5-8fb8429df303/); [Deckary](https://deckary.com/blog/tome-review)
- **Pitch:** ~$136M raised. Staff were cut ~30% in 2022, then ~two-thirds to ~78% in Jan 2024, with a CEO change. Most VC was returned to investors, the company turned profitable by mid-2024, and it pivoted to sales enablement at an estimated ~$10M ARR (Feb 2025) — [Sifted](https://sifted.eu/articles/pitch-lays-off-two-third-of-staff); [TechCrunch](https://techcrunch.com/2024/01/08/pitch-christian-reber-venture-funding); [Sacra](https://sacra.com/research/pitch)
- Commentary on why Tome failed where Gamma succeeded — [The Signal](https://signalhub.substack.com/p/tome-failed-in-ai-pptwhy-is-gamma)

### Inferences
- Lesson 1 (Tome): a viral "wow" generation moment brings users, not revenue. Tome had 20M users and under $4M ARR. A free, shareable LinkedIn link has the same risk, so monetization must be designed in from the start, for example through paid analytics, lead capture, custom domains or removal of branding.
- Lesson 2 (Tome, Pitch): standalone deck tools get squeezed when Microsoft and Google bundle AI generation. Both survivors moved toward sales workflows, where buyers pay per seat for analytics and CRM ties.
- Lesson 3 (Gamma, HeyGen): the winners are horizontal, product-led, low-burn and serve prosumer/SMB users at about $10–$30/mo. They ship fast enough to absorb adjacent features. A solo founder's niche feature (narration plus a Q&A agent on a link) is exactly the kind of feature they can add.
- Lesson 4 (Tome): deleting users' content at shutdown damaged trust. For a product whose output is a public link, link durability and export matter to buyers.

### Gaps
- No 2026 data was found on Gamma's paying-subscriber growth, Beautiful.ai, Prezi or Canva presentation revenue, or Pitch's 2026 ARR.
- No verified shutdowns of AI video tools in 2025–2026 were found in this research.
- Tome's total funding and final headcount were not verified here.

## Q5. Feature-gap analysis: what specific combination, if any, is not already covered by an incumbent?

### Takeaway
Every individual component is covered: content → deck (Gamma, Copilot, Gemini), content/URL → narrated or avatar video (HeyGen, Synthesia, Vids, Lumen5), link + AI Q&A over a deck (DeckChat, InteractPitch, SendNow, Papermark), narrated walkthrough + voice/chat agent (Storylane RepX, Supademo) and sources → narrated video + public chat link (NotebookLM). The combination that appears not to be packaged by any incumbent is a single, branded, LinkedIn-optimized company page generated end to end from pasted raw content (website, notes, docs, with no existing deck required and no founder recording, photo or voice sample), pairing an auto-generated narrated explainer with a voice agent, plus lead capture and analytics, at prosumer pricing. This gap is narrow and easily copied.

### Cited Findings
- Gamma lacks narration or voiceover (per user requests and an undated staff reply), though it does have share-link analytics — [Gamma ideas](https://ideas.gamma.app/ideas/p/videos); [Dupple](https://dupple.com/reviews/gamma)
- NotebookLM offers sources → Video Overview + public chat link, but only on consumer accounts and with no company branding or lead capture found — [NotebookLM Help](https://support.google.com/notebooklm/answer/16454555); [heise](https://www.heise.de/en/news/NotebookLM-makes-it-easier-to-share-content-with-public-links-10424873.html?view=print)
- InteractPitch requires an existing deck (PDF/PPTX) and a founder photo and voice sample for its avatar, and targets investors — [Toolify](https://www.toolify.ai/tool/interactpitch)
- DeckChat and SendNow start from an uploaded deck and answer questions; SendNow uses text chat only — [DeckChat](https://deckchat.io/); [SendNow](https://sendnow.live/solutions/ai-chatbot-pitch-deck)
- Storylane, Supademo and Navattic agents work on captured product-UI demos aimed at SaaS buyers. RepX starts at $2,000/mo — [Floe](https://floe.so/compare/storylane-alternatives); [Supademo Aug 2026](https://supademo.com/blog/product-update-august-recap)
- HeyGen (URL → explainer; LiveAvatar for real-time) and Synthesia (URL/file → video; conversational agents planned) have both halves in-house but separately packaged — [HeyGen tool](https://www.heygen.com/tool/ai-video-explainer); [The Deep View](https://www.thedeepview.com/articles/synthesia-doubles-to-usd4b-preps-ai-video-agents)
- Google Vids builds avatar-narrated video from Slides, and personal avatars are geo-restricted, with none in the EEA, CH or UK — [Google Workspace Updates](https://workspaceupdates.googleblog.com/2026/07/cast-yourself-in-ai-video-clips-using-your-personal-avatar-with-Gemini-Omni-in-Vids.html)

### Inferences
- The uncovered combination is roughly:
  1. raw, unstructured content as input (website URL plus notes plus docs, with no finished deck needed);
  2. zero founder recording (no avatar training, no photo or voice sample required, unlike InteractPitch and Vids personal avatars);
  3. one auto-generated narrated explainer, as a deck with TTS or a video;
  4. a voice and chat agent grounded in the same content;
  5. a single public, branded page built for social sharing (LinkedIn preview, mobile-first);
  6. visitor analytics and lead or meeting capture;
  7. a self-serve price in the $10–$50/mo range, versus Storylane RepX at $2,000/mo.
  No single incumbent found does all seven.
- The gap is shallow. Each component is available as an API or feature from well-funded players: HeyGen and Synthesia (video plus interactive avatars), Gamma (generation, sharing and analytics, with narration demand already visible) and Google (NotebookLM already does items 1–4 informally). The most likely fast followers are Gamma (adding narration and an agent to share links), HeyGen (combining Video Agent and LiveAvatar on a hosted page) and Supademo/Storylane (adding a "generate from docs" mode).
- Possible defensible angles for a solo founder: (a) a vertical focus, such as fundraising founders, with investor-specific analytics, Q&A logs and "what investors asked" summaries; (b) owning distribution on LinkedIn with a link format that previews and autoplays well; (c) answer-quality guardrails, such as citing sources and refusing to make up traction numbers, which matter more for pitch content than for marketing videos. These are hypotheses, not verified market needs.
- The demand signal is mixed. Several small startups (DeckChat, InteractPitch, SendNow, Tars) are attempting "talking pitch deck" products, which validates interest, but none shows public traction data. Tome's 20M users and <$4M ARR show how hard it is to monetize free, shareable AI decks.

### Gaps
- No quantitative evidence was found on how often visitors to AI-Q&A deck links actually use the chat or voice agent (engagement rates).
- No user reviews or traction data were found for DeckChat, InteractPitch, SendNow or the Tars pitch agent. G2/Capterra feature complaints about Gamma, HeyGen and Synthesia were not reached in this research.
- No evidence was found on whether LinkedIn treats such links differently in reach or previews compared with native video. This would need separate research.
- Whether NotebookLM public notebooks allow custom branding or embedding was not determined.
