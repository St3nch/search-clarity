# r05 — Client Report History + Market Signal Capture

**Document purpose:** Defines how SearchClarity stores paid customer report history, shop/listing/page records, keywords, recommendations, outcomes, and market opportunity signals created during paid SEO work. This document defines what SearchClarity keeps for customer continuity and what it captures for later Neon Ronin observatory/strategy use.

**Audience:** Internal SearchClarity team (operations, analysts, future engineering).
**Status:** Working plan. Not customer-facing. Pairs with r04 (the report system) and Neon Ronin r10 (the strategy layer). r04 defines what SearchClarity delivers. This document defines what SearchClarity keeps and captures. Neon Ronin r10 defines how generalized signals are scored, prioritized, and turned into research or strategy queues.

---

## 1. Executive Summary

SearchClarity is going to do a lot of paid SEO work across real markets. Every audit, every keyword research pack, every competitor observation teaches us something about how those markets actually work. The niche patterns, the keyword clusters with low competition, the buyer intents that are under-served, the product categories where good listings are rare — all of that is intelligence. If we deliver the report and archive it without capturing the signal, we waste the most valuable thing the work produces.

The core idea is simple:

> While doing paid SEO work, if we see a niche, product category, keyword cluster, or marketplace gap that looks promising — we mark it, score it, and research it later.

That is what this document defines. Client work reveals opportunity. Opportunity gets logged. Logged opportunity gets scored. Strong opportunities get researched independently. Research that confirms the opportunity can become SearchClarity strategy, content, products, or future listings.

**Three purposes of storing report history, in order.** (1) Returning customers get better reports — the analyst opens the history, sees what was recommended, sees what's changed, builds forward instead of starting cold. (2) SearchClarity's methodology improves faster — patterns across many clients sharpen templates, analyst training, and QC faster than any one person's experience would. (3) **SearchClarity spots market opportunities** — paid SEO work is also market research, and we should treat it that way.

**What we store.** Client identity, shop/site identity, orders, report files, intake answers, listing/page snapshots at time of audit, keywords researched, recommendations given with their rationale, action plans, follow-up notes, customer-shared outcomes, recurring issue patterns, and — critically — **market opportunity signals** flagged during research with scores and research status.

**What we don't store.** Payment data, Etsy buyer personal data, platform passwords or API keys, private analytics credentials, customer home addresses, personal phone numbers, unnecessary revenue or profit screenshots, and client assets (photos, designs, copy) beyond what's needed to produce the report.

**How this helps returning customers.** A second-order customer doesn't re-explain their shop. We open their history, see the prior recommendations, see which ones they implemented, and build the next report on top of that. Continuity is a moat against competitors who treat each order as a blank slate.

**How this improves our services.** Recurring patterns across many client reports sharpen our templates, QC checklist, and analyst training. "8 in 10 Etsy gift listings repeat identical tag sets." "Schema audits on Shopify gift shops consistently lack Brand markup." Patterns like these make every future report better.

**How this surfaces market opportunities.** Every time an analyst works through a niche and sees underserved keyword clusters, thin competition in a buyer-intent sub-niche, or a product category where the top listings are weak — that observation gets flagged as a Market Opportunity Signal. It gets scored. The strong ones get researched. The research drives strategy, not the client data that originally surfaced the signal.

**The practical line.** SearchClarity may record niches, product categories, keyword clusters, buyer-intent patterns, marketplace gaps, and opportunity signals discovered during client work. Those signals can improve services, content, strategy, and future products/listings. The hard lines are simple: do not publish private client-specific findings without permission, do not store unnecessary sensitive data, do not use fake proof, and do not copy a customer's exact titles, tags, descriptions, photos, designs, or private strategy documents. Section 7 defines the opportunity signal system in full.

---

## 2. Data Retention Philosophy

The philosophy in plain language:

- **Collect what makes the next report better, and what makes SearchClarity smarter.** If a stored field will improve a future audit, a follow-up report, a template revision, a generalized observation, or a market opportunity signal — keep it. If it won't, don't store it.
- **Minimize personal data.** Name, email, shop URL, platform username — that's the personal data floor. Phone numbers, home addresses, payment details, demographic data — that's the ceiling we don't approach.
- **Separate two layers cleanly.** Client-specific data and generalized market intelligence live in different operational compartments. The first serves the client. The second serves the business. The separation is what makes it possible to use the intelligence layer freely.
- **Store context, not surveillance.** We store snapshots of what listings looked like at audit time — not ongoing monitoring, not buyer behaviour, not anything the client didn't hand us through intake.
- **Avoid hoarding sensitive information.** Revenue numbers, profit margins, supplier names, conversion rates — we ask for these only when a specific report (Report 10) genuinely needs them, and we minimize how long they live in our records once delivery is complete.
- **Treat the intelligence layer as a business asset.** Market opportunity signals, generalized observations, keyword cluster patterns — this is legitimate business intelligence created from SearchClarity's own analytical work. We use it. That's the point.

**Doctrine statement (internal):**

> SearchClarity stores SEO work history to improve service quality for returning customers, sharpen our methodology over time, and build a market intelligence layer that informs our own strategy, content, products, and future listings. Every paid engagement is also market research, and we treat it that way. We do not store payment data, platform credentials, customer-buyer personal data, or sensitive financial information unless a specific report genuinely requires it. We do not copy a paying customer's specific products, listings, titles, tags, descriptions, photos, or designs, and we do not use their private intake answers or outcome data as competitive strategy. We research opportunities independently using public data — client work is the signal that points us toward research, not the basis for acting.

---

## 3. Data Categories To Store

| Category | Store? | Why | Example Fields | Sensitivity |
|---|---|---|---|---|
| Customer identity | Yes | Returning-customer continuity; delivery; support | First name, email, Fiverr/Etsy username (whichever applies) | Medium — minimize to what we need |
| Platform identity | Yes | We need to know where they came in (Fiverr, direct, etc.) for support routing | Source platform, platform handle, order ID on that platform | Low |
| Shop / website identity | Yes | Core to every report; required for returning customers | Shop name, shop URL, platform (Etsy / Shopify / etc.) | Low — public information |
| Orders | Yes | Service history; revenue records; package tier history | Order ID, report type, tier, date, status, turnaround | Low |
| Reports delivered | Yes | Returning customers expect us to know what we gave them | Report type, report version, delivery date, analyst initials | Low |
| Report files (PDF/XLSX) | Yes | We must be able to re-send and build on prior reports | Filename, file hash, storage path | Medium — contains client-specific findings |
| Intake answers | Yes | Recommendations are only defensible if intake context is preserved | All required intake fields per report type | Medium — may include positioning, sometimes revenue if Report 10 |
| Listings / pages reviewed | Yes | Snapshot at time of audit; enables before/after comparisons later | Listing URL, listing ID if available, snapshot date | Low — publicly viewable |
| Title / tags / descriptions at time of review | Yes | Required to track whether the client implemented our recommendations | Captured title text, tag list, description text, attributes, category | Low — publicly viewable |
| Keywords researched | Yes | Feeds future research and generalized clustering | Keyword, cluster, intent, estimated demand, source, date | Low |
| Data source snapshots | Yes | We need to know what eRank/Trends told us in the past; tool data shifts | Tool name, query, result excerpt, date | Low |
| Recommendations given | Yes | Foundation for follow-up reports; enables outcome tracking | Recommendation text in full 5-line block, listing/page reference, priority | Medium — internal-facing for now |
| Caveats given | Yes | Legal/trust trail; shows what we did and didn't promise | Caveat text per recommendation, plus boilerplate version used | Low |
| Action plans | Yes | Returning customers ask which items they completed | Action item text, priority, target listing, status (if reported back) | Medium |
| Customer-shared outcomes | Yes | Validates which recommendations work; never used as public proof without consent | Outcome text, date, confidence label, implementation status | High — sensitive; never republished without explicit consent |
| Revision requests | Yes | Operational learning; spot patterns in what buyers push back on | Revision reason, date, resolution | Low |
| Follow-up notes | Yes | Returning-customer context | Internal notes from analyst, date | Medium |
| Recurring issue patterns | Yes | Generalized layer; abstracted from many clients | Pattern label, frequency, niches observed in, example types | Low — by design, not client-specific |
| Market opportunity signals | Yes | Generalized layer; informs independent research | Signal label, evidence type (number of clients seen in / public source), date noted | Low — by design |
| Generalized observations | Yes | Reusable insights for templates, methodology, content | Observation, supporting evidence, confidence level | Low — by design |
| Payment data | **No** | Handled by the platform (Fiverr/Stripe/etc.); we don't need it | — | Critical — do not store |
| Customer-buyer personal data | **No** | We have no use for the client's own customers' names, addresses, etc. | — | Critical — do not store |
| Private analytics credentials | **No** | If a client shares GSC access, we view, take notes, never store credentials | — | Critical — do not store |
| Private revenue / profit data | **Only when Report 10 requires** | Otherwise irrelevant; if collected, retention is tightly time-boxed (see Section 10) | Rough split percentages preferred over exact figures | High — minimize collection, short retention |
| Customer home address | **No** | We don't ship anything; no operational need | — | Critical — do not collect |
| Platform passwords / API keys | **No** | We do not log in as the client; this is a firm boundary | — | Critical — refuse if offered |
| Personal phone numbers | **No** | Email is sufficient for all delivery and support | — | Critical — do not collect |
| Private supplier info | **No** | Irrelevant to SEO work | — | Critical — do not collect |
| Copyrighted client assets beyond what's needed | **No** | We don't archive photos, designs, branded media unless directly referenced in a report finding | — | High — minimize |

