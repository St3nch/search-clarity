# SearchClarity Roadmap

## Purpose

This roadmap defines the current build plan for SearchClarity as a professional SEO/GEO/marketplace visibility report business.

SearchClarity is a customer-facing service business.

It sells human-reviewed, evidence-backed visibility reports and related services.

The first offer is the Etsy Listing Visibility Audit.

This roadmap is practical and execution-focused. It exists to prevent SearchClarity from becoming a pile of good ideas, half-finished docs, and launch assets that do not connect.

---

## Current Status

```text
status: pre-launch / operations-buildout
first_offer: Etsy Listing Visibility Audit
primary_launch_channel_candidate: Fiverr
secondary_channels_later: Upwork Project Catalog, SearchClarity.co, LinkedIn, direct sales
neon_ronin_status: later onboarding target, not current operating system
```

SearchClarity has strong strategy docs and a growing operations layer.

The current gap is execution: sample report, production assets, reviewed operations docs, fulfillment process, and launch package.

---

## Core Direction

SearchClarity should become a professional visibility report service, not a cheap keyword dump gig.

SearchClarity reports should be:

- human-reviewed
- evidence-backed
- caveated correctly
- specific and actionable
- professionally formatted
- clear about limitations
- free of fake ranking/sales promises
- reusable as proof assets where appropriate

---

## Relationship To Neon Ronin

SearchClarity is not Neon Ronin.

SearchClarity defines:

- customer-facing services
- buyer intake
- report products
- offer scope
- pricing
- customer delivery
- quality standards
- SearchClarity-specific records
- raw market signal capture during paid work

Neon Ronin later defines or supports:

- workspace onboarding
- platform records
- agent/runtime boundaries
- audit records
- review queues
- task/workflow execution
- Observatory scoring
- cross-business intelligence
- automation governance

Current rule:

```text
Build SearchClarity's manual business process first.
Let Neon Ronin generalize later from real evidence.
```

---

## Current Docs Inventory

### Root strategy/system docs

| File | Role | Current Status |
|---|---|---|
| `r00-searchclarity-overview.md` | Business overview and positioning | usable |
| `r01-searchclarity-launch-strategy.md` | Launch strategy and competitor context | usable but perishable |
| `r02-sample-report-spec.md` | Sample report specification | usable |
| `r03-first-5-gig-report-strategy-review.md` | First gig/service sequence | usable |
| `r04-comprehensive-seo-report-system.md` | Report system and QC concepts | usable |
| `r05-client-report-history-and-market-signal-capture.md` | Client history and signal capture | verify boundary scope |
| `r06-report-production-pipeline.md` | Report production pipeline spec | exists, needs execution |
| `r07-minimal-tracker-system.md` | Manual tracker spec | exists, not final operating system |
| `searchclarity-audit-2026-05-23.md` | Prior audit | reference only |
| `searchclarity-audit-action-list.md` | Prior action list | reference, partly superseded by this roadmap |

### Operations docs

The operations folder now exists:

```text
docs/operations/
```

It is the home for SearchClarity business-process docs.

These docs were recently drafted and must be reviewed before being treated as final.

