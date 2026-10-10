# Product / Tech Feasibility, Cost Structure & Unit Economics: "Paste your content, get a shareable link with an AI explainer video/deck plus a voice/chat Q&A agent"

Method note (read first): research date was 9 Oct 2026. The sandbox's egress policy blocked direct fetches of almost every vendor pricing page (openai.com, ai.google.dev, elevenlabs.io, heygen.com, tavus.io and others returned DNS errors or proxy 403s). The one exception was Anthropic's pricing page, which I read in full. Every other price comes from search-engine extracts. Some of those extracts quote the official page (Google's Gemini pricing page, OpenAI's model pages, Remotion/Shotstack/Creatomate docs). The rest come from third-party aggregators. The search summaries did not always tie each number to one URL. Where a finding lists several URLs, the figure came from at least one of them. Third-party prices are flagged, and the writer should treat them as roughly ±25% until checked against the vendor page. The web-search budget ran out before these were covered: video CDN/hosting prices, standalone STT (Deepgram), web scraping (Firecrawl), GDPR specifics, and state voice-clone laws (ELVIS Act, California AB 2602). They are listed as gaps.

---

## 1. Reference architecture options and current (Oct 2026) API pricing per component

### Takeaway
Every component exists as a commodity API. Text LLM cost is negligible at today's prices: Claude Haiku 5.5 costs $0.10/$0.50 per million tokens and Sonnet 5.5 costs $2/$10. Cost and risk sit almost entirely in **media**: avatar video at about $1–5 per rendered minute, generative video at about $0.05–0.60 per second, real-time voice at about $0.02–0.30 per conversation minute, and live avatars at about $0.25–0.37 per minute. Vendor churn is real. OpenAI shut down the Sora video API on 24 Sep 2026.

### Cited Findings

**Reference architecture (components the product needs)**
- Ingestion: URL scrape and PDF/doc parse, then an LLM structures the content into a "company fact sheet", a deck outline and a narration script. Output goes to either (a) an HTML deck plus TTS narration, (b) an MP4 rendered programmatically (Remotion/Shotstack/Creatomate), (c) an avatar presenter (HeyGen/Synthesia/D-ID/Tavus), or (d) generative B-roll (Veo/Kling/Runway). Q&A runs as RAG chat on an LLM, as a voice agent (speech-to-speech or STT→LLM→TTS on a platform such as ElevenLabs Agents, Vapi, Retell or LiveKit), or as a live avatar (Tavus CVI, HeyGen LiveAvatar). This architecture is my synthesis of the component categories priced below.

