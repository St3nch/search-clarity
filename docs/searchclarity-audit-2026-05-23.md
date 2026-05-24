# SearchClarity Docs Audit

**Auditor scope:** r00 through r05 in `C:\dev\searchclarity\docs` (8 files including two `.bak` backups of r00 and r05; backups are stale and ignored).
**Total reviewed:** ~310KB of strategy/spec across 6 active docs.
**Date:** May 23, 2026.

---

## 1. Executive Verdict

**Is the doc set coherent enough?** Yes, surprisingly so. r00 → r01 → r02 → r03 → r04 → r05 follow a clean arc: brand frame → market validation → first sample spec → strategic gig review → full report system → data/intelligence layer. The pieces talk to each other. That's rarer than it should be.

**Is SearchClarity launchable from these docs?** **No, not yet.** Strategically launchable. Operationally not. You have specs for what the reports should *look like* but not for how the business actually *runs*. Specifically missing: the actual filled-in sample report (r02 specs it, r03 says "build it first," r04 says "build it first," and r05 references it — but nobody has built it), a real tracker/spreadsheet, the actual Fiverr gig copy, the intake form, the .co site, and any QA workflow that exists outside of r04 Section 17's checklist on paper.

**Biggest strength:** The brand discipline is real and consistently enforced across all six docs. Every doc independently arrives at: no ranking promises, no AI slop, evidence-backed, 5-line recommendation block, human-reviewed, transparent methodology. That kind of cross-doc consistency means the positioning is internalized, not just declared. r04 Section 3 (Universal Framework) is genuinely strong — it's the kind of system spec that scales without losing brand voice.

**Biggest weakness:** **Massive strategy-to-execution gap.** Six docs of planning, zero artifacts. r02 has been speccing the Maplewood Candle Co. sample report for ~28KB. r03 then re-specs the same anchor gig from a strategy angle (~47KB). r04 re-specs it again as a production template (~95KB). r05 references it as a foundation (~91KB). Nobody has actually written the 16-page sample PDF. **You have planned the same sample report four times and built it zero times.** Until the sample exists, the whole launch is theoretical.

**Highest-priority fix:** Stop planning. Write the Maplewood Candle Co. sample report this week. One artifact. r02 + r04 Section 4 are sufficient blueprints — you don't need more docs to start. Until that PDF exists, every other operational gap is academic.

---

## 2. Current Document Map

| Doc | Apparent Purpose | Strong / Weak / Needs Edit | Notes |
|---|---|---|---|
| r00-searchclarity-overview.md (11.85KB) | Brand overview, separation from Neon Ronin, first offer, pricing, website strategy | **Strong** | Tight, well-organized, sets up everything downstream. The Neon Ronin separation is clean. Pricing table is consistent with r01. Only nit: the "Current SearchClarity Docs" section at the bottom is going to rot — it already commits to `r06-minimal-searchclarity-tracker-system.md` as the next doc, which is one of the things this audit is supposed to evaluate. |
| r00-searchclarity-overview.md.bak (10.16KB) | Stale older draft | **Retire** | Was the prior version of r00 before being expanded. Earlier draft talks about "VEDA-style observatory" — that language is gone from current r00. Delete or move to an `archive/` subfolder. |
| r01-searchclarity-launch-strategy.md (36.75KB) | Fiverr/Upwork market research, competitor analysis, pricing bands, 90-day roadmap | **Strong but dated by category** | Excellent research — competitor names, prices, real Trustpilot/Marmalead/Waggoner citations, Fiverr/Upwork media slot rules. Caveats section is honest about the freshness. **Risk:** competitor prices and gig examples were observed in May 2026 and are referenced by name (Designer_rafy, Heycarla, Etsygeeks, Alan R., Scaledon, etc.). These need a "verify before launch" note even more prominent than the current caveat. |
| r02-sample-report-spec.md (28.60KB) | Detailed spec for the Maplewood Candle Co. sample report | **Strong as spec, but it's been spec'd long enough** | This doc has been doing its job for a while. The fictional shop concept, page-by-page blueprint, data labeling rules, and bad-vs-good recommendation examples are excellent. **Problem:** it's a spec for an artifact that doesn't exist yet. Every additional refinement to r02 is procrastination on the actual sample report. |
| r03-first-5-gig-report-strategy-review.md (47.07KB) | Strategic review of which of the planned 10 gigs to launch first, in what order, with what packaging | **Strong but partially superseded by r04** | Verdict that Pinterest is too early and Competitor Report should fold into Audit Premium is correct and important. **Overlap concern:** r03 Section 13 (Data Source and Tool Review) and r04 Section 14 (Package-Level Deliverable Differences) and r04 Section 15 (Universal Buyer Intake Rules) all cover the same ground from different angles. After r04 was written, large chunks of r03 became reference material rather than active strategy. |
| r04-comprehensive-seo-report-system.md (95.56KB) | Working template/spec for all 10 reports — sections, tables, recommendation formats, intake, delivery messages, QC | **Strong, but oversized for current stage** | This is the most operationally useful doc in the folder. The Universal Framework (Section 3), QC Checklist (Section 17), and Delivery Messages (Section 16) are immediately usable. **Problem:** it fully specs Reports 1–10 when only Reports 1–3 will launch in the first 60 days. r04 Section 18 itself says "Build full templates for these now: Report 1, 2, 3." Reports 4–10 are aspirational and could be split into a separate doc to reduce the chance the team treats them as immediate requirements. |
| r05-client-report-history-and-market-learning-observatory.md (91.07KB) | Data retention, customer history model, generalized observations, Market Opportunity Signal system, 12-factor scoring, future DB schema implications | **Strong content, badly placed for current stage** | The data philosophy, retention rules, consent rules, and minimization rules are excellent and should stay in SearchClarity. **The 12-factor opportunity scoring system, the future DB model in Section 15, and most of Section 14 (intelligence metrics) belong to Neon Ronin, not SearchClarity.** r05 currently does the job of two docs — a SearchClarity tracker/privacy spec AND a Neon Ronin observatory spec. It needs a split. See Section 3 of this audit. |
| r05-...md.bak (91.07KB) | Backup, identical size | **Retire** | Same size as live file. Either identical or near-identical. Delete or archive. |

---

## 3. SearchClarity vs Neon Ronin Separation Audit

The separation is **declared** crisply in r00 but **violated** quietly throughout r05.

