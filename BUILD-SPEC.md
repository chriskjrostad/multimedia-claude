# Multimedia Claude — Build Spec (v1)

> Public, open Claude setup. Same "published Claude configuration" pattern as the
> developer-focused Claude Council, aimed at a totally different audience:
> **non-technical content & social-media managers.** This doc is the build task.
> It is written to be published — keep it free of any private/client-specific info.

## What it is
A shareable **Claude Project** (runs in the Claude desktop/web app — **no terminal, no install, no server**) that turns one piece of long-form media into a week of ready-to-post social content, and **coaches the user click-by-click** through the free tools they already have to finish and schedule it.

Claude is the **director** (picks moments, writes copy, designs the card, gives exact steps). The human is the **hands** (does the clicks in tools they already use). No code execution, no APIs, no hosting, no liability.

## Who it's for
Non-technical people who manage social/content for a small organization and spend hours each week turning long content into posts by hand. Examples (the product is general, not tied to any one):
- A podcaster turning a 60-min episode into clips + quotes
- A small business turning a webinar or keynote into posts
- A creator repurposing a long YouTube video
- A community/nonprofit media volunteer turning a recorded talk into a week of content

They will never open a terminal. The entire experience is conversation in the Claude app.

## v1 MVP — ONE end-to-end loop (scope is deliberately tight)
One source → one highlight clip → one quote card → one scheduled post, each step with a checklist and a verification gate. Prove the loop works before adding breadth.

Flow:
1. **Get the transcript** — coach the user to a transcript (paste text, upload the file to Claude, or use the platform's auto-captions). Don't assume they have one.
2. **Pick the moment** — Claude reads the transcript and proposes the single most shareable 15-30s moment, with exact start/end timestamps and the verbatim quote. Fallback: if nothing clearly shareable, say so and offer the best 2 options instead of forcing one.
3. **Write the copy** — post caption in the org's voice (from personalization), platform-appropriate, with hashtags/CTA as configured.
4. **Make the graphic** — Claude writes the quote text + tells the user to paste it into a **pre-sized Canva template** (link provided). Do NOT have users screenshot raw SVG/HTML (aspect-ratio/border failures). Keep the card optional — real photos often outperform graphics.
5. **Cut the clip** — Claude gives a **numbered, bolded checklist** to cut the clip in **CapCut** (free, non-dev) using the exact timestamps from step 2.
6. **Schedule the post** — Claude gives a numbered checklist to schedule in **Meta Business Suite** (free, native, no developer API) or the relevant platform's native scheduler.

Output style everywhere: **bolded step-by-step checklists, not conversational paragraphs.** Brain heavy, hands light. Minimize app-switching; each handoff is one explicit, verifiable step.

## First-run personalization (the real differentiator — do this well)
A **guided conversation** (not a config file) that captures and remembers:
- Org/brand name, what they do, who their audience is
- Brand colors + the Canva template link
- Voice/tone (warm/plain vs punchy vs formal), things to always/never say
- Channels in use (FB, IG, YouTube, TikTok, etc.) and posting cadence
- Any recurring content types

This must be completable by a non-technical user with zero help. It is the hard part and the thing that makes the setup feel personal. Keep it short, plain-language, one question at a time.

## Guardrails
- **Copyright/music caution** on clips (don't add copyrighted audio to a clip that'll be posted).
- **No-clear-moment fallback** (above).
- **Voice safety** — never invent quotes; only use verbatim transcript text for quote cards.
- Platform-neutral: don't hard-code one network's rules; ask which channels.

## Explicitly DEFERRED to v2 (do NOT build in v1)
- Content calendar / multi-post packs / batch generation
- Deep multi-week personalization beyond the first-run basics
- A true hands-off "installed-for-you" tier (a Claude Code build with real ffmpeg + scheduling automation) — separate, technical, per-user install; not the public chat-Project v1.

## Architecture
- A Claude Project: a system/instruction prompt + a small set of reference files (the workflow, the personalization interview, the tool-coaching scripts, a voice/quality guide).
- No external dependencies, no API keys, no hosting. Everything happens in the chat + the user's own free tool accounts.
- Reference inspiration: the published Claude Council pattern (one-brain agent, surfaced via a clean setup, personalized on first run). **Do NOT reuse its CLI/bash flows** — those assume a terminal and are dead-on-arrival for this audience. This is a from-scratch, chat-only onboarding.

## Distribution
- A standalone public GitHub repo (owner creates it).
- A plain-English README + ONBOARDING one-pager written for non-devs (how to clone the Project and start).
- A LinkedIn post (owner writes it): the angle is "same architecture as the dev edition, totally different audience."

## Build checklist (the actual task)
- [ ] Project system prompt (director persona, output = checklists, guardrails)
- [ ] First-run personalization interview script (one question at a time, non-dev language)
- [ ] Weekly workflow prompt (steps 1-6 above)
- [ ] Tool-coaching scripts: transcript sourcing, CapCut clip, Canva card, Meta Business Suite scheduling (each a numbered checklist)
- [ ] Voice/quality guide (verbatim-only quotes, tone matching, platform-neutral)
- [ ] README + non-dev ONBOARDING one-pager
- [ ] Dogfood on ONE real piece of long-form media end to end before publishing
- [ ] Beta with one real non-technical content manager; log every friction point → v2 backlog

## Process note for whoever builds this
Run the design through office-hours (scope/frame) then COD (pressure-test) when making non-trivial calls — that two-pass loop already caught the major issues in the original design (scope was too big, screenshots fail for non-devs, keep it a separate repo).