The store/don't-store distinction is enforced by the intake form (which simply doesn't ask for the don't-store items) and by analyst training (which trains analysts to refuse credential offers and to minimize anything sensitive that arrives unsolicited).

---
## 4. Customer-Specific History Model

Conceptual structure — not a database schema. Eleven objects, each with a purpose, key fields, how it helps future reports, and the retention concern that constrains it.

### 4.1 Customer

| Aspect | Detail |
|---|---|
| Purpose | Identify the person paying for work; route delivery and support; recognise returning customers |
| Key fields | First name; email; preferred contact method; date of first order; total orders; communication notes (timezone, response speed) |
| How it helps future reports | Returning customer triggers a "prior history" check before the new report is started — analyst sees what we already know and avoids re-asking |
| Retention concern | Minimize personal data; email and first name are enough for almost everything; never collect phone, address, demographic data |

### 4.2 Shop / Website

| Aspect | Detail |
|---|---|
| Purpose | The unit of work — every report is anchored to a shop or site |
| Key fields | Shop name, shop URL, platform (Etsy / Shopify / WordPress / etc.), niche descriptor in client's own words, opened date if known, total listing count at first order |
| How it helps future reports | Shop is the join point — listings, reports, recommendations, and outcomes all link back here. Niche descriptor is gold for generalized learning later |
| Retention concern | Shop URLs are public; safe to retain. Niche descriptor may include positioning detail the client considers private — treat as Medium sensitivity |

### 4.3 Platform Account

| Aspect | Detail |
|---|---|
| Purpose | Capture how the customer found us and where the order lives, for support and for source-channel learning |
| Key fields | Source (Fiverr / direct / referral / etc.), platform username on Fiverr if applicable, platform order ID |
| How it helps future reports | Lets us route revisions and follow-ups through the right channel; gives us source-channel data for our own marketing |
| Retention concern | Low — operational |

### 4.4 Order

| Aspect | Detail |
|---|---|
| Purpose | The transactional record of a paid engagement |
| Key fields | Order ID, customer reference, shop reference, report type, tier (Basic / Standard / Premium per r04 Section 14), order date, agreed turnaround, actual delivery date, current status (received / in progress / delivered / closed), add-ons |
| How it helps future reports | Order history is what a returning customer expects us to know. "You delivered my Audit on March 12 — what's next?" — the order record answers this without asking the customer to remember |
| Retention concern | Low; the order record itself is non-sensitive but it points to sensitive content (reports, intake) |

### 4.5 Report

| Aspect | Detail |
|---|---|
| Purpose | The deliverable artifact and its metadata |
| Key fields | Report ID, order reference, report type, template version used, analyst initials, reviewer initials, delivery date, file references (PDF, XLSX), executive summary text (for quick recall), key findings count, action plan item count |
| How it helps future reports | A returning customer's new report opens with: "Here's what we recommended in the prior report; here's what's still relevant; here's what's changed." The Report object is the bridge |
| Retention concern | The file itself is Medium — it contains client-specific findings. Store with access controls; don't expose in any shared workspace beyond analysts directly on the account |

### 4.6 Audited Listing / Page