| Issue | Where It Appears | Why It Matters | Recommendation |
|---|---|---|---|
| 12-factor opportunity scoring lives in SearchClarity | r05 Section 7.2 | Scoring opportunities across niches is strategy-engine work. SearchClarity should *capture* the signal; Neon Ronin should *score* and *queue* it. Putting the scoring model in SearchClarity forces analysts doing $75 audits to also do strategic intelligence math. | Move the scoring rubric, classification bands (0-25 / 26-35 / etc.), and the example signals table to a new Neon Ronin doc: `neon-ronin/research-docs/r10-searchclarity-strategy-layer-and-market-observatory.md`. Leave a one-paragraph stub in r05 that says "signals are captured here; scoring happens in Neon Ronin per r10." |
| Future database schema for the intelligence layer | r05 Section 15 ("Future Database Implications") | The DB architecture for `MarketSignal`, `GeneralizedObservation`, `PatternTag`, and `Niche` is observatory territory. SearchClarity's DB needs are just Customer / Shop / Order / Report / Listing / Recommendation. | Split Section 15: keep customer-history entities in r05; move generalized/signal/pattern/niche entities to Neon Ronin r10. |
| Observability / intelligence metrics | r05 Section 14 | Half of these metrics (most-common-issue, niches frequently audited, recommendations most-often-reused, pattern frequencies, signal funnel) are observatory metrics. The other half (turnaround time, revision reasons, add-on conversion, repeat-order rate) are operational SearchClarity metrics. | Split. Operational metrics stay; intelligence metrics go to Neon Ronin r10. |
| "Cross-project learning" mentioned but undefined | r00 (Neon Ronin owns) | r00 says Neon Ronin owns "cross-project learning" but there's no doc on the Neon Ronin side that describes what that means. SearchClarity may eventually feed signals to Neon Ronin that benefit other projects, but the handoff is unspec'd. | When you write Neon Ronin r10, include a section on "what SearchClarity hands off and in what shape." |
| Agent-assistance is referenced but not separated | r00 says "Agents may assist with research, drafting, data extraction, and workflow later" | Agent workflows are explicitly Neon Ronin. But r04's analyst workflow doesn't mention agents at all. The handoff point — "when does an analyst use a Neon Ronin agent" — is unwritten. | Punt this for now. Real analysts shipping real reports come first. Agent integration is a Neon Ronin r1x topic, not a SearchClarity blocker. |
| "DataForSEO is only one provider" — but who owns the abstraction? | r00 mentions DataForSEO; r04 lists eRank, EverBee, etc. as analyst tools | If multiple data providers exist and the analyst rotates between them, that's SearchClarity's workflow concern. If there's a unified observatory data layer that abstracts providers, that's Neon Ronin. | Decide: are SearchClarity analysts going to use eRank directly (in which case forget the abstraction layer for now) or hit a Neon Ronin observatory that pools sources? Document the answer. |
| Customer-facing reports vs internal patterns — clean | r05 throughout | This separation is actually done well — generalized observations have no client identifiers, the policy in Section 7.4 is firm. | No change. This is the model for how to do separation right. |

**Net verdict:** SearchClarity correctly owns the customer-facing business. Neon Ronin correctly owns the engine. But r05 has annexed about 30% of what should be Neon Ronin territory. Fix by splitting r05, not by rewriting it.

---

## 4. Missing Documents

