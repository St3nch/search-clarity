# Etsy Listing Visibility Audit Offer Spec

## Status

```text
draft
```

## Purpose

This document defines the SearchClarity Etsy Listing Visibility Audit offer.

It is the source of truth for the first SearchClarity paid service before channel-specific copy is finalized.

Channel-specific versions, such as Fiverr gig setup, must reference this offer spec instead of inventing their own scope.

---

## Offer Summary

The Etsy Listing Visibility Audit is a human-reviewed SEO and marketplace visibility report for Etsy sellers.

The audit reviews visible listing/shop factors and gives specific recommendations to improve clarity, keyword coverage, buyer alignment, and marketplace readiness.

The audit does not guarantee rankings, traffic, sales, revenue, or Etsy placement.

---

## Target Customer

Primary customer:

```text
Etsy sellers who want a professional review of listing visibility and SEO factors without buying a cheap keyword dump.
```

Good-fit buyers:

- handmade sellers
- personalized gift sellers
- digital download sellers
- print-on-demand sellers
- small shops with unclear titles/tags/descriptions
- sellers who want practical recommendations before rewriting listings
- sellers who understand recommendations are not guarantees

Poor-fit buyers:

- buyers demanding guaranteed sales or rankings
- sellers selling counterfeit or trademark-risky products
- sellers who want fake reviews, manipulation, or blackhat tactics
- sellers who refuse to provide usable listing/shop URLs
- sellers who want SearchClarity to log into Etsy for them

---

## Core Deliverable

A PDF report containing:

- scope and methodology
- executive summary
- listing/title/tag/description observations
- keyword coverage observations
- buyer intent and clarity notes
- competitive context observations, where included
- prioritized recommendations
- implementation guidance
- caveats and next steps

The report should be specific enough for the seller to act on without guessing.

---

## Package Structure Candidate

This is the current Fiverr launch candidate. Final pricing must be reconciled in `docs/operations/pricing/pricing-source-of-truth.md` before publishing.

| Element | Basic | Standard | Premium |
|---|---:|---:|---:|
| Listings audited | 1 | 3 | 5 |
| Keyword research depth | 10 keywords | 25 keywords | 50 keywords + competitor pull |
| Approx report length | 10 pages | 16 pages | 24 pages |
| Delivery | 3 days | 5 days | 7 days |
| Revisions | 1 | 1 | 2 |
| Provisional price | $45 | $95 | $185 |
| Loom walkthrough | No | No | Yes |

Hero tier:

```text
Standard
```

Reason:

Standard gives enough scope to show real value without overloading production time.

---

## Included Analysis Areas

Depending on package scope, the report may include:

- title structure
- tag set review
- description clarity
- keyword phrase coverage
- buyer language alignment
- product positioning clarity
- attribute/category observations if visible
- photo/thumbnail visibility notes if relevant
- competitor listing pattern observations
- shop trust/policy observations if relevant
- action plan with priorities

---

## Out Of Scope

This service does not include:

- guaranteed rankings
- guaranteed sales
- guaranteed traffic
- direct Etsy account login
- listing implementation inside Etsy
- paid ad setup
- Etsy Ads management
- fake reviews
- competitor copying
- trademark-risky keyword bait
- legal/IP advice
- full shop branding strategy
- product photography editing
- full copywriting rewrite unless included in a separate service
- ongoing SEO management

---

## Buyer Inputs Required

Minimum required intake:

- Etsy shop URL
- listing URL(s) in scope
- short description of products sold
- target buyer or buyer context
- shop age or stage

Optional helpful inputs:

- current target keywords
- Etsy Stats screenshots
- specific concerns
- competitor listings buyer admires
- listings to avoid reviewing

SearchClarity should not request Etsy login credentials.

---

## Data And Observation Sources

Current state:

- manual review of public Etsy shop/listing pages
- manual review of visible title, tags where available/provided, description, images, policies, and shop context
- manual marketplace/search observations
- customer-provided screenshots if supplied
- public Etsy guidance where relevant

Future/deferred:

- eRank
- DataForSEO
- Etsy API
- Google Trends
- Pinterest Trends
- other third-party tools

Third-party or automated data pulls are not required for the first Fiverr version.

---

## Recommendation Standard

Major recommendations should generally use this structure:

```text
Observation:
Why it matters:
Recommendation:
How to implement:
Caveat:
```

Recommendations must be:

- specific
- actionable
- tied to the observed listing/shop context
- free of fake precision
- caveated where platform outcomes are uncertain
- compliant with the outcome-guarantee language policy

---

## Caveat Standard

Every report must include caveats that explain:

- Etsy rankings and sales are not guaranteed
- recommendations are based on visible factors and available information
- marketplace behavior can change
- buyer behavior, product fit, pricing, reviews, shipping, and photos also affect performance
- the seller is responsible for deciding what to implement

---

## QC Requirements

Before delivery:

- [ ] Correct package scope followed
- [ ] Correct listings reviewed
- [ ] No ranking/sales/traffic guarantees
- [ ] Recommendations are specific and actionable
- [ ] Caveats included
- [ ] No trademark-risky keyword recommendations
- [ ] No off-platform contact language
- [ ] Report is professionally formatted
- [ ] PDF/export opens correctly
- [ ] Delivery message is clear and on-scope

---

## Records Created

Each order should create or update records for:

- customer/order
- intake response
- listing/property reviewed
- report artifact
- QC result
- delivery message
- revision request, if any
- raw market signal, if a generalizable pattern appears
- consent, if buyer allows public use/testimonial/case study

---

## Raw Signal Capture

During the audit, analysts may notice generalizable patterns such as:

- repeated weak title structure in a niche
- unclear buyer language patterns
- keyword clusters with strong intent
- competitor listing gaps
- product category opportunities
- AI/search readiness gaps

SearchClarity captures raw signals only.

SearchClarity does not score opportunities.

Customer-identifying details must be removed from generalized notes.

---

## Launch Readiness Requirements

This offer is not ready to publish until:

- sample Maplewood report is finished
- sample PDF is exported
- first three PDF pages are Fiverr-gallery-ready
- pricing source of truth is reconciled
- Fiverr buyer requirements are written
- Fiverr gig copy is drafted and checked
- QC checklist is finalized
- fulfillment SOP is written
- Fiverr UI unknowns are verified or logged
- outcome-guarantee policy is applied to all assets

---

## Non-Goals

This spec does not:

- finalize Fiverr copy
- replace the fulfillment SOP
- replace the QC checklist
- define Neon Ronin workspace onboarding
- define database records
- approve third-party integrations

---

## Open Decisions

- Final launch pricing
- Whether Premium includes Loom by default
- Whether to include a gig extra for 7-day implementation check-in
- Whether to include competitor observations in Standard or only Premium
- Whether Basic should be shorter than 10 pages
- Final page count promises for each package