| File | Role | Current Status |
|---|---|---|
| `docs/operations/README.md` | Operations folder structure and rules | draft, review needed |
| `docs/operations/fiverr/README.md` | Fiverr folder structure and rules | draft, review needed |
| `docs/operations/fiverr/platform-operations-research.md` | Fiverr platform rules and implications | draft from research, review needed |
| `docs/operations/fiverr/ui-verification-log.md` | Live Fiverr UI unknowns to verify | draft, needs live UI checks |
| `docs/operations/fiverr/manual-ui-verification-checklist.md` | Required manual Fiverr UI checks before publishing | draft, required before publish |
| `docs/operations/fiverr/buyer-requirements.md` | Draft Fiverr buyer intake questions | draft, review needed |
| `docs/operations/fiverr/order-flow-and-delivery-sop.md` | Fiverr-specific order/delivery SOP | draft, review needed |
| `docs/operations/fiverr/etsy-listing-visibility-audit-gig-setup.md` | Fiverr setup checklist for first gig | draft, review needed |
| `docs/operations/fiverr/gig-copy.md` | Draft Fiverr gig copy | draft, not ready to publish |
| `docs/operations/services/new-service-onboarding-checklist.md` | Reusable SearchClarity service/gig onboarding process | draft, review needed |
| `docs/operations/services/etsy-listing-visibility-audit-offer-spec.md` | First offer scope and package spec | draft, review needed |
| `docs/operations/quality-control/outcome-guarantee-language-policy.md` | Banned/approved claims language | draft, high priority review |
| `docs/operations/quality-control/qc-checklist.md` | Pre-delivery report QC checklist | draft, review needed |
| `docs/operations/fulfillment/order-fulfillment-sop.md` | General fulfillment SOP | draft, review needed |
| `docs/operations/pricing/pricing-source-of-truth.md` | Candidate pricing source of truth | draft, pricing decision needed |
| `docs/operations/records-and-consent/recordkeeping-and-consent.md` | Records and consent rules | draft, review needed |
| `docs/operations/website/README.md` | Website operations folder rules | draft, review needed |
| `docs/operations/website/searchclarity-co-website-plan.md` | SearchClarity.co website plan, stack, SEO/GEO/schema/blog strategy | draft, review needed |
| `docs/operations/website/searchclarity-co-website-roadmap.md` | Future dedicated website build roadmap | planned |
| `docs/operations/website/searchclarity-site-architecture.md` | Future sitemap, URL architecture, service/channel page structure | planned |
| `docs/operations/website/searchclarity-glossary-and-resource-plan.md` | Future glossary/resource plan for report terminology and explainer pages | planned |
| `docs/operations/website/searchclarity-report-to-website-linking-standard.md` | Future standard for linking report terms to public SearchClarity resources | planned |
| `docs/operations/brand-presence/README.md` | Brand presence operations folder rules | draft, review needed |
| `docs/operations/brand-presence/brand-and-external-presence-plan.md` | Branding, social profiles, external presence, and short-form distribution plan | draft, review needed |

---

## Roadmap Phases

## Phase 0 - Structure And Repo Hygiene

### Goal

Keep SearchClarity docs organized so new operational work does not become root-folder clutter.

### Status

```text
in_progress
```

### Completed

- Git repo exists.
- Root docs are numbered and mostly coherent.
- `docs/operations/` folder created.
- `docs/operations/fiverr/` folder created.
- Initial operations README files drafted.

### Remaining

- Review the operations folder structure.
- Decide whether to create additional empty folders now or only when docs are needed.
- Confirm whether root `rXX` docs remain strategy/system docs while operations docs live under `docs/operations/`.

### Exit Criteria

- Operations structure approved.
- No new operational docs are dumped into root without reason.
- Roadmap committed.

---

## Phase 1 - Draft Review And Consolidation

### Goal

Review the new operations drafts and turn them from raw drafts into usable internal operating references.

### Status

```text
not_started
```

### Docs To Review First

Priority review order:

1. `docs/operations/quality-control/outcome-guarantee-language-policy.md`
2. `docs/operations/services/etsy-listing-visibility-audit-offer-spec.md`
3. `docs/operations/pricing/pricing-source-of-truth.md`
4. `docs/operations/fiverr/platform-operations-research.md`
5. `docs/operations/fiverr/ui-verification-log.md`
6. `docs/operations/fiverr/buyer-requirements.md`
7. `docs/operations/fulfillment/order-fulfillment-sop.md`
8. `docs/operations/quality-control/qc-checklist.md`
9. `docs/operations/fiverr/order-flow-and-delivery-sop.md`
10. `docs/operations/fiverr/etsy-listing-visibility-audit-gig-setup.md`
11. `docs/operations/fiverr/gig-copy.md`
12. `docs/operations/records-and-consent/recordkeeping-and-consent.md`
13. `docs/operations/services/new-service-onboarding-checklist.md`

### Review Questions

For each draft, answer:

- Is it in the right folder?
- Is it SearchClarity-specific rather than Neon Ronin doctrine?
- Does it conflict with any root docs?
- Does it depend on unverified Fiverr UI assumptions?
- Does it contain unsafe ranking/sales language?
- Does it create unrealistic scope or delivery promises?
- Does it need to be split into separate docs?
- Does it need to be renamed?

