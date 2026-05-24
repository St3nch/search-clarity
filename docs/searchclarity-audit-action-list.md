# SearchClarity Audit Action List

**Source:** `searchclarity-audit-2026-05-23.md`
**Purpose:** Convert the audit into a practical work list so SearchClarity can move from planning to launch artifacts.
**Working principle:** SearchClarity ships the customer-facing business first. Neon Ronin receives the strategy/scoring/observatory work later.

---

## 1. Immediate Verdict

The audit says the docs are strategically strong but operationally incomplete. The biggest issue is not thinking quality. The biggest issue is that the launch artifacts do not exist yet.

The priority is simple:

1. Build the sample report.
2. Build the production pipeline.
3. Build the tracker.
4. Split SearchClarity capture from Neon Ronin scoring.
5. Write the launch copy/forms/SOP.

Do not keep refining strategy docs before these exist.

---

## 2. P0 Blocking Work

These block launch.

| Order | Task | Output | Project | Status |
|---:|---|---|---|---|
| 1 | Build Maplewood Candle Co. sample report | `samples/maplewood-candle-co-listing-visibility-audit.md` and PDF | SearchClarity | Not started |
| 2 | Choose and build report production pipeline | Markdown/Pandoc/CSS or chosen equivalent | SearchClarity | Not started |
| 3 | Build branded report template | Audit report template + stylesheet | SearchClarity | Not started |
| 4 | Build minimal tracker system | `r06-minimal-tracker-system.md` and spreadsheet | SearchClarity | Not started |
| 5 | Create the actual 8 tracker sheets | Customer, Order, Report, Action Plan, Keyword, Market Signal, Generalized Observation, Consent | SearchClarity | Not started |
| 6 | Write Fiverr gig copy | `r07-fiverr-gig-copy.md` | SearchClarity | Not started |
| 7 | Write Fiverr buyer intake forms | `r08-buyer-intake-forms.md` | SearchClarity | Not started |
| 8 | Write first-order fulfillment SOP | `r09-order-fulfillment-sop.md` | SearchClarity | Not started |
| 9 | Build QC form from r04 checklist | One-page checklist or tracker tab | SearchClarity | Not started |
| 10 | Reconcile launch pricing | One source-of-truth pricing section/doc | SearchClarity | Not started |

---

## 3. SearchClarity / Neon Ronin Separation Fix

The audit confirms the separation problem we already identified:

- SearchClarity should capture customer history and raw market signals.
- Neon Ronin should score, prioritize, compare, queue, and execute strategy from those signals.

### Keep in SearchClarity r05

- Customer history model.
- Order/report retention.
- Listing/page snapshots.
- Recommendations and action plans.
- Outcome labels.
- Consent rules.
- Data minimization.
- Raw Market Signal Capture fields.
- Simple analyst instruction: if you notice a niche/product/keyword gap, log it.

### Move to Neon Ronin r10

- Opportunity scoring rubric.
- Strategy-layer calculations.
- Signal ranking and prioritization.
- Cross-project observatory model.
- Future intelligence database design.
- Market signal review queues.
- Agent assignment and execution flow.
- Cubicle cluster model: SearchClarity agents, other gig-service agents, and Observatory agents.

### New Neon Ronin doc needed

`C:\dev\neon-ronin\research-docs\r10-searchclarity-strategy-layer-and-market-observatory.md`

Working purpose:

> Defines how Neon Ronin receives raw market signals from SearchClarity, scores them, compares them across opportunities, assigns research/validation work to agents, and converts validated signals into content, service improvements, internal projects, or future listings/products.

---

## 4. Market Signal System Adjustment

The audit says the 12-factor scoring model is too heavy for SearchClarity analysts during paid work. That matches the project direction.

### Decision

SearchClarity should not own scoring.

SearchClarity captures a lightweight raw signal. Neon Ronin scores later.

### SearchClarity raw signal fields

Use these for the first tracker:

| Field | Purpose |
|---|---|
| signal_id | Unique ID |
| date_observed | When it was noticed |
| source_report_type | Which paid report surfaced it |
| source_context | General context, no private client details |
| niche | Broad niche/category |
| product_category | Product/service category |
| marketplace | Etsy, Shopify, Pinterest, Google, Fiverr, etc. |
| keyword_cluster | Main keyword group if known |
| why_it_stood_out | Analyst explanation |
| evidence_summary | High-level evidence only |
| recommended_next_step | Ignore / Watch / Send to Neon Ronin |
| status | Logged / Sent to Neon Ronin / Closed |
| notes | Internal note |

### Neon Ronin scoring fields

Neon Ronin can later score:

- Buyer intent clarity.
- Keyword depth.
- Demand signal.
- Competition weakness.
- Differentiation room.
- Product variation potential.
- Seasonality.
- Content expansion potential.
- Marketplace fit.
- Operational difficulty.
- Risk / IP exposure.
- Strategic value.

But that scoring belongs in the Neon Ronin strategy layer, not in the paid-report workflow.

---

## 5. Missing Docs To Create

### Launch-blocking docs

| File | Purpose |
|---|---|
| `r06-minimal-tracker-system.md` | Spreadsheet/tracker system from day one |
| `r07-fiverr-gig-copy.md` | Final copy for first 3 Fiverr gigs |
| `r08-buyer-intake-forms.md` | Copy-paste buyer requirements for Fiverr |
| `r09-order-fulfillment-sop.md` | Manual order workflow from intake to delivery |
| `r10-report-production-pipeline.md` | Markdown/PDF/report styling workflow |

### Next launch docs

| File | Purpose |
|---|---|
| `r11-website-architecture.md` | SearchClarity.co launch site plan |
| `r12-brand-voice-style-guide.md` | Report writing rules and examples |
| `r13-launch-checklist.md` | Final pre-launch checklist |
| `r14-revision-refund-policy.md` | Boundaries for revisions, refunds, disputes |
| `r15-fiverr-asset-production.md` | Gallery/video/sample asset specs |
| `r16-searchclarity-entity-and-geo-plan.md` | SEO/GEO/LLM visibility plan for SearchClarity itself |
| `r17-market-signal-logging-sop.md` | Five-minute post-report signal logging process |

### Neon Ronin doc

| File | Purpose |
|---|---|
| `r10-searchclarity-strategy-layer-and-market-observatory.md` | Strategy/scoring/observatory layer that receives SearchClarity signals |

---

## 6. Research Topics To Queue

### P0 / launch blocking

- Fiverr 2026 rules: off-platform contact, AI disclosure, repeat-buyer messaging, gig sample policies.
- Report production pipeline: Markdown to PDF, CSS styling, template toolchain.
- Fiverr buyer intake form constraints.
- Current eRank/Marmalead/EverBee pricing and feature comparison.

### P1 / important before serious scale

- SearchClarity.co entity/GEO/LLM plan.
- Etsy API ToS and what SearchClarity can legally observe/store.
- DataForSEO role: SearchClarity analyst tool vs Neon Ronin observatory input.
- Market signal logging SOP.
- Neon Ronin r10 strategy layer design.

### P2 / after launch starts moving

- Pricing validation.
- Competitor positioning refresh.
- Founder identity / trust asset strategy.
- LLM citation behavior.
- AI Search Readiness snapshot offer.

---

## 7. Recommended Work Order

1. Archive `.bak` files.
2. Build sample report source file.
3. Build PDF pipeline and CSS.
4. Export sample PDF.
5. Build tracker spreadsheet and r06 doc.
6. Trim r05 so it captures signals only.
7. Create Neon Ronin r10 for scoring/strategy layer.
8. Write Fiverr gig copy.
9. Write buyer intake forms.
10. Write fulfillment SOP.
11. Build SearchClarity.co minimum viable site plan.
12. Produce Fiverr gallery/video assets.
13. Launch first Audit gig.

---

## 8. Core Decision From The Audit

SearchClarity comes first because it creates real customer workflows, real report data, and real market signals.

Neon Ronin should be shaped by what SearchClarity actually needs, not by abstract architecture guesses.

That means:

- SearchClarity captures the work.
- SearchClarity captures raw opportunity signals.
- Neon Ronin becomes the office/agent system that manages execution and strategy.
- Neon Ronin's Observatory scores opportunities across SearchClarity and future gig businesses.

The next move is execution, not another strategy pass.