| Aspect | Detail |
|---|---|
| Purpose | Snapshot of a specific listing or page at the moment of audit |
| Key fields | Listing/page URL, listing/page ID if available, snapshot date, captured title, captured tags (Etsy), captured description (full text), captured category/attributes, captured photos (URL references only — we don't download), report reference linking back to the audit that captured it |
| How it helps future reports | Lets us compare "what the listing looked like when we audited" vs. "what it looks like now" — critical for outcome tracking and for second-order audits |
| Retention concern | Public information at the time of capture — Low sensitivity. But we store *snapshots* (text captured), not photos (URL references only). We don't archive image files unless a specific report finding genuinely requires it |

### 4.7 Keyword Observation

| Aspect | Detail |
|---|---|
| Purpose | The atomic unit of keyword research; every keyword we research for any client becomes a row here |
| Key fields | Keyword text, cluster (per r04 Section 6.6 nine-cluster system), buyer intent, product fit, estimated demand, competition note, seasonality, recommended use, confidence, source (tool name), source date, the report this was researched for, the niche it was researched in |
| How it helps future reports | The same keyword researched for Client A six months ago doesn't need to be researched cold for Client B today. We update tool numbers if stale; the cluster, intent, and seasonality assessments are already done. Massive efficiency gain |
| Retention concern | Low — keyword text and tool data are not client-specific. But the linkage back to "we researched this for Client A" is — keep that linkage internal and never publish |

### 4.8 Recommendation

| Aspect | Detail |
|---|---|
| Purpose | Every individual recommendation in every report — the five-line block from r04 Section 3.4 |
| Key fields | Recommendation ID, report reference, listing/page reference if applicable, observation text, why-it-matters text, recommendation text, how-to-implement text, caveat text, priority (do first / do next / test later / avoid), pattern tag (which generalized pattern this maps to, if any) |
| How it helps future reports | Returning customer wants a re-audit — we open the prior recommendations, check which were implemented (from outcome data or visible listing changes), and the new report focuses on what's still outstanding plus what's emerged. The pattern tag is what feeds generalized learning later |
| Retention concern | Medium — the recommendation is client-specific until abstracted. Pattern tag is the bridge to the generalized layer |

### 4.9 Action Plan Item

| Aspect | Detail |
|---|---|
| Purpose | The Do-first / Do-next / Test-later / Avoid items from each report; functionally a subset of Recommendation but kept separate for outcome tracking |
| Key fields | Item ID, report reference, item text, priority, target listing/page, implementation status (not implemented / implemented / partially implemented / unknown), outcome status (linked to Outcome object) |
| How it helps future reports | This is the layer the returning customer most often refers to. "Did you do the title rewrite we recommended?" — the analyst checks the item status, not the whole report |
| Retention concern | Medium |

### 4.10 Follow-Up / Outcome

| Aspect | Detail |
|---|---|
| Purpose | Customer-shared outcomes; analyst-observed outcomes from re-audits; the empirical layer |
| Key fields | Outcome ID, recommendation/action-item reference, outcome text (in client's words or analyst's words), date, source (customer-reported / analyst-observed / tool-rechecked), confidence (high / medium / low / unverified), implementation status, outcome label (see Section 13 — Not implemented / Implemented, no data yet / Implemented, positive signal / Implemented, mixed signal / Implemented, negative signal / Unknown), consent-for-public-use flag (default: No) |
| How it helps future reports | Validates which recommendations move the needle; sharpens future recommendations; cautious source for case studies (only with explicit consent) |
| Retention concern | High — outcomes can include revenue mentions, ranking screenshots, customer commentary about their own business. Treat as confidential by default. Public use requires the consent flag set explicitly to Yes plus a written consent record |

### 4.11 Revision / Support Note

| Aspect | Detail |
|---|---|
| Purpose | Operational record of revisions, support messages, and post-delivery conversations |
| Key fields | Note ID, order/report reference, date, channel (Fiverr message / email / etc.), summary text (not full transcript unless legally needed), category (factual revision / wording revision / scope dispute / question / outcome share), resolution |
| How it helps future reports | Spot patterns — "this category of revision comes up every third Audit" — informs template improvements. Also serves the next analyst working with this customer |
| Retention concern | Medium — may contain sensitive client commentary; store summaries, not raw transcripts, unless a transcript is operationally necessary |

---

## 5. Generalized Market Learning Model

Generalized learning is what makes SearchClarity smarter over time without compromising any individual client. The transformation flow is:

```
Client-specific observation
    → normalized issue pattern
    → aggregated market pattern
    → reusable SearchClarity insight
    → improved report / template / service / product / listing strategy
```

Three things make this safe:

1. **Abstraction strips identity.** Once a pattern is observed in 5+ unrelated clients, it loses its connection to any one of them.
2. **Generalized observations are stored separately.** Different operational layer; different access pattern; the link back to "originally observed in Client X's audit" exists for internal traceability but is never used in any output.
3. **Public sharing requires a higher bar than internal use.** Internal template improvements can use generalized patterns freely. Public content (blog posts, case studies, marketing) requires patterns to be either observed in 10+ unrelated clients *or* corroborated by independent public research.

### 5.1 Worked examples

**Example 1 — Etsy titles**

| Stage | Content |
|---|---|
| Client-specific observation | Client A's listing title is "Smells Like Retirement Candle Funny Retirement Gift for Coworker Retirement Party Decor Gag Gift" — leads with cute phrase, buries the buyer-intent term in position 5–7 |
| Normalized issue pattern | "Title leads with cute or theme phrase; buyer-intent recipient/occasion term buried mid-title" |
| Aggregated market pattern | Observed across 12 unrelated gift-niche Etsy audits over 6 months |
| Reusable SearchClarity insight | For gift listings, lead titles with recipient + occasion + product type; cute phrases work better as secondary positioning |
| Application | Updated standard recommendation pattern in r04 Section 4 template; added as a default check in the Title Structure Analysis section of Report 1 |

**Example 2 — Etsy tags**

| Stage | Content |
|---|---|
| Client-specific observation | Client B uses the same 13 tags across 47 listings |
| Normalized issue pattern | "Identical tag set across all listings — low-signal pattern" |
| Aggregated market pattern | Observed in 18 of 24 audited shops where listing count exceeds 20 |
| Reusable SearchClarity insight | Identical tag sets are the modal failure pattern for established Etsy shops, not the exception. Make it a standard finding in shop-level audits |
| Application | Now a default check in Report 5 (Shop Visibility); also surfaced in Report 1 cross-listing patterns chapter |

**Example 3 — Keyword clusters**

| Stage | Content |
|---|---|
| Client-specific observation | Client C's research surfaced "personalized 2026 retirement gift" with low competition and high specificity |
| Normalized issue pattern | "Year-specific personalization terms underserved" |
| Aggregated market pattern | Observed across retirement, wedding, graduation, and birthday niches in 8 separate keyword research packs |
| Reusable SearchClarity insight | Year-specific personalization is a recurring underserved sub-niche across occasion-driven gift categories; recommend as a rotating annual term |
| Application | Added as a standard cluster check in r04 Section 6.6; surfaces in Keyword Research Pack methodology |

**Example 4 — Competitor observations**

| Stage | Content |
|---|---|
| Client-specific observation | For Client D's term "personalized retirement gift for coworker", top results lean functional (mugs, plaques) over decorative (candles, ornaments) at ~11:4 |
| Normalized issue pattern | "Buyer intent for [recipient]+[occasion]+[personalization] queries skews functional over decorative" |
| Aggregated market pattern | Observed in 7 of 9 gift-niche Competitor Observation reports across different recipient/occasion combinations |
| Reusable SearchClarity insight | When a decorative product targets a recipient-specific gift query and underperforms, the pattern is more likely buyer-intent mismatch than listing weakness. Diagnostic question added to analyst training |
| Application | New row in Report 4 standard analysis framework; warning added to Report 1 when audit identifies decorative products targeting functional-skew queries |

**Example 5 — Shop structure**

| Stage | Content |
|---|---|
| Client-specific observation | Client E runs a shop split across three unrelated niches (retirement gifts, wedding gifts, funny coworker candles); each group competes independently |
| Normalized issue pattern | "Niche fragmentation across active listings dilutes shop-level signal" |
| Aggregated market pattern | Observed in roughly half of Shop Visibility Reports for shops over 40 listings |
| Reusable SearchClarity insight | Niche fragmentation is the dominant shop-level visibility problem at 40+ listings — more impactful than any individual listing fix |
| Application | Added as a top-priority diagnostic in r04 Section 8; informs the recommended path section of Report 5 |

**Example 6 — Pinterest**

| Stage | Content |
|---|---|
| Client-specific observation | Client F (established Etsy seller, 18 months in) asks for a Pinterest plan after Audit and Keyword Pack |
| Normalized issue pattern | "Pinterest requests cluster among sellers with existing Etsy traction, not pre-launch sellers" |
| Aggregated market pattern | 8 of 10 Pinterest Plan orders come from sellers with 12+ months Etsy history |
| Reusable SearchClarity insight | Position Pinterest Plan as a *traction-stage* product, not a launch-stage product. Sell sequencing: Audit → Keyword Pack → Pinterest |
| Application | Updated r04 Section 9.1 "When to sell"; informed the Channel Priority table in Report 10 |

**Example 7 — Shopify product pages**

| Stage | Content |
|---|---|
| Client-specific observation | Client G's Shopify meta titles include the brand name in position 1, consuming 13 characters before any buyer-intent term |
| Normalized issue pattern | "Brand-first meta titles waste high-value early characters" |
| Aggregated market pattern | Observed in 14 of 18 Shopify audits |
| Reusable SearchClarity insight | Brand-first meta titles are the default in most Shopify themes; sellers don't realise this is configurable. Make it a top finding |
| Application | Now a default check in Report 7; added to analyst training |

**Example 8 — Schema readiness**

| Stage | Content |
|---|---|
| Client-specific observation | Client H's Shopify product pages have basic Product schema (auto-generated) but lack Brand, AggregateRating, and MerchantReturnPolicy fields |
| Normalized issue pattern | "Auto-generated Shopify Product schema is incomplete relative to current Google Rich Results requirements" |
| Aggregated market pattern | Observed in 11 of 12 Shopify schema audits regardless of theme |
| Reusable SearchClarity insight | The auto-generated baseline is universally incomplete; assume incomplete and check for the three specific missing fields by default |
| Application | Standard table in Report 8 expanded to highlight these three fields explicitly |

**Example 9 — AI search readiness**

| Stage | Content |
|---|---|
| Client-specific observation | Client I's AI search readiness audit found that prompts for the brand return partial information — assistant knows category but not founder, products, or positioning |
| Normalized issue pattern | "Brand entity ambiguity to AI search systems — partial recognition without specificity" |
| Aggregated market pattern | Observed in 6 of 7 AI readiness audits to date |
| Reusable SearchClarity insight | Partial recognition is the modal state for small brands; the readiness gap is consistently in FAQ/About content depth and third-party mention sparsity, not in schema |
| Application | Reordered Report 9 priority recommendations to lead with entity content depth before schema |

**Example 10 — Cross-channel concentration**

| Stage | Content |
|---|---|
| Client-specific observation | Client J generates 92% of revenue from Etsy despite 14-month-old Shopify store |
| Normalized issue pattern | "Single-channel revenue concentration with inactive owned-asset channel" |
| Aggregated market pattern | Common pattern in established Etsy sellers who have launched but not invested in Shopify |
| Reusable SearchClarity insight | The default Strategy Report Channel Priority table should flag Shopify-inactive-but-launched as a top diversification readiness opportunity, not as a "build a Shopify store" recommendation |
| Application | Updated Report 10 Channel Priority table in r04 Section 13.5 |

**Example 11 — Revision patterns**

| Stage | Content |
|---|---|
| Client-specific observation | Client K asks for revision because they expected specific tags, not "tag directions" |
| Normalized issue pattern | "Buyers conflate audit and rewrite reports" |
| Aggregated market pattern | This revision reason appears in ~15% of Audit orders |
| Reusable SearchClarity insight | Audit description must clarify "diagnosis, not implementation" more aggressively at the point of sale and in delivery messages |
| Application | Updated Audit gig copy and Report 1 delivery message in r04 Section 16.3 |

**Example 12 — Returning-customer attach**

| Stage | Content |
|---|---|
| Client-specific observation | Client L purchases Audit then asks immediately about title/tag rewrites |
| Normalized issue pattern | "Audit→Rewrite attach within 7 days of delivery" |
| Aggregated market pattern | This sequence describes ~40% of second orders |
| Reusable SearchClarity insight | Audit delivery message should always close with the Rewrite as the recommended next step (already in r04 Section 16.3); offer a returning-customer discount |
| Application | Standardised in r04 Section 16.3 delivery template |

---
## 6. Returning Customer Use Cases

The point of storing history is concrete value delivered to the returning customer. Nine scenarios, each one showing what stored history gets used and how it improves the next deliverable.

| Returning Customer Scenario | Stored History Used | Better Feedback We Can Give |
|---|---|---|
| Customer buys a second Audit on the same shop, 3+ months after the first | Prior report; prior listing snapshots; action plan items with implementation status; outcome notes | "Of the 12 Do-first items we recommended in March, here's what's now reflected in your live listings (X, Y, Z) and what isn't (A, B). The new audit focuses on what's still outstanding plus the new listings you've added since." Saves analyst hours; shows the customer we actually remembered |
| Customer buys Title/Tag Rewrite after Audit | Original Audit; per-listing diagnoses; tag coverage analysis; keyword opportunities surfaced | "We're implementing the rewrites we already diagnosed — here's the rationale traced back to your Audit." Rewrites become defensible rather than guesswork. Analyst time on the Rewrite drops substantially |
| Customer buys Keyword Research Pack after Audit | Audit findings on missing keyword angles; cluster gaps surfaced; the niche descriptor; competitor patterns if Report 4 was purchased | "Your Audit flagged missing recipient-intent and occasion angles. The Keyword Pack focuses heavily on those clusters and lighter on what you're already covering." Customer gets a non-generic pack tuned to their actual gaps |
| Customer buys Shop Visibility Report after multiple Listing Audits | All prior listing audits aggregated; cross-listing patterns already identified; niche descriptor | "We've already audited 12 of your listings individually — the Shop Report builds shop-level patterns on top of that, doesn't re-audit them." Big efficiency gain; customer sees continuity |
| Customer asks if prior recommendations still apply (6+ months later) | Prior recommendations; listing snapshots at recommendation time; current live state checkable at analyst's end | "These 7 recommendations still apply because the listings haven't changed. These 3 are now moot because the listing has been retired. These 2 need updating because Etsy's search appears to have shifted on this term." Customer gets a quick check-in rather than a full new report |
| Customer shares outcomes after implementing recommendations | Action plan items linked to outcome records; confidence labels | Analyst can update internal patterns ("this recommendation pattern produced positive signal in X% of follow-ups") *and* tell the customer "your outcome aligns with what we see across other shops — here's the next adjustment to test" |
| Customer expands from Etsy to Shopify | Niche descriptor; positioning; Etsy keyword research already done; recommendations already made | "Your Shopify product page meta titles should lean on the keyword work we already did for Etsy — here's how the same research maps to Google search vs. Etsy search." Saves customer from paying for redundant research |
| Customer asks for AI Search Readiness later | All prior reports; brand mentions noted in earlier intake; entity content already reviewed during Shop or Shopify audits | "The entity content gaps we already noted in your About and FAQ are the foundation of the AI Readiness recommendations. Here's the layered plan." Layered, not stacked |
| Customer wants a 90-day Visibility Strategy Report | Every prior report; outcomes; implementation status; revision themes | Strategy Report becomes a genuine synthesis, not a stitched-together summary. The 30/60/90 plan can lean on what's already done and what's still outstanding, with realistic measurement signals based on the customer's actual implementation history |

The pattern across all nine: returning customers are *the* customers worth optimising for. The cost of acquisition is zero. The trust is already established. The value of the second order is materially higher if we've remembered them, and materially lower if we haven't.

---

## 7. Market Signal Capture During Paid Research

Every paid report can generate internal market intelligence. SearchClarity is not just delivering one-off customer reports; it is watching real niches, real listings, real keyword clusters, real buyer intent, and real marketplace gaps as paid work happens.

When analysts work on customer reports, they should pay attention to:

- niche demand
- product category strength
- buyer intent clarity
- keyword depth
- keyword cluster quality
- competition weakness
- product variation opportunities
- seasonality
- pricing bands
- marketplace fit
- Pinterest/content potential
- Shopify/site expansion potential
- schema/AI search readiness gaps
- whether sellers in the niche look sloppy
- whether the niche deserves deeper research later

Market signals are internal observations. They are not automatically part of the customer deliverable. If a signal is relevant to the paid report, it can appear as part of the customer's analysis. If it is not relevant to the customer's scope, it stays internal.

The point is blunt: paid SEO work shows us where money might be hiding. We mark it down.

The flow is:

```text
Paid report work
    → analyst notices a niche/product/keyword/market gap
    → analyst logs a Market Opportunity Signal
    → signal receives a simple score
    → low scores are ignored or watched
    → strong scores get researched later
    → validated signals improve services, content, strategy, or future products/listings
```

SearchClarity may record niches, product categories, keyword clusters, buyer-intent patterns, marketplace gaps, and opportunity signals discovered during client work. A market signal is not automatically a product or listing idea. It is an opportunity to research.

SearchClarity may use market signals to:

- improve reports
- improve service templates
- improve gig positioning
- create content
- identify niches worth researching
- build future products/listings
- improve internal marketplace strategy
- feed Neon Ronin's broader observatory and strategy layer

### 7.1 What Counts As A Market Opportunity Signal

An analyst should flag a signal whenever paid research surfaces something that looks commercially interesting. Examples:

- A keyword cluster with meaningful buyer intent and weak competition.
- A sub-niche where top listings are visibly sloppy, generic, thin, or poorly optimized.
- A buyer-intent angle that appears frequently in search but has few listings that genuinely serve it.
- A recipient, profession, occasion, style, material, or personalization combination with obvious search paths.
- A product category that appears repeatedly in research but lacks strong dedicated supply.
- A niche with many long-tail keyword variants.
- A Pinterest or content pattern with clear visual/search demand.
- A Shopify category where many sellers have weak product pages, weak FAQs, or missing schema.
- A small ecommerce niche where AI search readiness is poor across the board.
- A Fiverr or SEO-service demand pattern discovered from buyer questions or repeat requests.

Signals do not need to be certain to be logged. Log the signal, score it honestly, and move on. The score decides whether it deserves more time.

### 7.2 Opportunity Signal Scoring

Every Market Opportunity Signal gets scored across 12 factors. Each factor receives a score from 1 to 5.

- 1 = weak / bad / unclear
- 3 = decent but not proven
- 5 = strong / obvious / attractive

Higher is better. For Risk / IP exposure, lower risk gets the higher score.

| Factor | Score 1–5 | What To Look For |
|---|---:|---|
| Buyer intent clarity |  | Are people searching with purchase intent? |
| Keyword depth |  | Are there enough long-tail and cluster terms? |
| Demand signal |  | Does the niche appear to have meaningful search/market demand? |
| Competition weakness |  | Are competitors sloppy, generic, poorly optimized, or thin? |
| Differentiation room |  | Can we create a distinct angle? |
| Product variation potential |  | Are there many recipient/occasion/style/material variants? |
| Seasonality |  | Is there evergreen demand, seasonal demand, or both? |
| Content expansion potential |  | Can we build SEO/Pinterest/site content around it? |
| Marketplace fit |  | Does it fit Etsy, Shopify, Pinterest, Fiverr, or other channels? |
| Operational difficulty |  | Is it realistic to execute without a nightmare? |
| Risk / IP exposure |  | Are there trademark, copyright, or policy risks? Lower risk scores higher. |
| Strategic value |  | Does this help SearchClarity/Neon Ronin learn or expand? |

Maximum score: 60.

| Total Score | Classification | Meaning |
|---:|---|---|
| 0–25 | Ignore | Not worth time now. Keep only if the note may matter later. |
| 26–35 | Watch | Interesting but weak. See if it appears again. |
| 36–45 | Research Later | Worth researching when time opens up. |
| 46–55 | Research Next | Strong signal. Put it near the top of the research queue. |
| 56–60 | Serious Opportunity | Very strong. Research promptly and consider action if validated. |

This scoring is intentionally simple. If analysts need a spreadsheet formula, use:

```text
opportunity_score = sum(all 12 factor scores)
```

Do not over-engineer it yet.

### 7.3 Market Opportunity Signal Record

Each signal gets one record. The record should be useful without exposing private client details.

| Field | Purpose |
|---|---|
| signal_id | Unique internal ID |
| date_observed | When we noticed it |
| source_report_type | Which paid service surfaced it |
| source_context | General context without exposing private client details |
| niche | Broad niche/category |
| product_category | Product or service category |
| marketplace | Etsy, Shopify, Pinterest, Google, Fiverr, etc. |
| buyer_intent | What buyers appear to want |
| keyword_cluster | Main keyword group |
| why_it_stood_out | Analyst explanation |
| evidence_summary | High-level evidence without private client details |
| opportunity_score | Total score |
| confidence | Low / Medium / High |
| recommended_next_step | Ignore / Watch / Research / Validate / Build |
| status | Current state |
| notes | Internal notes |

Allowed status values:

- Logged
- Watch
- Research Later
- Research Next
- Validated
- Rejected
- Converted to Internal Project
- Converted to Content
- Converted to Service Improvement
- Converted to Listing/Product Idea

### 7.4 Market Opportunity Use Policy

SearchClarity may record niches, product categories, keyword clusters, buyer-intent patterns, marketplace gaps, and opportunity signals discovered during client work.

This is allowed because SearchClarity is doing real analysis in real markets. The analysis has value beyond a single report. That is part of the business model.

A market signal is not automatically a product or listing idea. It is an opportunity to research.

SearchClarity may use these signals to:

- improve customer reports
- improve report templates
- improve analyst checklists
- improve gig positioning
- create SearchClarity.co content
- identify niches worth researching
- build future products/listings
- improve internal marketplace strategy
- feed Neon Ronin's strategy layer

Hard lines:

- Do not publish or expose private client-specific findings without permission.
- Do not store or misuse unnecessary sensitive data.
- Do not use fake proof.
- Do not copy a customer's exact titles, tags, descriptions, photos, designs, or private strategy documents.
- Do not present one customer's reported results as a general marketing claim.

What this policy does **not** do: it does not prevent SearchClarity or Neon Ronin from researching or entering a good niche. If paid work surfaces a strong market signal, we log it, research it, validate it with public data, and decide what to do.

### 7.5 Research Workflow For Strong Signals

Signals classified as **Research Later**, **Research Next**, or **Serious Opportunity** should eventually get independent research.

Research should use public or properly licensed sources such as:

- Etsy search observation
- eRank or comparable Etsy tools
- Google Trends
- Pinterest Trends
- Google SERPs
- Shopify/site observations
- Fiverr/Upwork marketplace observations
- public competitor listings
- public content gaps

The research workflow:

1. Pull the signal record.
2. Confirm the score still looks reasonable.
3. Run public-data research.
4. Update the evidence summary.
5. Decide whether the signal is Rejected, Watch, Research Next, Validated, or Converted.
6. If converted, label the conversion type: content, service improvement, internal project, or listing/product idea.

### 7.6 Example Market Signals

| Example | Signal | Why It Stood Out | Sample Score | Next Step |
|---|---|---|---:|---|
| Profession-specific retirement gifts | Retirement gift searches split by profession: teacher, nurse, police, firefighter, coworker, boss | Strong buyer intent, lots of recipient variants, obvious personalization angles | 52 | Research Next |
| Teacher appreciation digital printables | Searches cluster around teacher appreciation week, end-of-year gifts, classroom signs, thank-you notes | Seasonal demand plus easy product variation; good Etsy/Pinterest fit | 48 | Research Next |
| Pet memorial gifts | Long-tail searches around dog memorial, cat memorial, loss of pet, personalized pet remembrance | Emotional buyer intent, strong personalization, evergreen demand | 50 | Research Next |
| Wedding template bundles | Buyers search for editable wedding signs, seating charts, invitation bundles, Canva templates | Deep keyword clusters and product variation; competition may be strong but sloppy in sub-niches | 44 | Research Later |
| Shopify product pages with missing FAQ/schema | Small ecommerce product pages often lack FAQ blocks, Product schema depth, review markup, return-policy markup | Strong service/template improvement signal; good upsell path from Shopify audit to schema/AI readiness | 47 | Research Next |
| Etsy shops with strong Pinterest potential | Visual products with good gift/decor appeal but no Pinterest strategy | Search + visual discovery fit; content expansion potential high | 43 | Research Later |
| AI search readiness gaps in small ecommerce brands | Brands often have thin About pages, weak FAQs, poor entity clarity, and little third-party mention footprint | Future-facing service opportunity; strong fit with GEO/LLM positioning | 46 | Research Next |
| Weak title/tag structure niche | A niche where top Etsy results use cute titles, repeated tags, and broad single-word terms | Competition weakness is visible; strong chance for better listing structure to stand out | 49 | Research Next |
| Long-tail buyer-intent niche | Many searches combine recipient + occasion + product + personalization | Keyword depth and buyer intent are both strong; useful for reports and possible internal products | 51 | Research Next |
| Fiverr SEO service niche | Customer questions reveal demand for niche-specific Etsy SEO reports, Pinterest plans, or AI readiness audits | Service expansion signal; helps decide which gigs to package next | 42 | Research Later |

### 7.7 Review Cadence

Market Opportunity Signals are reviewed monthly.

The review asks:

- What new signals were logged?
- Which signals scored 46+?
- Which Watch signals appeared repeatedly and deserve a higher score?
- Which signals should move to Research Later or Research Next?
- Which validated signals should become content, service improvements, internal projects, or listing/product ideas?
- Which signals are weak enough to ignore?

At low volume, this is a 30-minute monthly spreadsheet review. Do not turn it into ceremony.

---

## 8. Privacy / Platform / Trust Boundaries

These are practical operating boundaries. Where law or platform Terms of Service might apply, we flag what needs verification — we don't invent it.

| Boundary | Rule | Why It Matters |
|---|---|---|
| Fiverr off-platform contact risk | Do not move communication off Fiverr during an active Fiverr order. Direct contact (email, phone) only after the order is complete *and* the customer initiates it — and even then, prefer continuing in Fiverr where possible | Fiverr's TOS treats off-platform solicitation as a serious violation; account termination is the typical penalty. Needs verification of current Fiverr TOS for each new policy revision |
| Etsy seller/customer personal data | We do not collect or process the customer's own buyers' personal data. If a customer shares an Etsy Marketplace Insights screenshot that includes their buyer information, we ask them to redact before re-sharing | The customer's buyers haven't consented to anything with us; we have no basis to handle their data |
| Payment data | Never store. Payment is handled by Fiverr / Stripe / whatever platform; we don't see card numbers and we don't want to | Storing payment data invites PCI-DSS obligations and breach liability. There is no operational reason to keep it |
| Etsy buyer personal data | Never store. If it appears in materials the customer sends us, we redact internally and ask the customer to redact in future | Same as above — third parties who haven't consented to our data handling |
| Email lists / marketing | A customer is not opted in to marketing emails by virtue of placing an order. Marketing email requires a separate, explicit opt-in at intake or post-delivery. Default to off | Anti-spam laws (CAN-SPAM in the US, PECR/GDPR in the UK/EU, CASL in Canada) require explicit consent for marketing emails. Order delivery emails are transactional and allowed; promotional emails are not |
| Off-platform sales push in Fiverr messages | Do not use the Fiverr message channel to push direct-purchase off-platform | Fiverr TOS violation. Always direct returning customers to place orders through the same channel they first used, until they explicitly choose to move off-platform |
| Platform credentials | Refuse if offered. We do not store, use, or hold platform passwords, API keys, or active session tokens. If a customer offers, we explain the policy and ask for a different way to share what we need (screenshots they take and send) | A credential breach implicates us in unauthorized access. The policy line is firm: we do not act as the customer on their accounts |
| Analytics access (GSC, Etsy Insights) | Optional, never required for basic services. When granted, view-only; do not export raw data beyond what's needed for the report; do not retain credentials | Reduces the customer's data exposure; reduces our breach liability |
| Testimonials / case studies / public examples | Written consent required, scoped specifically to what's being shown. Verbal consent is not enough. Consent must specify what's shared (shop name? screenshot? findings?) and where it appears (website? Fiverr profile? blog?) | A customer who didn't realise their case study would be on the public website is a churn risk and a trust risk |
| Anonymizing real client work | When using a real example without consent for naming, all identifying details must be removed: shop name, exact product, distinctive phrases, photos, dates that pinpoint the order. Use "a personalized gifts shop on Etsy" not "[Shop Name]" | The test: can a reader Google the example details and find the actual shop? If yes, it's not anonymized |
| Fictional samples vs. real samples | Public mock samples (like the "Smells Like Retirement" example in r04) are fictional and labelled as such. Real samples — even anonymized — appear only with consent | Fictional samples avoid the consent question entirely. They should be the default for marketing |
| Sensitive findings in delivery | When a report surfaces something the customer didn't ask about (e.g., a possible trademark issue with one of their products), deliver it carefully in the report, not as a casual side comment in a chat message | Casual chat comments don't have the caveat framing the report does, and create unnecessary alarm or legal exposure |

**Items that need verification in the current platform TOS** before formal policy publication: Fiverr's specific 2026 rules on off-platform contact, repeat-customer messaging, and external links in delivery files; Etsy's policies on third-party SEO services representing themselves to Etsy sellers; whether any platform restricts SEO services from storing screenshots of marketplace data.

---

## 9. Data Minimization Rules

Explicit list of what we don't store, and why.

| Data Type | Store? | Reason |
|---|---|---|
| Credit card / payment info | **No** | Handled by the platform. No operational use. PCI-DSS exposure if stored |
| Customer home address | **No** | We don't ship; no operational use |
| Etsy buyer personal data | **No** | Not ours to hold |
| Private customer-buyer messages | **No** | Not ours to hold; if shared, summarize and discard the raw |
| Platform passwords / API keys | **No** | Firm boundary; refuse if offered |
| Private analytics credentials | **No** | View-only access; never retain credentials |
| Bank / tax info | **No** | No operational use |
| Unnecessary revenue / profit screenshots | **No** | If shared for a specific report (Report 10), summarise to rough split percentages and discard the screenshot |
| Personal phone numbers | **No** | Email is sufficient for all communication |
| Private supplier info | **No** | Irrelevant to SEO work |
| Unneeded raw screenshots | **No** | Capture the data point we need (e.g., the title text); don't archive the full screenshot |
| Copyrighted client assets beyond report needs | **No** | Photos, designs, branded media — we reference URLs in audit, we don't archive copies |
| Customer's customers' email addresses / contact info | **No** | Not ours to hold |
| Customer's internal team communications | **No** | Out of scope |
| Conversations we accidentally see (in shared docs, etc.) | **No** | If it shows up, we don't read more than necessary, we don't retain it |

**The default question for any new data field:** "Will this make a future report better?" If yes, document why and keep it. If no, don't collect it.

---

## 10. Retention Rules

Recommended retention periods. Practical for a small business, defensible if asked, conservative on sensitive items.

| Data Type | Recommended Retention | Reason |
|---|---|---|
| Order record (transactional facts) | 7 years | Tax/accounting record-keeping in most jurisdictions; check local requirements |
| Report PDF | 3 years from delivery, then archive offline if needed for accounting | Long enough to serve returning customers; not indefinite |
| Spreadsheet deliverable (Reports 2, 3) | 3 years from delivery | Same as PDF |
| Intake answers | 3 years from delivery (or duration of customer relationship if active) | Useful for returning customers; not indefinite |
| Listing / page snapshots | 3 years | Enables before/after comparisons for returning customers; sufficient |
| Keyword observations | 5 years | Tool data ages but cluster/intent assessments retain value; longer retention justified |
| Recommendations | 3 years from delivery | Tied to report lifecycle |
| Outcome notes | 3 years (with consent flag for use), then either consent-confirmed retention or delete | Sensitive; default to delete unless explicit consent for longer retention |
| Revision messages | 1 year summary; raw transcripts 90 days unless legally needed | Operational signal mostly extracted within weeks |
| Generalized observations | Indefinite (no client identifiers) | The intelligence layer is what we're building |
| Raw screenshots from client uploads | 90 days unless directly referenced in a report finding | Don't archive what's not needed |
| Customer contact info (active customer) | Duration of relationship + 3 years | Allows returning-customer recognition |
| Customer contact info (inactive 24+ months) | Delete email and any personal data; retain de-identified order/shop record | Reduces breach exposure for inactive accounts |
| Deleted / cancelled order data | 12 months minimal record (for refund / dispute window), then delete | Just enough for the dispute window |
| Consent records (for case studies, testimonials) | Indefinite for as long as the asset is in use; plus 2 years after retirement | Defensible if the customer later disputes consent |

**Retention discipline matters more than retention duration.** A clear, applied policy at 3 years is far better than an aspirational policy at 1 year that nobody enforces.

---
## 11. Case Studies and Public Samples

How SearchClarity can use past work publicly without burning the trust the work depended on.

| Public Asset Type | Allowed? | Requirements |
|---|---|---|
| Fictional mock reports (like the "Smells Like Retirement" example in r04) | Yes — default and preferred | Labelled clearly as a sample. No real shop, no real listings. The example must be realistic enough to demonstrate quality but invented end-to-end |
| Anonymized real samples (no shop name, no distinctive details, no screenshots) | Yes, with caution | Identifying details fully removed. Apply the "could a reader Google this and find the shop" test. If yes — anonymization has failed; redo or scrap |
| Permission-based case studies (named shop, real findings, with consent) | Yes, with strict requirements | Written consent specifying what is shared (shop name, screenshots, specific findings, outcome data) and where it appears (website page, Fiverr profile, blog post, social media). Verbal consent is not enough. Consent is revocable; if revoked, the asset is taken down within a reasonable window |
| Customer testimonial quotes | Yes, with written consent | Quote must be approved by the customer in writing (in-platform message counts if attributable to the customer). Attribution can be "Sarah K., personalized gifts shop owner" rather than full identification, if the customer prefers |
| Anonymous before/after screenshots | No, by default | Screenshots of a customer's actual listing changes are too easy to back-trace. Use fictional examples instead. Exception: with explicit written consent for that specific screenshot |
| Outcome numbers as marketing claims | No, by default | A single customer's outcome is not a generalizable claim. "Sarah's impressions went up 40%" is misleading as a marketing claim because it suggests other customers will see similar results. If outcomes are referenced at all, frame them as anecdotes with explicit context, not as predictions |
| Aggregated outcome statistics | Yes, with high bar | Only if based on a meaningful sample (15+ outcomes), only with confidence labels included, and only with framing that doesn't imply predictability. "Across [N] follow-up reports, [X]% of customers reported some positive signal on the top-priority recommendation" — that level of caution. Never specific percentage claims tied to specific actions ("our customers see 40% more impressions") |
| Generalized observations / insights | Yes, freely | Patterns observed across 10+ unrelated clients (or 5+ plus public corroboration) can be shared in blog posts, methodology pages, gig descriptions, without identifying any single client |
| Niche-level commentary | Yes, with care | "We've observed that personalized retirement gift listings frequently lead titles with cute phrases rather than buyer-intent terms" — fine, no single client identified. "We audited 24 personalized retirement gift shops" — getting close to identifying specific work; prefer the first framing |
| Methodology explanations | Yes, freely | How we audit, how we cluster keywords, how we score competition — all freely shareable; this is brand-building content |
| Real shop screenshots in marketing | No, by default | Even with consent, marketplace platforms have policies on screenshot reuse, and the trust optics are bad. Use fictional examples |
| Customer name on website "trusted by" or similar | No | Implies endorsement the customer didn't necessarily intend |

### 11.1 Anonymization checklist

Before publishing any "anonymized real example", the analyst applies this checklist:

- Shop name removed.
- Specific product names removed or generalized ("a personalized candle" not "Smells Like Retirement Candle").
- Distinctive phrases (the seller's actual title, the seller's actual tag set) removed or substantially altered.
- Screenshots removed (or so heavily redacted they convey no identifying detail).
- Date specifics removed (use "in early 2026" not "delivered March 12, 2026").
- Geographic specifics removed if the seller is geographically identified.
- Niche specifics generalized one level up (a "retirement gift seller" rather than "a teacher-retirement-gift seller", if the latter narrows the field to a small number of shops).
- The Google test: search the most distinctive remaining detail. If the actual shop appears in the top 20 results, anonymization has failed.

### 11.2 The fictional-sample preference

By default, fictional samples (like the r04 mock) handle the consent question by not having one. The cost is creative effort; the benefit is zero risk to any client. For most marketing purposes, fictional samples are the right call.

---

## 12. Report History Fields Needed For Future Reports

What we save per report type, and what each saved field enables in future work.

| Report Type | Save These Fields | Used Later For |
|---|---|---|
| 1. Etsy Listing Visibility Audit | Per-listing diagnosis text; title/tag/description captures; cross-listing patterns identified; action plan items with priority; pattern tags on each recommendation; analyst initials | Returning audits (compare snapshots); Rewrites (reuse diagnosis as basis for implementation); Shop Visibility Reports (aggregate listing patterns into shop-level findings); Strategy Reports (cite original findings); generalized learning (pattern tags feed the aggregated layer) |
| 2. Etsy Title and Tag Rewrite | Original title + recommended title; original tag set + recommended tag set; rationale per change; tag strategy notes; intent mix description | Outcome tracking when customer reports back; returning Rewrites (don't suggest the same changes twice); template refinement (which rationales held up under outcome data); generalized learning (which title patterns recur as successful) |
| 3. Etsy Keyword Research Pack | Keyword text; cluster assignment; intent; estimated demand at research time; competition note; seasonality; recommended use; source + source date; niche the research was for | Reuse for related clients (massive efficiency); cluster expansion over time; tool-data drift tracking (compare tool numbers across time); generalized learning (cluster popularity, intent patterns by niche) |
| 4. Etsy Competitor Visibility Observations | Search terms observed; observation date; pattern findings (anonymized — no shop names); opportunity gaps identified; recommended response strategy | Returning competitor observations (compare patterns over time on same search terms); Strategy Reports (cite); generalized learning (recurring patterns across niches and search terms) |
| 5. Etsy Shop Visibility Report | Shop-level diagnosis; niche descriptor; listing-group identification; section/category structure; keyword theme consistency findings; shop-level action plan | Returning Shop Reports (rare but valuable if shop has grown materially); Strategy Reports (cite); generalized learning (recurring shop-level issues by shop size band) |
| 6. Pinterest SEO Plan | Board recommendations; pin templates; 30-day plan; keyword themes adapted from Etsy research; seasonal timing notes | Pinterest plan updates as account matures; Strategy Reports (cite as off-platform channel); generalized learning (Pinterest content patterns by niche) |
| 7. Shopify Product Page SEO Audit | Per-page diagnosis; meta title/description captures; description clarity findings; collection notes; FAQ/content gap findings; schema readiness preview | Returning audits (compare); Schema Readiness Audit (use the preview findings as foundation); AI Readiness Audit (FAQ gap findings feed entity work); generalized learning (Shopify-specific patterns) |
| 8. Schema Readiness Audit | Per-page current schema; missing schema opportunities; entity clarity findings; validation results | Returning audits after implementation; AI Readiness Audit (schema alignment); generalized learning (universal schema gaps by platform) |
| 9. AI Search / LLM Visibility Readiness Audit | Brand entity clarity findings; sourceable content review; FAQ/About/Policy review; citation-worthy page opportunities; third-party mention gaps; prompt-visibility check results with date | Returning audits (re-run prompt checks; compare); Strategy Reports (cite); generalized learning (recurring entity gaps; prompt response patterns) |
| 10. Seller Visibility Strategy Report | Synthesis cross-references to all prior reports; channel priority assessment; 30/60/90 plan; measurement plan; metric baseline | Quarterly follow-up reviews; future Strategy Reports (the customer's strategy history is itself a research input); generalized learning (channel-mix patterns by niche and seller maturity) |

The pattern: **what you save now is what the next report can lean on**. The pattern tags on recommendations (Section 4.8) are the single highest-leverage field — they're what bridge client-specific work to generalized learning.

---

## 13. Outcome Tracking

Outcomes are the empirical layer. They're how we tell, over time, whether our recommendations actually work — and they're the data we are least able to verify independently. Rules below are designed to be useful without overclaiming.

### 13.1 Outcome inputs (what counts as outcome data)

- Customer-reported impressions (from Etsy stats, Google Search Console, Pinterest analytics, etc.).
- Customer-reported visits / click-through.
- Customer-reported sales.
- Customer-reported ranking changes.
- Customer-reported conversion or revenue commentary.
- Screenshots, if voluntarily shared (handled per Section 9 — point captured, screenshot itself retained 90 days).
- Follow-up audit observations (we recheck listings ourselves).
- Tool-based recheck (we requery eRank, GSC if granted, Etsy search).
- Customer says "this did not help" — that's an outcome too, and equally important.

### 13.2 Outcome rules

- **Outcomes are self-reported unless we independently verify.** A customer-reported "impressions up 30%" is one data point with low independent confidence. An analyst recheck via GSC (with granted access) is higher confidence.
- **Single-client outcomes do not become public claims.** No marketing material says "we got Sarah a 40% lift." See Section 11.
- **Recommendations are not promised repeatable.** Outcome data informs which recommendation patterns are stronger or weaker, but the language around them stays directional, not promising.
- **Confidence level is always stored alongside the outcome.** A vague positive comment is Low confidence. An analyst-verified GSC delta is High.
- **Implementation status is stored alongside the outcome.** A "no change" outcome on an unimplemented recommendation says nothing about the recommendation.

### 13.3 Outcome fields

| Outcome Field | Meaning | Confidence Level |
|---|---|---|
| Customer-reported impressions change | What the customer told us about impressions | Low to Medium (depending on whether they shared a screenshot or just commented) |
| Customer-reported visits change | Same, for visits | Low to Medium |
| Customer-reported sales change | Same, for sales | Low — sales fluctuate for many reasons; isolating SEO impact is hard |
| Customer-reported ranking change | What position the listing now appears at for a target keyword, per customer | Medium — checkable if we can search the same term |
| Customer-reported conversion / revenue commentary | Qualitative ("things picked up", "no change") | Low |
| Analyst-observed listing change | Did the customer implement the recommendation? (Visible by checking the listing live) | High — we can verify directly |
| Analyst-rechecked search appearance | Where does the listing now appear for the target keyword | High — but a snapshot in time |
| Tool-based metric recheck (eRank / GSC) | Updated tool data | Medium — tool data shifts and is estimated |
| Customer-shared screenshot | Visual evidence of metric change | Medium-High — depends on what's shown |
| Voluntary positive testimonial | Customer expresses satisfaction in their own words | High for satisfaction signal; Low for attributing to specific recommendations |

### 13.4 Outcome labels

Every action plan item gets one of these labels updated over time:

- **Not implemented** — customer hasn't applied the recommendation (verified by checking the listing).
- **Implemented, no data yet** — change is live but it's too early to assess; default for first 21 days post-implementation.
- **Implemented, positive signal** — implementation + some indication of improved performance (customer report, recheck, screenshot).
- **Implemented, mixed signal** — implementation + ambiguous results (some metrics improved, others didn't).
- **Implemented, negative signal** — implementation + clear indication performance got worse.
- **Unknown** — we cannot verify implementation status or outcome.

These labels feed the generalized layer. "Recommendation pattern X has been applied N times with positive signal in Y% of cases" — that's the kind of statement we can defensibly make internally, and (with high enough N) carefully reflect in methodology content.

---

## 14. Observability / Intelligence Metrics

Internal metrics SearchClarity should watch over time. These are not customer-facing; they're operational and strategic.

| Metric | Why It Matters | How To Use It |
|---|---|---|
| Most common listing issues identified | Tells us what the template needs to address best | Strengthen the most-common-issue section in Report 1 template; train analysts on the modal failure patterns |
| Most common title problems | Sharpens Title Structure Analysis section | Add default checks; refine recommendation patterns |
| Most common tag problems | Sharpens Tag Coverage section | Same |
| Niches frequently audited | Tells us where our market is concentrated | Inform gig positioning, marketing focus, and which adjacent niches to consider (per Section 7) |
| Niches with repeat demand (multiple orders, same niche) | Higher value than single-order niches | Justifies developing niche-specific methodology cheat sheets for analysts; could justify niche-specific gig variants |
| Keyword clusters appearing across clients | Shows market-wide demand patterns | Generalized layer; informs r04 Section 6.6 cluster definitions; informs methodology content |
| Recommendations most often reused (pattern tag frequency) | The patterns that recur are the patterns that matter most | Promote to default checks in the relevant report; consider for blog/methodology content |
| Recommendations with positive follow-up signals | Validates which patterns actually move the needle | Strengthen confidence in those recommendation patterns; reflect cautiously in methodology content |
| Recommendations with negative or mixed signals | Tells us which patterns are weaker than thought | Revise; potentially deprecate; warn analysts |
| Report types with most repeat orders | Identifies the highest-LTV report types | Prioritise quality investment; identify natural attach-rate opportunities |
| Revision reasons (categorised) | Operational learning | Spot patterns; fix in gig copy, intake, or report template |
| Average turnaround time per report type | Operational health | Detect drift; flag training needs; inform pricing |
| Customer questions after delivery (categorised) | What our reports are not explaining well enough | Update report template; update gig copy |
| Add-on conversion rates (Audit → Rewrite, Audit → Keyword Pack, etc.) | Revenue per customer; bundle-design signal | Inform delivery message templates (per r04 Section 16); inform bundle pricing |
| First-order to second-order conversion rate | The whole point of returning-customer focus | If low, returning-customer experience is broken; investigate |
| Time between first and second order | Tells us how aggressively to nudge | Inform timing of follow-up review-request messages |
| Outcome label distribution per recommendation pattern | Empirical methodology quality | Direct input to template refinement |
| Market Opportunity Signals logged per month | Measures analyst engagement with the intelligence layer | If low, add flagging as an explicit step in the post-research analyst checklist |
| Composite score distribution across signals | Tells us whether the scoring system is being applied or just all checked as high | Recalibrate scoring guidance if distribution is skewed; flag if most signals cluster at extreme scores |
| Signals per niche | Which niches keep surfacing as interesting | Strongest indicator of where independent research time should go |
| Signals progressed to Validated | Measures the funnel from observation to confirmed opportunity | If low relative to signals logged, the research step has a bottleneck |
| Validated signals actioned (into content / listings / gigs) | Measures conversion from intelligence to strategy | The terminal metric — the whole system exists to produce this |

These metrics are watched at quarterly intervals minimum. None of them are individually published; aggregated insights from them can inform public content per Section 11.

---

## 15. Future Database Implications

Not a software design. A list of what the future data model must support, so that whoever builds it knows the requirements up front.

| Future Entity | Purpose | Notes |
|---|---|---|
| Customer | Person paying for work; returning-customer recognition | Email is the natural unique identifier; minimize fields |
| Shop / Website | The unit of work; every report links here | Multiple shops per customer possible; one shop per report typical |
| Platform Account | Source channel + platform-side order tracking | Multiple platform accounts per customer possible (Fiverr now, direct later) |
| Order | Transactional record | Foreign keys to customer, shop, platform account |
| Report | Deliverable; metadata + file references | Foreign key to order; one report per order typical, but allow multiple (for bundles) |
| Audited Listing / Page | Snapshot at audit time | Foreign key to report; multiple per report; capture text content, reference URLs to media |
| Keyword Observation | Atomic keyword research unit | Foreign keys to report and niche; keyword text indexable for cross-client reuse; source + source date critical |
| Recommendation | Five-line recommendation block | Foreign keys to report, listing/page (optional), pattern tag (optional); priority enum |
| Action Plan Item | Subset of Recommendation tracked for outcome | Foreign keys to report and recommendation; status enum; outcome link |
| Outcome | Empirical layer | Foreign keys to action plan item; outcome label enum; confidence enum; consent flag |
| Revision / Support Note | Operational log | Foreign keys to order/report; summary text, not raw transcripts |
| Generalized Observation | The intelligence layer | No foreign keys to specific clients (by design); links to source observations counted, not retained as identifiers |
| Market Signal / Opportunity | Scored, researched opportunities flagged during paid work | **No client identifiers**; source field records engagement type, not client name; the signal exists independently of any one client; scores and research status evolve over time |
| Pattern Tag | Bridge entity between Recommendation and Generalized Observation | Many-to-many; allows abstracting a specific recommendation into a generalized pattern category |
| Niche | Categorisation for shops and keyword observations | Free-text descriptor + normalized cluster; allows cross-shop pattern aggregation |
| Consent Record | For testimonials, case studies, public examples | Foreign key to customer; specifies scope and revocability |
| Retention Schedule | Configurable retention policy applied automatically | Per data type; per Section 10 |
| Anonymization Status | Flag indicating whether a record has been anonymized for public use | Per record where applicable |

**Architectural notes for the future build:**

- **Client-specific data and generalized observations must be cleanly separable.** Either separate schemas, separate databases, or rigorously enforced access controls — but the boundary needs to be operationally real, not just notional.
- **Retention rules must be applied automatically.** Manual deletion will not happen on schedule. The database should know its own retention rules and act on them.
- **Consent records are mandatory before publication.** Building the consent record system before the public case study system is the correct order.
- **Pattern tags need to be a controlled vocabulary, not free-text.** A free-text "what kind of recommendation is this" field will drift into uselessness within months.
- **The customer's portal view (if we ever build one) shows the customer their own data — only.** No cross-customer visibility, no generalized layer exposed, no leakage between accounts.
- **Audit logs.** Internal access to client-specific data should be logged. Not for surveillance — for accountability if a customer ever asks "who saw my data".

This is enough specification to inform a future build. The current state is "spreadsheets and folders"; that's fine for the first 20–50 orders. Moving to a real database becomes important once volume exceeds what a single analyst can hold in their head.

---

## 16. Operational Workflow

The end-to-end workflow for a single paid order. Each step has what's stored, what's not, and what may become generalized learning.

```
Order received
    → intake stored
    → shop / listings recorded
    → research performed + opportunity signals flagged
    → observations captured
    → report written
    → recommendations saved
    → report delivered
    → follow-up / outcome recorded
    → generalized patterns extracted
    → opportunity signals scored and queued for research
```

| Step | Store | Do Not Store | Generalized Learning Opportunity |
|---|---|---|---|
| Order received | Order record (ID, customer, shop, report type, tier, dates, status) | Payment data; card details; billing address | Source channel statistics (Fiverr vs. direct over time); turnaround data |
| Intake stored | Intake answers per the report's defined intake (r04 Section 15.2); written confirmation that intake is complete | Anything we asked for that the customer chose not to provide; analytics credentials offered (refuse and don't store); any information volunteered that's outside scope | Common intake gaps (where do customers most often skip a field?); niche descriptors across many customers |
| Shop / listings recorded | Shop record; listing/page snapshots; captured titles, tags, descriptions, attributes | Photo files (URL references only); customer's customer data if accidentally visible; any private analytics view | Niche frequency; shop size distribution; listing structure patterns |
| Research performed | Keyword observations with full metadata (cluster, intent, source, date); data source snapshots; **Market Opportunity Signals flagged during research with scores** | Tool screenshots beyond what's referenced in the report; competitor screenshots (use anonymized pattern descriptions, not shop names) | Keyword cluster reuse; tool data drift over time; recurring competitive patterns; **opportunity signals across multiple engagements** |
| Observations captured | Pattern-tagged observations linking each finding to a generalized pattern (if applicable) | Raw notes that include identifying details about competitors or other clients | The pattern tags themselves — this is the bridge to generalized learning |
| Report written | The report file; the structured per-section content; analyst initials | Drafts beyond the final version (delete after delivery); side commentary that didn't make it into the report | Recurring report-section content patterns (informs template improvements) |
| Recommendations saved | Each recommendation as a structured entity (the five-line block); priority; target listing/page; pattern tag | Recommendations the analyst considered but rejected (unless they inform a follow-up) | Recommendation pattern frequency by report type and niche |
| Report delivered | Delivery date; delivery message used; delivery file references | The customer's emotional response to delivery if shared informally | Delivery message effectiveness (which templates produce positive follow-up signals) |
| Follow-up / outcome recorded | Outcome records linked to action plan items; confidence labels; implementation status; consent flag (default No) | Outcomes the customer didn't actually report (don't infer); private commentary the customer shared in confidence | Outcome label distribution per recommendation pattern — the core empirical learning |
| Generalized patterns extracted | Generalized observations (no client identifiers); pattern frequencies; cross-client trends | Anything that retains client-specific identifiability | This step is the generalized learning, by definition |

**One iron rule across all steps:** if a step's "Store" column contains something sensitive, the corresponding retention policy from Section 10 applies automatically. Storage is not the same as permanent retention.

---

## 17. Risks

The risks SearchClarity must actively manage. Severity is the realistic assessment for a small but reputation-dependent service business.

| Risk | Severity | Why It Matters | Mitigation |
|---|---|---|---|
| Privacy risk (data we shouldn't have, exposed) | High | Customer trust collapse; legal liability under GDPR/CCPA/etc. | Data minimization (Section 9); retention discipline (Section 10); access controls; refuse credentials proactively |
| Platform Terms of Service risk (Fiverr, Etsy) | High | Account termination ends the entire current sales channel | Verify TOS per platform at policy revision time; train on platform boundaries (Section 8); never push off-platform during active Fiverr orders |
| Client trust risk (perceived data misuse) | High | A client who believes we used their data against them will say so publicly | Section 7.4 firm line applied consistently; independent research (not client data) is the basis for acting on signals; client-specific data and generalized intelligence separated operationally |
| Competing-with-client reputation risk | Medium | If SearchClarity sells in any marketplace, perception of conflict is real regardless of actual behaviour | Section 7: we do not copy specific listings, titles, tags, photos, or designs; opportunity signals are triggered by observation, but validated and acted on using only public data |
| Overcollecting data (asking for things we don't need) | Medium | Erodes trust at intake; increases breach surface | Intake review per report type (per r04 Section 15.2); challenge any new intake field with "does the report use this?" |
| Storing sensitive data unnecessarily | Medium-High | Increases breach impact; creates legal exposure | Section 9 minimization list; analyst training |
| Weak anecdotal outcomes used as proof | High | Single-client outcome claims are misleading and create refund/trust risk | Section 13 rules; Section 11 case-study requirements; "no ranking promises / no sales promises" in every report (r04 Section 3.6) |
| Mixing private data with generalized insights | Critical | The whole intelligence layer's safety depends on this separation | Pattern tags (controlled vocabulary); generalized observation records have no client identifiers by design; access controls between layers |
| Data breach risk | High | Even minimal client data, if breached, is reputation-fatal | Encryption at rest where possible; access controls; minimal data retained per Section 9; audit logs; principle of least retention |
| Inaccurate historical snapshots | Medium | A snapshot of a listing taken three months ago may not match memory; analyst could make wrong inferences | Always store snapshots with capture date; always verify current state before basing returning-customer recommendations on prior snapshots |
| Stale recommendations | Medium | A recommendation that was correct six months ago may be wrong now (Etsy search shifts, Google algorithm changes, etc.) | Caveats in returning-customer reports about the age of prior findings; rerun current research before reusing prior conclusions |
| Analyst misuse of client data | Critical | A bad actor on the team is the highest-impact internal threat | Access controls; audit logs; team agreements that include client data handling; small-team trust + verification |
| Consent confusion (customer didn't realise something was public) | High | Even with consent, miscommunication about scope can break trust | Section 11 written consent requirements specify scope and revocability; consent records retained per Section 10 |
| Returning customer surprised by what we remember | Medium | "How do you know that?" is a question we should welcome, not dread | Transparency: customer can ask what we have on file; willingness to delete on request |
| Loss of intelligence layer through over-deletion | Low-Medium | Aggressive deletion of generalized observations would hurt the business without protecting any client | Generalized observations (no identifiers) retained indefinitely; client-specific data retention is what's bounded |

The two Critical risks are client trust and analyst misuse. Both are mitigated by the same things: clear policy, real boundaries, audit trails, and a small team that takes the boundaries seriously.

---

## 18. Final Recommendations

### What to store from day one

- **Customer** (name, email, source channel, communication preferences).
- **Shop / website** (URL, platform, niche descriptor, opened date, listing count at first contact).
- **Orders** with full transactional metadata.
- **Reports** delivered with file references, executive summary text, analyst/reviewer initials.
- **Listing / page snapshots** at audit time (text captures, URL references for media — not files).
- **Intake answers** for every report.
- **Keyword observations** with full metadata (cluster, intent, source, date, niche).
- **Recommendations** in full five-line block form, with pattern tags.
- **Action plan items** with priority and implementation status.
- **Outcomes** with confidence labels and consent flags (default No).
- **Revision / support notes** as summaries.
- **Market opportunity signals** flagged during research, with scores and research status — from day one, even in a single spreadsheet tab.
- **Generalized observations** (the intelligence layer; client-de-identified by design).
- **Consent records** for any public use.

This is the minimum for the intelligence layer to function. Start here on day one — even in spreadsheets.

### What not to store

Payment data; customer home addresses; phone numbers; Etsy buyer personal data; platform passwords / API keys; private analytics credentials; private revenue/profit data (except when Report 10 explicitly requires, and then only as rough split percentages with short retention); customer's customers' contact info; copyrighted client assets beyond what's referenced in reports; raw screenshots beyond 90 days unless directly referenced in a finding.

### Returning customer workflow

When a returning customer places a new order:

1. Pull all prior reports, intake, snapshots, recommendations, and outcomes for the shop.
2. Surface the action plan items from prior reports and check their implementation status against the live shop.
3. Note what's changed in the shop since the last snapshot — new listings, removed listings, changed titles/tags.
4. Frame the new report in continuity with the old: "Building on what we recommended in [prior report]…"
5. Avoid re-recommending items that are still in the prior report's action plan but unimplemented — instead, ask the customer whether they want help implementing them, or want the new report focused elsewhere.
6. Update the customer record with the new order.

The promise to a returning customer: **we remembered, and we built on it.**

### Generalized market learning workflow

For every report delivered:

1. Analyst tags each recommendation with the appropriate pattern tag from the controlled vocabulary.
2. Periodically (monthly, quarterly), the generalized observations layer is updated: pattern frequencies recalculated, new patterns proposed (require 5+ unrelated client observations before promotion to the layer), existing patterns reviewed.
3. Outcome data per pattern is reviewed: which patterns have positive signal, which have mixed, which have negative.
4. Template, methodology, and analyst training updated based on the generalized layer — not based on any single client's data.
5. Public content (blog posts, methodology pages, gig descriptions) draws on the generalized layer only, with the bar in Section 11 (10+ unrelated clients or 5+ plus public corroboration).

### Market opportunity use policy

Client work is the signal that points us toward research questions. Public market research is the basis for acting. The full system is in Section 7. The short version:

- Every analyst flags Market Opportunity Signals during paid research work — whenever a niche, cluster, or gap looks interesting.
- Every signal gets logged and scored across the 12-factor opportunity model (12×5-point scale, max 60).
- Signals scoring 36+ go into the research queue. Signals scoring 46+ get prioritized. Signals scoring 56+ are serious opportunities.
- Independent research uses public data only: eRank, Etsy search, Google Trends, Pinterest Trends, direct marketplace browsing.
- Validated opportunities feed SearchClarity strategy, content, gig positioning, and where applicable, our own listings.
- We do not copy a paying customer's specific listings, titles, tags, descriptions, photos, or designs. We do not use their private intake answers or outcome data as the basis for acting. The signal triggers the research; public data is what we act on.

### Consent / case study rules

- Fictional samples are the default; they handle consent by not having one.
- Anonymized real examples require the Section 11.1 anonymization checklist passed end-to-end.
- Named case studies, testimonials, and any use of real shop names require written consent specifying scope and revocability. Verbal consent is not enough.
- Consent is revocable; revoked consent triggers takedown within a reasonable window.
- Single-client outcomes never become public marketing claims. Aggregated outcomes only with high enough N (15+) and framed without implying predictability.

### Retention rules

The full table is in Section 10. The short version: orders 7 years (tax); reports and intake 3 years; outcomes 3 years with consent flag enforcement; keyword observations 5 years; raw screenshots 90 days; generalized observations indefinitely (because they're already de-identified); inactive customer contact info deleted after 24 months of no activity.

Automatic retention enforcement matters more than aspirational retention durations.

### Future data model priorities

The build priority order, when SearchClarity moves off spreadsheets:

1. Customer / Shop / Order / Report core (the spine).
2. Listing snapshots + Recommendations + Action Plan Items (the audit content).
3. Keyword Observations (the cross-client reuse layer).
4. Outcomes + Consent Records (the empirical layer with safety guardrails).
5. Pattern Tags as a controlled vocabulary (the bridge).
6. Generalized Observations + Market Signals (the intelligence layer, with strict separation).
7. Retention automation.
8. Audit logs.

Build in that order. Don't build the generalized layer before the recommendation layer; don't build outcomes before consent records; don't build any of it before retention automation if data is going to live longer than 90 days.

### Biggest risk

**Client trust collapse from perceived data misuse.** The risk is the *perception*, not just actual misuse. The mitigation is the entire policy framework in this document plus the discipline to apply it consistently. The day a paying customer concludes we used their data against them, the business loses something that cannot be recovered with an apology.

### Next practical step

Set up a minimal client history system this week, even if it's spreadsheets:

1. A customer sheet (name, email, shop URL, niche, first order date).
2. An order sheet (order ID, customer, report type, tier, dates).
3. A report sheet (report ID, order, filename, analyst, delivery date, executive summary in 3–4 lines).
4. An action plan sheet (item, report, priority, target listing, implementation status, outcome label, confidence).
5. A keyword sheet (keyword, cluster, intent, source, date, niche, source report).
6. A **market opportunity signals sheet** (signal ID, date, source engagement type, niche description, signal description, 12 score fields, composite score, research status, notes). This is the tab that turns paid work into strategy.
7. A generalized observations sheet (observation, supporting evidence count, status: emerging / confirmed / deprecated).
8. A consent records sheet (customer, scope, granted date, revocable Yes/No).

Use these from order #1. Refine as volume grows. Move to a real database once a single analyst can no longer hold the customer list in their head — somewhere around 20–50 customers depending on order frequency.

The discipline matters more than the tooling. A small business with seven spreadsheets used consistently is better off than a sophisticated database used carelessly.

---

**End of r05 — Client Report History + Market Learning Observatory.**