| Missing Doc | Why It Is Needed | Priority | Suggested Filename |
|---|---|---|---|
| **The actual filled-in sample report PDF** | Spec'd four times, built zero times. Cannot launch without it. | **P0 — blocking** | `samples/maplewood-candle-co-listing-visibility-audit.pdf` (and source `.md` or `.docx`) |
| Minimal tracker/spreadsheet spec | r00 promises this as r06. r05 Section 18 lists 8 sheets that should exist from day one. Currently they don't exist. | **P0 — blocking** | `r06-minimal-tracker-system.md` plus actual `trackers/searchclarity-master.xlsx` |
| Fiverr gig copy (all 3 launch gigs) | r01 sketches the structure, r03 has FAQ items, but nobody has written the actual final copy ready to paste into Fiverr. | **P0 — blocking** | `r07-fiverr-gig-copy.md` with sub-sections for Audit, Rewrite, Keyword Pack |
| Customer intake form spec (actual form, not abstract questions) | r04 Section 15 lists fields. There is no actual form built. Fiverr's "Buyer Requirements" field has a character limit and a specific format. | **P0 — blocking** | `r08-buyer-intake-forms.md` with one form per gig, copy-paste-ready |
| First order workflow / manual fulfillment SOP | Once an order arrives, what happens? Who does what, in what order, with what handoffs? r04 has delivery messages but no end-to-end SOP. | **P0 — blocking** | `r09-order-fulfillment-sop.md` |
| Report file production workflow (Markdown → PDF, branding, style) | r04 says "Markdown-to-PDF pipeline with a SearchClarity stylesheet, or Word document with a defined stylesheet." Neither is built. The actual production pipeline (template files, fonts, colors, footer/header, file naming) is unwritten. | **P0 — blocking** | `r10-report-production-pipeline.md` + actual template files in `templates/` |
| SearchClarity.co site architecture spec | r00 lists the URL structure but there is no actual site plan: which pages launch when, what content each page has, what the sample report page does, what the email gate captures, etc. | **P1 — needed for launch** | `r11-website-architecture.md` |
| Brand voice / writing style guide | r02 has bad-vs-good examples. r04 has a "no AI slop" QC line. There is no single style doc analysts can reference. | **P1 — needed for launch** | `r12-brand-voice-style-guide.md` |
| Launch checklist (the actual launch day list) | What must be true before the Audit gig goes live? No doc gathers this. r01's "Stage 1 — Pre-launch" is the closest but it's strategic, not operational. | **P1 — needed for launch** | `r13-launch-checklist.md` |
| Revision/refund/dispute boundary doc | r04 Section 16.7 has the revision template. There is no internal SOP for when/how to grant refunds, escalate disputes, handle a buyer who claims results didn't come, etc. | **P1 — needed for launch** | `r14-revision-refund-policy.md` |
| Fiverr gallery + video production spec | r02 outlines gallery images and video script. Neither has been produced. Fiverr image specs (dimensions, file size, no-text-overlay rules where they apply) need to be documented before production. | **P1 — needed for launch** | `r15-fiverr-asset-production.md` |
| SEO/GEO/LLM entity plan for SearchClarity.co | r00 lists 7 entities (SearchClarity, Etsy Listing Visibility Audit, etc.). There is no doc on how each entity gets its canonical page, what schema each carries, what internal linking pattern joins them, what FAQ content lives where, or how the site builds entity recognition for AI search. **This is conspicuously absent given you sell AI search readiness.** | **P1 — needed for launch+positioning** | `r16-searchclarity-entity-and-geo-plan.md` |
| Market signal logging SOP | r05 Section 7 describes the system. Nobody has documented "after delivering a report, here are the exact 5 minutes you spend logging signals." Without a tight SOP, the intelligence layer never gets populated. | **P1 — operational** | `r17-market-signal-logging-sop.md` |
| Neon Ronin r10 — strategy layer / observatory | r00 already names this file. It doesn't exist. The 12-factor scoring and aggregation logic from r05 belongs here. | **P1 — for Neon Ronin** | `neon-ronin/research-docs/r10-searchclarity-strategy-layer-and-market-observatory.md` |
| Pricing & checkout policy doc | r00, r01, and r03 all reference prices. They don't fully agree (r00 lists $75/$145/$245; r03 suggests Standard launches at $125 then $145; r01 has launch pricing $65/$125/$215). One doc should be the source of truth. | **P2 — clarification** | `r18-pricing-policy.md` |
| Communication templates beyond delivery | r04 has 10 buyer-facing message templates. Missing: order acknowledgment for direct (non-Fiverr) buyers; reactivation message for inactive buyers; follow-up review request variants; "we can't take this order" decline message; "this is outside our scope" redirect. | **P2 — operational** | Add to `r19-customer-comms-templates.md` or fold into r04 Section 16 |
| Competitor IP / takedown response policy | r03 and r04 both flag trademark risk. There's no doc on what to do if SearchClarity is *accused* of IP infringement, has a takedown request, or a buyer reports we recommended a trademark-risky keyword. | **P2 — defensive** | `r20-ip-incident-response.md` |
| Data retention automation spec | r05 Section 10 lists retention durations. Section 17 lists "Storing sensitive data unnecessarily" as a risk. Nobody has written how retention is actually enforced — spreadsheet review cadence? Auto-deletion script? Manual quarterly purge? | **P3 — formalize later** | Fold into the eventual database doc; for spreadsheet stage, add to r06 tracker doc |
| Analyst onboarding/training plan | When the first non-founder analyst joins, what do they read? r02 + r04 are the right canon, but no "read these in this order, then shadow one delivery, then own one delivery" exists. | **P3 — only when hiring** | `r21-analyst-onboarding.md` |
| Neon Ronin handoff requirements (from SearchClarity's POV) | What does SearchClarity need from Neon Ronin to integrate later? r05 names some entities. There's no requirements doc written from the SearchClarity side. | **P3 — when Neon Ronin is being built** | `r22-neon-ronin-integration-requirements.md` |

**Note on r06 specifically:** r00 promises r06 as "minimal-searchclarity-tracker-system." That's correct as a *concept* but should be expanded. The minimal tracker should be one doc; the production pipeline, intake forms, gig copy, fulfillment SOP, and sample report production are all also "next." Don't insist on r06 being only the tracker. The next four or five docs all need to exist before launch.

---

## 5. Launch Readiness Gaps

| Gap | Severity | Why It Blocks Launch | Fix |
|---|---|---|---|
| No actual sample report exists | **Critical** | Cannot post a Fiverr gig without the sample. Cannot launch SearchClarity.co. Cannot upload to Upwork later. Every doc says this is the #1 launch asset. | Write Maplewood Candle Co. audit this week. 16 pages. r02 + r04 Section 4 are the blueprint. Total work: 6-12 focused hours if discipline holds. |
| No Fiverr account configured | **Critical** | Need profile copy, "About," profile photo, account email separate from personal, payout setup. r01 mentions LinkedIn Services as a brand presence asset — also unbuilt. | Set up the Fiverr seller account and verify identity *before* the sample is finished — Fiverr verification can take days. |
| No actual gig copy written | **Critical** | r01 Section 10 sketches structure. Final copy with character counts, packaging math, FAQ wording, and intake question wording does not exist. | Write final gig copy as a deliverable artifact, not as a doc section. |
| No intake form built | **Critical** | r04 lists fields. Fiverr buyer-requirements field needs the actual questions formatted to Fiverr's UI constraints. | Write the literal intake text per gig. |
| No file production pipeline | **High** | Without it, the first paid order will be produced ad hoc with whatever tool happens to be open. That guarantees the report won't match the sample's quality. | Pick: Markdown + Pandoc + custom CSS, or Word with style sheet, or Docx-with-Python. Commit. Build template. |
| SearchClarity.co does not exist yet (presumed) | **High** | r00 specifies the URL structure. The site is part of the trust strategy. Without it, the only proof asset is the Fiverr gallery. | Single-page launch site at minimum — home, method, sample download (gated by email), about, contact. Five pages. |
| No payment/refund path defined for non-Fiverr buyers | **Medium** | If a buyer wants to pay direct, what happens? Stripe? PayPal? Invoice? Refund mechanics? | Don't accept direct orders until Fiverr is proven. State this on the site if needed: "Currently accepting orders via Fiverr only." |
| No legal entity / business setup mentioned | **Medium-High** | LLC? Sole proprietor? Business bank account? Tax handling? Not a doc gap, but a real-world gap. Mentioning it here because no doc addresses it. | Out of scope for docs, but solve before order #5 or your tax situation gets messy. |
| No business email / Google Workspace | **Medium** | hello@searchclarity.co or similar. Replies from gmail.com hurt credibility. | Set up before launch. |
| Founder identity / About page is undefined | **Medium** | r01 references "Rachel: I run my own Etsy shop with 4,000 sales" as a competitor's credibility move. SearchClarity's founder credibility is unmentioned. | Decide: founder name + face + bio on website? Or pseudonymous brand? r01 implicitly suggests the former (LinkedIn Services page). |
| No QC second-reviewer plan when team is one person | **Medium** | r04 Section 17 says "Reviewed by a second pair of eyes if the report is over 12 pages" and the sample is 16. If you are the only analyst at launch, this check fails for every report. | Decide explicitly: solo-analyst QC is self-review with cooling-off period (24 hours minimum between drafting and review), then formal sign-off. Document it. |
| No order-volume capacity plan | **Low** | If 3 orders come in at once on day one, what's the turnaround commitment? r03 says 3 business days basic. Can one person produce a 16-page audit in 3 days while also doing intake review, communications, and Fiverr account management? | Throttle: set Fiverr to max 2 active orders for the first 2 weeks. Raise as you prove you can hit 3-day delivery. |

---

## 6. Report Production Gaps

| Gap | Why It Matters | Recommendation |
|---|---|---|
| No actual report template file exists | r04 specifies sections, tables, and recommendation blocks. There is no `.md`/`.docx`/`.idml` template the analyst opens to start writing. | Build one template file per launch report (Audit, Rewrite, Keyword Pack). These are working files, not specs. |
| Markdown-to-PDF pipeline undefined | r04 mentions Pandoc-style pipeline OR Word stylesheet. No decision made. | Pick Pandoc + custom CSS for Markdown source → PDF. Reasons: version control friendly, plays well with future Neon Ronin agent assistance, doesn't lock you into Word's quirks. Build once. |
| No SearchClarity branding assets | No logo file specified. No color palette. No font choices. r00 mentions "wordmark" but the wordmark doesn't exist. | Commission or DIY: wordmark, 1-2 brand colors, accessible body/heading font. Lock it before sample production. |
| Spreadsheet deliverable format undefined | r04 says Reports 2 and 3 deliver .xlsx and .csv. No template. | Build the spreadsheet template alongside the report template. Keep formatting boring — sortable, filterable, no merged cells, no fancy conditional formatting that breaks on Excel/Sheets/Numbers cross-platform. |
| File naming convention defined but not enforced | r04 QC Section 17 has `SearchClarity_[ReportName]_[ShopName]_[YYYY-MM-DD].pdf`. No naming script. | For solo stage: a templated text file or shortcut that builds the filename. Trivial but easy to forget. |
| QC checklist exists as table, not as workflow | r04 Section 17 is a brilliant 25-row checklist. Nobody applies a 25-row checklist to every report unless it's frictionless. | Convert Section 17 into a 1-page printable checkbox file the analyst physically marks for each report. Or a Notion/spreadsheet form. |
| No second-reviewer plan documented (see Section 5 above) | "Reviewed by a second pair of eyes" assumes a team. Solo launch reality is different. | Solo: 24-hour cooling-off between drafting and review. Read aloud. Different time of day. Document this as the substitute for two-reviewer. |
| Revision boundary template exists; revision *workflow* doesn't | r04 Section 16.7 is the message. What if the buyer escalates? Who decides if a revision is in-scope? | Solo-stage: founder decides. When team grows: written escalation path. For now, just write down "founder always decides revision scope." |
| No example of what a "bad" finished report looks like for analyst training | The bad-vs-good in r02 is at the recommendation level. There's no "this whole report is what we don't ship" full example. | Optional but useful when you onboard a second analyst. Not blocking. |
| No customer-facing delivery checklist | r04 has internal QC. There's no "before hitting send: did we attach the right files, the right shop name, the right email, the right delivery message template?" | Trivial pre-send checklist. Five items. Pin to wall. |

---

## 7. Customer Journey Gaps

| Stage | Weakness | Improvement |
|---|---|---|
| Buyer sees gig/site | Fiverr gig copy doesn't exist. SearchClarity.co doesn't exist. Buyer has nothing to see. | Write gig copy. Build site. (See Section 5 gaps.) |
| → trusts offer | Sample report doesn't exist. The single most important trust asset is missing. Founder bio/identity undefined. No reviews (expected for launch). | Build sample. Decide founder positioning. Set Fiverr "launch pricing" framing to reduce first-buyer risk per r01. |
| → orders | Pricing inconsistencies across r00/r01/r03 will confuse the buyer-facing copy. | Resolve pricing in one doc. Use it. |
| → submits intake | Intake form doesn't exist. r04 specifies fields but not the exact wording in Fiverr's UI. Multiple gigs need separate intake question sets. | Write Fiverr-formatted intake questions for each gig. Stay under 8 questions per r03/r04. |
| → receives report | Report template doesn't exist. Production pipeline doesn't exist. Delivery message template exists (r04 Section 16). | Build template + pipeline. Lift delivery message verbatim. |
| → understands actions | r04's recommendation 5-line block + priority action plan is the answer here. This part is genuinely strong on paper. | No doc gap. Make sure the template enforces it. |
| → asks follow-up | r04 Section 16.7 covers revisions. Doesn't cover: "I implemented your changes, what now?" or "Etsy banned my listing for an unrelated reason, can you help?" | Add to delivery message: explicit "what to do in the next 30 days" + "when to come back to us." |
| → buys next service | Add-on attach is the single biggest revenue lever for SearchClarity. r05 Section 6 lists 9 returning-customer scenarios. None of them have a triggered next-step message. | Build a "review request + next-service recommendation" message sent 14-21 days after delivery. r04 Section 16.8 (review request) is the skeleton; add the next-service nudge. |
| → becomes returning customer | History tracking doesn't exist yet (r05 Section 18 lists the spreadsheets — they're not built). Without history, the returning-customer promise in r05 Section 6 collapses. | Build the 8 spreadsheets from r05 Section 18 *before* order #1. |
| → leaves a review | r04 Section 16.8 has the review request. Timing isn't specified. | Send 7-10 days after delivery — long enough they've tried something, short enough the experience is still fresh. |