### Exit Criteria

- Drafts reviewed.
- Critical conflicts resolved.
- Outcome-guarantee policy accepted as required review standard.
- Offer spec and pricing are aligned enough to continue production work.

---

## Phase 2 - First Offer Lock

### Goal

Lock the Etsy Listing Visibility Audit as the first SearchClarity offer.

### Status

```text
not_started
```

### Required Decisions

- Final package structure.
- Final launch pricing after Fiverr competitor research.
- Final delivery times.
- Final revision counts.
- Whether Premium prepares for a future short video report walkthrough.
- Whether a post-delivery follow-up/re-audit becomes a separate future service.
- Whether competitor observations are Standard or Premium only.
- Internal page-count guidance, with no public page-count promises unless deliberately approved later.
- What Basic includes without becoming underpriced custom consulting.

### Pricing Blocker

Pricing is not locked yet.

Manual Fiverr tier verification is required before final package prices are approved.

Reason:

- crawler/search research confirmed Basic/start prices better than full tier pricing
- Fiverr Standard/Premium tier details often require logged-in manual review
- early manual checks show large tier spread, such as Kristen around $120 Premium and Twocakes around $350 Premium
- SearchClarity should not launch at a price that looks weak, confused, or mispositioned against real package comparisons

Required manual data collection:

- capture competitor Basic/Standard/Premium prices
- capture package scope for each tier
- capture screenshots or PDF evidence where possible
- compare SearchClarity package-to-package before locking pricing

Until this is done, pricing remains:

```text
unresolved / pending manual Fiverr tier verification
```

### Pricing Principles To Confirm

- SearchClarity pricing should not be based only on production time.
- Pricing should reflect buyer value, report quality, human review, delivery polish, claim safety, and market positioning.
- Agent-assisted production may improve margins later, but it should not push SearchClarity into commodity pricing.
- Do not race to the $5-$20 Fiverr keyword-dump market.

### Required Docs

- `docs/operations/services/etsy-listing-visibility-audit-offer-spec.md`
- `docs/operations/pricing/pricing-source-of-truth.md`
- `docs/operations/quality-control/outcome-guarantee-language-policy.md`

### Companion Gig Notes

- Companion gigs require mini specs before launch.
- Candidate near-launch companion gigs: Etsy Title and Tag Rewrite, Etsy Keyword Research Pack.
- Candidate follow-up product: 60-90 Day Post-Implementation Visibility Review.
- Companion gigs may be ordered separately or work better after an audit, but they must not be buried inside the main audit package.

### Release List Work

- Pick which companion gigs are launch, near-launch, later, or parked.
- Build a release list once pricing/package scope is locked.
- Every launch or near-launch gig needs its own mini spec.

### Exit Criteria

- First offer scope is stable.
- Pricing is stable.
- Package table is stable.
- Out-of-scope boundaries are clear.
- Companion gig release-list decisions are recorded.
- No ranking/sales guarantees exist in offer language.

---

## Phase 3 - Sample Report Completion

### Goal

Finish the Maplewood Candle Co. sample report as the proof asset for SearchClarity's first offer.

### Status

```text
not_started
```

### Primary File

```text
docs/samples/maplewood-candle-co-listing-visibility-audit.md
```

### Required Work

- Review against `r02-sample-report-spec.md`.
- Review against `r04-comprehensive-seo-report-system.md`.
- Ensure report includes scope, methodology, executive summary, findings, recommendations, caveats, action plan, and next steps.
- Ensure major recommendations follow the preferred structure:

```text
Observation:
Why it matters:
Recommendation:
How to implement:
Caveat:
```

- Remove generic filler.
- Ensure no outcome guarantees.
- Ensure sample is clearly fictional.
- Add useful report visuals where they clarify findings, such as a priority matrix, keyword/theme coverage map, listing clarity scorecard, or competitor comparison table.
- Report visuals/graphs should explain observations, not imply fake precision.
- Ensure first three pages will sell the report when previewed on Fiverr.

### Exit Criteria

- Sample Markdown complete.
- QC pass complete.
- Ready for PDF production.

---

## Phase 4 - Report Production Pipeline

