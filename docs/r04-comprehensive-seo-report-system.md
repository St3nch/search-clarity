# r04 — Comprehensive SearchClarity SEO Report System

**Document purpose:** Defines the actual customer-facing reports SearchClarity delivers to paying customers across all planned SEO services. This is the working template structure — sections, tables, recommendation formats, intake rules, delivery messages, and quality control — not a strategy brainstorm.

**Audience:** Internal SearchClarity team (report production, QA, delivery).
**Status:** Working spec. Reports built from this document are the deliverables we hand to buyers.

---

## 1. Executive Summary

SearchClarity sells human-reviewed visibility reports. Every paid order produces a structured PDF (and, where relevant, a spreadsheet) that a real analyst has read end-to-end before delivery. The system must feel like a competent SEO analyst sat down with the buyer's shop, listings, or site and gave them a defensible plan — not a tag dump, not generic AI advice, not a pretty cover page wrapped around filler.

**What the report system should look like.** Ten reports, four of them foundational, the rest building outward from the Etsy core. Every report shares a universal framework (cover, scope, data sources, findings, analysis, recommendations, reasoning, action plan, caveats, next step). Each report uses the same recommendation block format and the same caveat language so the brand reads consistently across services and across analysts.

**Which reports are foundational.** Three: the Etsy Listing Visibility Audit (Report 1), the Etsy Keyword Research Pack (Report 3), and the Etsy Shop Visibility Report (Report 5). Every other Etsy-side report either feeds into or builds on these three.

**Which reports depend on another report.** The Title and Tag Rewrite (Report 2) is strongest when sold after a Listing Visibility Audit, because rewrites without diagnosis are guesswork. The Seller Visibility Strategy Report (Report 10) is a synthesis report — its quality is bounded by how many upstream reports the buyer already owns. The AI Search Readiness Audit (Report 9) and Schema Readiness Audit (Report 8) are strongest as a pair, because schema is one of the inputs into LLM visibility readiness.

**Which reports are standalone.** The Listing Visibility Audit (1), the Keyword Research Pack (3), the Shop Visibility Report (5), the Pinterest SEO Plan (6), the Shopify Product Page Audit (7), and the Schema Readiness Audit (8) can all be sold cold without prerequisites. The Competitor Visibility Observations (4) can also be standalone but reads better as a premium add-on.

**Which reports should be add-ons.** The Title and Tag Rewrite (2), the Competitor Visibility Observations (4), and early-stage Keyword Research Packs (3). Bundling these as upsells on the Audit raises average order value and avoids commoditising them as cheap Fiverr gigs.

**Which report should be built first.** Report 1, the Etsy Listing Visibility Audit. It is the highest-intent, highest-volume entry point on Etsy-focused marketplaces, it produces the template structure every other Etsy report inherits, and it is the natural anchor for a public mock sample.

**Which report should become the public mock sample.** Also Report 1. A fully filled-in Listing Visibility Audit using the fictional "Smells Like Retirement — Candle Gift" listing, published as a downloadable PDF on the SearchClarity site, doubles as a sales asset and as a quality benchmark for analysts.

**Biggest risk to report quality.** Drift toward AI-generated filler. The format encourages tables and section headings; an unsupervised analyst can fill those tables with vague rows and the report will *look* professional while saying nothing specific. The QC checklist in Section 17 exists specifically to catch this.

**Biggest risk to buyer trust.** Ranking and sales promises — explicit or implied. A single sentence like "this will get you to page one" or "expect a sales lift" turns the entire report into a refund risk. Every report must use the caveat block in 3.6 verbatim, and every recommendation must be phrased as a direction, not a guarantee.

---

## 2. Report Dependency Map

| # | Report | Can Be Standalone? | Depends On | Feeds Into | Best Role |
|---|---|---|---|---|---|
| 1 | Etsy Listing Visibility Audit | Yes | — | 2, 3, 4, 5, 10 | Flagship entry product; public mock sample |
| 2 | Etsy Title and Tag Rewrite | Yes, but weaker | 1 (recommended) | 5, 10 | Premium add-on to Audit; implementation deliverable |
| 3 | Etsy Keyword Research Pack | Yes | — | 1, 2, 4, 5, 6, 10 | Standalone research product; add-on to Audit |
| 4 | Etsy Competitor Visibility Observations | Yes | 3 (helpful) | 5, 10 | Premium add-on; standalone for established sellers |
| 5 | Etsy Shop Visibility Report | Yes | 1, 3 (recommended) | 6, 10 | Shop-level synthesis; mid-tier offer |
| 6 | Pinterest SEO Plan for Etsy Sellers | Yes | 3 (helpful) | 10 | Off-platform expansion product |
| 7 | Shopify Product Page SEO Audit | Yes | — | 8, 9, 10 | Entry product for owned-site sellers |
| 8 | Schema / Structured Data Readiness Audit | Yes | 7 (often) | 9, 10 | Technical readiness add-on |
| 9 | AI Search / LLM Visibility Readiness Audit | Yes | 7, 8 (recommended) | 10 | Premium readiness audit; differentiator |
| 10 | Seller Visibility Strategy Report | Yes, but thin | Any of 1–9 | — | Premium strategy synthesis |

### Ideal customer journey

**Etsy-only seller path.**
Listing Visibility Audit (1) → Title and Tag Rewrite (2) → Keyword Research Pack (3) → Competitor Visibility Observations (4) → Shop Visibility Report (5).

This is the core funnel. A buyer who completes this sequence has a diagnosis, an implementation, a research foundation, market context, and a shop-level synthesis.

**Multi-channel seller path (continues from above).**
Shop Visibility Report (5) → Pinterest SEO Plan (6) → Shopify Product Page Audit (7) → Schema Readiness Audit (8) → AI Search Readiness Audit (9) → Seller Visibility Strategy Report (10).

This is the expansion path for sellers who run an Etsy shop *plus* a Shopify store or other owned site. It builds outward from Etsy SEO into off-platform discovery, technical readiness, and finally a synthesis strategy.

**Practical reality.** Most buyers will start with one report. The dependency map is the map we follow when *recommending the next step* in delivery messages, not a forced sequence. Sections 16 (delivery messages) and 18 (final recommendations) reinforce this.

---

## 3. Universal Report Framework

Every SearchClarity report uses this framework. The wording in 3.1, 3.3, and 3.6 is reusable verbatim across reports.

### 3.1 Cover Page

```
SearchClarity

[Service Name]

Prepared for:   [Shop / Brand Name]
URL:            [Shop / Website URL]
Date:           [Date]
Prepared by:    SearchClarity

Human-reviewed visibility recommendations.
Evidence-based. No fake ranking promises.
```

The positioning line is mandatory. It sits directly under the prepared-by line on the cover. It is the single most important brand differentiator on the page.

### 3.2 Scope Section

Every report opens (after the cover) with a Scope section. Reusable structure:

> **Scope of this report**
>
> This report reviewed:
> - [Number] [listings / pages / keywords / boards / etc.]
> - [Specific URLs, search terms, or shop areas covered]
>
> This report did not review:
> - [Items explicitly out of scope: photography, pricing, product development, paid ads, fulfillment, returns policy, customer service messaging, etc., as relevant]
>
> Tools and sources used:
> - [List per Section 3.3]
>
> Limitations:
> - [Specific to the report: e.g., marketplace search data is estimated; the report reflects a snapshot in time; AI search results vary by session.]

Scope is non-negotiable. A buyer who reads the scope before complaining about something missing has been told upfront what they got.

### 3.3 Data Source Disclosure

Reusable block. Appears in every report immediately after Scope:

> **About the data in this report**
>
> SearchClarity uses a combination of manual review, marketplace search observation, and third-party SEO tools. Tool data (search volume, competition scores, trend curves) is estimated, not measured. Marketplace and search algorithms change continuously, so observations reflect a specific point in time.
>
> No data source — including ours — can guarantee rankings, traffic, or sales. Recommendations in this report are direction-setting, not outcome-guaranteeing. The buyer is responsible for testing, measuring, and iterating on the changes they implement.

### 3.4 Recommendation Format

Every individual recommendation in every report uses this five-line block. Analysts do not freestyle.

```
Observation:    [What was found, in concrete terms with evidence.]
Why it matters: [Why this affects visibility, discoverability, or buyer intent.]
Recommendation: [Specific direction the seller should take.]
How to implement: [Practical steps the seller can act on today.]
Caveat:         [What could prevent this from working, or what to avoid.]
```

The "How to implement" line is the difference between a real audit and a Fiverr tag dump. If an analyst cannot write a usable implementation step, the recommendation is not ready to ship.

### 3.5 Action Plan Format

Every report ends with an Action Plan table:

| Priority | Action | Why It Matters | Where To Apply | Suggested Timing |
|---|---|---|---|---|
| Do first | [Specific action] | [Reason] | [Listing/page/board] | [Within 7 days, etc.] |
| Do next | … | … | … | … |
| Test later | … | … | … | … |
| Avoid | [What not to do, e.g., adding trademark-risky terms] | [Reason] | — | — |

The four priority labels are fixed: **Do first**, **Do next**, **Test later**, **Avoid**. Analysts must include at least one row in each of the first three; the Avoid row is included whenever the report identifies a risk pattern.

### 3.6 Caveat Block

Reusable verbatim. Appears immediately before the Next Steps section of every report:

> **Caveats and limits of this report**
>
> SearchClarity does not guarantee rankings, search placement, traffic, clicks, or sales. SEO and marketplace visibility are influenced by factors outside our scope — including product-market fit, photography quality, pricing, review history, shipping options, demand seasonality, and platform algorithm changes. SEO cannot fix weak product-market fit, poor photos, poor pricing, bad reviews, or low underlying demand.
>
> Search and marketplace algorithms change without notice. Recommendations in this report reflect current best-understanding patterns; they should be tested over time and revised based on results.
>
> The buyer is responsible for final implementation, for verifying that any keyword or claim is appropriate for their products, and for ensuring all listing language complies with marketplace policy, trademark law, and applicable advertising regulations.
>
> Specifically:
> - Avoid keyword stuffing — it harms readability and can violate marketplace policy.
> - Avoid trademark- or IP-risky terms (brand names, character names, protected slogans) unless the seller holds appropriate rights.
> - Avoid copying competitor titles, tags, descriptions, photos, or branding.

---

## 4. Report 1 — Etsy Listing Visibility Audit

**Buyer problem:** "My Etsy listings are live, but they are not getting found. I do not know what to fix first."

This is the flagship report and the first public mock sample.

### 4.1 When To Sell This Report

Sell to sellers who:

- Have 5+ active Etsy listings.
- Have been live at least 30 days (long enough for some search exposure).
- Report low impressions, low visits, or low conversion despite finished listings.
- Are unsure whether the problem is titles, tags, descriptions, photos, or demand.

Do not sell to sellers who have fewer than 3 active listings (not enough material to audit), or who explicitly want copywriting only (route them to the Title and Tag Rewrite).

### 4.2 What This Report Should Prove

After reading, the buyer should be able to answer:

- Which of my listings are the weakest from a visibility standpoint, and why.
- Are my titles structured for Etsy search, or for human reading first.
- Are my tags covering the buyer-intent angles people actually search.
- Are my descriptions giving Etsy enough signal to categorize me.
- What should I fix this week, this month, and what should I leave alone.
- What patterns am I repeating across listings that may be hurting all of them at once.

### 4.3 Buyer Inputs Needed

1. Etsy shop URL.
2. URLs of up to [N] listings to be audited (package-dependent — see Section 14).
3. Primary product category / niche in the seller's own words.
4. Who they think the buyer is (gift buyer, hobbyist, professional, etc.).
5. Anything they have already tried (recent title changes, tag changes, photo updates).
6. Whether the shop is on Etsy Plus or has access to Etsy Marketplace Insights.
7. Optional: any specific listings they suspect are underperforming.
8. Optional: any keywords they have already targeted.

### 4.4 Data / Tools Used

- Manual review of every audited listing (title, tags, description, attributes, category, photos as signal — not as critique).
- Etsy on-platform search observation for the seller's primary keywords.
- Etsy Marketplace Insights, if the seller has access and provides screenshots.
- eRank or comparable marketplace SEO tool for keyword coverage estimates.
- Google Trends for seasonality cross-checks where relevant.
- Pinterest Trends, only when the niche has clear visual-discovery overlap.
- Seller-provided context from intake.

All tool data is labelled "estimated" in the report itself. See 3.3.

### 4.5 Report Table of Contents

1. Cover Page
2. Scope
3. Data Sources Used
4. Executive Summary
5. Listing Diagnosis Overview
6. Per-Listing Findings (one section per audited listing)
7. Title Structure Analysis
8. Tag Coverage Analysis
9. Description and Attribute Analysis
10. Keyword Opportunity Findings
11. Cross-Listing Patterns
12. Priority Action Plan
13. Caveats
14. Next Steps

### 4.6 Required Tables

**Listing Diagnosis Table** — appears in section 5.

| Listing | Current Issue | Visibility Impact | Priority | Recommended Fix |
|---|---|---|---|---|
| [Listing title or short ID] | [Specific issue] | [High / Medium / Low] | [Do first / Do next / Test later] | [One-line direction] |

**Title Structure Table** — appears in section 7.

| Listing | Current Title | Main Problem | Recommended Title Direction | Reason |
|---|---|---|---|---|
| | | | | |

**Tag Coverage Table** — appears in section 8.

| Listing | Current Tag Pattern | Missing Keyword Angles | Recommended Tag Direction |
|---|---|---|---|
| | | | |

**Keyword Opportunity Table** — appears in section 10.

| Keyword / Phrase | Buyer Intent | Estimated Demand | Competition Note | Recommended Use | Source |
|---|---|---|---|---|---|
| | | [Low / Medium / High, est.] | | [Title / Tag / Description] | [eRank / Etsy search / Google Trends] |

**Priority Action Plan** — appears in section 12.

| Priority | Action | Listing(s) | Why It Matters | Timing |
|---|---|---|---|---|
| Do first | | | | |
| Do next | | | | |
| Test later | | | | |
| Avoid | | | | |

### 4.7 Example Filled-In Section

The following is the per-listing finding template, filled in with fictional data. This same example becomes the public mock sample.

---

> **Listing 3 of 12 — "Smells Like Retirement — Candle Gift"**
>
> **Current title:** Smells Like Retirement Candle Funny Retirement Gift for Coworker Retirement Party Decor Gag Gift
>
> **Diagnosis**
>
> The title leads with a strong product-fit phrase ("Smells Like Retirement Candle") but loses search weight in the back half through repetition of the word "retirement" four times and the inclusion of low-intent terms ("Decor", "Gag Gift") that compete with stronger buyer-intent phrases the title is not yet using.
>
> **Title issue**
>
> Observation: The phrase "Retirement Gift for Coworker" is the strongest buyer-intent phrase in this title, but it appears in position 5–7, after weaker terms. Etsy's search weighting favours earlier title positions.
> Why it matters: Buyers searching "retirement gift for coworker" are higher-intent than those searching "gag gift". The current title is positioned for the lower-intent search.
> Recommendation: Move the highest-intent gift phrase forward; remove one repetition of "retirement"; replace "Decor" with a recipient-specific term.
> How to implement: Rewrite in the direction of: `Funny Retirement Candle for Coworker — Office Retirement Gift, Gag Gift Idea for Boss or Colleague`. This keeps the funny/gag positioning but leads with the buyer-intent phrase.
> Caveat: This is a direction, not the final wording. Test for 14–21 days before iterating. Do not add "Yankee Candle", "Bath & Body Works", or other brand names as keyword bait — that is a trademark risk.
>
> **Tag issue**
>
> Observation: Current tags appear to be: `retirement gift, funny candle, gag gift, retirement party, coworker gift, office gift, retirement decor, candle gift, funny gift, retirement, candle, gift idea, retire`.
> Why it matters: Several tags are single words ("retirement", "candle", "retire") which compete against millions of listings. The 13-tag slot is being spent on broad terms instead of buyer-intent long-tail phrases.
> Recommendation: Replace 4–6 of the single-word and broad tags with longer buyer-intent phrases.
> How to implement: Direction for tag replacements — drop `retirement`, `candle`, `retire`, `gift idea`. Test in the direction of: `retirement gift coworker`, `funny retirement candle`, `boss retirement gift`, `office retirement gift`, `last day work gift`, `retiring teacher gift` (only if relevant to product).
> Caveat: Do not duplicate the same tag set across every listing in the shop — Etsy can interpret this as low-signal. Tag intent should match each listing's specific angle.
>
> **Description issue**
>
> Observation: The first 160 characters of the description (the portion visible without expanding) repeat the title almost verbatim and do not introduce any new keyword angles or buyer-context language.
> Why it matters: The first 160 characters carry weight in marketplace search and in off-platform discovery (Google snippet, Pinterest pin). Repeating the title wastes this real estate.
> Recommendation: Use the first 160 characters to introduce buyer-context phrases the title cannot fit.
> How to implement: Open the description with a sentence in the direction of: `A funny retirement candle for a coworker leaving the office — a lighthearted last-day gift idea for the colleague, boss, teacher, or nurse who's finally calling it a career.` This introduces 3–4 recipient angles without keyword stuffing.
> Caveat: Do not pack the opening with comma-separated keywords. Etsy and Google both downrank descriptions that read as keyword lists.
>
> **Recommended tag angles (for analyst reference, not as a delivered tag list)**
>
> - Recipient angles: coworker, boss, colleague, teacher, nurse, dad, mom
> - Occasion angles: last day, retirement party, going-away
> - Intent angles: funny, gag, lighthearted
> - Specificity angles: office, work, career
>
> **Reasoning**
>
> The current listing is structured as a single-message listing ("funny retirement candle") but the buyer demand splits across recipient and occasion. Without recipient-specific terms in the title or tags, the listing competes only on broad terms where it is buried. Adding recipient and occasion specificity opens 4–6 additional search paths into the same product without changing the product itself.
>
> **Caveat**
>
> Any recipient term used in the title or tags must accurately describe a buyer the listing actually serves. Do not add "nurse retirement gift" to the title if the candle's design or messaging is not appropriate for that recipient. Mismatched listings get clicked but not bought, which hurts the listing's conversion signal and therefore its search position.
>
> **Action step**
>
> Within 7 days: rewrite the title in the direction above; replace 4 tags as listed; rewrite the first 160 characters of the description. Hold all other changes for 21 days to measure the effect of these three changes in isolation.

---

### 4.8 What To Avoid

A Listing Visibility Audit fails when it:

- Lists tags without explaining intent or angle.
- Uses single-word recommendations like "fix title" without a direction.
- Includes fake search volume numbers presented as fact (always label "estimated" with source).
- Mentions ranking positions or sales predictions.
- Suggests trademark-risky terms (brand names, character names, protected slogans).
- Recommends copying a specific competitor's title or tag set.
- Pads sections with generic SEO advice ("write good titles", "use keywords") instead of listing-specific findings.
- Avoids the "How to implement" line in the recommendation block.
- Skips the cross-listing patterns section — the buyer paid for shop-wide observation, not just isolated finds.
- Delivers without a Priority Action Plan the buyer can act on within 7 days.

---

## 5. Report 2 — Etsy Title and Tag Rewrite

**Buyer problem:** "I want implementation-ready Etsy titles and tags, not just an audit."

### 5.1 When To Sell This Report

Sell to sellers who:

- Have already received a Listing Visibility Audit (ideal).
- Or have done their own diagnosis and now want clean, ready-to-paste rewrites.
- Have a stable product line — rewrites for listings that are about to be discontinued or redesigned are wasted work.

This report is implementation, not diagnosis. Buyers who do not know what is wrong with their listings should be steered to the Audit first.

### 5.2 Relationship To Listing Visibility Audit

When sold after an Audit, the Rewrite uses the Audit's findings as its source of truth. The analyst does not re-diagnose; they execute. This makes the work faster and the recommendations more defensible (every rewrite traces back to a documented Audit finding).

When sold standalone, the analyst performs a lightweight diagnosis pass — sufficient to justify each rewrite, but not as deep as a full Audit. The cover page and scope must make this distinction visible to the buyer so they understand what they are and are not buying.

### 5.3 Buyer Inputs Needed

1. Etsy shop URL.
2. URLs of listings to be rewritten (package-dependent).
3. Target buyer in one sentence (for context, not strategy).
4. Any keywords the seller knows convert for them.
5. Any words or phrases the seller wants to keep in the title (brand voice, signature phrases).
6. Any words or phrases the seller does *not* want used.
7. If sold after an Audit: confirmation that the Audit findings still apply (no major listing changes since).
8. Optional: target geography if relevant (e.g., UK spelling for UK sellers).

### 5.4 Report / Deliverable Sections

1. Cover Page
2. Scope
3. Rewrite Summary
4. Listing Rewrite Table
5. Title Rationale Notes
6. Tag Rationale Notes
7. Optional Description Opening Rewrite
8. Implementation Notes
9. Caveats

### 5.5 Required Rewrite Table

| Listing | Current Title | Recommended Title | Why This Change | Recommended Tags | Tag Strategy Notes |
|---|---|---|---|---|---|
| | | | | [13 tags] | [Intent mix, e.g., 4 recipient / 3 occasion / 3 intent / 3 long-tail] |

The table is the centerpiece of the deliverable. Every other section supports it.

### 5.6 Tag Rules

Buyer-facing rules, included verbatim in the Implementation Notes section:

> **SearchClarity tag rules**
>
> - No irrelevant tags. Every tag must describe an aspect a buyer might search for in relation to this specific listing.
> - No trademark-risky tags. Brand names (e.g., specific candle brands, character names, sports team names) are excluded unless the seller holds the appropriate rights or licensing.
> - No keyword stuffing. Tags do not stack words at random; each tag is a coherent search phrase.
> - No identical tag sets across every listing. Each listing's tag mix is tuned to its specific angle. Repeating the same 13 tags across 50 listings sends a low-signal pattern to Etsy.
> - Balance broad, mid-tail, and long-tail terms. A working tag set typically mixes 2–3 broad (high competition, high volume), 4–6 mid-tail (moderate competition, moderate volume), and 4–6 long-tail (low competition, specific intent) phrases.
> - Match buyer intent. A tag's job is to match what a buyer types into search, not what the seller wishes they would type.

