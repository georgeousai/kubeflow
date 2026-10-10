# Sell the AI pitch link to sellers

**Verdict: don't build this idea as described. Build it only in a modified form, and only after about three weeks of cheap validation.** In the original concept, a founder pastes their content and gets one link to post on LinkedIn, where investors and followers watch an AI explainer or talk to a voice agent. That concept fails on the three things that decide recurring revenue for a solo founder. First, the buyers with the most urgent need, fundraising founders, need it for a raise that lasts 3–6 months and comes roughly once every two years. Second, their audience, VCs, openly treat AI-made pitch material as a negative signal. Third, free or bundled substitutes already cover most of the product: Google NotebookLM's public notebooks with Video Overviews, Gamma and HeyGen. At least seven small, unfunded "talking pitch deck" tools also exist. On top of that, AI tools priced under $50/month keep only about 23% of their revenue after a year, and LinkedIn cuts the reach of posts that contain links. **Even if it gets traction, the pure version will most likely stall at about $2–4k MRR. The median new AI micro-SaaS earns about $150–200 a month.**

The version worth building is a self-serve **"follow-up link" for seed-to-Series A B2B startups doing founder-led sales, and for small agencies.** It has three parts:

- a narrated deck generated from pasted content;
- an opt-in Q&A agent that answers only from facts the founder has approved;
- the real product: a summary of what each prospect watched and asked, plus lead alerts.

Recommended pricing is about **$79/month for Pro and $199–299/month for teams or agencies.** Voice minutes are metered, and fundraising is sold as a one-time $99 "raise pass". At that price the product escapes the worst churn band and keeps roughly 80% gross margin. A competent solo developer can ship the MVP in 4–8 weeks. **A good outcome is $3–6k MRR at month 12 and a ceiling of $10–30k at maturity. Anything above $10k in year one is a top-decile result.** The main risks are retention and big platforms adding this as a feature (Gamma, HeyGen, Supademo/Storylane, Google), not build difficulty or AI cost. The researchers could not open most pages, so nearly every figure below comes from search-result summaries. Load-bearing numbers are marked "(verify)", and a full list of figures to verify is in the section on where the notes disagree.

## Customers: fundraisers hurt most, but sellers pay every week

The product has two audiences. The **creator** pastes the content and pays. The **viewer** watches and asks questions. The evidence splits cleanly between them. The creators with the most acute pain are the ones least likely to stay subscribed. The viewers who most want self-serve explanations are buyers, not investors.

**Fundraising founders have the sharpest pain, but it comes and goes.**

The volume of outreach is high:

- DocSend's 2020 data found that a large group of founders "needs to contact upwards of 100, 150 or even 200 investors" to close a pre-seed round ([TechCrunch](https://techcrunch.com/2020/03/03/docsends-new-pre-seed-data-shows-how-many-founders-you-should-have-and-how-many-investors-you-should-meet/)).
- A later DocSend report put the average at **71 investors contacted and 46 meetings** ([DocSend](https://www.docsend.com/blog/pre-seed-fundraising-report/)).

The job is also short and rare:

- DocSend's 2024 analysis found pre-seed rounds averaged **12 weeks** ([StockTitan/DocSend](https://www.stocktitan.net/news/DBX/v-cs-prioritize-people-in-an-ai-heavy-landscape-according-to-new-z3rqvcox6orq.html)).
- 2026 guides say a seed round takes three to six months ([SeedForge](https://seedforge.com/blog/how-long-does-it-take-to-close-a-seed-round-in-2026)).
- Carta's median gap from seed to Series A was **1.9 years** in Q4 2025 ([Carta](https://carta.com/data/linkedin-time-between-startup-rounds-improving/)).

A subscriber whose need lasts three to six months behaves like a customer with roughly 17–33% monthly churn. That figure is an inference, but it matches the only public warning from someone who built a near-identical product. An Indie Hackers founder making AI explainers for SaaS companies flagged "high churn risk after they finish their explainer" ([Indie Hackers](https://www.indiehackers.com/post/pivoting-my-saas-mvp-away-from-ai-images-feedback-wanted-on-planned-acquisition-vs-retention-strategy-BIPxmQ52P6FB2rzfawXo)).

The number of fundraising founders is also falling:

- Carta recorded **50,316 pre-seed SAFEs and notes in 2025, 13% fewer than in 2024** ([Carta](https://carta.com/data/state-of-pre-seed-2025-full-report/)).
- Q2 2026 pre-seed instruments fell about 22% year over year ([Carta](https://carta.com/data/state-of-pre-seed-q2-2026/)).
- In Q2 2026, seed dollars rose 37% while the number of seed rounds fell 20% ([TipRanks](https://www.tipranks.com/news/private-companies/carta-data-points-to-larger-venture-rounds-and-tighter-selection-in-q2-2026)).

**Early B2B startups have a weaker but continuous pain: explaining the offering to every new prospect.**

Their buyers want exactly the kind of self-serve explanation this product produces. Gartner found that **61% of B2B buyers prefer a rep-free buying experience** and 73% avoid suppliers that send irrelevant outreach ([Gartner](https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-sales-survey-finds-61-percent-of-b2b-buyers-prefer-a-rep-free-buying-experience)). A follow-up survey raised the rep-free figure to **67%**, although buyers still want seller input on whether a product fits their company ([Digital Commerce 360](https://www.digitalcommerce360.com/2026/03/17/gartner-b2b-buyers-rep-free-purchasing-ai-reshapes-sales/)).

These teams already buy async explanation tools. In Vidyard's survey, 92% of 656 sales and marketing leaders called video essential to their revenue strategy ([Vidyard](https://www.vidyard.com/future-revenue-strategy-agentic-ai-and-video/)). Loom's business tiers cost $15–24 per seat ([Trainn](https://trainn.co/blog/loom-pricing/)).

**Agencies have similar continuous demand, with a structural bonus: one account creates links for many clients.**

Qwilr sells interactive proposals to "agencies, small to mid-sized teams, and consultants" at $35–39 per user ([Verdocs](https://verdocs.com/blog/qwilr-pricing)). White-label chat-and-voice-agent platform Stammer claims 1,300+ agencies charging clients $300–500 MRR each ([Stammer](https://stammer.ai)). Treat that as a marketing claim, not evidence. Stammer's own agency plans are reported at $197 and $497 a month, though sources conflict ([Robofy](https://www.robofy.ai/blog/stammer-ai-alternatives)).

**The remaining segments are weaker.**

- **Coaches and creators:** Delphi already serves them with AI "digital minds" at $79–399/month ([Creator Economy Tools](https://creatoreconomytools.com/tool/delphi)).
- **Job seekers:** their need is episodic, and recruiters increasingly screen with AI rather than watch media ([The Interview Guys](https://blog.theinterviewguys.com/83-of-companies-will-use-ai-resume-screening-by-2025-despite-67-acknowledging-bias-concerns/)).
- **Accelerators:** they spend their software budgets on cohort-management platforms. No accelerator was found buying portfolio-wide pitch-tool licenses ([Innoloft](https://innoloft.com/en-us/blog/accelerator-software)). Startup perks marketplaces exist as a channel ([GetProven](https://og.getproven.com/vendor/arcade)).
- **Real estate:**
  - The job recurs with every listing. Professional listing video costs $350–750 per property ([Reel-E](https://www.reel-e.ai/blog/real-estate-video-cost)), and AI listing tools sell for $59–249/month ([AutoReel](https://www.autoreelapp.com/faq/ai-real-estate-tools/what-is-the-roi-of-ai-video-tools-for-real-estate-agents)).
  - Indie products convert poorly here. One AI listing-video platform had more than 4,000 agent sign-ups but only $49.9k in trailing-twelve-month revenue ([Acquire.com](https://app.acquire.com/public/4kyu863x8a-ai-real-estate-video-platform-turning-listing-photos-into-cinematic-property-videos)).

| Segment | Pain and frequency | Adjacent spend today | How viewers receive it | Role |
|---|---|---|---|---|
| Pre-seed/seed founders raising | Acute; 12 weeks–6 months per raise, ~1.9 years between rounds | DocSend $10–65/user/mo; freelance explainer $200–2,000 one-off | VCs see AI-made pitch content as a negative signal | Acquisition wedge plus one-time raise pass |
| Seed–Series A B2B startups, founder-led sales | Moderate; every prospect, every week | Loom $15–24, DocSend, Gamma, Storylane $40–50/seat | 61–67% of buyers prefer rep-free research | **Beachhead** |
| Small agencies and consultancies | Moderate; many client links | Qwilr $35–39/user; white-label agent platforms $197–497/mo (verify) | Client-facing | **Second segment**, white-label |
| Coaches, creators, solo experts | Continuous, small budgets | Delphi $79–399/mo | Fans and followers | Skip; Delphi and Coachvox own it |
| Job seekers | Episodic, low willingness to pay | Little | Recruiters screen with AI | Skip |
| Accelerators and VCs | No evidence of license budgets | Perks bundles | Cohort founders | Distribution channel only |
| Real estate agents | Recurring per listing | $350–750 per listing video; AI tools $59–249/mo | Home buyers | Defer; separate go-to-market and weak indie conversion |

### Investors give a deck about two minutes and distrust AI stand-ins

The most-quoted benchmark, **3 minutes 44 seconds per seed deck**, comes from DocSend's 2015 study. 2026 summaries still repeat it ([Hummingdeck](https://hummingdeck.com/blog/pitch-deck-benchmarks-2026)). More recent readings are lower:

- **2 minutes 12 seconds** in 2023 ([TechCrunch](https://techcrunch.com/?p=2592727));
- 2:24 in Q4 2023 ([GuruFocus/PR Newswire](https://m.gurufocus.com/news/2154228/));
- 1:56 in a May 2026 promotional release that described a market "flooded with AI-generated submissions" ([press release](https://www.myknoxcountynews.com/online_features/press_releases/article_1f0551b9-cec9-5b2e-b8a6-5297b0879e40.html)).

Plan for about two minutes of investor attention. A 60–90 second narrated summary fits that window. A voice conversation does not.

Investor commentary in 2025–2026 is consistently hostile to AI-made pitch material:

- An early-stage VC wrote in Fast Company that AI-built decks "sound exactly like everyone else" ([Fast Company](https://www.fastcompany.com/91591431/ai-generated-pitch-decks)).
- An investor on Searchfunder said such decks signal "I outsourced my thinking to AI", with stigma attached "even if your deck just *looks* AI-generated" ([Searchfunder](https://searchfunder.com/post/investor-perspective-ai-generated-pitch-decks-really-hurt-your-credibility)).
- A March 2026 newsletter argued that "the in-person test still works, but only in a room, with follow-up questions, in real time" ([Monday Morning](https://mondaymorning.substack.com/p/ai-is-the-worst-thing-to-happen-to)).

Some investors are more nuanced. Mayfield's Navin Chaddha accepts AI-polished decks if founders edit and own them ([The Venture Lens](https://theventurelens.substack.com/p/ai-founders-vc)). The PitchBook account of Polsia shows the extreme case: an AI agent reportedly ran a $30M fundraise, but the same article notes that some VCs find agent-mediated contact rude ([PitchBook](https://pitchbook.com/news/articles/want-to-invest-in-my-startup-talk-to-my-agent)).

Investors are also moving toward reading decks with their own AI. VCs at firms such as EQT and Moonfire reportedly pre-screen decks with AI before a partner opens them ([The Venture Lens](https://theventurelens.substack.com/p/ai-founders-vc)) (verify). That means the "agent" investors actually use is often their own, reading the founder's materials, not the founder's chatbot.

There are trust risks too. Investor impersonation with AI-generated executives has already appeared in a federal indictment ([Lawyerd](https://lawyerd.net/blog/fake-vc-investor-impersonation-deepfake-scam/)). Even a HeyGen-focused blog concedes that slightly-off avatar gaze or timing "can create distrust" ([Mean CEO](https://blog.mean.ceo/heygen-news-october-2026/)).

### Buyers self-serve, but mostly through their own AI

The B2B viewer side is more welcoming, but with a twist.

**Buyers do their research in their own AI tools:**

- G2 reports that **51% of B2B software buyers now start research in an AI chatbot** more often than in Google, up from 29% in April 2025 ([G2 via PR Newswire](https://www.prnewswire.com/news-releases/new-g2-research-half-of-b2b-software-buyers-now-start-their-research-with-ai-chatbots-302742807.html)).
- Gartner found customers are **3x more likely to use third-party GenAI than a company's own chatbot**, and 87% say companies using GenAI must keep a human reachable ([The Next Web](https://thenextweb.com/news/gartner-customers-third-party-genai-over-company-chatbots)).

**On-site chat engagement is a minority behaviour.** The available benchmarks are weak and come from vendors:

- about 5–10% of visitors, and 10%+ on high-intent pages ([TRTC](https://trtc.io/blog/details/chat-widget-conversion-rate-v2));
- 8.99% in one Tidio retail case ([Tidio](https://www.tidio.com/blog/chatbot-statistics/));
- 3–8% for general qualification bots, rising to 10–20% for meeting-booking bots on high-intent pages ([ZoomInfo](https://pipeline.zoominfo.com/marketing/chatbot-metrics)).

Hacker News threads show that people hate chat windows that pop up uninvited. One commenter wrote, "the chatbot should never pop up on its own" ([HN](https://news.ycombinator.com/item?id=33905175)). A recent thread compared AI chatbots to the website-carousel fad ([HN](https://news.ycombinator.com/item?id=48072720)).

**Video helps if it is short.** Videos under one minute reach about 65% completion ([Vidico/Vidyard](https://vidico.com/news/b2b-video-marketing-statistics/)).

**No engagement data was found for voice agents embedded in websites or links.** The voice agent, the most distinctive part of the original idea, is therefore also the least supported by evidence.

For the product, this means:

- the narrated deck must carry the explanation;
- the Q&A should be opt-in;
- a "talk to the human" path must always be available;
- the content should also be machine-readable, so buyers' own AI can use it.

### Demand signals favor preparation tools, not AI proxies

The public demand evidence the researchers could reach clusters around tools that help founders prepare, where the founder stays in control:

- SaaStr's AI deck analyzer processed **700+ decks** soon after launch ([SaaStr](https://www.saastr.com/what-weve-learned-from-our-first-700-vc-pitch-decks-in-saastrs-new-ai-pitch-analyzer-the-data-is-brutal-and-eye-opening/)).
- Gatekeep, a tool for pitching to an AI investor persona, reported 30+ founders in about 63 days ([Indie Hackers](https://www.indiehackers.com/product/gatekeep)).
- Harvard Innovation Labs teaches founders to build ElevenLabs voice agents to rehearse VC meetings, not to stand in for them ([Harvard Innovation Labs](https://innovationlabs.harvard.edu/how-to/accelerate-your-startups-vc-fundraising-with-ai)).

Narrated async decks are established practice. The Supademo founder recommends sending "a short 5-min narrated version" of the deck ([Indie Hackers](https://www.indiehackers.com/post/a-step-by-step-playbook-to-raising-in-a-down-market-4e0b080831)). Gamma users keep asking for automatic voiceover export ([Gamma ideas](https://ideas.gamma.app/ideas/p/export-gammas-as-videos-with-automatic-voiceovers-eg-for-social-media-posts)). Curiosity about "talk to my AI clone" on LinkedIn is real: BlaBlaCar co-founder Frédéric Mazzella launched his clone "Fred24" live on LinkedIn, and other French Tech founders followed within days ([Cap Entreprendre](https://www.capentreprendre.fr/ces-pionniers-de-la-french-tech-devoilent-leur-clone-ia-revolutionnaire-pour-accompagner-les-entrepreneurs/)). That launch was positioned as mentorship, though, not as company explanation.

Two major gaps limit this picture. **Reddit could not be searched, and X/LinkedIn founder posts were not collected**, so the evidence lacks raw founder language from those channels. Founder interviews have to fill that gap before any build.

## Market: big adjacent categories, a crowded low end, fast bundling

### Analyst market sizes overlap and disagree by up to eightfold

No analyst category matches this product. The adjacent ones are large, growing and inconsistent with each other. Their scopes overlap, so the figures cannot be added together.

| Adjacent category | 2025 size estimates | Growth (CAGR) | Sources |
|---|---|---|---|
| AI video generators | $0.79B–$1.08B | 12.8–20.3% | [Grand View](https://www.grandviewresearch.com/press-release/global-ai-video-generator-market); [KSI](https://www.gii.tw/report/ksi1697395-ai-video-generator-market-forecasts-from.html) |
| Presentation software | $6.7B–$13.4B | 11.9–17.4% | [Coherent](https://cn.gii.tw/report/coh1705902-presentation-software-market-by-platform-by.html); [SkyQuest](https://www.gii.tw/report/sky1973346-presentation-software-market-size-share-growth.html); [TBRC](https://www.gii.tw/report/tbrc1706136-presentation-software-global-market-report.html) |
| Sales enablement | $2.4B (2024)–$5.9B | 12.3–20.2% | [GMI](https://www.gminsights.com/industry-analysis/sales-enablement-platform-market); [Mordor](https://www.researchandmarkets.com/reports/5026054/sales-enablement-platform-market-share); [Coherent](https://www.giikorea.co.kr/report/coh1812564-sales-enablement-platform-market-by-functionality.html) |
| Conversational AI | $13.2B (2024)–$17.05B | 19.6–24.9% | [MarketsandMarkets](https://marketsandmarkets.com/PressReleases/conversational-ai.asp); [MnM newer edition](https://www.marketsandmarkets.com/ResearchInsight/conversational-ai-market-size-share.asp) |
| AI avatars / digital humans | $0.8B–$6.3B | 29–33%+ | [MarketsandMarkets](https://www.marketsandmarkets.com/PressReleases/ai-avatar.asp); [GMI](https://gminsights.com/industry-analysis/ai-avatars-market) |

All of these are paid-report estimates whose methods the researchers could not see, so treat them as directional only.

**Company revenue is better evidence of willingness to pay:**

- Gamma reached about **$100M ARR profitably, with 600,000+ paying subscribers among ~70M users** (Nov 2025) ([The Outpost](https://theoutpost.ai/news-story/ai-presentation-startup-gamma-reaches-2-1-b-valuation-with-profitable-100-m-revenue-run-rate-21585/)). That implies about **$14/month per payer** and about **0.9% user-to-payer conversion**.
- HeyGen announced **$200M ARR in June 2026**, having doubled in about eight months ([HeyGen](https://www.heygen.com/blog/heygen-surpasses-200m-arr)).
- Synthesia is valued at $4B ([CNBC](https://www.cnbc.com/2026/01/26/nvidia-alphabet-vc-arms-back-synthesia.html)).

Overall spending is rising fast. Menlo Ventures estimates enterprise generative-AI spend tripled to $37B in 2025 ([Menlo Ventures](https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/)). Ramp's card data shows more than half of US businesses now pay for AI tools ([Ramp](https://assets.ramp.com/nextjs/files/spring-2026-business-spending-report.pdf)). Spending is concentrating in a few horizontal winners rather than spreading across small tools.

### Distribution and churn, not market size, cap a solo founder

There are two pools of potential customers:

- **Fundraising founders:** the pool is small and shrinking. The Carta figures above suggest the US has only low tens of thousands of companies actively raising pre-seed or seed in any year. That is an inference from instrument counts, since one company often issues several instruments.
- **B2B companies and service businesses:** the pool is huge. The US has **36.2M small businesses** ([SBA Advocacy](https://advocacy.sba.gov/?p=30239)) and 27.6M full-time independent workers ([MBO Partners](https://www.mbopartners.com/state-of-independence)). There are a reported ~71M LinkedIn company pages ([PromiseClick](https://www.promiseclick.com/blog/linkedin-statistics-2026)) (verify).

The market-sizing note built an illustrative serviceable market. It assumes 0.5–1% of LinkedIn company pages belong to active B2B marketers who would pay $20–50/month, which gives about **$85M–$425M ARR**. That is an assumption, not a sourced figure.

The target is tiny by comparison. $10k MRR needs about 345 customers at $29/month, 204 at $49 or 101 at $99. That is under 0.1% of even the low end of that range. **Market size is not the constraint. Acquisition and churn are.**

### Every layer of the product already has an owner

| Layer | Main players (Oct 2026) | Evidence of scale | Implication |
|---|---|---|---|
| Content → deck | Gamma, Microsoft Copilot, Gemini in Slides, Canva, Beautiful.ai, Pitch | Gamma ~$100M ARR; Gamma 5 rebuild launched Oct 6, 2026 ([Business Wire](https://www.businesswire.com/news/home/20261006266441/en/Gamma-Launches-Gamma-5-to-Eliminate-the-AI-Smell-From-AI-Generated-Content)) | Commodity; build on it, don't compete with it |
| Content/URL → narrated or avatar video | HeyGen, Synthesia, Google Vids, NotebookLM, Lumen5/Pictory/InVideo | HeyGen's explainer tool takes a pasted URL ([HeyGen](https://www.heygen.com/tool/ai-video-explainer)); Synthesia takes files or URLs ([Synthesia](https://www.synthesia.io/tools/explainer-video-maker)) | Commodity; rent it through an API |
| "Talking pitch deck" lookalikes | DeckChat, Interactpitch, SendNow, Pitch Avatar, dataroom.pro, Dataroomed, Peony, Tars | No disclosed funding or traction; prices €0–99 or $9–79 ([DeckChat](https://deckchat.io/); [SendNow](https://sendnow.live/blog/docsend-vs-sendnow); [Pitch Avatar](https://pitchavatar.com/pricing/)) | Crowded at the feature level; weak willingness to pay |
| Clone and live-avatar agents | Delphi, Tavus, HeyGen LiveAvatar, D-ID, Miria | Delphi ~$19M raised ([StartupIntros](https://startupintros.com/orgs/delphi)); Tavus $40M Series B ([Sacra](https://sacra.com/c/tavus/)) | Rentable infrastructure; Delphi already offers shareable "talk to me" profiles |
| Interactive demos with AI agents | Storylane (RepX), Supademo (Demo Agents), Navattic (Agent Demos beta), Arcade | Storylane $10M ARR ([ARR Club](https://www.arr.club/storylane/storylane-reaches-10m-arr)); Supademo ~$4M ARR ([Latka](https://getlatka.com/interviews/supademo-joseph-lee-2026)) | Same pattern applied to software demos; the most likely fast followers |
| Digital sales rooms with buyer-facing AI | Aligned (Buyer-Assist), Dock, Trumpet, Qwilr | Aligned $60M Series B, Jul 2026 ([Everything PR](https://everything-pr.com/aligned-raises-60-million-series-b-for-ai-b2b-sales-workspace)) | Buyer Q&A is becoming a standard feature |
| Free substitutes | NotebookLM public notebooks, Chatbase Agent Page, ElevenLabs Agents free tier | Chatbase $10M ARR, bootstrapped ([Stripe](https://stripe.com/customers/chatbase)) | "80% of the idea for free" baseline |

**The closest substitute is free.** NotebookLM lets users share a notebook publicly by link, in a chat-only or full view ([9to5Google](https://9to5google.com/2025/06/03/notebooklm-public-links/)). It generates narrated Video Overviews from uploaded sources ([Google Workspace Updates](https://workspaceupdates.googleblog.com/2025/07/video-overviews-studio-panel-updates-notebooklm.html)). Since March 2026, each visitor's chat in a shared notebook is private to them ([Google Workspace Updates](https://workspaceupdates.googleblog.com/2026/03/new-ways-to-customize-and-interact-with-your-content-in-NotebookLM.html)). Its limits for this use case:

- public sharing works only from consumer accounts ([NotebookLM Help](https://support.google.com/notebooklm/answer/16454555));
- it carries Google branding;
- it has no lead capture or analytics.

**The gap left by all of the above is real but shallow.** No single player was found that combines all seven of these:

1. raw, unstructured content as input;
2. no recording by the founder;
3. an auto-generated narrated explainer;
4. a voice and chat agent grounded in that content;
5. a branded page built for social sharing;
6. visitor analytics and lead capture;
7. self-serve pricing.

Each piece belongs to a well-funded company that could add the rest:

- Gamma lacks narration and has said it has "no current plans" for it, in an undated reply.
- HeyGen has both a URL-to-explainer tool and LiveAvatar.
- Synthesia is building conversational agents ([The Deep View](https://www.thedeepview.com/articles/synthesia-doubles-to-usd4b-preps-ai-video-agents)).
- Supademo made its Demo Agents self-serve in August 2026, with about 70 free conversations per workspace ([Supademo](https://supademo.com/blog/product-update-august-recap)).

### Price anchors cluster at $10–65 a seat while AI agents move down-market

| Product | Entry price (per month) | Upper tiers (per month) | Notes |
|---|---|---|---|
| Gamma | Plus ~$8–10; Pro ~$15–20 | Ultra ~$90–100 | Sources conflict ([eesel](https://www.eesel.ai/en/blog/gamma-pricing)) |
| DocSend | Personal $10–15; Standard $45–65 | Advanced $150–250 (3 users); Data Rooms $180–300 | Annual vs monthly billing ([DocSend](https://www.docsend.com/pricing/)) |
| Loom | Business $15–18 | Business + AI $20–24 | ([Trainn](https://trainn.co/blog/loom-pricing/)) |
| HeyGen | Creator $24–29 | Pro $49; Business $149 | ([Konabayev](https://konabayev.com/blog/heygen-pricing/)) |
| Storylane | Starter $40–50/seat | Growth $500+; RepX AI agent from $2,000 | Competitor-sourced ([Supademo blog](https://supademo.com/blog/storylane-alternatives)) |
| Chatbase | Hobby $32–40 | Standard $120–150; Pro $400–500 | ([Chatarmin](https://chatarmin.com/en/blog/chatbase-pricing)) |
| Delphi | Builder $79–99 | Scaler $299–399 | ([David Riha](https://davidriha.com/blog/delphi-vs-buddypro-2026/)) |
| Tavus (live video agent) | ~$59 for 100–175 min | $397–975 | ([usagepricing](https://www.usagepricing.com/tools/pricing-calculator/tavus)) |
| DeckChat / SendNow / Pitch Avatar | €29 / $9–17 / $29 | €99 / $43 / $79 | The direct lookalikes |
| Qwilr / Storydoc | $35–39 per user / $19.80 | Storydoc Pro $36 | ([Verdocs](https://verdocs.com/blog/qwilr-pricing); [AnyGen](https://www.anygen.io/showcase/storydoc-review/index.html)) |

All prices except DocSend's come from third-party pages (verify). Two things stand out:

- **The direct lookalikes price at or below $29**, which says founders will not pay much for "chat with my deck" on its own.
- **AI sales agents are moving from premium to commodity within one year.** Storylane's RepX starts at $2,000/month, while Supademo now gives away about 70 agent conversations.

### Five trends shape what can survive

**1. Bundling is turning the core output into a free feature.**

- NotebookLM added Video Overviews in July 2025.
- It added "Cinematic" overviews in March 2026 and 60-second "Short Video Overviews" in June 2026 ([TechMyMoney](https://techmymoney.com/2026/07/04/notebooklm-short-video-overviews-turn-dense-documents-into-60-second-clips/)).
- Gemini builds Slides decks from Drive context (July 2026) ([Google Workspace](https://workspace.google.com/blog/product-announcements/july-2026-workspace-feature-drop)).
- Google Vids added AI avatars to Slides-to-video conversion in May 2026 ([Google Workspace Updates](https://workspaceupdates.googleblog.com/2026/05/add-avatars-when-you-convert-presentations-to-Vids.html)).

**2. Value is concentrating in a few winners, and novelty products are dying.**

- Tome had 20M+ users but **under $4M ARR**. It shut its presentation product on April 30, 2025 ([Sacra](https://sacra.com/chat/h/5e9af049-ca7f-4b2a-924a-cf5df305fed9); [Deckary](https://deckary.com/blog/tome-review)).
- Pitch cut most of its staff and pivoted to sales enablement ([Sacra](https://sacra.com/research/pitch)).
- Jasper's growth stalled after customers swapped $50 subscriptions for ChatGPT ([Sacra](https://sacra.com/research/copy-ai-jasper-ai-writing-tools)).
- Chat-with-PDF tools were hit when ChatGPT added PDF upload ([Decrypt](https://decrypt.co/203920/openai-pdf-chatbot-ai-startups-sherlocked)).
- In 2026, voice-clone startup LOVO filed for Chapter 7, Weights closed, and the Sora app shut down ([TechCrunch](https://techcrunch.com/2026/09/15/the-ai-graveyard-a-running-list-of-projects-and-startups-that-didnt-make-it/)).

Every survivor moved toward a sales workflow.

**3. AI costs keep falling, but the underlying models are unstable.**

- OpenAI cut realtime audio prices 60% in December 2024 and about 25% again in August 2025 ([Forasoft](https://www.forasoft.com/blog/article/openai-realtime-api-pricing)).
- OpenAI also **removed the Sora video API on September 24, 2026, with no successor** ([Make.com](https://help.make.com/openai-sora-and-video-modules-deprecation-by-september-24-2026)).
- Some Gemini prices double on January 1, 2027 ([Vertex AI pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing)).

**4. LinkedIn is a poor host for a product whose output is a link.**

- Richard van der Blom's 2026 analysis of 1.3M posts found **reach down 60% for active creators over two years** ([Creator Science podcast](https://www.castfox.net/podcast/creator-science-with-jay-clouse-111713/episode/307-richard-van-der-blom-the-state-of-linkedin-in-2026-based-on-data-from-13-million-posts-2124510)).
- Posts with external links lose reach. Estimates are **18.8%** ([Agility PR](https://www.agilitypr.com/pr-news/social-media-influencer-marketing/the-linkedin-link-tax-why-sharing-your-blog-is-costing-you-60-percent-of-your-audience/)), **26.5%** ([Ordinal](https://www.tryordinal.com/blog/linkedin-link-penalty-study)) and about **half of median impressions** ([MagicPost](https://magicpost.in/blog/linkedin-external-links-reach)).
- Document posts average 2,639 views against 887 for video ([Magnettu](https://www.magnettu.com/en/blog/what-works-on-linkedin-in-2026)).
- Company pages engage less than personal profiles, 1.74% vs 2.6% ([Justpollen](https://justpollen.com/blog/linkedin-statistics-2026)).

**5. The "AI churn wave" punishes cheap tools.** ChartMogul and Kyle Poyar's December 2025 report found that AI products **under $50/month keep about 23% of revenue after a year**. The figure is **45% at $50–249 and 70% above $250** ([Userpilot summary](https://userpilot.com/blog/customer-churn/); [Gainsight](https://www.gainsight.com/episode/why-100m-ai-companies-are-failing-at-renewals-ft-cassie-young-kyle-poyar/)) (verify). This one finding does more than any other to set the pricing recommendation.

## Product: a four-to-eight-week build with costs hidden in voice and avatars

### A solo developer can ship an MVP in four to eight weeks

Every component is a commodity API. The product note's recommended stack:

- **Fact sheet and script:** Claude Sonnet 5.5 turns pasted content into a structured fact sheet that the founder edits, plus a deck and narration script. It costs $2/$10 per million tokens, read directly from Anthropic's pricing page ([Anthropic](https://platform.claude.com/docs/en/about-claude/pricing)).
- **Viewing:** a themed HTML slide player with ElevenLabs or Cartesia narration, so no video rendering is needed.
- **MP4 export:** Remotion, free for companies of up to three people ([Remotion](https://www.remotion.dev/docs/license/pricing)), or Shotstack at $0.05–0.20 per rendered minute ([Shotstack](https://shotstack.io/pricing/)).
- **Q&A:** text chat on Haiku 5.5 or Gemini Flash-Lite over the fact sheet.
- **Voice:** hosted, through ElevenLabs Agents or OpenAI Realtime-mini over WebRTC.

The note's build sequence:

| Week | Work |
|---|---|
| 1 | Ingestion and fact-sheet extraction |
| 2–3 | Deck player and per-slide narration |
| 3–4 | Grounded chat with citations, share page, analytics and email capture |
| 5 | Hosted voice with minute caps |
| 6 | Billing, metering, auth and rate limits |
| +1–2 | Buffer |

**A polished v1 takes about 3–5 months.** It adds brand templates, MP4 export, an optional avatar intro with consent capture, a founder approval workflow and numeric-claim checker, fundraising mode, CRM exports, EU disclosures and a provider-abstraction layer. These timelines are judgment-based. No case study of this exact build was found.

The hard parts are mostly not API work. In rough order:

1. **Generic-looking output.** Gamma's October 2026 relaunch was literally framed around eliminating "the AI smell".
2. **Faithful numbers.** Traction figures and terms need deterministic checks.
3. **Voice latency.** The best measured stacks still take about **0.8–1.3 seconds** to the first audio of a reply, and phone p95 runs up to about 1.8 s ([softcery](https://softcery.com/lab/ai-voice-agents-real-time-vs-turn-based-tts-stt-architecture); [openbenchmarks](https://openbenchmarks.com/voice-agent-latency)).
4. **Robust ingestion** of messy websites and image-only PDFs.
5. **Metering and abuse control.**
6. **Vendor churn.** The product note expects at least one media vendor swap per year.

For someone building a portfolio of apps, that last point matters. This product carries more ongoing maintenance than a typical micro-SaaS.

### Slides plus narration cost under $2; avatars and live voice need meters

Cost to produce one 2.5-minute explainer, from the product note's component math:

| Production path | Cost per 2.5-min explainer | With realistic re-renders |
|---|---|---|
| Slides + TTS narration (web player or MP4) | **$0.30–1.50** | $0.60–2.00 |
| Slides + 20–30 s avatar intro | $1–3 | $2–5 |
| Full avatar presenter (HeyGen, Synthesia, D-ID, Tavus) | $2.50–12.50 | $5–25 |
| Fully generative video (Veo, Kling, Runway) | $7.50–90 | $19–225 |

Generative video also cannot reliably render accurate charts or product screens, so it fails on content as well as cost. Avatar API prices come from third parties, for example HeyGen at about $3/min for Avatar IV/V ([realtimeavatar.ai](https://realtimeavatar.ai/blog/heygen-api-pricing-explained)) (verify).

Cost per minute of visitor conversation:

| Mode | Cost per conversation minute |
|---|---|
| Text chat, Claude Haiku 5.5 | ~$0.0013 |
| Text chat, Claude Sonnet 5.5 | ~$0.025 |
| Voice, OpenAI Realtime mini / flagship | $0.02–0.05 / $0.06–0.11 ([Forasoft](https://www.forasoft.com/blog/article/openai-realtime-api-pricing)) |
| Voice, ElevenLabs Agents | ~$0.09 ($0.16 in burst) ([CloudZero](https://www.cloudzero.com/blog/elevenlabs-pricing/)) |
| Voice, Vapi or Retell all-in | $0.10–0.31 ([CloudTalk](https://www.cloudtalk.io/blog/how-much-does-voice-ai-cost/)) |
| Live avatar, HeyGen LiveAvatar (reported) | ~$0.10–0.20 ([The Rundown](https://www.therundown.ai/tools/heygen-labs-interactive-avatar)) |
| Live avatar, Tavus | ~$0.24–0.37 ([usagepricing](https://www.usagepricing.com/tools/pricing-calculator/tavus)) |

The product note modelled gross margin at four price points. It assumed 20% of visitors open chat and 10% start voice. The last row is this report's own calculation for the recommended Pro plan, using the same inputs.

| Plan | Includes | Visitors/mo | Cost per customer | Gross margin after card fees |
|---|---|---|---|---|
| $19 | Narrated deck, chat only | 200 | $3–4.50 | 72–79% |
| $49 | + voice agent | 500 | $12–21 | 54–72% |
| $99 | + avatar video | 1,000 | ~$49 | ~47% |
| $299 | + live avatar | 2,000 | ~$189 | ~34% |
| **$79 Pro (recommended)** | Narrated deck, chat, 60 voice minutes capped | 500 | ~$12–15 incl. fees | **~81–85%** |

**Text chat plus narrated slides is a normal high-margin SaaS product. Voice works if the minutes are capped. Avatars only work as paid add-ons.**

The engagement assumptions above are two to four times the 5–10% chat benchmarks cited earlier. That means costs are probably overstated, but so is the share of visitors who will ever use the agent.

### A viral post can burn 35 months of revenue in voice minutes

The product note's spike model assumes 8% of visitors start voice and talk for 4 minutes:

| Visitors | Voice minutes | ElevenLabs ($0.09) | ElevenLabs burst ($0.16) | Live avatar ($0.30) | Text chat only |
|---|---|---|---|---|---|
| 5,000 | 1,600 | $144 | $256 | $480 | ~$38 |
| 20,000 | 6,400 | $576 | **$1,024** | **$1,920** | ~$152 |

Against a $29 plan, $1,024 of burst-priced voice is 35 months of revenue. Live avatar at 20,000 visitors is 66 months.

Concurrency is the second failure mode. Vapi includes 10 concurrent calls, Retell 20 and Tavus 3–10 ([ainora](https://ainora.lt/blog/ai-voice-agent-cost-per-minute-2026)), so a spike either fails or pays burst rates.

Comparable products all meter usage:

- ElevenLabs uses minute pools plus burst pricing.
- Chatbase sells message credits and charges $99/month to remove its badge ([resolve247](https://resolve247.ai/blog/chatbase-pricing/)).
- Delphi creators cap messages and voice minutes per user.

The product therefore needs these guardrails:

- a hard monthly minute pool per workspace, falling back to chat when it runs out;
- per-session caps;
- an email gate before voice starts, which doubles as lead capture;
- bot protection;
- top-up packs priced at least 3x cost;
- voice off by default.

### Paid acquisition only pencils out above $50 a month

Lifetime revenue per customer at three price points:

| Price | Monthly revenue churn | Lifetime revenue |
|---|---|---|
| $29–49 | ~11.5% (the 23% annual retention band) | ~$250–430 |
| $79 | ~6.4% (the 45% band) | ~$1,230 |
| $89 | ~6.4% | ~$1,390 |

Self-serve SMB customer acquisition costs are about $300–1,500 ([SaaS Hero](https://saashero.net/google-ppc/saas-cac-benchmarks-2026/)). Product-led companies with contracts under $500 a year report about $280–420 ([Stealth Agents](https://stealthagents.com/research/startup-cac-payback-period-benchmarks-2026)) (verify).

At sub-$50 pricing, the business must grow entirely organically. Above $50, small paid experiments become possible.

### Fundraising mode concentrates the legal risk

**The chatbot's owner answers for what it says.** In *Moffatt v. Air Canada*, a Canadian tribunal held the airline liable for its chatbot's misstatement and rejected the argument that the bot was "a separate legal entity" ([ABA](https://www.americanbar.org/groups/business_law/resources/business-law-today/2024-february/bc-tribunal-confirms-companies-remain-liable-information-provided-ai-chatbot/)). The damages were small and the ruling binds no other court, but the logic transfers.

**US regulators are watching AI claims:**

- In July 2026 the FTC proposed a policy on "deceptive steering" by AI products ([Reed Smith](https://www.reedsmith.com/our-insights/blogs/viewpoints/102n7u7/ftc-proposes-policy-prohibiting-deceptive-steering-of-ai-products-and-services/)).
- The FTC settled with DoNotPay for $193,000 over untested AI capability claims ([Benesch](https://www.beneschlaw.com/insight/one-year-in-ftcs-operation-ai-comply-continues-under-new-administration-signaling-enduring-enforcement-focus/)).

**Securities law is the bigger issue for the original idea.**

- A public link that describes an offering is likely "general solicitation". One securities lawyer warns that a web page describing investment terms "can destroy your [506(b)] exemption" ([securitieslawyer101](https://www.securitieslawyer101.com/2026/08/14/rule-506b-vs-506c/)).
- That pushes founders into Rule 506(c), where every purchaser must be accredited and verified ([Paul Weiss](https://www.paulweiss.com/insights/client-memos/sec-staff-no-action-letter-on-exempt-offerings-with-general-solicitation-under-rule-506-c)).
- An agent that misstates traction to investors creates the most severe trust risk of anything in this report.

**EU and likeness rules add requirements:**

- **EU AI Act Article 50** has required chatbot disclosure and deepfake labelling since August 2, 2026. Systems already on the market must add machine-readable marking by December 2, 2026 ([Elevate](https://elevateconsult.com/insights/eu-ai-act-article-50-icp-impact/); [CSA](https://labs.cloudsecurityalliance.org/research/csa-research-note-eu-ai-act-article50-watermarking-deadline/)).
- The federal **NO FAKES Act** covering voice and likeness replicas advanced in the Senate in June 2026 but is not law ([Congress.gov](https://www.congress.gov/bill/119th-congress/senate-bill/4591)).
- GDPR obligations were not researched and need counsel.

For the product, this means:

- the agent answers only from founder-approved facts and cites its sources;
- every number in an answer must match the fact sheet, checked deterministically;
- valuation, terms, projections and investor names are refused outright;
- there is a visible "AI assistant" disclosure;
- fundraising links are private and issued per investor by default.

These requirements are a key reason to make fundraising a guarded add-on rather than the core product.

### Moats accumulate around the link, not inside the generator

Model quality, voices and avatars are rented and improving for everyone, so they are no moat. The plausible advantages, in order:

1. **A "Made with" badge loop.** It drove about 30% of Supademo's signups ([Latka](https://getlatka.com/interviews/supademo-joseph-lee-2026)) and is central to Gamma's growth ([GTM Newsletter](https://thegtmnewsletter.substack.com/p/how-gamma-grew-to-100m-arr-and-a)).
2. **Question intelligence.** Which prospect watched what, what they asked, and where the pitch confuses people.
3. **A trust and governance layer.** Approved answers, an "I'll ask the founder" escalation, and audience-specific disclosure. Interactpitch users already complain about weak answers to rephrased questions and false "not in the deck" refusals ([Product Hunt](https://www.producthunt.com/products/interactpitch-2)).
4. **Workflow lock-in** through CRM and Slack integrations.
5. **An agent-readable company profile.** YC's Summer 2026 Requests for Startups ask for "software for agents" ([The VC Corner](https://www.thevccorner.com/p/yc-summer-2026-requests-for-startups-ideas)), and DocSend is beta-testing an MCP connector ([Peony](https://www.peony.ink/blog/top-10-alternatives-to-docsend)).

None of these is strong at launch. All of them strengthen with usage.

### Seven risks, ranked by how likely they are to kill the business

| Risk | Severity | Evidence | Mitigation |
|---|---|---|---|
| Episodic use and AI-tool churn | High | Raises last 3–6 months; sub-$50 AI tools keep ~23% of revenue after a year | Price above $50; target a weekly sales workflow; annual plans; pause instead of cancel |
| A big platform adds this as a feature | High | Gamma, HeyGen, Synthesia, Supademo, Storylane and Google each own most of the stack | Own the workflow (question intelligence, CRM alerts) and a niche segment. Niche survivors persist in the shadow of platforms: chat-with-PDF tool AI PDF reportedly made $1.7M in 2025 ([Latka](https://getlatka.com/companies/aipdf.com)). |
| Weak distribution | High | LinkedIn link penalty; viewers are rarely creators; paid acquisition can't pay back below $50 | One-to-one follow-ups as the main channel; native LinkedIn exports; free no-signup tool; accelerators and agencies as channels |
| Wrong answers and the liability they create | High in fundraising mode, medium in sales | *Moffatt v. Air Canada*; Reg D general solicitation; Interactpitch answer complaints | Approved-fact grounding, numeric checks, refusals, disclosure, private investor links |
| Variable cost spikes | Medium | $1,024–1,920 for one 20k-visitor spike; concurrency caps | Minute pools, email gates, top-up packs, voice off by default |
| Vendor deprecation and price changes | Medium | Sora API removed; GPT-5 mini/nano deprecated; Gemini prices doubling in 2027 | Provider-abstraction layer; no hard dependency on any one media model |
| Viewers distrusting avatars and synthetic voices | Medium | Deepfake scams; HeyGen-side admission of avatar distrust; EU disclosure duty | No avatar by default; the founder's real slides; clear "AI assistant" labelling |

## Where the notes disagree, and which numbers to verify

The six research notes broadly converge. Where they disagree, this report resolves the conflict as follows.

| Question | What the notes say | Resolution used in this report |
|---|---|---|
| Which segment to build for | The product and deck-competitor notes argue for differentiating through fundraising-specific trust and investor analytics. The customer, go-to-market, market and agent-competitor notes argue for B2B sales. | **B2B sales is the revenue base.** Fundraising features ship as a one-time raise pass, and the trust layer serves both segments. Fundraising has the better story but the worse economics: episodic use, a hostile audience and securities exposure. |
| Investor time per deck | 3:44 (DocSend 2015, still quoted in 2026); 2:12–2:24 (2022–23); 1:56 (May 2026 promotional release) | 3:44 is a stale figure being recycled. Plan for about two minutes. |
| LinkedIn link penalty | 18.8% (van der Blom), 26.5% (Ordinal), ~50% (MagicPost), "60%" (marketing blogs). LinkedIn's product leadership says there is no penalty ([ContentIn](https://contentin.io/glossary/external-link-penalty/)). | Large datasets show one-fifth to one-half less reach. Whatever the cause, the link post should not be the growth loop. |
| Best LinkedIn format | LinkedIn video viewership +36% (official, early 2025, [Digiday](https://digiday.com/marketing/linkedins-video-push-appears-to-be-working-in-2025/)) vs documents out-viewing video about 3:1 in 2026 third-party data | Growth in total video viewing does not mean more reach per post. Export a PDF carousel first and a short MP4 second. |
| Visitor engagement with Q&A | Benchmarks 3–10% (up to 20% on high-intent pages); the product note's cost model assumes 20% chat plus 10% voice | The cost model is conservative on cost and optimistic on value. The deck and the analytics must carry the product. |
| Free-to-paid conversion | Gamma ~0.9% of users become payers; B2B benchmarks 3–8% ([ChartMogul](https://chartmogul.com/reports/saas-conversion-report/); [Schematic](https://schematichq.com/blog/freemium-to-paid-conversion-saas)) | Gamma's rate counts 70M mostly casual users. Use 3–5% for a targeted B2B tool, and treat ~1% as the downside. |
| Indie revenue base rates | "Top 10% earn >$10k/month" (5,079 Stripe-verified TrustMRR projects, [Indie Hackers](https://www.indiehackers.com/post/i-analyzed-5-079-stripe-verified-startups-f0f6bd053f)) vs a 90th percentile of $5,107 (3,787 earning projects, [BigIdeasDB](https://bigideasdb.com/state-of-indie-saas-revenue-2026)) | The samples differ. Treat $5–10k MRR as a top-decile outcome. |
| Solo-founder revenue ceiling | Market note: $10–30k MRR is attainable. Go-to-market note: $1.5–3.5k MRR at month 12 in the base case. | Both are right. The first is a mature ceiling for the right positioning; the second is a year-one expectation. |
| Badge loop as the main moat | The product note ranks it first. The go-to-market note says viewers are investors and prospects, not creators, so the loop will be weaker than Gamma's or Calendly's. | Build the badge, but don't plan around it. It works best at demo days and when customers sell to other startups. |
| Live avatar and voice unit costs | Live avatar $0.10–0.20 (HeyGen, reported), $0.24–0.37 (Tavus), $0.56–1.09 (premium stacks, [LemonSlice](https://lemonslice.com/i/best-avatar-api)). Voice $0.02–0.42 depending on stack and telephony. | Plan for $0.09/min voice in the browser and $0.30/min live avatar. The conclusion (meter these) holds at any value in the range. |
| Do investors penalize AI decks? | VC commentary is negative, but a 2023 blind test found 80% of investors and owners rated GPT-4 decks convincing vs 39% for human decks ([Clarify Capital](https://clarifycapital.com/the-future-of-investment-pitching)) | A blind test hides who wrote the deck. A disclosed AI agent cannot hide, and EU Article 50 requires disclosure, so the stigma applies. |
| Scale of HeyGen, Synthesia, Chatbase | HeyGen ~$95M ARR (Sacra estimate, Sep 2025) vs $200M (company, Jun 2026); Synthesia $140–150M; Chatbase $8–10M | Mostly a matter of timing. This report uses the latest company-stated figures, which are unverified. |
| Sora API shutdown | "Reported" in the market note; confirmed in the product and agent notes ([TechCrunch](https://techcrunch.com/2026/03/24/openais-sora-was-the-creepiest-app-on-your-phone-now-its-shutting-down/)) | Treated as confirmed. |
| Minor conflicts | Tome's user count (20M vs 25M) and whether AngelList bought the Tome brand; Delphi's Series A date (June vs Aug 2025) and revenue share (15% vs 20%) | Immaterial to the verdict. |

**Figures to verify before relying on them.** Only Anthropic's pricing was read from the primary page. Everything else came from search-result summaries. The most load-bearing items to check:

- **ChartMogul's retention bands (23% / 45% / 70%).** These were read only through secondary summaries, and it is unclear whether "under $50" refers to price per account or list price.
- **All vendor prices.** Treat them as roughly ±25%. Most uncertain: Synthesia API pricing, the HeyGen LiveAvatar dollar rate, Tavus's current plan table, and a reported 20% ElevenLabs TTS price cut on October 5, 2026.
- **The LinkedIn link-penalty figures and the ~71M company-page count.**
- **NotebookLM's current sharing rules.** It is unconfirmed whether viewers need a Google sign-in, whether the reported July 2026 rename to "Gemini Notebook" is accurate ([notebooklm-guide](https://notebooklm-guide.com/notebooklm-updates/)), and what the Workspace account restrictions are now.
- **Gamma's undated "no current plans" reply on narration.**
- **Supademo's 30% badge share.**
- **The TrustMRR and BigIdeasDB base rates.**
- **Carta's round counts.** The full reports could not be fetched.
- **Gartner's 67% and G2's 51% buyer figures.**

Two questions need counsel, not more research: GDPR controller/processor obligations, and whether a password-protected per-investor link avoids general solicitation.

## Verdict: build a modified version, gated by cheap tests

**The six notes reach the same verdict: build only in a modified form.** The strongest case for the original idea:

- the pain is real and acute;
- clone launches on LinkedIn draw attention;
- high-profile founders already let AI field investor questions ([AOL](https://www.aol.com/articles/perplexitys-ceo-turns-ai-investor-061502941.html));
- no funded company owns "the one link that explains your startup";
- it is cheap to build.

But seven or more unfunded lookalikes plus an empty category more likely signal weak demand than open space. The money in "an agent that represents a company" has gone to tools tied to revenue: Aligned ($60M), 1mind ($40M, [Forbes](https://www.forbes.com/sites/gemmaallen/2026/01/25/inside-1minds-40m-ai-bet-and-the-superhuman-vision-behind-it/)) and Supersonik ($5M from a16z, [EU-Startups](https://www.eu-startups.com/2025/09/spanish-startup-supersonik-launches-from-stealth-and-raises-e4-2-million-for-its-multilingual-ai-agent/)). Fundraising tools have not drawn that money.

### Segment and positioning

**Target customers:**

- **Primary:** seed-to-Series A B2B startups of roughly 2–20 people where a founder still sells a technical or complex product.
- **Secondary:** the small marketing, development and consulting agencies that serve them, who can resell under their own brand.

**Positioning:** "the follow-up link that answers a prospect's questions and tells you what they asked." Do not position it as an AI avatar, a voice clone or a pitch-deck chatbot.

**How it works:**

1. The founder pastes their website, deck, notes, case studies and pricing.
2. The product drafts a fact sheet, which the founder edits and approves.
3. From that fact sheet it generates:
   - a 60–90 second narrated deck: slides plus TTS, with no avatar by default and no recording;
   - an opt-in Q&A that cites its sources and escalates anything off-sheet to the founder;
   - a per-viewer summary of what each prospect watched and asked, pushed to email, Slack or the CRM.

**Distribution:** the main channel is one-to-one follow-up after calls and in outbound, where LinkedIn's link penalty doesn't apply. LinkedIn becomes an export target: a native PDF carousel and a short MP4, with the link in comments or the profile.

**Fundraising** becomes a mode, not the product. It provides private per-investor links, no search indexing, hidden terms, hard refusals on valuation and projections, and investor-level analytics.

**Feature priorities:**

- **Voice:** a metered add-on.
- **Live avatars and generative video:** off the roadmap until paying customers ask for them.
- **Agent-readable profile** (structured data or MCP, so buyers' and investors' own AI can query the company): a month-four experiment, not a launch feature.

### Pricing

| Plan | Price | Includes | Why |
|---|---|---|---|
| Free | $0 | 1 link with "Made with" badge, narrated deck, capped text chat, no voice | Feeds the badge loop; matches the NotebookLM baseline |
| Pro | **$79/month** (about $790/year) | 3–5 active links, question summaries, lead capture, Slack/CRM alerts, LinkedIn exports, branding, 60 voice minutes | Sits above the sub-$50 churn band. Anchored by DocSend Standard ($45–65), Delphi Builder ($79–99) and Pitch Avatar Business ($79). ~81–85% margin. |
| Team / Agency | **$199–299/month** | 15–25 links or client workspaces, white-label, custom domain, seats, 300 voice minutes | Anchored by Chatbase Standard ($150) and Supademo's implied ~$111 average per account. ~75–81% margin. |
| Raise Pass | **$99 one-time, 90 days** | Fundraising mode, private per-investor links, investor analytics, guardrails | Charges for the episodic need without pretending it is a subscription. Within the $49–149 range the customer note suggested. |
| Voice packs | e.g. 100 minutes for $15–25 | Top-ups | At least 3x unit cost |

Two retention mechanics are worth adding from launch:

- Offer **pause instead of cancel**. Vendor data suggests pausing beats discounts for long-term retention ([Churnkey](https://churnkey.co/blog/seasonality-patterns-in-business)).
- Push annual plans.

### Validation tests to run before writing product code

These tests cost a few hundred dollars and about three to four weeks. The pass thresholds are this report's own judgment calls.

| Test | How | Cost and time | Pass signal |
|---|---|---|---|
| 1. Problem interviews | 20 B2B founders doing founder-led sales plus 10 agency owners. Ask what they send after calls and in outbound, and what prospects ask repeatedly. | Time only; ~2 weeks | At least half send follow-up material every week, can list recurring prospect questions, and already pay for Loom, DocSend, Gamma or a demo tool |
| 2. Substitute test | In the same calls, show a free NotebookLM public notebook and a Gamma link built from their own content | $0–20 | Most name a specific gap they would pay to close (question log, lead alerts, branding). Stop if most say "good enough". |
| 3. Concierge pilot | Hand-build links for 5–10 companies with Gamma, ElevenLabs narration, a Chatbase Agent Page or ElevenLabs widget, and simple analytics. Charge $99–299 for setup and the first month. | ~$100–200 in tools; 2–3 weeks | At least 3 pay. Links reach real prospects. At least 5% of viewers open the Q&A, against the 5–10% benchmark. Founders read the question summary. |
| 4. Pre-sale page | Publish a landing page with Pro at $79, Agency at $249 and a $99 Raise Pass. Take discounted annual pre-orders or refundable deposits. | $50–300; 1–2 weeks | About 10 paid commitments from 50–100 qualified conversations |
| 5. Agency pitch | Offer a white-label pilot at $199–299/month to 15–20 agencies | Time only | At least 2 paid pilots |
| 6. Distribution micro-tests | Post the same content as a native PDF carousel and as a link post. Give one accelerator cohort free links for demo day. | ~$0 | Measurable badge signups from viewers. The carousel beats the link post. |

**Kill rule:** if tests 1–3 fail, do not build; move to the next app idea. If they pass, build the MVP.

### First 90 days

| Weeks | Focus |
|---|---|
| 1–3 | Tests 1–3 |
| 4 | Tests 4–5, then a go/no-go decision |
| 5–12 | Build the MVP in the product note's order: ingestion and fact sheet; narrated deck player; grounded chat with citations, analytics and lead capture; billing, metering and rate limits. Voice comes last, behind caps. |

Include two things from the first commit: the provider-abstraction layer and the EU "you are talking to an AI" disclosure.

**Launch channels:**

1. **Concierge customers.** Convert them to paid plans first.
2. **One accelerator cohort.** Founders there are both viewers and potential creators.
3. **Product Hunt.** Its audience is founders, but expect single-digit paying customers per launch. A #3 product of the day earned 7 purchases ([Product Hunt](https://www.producthunt.com/p/indiemerger/we-placed-3rd-on-product-hunt-and-earned-543)).
4. **A free, no-signup "explain my company from a URL" tool for search traffic.** This copies the Supademo playbook: free no-signup tools drove over half its traffic at 11–12% conversion ([StarterStory summary](https://onepage-research.sliplane.app/articles/starterstory.com/starterstory-supademo)).

**Month-6 checkpoint:** the go-to-market note sets $2–5k MRR six months after launch as the bar. Below roughly $2k, cut losses or fold the features into another app.

### Realistic MRR expectations

The scenarios below use this report's own model:

- signups ramp up linearly over the first three months;
- monthly revenue churn comes from ChartMogul's retention bands: 11.5% under $50 and 6.4% at $50–249.

The model is generous, because real launches often ramp more slowly.

| Scenario | Assumptions | Month 6 | Month 12 | Ceiling at that inflow |
|---|---|---|---|---|
| Base rate for any new AI micro-SaaS | TrustMRR/BigIdeasDB medians ([BigIdeasDB](https://bigideasdb.com/saas-revenue-benchmarks-by-category-2026)) | — | **~$150–200** | — |
| Original idea, with traction | 300 signups/mo, 4% convert, $39 ARPU, 11.5% churn | ~$1.8k | ~$3.0k | ~$4.1k |
| Original idea, fundraising-driven churn | Same inflow, 25% monthly churn | ~$1.4k | ~$1.8k | ~$1.9k |
| Modified, downside | 100 signups/mo, 3%, $79, behaves like a cheap tool (11.5%) | ~$0.9k | ~$1.5k | ~$2.1k |
| **Modified, base** | 200 signups/mo, 4%, $95 blended ARPU, 6.4% churn | ~$3.3k | **~$6.1k** | ~$11.9k |
| Modified, upside | 600 signups/mo, 5%, $95, 6.4% churn | ~$12.5k | ~$23k | ~$44.5k |

**Plan on $3–6k MRR at month 12 if validation passes.** Treat $10k+ as a top-decile result: only 2.4% of AI startups with reported figures have crossed $10k MRR ([BigIdeasDB](https://bigideasdb.com/ai-saas-revenue-reality-check-2026)). The upside case needs Supademo-like loops. Supademo reached about $1M ARR in 12 months, but it did so in 2023 with a recurring software-demo use case ([StarterStory summary](https://onepage-research.sliplane.app/articles/starterstory.com/starterstory-supademo)).

The original idea's ceiling is set by churn, not demand. At a fixed signup rate, revenue stops growing at about $2–4k MRR.

## Conclusion

The generated video and the voice agent, the parts of the idea that feel most novel, are the least valuable: Google gives them away, HeyGen and Gamma can add them in a quarter, and no evidence shows viewers want to talk to them. The part that compounds is the log of questions, which captures exactly what each prospect or investor wanted to know and where the story confused them. That makes the right product a lightweight, founder-friendly sales room that happens to generate its own content, not a video tool with a chatbot attached.

A second shift points further out. Buyers increasingly research through their own AI assistants, and investors pre-screen decks with AI. A chatbot hosted by the founder may therefore be a transitional form. The more durable asset could be a founder-approved, machine-readable company profile that serves humans as a narrated deck and AI agents as a structured endpoint. That is worth testing once the sales use case is paying.

For a solo founder building a portfolio of apps, this idea earns a time-boxed bet, not a default build. It costs three to four weeks to validate and four to eight weeks to build, needs more maintenance than a typical micro-SaaS because of vendor churn and disclosure rules, and has a realistic $10–30k MRR ceiling only if it sells to sellers.