### Goal

Make SearchClarity able to produce professional PDFs consistently.

### Status

```text
not_started
```

### Primary File

```text
docs/r06-report-production-pipeline.md
```

### Required Work

- Decide final Markdown-to-PDF path.
- Build or refine stylesheet.
- Test export on Maplewood sample.
- Confirm PDF formatting.
- Define a report graph/visual standard.
- Confirm filenames and export locations.
- Confirm first three pages work as Fiverr gallery preview.

### Required Outputs

- finished sample PDF
- reusable report styling system
- export command/process
- first-pass report template compatibility

### Exit Criteria

- Maplewood sample exports cleanly.
- PDF is professional enough to show publicly.
- Production process is repeatable.

---

## Phase 5 - Fiverr Channel Preparation

### Goal

Prepare Fiverr as the first launch channel without rushing publication.

### Status

```text
not_started
```

### Required Docs

- `docs/operations/fiverr/platform-operations-research.md`
- `docs/operations/fiverr/ui-verification-log.md`
- `docs/operations/fiverr/manual-ui-verification-checklist.md`
- `docs/operations/fiverr/buyer-requirements.md`
- `docs/operations/fiverr/etsy-listing-visibility-audit-gig-setup.md`
- `docs/operations/fiverr/gig-copy.md`
- `docs/operations/fiverr/order-flow-and-delivery-sop.md`

### Required Work

- Create/prepare Fiverr account if proceeding.
- Verify live Fiverr UI constraints.
- Complete the manual Fiverr UI verification checklist or record blockers before publish.
- Record findings in UI verification log.
- Finalize title, tags, description, FAQ, packages, buyer requirements.
- Prepare gallery images.
- Prepare sample PDF upload.
- Decide whether to use video at launch or park it as a future Premium feature.
- Verify video walkthrough hosting/captions/transcript options.
- If video is used, require a recording outline, internal transcript, transcript/QC review, and captions or an equivalent accessible text option.
- Review all assets against outcome-guarantee policy.

### Exit Criteria

- Fiverr setup checklist complete.
- UI unknowns resolved or intentionally parked.
- Final gig copy is publish-ready.
- Gallery/sample assets are ready.
- Fulfillment SOP is ready.

---

## Phase 6 - Fulfillment And QC Dry Run

### Goal

Run a complete mock order using the Etsy Listing Visibility Audit workflow.

### Status

```text
not_started
```

### Dry Run Flow

```text
mock order
-> buyer requirements
-> intake review
-> manual observations
-> draft report
-> QC checklist
-> final PDF
-> delivery message
-> record update
-> raw signal capture review
-> closeout
```

### Required Docs

- `docs/operations/fulfillment/order-fulfillment-sop.md`
- `docs/operations/fiverr/order-flow-and-delivery-sop.md`
- `docs/operations/quality-control/qc-checklist.md`
- `docs/operations/records-and-consent/recordkeeping-and-consent.md`

### Exit Criteria

- Mock order can be completed end-to-end.
- QC checklist catches real issues.
- Delivery message works.
- Records needed are clear.
- Signal capture is understood.
- Any operational friction is logged.

---

## Phase 7 - Records, Consent, And Internal Learning Loop

### Goal

Make sure SearchClarity can keep enough records to support customers, improve services, and later provide clean evidence for Neon Ronin onboarding.

### Status

```text
not_started
```

### Required Work

- Review `recordkeeping-and-consent.md`.
- Decide temporary recordkeeping system before Neon Ronin onboarding.
- Define consent language for testimonials/case studies.
- Define raw signal capture rules.
- Decide what not to store.
- Decide retention expectations.

### Important Constraint

The old tracker workbook idea is not the final operating system.

A temporary manual record system may be used only as proof/evidence if needed.

SearchClarity's long-term operating records should later be supported through Neon Ronin or another deliberate system.

### Exit Criteria

- Order/report/customer record needs are clear.
- Consent rules are clear.
- Raw signal capture is clear.
- No customer-private data is used publicly without consent.

---

## Phase 8 - Launch Readiness Review

### Goal

Decide whether SearchClarity is ready to publish the first Fiverr gig or remain in preparation.

### Status

```text
not_started
```