**LLMs: content structuring and RAG Q&A (per 1M tokens)**
- Anthropic (read directly from the official page, 9 Oct 2026). Claude Haiku 5.5: $0.10 input / $0.50 output for prompts up to 100K tokens ($0.50/$2.50 above that), with cache hits at $0.01. Claude Sonnet 5.5: $2 / $10, with cache hits at $0.10 and 5-minute cache writes at $2.50. Claude Opus 5.5: $4 / $20, with cache hits at $0.20. Claude Haiku 4.5: $1 / $5. — [Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing)
- Anthropic Batch API gives a 50% discount on input and output (for example, Opus 5.5 batch is $2/$10). — [Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing)
- Anthropic caveat: Claude 4.7 and later models use a newer tokenizer that produces "approximately 30% more tokens for the same text." — [Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing)
- OpenAI GPT-5.5 costs $5 input / $30 output, with cached input at $0.50. Prompts over 272K tokens are billed at 2x input and 1.5x output, and regional processing adds 10%. The model page was about 169 days old when indexed. — [OpenAI GPT-5.5 model page](https://developers.openai.com/api/docs/models/gpt-5.5)
- OpenAI GPT-5 mini costs $0.25/$2 and GPT-5 nano $0.05/$0.40. **Both are marked deprecated.** The nano page points new workloads to "GPT-5.6 Luna", but I found no price for Luna. — [GPT-5 mini](https://developers.openai.com/api/docs/models/gpt-5-mini); [GPT-5 nano](https://developers.openai.com/api/docs/models/gpt-5-nano)
- Google Gemini Developer API: Gemini 3.1 Flash-Lite costs $0.25 input (text/image/video), $0.50 input (audio) and $1.50 output. Gemini 3.5 Flash-Lite costs $0.30/$2.50. Gemini 2.5 Flash costs $0.30/$2.50. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)
- Vertex lists Gemini 3.6–3.8 Flash at introductory pricing of $0.75/$3.75 through 31 Dec 2026, rising to $1.50/$7.50 from 1 Jan 2027. Gemini 3.1 Pro Preview input costs $2.00 (output price not captured). — [Vertex AI pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing)
- Aggregators list Gemini 3 Flash at $0.50/$3 and Gemini 3.5 Flash at $1.50/$9 (third-party, Jul–Sep 2026). — [morphllm](https://www.morphllm.com/gemini-api-pricing); [benchlm](https://benchlm.ai/blog/posts/gemini-api-pricing)

**TTS / voiceover**
- ElevenLabs API TTS: most 2026 sources list $0.10 per 1K characters (Eleven v3, Multilingual v2) and $0.05 per 1K (Flash/Turbo). A tracker snapshot dated 2 Oct 2026 shows $0.08 and $0.04, after a reported 20% TTS price cut on 5 Oct 2026. This is **unconfirmed** against the ElevenLabs page. — [unifically](https://unifically.com/blogs/elevenlabs); [goodvibecode (Sep 2026)](https://www.goodvibecode.com/text-to-speech/elevenlabs-api-pricing-explained); [usagepricing](https://www.usagepricing.com/blueprint/elevenlabs)
- OpenAI gpt-4o-mini-tts costs $0.60 input / $12.00 output per 1M tokens. Third parties estimate about $0.015 per minute of audio. **The model page marks it deprecated.** — [OpenAI gpt-4o-mini-tts](https://developers.openai.com/api/docs/models/gpt-4o-mini-tts); [costgoat](https://costgoat.com/pricing/openai-tts)
- Cartesia Sonic bills about 1 credit per character. Plans: Free gives 20K credits with no commercial use. Startup is $49/month for 1.25M credits, about $39 per 1M characters. Scale is $299/month for 8M credits, about $37 per 1M characters. Credits expire monthly. — [cloudtalk](https://www.cloudtalk.io/blog/cartesia-pricing/); [eesel](https://www.eesel.ai/blog/cartesia-sonic-3-pricing); [texttolab](https://texttolab.com/blog/cartesia-pricing)
- Gemini 3.8 Flash-Lite TTS costs $0.50 per 1M text input tokens and $6.00 per 1M audio output tokens through 31 Dec 2026, and both prices double from 1 Jan 2027. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)

**Avatar video generation (pre-rendered)**
- HeyGen API uses a prepaid USD wallet (minimum $5) billed per second. Photo Avatar (Avatar IV/V) costs about $0.05/sec (about $3/min). Digital Twin and Studio Avatar cost about $4/min at 1080p, and Video Agent about $2/min. Reportedly there have been no free API credits since Feb 2026. — [realtimeavatar.ai](https://realtimeavatar.ai/blog/heygen-api-pricing-explained)
- HeyGen Avatar III via API is reported at $1/min (720p/1080p) or $1.20/min (4K) (third-party). — [diyai.io](https://diyai.io/ai-tools/video-generation/heygen-pricing/); [eesel](https://www.eesel.ai/blog/heygen-pricing)
- Synthesia API: sources conflict. One reports $1/min (Avatar III, 1080p) up to $5/min (Avatar IV Digital Twin, 4K). Another reports 75 credits per minute, estimated at $2–3/min. API write access may require the Creator or Enterprise tier. — [creatify](https://creatify.ai/blog/synthesia-pricing-(2026)-plans-credits-and-what-you-ll-actually-pay); [autogpt.net](https://autogpt.net/synthesia-api/); [aitoolsdevpro](https://aitoolsdevpro.com/ai-tools/synthesia-guide/)
- D-ID API access reportedly starts on the Build plan ($14.40/month). Bulk credits are reported at about $1.80/min (third-party, single source). — [digen.ai](https://resource.digen.ai/d-id-vs-synthesia-pricing-comparison-2026/)
- Tavus pre-rendered video is metered at $1/min (Builder), $0.90/min (Growth) and $0.80/min (Business), per an Aug 2026 snapshot. — [usagepricing Tavus](https://www.usagepricing.com/tools/pricing-calculator/tavus); [dreaming.press](https://dreaming.press/stack/tavus)

**Programmatic slide/motion video rendering**
- Remotion is free for individuals and organisations of up to 3 people. Companies pay either "Automators" at $0.01 per render (billed in blocks of 1,000, minimum $100/month) or "Creators" at $25 per seat per month. Enterprise starts at $500/month. Compute (for example, Lambda) is not included. — [Remotion License & Pricing](https://www.remotion.dev/docs/license/pricing); [Remotion License FAQ](https://www.remotion.dev/docs/license/faq)
- Shotstack bills per rendered minute. Pay-as-you-go is 50 minutes for $10 ($0.20/min). Monthly plans run from $39 for 250 minutes ($0.156/min) to $499 for 10,000 minutes ($0.05/min). Overage reportedly costs 30% more. — [Shotstack pricing](https://shotstack.io/pricing/); [spotsaas](https://www.spotsaas.com/product/shotstack/pricing)
- Creatomate tiers: Essential is $54 for 2,000 credits, Growth $129 for 10,000, and Beyond $329 for 50,000. About 14 credits buy 1 minute of 720p/25fps video, and the cost scales with resolution and fps. — [Creatomate pricing docs](https://creatomate.com/docs/account/how-does-the-pricing-work); [json2video comparison](https://json2video.com/how-to/creatomate-alternative/)

**Generative video (price per second of output)**
- Google Veo 3.1 Standard costs $0.40/s (720p/1080p) and $0.60/s (4K). Veo 3.1 Fast costs $0.10 (720p), $0.12 (1080p) and $0.30 (4K). Veo 3.1 Lite costs $0.05 (720p) and $0.08 (1080p). There is no free tier. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)
- **OpenAI Sora API is gone.** OpenAI notified developers on 24 Mar 2026 that the Videos API and all sora-2 and sora-2-pro aliases would be removed on 24 Sep 2026, with no replacement model listed. The consumer Sora app shut down on 26 Apr 2026. Before shutdown, sora-2 cost about $0.10/s at 720p and sora-2-pro $0.30–0.50/s. — [Make.com deprecation notice](https://help.make.com/openai-sora-and-video-modules-deprecation-by-september-24-2026); [invideo](https://invideo.io/blog/sora-ai-video-generator/); [eesel (prior pricing)](https://www.eesel.ai/blog/sora-2-pricing)
- Runway API credits cost $0.01 each, with a $10 minimum top-up. Gen-4 Turbo costs about $0.05/s, and Gen-4 or Gen-4.5 about $0.12/s. Sources conflict on Gen-4.5. — [apiframe](https://apiframe.ai/guides/runway-api-guide); [unifically](https://unifically.com/blogs/runway-gen-4)
- Kling 3.0 list prices are $0.084/s (720p), $0.112/s (1080p) and $0.42/s (4K). Kling 3.0 Turbo is $0.112/s (720p) and $0.14/s (1080p). One unit costs $0.14. — [costbench](https://costbench.com/software/ai-media-apis/kling-api/); [aireiter](https://aireiter.com/blog/kling-api-pricing)

**Real-time voice agents**
- OpenAI Realtime flagship ("gpt-realtime-2" on the pricing page; later coverage calls it 2.1) costs $32 audio input, $0.40 cached input and $64 audio output per 1M tokens. — [OpenAI pricing](https://openai.com/api/pricing/); [forasoft](https://www.forasoft.com/blog/article/openai-realtime-api-pricing)
- gpt-realtime-2.1-mini costs $10 input, $0.30 cached input and $20 output per 1M tokens. Older tables listing it at $0.60/$2.40 conflict with this. — [OpenAI pricing](https://developers.openai.com/api/docs/pricing); [layer3labs](https://www.layer3labs.io/guides/openai-realtime-api-pricing)
- Third-party per-minute estimates: realistic flagship cost is about $0.06–0.11/min and mini about $0.02–0.05/min once caching works. Flagship output audio alone is about $0.077/min, assuming about 1,200 audio tokens per minute of speech. — [forasoft](https://www.forasoft.com/blog/article/openai-realtime-api-pricing); [eesel](https://www.eesel.ai/en/blog/gpt-realtime-mini-pricing)
- Gemini Live API: Gemini 2.5 Flash Native Audio costs $3 audio input and $12 audio output per 1M tokens. The 2.5 models are reportedly limited to prior users. On Vertex, Gemini 3.8 Live costs $3 audio input and $12 audio output. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing); [Vertex pricing](https://docs.cloud.google.com/vertex-ai/generative-ai/pricing)
- ElevenLabs Agents: overage costs $0.08/min, "burst" minutes above the concurrency limit cost $0.16/min, and text-only messages cost $0.003 each. LLM token cost is passed through separately. Included minutes range from 15 (free) to 12,375 (Business). — [cloudzero](https://www.cloudzero.com/blog/elevenlabs-pricing/); [pxlpeak](https://pxlpeak.com/blog/ai-tools/elevenlabs-pricing-guide); [cekura](https://www.cekura.ai/blogs/elevenlabs-pricing)
- Vapi charges a $0.05/min platform fee, and you bring your own STT/LLM/TTS keys, which add $0.08–0.25/min. All-in cost is about $0.10–0.30/min, and the plan includes 10 concurrent calls. — [cloudtalk](https://www.cloudtalk.io/blog/how-much-does-voice-ai-cost/); [ainora](https://ainora.lt/blog/ai-voice-agent-cost-per-minute-2026)
- Retell advertises from $0.07/min (voice infrastructure $0.055/min), excluding LLM and telephony. All-in cost is about $0.07–0.31/min, and pay-as-you-go includes 20 concurrent calls. — [cekura](https://www.cekura.ai/blogs/retell-ai-pricing-per-minute); [cloudtalk](https://www.cloudtalk.io/blog/how-much-does-voice-ai-cost/)
- LiveKit Cloud charges about $0.01 per agent-session minute beyond plan-included minutes. Models, telephony and observability are billed separately. — [dev.to calculator](https://dev.to/jareer_nauman_ba24aa80b87/how-much-does-a-voice-ai-agent-cost-per-minute-a-calculator-for-vapi-retell-and-livekit-26kb)

**Real-time interactive avatars**
- Tavus CVI, older/most-cited plans: Free gives 25 CVI minutes. Starter is $59/month for 100 minutes, 3 concurrent streams and $0.37/min overage. Growth is $397/month for 1,250 minutes, 10 concurrent streams and $0.32/min overage. — [rightaichoice](https://rightaichoice.com/tools/tavus); [therundown](https://www.therundown.ai/tools/tavus)
- Tavus CVI, newer table (visible pricing UI on 20 Aug 2026): Builder is $59/month for 175 minutes ($0.35 overage). Growth is $397 for 1,300 minutes ($0.31 overage). Business is $975 for 4,000 minutes ($0.26 overage). Overage is uncapped. — [usagepricing Tavus](https://www.usagepricing.com/tools/pricing-calculator/tavus); [dreaming.press](https://dreaming.press/stack/tavus)
- HeyGen LiveAvatar advertises 1080p avatars with "unlimited concurrency" and rates "falling to $0.01/min at scale", which is a top-tier marketing figure. A third party describes the credit mechanics: in FULL mode (HeyGen runs LLM, TTS and ASR) 1 credit buys 30 seconds, and in LITE mode (you bring your own AI stack) 1 credit buys 1 minute. — [LiveAvatar](https://www.liveavatar.com/); [realtimeavatar.ai](https://realtimeavatar.ai/blog/heygen-api-pricing-explained)

### Inferences
- **Recommended default architecture for a solo founder:**
  - Use Claude Sonnet 5.5 (or Opus 5.5 for one-off generation) to turn the content into a structured fact sheet and deck/script JSON.
  - Render the deck as an HTML/React web player with ElevenLabs or Cartesia narration, synced per slide. This is cheap, fast, editable, and needs no video rendering for viewing.
  - Offer MP4 export via Remotion (free while the company has ≤3 people) or Shotstack.
  - Run chat Q&A on Haiku 5.5 or Gemini Flash-Lite with RAG over the fact sheet.
  - Run voice through ElevenLabs Agents or OpenAI Realtime-mini via WebRTC.
  - Keep avatar and live avatar as premium add-ons. Use generative video only for short B-roll, if at all.
- At these prices, text-LLM choice matters little for margins. Model choice for the Q&A agent should optimise for **faithfulness and refusal behaviour**, not price.
- Deprecations are a recurring risk across vendors: the Sora API, GPT-5 mini/nano, gpt-4o-mini-tts and Gemini 2.5 native audio. A provider-abstraction layer, with no hard dependency on any single media model, is a requirement, not an optional extra.

### Gaps
- Could not fetch vendor pricing pages directly (egress blocked), so all non-Anthropic prices are search extracts. Most uncertain: the ElevenLabs Oct 2026 TTS cut, Synthesia API, D-ID, the HeyGen LiveAvatar credit price in USD, and Tavus's current plan table.
- No price found for OpenAI "GPT-5.6 Luna" or for current Gemini Pro output.
- Not researched because the search budget ran out: Deepgram/AssemblyAI STT per-minute prices for a cascaded pipeline, Pipecat (licensing/hosting), embedding prices, Firecrawl/Jina scraping prices, and video CDN prices (Cloudflare Stream, Mux).

---

## 2. Cost per 2–3 min explainer video, cost per visitor conversation minute, and gross margin at $19 / $49 / $99 / $299

### Takeaway
A slides-plus-voiceover video costs about **$0.30–2** to produce. A full avatar presenter costs about **$2.50–12.50 per render**, or $5–25 with one re-render. A fully generative video costs **$7.50–90 per pass**, or $20–225 with retakes, and is not viable at SaaS prices. Visitor conversation cost per minute: chat about **$0.001–0.03**, voice about **$0.02–0.30** (typically about $0.05–0.10), live avatar about **$0.25–0.37**. Chat-only tiers have about 75–85% gross margin. Voice tiers have 50–75% depending on the voice stack and caps. Live-avatar tiers fall to about 35–45% unless minutes are hard-capped or sold as metered add-ons.

### Cited Findings
- Input prices for the math come from Section 1. Main ones:
  - Claude Sonnet 5.5 $2/$10 and Haiku 5.5 $0.10/$0.50 — [Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing)
  - ElevenLabs TTS $0.05–0.10 per 1K chars — [unifically](https://unifically.com/blogs/elevenlabs)
  - HeyGen about $3/min (Avatar IV/V) and $1/min (Avatar III) — [realtimeavatar.ai](https://realtimeavatar.ai/blog/heygen-api-pricing-explained); [diyai.io](https://diyai.io/ai-tools/video-generation/heygen-pricing/)
  - Shotstack $0.05–0.20/min — [Shotstack](https://shotstack.io/pricing/)
  - Veo 3.1 $0.08–0.60/s — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)
  - Kling 3.0 $0.112/s at 1080p — [costbench](https://costbench.com/software/ai-media-apis/kling-api/)
  - Runway Gen-4 Turbo $0.05/s — [apiframe](https://apiframe.ai/guides/runway-api-guide)
  - ElevenLabs Agents $0.08/min plus LLM — [cloudzero](https://www.cloudzero.com/blog/elevenlabs-pricing/)
  - OpenAI Realtime $0.06–0.11/min (flagship) and $0.02–0.05/min (mini) — [forasoft](https://www.forasoft.com/blog/article/openai-realtime-api-pricing)
  - Tavus CVI overage $0.26–0.37/min — [usagepricing](https://www.usagepricing.com/tools/pricing-calculator/tavus); [rightaichoice](https://rightaichoice.com/tools/tavus)
- Creatomate uses about 14 credits per minute of 720p25 video. At the Essential plan rate ($54 for 2,000 credits) that is about $0.38/min. — [Creatomate docs](https://creatomate.com/docs/account/how-does-the-pricing-work)

### Inferences

**Stated assumptions (my own, not sourced):**
- A 2.5-minute narration is about 375 words, or about 2,250 characters (about 150 words per minute).
- Script/deck generation uses 30K input and 5K output tokens per pass, with 3 passes.
- One chat turn uses 5K uncached input tokens (RAG chunks, history and question), 2K cached system tokens and 250 output tokens.
- One chat "minute" is about 2 turns.
- On the newer Claude tokenizer, real token counts may be about 30% higher than these figures (see the [Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing) tokenizer note). This does not change any conclusion.

**A. Cost to produce one 2.5-minute explainer**

| Path | Component math | Per render | With realistic re-renders |
|---|---|---|---|
| Slides + voiceover (web player or MP4) | LLM: Sonnet 5.5, 3 passes = $0.33 (Haiku 5.5 = $0.02; Opus 5.5 = $0.66). TTS: 2,250 chars × $0.10/1K = $0.225 (ElevenLabs premium); $0.11 on Flash; about $0.09 on Cartesia; about $0.04 on OpenAI mini-TTS. Render: Shotstack 2.5 min × $0.05–0.20 = $0.13–0.50; Creatomate 720p about $0.95; Remotion $0.01/render license plus compute (or free while ≤3 people). | **about $0.30–1.50** | about $0.60–2.00 (3 TTS takes = $0.68 at the premium voice) |
| Avatar presenter, full length | HeyGen Avatar IV/V 2.5 × $3 = $7.50; Digital Twin 2.5 × $4 = $10; Avatar III 2.5 × $1 = $2.50; Synthesia 2.5 × $1–5 = $2.50–12.50; D-ID 2.5 × $1.80 = $4.50; Tavus pre-render 2.5 × $0.80–1.00 = $2.00–2.50. Plus about $0.33 LLM. | **about $2.50–12.50** | about $5–25 (one re-render after the founder's edits) |
| Hybrid: slides with a 20–30 s avatar intro | 0.5 min × $1–4 + slides path | about $1–3 | about $2–5 |
| Fully generative video (150 s) | Veo 3.1 Std 150 × $0.40 = $60; 4K 150 × $0.60 = $90; Veo Fast 1080p 150 × $0.12 = $18; Veo Lite 1080p 150 × $0.08 = $12; Kling 3.0 1080p 150 × $0.112 = $16.80; Runway Gen-4 Turbo 150 × $0.05 = $7.50; Gen-4.5 150 × $0.12 = $18 | **about $7.50–90** | about $19–225 (assuming 2.5× takes for keepers) |

- Generative video is also a poor fit for content. It cannot reliably render accurate charts, metrics or product UI, and output comes as short clips that must be stitched. Use it only for short B-roll (for example 3 × 8 s with Veo Fast, about $3) on top of the slides path.

**B. Cost per visitor conversation minute**

| Mode | Math | $/minute |
|---|---|---|
| Chat, Haiku 5.5 | turn = 5,000×$0.10/M + 2,000×$0.01/M + 250×$0.50/M = $0.00065; × 2 turns | **about $0.0013** |
| Chat, Gemini 3.1 Flash-Lite | $0.00167 per turn × 2 | about $0.0033 |
| Chat, Sonnet 5.5 | 5,000×$2/M + 2,000×$0.10/M + 250×$10/M = $0.0127 per turn × 2 | **about $0.025** |
| Chat, Opus 5.5 / GPT-5.5 | $0.0254 / $0.0335 per turn × 2 | about $0.05 / $0.07 |
| Voice, OpenAI Realtime mini | third-party estimate | **about $0.02–0.05** |
| Voice, OpenAI Realtime flagship | output audio alone about 1,200 tok × $64/M = $0.077; all-in estimate $0.06–0.11 | **about $0.06–0.11** |
| Voice, ElevenLabs Agents | $0.08 platform + about $0.005–0.01 LLM (Haiku/Flash) | **about $0.09** ($0.16 in burst) |
| Voice, Vapi / Retell all-in | per sources | about $0.10–0.31 |
| Voice, self-built LiveKit + components | $0.01 LiveKit + TTS (agent speaks about 50% of the time ≈ 450 chars × $0.05/1K = $0.023) + LLM about $0.005 + STT (price not researched) | about $0.04–0.06, excluding engineering time |
| Live avatar, Tavus CVI | plan-effective $59/175 = $0.34, $397/1,300 = $0.305, $975/4,000 = $0.244; overage $0.26–0.37 | **about $0.25–0.37**, plus LLM |
| Live avatar, HeyGen LiveAvatar | USD credit price not found; vendor claims down to $0.01/min at scale | unknown (gap) |

- Prompt-caching nuance: Anthropic's 5-minute cache write costs 1.25× input. For low-traffic links, most sessions pay a cache write rather than a hit, so caching saves money mainly within a session, not across visitors. Cost is still a fraction of a cent per turn.

**C. Monthly gross-margin model (per customer, with explicit assumptions)**

Assumptions for every tier:
- 20% of visitors open chat and average 3 turns.
- Voice tiers: 10% of visitors start voice and average 3 minutes.
- Live-avatar tier: an extra 5% of visitors use live avatar for 3 minutes.
- Chat runs on Sonnet 5.5 ($0.0127 per turn) unless noted.
- Voice costs $0.09/min (ElevenLabs Agents all-in), with a cheaper Realtime-mini variant at $0.03/min.
- Hosting, storage and bandwidth are a placeholder of $0.50–5 (not researched).
- Payment fees are assumed at 2.9% + $0.30. This is a common card rate, not verified here.

| Plan | What's included | Visitors/mo | COGS breakdown | COGS | Gross margin (before / after payment fees) |
|---|---|---|---|---|---|
| **$19** | Slides+VO video (2 renders), chat only | 200 | chat 40×3×$0.0127 = $1.52; video $2.00; ingest $0.50; host $0.50 | **$4.52** | **76% / 72%** (with Haiku 5.5 chat: COGS $3.08 → 84% / 79%) |
| **$49** | + voice agent | 500 | chat 100×3×$0.0127 = $3.81; voice 50×3 min×$0.09 = $13.50; video $2; ingest $0.50; host $1 | **$20.81** | **58% / 54%** (voice on Realtime-mini: COGS $11.81 → 76% / 72%) |
| **$99** | Avatar video (1.5 renders/mo at $7.50) + voice | 1,000 | chat $7.62; voice 100×3×$0.09 = $27; avatar $11.25; ingest $1; host $2 | **$48.87** | **51% / 47%** |
| **$299** | + live avatar | 2,000 | chat $15.24; voice 200×3×$0.09 = $54; live avatar 100×3×$0.30 = $90; avatar video ×2 $22.50; ingest $2; host $5 | **$188.74** | **37% / 34%** |

Worst case when a customer fully uses hard caps:

| Cap | Worst-case COGS | Margin |
|---|---|---|
| $19 with 1,000 Sonnet chat turns | $15.70 | 17%. The fix is Haiku/Flash-Lite for chat, which makes 1,000 turns cost about $0.65. |
| $49 with 100 voice minutes | $18.85 | 62% |
| $99 with 300 voice minutes | $53.95 | 46% |
| $299 with 500 voice + 200 live-avatar minutes | $159.90 | 47% |

- Conclusion: chat plus slides is a high-margin SaaS product (75–85%). Voice is fine when the minute pool is hard-capped and runs on a cheap S2S model. Live avatar and avatar video only make sense as **metered add-ons or credits**, not "unlimited" features. Platform minimums also need to be covered: Remotion's $100/month company minimum once past 3 people, and Tavus's $59–975 plan floors.

### Gaps
- Real visitor engagement rates (share of link visitors who start chat or voice, and session length) were not found for this category. The 10–20% rates above are assumptions and the biggest driver of COGS.
- Hosting and video-delivery cost per view (Cloudflare Stream, Mux, S3/CloudFront) and STT pricing were not researched.
- Stripe fee level was not verified.

---

## 3. Key cost risk: a viral LinkedIn post driving thousands of voice minutes on a $29 plan, and how comparable products cap usage

### Takeaway
Without caps, one viral link can wipe out months of revenue. 5,000 visitors × 8% voice × 4 minutes is 1,600 minutes, costing about **$96–256 for voice** or **$480 for live avatar**, against $29 of revenue. 20,000 visitors costs **$384–1,024 for voice** or **$1,920 for live avatar**. Comparable products all meter usage: included minute or credit pools with paid overage (ElevenLabs, Tavus, Chatbase, HeyGen, Synthesia), concurrency ceilings (Vapi 10, Retell 20, Tavus 1/3/10), burst surcharges (ElevenLabs $0.16/min), and creator-set per-user message and minute caps (Delphi).

### Cited Findings
- ElevenLabs Agents uses included minutes per plan (15 to 12,375). Overage costs $0.08/min, and "burst" minutes above the concurrency limit cost $0.16/min. Text messages are metered at $0.003. — [cloudzero](https://www.cloudzero.com/blog/elevenlabs-pricing/); [pxlpeak](https://pxlpeak.com/blog/ai-tools/elevenlabs-pricing-guide)
- Tavus plans pair included CVI minutes with concurrency limits: 1 stream on Free, 3 on Starter, 10 on Growth. Overage is pay-as-you-go and "has no cap". — [rightaichoice](https://rightaichoice.com/tools/tavus); [usagepricing](https://www.usagepricing.com/tools/pricing-calculator/tavus)
- Vapi includes 10 concurrent calls and Retell's pay-as-you-go plan includes 20. — [cloudtalk](https://www.cloudtalk.io/blog/how-much-does-voice-ai-cost/); [ainora](https://ainora.lt/blog/ai-voice-agent-cost-per-minute-2026)
- Chatbase sells message credits: Free $0 for 50 credits, Hobby $40 for 700, Standard $150 for 4,000, Pro $500 for 15,000. Each AI response uses 1–6 credits depending on the model. Auto-recharge costs $40 per 1,000 credits, and removing the "Powered by Chatbase" branding costs $99/month. — [resolve247](https://resolve247.ai/blog/chatbase-pricing/); [seldonframe](https://www.seldonframe.com/chatbase-pricing)
- Delphi (AI clone platform) lists Free, Builder ($79–99/month, adds voice calling and analytics), Scaler ($299–399/month) and a custom tier. One creator's 2025 setup capped free users at 20 messages and 5 voice minutes per month, and paid users at 200 messages and 40 voice minutes (anecdotal). Delphi reportedly takes 20% of subscription revenue when creators charge for access. — [coldiq](https://coldiq.com/tools/delphi-ai); [Greg Faxon](https://www.gregfaxon.com/blog/ai-clone); [creatoreconomytools](https://creatoreconomytools.com/tool/delphi)
- HeyGen's $29/month web Creator plan includes 600 credits. Avatar IV/V uses about 20 credits per minute, so that is about 30 minutes. — [eesel HeyGen](https://www.eesel.ai/blog/heygen-pricing)
- Synthesia's Starter plan is reported at $22/month with a 10-minute video cap. — [fluxnote](https://fluxnote.io/guides/synthesia-pricing-2026)

### Inferences

**Viral-spike math.** Assumes 8% of visitors start voice and average 4 minutes, which is my assumption.

| Visitors | Voice minutes | ElevenLabs $0.09 | ElevenLabs burst $0.16 | OpenAI Realtime $0.06–0.11 | Live avatar $0.30 | Chat only (15% × 4 Sonnet turns) |
|---|---|---|---|---|---|---|
| 5,000 | 1,600 | $144 | $256 | $96–176 | $480 | $38 |
| 20,000 | 6,400 | $576 | $1,024 | $384–704 | $1,920 | $152 |

- Concurrency is a second failure mode. A viral spike may bring 50+ simultaneous voice sessions. That exceeds the 10–20 concurrent limits on Vapi and Retell and the 3–10 on Tavus, so calls fail or burst pricing applies.

**Recommended guardrails:**
1. Give each workspace a hard monthly pool of voice and avatar minutes, with auto-fallback to chat when the pool is exhausted. Chat stays cheap even when viral (about $38 per 5,000 visitors on Sonnet, about $2 on Haiku).
2. Cap each visitor session (for example 3–5 minutes of voice) and each link per day.
3. Require a lightweight email or LinkedIn gate before voice or live avatar starts. This doubles as lead capture, which founders value.
4. Rate-limit by IP and device, add bot protection, and cap concurrency per workspace with a queue or "leave a voice note" fallback.
5. Sell prepaid top-up packs priced at least 3× unit cost (for example 100 voice minutes for $15–25).
6. Send the founder "your link is going viral" alerts with one-click top-up. This is an upsell moment, not just a cost event.
7. Default new links to chat plus narrated deck, with voice opt-in.

### Gaps
- I found no published data on how often founder or company share links actually go viral, or on typical voice-session length for this use case.
- I could not verify ElevenLabs' per-plan concurrency limits or included-minute counts for each mid-tier plan.

---

## 4. Quality / trust / legal risks: hallucination on a founder's behalf, securities rules (506(b) vs 506(c)), misleading statements, voice-clone consent, EU AI Act Article 50, GDPR

### Takeaway
The biggest non-technical risk is the agent making **material misstatements about traction, terms or the offering to investors**. Companies are held liable for their chatbots' statements (Moffatt v. Air Canada). A **publicly shareable fundraising link is likely general solicitation**, which pushes founders into Rule 506(c): every purchaser must be accredited, with verification. The product needs a "fundraising mode" with guardrails. EU AI Act Article 50 chatbot-disclosure and deepfake-labelling duties have applied since 2 Aug 2026. Voice and likeness cloning of a real founder needs documented consent. Federal law here (NO FAKES Act) is pending, not enacted.

### Cited Findings

**Hallucination liability**
- In Moffatt v. Air Canada (2024 BCCRT 149), the tribunal held Air Canada liable for negligent misrepresentation by its website chatbot. It rejected the argument that the chatbot was "a separate legal entity", and held the company responsible for all information on its website, "whether it came from a static page or a chatbot". Damages were CAD 650.88. This is a small-claims tribunal decision and does not bind other courts. — [ABA Business Law Today](https://www.americanbar.org/groups/business_law/resources/business-law-today/2024-february/bc-tribunal-confirms-companies-remain-liable-information-provided-ai-chatbot/); [McCarthy Tétrault](https://www.mccarthy.ca/en/insights/blogs/techlex/moffatt-v-air-canada-misrepresentation-ai-chatbot)

**FTC**
- On 1 Jul 2026 the FTC proposed (not finalised) a policy statement applying FTC Act Section 5 to AI products that "steer" outputs against consumers' reasonable expectations. Comments closed 31 Jul 2026. — [Reed Smith](https://www.reedsmith.com/our-insights/blogs/viewpoints/102n7u7/ftc-proposes-policy-prohibiting-deceptive-steering-of-ai-products-and-services/); [Stanford CodeX](https://law.stanford.edu/2026/07/08/when-or-how-principles-can-become-law-the-ftcs-proposed-deceptive-steering-policy-scoped-against-the-ai-life-cycle-core-principles/)
- One analysis reads the FTC as treating hallucinations "in and of themselves" as outside Section 5, while misrepresenting how reliable an AI is can still be deceptive. A chatbot that makes consumers believe they are talking to a human, where that belief affects their decisions, fits the standard deception analysis. — [Consumer Finance Monitor](https://www.consumerfinancemonitor.com/2026/07/14/ftc-takes-aim-at-ai-accuracy/)
- The FTC settled with DoNotPay ("world's first robot lawyer") for $193,000 over untested AI capability claims. "Operation AI Comply" has continued under the new administration. — [Benesch](https://www.beneschlaw.com/insight/one-year-in-ftcs-operation-ai-comply-continues-under-new-administration-signaling-enduring-enforcement-focus/); [aipolicydesk](https://www.aipolicydesk.com/blog/ftc-ai-enforcement-actions-2026)

**Securities (US Reg D)**
- Rule 506(b) generally prohibits general solicitation. Rule 506(c) permits it, but every purchaser must be accredited and the issuer must take "reasonable steps" to verify that. — [Paul Weiss](https://www.paulweiss.com/insights/client-memos/sec-staff-no-action-letter-on-exempt-offerings-with-general-solicitation-under-rule-506-c); [securitieslawyer101 (Aug 2026)](https://www.securitieslawyer101.com/2026/08/14/rule-506b-vs-506c/)
- On 12 Mar 2025, SEC Corporation Finance staff issued a no-action letter. Under 506(c), high minimum investment amounts plus written investor representations (that they are accredited and did not finance the purchase through a third party) can count as reasonable verification. Reported thresholds are $200,000 for natural persons and $1,000,000 for entities. This is staff guidance, not a Commission rule. — [Arnold & Porter](https://www.arnoldporter.com/en/perspectives/advisories/2025/03/secs-corp-fin-issues-no-action-letter-response); [Nixon Peabody](https://www.nixonpeabody.com/insights/alerts/2025/04/02/sec-guidance-on-accredited-investor-verification-in-general-solicitation-securities-offerings); [Foley](https://www.foley.com/insights/publications/2025/03/no-action-letter-regulation-d-rule-506c/)
- One securities lawyer warns that "a website page describing investment terms can destroy your [506(b)] exemption". If marketing might count as general solicitation, file under 506(c). — [securitieslawyer101](https://www.securitieslawyer101.com/2026/08/14/rule-506b-vs-506c/)
- Far more capital is raised under 506(b) than 506(c), reflecting the verification burden. — [Paul Weiss](https://www.paulweiss.com/insights/client-memos/sec-staff-no-action-letter-on-exempt-offerings-with-general-solicitation-under-rule-506-c)

**EU AI Act Article 50**
- The Article 50 transparency duties (chatbot disclosure, deepfake labelling, emotion-recognition notice) have been enforceable since 2 Aug 2026. The Digital Omnibus did **not** delay them. — [Elevate Consult](https://elevateconsult.com/insights/eu-ai-act-article-50-icp-impact/); [hellogrowth](https://hellogrowth.ai/en/blog/eu-ai-act-2026-omnibus-labelling-ai-content); [Legalithm](https://www.legalithm.com/en/blog/eu-ai-act-what-applies-2-august-2026)
- Generative AI systems already on the market before 2 Aug 2026 have until **2 Dec 2026** to implement the Article 50(2) machine-readable marking. New systems must comply when placed on the market. The European AI Board's 17 Sep 2026 meeting granted no further relief. — [CSA research note](https://labs.cloudsecurityalliance.org/research/csa-research-note-eu-ai-act-article50-watermarking-deadline/); [Techjack Solutions](https://techjacksolutions.com/ai-brief/eu-ai-act-article-50-august-2-annex-iii-december-2027/)
- What the Omnibus did delay: Annex III high-risk obligations to 2 Dec 2027 and Annex I obligations to 2 Aug 2028. Sources conflict on whether the Omnibus regulation (reported as Regulation (EU) 2026/1744) has been published in the Official Journal. — [Legalithm](https://www.legalithm.com/en/blog/eu-ai-act-what-applies-2-august-2026); [Gibson Dunn](https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/)
- Article 50 penalties are reported at up to €15M or 3% of global turnover (secondary source). — [theaienterprise](https://www.theaienterprise.io/p/eu-ai-act-omnibus-reprieve-strategy)

**Voice and likeness cloning**
- The federal NO FAKES Act of 2026 (S.4591 / H.R.8915) was introduced on 20 May 2026. The Senate Judiciary Committee advanced it by voice vote on 18 Jun 2026. As of 30 Sep 2026 the House companion had not been taken up, so **it is not law**. Key terms:
  - A federal right to authorise digital replicas of voice and likeness.
  - Licences for a living person's replica must be written, signed, and last no more than 10 years.
  - A DMCA-style notice-and-takedown process.
  - Preemption that preserves state laws in place as of 2 Jan 2025, including Tennessee's ELVIS Act.
  — [Congress.gov S.4591](https://www.congress.gov/bill/119th-congress/senate-bill/4591); [Holland & Knight](https://www.hklaw.com/en/insights/publications/2026/06/senate-judiciary-committee-advances-legislation-to-protect-name); [ByteBack Law](https://www.bytebacklaw.com/2026/08/a-federal-shift-in-ai-and-the-right-of-publicity-no-fakes-act-advances-in-congress/); [Manatt](https://www.manatt.com/insights/newsletters/client-alert/congress-reintroduces-the-no-fakes-act-what-s-new-in-the-2026-bill)

### Inferences

**Product requirements that follow from the above:**
1. **Founder-approved fact sheet as the only source of truth.** The agent answers only from approved facts and cites the slide or document it used.
2. **Hard "do-not-answer" topics in fundraising mode:** valuation, terms, round size, investor names, projections and legal or tax matters. The agent routes these to "ask the founder" with a contact capture.
3. **Numeric-claim verification.** Any number in an answer must match a number in the fact sheet, or the answer is blocked. This is a deterministic check after the LLM generates the answer.
4. **Full transcript logging** with founder review, plus a visible "AI assistant, may be inaccurate; not an offer to sell securities" disclosure.
5. **Fundraising-mode toggle.** In 506(b) mode the link is private: access-controlled, per-investor links, no indexing, offering terms hidden. In 506(c) mode the founder attests to verification. The product should not give legal advice, but defaults should be conservative. Moffatt plus the FTC deception framing mean the founder (and possibly the platform) owns what the bot says.

**Misleading statements to investors:** beyond Reg D, an agent misstating traction to investors is a potential securities-antifraud problem. I did not source the antifraud rule specifically (see Gaps), but this is the most severe trust risk and argues for guardrails 1–3 above.

**EU visitors:** the product is the *provider* of a system that interacts with people, so it needs a clear "you're talking to an AI" notice and machine-readable marking of synthetic audio and video (C2PA/watermark) for new deployments now. A founder deploying an avatar or voice clone of themselves is plausibly a *deployer* of a deepfake who must disclose it. Build the disclosure banner and the marking in from day one.

**Voice and avatar cloning:** require the cloned person's own recorded consent (a verification phrase, as HeyGen and ElevenLabs-style flows do), keep consent records, block cloning third parties, and have a takedown process. This anticipates NO FAKES-style notice-and-takedown even though it is not law yet.

### Gaps
- **GDPR:** no sources were retrieved because the search budget ran out. To verify with counsel:
  - Founder as controller vs platform as processor, which needs an Art. 28 DPA.
  - Lawful basis for storing visitor chat and voice transcripts and for lead capture.
  - Voice recordings as personal data, and whether voiceprints would be biometric data.
  - Retention limits, cross-border transfers to US model vendors, and cookie/analytics consent.
- I found no source on Rule 10b-5 / antifraud exposure for AI-generated investor communications, or on whether a password-protected link avoids "general solicitation". Securities counsel is needed.
- I found no current details on the ELVIS Act, California AB 2602/AB 1836, the New York digital-replica laws, or US state chatbot-disclosure laws (for example California's bot-disclosure statute).
- Whether the EU Omnibus regulation is published in the Official Journal is unconfirmed (sources conflict).

---

## 5. Build effort for a competent solo developer (MVP vs polished v1) and the hardest parts

### Takeaway
An MVP built on APIs (ingestion, narrated web deck, RAG chat, one voice-agent integration, share link, basic analytics, billing) takes about **4–8 weeks** for a competent solo developer. A polished v1 adds branded templates, MP4 export, avatar option, guardrails and approval workflow, analytics, metering and compliance, and takes about **3–5 months**. These are inferences; no source benchmarks this exact build. The hardest parts:
- Making output look non-generic.
- Answer faithfulness on numbers.
- Voice latency: real-world turn latency is about 0.8–1.8 s even on the best stacks.
- Robust ingestion of messy sites and PDFs.
- Usage metering and abuse control.
- Constant vendor and model churn.

### Cited Findings
- Voice latency in practice: a caller-side benchmark of real phone calls measured the best median time-to-first-audio-byte at 1,296 ms (Telnyx), with ElevenLabs at 1,768 ms p95. — [openbenchmarks voice-agent latency](https://openbenchmarks.com/voice-agent-latency)
- Speech-to-speech models, per Artificial Analysis measurements from Apr 2026: end-to-end time to first token ranged from 0.78 s (xAI Grok Voice Agent) to 2.98 s (Gemini 3.1 Flash Live), with OpenAI gpt-realtime-1.5 at 0.82 s. — [softcery](https://softcery.com/lab/ai-voice-agents-real-time-vs-turn-based-tts-stt-architecture); [gradium TTFA blog](https://gradium.ai/blog/time-to-first-audio)
- TTS-only time to first audio, per the Coval leaderboard as of 8 Sep 2026: ElevenLabs Flash v2.5 at 185 ms median, Gradium at 214 ms, Cartesia Sonic 3.6 at 440 ms. Vendor-reported numbers conflict; Inworld cites Cartesia at 40 ms. — [gradium TTS benchmark](https://gradium.ai/content/tts-latency-benchmark-2026); [Inworld](https://inworld.ai/resources/best-voice-ai-tts-apis-for-real-time-voice-agents-2026-benchmarks)
- Vendor churn is high:
  - Sora API removed 24 Sep 2026 on six months' notice, with no successor. — [Make.com](https://help.make.com/openai-sora-and-video-modules-deprecation-by-september-24-2026)
  - GPT-5 mini/nano and gpt-4o-mini-tts marked deprecated. — [OpenAI GPT-5 nano](https://developers.openai.com/api/docs/models/gpt-5-nano); [gpt-4o-mini-tts](https://developers.openai.com/api/docs/models/gpt-4o-mini-tts)
  - Gemini 2.5 native-audio models reportedly limited to past users. — [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing)
  - Gemini 3.8 TTS and Flash prices double on 1 Jan 2027. — [Vertex pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing)
- Remotion is free for organisations of up to 3 people, so a solo founder can build MP4 export on it at no licence cost initially. — [Remotion pricing](https://www.remotion.dev/docs/license/pricing)
- Hosted voice platforms impose concurrency limits (Vapi 10, Retell 20), which shape the architecture for spiky traffic. — [ainora](https://ainora.lt/blog/ai-voice-agent-cost-per-minute-2026)

### Inferences

**MVP, about 4–8 weeks of focused work:**

| Week | Work |
|---|---|
| 1 | Ingestion: URL fetch with a headless browser plus a readability pass, PDF/DOCX parse, and an LLM extraction into a structured fact sheet the founder edits. |
| 2–3 | Deck generation (JSON to a themed HTML/React slide player) and narration script plus per-slide TTS with audio sync. |
| 3–4 | RAG chat with citations and refusal rules, the share-link page, and view analytics (slide dwell, questions asked, email capture). |
| 5 | Voice via a hosted agent (ElevenLabs Agents widget or OpenAI Realtime over WebRTC), plus minute caps. |
| 6 | Stripe billing, metering, auth, rate limits. |

Allow 1–2 weeks of buffer.

**Polished v1, about 3–5 months:**
- Brand-kit theming and several high-quality templates.
- Slide-level editing and regeneration.
- MP4 export (Remotion Lambda or Shotstack).
- Optional avatar intro (HeyGen/Tavus API) with consent capture.
- Founder approval workflow and numeric-claim checker.
- Fundraising mode, private per-investor links and access logs.
- Analytics dashboard with intent signals and CRM exports (HubSpot, Attio, Notion).
- EU AI Act disclosures and C2PA marking, a GDPR DPA, retention controls.
- Provider-abstraction layer and evaluation harness for answer accuracy.

**Hardest parts, ranked:**
1. **Non-generic visual quality.** LLM-generated decks look the same. Quality depends on design templates, a good layout engine, and real assets (logos, product screenshots, charts from the company's data). This is design work more than API work.
2. **Answer faithfulness on investor-critical facts.** RAG works for most answers, but numbers, terms and comparisons need deterministic validation. Building an eval set for this is non-trivial.
3. **Voice UX.** Even top stacks are at about 0.8–1.3 s turn latency and up to about 1.8 s p95 on phone. A browser WebRTC session avoids the telephony legs, but barge-in, turn-taking and accents still take tuning. Hosted platforms (ElevenLabs Agents, Realtime) remove most of that work, at roughly $0.05–0.10/min more than self-hosting.
4. **Ingestion robustness.** JS-heavy sites, gated content, decks saved as image-only PDFs, and conflicting sources.
5. **Metering, abuse and cost control** (Section 3).
6. **Churn management.** Expect to swap at least one media vendor per year.

### Gaps
- No published case studies of solo developers building this exact product, so the timelines are judgement-based.
- Browser-WebRTC voice latency benchmarks (as opposed to phone-call benchmarks) were not found.
- No quantitative data on how viewers rate AI-generated explainer quality versus human-made decks.

---

## 6. Defensibility: what could become a moat when the components are commodity APIs

### Takeaway
The generation layer is not defensible. Every component is rentable, and avatar, voice and video vendors themselves sell competing end-user products (HeyGen, Synthesia, Tavus, Delphi, ElevenLabs widgets). Plausible moats come from what accumulates *around* the link:
- A "Made with X" distribution loop on every shared link.
- Viewer-engagement and intent analytics (which investor watched what, and what they asked).
- A cross-company corpus of investor and buyer questions that improves answers and benchmarks.
- A trust and compliance layer specific to fundraising.
- Workflow integrations (CRM, data room) that create switching costs.

### Cited Findings
- Branding badges are a recognised monetisation and distribution lever in adjacent tools: Chatbase charges $99/month to remove "Powered by Chatbase". — [resolve247](https://resolve247.ai/blog/chatbase-pricing/)
- Adjacent "AI clone" platforms already bundle voice calling plus analytics in paid tiers (Delphi Builder) and monetise creators via revenue share (reported 20%). — [coldiq](https://coldiq.com/tools/delphi-ai); [creatoreconomytools](https://creatoreconomytools.com/tool/delphi)
- Media vendors sell end-user plans directly: HeyGen Creator $29/month, Synthesia Starter about $22/month, Tavus Starter or Builder $59/month. These vendors can move downstream into the same use case. — [eesel HeyGen](https://www.eesel.ai/blog/heygen-pricing); [fluxnote](https://fluxnote.io/guides/synthesia-pricing-2026); [rightaichoice](https://rightaichoice.com/tools/tavus)
- HeyGen's LiveAvatar is advertised at "pennies a minute" with "unlimited concurrency", which suggests live-avatar cost will commoditise quickly. — [LiveAvatar](https://www.liveavatar.com/)

### Inferences

**Ranked moat candidates:**
1. **Distribution loop.** Every link is seen by investors, customers and candidates. A tasteful "Make your own" footer plus a viewer-side "ask follow-up / get notified" hook can drive low-cost acquisition, in the same way document-tracking and scheduling links grew. This is the most realistic early moat for a solo founder.
2. **Engagement and intent analytics.** This includes per-viewer slide dwell, replays, the exact questions asked, voice sentiment, and "hot lead" scoring sent to the founder. The data is proprietary to the platform and becomes more valuable with CRM sync.
3. **Question corpus.** Thousands of real investor and buyer questions across companies can power suggested FAQs ("investors usually ask about CAC at seed; you haven't answered it"), pre-emptive answer coverage, and benchmarks. This compounds only at scale.
4. **Trust layer.** This means verified claims (numbers linked to source documents), fundraising-mode compliance defaults, consent-verified voice clones, and EU AI Act-compliant disclosure and marking. It is hard for generic avatar or chatbot vendors to prioritise, and it matters to the target users (founders raising money).
5. **Workflow lock-in.** This means the founder-curated fact sheet and approved-answer bank, team seats, data-room or CRM integrations, and a link history with analytics. Switching costs are moderate.

**Weak moats:** model quality, voices and avatar realism are all rented and improving for everyone.

**Strategic risk:** HeyGen, Tavus, Delphi, ElevenLabs, or a deck tool adding "share with AI Q&A" could ship this as a feature. Differentiation must come from the investor/fundraising-specific workflow and analytics, not from generation.

### Gaps
- No data found on the retention or virality of comparable share-link products in 2026, or on whether investors actually engage with AI agents on pitch links rather than ignoring them. This is the key demand-side uncertainty. See the companion competitor notes in this folder (competitors_deck_video_demo.md) for market evidence.
- Whether DocSend-style tools or deck tools (Pitch, Gamma, Tome successors) have added voice or chat Q&A agents as of Oct 2026 was not checked in this research stream.