---

## 8. SEO/GEO/LLM Visibility Gaps

This section deserves extra weight because SearchClarity sells AI search readiness. Your own visibility is the credibility test.

| Gap | Why It Matters | Suggested Research/Doc |
|---|---|---|
| Entity plan for SearchClarity.co | r00 lists 7 entities. There is no doc defining canonical pages, schema per page, internal linking, or entity reinforcement strategy. | New doc: `r16-searchclarity-entity-and-geo-plan.md`. Cover: which entities get pages, what's the URL slug, what schema each page carries, how they link to each other. |
| Topical authority cluster strategy | r00 says use subfolders for `/resources/etsy-seo/`, `/resources/marketplace-seo/`, etc. No content plan exists for these resource hubs. | Decide which 1-2 topical clusters are launch priority (probably Etsy SEO methodology + AI search readiness, given the differentiator). Plan 5-10 pillar pages per cluster. |
| Service pages — content brief unwritten | r00 lists 10 services. Each one needs a SearchClarity.co page with consistent structure (problem, what's included, methodology, FAQ, sample, schema). No brief exists. | Write a single service-page template (one MD with placeholder sections). Apply to each service as it launches. Don't pre-build 10 pages — build as services launch. |
| Sample reports as standalone web pages | r04 Section 18 says "gated by an email opt-in." The page itself is unspec'd: what's above the gate? What's the preview structure? How is the schema marked? | Spec the public sample-report page in the website architecture doc. The first 3 pages of the PDF should display inline as web content (better for SEO than a PDF link), with the full PDF behind email. |
| Schema markup plan | r04 Report 8 (Schema Readiness Audit) is a *service*. The plan for schema on SearchClarity.co itself is unwritten. Eat your own dog food. | Plan: Organization schema on home; Service schema on each service page; FAQPage schema on FAQ pages; Article schema on resource pages; Person schema for founder; Review schema only if real reviews exist (per r05 Section 11, no fake reviews). |
| Citation-worthy methodology pages | This is the differentiator for AI search visibility. Methodology pages that AI systems can cite when explaining "how should I audit my Etsy listing" are pure entity-building. | Plan 3-5 methodology pages: "How SearchClarity audits an Etsy listing", "Our keyword research methodology", "How we score AI search readiness", "Why we don't promise rankings", "What makes a good Etsy title". These do double duty: SEO content + analyst reference. |
| FAQ page strategy | Connected to schema. Buyers ask consistent questions; FAQ pages capture them; FAQPage schema makes them eligible for rich results AND helps LLM citation. | Build FAQ pages per service. Pull questions from r03 FAQ topics. |
| Founder/author trust signals | r00 lists author/founder trust as a "core public entity" but provides no plan. AI search systems weight author entity strongly. | Decide founder identity. Build founder Person schema. Write a substantive About page. LinkedIn matters here per r01. |
| Comparison pages | "SearchClarity vs cheap Fiverr SEO gigs" is a high-intent search. r01's competitor research has the raw material. | Plan one comparison page after launch (don't lead with it — looks defensive). |
| Content cluster mapping | r00 mentions /resources/ subfolders but doesn't say how they connect to service pages internally. | When building the entity/GEO plan doc, include the internal linking pattern: every resource page links to its parent service, every service links to its sample, every methodology page links to the relevant service. |
| LLM citation prep — sourceable facts about SearchClarity | r04 Report 9 says brands need sourceable content for AI citation. SearchClarity itself needs the same. | Build at least one page with the brand's clear, factual story: founded date, founder, what we do, what we don't do, methodology principles, public sample. Concise. Citable by an LLM. |
| Third-party mention strategy | r04 Report 9 says brands need third-party citations for entity strength. SearchClarity has none yet. | Plan: guest posts on Etsy seller blogs; thoughtful Reddit answers; podcast guesting on Etsy seller podcasts. Slow burn. Not launch-blocking but should be in the 90-day plan. |
| No `/method/` or `/process/` page planned in detail | r00 lists `/method/` as a URL. Content unspec'd. | This is the most important page after the sample. It's where buyers and AI systems go to understand what SearchClarity does. Spec it explicitly. |
| robots.txt, sitemap, hreflang | None of these are mentioned. Fundamentals. | Trivial; document once. |
| AI bot crawling policy | Should SearchClarity.co allow GPTBot, ClaudeBot, PerplexityBot? Given the service sells AI visibility, blocking them would be hypocritical. | Allow. State explicitly in robots.txt. Document the decision. |