### 5.7 Example Filled-In Rewrites

**Example A — Funny retirement candle**

- Old title: `Smells Like Retirement Candle Funny Retirement Gift for Coworker Retirement Party Decor Gag Gift`
- New title: `Funny Retirement Candle for Coworker — Office Retirement Gift, Gag Gift Idea for Boss or Colleague`
- Why: Moves the highest-intent phrase ("Retirement Gift for Coworker") earlier; removes one repetition of "retirement"; replaces low-intent "Decor" with recipient-specific terms ("Boss or Colleague").
- 13 suggested tags: `funny retirement candle`, `retirement gift coworker`, `office retirement gift`, `boss retirement gift`, `colleague retirement gift`, `gag gift retirement`, `last day work gift`, `retirement party gift`, `funny coworker gift`, `going away gift`, `retirement candle`, `office gag gift`, `retiring coworker`
- Tag strategy note: 3 recipient (coworker, boss, colleague) / 3 occasion (last day, retirement party, going away) / 3 intent (funny, gag) / 4 long-tail composite. No single-word tags.
- Caveat: This rewrite assumes the candle's design and packaging are appropriate for any of the recipients listed. If the candle's design specifically targets one recipient (e.g., visibly office-themed but not boss-appropriate), narrow the tag set accordingly to protect conversion signal.

**Example B — Personalized teacher mug**

- Old title: `Personalized Teacher Mug Custom Name Teacher Gift Coffee Mug for Teacher Appreciation`
- New title: `Personalized Teacher Mug with Name — Teacher Appreciation Gift, Custom Coffee Mug for End of Year`
- Why: Adds the "with Name" specificity early (matches how buyers search for personalized gifts); adds "End of Year" as a high-seasonality occasion term; removes the redundant second "Teacher".
- 13 suggested tags: `personalized teacher mug`, `teacher appreciation gift`, `custom teacher mug`, `end of year teacher gift`, `teacher name mug`, `teacher coffee mug`, `gift for teacher`, `personalized coffee mug`, `teacher thank you gift`, `last day school gift`, `custom name mug`, `teacher gift idea`, `appreciation week gift`
- Tag strategy note: 3 product-specific (personalized teacher mug, custom teacher mug, teacher coffee mug) / 4 occasion (end of year, last day school, appreciation week, thank you) / 3 recipient (teacher gift, gift for teacher, teacher name mug) / 3 long-tail composite.
- Caveat: "End of year" demand peaks May–June in the US, April–July in the UK; the seller should expect this term to drive limited traffic outside those windows.

### 5.8 What To Avoid

A Title and Tag Rewrite fails when it:

- Reads like a Fiverr "13 tags for $5" gig with no rationale.
- Delivers tags without explaining the intent mix.
- Recommends identical tag sets across all the seller's listings.
- Includes brand names, character names, or copyrighted phrases.
- Recommends titles that exceed Etsy's character limit (140 at time of writing).
- Uses keyword strings instead of readable titles (e.g., `Retirement Candle Coworker Gift Boss Office Funny Gag`).
- Skips the "Why this change" column — the buyer must be able to defend the change to themselves.
- Avoids the implementation notes section — buyers need to know what to test, when, and for how long.

---

## 6. Report 3 — Etsy Keyword Research Pack

**Buyer problem:** "I do not know what buyers are actually searching for, and I do not want random tags."

### 6.1 When To Sell This Report

Sell to sellers who:

- Are planning new listings or a new product line and want to research demand first.
- Have completed an Audit and want a deeper keyword foundation.
- Are entering a new niche or expanding an existing one.

Sell as an add-on first (bundled with the Audit at a higher tier). Promote as standalone once the brand has enough reputation to anchor a research-only purchase.

### 6.2 Relationship To Listing Audit and Rewrite

The Keyword Research Pack supplies the raw research material the Audit and Rewrite both lean on. An Audit identifies that a listing is missing recipient-intent terms; a Rewrite implements specific ones; a Keyword Research Pack gives the seller the full library of recipient-intent terms to choose from over time.

Sold together as a bundle, the three reports form a complete loop: research → diagnosis → implementation.

### 6.3 Buyer Inputs Needed

1. Etsy shop URL (or planned shop concept if pre-launch).
2. The product type or niche to research.
3. The target buyer in one sentence.
4. Any seed keywords the seller already uses.
5. Any sub-niches or angles to include or exclude.
6. Geography focus, if relevant.
7. Seasonality preferences (year-round vs. occasion-driven).
8. Optional: competitor shop URLs as research starting points (used for pattern observation, not copying).

### 6.4 PDF Report Sections

1. Cover Page
2. Scope
3. Keyword Research Summary
4. Keyword Cluster Overview
5. Buyer Intent Groups
6. Recommended Keyword Uses
7. Keywords to Avoid
8. Seasonal Notes
9. Caveats
10. Next Steps

The PDF is the readable narrative. The spreadsheet (6.5) is the working tool.

### 6.5 Spreadsheet Structure

Delivered as `.xlsx` and `.csv`. Single sheet, sortable by every column.

| Keyword | Cluster | Buyer Intent | Product Fit | Estimated Demand | Competition Note | Seasonality | Recommended Use | Confidence | Source | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| | [from 6.6] | [Browsing / Comparing / Ready to buy] | [Strong / Moderate / Weak] | [Low / Medium / High, est.] | [Crowded / Moderate / Open, est.] | [Year-round / Q4 peak / etc.] | [Title / Tag / Description / Pin / Avoid] | [High / Medium / Low] | [eRank / Etsy search / Trends] | |

Every row's "Estimated Demand" and "Competition Note" carry the word "estimated" so the buyer cannot mistake third-party tool numbers for measured truth.

### 6.6 Keyword Cluster System

Every keyword is tagged into one of nine clusters. This is what makes the deliverable usable instead of a dump.

1. **Product type** — what the item is (`personalized mug`, `engraved cutting board`).
2. **Recipient** — who it is for (`teacher`, `nurse`, `dad`, `coworker`, `boss`).
3. **Occasion** — when it is bought (`retirement`, `wedding`, `graduation`, `christmas`, `mother's day`).
4. **Personalization** — what is customized (`custom name`, `engraved date`, `monogram`).
5. **Seasonal** — time-bound demand patterns (`spring`, `back to school`, `holiday`).
6. **Style / material** — descriptors (`minimalist`, `farmhouse`, `wood`, `ceramic`).
7. **Buyer problem** — what the buyer is trying to solve (`last minute gift`, `meaningful gift`, `unique gift`).
8. **Gift intent** — the gifting frame (`thank you gift`, `appreciation gift`, `memorial gift`).
9. **Avoid list** — terms that surfaced in research but should not be used (trademark risk, low relevance, banned by marketplace policy, misleading).

The Avoid list is itself a deliverable. Sellers value being told what *not* to chase as much as what to chase.

### 6.7 Example Filled-In Keyword Table

Fictional rows, niche: personalized retirement gifts. All demand and competition values are estimated and labelled as such.

| Keyword | Cluster | Buyer Intent | Product Fit | Estimated Demand | Competition Note | Seasonality | Recommended Use | Confidence | Source | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| retirement gift coworker | Recipient | Ready to buy | Strong | Medium (est.) | Crowded (est.) | Year-round | Title + Tag | High | eRank | Highest converting recipient-intent in cluster |
| funny retirement candle | Product type | Comparing | Strong | Low–Medium (est.) | Moderate (est.) | Year-round | Title + Tag | Medium | eRank | Niche-specific, low competition |
| personalized retirement plaque | Personalization | Ready to buy | Moderate | Low (est.) | Open (est.) | Year-round | Title + Tag | Medium | Etsy search | Underserved — verify product fit |
| boss retirement gift | Recipient | Ready to buy | Strong | Medium (est.) | Crowded (est.) | Year-round | Title + Tag | High | eRank | Pairs with coworker term |
| nurse retirement gift | Recipient | Ready to buy | Strong | Low–Medium (est.) | Moderate (est.) | Year-round | Title + Tag | Medium | eRank | Only use if listing genuinely fits nurse recipient |
| retirement party decorations | Occasion | Browsing | Weak | Medium (est.) | Crowded (est.) | Year-round | Avoid | Medium | Etsy search | Wrong product category — decorations, not gifts |
| last day at work gift | Buyer problem | Ready to buy | Strong | Low (est.) | Open (est.) | Year-round | Tag + Description | Medium | Etsy search | Long-tail entry — low volume, high intent |
| teacher retirement gift personalized | Recipient + Personalization | Ready to buy | Strong | Low (est.) | Open (est.) | Q2 peak (May–June US) | Title + Tag | Medium | Trends | Seasonal — plan listing pushes for spring |
| retirement gift for dad | Recipient | Ready to buy | Moderate | Medium (est.) | Crowded (est.) | Year-round | Title + Tag | High | eRank | Family recipient — high-volume |
| retirement gag gift | Gift intent | Comparing | Strong | Medium (est.) | Moderate (est.) | Year-round | Title + Tag | High | eRank | Pairs naturally with "funny" cluster |
| meaningful retirement gift | Buyer problem | Comparing | Moderate | Low (est.) | Open (est.) | Year-round | Description | Low | Etsy search | Use as description language, not title bait |
| Hallmark retirement card | Cluster: Avoid | — | — | — | — | — | Avoid | — | — | Trademark — do not use |
| 2026 retirement gift | Personalization (year) | Ready to buy | Strong | Low (est.) | Open (est.) | Year-bound | Title + Tag (rotating) | Medium | Trends | Update annually; high specificity drives conversion |

### 6.8 What To Avoid

A Keyword Research Pack fails when it:

- Delivers as a flat keyword list with no clustering, no intent labels, and no usage guidance.
- Presents tool data as measured fact instead of estimated.
- Omits the Avoid list — buyers value being told what not to chase.
- Recommends trademark-risky or marketplace-banned terms.
- Suggests using every keyword in every listing (defeats clustering).
- Skips seasonality on terms that are clearly seasonal.
- Uses generic "high / medium / low" without any source attribution.
- Pads the deliverable with hundreds of low-relevance keywords to inflate the row count.

---

## 7. Report 4 — Etsy Competitor Visibility Observations / Report

**Buyer problem:** "My competitors are showing up better than I am, but I do not know what they are doing differently."

### 7.1 When To Sell This Report

Sell as a **premium audit section first** (a chapter inside a higher-tier Audit), and as a **standalone report later** once SearchClarity has the reputation and intake flow to support it.

Standalone is appropriate for sellers who:

- Have at least 90 days of Etsy history.
- Are established enough that broad keyword research won't suffice — they need to understand why specific listings outrank theirs.
- Understand they will receive pattern analysis, not copy-paste plans.

Do not sell to sellers who explicitly want "tell me what my competitors do so I can do it too" — refund risk and IP risk are both high. Section 7.6 exists to head this off.