### Launch Readiness Checklist

SearchClarity is launch-ready only when:

- [ ] first offer is locked
- [ ] pricing is locked
- [ ] sample report is finished
- [ ] sample PDF is exported
- [ ] Fiverr first three PDF pages are strong
- [ ] gallery images are ready
- [ ] buyer requirements are final
- [ ] fulfillment SOP is final enough
- [ ] QC checklist is usable
- [ ] outcome-guarantee language policy is applied
- [ ] Fiverr UI unknowns are verified or logged
- [ ] records/consent process is defined
- [ ] revision/refund/cancellation handling is defined
- [ ] final gig copy is reviewed
- [ ] owner intentionally approves publication

### Exit Criteria

Decision recorded:

```text
publish / do_not_publish_yet / private_test_first / park
```

---

## Phase 9 - First Orders / Manual Business Proof

### Goal

Use the first real orders to prove the SearchClarity business workflow manually.

### Status

```text
not_started
```

### First 5 Orders Focus

The first orders are not just revenue.

They are proof of:

- buyer clarity
- intake quality
- production time
- report usefulness
- revision patterns
- pricing fit
- recordkeeping needs
- raw signal capture opportunities
- future Neon Ronin onboarding requirements

### Required Tracking

For each early order, record:

- package purchased
- production time
- revision requests
- buyer questions
- delivery friction
- QC issues
- feedback/review themes
- raw signals noticed
- improvement actions

### Exit Criteria

After 3-5 orders:

- revise offer if needed
- revise intake if needed
- revise SOP if needed
- revise QC if needed
- revise pricing if needed
- identify what Neon Ronin would need to support

---

## Phase 10 - SearchClarity.co Trust Hub

### Goal

Build SearchClarity.co as a credibility and proof hub after the first offer/proof assets are strong enough.

### Status

```text
not_started
```

### Minimum Site Pages

- Home
- Services
- Etsy Listing Visibility Audit
- Sample Report
- Methodology
- About
- Contact
- Privacy / Terms

### Required Docs

- `docs/operations/website/searchclarity-co-website-plan.md`
- `docs/operations/website/searchclarity-co-website-roadmap.md` later
- `docs/operations/website/searchclarity-site-architecture.md` later
- `docs/operations/website/searchclarity-glossary-and-resource-plan.md` later
- `docs/operations/website/searchclarity-report-to-website-linking-standard.md` later
- `docs/operations/quality-control/outcome-guarantee-language-policy.md`
- `docs/operations/services/etsy-listing-visibility-audit-offer-spec.md`
- `docs/operations/pricing/pricing-source-of-truth.md`
- `docs/operations/records-and-consent/recordkeeping-and-consent.md`

### Required Inputs

- finished sample PDF
- final offer positioning
- outcome-guarantee language policy
- pricing decision
- founder/brand identity decision
- consent/testimonial policy
- website stack/hosting decision
- initial sitemap and entity architecture
- analytics/Search Console plan
- report-to-website linking approach
- glossary/resource page plan
- website sub-roadmap

### Exit Criteria

- website explains what SearchClarity does
- website shows proof
- website avoids fake promises
- website supports Fiverr/direct trust

---

## Phase 10.5 - Branding And External Presence

### Goal

Define SearchClarity brand assets, social profiles, external presence, and short-form distribution without turning the roadmap into a brand guide.

### Status

```text
not_started
```

### Required Doc

- `docs/operations/brand-presence/brand-and-external-presence-plan.md`

### Scope

- logo/avatar/banner requirements
- LinkedIn, YouTube, X/Twitter, Instagram, and TikTok presence planning
- YouTube-first short-form video republishing model for Reels/TikTok
- optional later channels such as Substack, Reddit, Medium, Pinterest, and Product Hunt
- consistent entity language pointing back to SearchClarity.co

### Exit Criteria

- brand asset requirements are defined
- priority profiles/handles are reserved or intentionally parked
- external profiles link back to SearchClarity.co
- short-form video distribution model is understood
- no external channel becomes the canonical home instead of SearchClarity.co

---

## Phase 11 - Future Services

### Future AI/GEO Service Homework

Potential future services to research after launch path stabilizes:

- AI Search / LLM Visibility Readiness Audit
- GEO Mentions And Citations Readiness Audit
- Ecommerce AI Visibility Snapshot
- Schema / Structured Data Readiness Audit
- Entity Footprint Review

Rules:

- Do not guarantee AI mentions, citations, rankings, or inclusion.
- Define what can actually be observed before selling the service.
- Research tools/data sources and competitor pricing before writing gig copy.
- Treat this as future SearchClarity service planning, not Neon Ronin platform doctrine.


### Goal

Use the new-service onboarding checklist to add services deliberately.

### Status

```text
not_started
```

### Candidate Future Services

- Etsy Title and Tag Rewrite
- Etsy Keyword Research Pack
- Etsy Competitor Visibility Observations Report
- Etsy Shop Visibility Report
- Pinterest SEO Plan for Etsy Sellers
- Shopify Product Page SEO Audit
- Schema / Structured Data Readiness Audit
- AI Search / LLM Visibility Readiness Snapshot
- Seller Visibility Strategy Report

### Rule

No future service is published until it passes:

```text
docs/operations/services/new-service-onboarding-checklist.md
```

### Exit Criteria

- each new service has offer spec
- channel fit is clear
- pricing is clear
- intake is clear
- fulfillment is clear
- QC is clear
- sample/proof asset exists if needed

---

## Phase 12 - Neon Ronin Compatibility Evidence

### Goal

Prepare clean evidence for later Neon Ronin compatibility/onboarding work.

### Status

```text
not_started
```

### Evidence SearchClarity Should Produce First

- real service workflow
- offer spec
- intake requirements
- report artifact shape
- QC/review process
- delivery process
- recordkeeping needs
- raw signal capture examples
- consent/public-use requirements
- manual proof from early orders

### Important Rule

Do not make Neon Ronin generalize from guesses.

Let Neon Ronin generalize from SearchClarity evidence after SearchClarity proves the manual business process.

---

## Blocked / Not Working Yet

The following are not current priorities:

- full Neon Ronin onboarding
- SearchClarity automation
- executable agents
- third-party SERP/eRank/DataForSEO integrations
- complex database buildout
- full SearchClarity.co build before sample proof
- paid ad strategy
- large content marketing plan
- AI Search Readiness full report product
- multiple Fiverr gigs before first gig proof

---

## Immediate Next Work Queue

| Priority | Task | Output |
|---:|---|---|
| P0 | Review new operations drafts | Approved/edited operations docs |
| P0 | Lock outcome-guarantee language policy | Safe claims standard |
| P0 | Lock Etsy Audit offer spec | Final first-offer scope |
| P0 | Reconcile pricing | Final launch pricing table |
| P0 | Finish Maplewood sample report | Complete Markdown sample |
| P0 | Export sample PDF | Public proof asset |
| P1 | Verify Fiverr UI constraints | Completed UI verification log |
| P1 | Finalize buyer requirements | Publish-ready Fiverr intake |
| P1 | Finalize QC checklist | Usable pre-delivery gate |
| P1 | Finalize fulfillment SOP | Repeatable order workflow |
| P1 | Finalize Fiverr gig copy | Publish-ready copy |
| P2 | Prepare gallery images/video | Fiverr proof assets |
| P2 | Launch readiness review | Publish/no-publish decision |
| P2 | Define branding/social asset requirements | Roadmap section or future brand-presence doc |
| P2 | Reserve priority external profiles/handles | LinkedIn, YouTube, X, Instagram, TikTok |

---

## Definition Of Launch-Ready

SearchClarity is launch-ready for the first Fiverr gig when:

```text
sample report is finished
sample PDF is polished
first offer is scoped
pricing is final
Fiverr UI constraints are verified
buyer requirements are final
fulfillment SOP exists
QC checklist exists
outcome policy is applied
records/consent process is clear
final gig copy and assets are ready
branding basics are defined
priority external profiles/handles are reserved or intentionally parked
owner approves publishing
```

Until then, SearchClarity remains in pre-launch operations buildout.

---

## Final Principle

```text
Build the proof asset.
Prove the workflow.
Then publish.
Then learn from real orders.
Then let Neon Ronin generalize from evidence.
```