---

## 9. Fiverr / Marketplace Positioning Gaps

| Gap | Recommendation |
|---|---|
| No final gig titles | r01 sketches them ("I will audit your Etsy listings with a professional PDF report and reasoning"). Lock final wording with character count check (Fiverr title limit). |
| No thumbnails/gallery images produced | r02 specs 3 images. r04 cross-references. None produced. Produce as part of sample report build. |
| No PDF sample uploaded | Needs the 3-page public preview built first. Spec is in r02 Section 9. |
| No gig video produced | r02 has 45-60 second script. r01 says faces build trust. Founder needs to be on camera (unless brand is staying pseudonymous, in which case decide alternative). |
| Pricing not fully reconciled | r00 says $75/$145/$245. r01 launch pricing $65/$125/$215. r03 says start Standard at $125 then $145. Pick one, document in one doc. |
| Package FAQ not finalized | r03 has FAQ topics. Write final FAQ answers under 200 words each. |
| Package tier descriptions inconsistent across docs | r00 says Premium = "20 listings plus deeper recommendations." r03 says Premium = "8 listings, 5 business days, includes 20-min Loom." r04 Section 14 says Premium Audit = "25 listings audited, 30-day follow-up." Reconcile. |
| Buyer requirements not in Fiverr-format | Fiverr buyer requirements have a specific UI. Translate r04 Section 15.2's intake questions into Fiverr's required-question format with character limits. |
| Proof asset strategy unfinished | r02 specs the sample. r01 references it. Nobody built it. (Recurring theme.) |
| Differentiation copy untested | r01's "no fake ranking promises" wording is good but unrehearsed. Decide where in the gig copy this lives — gig description? FAQ? "About my service" section? |
| Avoiding weak Fiverr vibes | r03 Section 14 covers this implicitly. Gallery design choice and sample report design choice are the actual execution. | Be ruthlessly anti-Canva-template. Boring professional > flashy template. |
| Cheap-competitor differentiation | r01 has the market research. Final positioning copy (the 2-3 sentence "why us, not them" line) is unwritten. Write it. |
| Upwork Project Catalog plan | r01 says Day 45-60. The 2-PDF, 60-second-video, 20-image media spec exists. The actual Upwork listing copy doesn't. Defer until Fiverr Level 1 reached. |
| LinkedIn Services profile | r01 mentions as brand presence asset. Unwritten. Defer past launch. |

---

## 10. Data / Tracker / Database Gaps