### 7.2 Relationship To Listing Audit and Keyword Research

The Competitor Visibility Observations is the natural follow-on once a seller has an Audit and a Keyword Research Pack. The Audit identifies what's wrong on the seller's side; the Keyword Research Pack provides the demand context; the Competitor Observations explains what visible patterns appear in the top results for those same keywords, and where the seller's positioning genuinely differs.

### 7.3 Buyer Inputs Needed

1. Etsy shop URL.
2. The 5–10 keywords or search terms the seller most wants to be found for.
3. The seller's own listings competing for those terms.
4. Optional: up to 3 specific competitor shops the seller has noticed outranking them (used as starting points for observation, not as named targets in the report unless there is a clear reason).
5. The seller's positioning in one sentence — what makes their product different.
6. Any product categories or sub-niches to exclude from observation.

### 7.4 Report Sections

1. Cover Page
2. Scope
3. Competitor Observation Method
4. Search Terms Observed
5. Competitor Pattern Summary
6. Title Pattern Analysis
7. Keyword Theme Analysis
8. Listing Trust Signal Observations
9. Opportunity Gaps
10. Recommended Response Strategy
11. Ethical Use Note
12. Caveats

### 7.5 Required Tables

**Search Observation Table** — section 4.

| Search Term | What We Observed | Pattern | Opportunity |
|---|---|---|---|
| | [Top results were predominantly X type of listing with Y price band and Z recipient framing] | [Recurring pattern] | [Gap or angle worth testing] |

**Competitor Pattern Table** — section 5.

| Pattern | Seen In Top Listings? | Why It Matters | How You Can Respond |
|---|---|---|---|
| | [Yes — 7 of top 10 / No / Mixed] | | [Direction, not copy] |

**Opportunity Gap Table** — section 9.

| Gap | Your Current Position | Market Pattern | Recommended Response |
|---|---|---|---|
| | | | |

### 7.6 Ethical Language

Reusable verbatim in section 11 of the report:

> **Ethical use of this report**
>
> This report identifies visible marketplace patterns. It does not recommend copying competitor titles, tags, photos, branding, designs, descriptions, or any protected language. Patterns described here reflect aggregate observations across multiple top-ranking listings — not instructions to replicate any individual shop's work.
>
> Copying another seller's listing copy, photography, or design risks marketplace policy violations, intellectual property claims, and reputational damage. Where this report identifies a pattern (for example, "top-ranking listings in this search emphasise recipient specificity"), the recommended response is to apply that pattern to the seller's own product in the seller's own voice — not to mirror any specific competitor's execution.

This block must appear in every Competitor Visibility report. It is not optional and not editable.

### 7.7 Example Filled-In Competitor Observation

Fictional example using visible pattern analysis only. No named shops.

---

> **Search term observed: `personalized retirement gift for coworker`**
>
> **What we observed**
>
> Reviewing the first three pages of Etsy results for this term, top-ranking listings shared several visible patterns:
>
> - 8 of the top 15 results included the buyer's recipient ("coworker") in the first 40 characters of the title.
> - 9 of the top 15 led the title with the personalization angle ("Personalized", "Custom", "Engraved") rather than the product type.
> - The product mix skewed toward functional items (mugs, tumblers, plaques, pens) over decorative items (candles, ornaments) at roughly 11:4 in the top 15.
> - Price points clustered in the $18–$35 band; listings priced under $15 or over $50 were rare in the top 15.
> - Mockup style leaned heavily on lifestyle photography (the item in a workplace or gifting context) rather than isolated product shots.
>
> **Pattern: personalization-first titles**
>
> Observation: 9 of 15 top results lead with "Personalized" or a synonym. The seller's current listing leads with the product type.
> Why it matters: Etsy's search appears to weight the buyer-intent modifier when the search query itself contains it ("personalized" in the search term).
> Recommendation: Restructure the title to lead with the personalization angle, then product type, then recipient.
> How to implement: Test a title in the direction of `Personalized Retirement Gift for Coworker — Custom [Product Type] with Name`. Do not copy any specific competitor's title verbatim or near-verbatim.
> Caveat: Personalization-first only works if the listing actually offers personalization. Do not lead with the term if personalization is upsell-only.
>
> **Pattern: functional product skew**
>
> Observation: Decorative items (candles, ornaments) are present in this search but underrepresented in the top results.
> Why it matters: This may reflect a buyer-intent mismatch — buyers searching "personalized retirement gift for coworker" may convert more readily on functional items, which makes Etsy's search learn to rank them higher.
> Recommendation: For decorative products competing in this search, consider whether to invest in this specific keyword or pivot toward keywords where decorative products dominate the top results (e.g., "retirement party decor", though buyer intent there is lower).
> How to implement: Run the seller's current decorative listing for 21 days with the personalization-first title pattern. If impressions improve but conversion does not, the buyer-intent mismatch is the likely cause, and the seller should redirect keyword focus.
> Caveat: This is a hypothesis based on visible patterns. It cannot be confirmed without listing-level conversion data.
>
> **Opportunity gap: occasion + personalization combinations**
>
> Most top results targeted recipient + personalization. Fewer combined recipient + occasion + personalization (e.g., "Personalized 2026 Retirement Gift for Coworker"). This three-way combination appeared in only 2 of the top 15 — suggesting a possible underserved long-tail opportunity for sellers willing to refresh listings annually with year-specific terms.

---

### 7.8 What To Avoid

A Competitor Visibility report fails when it:

- Names specific competitor shops as targets without clear justification.
- Recommends copying competitor titles, tags, descriptions, photos, or designs in any form.
- Suggests trademark- or IP-risky positioning ("use 'Yankee Candle alternative' in your title").
- Presents observed patterns as universal truths instead of snapshots in time.
- Confuses correlation with causation ("they rank because they used the word X").
- Skips the Ethical Use Note in section 11.
- Delivers as a list of competitor shop URLs with notes — that is intelligence, not analysis, and exposes both SearchClarity and the buyer to platform risk.
- Inflates the report with screenshots of competitor listings.

---

## 8. Report 5 — Etsy Shop Visibility Report

**Buyer problem:** "My whole shop feels unfocused, not just one listing."

### 8.1 When To Sell This Report

Sell to sellers who:

- Have 15+ active listings (enough material for shop-level patterns to be meaningful).
- Have already addressed individual listing issues and are now thinking shop-wide.
- Suspect their shop's overall niche or theme is hurting visibility.
- Are preparing to scale to a larger catalog and want a foundation review first.

This is a mid-tier offer in the SearchClarity range — broader than an Audit, narrower than the Seller Visibility Strategy Report.

### 8.2 Relationship To Listing Audit

The Listing Audit asks "is this listing working?" The Shop Visibility Report asks "is the *shop* working as a whole, beyond the sum of its listings?" The two are complementary, not redundant.

A seller who has completed an Audit on 10–15 listings can often produce a Shop Visibility Report at lower cost, because the per-listing diagnosis is already on file. The Shop Report then focuses on cross-listing patterns, category clarity, and shop-level signals that an individual listing audit does not surface.

### 8.3 Buyer Inputs Needed

1. Etsy shop URL.
2. Shop opened date (to gauge maturity).
3. Total active listings.
4. Top 3 sellers in their own words.
5. The shop's positioning or theme in one sentence (what would the seller say the shop is "about"?).
6. Whether shop sections / categories are in use and how the seller groups listings.
7. Any planned product launches or removals in the next 60 days.
8. Optional: prior reports purchased from SearchClarity (so we can build on, not duplicate, earlier findings).

### 8.4 Report Sections

1. Cover Page
2. Scope
3. Shop Visibility Summary
4. Product / Niche Clarity Review
5. Listing Group Review
6. Shop Section / Category Review
7. Keyword Theme Consistency
8. Buyer Trust Signal Review
9. Internal Consistency Issues
10. Priority Shop-Level Fixes
11. Recommended Path
12. Caveats
13. Next Steps

### 8.5 Required Tables

**Shop Visibility Diagnosis Table** — section 3.

| Area | Current Issue | Visibility Impact | Recommended Fix |
|---|---|---|---|
| Niche clarity | | [High / Medium / Low] | |
| Listing groups | | | |
| Section structure | | | |
| Keyword themes | | | |
| Trust signals | | | |
| Internal consistency | | | |

**Listing Group Table** — section 5.

| Product Group | Current Theme | Buyer Intent | Issue | Recommendation |
|---|---|---|---|---|
| | | | | |

**Shop-Level Action Plan** — section 10.

| Priority | Action | Why It Matters | Timing |
|---|---|---|---|
| Do first | | | |
| Do next | | | |
| Test later | | | |
| Avoid | | | |

### 8.6 Example Filled-In Shop-Level Finding

Fictional example.

---

> **Finding: niche fragmentation across 47 active listings**
>
> Observation: The shop's listings split roughly into three groups — personalized retirement gifts (18 listings), funny coworker candles (14 listings), and wedding party gifts (15 listings). The three groups share no common keywords, no common buyer recipient, and no common occasion.
>
> Why it matters: Etsy's search ranking takes shop-level signal into account. A shop where every listing reinforces the same niche (e.g., "personalized retirement gifts") builds compounding signal — every additional listing strengthens the shop's authority on the niche keyword set. A shop split across three unrelated niches forces each group to compete independently, with none of them benefiting from shop-level reinforcement.
>
> Recommendation: Consolidate around one primary niche; treat the other two as either secondary or candidates for migration to a separate shop.
>
> How to implement: Identify which of the three groups produces the most revenue per active listing over the past 90 days. Lead with that group as the primary niche. Reorganise shop sections so the primary niche occupies the first 3–4 sections. Either gradually retire the smallest group, or migrate it to a new dedicated shop if revenue justifies a separate brand.
>
> Caveat: Do not delete revenue-producing listings to "clean up" the niche. Phased migration over 90+ days is preferable. Splitting a shop is a significant operational decision that affects reviews, favourites, and existing buyer relationships — the recommendation is direction-setting, not a directive.

---

### 8.7 What To Avoid

A Shop Visibility Report fails when it:

- Becomes a 47-listing audit (that is the Audit; this is shop-level).
- Drifts into branding consulting, photography critique, pricing strategy, product development advice, or full business consulting unless explicitly scoped at a higher tier.
- Treats the shop as if it should match a textbook ideal rather than the seller's actual goals.
- Recommends a full shop rebuild without acknowledging the cost and risk of doing so.
- Skips the Recommended Path section — buyers need to know which findings are urgent and which can wait.
- Repeats individual listing findings the buyer has already received in an Audit.

---

## 9. Report 6 — Pinterest SEO Plan for Etsy Sellers

**Buyer problem:** "I want Pinterest traffic for my Etsy shop, but I do not know what to pin, what boards to create, or how to write pin titles/descriptions."

### 9.1 When To Sell This Report

Sell to sellers who:

- Have a visually-driven product (gifts, decor, fashion, stationery, anything where the buyer decision is partly aesthetic).
- Already have a stable Etsy listing set worth driving traffic to (don't pin into a broken funnel — recommend Audit first).
- Are willing to pin consistently (this is a strategy report, not a "we'll grow your Pinterest for you" service).
- Have or are willing to create a Pinterest business account.

### 9.2 Relationship To Etsy SEO Reports

Pinterest is not Etsy search. The two have overlapping but distinct buyer-intent patterns. Pinterest excels at discovery (early-stage browsing); Etsy search excels at intent (ready-to-buy). A Pinterest SEO Plan extends a seller's reach into the discovery side of the funnel while Etsy SEO covers the intent side.

This report works best after the seller has a Keyword Research Pack — Pinterest keyword themes draw on, but are not identical to, the Etsy keyword set. Pinterest favours descriptive, aspirational, and search-intent language; Etsy favours product-intent and buyer-recipient language. The Pinterest Plan reuses the Etsy research as a foundation and re-clusters terms for Pinterest's discovery model.

### 9.3 Buyer Inputs Needed

1. Etsy shop URL.
2. Pinterest business account URL (or confirmation the seller will create one).
3. Top 5–10 listings to promote.
4. Existing Pinterest boards (if any).
5. Existing pin templates or visual style (link to portfolio or example pins).
6. Hours per week the seller can commit to Pinterest (10–60 minutes is the realistic range for solo sellers).
7. Seasonality of the seller's products (year-round / Q4 peak / occasion-driven).
8. Whether the seller produces lifestyle imagery or only product imagery.

### 9.4 Report Sections

1. Cover Page
2. Scope
3. Pinterest SEO Summary
4. Priority Products to Promote
5. Pinterest Keyword Themes
6. Board Structure Recommendations
7. Pin Title Templates
8. Pin Description Templates
9. 30-Day Content Plan
10. Seasonal Timing Notes
11. Etsy-to-Pinterest Alignment Notes
12. Caveats
13. Next Steps

### 9.5 Required Tables

**Pinterest Keyword Theme Table** — section 5.

| Theme | Related Keywords | Buyer Intent | Recommended Board / Pin Use |
|---|---|---|---|
| | | [Browsing / Comparing / Ready to buy] | |

**Board Recommendation Table** — section 6.

| Board Name | Purpose | Products To Include | Notes |
|---|---|---|---|
| | | | |

**Pin Template Table** — sections 7–8.

| Product / Listing | Pin Title Template | Pin Description Template | Keywords Used |
|---|---|---|---|
| | | | |

**30-Day Content Plan** — section 9.

| Week | Action | Products / Themes | Notes |
|---|---|---|---|
| Week 1 | | | |
| Week 2 | | | |
| Week 3 | | | |
| Week 4 | | | |

### 9.6 Example Filled-In Pinterest Plan Snippet

Fictional example — a personalized retirement gifts Etsy shop.

---

> **Board recommendations (selection)**
>
> | Board Name | Purpose | Products To Include | Notes |
> |---|---|---|---|
> | Retirement Gift Ideas | Top-of-funnel discovery for retirement gifting | All retirement-themed listings | Lead board; pin frequency 3–5/week |
> | Personalized Gifts for Coworkers | Recipient-specific discovery | Coworker-relevant retirement, birthday, leaving listings | Cross-board with leaving and birthday boards |
> | Funny Office Gifts | Aesthetic + humour discovery | Funny candles, gag mugs, novelty desk items | Visual-led; lifestyle pins outperform product-only pins |
> | Last Day at Work Ideas | Long-tail buyer-problem discovery | Retirement, job change, going-away listings | Lower volume but higher intent |
> | Teacher Retirement Gifts | Niche recipient discovery | Teacher-specific listings only | Seasonal peak Apr–Jun |
>
> **Pin title and description template — funny retirement candle for coworker**
>
> - Pin title template: `Funny Retirement Gift for Coworker — Personalized Candle for the Office`
> - Pin description template: `Looking for a funny retirement gift for a coworker, boss, or office friend? This personalized candle is a lighthearted last-day gift idea that won't end up in a desk drawer. Shop personalized retirement gifts at [shop name]. #retirementgift #coworkergift #funnygift #personalizedgift`
> - Keywords used: `funny retirement gift`, `retirement gift for coworker`, `personalized candle`, `last day gift`, `office gift`, `funny gift`, `personalized gift`
> - Note: Pinterest descriptions are longer and more conversational than Etsy. Treat the first sentence as the hook and the rest as keyword-supportive context.
>
> **30-day plan (excerpt)**
>
> Week 1: Create 5 boards above. Pin 3 existing listings per day, 1 per board, varying which listings go to which board. Total ~15 pins.
> Week 2: Create 10 fresh pin designs for the top 5 listings (2 design variants per listing). Pin across relevant boards. Total ~10 new pins.
> Week 3: Repin top performers from weeks 1–2 to a second relevant board. Add 5 group-board contributions if invited to any niche group boards. Total ~10–15 actions.
> Week 4: Review Pinterest analytics for top-performing pins. Create 5 new pin designs in the same template as the top performers. Pin to lead boards. Total ~5 new pins.
>
> Total time commitment: 20–40 minutes/week.

---

### 9.7 What To Avoid

A Pinterest SEO Plan fails when it:

- Promises traffic, follower growth, click-through rates, or sales.
- Treats Pinterest like Etsy search (different intent, different algorithm).
- Recommends a posting schedule the seller cannot realistically maintain.
- Includes specific pin designs or templates as deliverables (this is a strategy report, not a graphic design service).
- Suggests using copyrighted images, brand logos, or licensed characters in pin designs.
- Recommends following / unfollowing / engagement loops (against Pinterest policy and ineffective).
- Skips the Etsy-to-Pinterest Alignment Notes — pins that drive clicks to listings that don't match the pin's promise will hurt conversion.

---

## 10. Report 7 — Shopify Product Page SEO Audit

**Buyer problem:** "My Shopify product pages exist, but they are not getting found or understood by search engines."

### 10.1 When To Sell This Report

Sell to sellers who:

- Own a Shopify store (or migration to one is imminent).
- Have 10+ product pages live.
- Have been live at least 60 days.
- Report low organic search traffic or low Google impressions.
- Are not currently running a full technical SEO retainer with another agency.

### 10.2 Relationship To Etsy Reports

This report is an **expansion product** for sellers who run an Etsy shop *plus* their own Shopify site, or who are migrating from Etsy to a standalone storefront. The Etsy reports treat the marketplace as the discovery surface; this report treats Google as the discovery surface. The two are not interchangeable.

Sellers who have completed the Etsy reports often bring transferable keyword research, recipient framing, and listing copy patterns into Shopify. This report leverages that prior work where it applies, and identifies where Shopify-specific demands diverge (longer descriptions, metadata, collections, internal linking, schema).

### 10.3 Buyer Inputs Needed

1. Shopify store URL.
2. URLs of up to [N] product pages to be audited.
3. URLs of relevant collection pages.
4. Primary product category in the seller's own words.
5. Target buyer in one sentence.
6. Access to Google Search Console data (optional but strongly recommended).
7. Theme name and version (some recommendations depend on theme capabilities).
8. Whether the seller currently uses any SEO app (Shopify SEO apps vary widely in what they auto-generate).

### 10.4 Report Sections

1. Cover Page
2. Scope
3. Product Page SEO Summary
4. Product Title / Meta Title Review
5. Meta Description Review
6. Product Description Clarity
7. Collection / Internal Link Notes
8. FAQ / Content Gap Suggestions
9. Schema Readiness Notes
10. Priority Product Page Fixes
11. Caveats
12. Next Steps

### 10.5 Required Tables

**Product Page Diagnosis Table** — section 3.

| Page URL | Current Issue | SEO Impact | Recommended Fix |
|---|---|---|---|
| | | [High / Medium / Low] | |

**Metadata Recommendation Table** — sections 4–5.

| Page URL | Current Title / Meta | Recommended Direction | Reason |
|---|---|---|---|
| | | | |

**Content Gap Table** — section 8.

| Page URL | Missing Content | Why It Matters | Suggested Addition |
|---|---|---|---|
| | | | |

### 10.6 Example Filled-In Shopify Finding

Fictional example.

---

> **Page: /products/personalized-retirement-candle-coworker**
>
> **Current meta title:** Personalized Retirement Candle | Acme Gifts
>
> Observation: The meta title leads with the product type but does not include the recipient or buyer-intent modifier. The shop brand ("Acme Gifts") consumes 13 characters that could carry buyer-intent terms instead.
> Why it matters: Google search snippets are scanned in roughly 1–2 seconds. The first 40–50 characters of the meta title determine click-through more than the back half. Recipient-specific intent ("for coworker") materially increases click-through when the search query includes the recipient.
> Recommendation: Restructure the meta title in the direction of: `Personalized Retirement Candle for Coworker — Funny Office Gift | Acme Gifts`. Total length should stay under 60 characters where possible.
> How to implement: Edit the product page meta title in Shopify Admin → Products → [Product] → Search engine listing preview. Save and submit the URL to Google Search Console for re-crawl. Allow 14–21 days for any change to register in search appearance.
> Caveat: Meta title changes affect existing rankings unpredictably. Pages with existing organic traffic should be changed conservatively. Track Search Console impressions and average position for at least 21 days before further iteration.

---

### 10.7 What To Avoid

A Shopify Product Page SEO Audit fails when it:

- Pretends to be a full technical SEO audit (Core Web Vitals, crawl budget, site architecture, redirects, hreflang) unless specifically scoped as such.
- Recommends app installations without explaining the trade-offs (apps add load time, complexity, and recurring cost).
- Suggests metadata changes for pages with strong existing organic traffic without flagging the risk.
- Confuses Shopify's product description fields with the meta description (they are separate).
- Skips schema readiness notes — even a brief note flags whether Report 8 is the recommended next step.
- Includes "speed up your site" as a recommendation without a specific page-level finding (this is technical SEO, scoped separately).

---

## 11. Report 8 — Schema / Structured Data Readiness Audit

**Buyer problem:** "My website / product pages are not structured clearly for Google or AI search systems."

### 11.1 When To Sell This Report

Sell to sellers who:

- Own a website where they can control schema markup (Shopify, WordPress, Webflow, custom build).
- Have product, FAQ, About, or content pages live.
- Want to improve eligibility for Google rich results, knowledge panel entity recognition, and AI search system parsing.

Do not sell this report for Etsy-only sellers. Etsy controls its own structured data; sellers cannot meaningfully add or edit schema on Etsy listings. Etsy-only sellers asking about "schema" or "structured data" should be redirected to the Listing Visibility Audit or the Shop Visibility Report.

### 11.2 Relationship To Shopify Product SEO and AI Search Readiness

This report sits between the Shopify Product Page SEO Audit (Report 7) and the AI Search Readiness Audit (Report 9). The Shopify audit identifies what content gaps exist; the Schema audit identifies how to mark up that content so machines understand it; the AI Search audit identifies how that machine-readable content positions the brand for LLM-based discovery.

Sold as a pair with the AI Search Readiness Audit, this report is the technical foundation; the AI Search audit is the strategic application.

### 11.3 Buyer Inputs Needed

1. Website URL.
2. Platform (Shopify, WordPress, Webflow, custom).
3. URLs of up to [N] pages to be audited.
4. Page types to prioritise (product, FAQ, About, blog, service).
5. Whether any schema is currently installed (and via what method — app, plugin, theme, manual).
6. Whether the site has multiple locations, multiple brands, or multiple languages (affects entity schema).
7. Access to Google Search Console (optional but helps validate Rich Results status).
8. Any structured data validation errors the seller has already noticed.

### 11.4 Report Sections

1. Cover Page
2. Scope
3. Structured Data Summary
4. Pages Reviewed
5. Current Schema Found
6. Missing Schema Opportunities
7. Recommended Schema Types
8. Entity Clarity Notes
9. Implementation Guidance
10. Validation / Testing Notes
11. Caveats
12. Next Steps

### 11.5 Required Tables

**Schema Opportunity Table** — section 6.

| Page | Current Schema | Missing / Recommended Schema | Why It Matters | Priority |
|---|---|---|---|---|
| | | | | [Do first / Do next / Test later] |

**Entity Clarity Table** — section 8.

| Entity | Current Signal | Gap | Recommendation |
|---|---|---|---|
| Brand / Organization | | | |
| Products | | | |
| People (founder, etc.) | | | |
| Location | | | |

### 11.6 Example Filled-In Schema Recommendation

Fictional example.

---

> **Page: /products/personalized-retirement-candle-coworker**
>
> Current schema: Basic Product schema present (name, image, description, price, availability). Auto-generated by Shopify theme.
> Missing / recommended: AggregateRating (no review markup despite 47 reviews on the page); Brand (currently absent — name only appears in page text); MerchantReturnPolicy (absent, despite return policy being clearly stated in shop policies).
> Why it matters: Aggregate ratings make the product eligible for star-rating rich snippets in Google search results, which materially affects click-through. Brand markup helps Google associate the product with the shop's brand entity. MerchantReturnPolicy improves trust signals and supports Google Shopping eligibility.
> Recommendation: Extend Product schema to include AggregateRating, Brand, and MerchantReturnPolicy fields.
> How to implement: For Shopify, this can be added either via a dedicated SEO app that supports custom Product schema, or via a theme-level edit to the product template's JSON-LD block. Pull review data from the existing reviews app's API or data attributes. Validate with Google's Rich Results Test (search.google.com/test/rich-results) after deployment.
> Caveat: Schema does not guarantee rich results. Google decides which markup to surface based on its own quality signals. Mark up accurately — falsely claiming aggregate ratings that don't exist is a Google policy violation and can result in manual action against the entire site.

---

### 11.7 What To Avoid

A Schema Readiness Audit fails when it:

- Treats schema as magic ranking dust. Schema does not improve rankings directly; it improves machine understanding and *eligibility* for rich results.
- Promises rich snippets, knowledge panels, or AI citations.
- Recommends schema types the page content does not genuinely support (e.g., AggregateRating on a page with no reviews).
- Skips validation guidance — the buyer needs to know how to test the markup after implementing it.
- Recommends schema that the buyer's platform cannot reasonably support without development work, without flagging the cost.
- Includes schema for Etsy listings (Etsy controls its own markup).

Reusable caveat to include in section 11:

> **About schema and search visibility**
>
> Structured data helps search engines and AI systems understand page content. It does not guarantee rich results in Google search, knowledge panel inclusion, AI citations, or improved ranking. Google and other systems decide whether to surface marked-up content based on their own quality and trust signals. Mark up content accurately and only when the markup matches what is actually on the page — false or misleading markup can result in Google manual actions.

---

## 12. Report 9 — AI Search / LLM Visibility Readiness Audit

**Buyer problem:** "I want my shop, brand, or website to be easier for AI search tools to understand, cite, or mention."

### 12.1 When To Sell This Report

Sell to sellers who:

- Own a website or brand presence with citable content (FAQ, About, product info, blog, founder bio).
- Have an established brand worth being cited (this is not for sellers with zero brand history).
- Are willing to invest in content and entity work (this is a readiness audit, not a quick fix).
- Understand AI search results are not deterministic and no one controls citations.

This is a premium-tier offering and a strong differentiator. Few competing SEO services address this; positioning matters.

### 12.2 Relationship To Schema Readiness and Seller Visibility Strategy

This report builds on Schema Readiness (Report 8) — schema is one of several inputs into AI search comprehension. It feeds into the Seller Visibility Strategy Report (Report 10), where AI search readiness becomes one channel within a multi-channel visibility plan.

Sold standalone, this report includes a lightweight schema readiness review. Sold after Report 8, it can skip the schema review and focus on the AI-specific layers: entity clarity, sourceable content, third-party mentions, and prompt-visibility checks.

### 12.3 Buyer Inputs Needed

1. Website URL.
2. Brand name and any common variations or misspellings.
3. URLs of About, FAQ, founder bio, and core content pages.
4. Notable third-party mentions (press, podcasts, interviews, listings).
5. Wikipedia presence (yes / no / pending).
6. Industry / niche the brand operates in.
7. 5–10 example questions a prospective buyer might ask an AI assistant about the seller's category.
8. Whether the seller has any structured FAQ content live.

### 12.4 Report Sections

1. Cover Page
2. Scope
3. AI Search Readiness Summary
4. Brand / Entity Clarity Review
5. Sourceable Content Review
6. FAQ / About / Policy Page Review
7. Citation-Worthy Page Opportunities
8. Third-Party Mention / Source Gaps
9. Schema and Structured Data Alignment
10. Example Query / Prompt Visibility Check
11. Priority Readiness Fixes
12. Caveats
13. Next Steps

### 12.5 Required Tables

**Entity Clarity Table** — section 4.

| Entity | Current Signal | Gap | Recommended Fix |
|---|---|---|---|
| Brand name | | | |
| Founder / key people | | | |
| Product line | | | |
| Location | | | |
| Category / niche | | | |

**Sourceable Content Gap Table** — sections 5–7.

| Question / Query | Current Page Exists? | Gap | Recommended Page / Section |
|---|---|---|---|
| | [Yes / No / Partial] | | |

**AI Readiness Action Plan** — section 11.

| Priority | Action | Why It Matters | Timing |
|---|---|---|---|
| Do first | | | |
| Do next | | | |
| Test later | | | |
| Avoid | | | |

### 12.6 Example Filled-In AI Readiness Finding

Fictional example.

---

> **Finding: brand entity is ambiguous to AI search systems**
>
> Observation: A prompt-visibility check across three AI search systems for the query "best personalized retirement gift shops" returned recommendations of 8–12 shop names per response, none of which were the seller's brand. Direct prompts for the seller's brand name returned partial information — the assistant correctly identified the brand as a retirement gift shop, but could not name specific products, the founder, or the brand's distinguishing positioning.
>
> Why it matters: AI search systems lean on Wikipedia, structured data, FAQ content, and high-trust third-party mentions to understand brand entities. The seller's brand has none of these in adequate form. As AI search shifts more discovery away from traditional search results pages, brand entity weakness becomes a compounding visibility cost.
>
> Recommendation: Build the entity. This is a multi-quarter effort, not a quick fix.
>
> How to implement:
> - Create or expand the About page with explicit, factual statements: when the brand was founded, by whom, in what location, what it makes, who it serves, what makes it different (specifics, not adjectives).
> - Create a dedicated FAQ page answering the 5–10 prospective-buyer questions surfaced in intake.
> - Apply Organization and FAQ schema (see Report 8 if not already implemented).
> - Identify 3–5 third-party publications, podcasts, or directories in the personalized gifts niche; pursue mentions over the next 6 months.
> - Do not pursue Wikipedia inclusion prematurely — Wikipedia requires sustained third-party coverage. Build coverage first; Wikipedia eligibility follows.
>
> Caveat: SearchClarity does not control whether any AI system cites or mentions the brand. This recommendation improves the *readiness* and *clarity* of the brand's signals. Whether and when any AI system surfaces the brand remains entirely outside our control.

---

### 12.7 What To Avoid

An AI Search Readiness Audit fails when it:

- Promises ChatGPT mentions, citations, AI traffic, AI rankings, or LLM recommendations.
- Uses any language suggesting SearchClarity can "get the brand into ChatGPT."
- Recommends prompt-injection, AI-targeting hacks, or any technique designed to manipulate AI output.
- Treats AI search as if it works like traditional search (it doesn't, and won't, predictably).
- Skips the prompt-visibility check section — the buyer needs to see actual examples of how their brand currently appears (or doesn't) in AI responses.
- Pretends a single audit can produce AI citations. Entity-building takes quarters, not weeks.

Reusable language for the report (section 12):

> **About AI search readiness**
>
> This report improves the readiness, clarity, and citability of the brand's online presence. It does not control whether any AI system cites, mentions, or recommends the brand. AI search systems are non-deterministic; the same prompt can produce different responses minutes apart, and citation policies vary by system and change without notice.
>
> Recommendations in this report focus on signals that are within the seller's control: entity clarity, sourceable content, structured data, and third-party mention opportunities. Outcomes depend on these signals being present *and* on AI systems weighting them — only the first is within scope.

---

## 13. Report 10 — Seller Visibility Strategy Report

**Buyer problem:** "I need a bigger visibility plan, not just listing fixes."

### 13.1 When To Sell This Report

Sell to sellers who:

- Have already purchased multiple SearchClarity reports (ideally 3+).
- Are running an established operation (12+ months, multi-channel, or 50+ listings / pages).
- Want a roadmap, not another audit.
- Are willing to invest in 90+ days of execution before judging outcomes.

This is the most premium offering in the range. It must read like strategy, not like a stacked summary of prior reports.

### 13.2 Relationship To Other Reports

This report synthesises findings from across the SearchClarity range. Its quality is bounded by how many upstream reports the buyer has commissioned:

- With 5+ prior reports, the synthesis is rich: per-channel diagnoses, prior keyword research, prior shop-level findings, prior competitor observations, prior technical readiness audits.
- With 2–3 prior reports, the analyst supplements with a focused, lighter-touch review across gaps (a partial Shop Visibility pass, a partial Keyword Research pass) — but this should be priced into a higher tier or noted as a scope expansion.
- With 0 prior reports, this report is significantly weaker and should generally be declined or repackaged as "Audit + Strategy" at a higher tier.

Reports this synthesises (where applicable):

- Listing Visibility Audit (1)
- Keyword Research Pack (3)
- Competitor Visibility Observations (4)
- Etsy Shop Visibility Report (5)
- Pinterest SEO Plan (6)
- Shopify Product Page Audit (7)
- Schema Readiness Audit (8)
- AI Search Readiness Audit (9)

### 13.3 Buyer Inputs Needed

1. All prior SearchClarity report deliverables (so we synthesise, not duplicate).
2. Seller's business goals for the next 6–12 months in plain words.
3. Channels currently active (Etsy, Shopify, Pinterest, Instagram, email list, paid ads, wholesale).
4. Revenue split across channels (rough percentages, not exact figures).
5. Capacity constraints — hours per week, team size, budget for tooling.
6. Any known dependencies (busy season, upcoming launch, planned product line changes).
7. What the seller has already tried in the past 12 months and what worked or didn't.
8. Optional: target metric the seller wants to improve (e.g., Etsy impressions, Google organic clicks, AI mention rate).

### 13.4 Report Sections

1. Cover Page
2. Scope
3. Executive Strategy Summary
4. Current Visibility Position
5. Core Search / Marketplace Gaps
6. Keyword / Demand Opportunities
7. Marketplace Positioning Recommendations
8. Off-Platform Traffic Opportunities
9. Website / Schema / AI Search Readiness Notes
10. 30/60/90-Day Action Plan
11. Priority Roadmap
12. Measurement Plan
13. Caveats
14. Next Steps

### 13.5 Required Tables

**Visibility Roadmap Table** — section 10.

| Timeline | Focus | Actions | Expected Signal To Watch |
|---|---|---|---|
| Days 1–30 | | | |
| Days 31–60 | | | |
| Days 61–90 | | | |

**Channel Priority Table** — section 11.

| Channel | Current State | Opportunity | Priority | Why |
|---|---|---|---|---|
| Etsy | | | | |
| Shopify | | | | |
| Pinterest | | | | |
| Email | | | | |
| AI Search | | | | |

**Measurement Plan** — section 12.

| Metric | Where To Check | Why It Matters | Review Timing |
|---|---|---|---|
| | | | [Weekly / Monthly / Quarterly] |

### 13.6 Example Filled-In Strategy Finding

Fictional example.

---

> **Strategic finding: channel concentration is creating fragility**
>
> Observation: The seller currently produces approximately 92% of revenue through Etsy. Shopify, despite being live for 14 months, drives less than 6% of revenue. Pinterest is dormant. The brand has no email list. AI search readiness is low (per Report 9).
>
> Why it matters: A 92% Etsy concentration means the business's revenue trajectory is set by Etsy's algorithm decisions, fee schedule, and policy changes — none of which are within the seller's control. The Shopify store exists but functions as an inactive asset. The lack of email and dormant Pinterest mean there is no owned-audience cushion when marketplace traffic dips.
>
> Recommendation: Treat the next 90 days as a *diversification readiness* phase, not a traffic-driving phase. The goal is to make non-Etsy channels capable of carrying real volume, not to immediately shift revenue away from Etsy.
>
> 30/60/90-day shape:
> - Days 1–30: Shopify product page SEO fixes (per Report 7); email capture installation; first 10 Pinterest pins per Report 6.
> - Days 31–60: Schema implementation on Shopify (per Report 8); first email broadcast to capture list; Pinterest content cadence steady at 3–5 pins/week.
> - Days 61–90: AI search readiness work begins (entity content per Report 9); review Shopify Search Console for first organic signal; assess whether Pinterest is producing measurable clicks.
>
> Expected signals at 90 days: Shopify impressions in Google Search Console up materially from baseline (specific %s depend on baseline — not promised); Pinterest impressions trending; email list begun; AI search entity content live.
>
> Caveat: Diversification takes longer than 90 days to show in revenue. The 90-day window is for readiness signals, not revenue shift. A realistic revenue rebalance target is 12–18 months. Do not abandon the strategy because revenue has not moved by month 3.

---

### 13.7 What To Avoid

A Seller Visibility Strategy Report fails when it:

- Becomes full business consulting (operations, hiring, financial planning) unless explicitly scoped at a higher tier.
- Promises revenue, traffic, sales, or specific growth percentages.
- Uses vague "grow your brand" / "build authority" / "engage your audience" filler.
- Stacks prior reports verbatim instead of synthesising them.
- Recommends 47 priorities (a strategy is what you choose *not* to do).
- Skips the Measurement Plan — without it, the buyer cannot tell whether the strategy is working.
- Treats every channel as equally worth investing in (channel choice is the core strategic act).

---

## 14. Package-Level Deliverable Differences

Three tiers per report: Basic, Standard, Premium. The tier names stay constant across reports; the scope contents change. Buyers should be able to skim a tier matrix and immediately understand what they receive.

| Report | Basic | Standard | Premium |
|---|---|---|---|
| 1. Etsy Listing Visibility Audit | 5 listings audited; PDF report; Priority Action Plan | 12 listings audited; PDF report; Action Plan; Title Structure + Tag Coverage + Description analysis | 25 listings audited; PDF report; Action Plan; full per-listing findings; cross-listing patterns chapter; 30-day implementation check-in (1 written follow-up) |
| 2. Etsy Title and Tag Rewrite | 5 listing rewrites; PDF + spreadsheet | 12 listing rewrites; PDF + spreadsheet; tag rationale notes per listing | 25 listing rewrites; PDF + spreadsheet; tag rationale + description opening rewrites; one 30-day rewrite review (single follow-up document) |
| 3. Etsy Keyword Research Pack | 50 keywords; PDF summary + .xlsx | 150 keywords; PDF + .xlsx; clustering; intent groups; Avoid list | 300+ keywords; PDF + .xlsx; clustering; intent groups; seasonal notes; recommended use per keyword; competitor pattern overlay |
| 4. Etsy Competitor Visibility Observations | 3 search terms observed; PDF report; pattern summary | 7 search terms; PDF report; pattern + opportunity gap analysis | 12 search terms; PDF report; pattern + gap + recommended response strategy; positioning chapter |
| 5. Etsy Shop Visibility Report | Up to 25 listings reviewed at shop level; PDF report | Up to 50 listings; PDF report; section/category review; keyword theme consistency | Up to 100 listings; PDF report; full shop chapter set; recommended path; 60-day follow-up review (single document) |
| 6. Pinterest SEO Plan for Etsy Sellers | 5 boards recommended; 10 pin templates; PDF | 10 boards; 25 pin templates; PDF + 30-day plan | 15 boards; 50 pin templates; PDF + 90-day plan + seasonal calendar |
| 7. Shopify Product Page SEO Audit | 5 product pages; PDF report | 12 product pages; PDF + collection page notes; FAQ gap analysis | 25 product pages; PDF + collection + FAQ + schema readiness preview |
| 8. Schema Readiness Audit | Up to 10 pages reviewed; PDF; opportunity table | Up to 25 pages; PDF + entity clarity review + implementation guidance | Up to 50 pages; PDF + entity + implementation + validation walkthrough; one validation follow-up after implementation |
| 9. AI Search Readiness Audit | Brand-level review + 5 prompt-visibility checks; PDF | Brand + 10 prompt checks; sourceable content review; entity clarity table | Brand + 20 prompt checks; full sourceable content review; third-party mention opportunity list; 90-day readiness plan |
| 10. Seller Visibility Strategy Report | Synthesis of up to 2 prior reports; PDF; 30-day plan only | Synthesis of up to 5 prior reports; PDF; 30/60/90-day plan; measurement plan | Synthesis of up to 9 prior reports; PDF; 30/60/90-day plan; measurement plan; quarterly check-in (one follow-up review at day 90) |

Tier principles:

- Basic exists to be affordable enough to be a first purchase; it is not "the cheap version" — it is the entry product.
- Standard is the default recommendation for most sellers.
- Premium adds depth, breadth, or one structured follow-up — not "more value" via marketing puffery.

Follow-ups, where included in Premium, are scoped: one written follow-up document, not ongoing consulting. The scope of the follow-up is defined in the original report's delivery.

---

## 15. Universal Buyer Intake Rules

### 15.1 Universal Intake Questions (every report)

1. Shop or website URL.
2. The buyer's email (delivery + follow-up).
3. Niche or product category in one sentence.
4. Target buyer in one sentence.
5. Any specific listings, pages, or terms the report should prioritise.
6. Any words, brands, or topics to exclude.
7. Any prior SearchClarity reports purchased.

That's seven. The eighth slot is reserved for any report-specific question that cannot fit elsewhere.

### 15.2 Report-Specific Intake Questions

**Report 1 — Listing Visibility Audit**
1. Listing URLs to audit.
2. Anything already tried (recent title/tag/photo changes).

**Report 2 — Title and Tag Rewrite**
1. Listing URLs.
2. Words to keep or avoid (brand voice).

**Report 3 — Keyword Research Pack**
1. Seed keywords or angles.
2. Seasonality preference (year-round vs. occasion-driven).

**Report 4 — Competitor Visibility Observations**
1. 5–10 target keywords.
2. Optional: up to 3 competitor shops.

**Report 5 — Shop Visibility Report**
1. Total listing count.
2. Shop positioning in one sentence.

**Report 6 — Pinterest SEO Plan**
1. Pinterest account URL (or confirmation of intent to create).
2. Hours per week available for pinning.

**Report 7 — Shopify Product Page SEO Audit**
1. Product page URLs.
2. Whether Google Search Console access can be shared (optional).

**Report 8 — Schema Readiness Audit**
1. Platform (Shopify, WordPress, etc.).
2. Page URLs to audit.

**Report 9 — AI Search Readiness Audit**
1. 5–10 example questions a prospective buyer might ask an AI assistant.
2. Notable third-party mentions (press, podcasts, directories).

**Report 10 — Seller Visibility Strategy Report**
1. All prior SearchClarity reports.
2. Business goals for the next 6–12 months in plain words.

### 15.3 Intake Rules (enforced by intake form)

- Maximum 8 required questions per report (7 universal + 1 specific, or 6 universal + 2 specific where the universal one is genuinely irrelevant).
- Do not ask for revenue, profit, or financial figures unless the report explicitly requires it (Report 10 only).
- Do not require analytics access (Google Search Console, Etsy Marketplace Insights) for entry-level Basic tiers — request as optional.
- Keep Fiverr-buyer friction low: every additional required field costs orders.
- Ask only what is needed to produce the report. If a field's data is not used in the report itself, it does not belong in intake.
- Allow free-text for any "in one sentence" answer — drop-downs constrain useful detail.
- Provide an "anything else?" optional field at the end of every intake.

---

## 16. Universal Delivery Messages

Templates for buyer-facing messages. Tone: professional, direct, helpful, not desperate, not fake-friendly, not spammy. First-person plural ("we"); concise; no exclamation marks unless the buyer leads with celebratory language first.

### 16.1 Order received

> Hi [name],
>
> Thanks for your order — we've received it and your report is in the queue. Standard turnaround for this report is [X] business days. We'll review your intake responses in the next 24 hours and message you if anything needs clarification before we begin.
>
> If you'd like to add or change anything in your intake, the easiest way is to reply to this message.
>
> — SearchClarity

### 16.2 Missing information

> Hi [name],
>
> Before we begin your report, we need a couple of clarifications from your intake:
>
> 1. [Specific question]
> 2. [Specific question, if applicable]
>
> Once you reply, your turnaround timer starts from that point. We try to ask everything we need in one message so it's not back-and-forth.
>
> — SearchClarity

### 16.3 Delivery — Audit-type reports (1, 5, 7, 8, 9)

> Hi [name],
>
> Your [report name] is attached. A few things to know:
>
> - The Executive Summary on page 2 is the fastest way in.
> - The Priority Action Plan on page [X] is what to do this week.
> - The Caveats section explains what this report does and doesn't promise — please read it.
>
> Most sellers see the biggest gains from the "Do first" items in the action plan. Test changes over 14–21 days before iterating further, so you can see what's actually moving.
>
> If you'd like a follow-on report once you've implemented changes (commonly: [recommended next report]), let us know — we'll apply a returning-customer discount.
>
> — SearchClarity

### 16.4 Delivery — Rewrite-type reports (2)

> Hi [name],
>
> Your [report name] is attached as a PDF and spreadsheet.
>
> - The spreadsheet is the working document — copy titles and tags straight from it.
> - The PDF explains the rationale for each rewrite. Read this before implementing so you know why each change is recommended.
> - Implement changes in batches, not all at once, so you can see what's moving.
>
> Please read the Caveats section. Etsy search changes; rewrites are direction-setting, not outcome-guaranteeing.
>
> — SearchClarity

### 16.5 Delivery — Research-type reports (3, 4, 6)

> Hi [name],
>
> Your [report name] is attached.
>
> - The PDF is the narrative — read this first to understand how to use the data.
> - The spreadsheet (where included) is the working tool — sortable, filterable, ready to mark up.
> - The "Recommended Use" column tells you where each item belongs (title, tag, description, board, etc.).
>
> A common mistake is using every item we surface. Don't. Choose the items that match your specific products and skip the rest.
>
> — SearchClarity

### 16.6 Delivery — Strategy report (10)

> Hi [name],
>
> Your Seller Visibility Strategy Report is attached.
>
> - Read the Executive Strategy Summary first, then the 30/60/90-day Action Plan.
> - The Measurement Plan tells you which signals to track over the 90 days — this is how you'll know whether the strategy is working.
> - Diversification work is slow. The 90-day window is for readiness signals, not revenue shift.
>
> If you'd like a 90-day follow-up review (Premium tier includes this; other tiers can purchase it as an add-on), reply and we'll schedule.
>
> — SearchClarity

### 16.7 Revision boundary

> Hi [name],
>
> Happy to look at this. To set expectations on revisions:
>
> - We revise factual errors at no charge — if we got something wrong about your shop, listings, or pages, send specifics and we'll correct it within 2 business days.
> - We revise wording or formatting at no charge if the report is hard to use as written.
> - Recommendations we revise on request *only* when you've identified a specific reason the recommendation doesn't fit your situation (e.g., a product detail we missed, a constraint we weren't told about). "I want different recommendations" without a reason isn't a revision — it's a new scope.
>
> If you'd like a re-audit after you've implemented the recommendations, that's a returning-customer order at a discount.
>
> — SearchClarity

### 16.8 Review request

> Hi [name],
>
> Hope your [report name] has been useful. If you've had a chance to implement any of the recommendations, we'd genuinely value a review of the work.
>
> Reviews help other sellers find us — and they help us prioritise which reports to build next based on what's working for sellers like you.
>
> No pressure either way.
>
> — SearchClarity

### 16.9 When a buyer asks for a ranking guarantee

> Hi [name],
>
> We don't offer ranking guarantees, and we don't sell reports that promise specific search positions, traffic numbers, or sales lifts. Every SEO service that does is either misleading buyers or guessing.
>
> What we do guarantee:
>
> - The report is reviewed by a human analyst before delivery.
> - Every recommendation includes specific reasoning and an implementation step.
> - We will fix factual errors at no charge.
>
> If you're looking for ranking guarantees, we're not the right service. If you're looking for a defensible diagnosis of what's hurting your visibility and what to test, we are.
>
> — SearchClarity

### 16.10 When a buyer asks why tool data differs from another tool

> Hi [name],
>
> Different SEO tools report different numbers because each one uses different methods to estimate search demand and competition. None of them measure real-time marketplace search data directly — they all model it.
>
> When tools disagree, we treat it as a signal that the keyword in question has *some* level of demand, and we lean on direct marketplace observation (what actually appears in search results) over any single tool's estimate.
>
> The report labels tool data as "estimated" for this reason. The recommendation is to use the direction the data points to, not the specific volume number.
>
> — SearchClarity

---

## 17. Quality Control Checklist

Every report passes through this checklist before delivery. No exceptions. The reviewing analyst signs off on each row.

| Check | Applies To | Pass Criteria |
|---|---|---|
| Cover page complete | All reports | Shop name, URL, date, prepared-by line, positioning line all present |
| Scope section present | All reports | Lists what was reviewed, what was not, tools used, limitations |
| Data source disclosure present | All reports | Section 3.3 language included verbatim |
| Every recommendation uses 5-line block | All reports | Observation / Why it matters / Recommendation / How to implement / Caveat — all five lines on every recommendation |
| "How to implement" line is actionable | All reports | A real seller can act on the step today without further analysis |
| Specific recommendations, not generic | All reports | No "write better titles" / "use more keywords" / "engage your audience" |
| Source labels on tool data | Reports 1, 3, 4, 5, 10 | Every search volume, competition score, trend reference labelled "estimated" with source |
| No fake metrics | All reports | No invented numbers presented as measured |
| No ranking promises | All reports | No language suggesting specific search positions will be achieved |
| No sales promises | All reports | No language suggesting specific revenue, conversion, or click-through lifts |
| No trademark-risky recommendations | All reports | No brand names, character names, protected slogans suggested as keywords |
| No generic AI wording | All reports | No "leverage", "synergy", "unlock potential", "supercharge", "game-changer" |
| Action plan included | All reports | Section 3.5 table present with Do first / Do next / Test later / Avoid rows filled |
| Caveat block included verbatim | All reports | Section 3.6 language present |
| Next Steps section included | All reports | One paragraph naming the recommended next SearchClarity report (or "no immediate next step" if appropriate) |
| Tables filled, not blank | All reports | Every required table for the report has content, not just headers |
| Ethical Use Note present | Report 4 only | Section 7.6 language included verbatim |
| Schema caveat present | Report 8 only | Section 11.7 closing language present |
| AI search caveat present | Report 9 only | Section 12.7 closing language present |
| Formatting clean | All reports | No broken tables, no orphaned headings, no placeholder text left in ("[XXX]" or "TBD") |
| Buyer can act within 7 days | All reports | At least 3 Do-first items the buyer can implement this week |
| Spelling and grammar | All reports | Reviewed by a second pair of eyes if the report is over 12 pages |
| Human review confirmed | All reports | Reviewing analyst's initials in the file metadata or footer |
| File naming convention | All reports | `SearchClarity_[ReportName]_[ShopName]_[YYYY-MM-DD].pdf` |
| Spreadsheet delivered where applicable | Reports 2, 3 | `.xlsx` and `.csv` both attached |

A report failing any row in this checklist does not ship. It returns to the analyst for revision.

---

## 18. Final Recommendations

### First report to build

**Report 1 — Etsy Listing Visibility Audit.** It is the highest-volume buyer-problem entry point on marketplace SEO, it establishes the universal framework (Section 3) every other report inherits, and its template structure is the most leveraged piece of work in the system. Build this first, ship it, get the first 10 paid customers through it, and then build outward.

### Public mock sample to create

**A filled-in Listing Visibility Audit using the fictional "Smells Like Retirement — Candle Gift" example.** Published as a downloadable PDF on the SearchClarity site, gated by an email opt-in (light — first name + email, nothing more). The mock sample doubles as a sales asset (prospective buyers see what they'd get) and as a quality benchmark (every shipped audit must meet or exceed this depth).

The mock must include all sections from 4.5 — not a truncated teaser. Buyers shopping for SEO services have been burned by gated previews that hide the real content; the differentiator is showing the full thing.

### Reports that should be templates immediately

Build full templates for these now, in order:

1. **Report 1 — Listing Visibility Audit** (anchor template — every Etsy-side report inherits from this)
2. **Report 2 — Title and Tag Rewrite** (highest natural add-on attach rate)
3. **Report 3 — Keyword Research Pack** (foundation for upsells; also standalone)

Three templates is enough to launch.

### Reports that can wait

These can be built after the first 30–60 paid orders have validated demand:

- Report 4 — Competitor Visibility Observations (start as a chapter inside Premium tier of Report 1, promote to standalone once intake demand justifies it).
- Report 5 — Shop Visibility Report (build after Audit volume creates returning-customer demand).
- Report 6 — Pinterest SEO Plan (build when at least 5 customers have requested Pinterest-related work).
- Report 7 — Shopify Product Page Audit (build when at least 3 customers have asked for Shopify work — wait for demand signal).
- Report 8 — Schema Readiness Audit (build alongside or after Report 7).
- Report 9 — AI Search Readiness Audit (build last; this is a differentiator but the buyer market for it is currently small).
- Report 10 — Seller Visibility Strategy Report (build only after at least 5 customers have purchased 3+ reports each — synthesis reports without prior reports are weak).

### Reports that depend on earlier reports

- **Report 2** depends on Report 1 for full strength (can be sold standalone with a lightweight diagnosis pass).
- **Report 9** depends on Report 8 for full strength (can be sold standalone with a lightweight schema review).
- **Report 10** depends on multiple prior reports for full strength (should generally not be sold to buyers with zero prior reports).
- **Report 5** is stronger when sold after Report 1, but does not require it.

### Standard sections that must appear everywhere

These five sections are non-negotiable in every report we ship:

1. Cover page with the positioning line (3.1).
2. Scope section (3.2).
3. Data source disclosure (3.3).
4. Action plan in the standard table format (3.5).
5. Caveat block (3.6).

A report missing any of these does not ship — it fails QC.

### Biggest risk to report quality

**Drift toward AI-generated filler.** The format is structured enough that an under-attentive analyst can fill the required tables with plausible-sounding generic rows ("Improve title structure", "Add more long-tail keywords") and the report will look complete. Section 17's QC checklist exists specifically to catch this. The "Specific recommendations, not generic" row is the most important QC check; if it fails, every other section is suspect.

Mitigation: every report is human-reviewed; the QC checklist is enforced; the public mock sample sets the depth benchmark for all internal work.

### Biggest risk to buyer trust

**Ranking and sales promises — explicit or implied.** A single sentence anywhere in any report that suggests a specific ranking improvement, traffic lift, or revenue outcome turns the entire report into a refund risk and turns the brand into another "guaranteed SEO results" service. The Caveat block (3.6) and the QC checks "No ranking promises" / "No sales promises" exist to enforce this.

Secondary trust risk: trademark-adjacent keyword recommendations. A single suggestion to use a protected brand name as a keyword can expose the buyer to a marketplace policy action or worse. The QC check "No trademark-risky recommendations" must hold.

### Next practical step

Build Report 1 — Etsy Listing Visibility Audit — as a working template document, in the same structure as Section 4 of this spec. Use the fictional "Smells Like Retirement — Candle Gift" example to fill in the per-listing finding template at full depth. Treat the resulting document as both the production template (analysts fill it in for each paid order) and the public mock sample (gated download on the SearchClarity site).

The template should be in a format that supports clean PDF export — a Word document with a defined style sheet, or a Markdown-to-PDF pipeline with a SearchClarity stylesheet, are both viable. The format choice is secondary to the content discipline.

Ship the template, take 5 paid orders, run them through the QC checklist in Section 17, then build Reports 2 and 3 in the same way.

---

**End of r04 — Comprehensive SearchClarity SEO Report System.**