| Gap | Risk | Recommendation |
|---|---|---|
| The 8 spreadsheets from r05 Section 18 don't exist | If you start taking orders without these, you lose the returning-customer benefit on order #2 and lose the intelligence layer entirely. r05 is the single highest-value system in the docs and it has zero implementation. | **Build before order #1.** Spreadsheets are 2-3 hours. Not optional. |
| File storage plan unwritten | Where do report PDFs live? Google Drive? Dropbox? Local + backup? r05 says "filename, file hash, storage path" as fields. Doesn't say *where*. | Pick one. Cloud (Drive/Dropbox) with versioning preferred for accident recovery. Document the path convention. |
| Customer ID convention undefined | What's the customer ID format? CUS-001? UUID? Email-as-ID? r05 just says "customer record." | Use a short ID — CUS-001 — separate from email so you can change email later. |
| Order ID convention undefined | Same issue. | ORD-001. Per-order, increments. |
| Report ID convention undefined | Same issue. | RPT-001. Or RPT-{order_id}-{type}. |
| Shop ID convention undefined | A shop may have multiple orders. Need stable shop reference. | SHO-001. Linked to customer ID. |
| Listing snapshot retention policy | r05 says 3 years for snapshots. Spreadsheet rows don't expire automatically. | Document: quarterly review, delete rows older than 3 years. Or add a `delete_after` column. |
| Keyword observations dedup strategy | If the same keyword is researched for 5 different clients, do you create 5 rows or 1 row with 5 links? | 5 rows initially (simpler). Aggregate later when you build the real DB. |
| Outcome tracking process | r05 Section 13 has the labels. Nobody tracks them today. Outcomes require *asking* the customer or *checking* the listing yourself. | Add to delivery: "we'll check in at day 21 to see how things are going." Make outcome capture a 5-minute task at day 21. |
| Market signal record format | r05 Section 7.3 has 15 fields. That's a wide spreadsheet. | Build the spreadsheet with all 15 columns. Don't shortcut to "I'll fill in only the important ones later" — the fields are designed to make scoring fast. |
| Consent records — no template | r05 Section 11 requires written consent for any public use. No consent template exists. | Write a simple consent message template: "I, [name], consent to SearchClarity using [scope] in [locations] until [revoke conditions]." Email reply with explicit "yes" counts. |
| What NOT to store — analyst training material | r05 Section 9 is the list. Nobody has been trained on it because there's only one analyst. | When second analyst joins, this is mandatory reading. For now: founder must internalize. |
| Audit logs (per r05 Section 17 risks) | Spreadsheets don't audit themselves. | Stage 1: don't worry about it. Stage 2 (DB build): mandatory. Note in r05. |
| Backup plan | Spreadsheets in Google Drive vs Dropbox vs local. What if account is locked? | Three-copy rule: working copy, cloud backup, monthly local export. |
| Encryption at rest | r05 Section 17 lists this as mitigation. Spreadsheets in Google Drive are encrypted at rest by Google. Local Excel files aren't. | If you keep any local copies, encrypt the drive. macOS FileVault, Windows BitLocker. |
| Data privacy policy for SearchClarity.co | r05 has retention rules internally. The site needs a public privacy policy. | Write one. Reference standard policies (GDPR/CCPA at minimum). Honest about what's collected and retained. |

---

## 11. Market Signal / Opportunity System Audit

The 12-factor scoring system in r05 Section 7 is the most ambitious and most over-engineered piece of the entire doc set.

| Issue | Recommendation |
|---|---|
| **12 factors is too many for analyst use during a paid order.** Each factor takes thought. Analysts under turnaround pressure will either skip the scoring entirely or score everything as a default 3 (which makes the total meaningless). | Cut to 5 factors at launch. Suggested keepers: Buyer intent clarity, Competition weakness, Keyword depth, Marketplace fit, Strategic value. The other 7 (product variation, seasonality, content expansion, operational difficulty, risk/IP, demand signal, differentiation room) can be captured as free-text notes if relevant. 5 factors × 5 points = 25 max. Reclassify bands accordingly (0-10 ignore, 11-15 watch, 16-20 research later, 21-25 research next). |
| **Scoring belongs in Neon Ronin, not SearchClarity.** SearchClarity analysts should capture the signal (description, niche, evidence, why-it-stood-out). Scoring is strategy work that benefits from comparing across many signals, which is observatory-level. | Move scoring to Neon Ronin r10. SearchClarity captures raw signals. Neon Ronin scores them during the monthly review. |
| **No factors are obviously missing**, but "Differentiation room" overlaps with "Competition weakness" and could be folded. | When the cut to 5 happens, "Differentiation room" goes. It's a derivative of competition weakness + buyer intent clarity. |
| **The Section 7.6 example signals are too neat** — all have scores in the 42-52 band. Realistic distribution would have some 28s and some 58s. | Add a "what a low-score signal looks like" example so analysts calibrate. |
| **No clear definition of what triggers signal logging.** Right now Section 7.1 lists 10 examples but the threshold for "worth logging" is fuzzy. New analysts will either log everything or nothing. | Add: "If you spent more than 2 minutes thinking about the niche/keyword/gap during this report, log it. Otherwise don't." Forces a soft floor. |
| **Minimum viable signal record for order #1:** signal_id, date_observed, source_report_type, niche, signal_description, why_it_stood_out, opportunity_score (or 5-factor partial), recommended_next_step, status. Nine fields, not fifteen. | At launch, 9 fields in a spreadsheet. Expand toward Section 7.3's full 15 once Neon Ronin r10 is built. |
| **Review cadence is sensible.** Monthly 30-minute review is right for this volume. | Keep. Move execution to Neon Ronin's responsibility once that side exists. |
| **The "we don't compete with clients" line in Section 7.4 is the most important sentence in r05.** It's the entire ethical foundation of the intelligence layer. | Bold it. Repeat it in three places: r05, the analyst onboarding doc when it's written, and the public site's About page. |

---

## 12. Service Roadmap Audit

The 10 services are sensible. r03 already audited the launch order with the right verdict. Here's the cross-check.

| Service | Launch Timing | Dependency | Needed Before Launch |
|---|---|---|---|
| 1. Etsy Listing Visibility Audit | **Day 1 (launch)** | None | Sample report, gig copy, intake, template, production pipeline, gallery images, video |
| 2. Etsy Title and Tag Rewrite | Day 14-21 (after 3 Audit reviews) | r03 confirms — depends on Audit credibility | Rewrite template, gig copy, intake |
| 3. Etsy Keyword Research Pack | Day 21-30 (as Audit add-on initially per r03) | Best when bundled with Audit | Spreadsheet template, cluster framework (r04 6.6 is good), PDF interpretation guide template |
| 4. Etsy Competitor Visibility Observations | Day 60+ (fold into Audit Premium first per r03) | Audit must have 10+ reviews | Audit Premium add-on language; standalone deferred. Ethical-use boilerplate (r04 Section 7.6) is ready. |
| 5. Etsy Shop Visibility Report | Day 60+ | Better after Audit volume creates returning-customer demand | Shop-level template; not blocking. |
| 6. Pinterest SEO Plan | Day 75+ per r03 | After 15+ combined reviews on Etsy gigs | Pinterest methodology untested. Plan a pilot with one volunteer before launching. |
| 7. Shopify Product Page SEO Audit | Day 60-90 | Different buyer; wait for 3+ buyer requests | Shopify methodology, Search Console access workflow |
| 8. Schema / Structured Data Readiness Audit | Day 90+ | Often pairs with Shopify audit (#7) | Schema validation tooling, output template |
| 9. AI Search / LLM Visibility Readiness Audit | Day 90-120 | Strong differentiator but small buyer market today | Prompt-test methodology, entity assessment framework |
| 10. Seller Visibility Strategy Report | Day 120+ | Synthesis report — useless without prior reports per r04 18 | Wait for 5+ customers with 3+ reports each. Could be 6 months out. |

**Roadmap-level concerns:**

- **The roadmap collapses if the Audit doesn't sell.** Everything depends on the Audit. Pre-launch, build only the Audit. Don't pre-build templates for services 2-10. r04 already specs them; that's enough until validated demand exists.
- **The AI Search Readiness Audit is the brand-defining differentiator.** Don't bury it past Day 90. r01 originally said Day 30 launch as differentiator gig. r03 demurred. **Compromise: launch a stripped-down version (1-2 page "AI Visibility Snapshot" upsell) at Day 30 instead of the full audit.** Differentiates the brand early; validates demand cheaply.
- **Services 4 and 5 (Competitor Observations, Shop Visibility) could both happily live as Audit Premium tiers without ever becoming standalone gigs.** Don't force standalone if the bundle works.

---

## 13. Research Topics Needed Next

| Research Topic | Why It Matters | Priority | Which Project |
|---|---|---|---|
| Sample report production research — markdown-to-PDF pipeline with branded CSS, or Pandoc + reference template, or Word stylesheet | Cannot ship anything without it. | **P0** | SearchClarity |
| First sample report production (the actual artifact) | Not "research" per se but the single most blocking deliverable. | **P0** | SearchClarity |
| Fiverr 2026 current rules — off-platform contact, AI disclosure, repeat-buyer messaging, gig sample policies | r01 cites May 2026 rules. Verify before launch. | **P0** | SearchClarity |
| Etsy API ToS verification — what can SearchClarity legally observe and store from Etsy listings | r03 mentions "Etsy API Terms now explicitly prohibit using API data for machine learning or analytics without written authorization." Verify scope. | **P1** | SearchClarity |
| eRank/Marmalead/EverBee 2026 pricing and tool feature comparison | r03 has 2025 pricing. Verify before locking analyst tool stack and gig copy. | **P1** | SearchClarity |
| Customer intake best practices for Fiverr buyer requirements | Fiverr's UI has character limits and required-question format. Test against the 8-question target. | **P1** | SearchClarity |
| Report PDF production workflow — choose tooling, build template, test cross-platform rendering | Block on this. | **P1** | SearchClarity |
| SearchClarity.co tech stack decision | Static site? Webflow? Ghost? WordPress? Each has SEO/GEO implications. | **P1** | SearchClarity |
| SearchClarity.co SEO/GEO/LLM architecture (the missing entity plan doc) | See Section 8 above. | **P1** | SearchClarity |
| DataForSEO role and integration scope | r00 mentions but doesn't define. Is it for SearchClarity (analyst tool) or Neon Ronin (data layer)? | **P2** | Both |
| Tracker/spreadsheet template implementation — the actual 8 sheets | r05 Section 18 lists them. Build them. | **P1** | SearchClarity |
| Market signal logging SOP | Without a tight SOP, the intelligence layer never gets populated. | **P1** | Both (signal capture is SearchClarity; signal scoring/use is Neon Ronin) |
| Neon Ronin r10 design — strategy layer + observatory | Receives signals from SearchClarity; runs the 12-factor scoring; manages research queues. | **P1** | Neon Ronin |
| Database schema for SearchClarity customer history (when spreadsheets break) | r05 Section 15 has architectural notes. Real schema work is later. | **P3 (Q3 2026)** | SearchClarity → eventually Neon Ronin |
| Database schema for the intelligence layer | Separate from customer history per r05 Section 17. | **P3** | Neon Ronin |
| Founder identity research — Fiverr seller-level requirements, LinkedIn presence, About page | Affects positioning, gallery video, page bios. | **P2** | SearchClarity |
| Competitor positioning audit — how do mid-market Etsy SEO providers actually position themselves in 2026 | r01 has the snapshot. Position differentiator at launch needs fresh validation. | **P2** | SearchClarity |
| Pricing validation — does $75 / $145 / $245 hold at SearchClarity's positioning or should launch undercut? | r01 says undercut for 14 days. r03 says don't go below $65. Soft pilot would help. | **P2** | SearchClarity |
| Proof/trust asset strategy beyond the sample | Once sample is done: case studies? Methodology pages? Founder content? Where does trust scale next? | **P3** | SearchClarity |
| Etsy 2026 search algorithm changes since June 2024 AI disclosure rule | Affects every Etsy report recommendation. | **P2** | SearchClarity |
| AI search consumer adoption metrics — is the 20% Etsy referral figure (r01) still directionally true in mid-2026? | Affects how aggressively to position AI Search Readiness as a service. | **P2** | SearchClarity |
| Pinterest 2026 algorithm and content patterns | Pinterest gig blocked on this. | **P3** | SearchClarity |
| Shopify Product schema rich-results eligibility 2026 | Schema audit gig blocked on this. | **P3** | SearchClarity |
| LLM citation behavior — which LLMs cite what kinds of pages, what schema, what structures | Strategic input for AI Search Readiness service AND SearchClarity's own GEO strategy. | **P2** | Both |
| Comparison of small-business SEO observatory tools (or whether to build) | Affects Neon Ronin DB build vs buy. | **P3** | Neon Ronin |

---

## 14. Suggested Doc Order From Here

This is opinionated. Followed in order, SearchClarity reaches Fiverr launch ready in 2-3 weeks of focused work.

| Order | Action | File | Reason |
|---|---|---|---|
| 1 | **Build the Maplewood Candle Co. sample report** | `samples/maplewood-candle-co-listing-visibility-audit.md` + exported PDF | Single biggest blocker. Spec exists 4x over. Stop planning. |
| 2 | **Build the report production pipeline** (Markdown → branded PDF) | `templates/audit-template.md` + `templates/searchclarity.css` + Pandoc command | Required to produce step 1 cleanly. Solved once, reused forever. |
| 3 | **Write the tracker doc and build the 8 spreadsheets** | `r06-minimal-tracker-system.md` + `trackers/searchclarity-master.xlsx` | Required for returning-customer continuity and signal capture from order #1. |
| 4 | **Split r05 — move intelligence/scoring/DB-future to Neon Ronin r10** | `r05` (trimmed) + new `neon-ronin/research-docs/r10-...md` | Fixes the boundary violation. Frees r05 to be a tight SearchClarity ops doc. |
| 5 | **Write Fiverr gig copy** (all 3 launch gigs) | `r07-fiverr-gig-copy.md` | Final wording, character counts checked, FAQ answers locked. |
| 6 | **Write customer intake forms in Fiverr-format** | `r08-buyer-intake-forms.md` | Map r04 Section 15.2 fields to Fiverr's required-questions UI. |
| 7 | **Write the order fulfillment SOP** | `r09-order-fulfillment-sop.md` | End-to-end: order arrives → intake review → research → drafting → QC → delivery → follow-up. |
| 8 | **Build SearchClarity.co minimum viable site** (5 pages: Home, Method, Sample, About, Contact) | Plus `r11-website-architecture.md` if needed | Trust hub. Sample-report hosting. Email capture. |
| 9 | **Write the entity / GEO plan for the site** | `r16-searchclarity-entity-and-geo-plan.md` | Walks the AI-visibility talk. Sets schema/internal-linking/cluster strategy. |
| 10 | **Produce Fiverr gallery images and gig video** | Asset files only | Lift from the sample report. |
| 11 | **Write launch checklist** | `r13-launch-checklist.md` | Verify everything before publishing the gig. |
| 12 | **Launch Audit gig on Fiverr** | — | First real test. Throttle to max 2 active orders for first 2 weeks. |
| 13 | After 3 orders + reviews: **write Rewrite gig + launch** | Builds on r04 Section 5 spec | Per r03 sequencing. |
| 14 | After 5 orders: **write the brand voice / style guide** | `r12-brand-voice-style-guide.md` | Now informed by real reports, not theoretical. |
| 15 | Day 30: **Launch AI Search Readiness "Snapshot" upsell** (the stripped-down version) | Spec under r04 Section 12 | Brand differentiation early, lower than full service. |

**Things to retire / archive immediately:** the two `.bak` files. Move to `archive/` or delete.

---

## 15. Top 10 Improvements

1. **Build the damn sample report this week.** It has been spec'd in r02, referenced as foundational in r03, named as the public mock in r04, and built upon in r05. It is the unblocker for ~70% of the launch checklist. Block calendar time. Six to twelve hours. Done.

2. **Split r05.** Move the 12-factor scoring (Section 7.2), future DB schema (Section 15), and intelligence metrics (Section 14) to Neon Ronin r10. SearchClarity r05 becomes a tight 30-40KB ops doc covering customer history, retention, privacy, and signal *capture* (not scoring). This single move fixes the boundary violation and makes both projects cleaner.

3. **Cut the 12-factor scoring to 5 factors.** Buyer intent clarity, Competition weakness, Keyword depth, Marketplace fit, Strategic value. 5 × 5 = 25 max. Realistic for analyst use under turnaround pressure. Add factors back later if data proves they matter.

4. **Reconcile pricing in exactly one doc.** Three docs name different prices and tier scopes. Pick one. The other docs reference it. Pricing drift in your own documentation predicts pricing drift in customer-facing copy.

5. **Build the 8-spreadsheet tracker before order #1.** Not after, not "I'll do it once I have customers." r05's entire returning-customer promise and intelligence layer depend on these spreadsheets existing on day zero. 2-3 hours of work. Don't skip.

6. **Write SearchClarity.co's own AI-visibility plan.** You are selling AI Search Readiness as Service #9. If a buyer Googles your brand or asks ChatGPT about SearchClarity, what comes back? Right now: nothing. That's a credibility hole the size of the service category. Write `r16-searchclarity-entity-and-geo-plan.md`. Eat your own dog food publicly.

7. **Launch the AI Search Readiness "Snapshot" at Day 30, not Day 90+.** A stripped-down 2-page version is enough to differentiate the brand early. The full service can be Day 90. Differentiation that comes 90 days late doesn't differentiate.

8. **Convert r04 Section 17 QC checklist from prose table to a usable form.** A 25-row table in a 95KB doc gets read once and forgotten. A 1-page printable checkbox sheet (or Notion form) gets used every order. Same content, different delivery.

9. **Define a real solo-analyst QC substitute.** r04 says "second pair of eyes for reports over 12 pages." Your sample is 16 pages. If you're solo, the second-eyes check fails every time. Write it explicitly: 24-hour cool-off between draft and review, read-aloud check, formal QC pass. Don't pretend the team-review check is met when it isn't.

10. **Decide founder identity before building Fiverr profile or website.** Named founder with LinkedIn + face + bio is one positioning. Pseudonymous brand-only is another. Both are valid; mixing them is not. r01 implies the former. Lock the decision before designing any trust assets. This affects the gig video, the About page, the LinkedIn presence, the brand voice, and whether the methodology pages have a byline.

---

## 16. Final Recommendation

**Should you keep working SearchClarity first before more Neon Ronin design?** Yes. Absolutely. SearchClarity is one good week of execution away from being a real business. Neon Ronin is one good month away from being a real engine. Cash flow comes from SearchClarity. Cash flow buys the time to build Neon Ronin. Reverse the order and you fund the engine with nothing.

**What should be done today?** Three things, in this order:
1. Block calendar time for the Maplewood Candle Co. sample report build. Not "soon" — a specific 6-12 hour window in the next 5 days.
2. Delete or archive the two `.bak` files. They're noise.
3. Pick the report production pipeline (Markdown + Pandoc + CSS is my recommendation) and write the `searchclarity.css` stylesheet. 2 hours.

**What should wait?**
- All Reports 4-10 templates. r04 has spec'd them. Don't build them until each has either demand or a reason to launch.
- Neon Ronin r10. Write it after SearchClarity has 3 paid orders so you know what handoff actually looks like.
- The full DB build. Spreadsheets are correct for 0-50 customers.
- The brand voice / style guide. Better written after you've shipped 5 reports than before.
- LinkedIn Services, Upwork Project Catalog, Contra. All post-launch.

**Biggest trap to avoid:** **Continuing to plan instead of shipping.** This doc set has 310KB of strategy and zero artifacts. The pattern is "spec the same thing in more detail" instead of "build the thing." Every additional doc revision is a procrastination signal. The trap is intellectually satisfying (planning feels productive) and operationally fatal (no money comes in).

A secondary trap: **trying to launch all 10 services or even all 3 launch services simultaneously.** r03 is right — one excellent gig with a real sample beats three mediocre gigs scrambling for the same buyer. Ship the Audit. Get 3 reviews. Then the Rewrite. Then the Keyword Pack. The sequencing in r03 Section 10 is correct.

**What would I do if this were my project?**

I would clear my calendar for one week. I would write the Maplewood Candle Co. sample report front to back, end to end, on day 1-2. I would not refine, I would not optimize — I would produce a real artifact at the quality level r02 and r04 demand. On day 3, I would build the Markdown→PDF pipeline with the brand CSS and re-export the report cleanly. On day 4, I would build the 8 spreadsheets from r05 Section 18 — empty, just the columns. On day 5, I would write the Fiverr gig copy and the intake form. On day 6, I would set up the Fiverr seller account and put the gig in draft. On day 7, I would publish the gig — at launch pricing — and wait.

Then I would keep refining the docs only when real orders revealed real gaps. Not before.

The docs are good. The execution gap is the entire problem. Close it.

---

*End of audit.*
