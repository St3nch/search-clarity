# Fiverr Platform Operations Research

## Status

```text
draft
```

## Purpose

This document captures the Fiverr-specific platform rules, constraints, operational risks, and SearchClarity implications for launching and running the first SearchClarity Fiverr gig.

This is a SearchClarity operations reference.

It is not final gig copy.

It is not Neon Ronin doctrine.

---

## Source Basis

Primary source for this draft:

```text
Claude Fiverr operational research report, May 2026
```

The report prioritized official Fiverr Help Center / Fiverr policy material where available and separated confirmed platform facts from seller-experience or third-party claims.

Any Fiverr rule that is not confirmed in the live Fiverr UI must be verified before publishing a gig.

---

## High-Level Summary

Fiverr can support SearchClarity's Etsy Listing Visibility Audit as a professional, human-reviewed PDF report service.

The platform constraints are workable, but they create several operating requirements:

- no outcome guarantees anywhere
- careful title choice before first publish because the gig URL slug is locked
- strong first three PDF pages because Fiverr only previews the first three pages of gallery PDFs
- clean buyer requirements because the order timer starts after requirements are submitted
- tight delivery/revision discipline because early seller performance matters
- all buyer communication must remain on Fiverr
- no Etsy login credentials should be requested

---

## Confirmed Fiverr Constraints

### Seller account and publishing

| Item | Confirmed rule / operating note |
|---|---|
| Account creation | Free; Fiverr does not require verification when opening an account unless triggered later |
| Account limit | One Fiverr account per person |
| Seller profile | Requires display name, profile photo/logo, professional title, bio, languages, skills, education/certifications as applicable |
| Desktop requirement | Gigs and freelancer accounts can only be created on desktop |
| ID verification | If triggered, Fiverr gives a 14-day completion window |
| Payout setup | PayPal, Payoneer, Bank Transfer through Payoneer, and Fiverr Revenue Card / Payoneer card handling |
| Commission | Fiverr takes 20% of every order |
| Earnings clearance | Usually 14 days; 7 days for Seller Plus, Top Rated, and Pro Talent |
| New Seller gig limit | Confirmed as 4 active gigs |
| First publish blockers | Missing tax form, unverified personal/business info, no required gallery image, VPN/ad-blocker/editor issues |

### Gig creation fields

| Field | Confirmed rule / operating note |
|---|---|
| Title | Mandatory `I will` prefix; up to 80 characters |
| Title URL slug | Slug is created at first publish and does not update if the title changes |
| Title banned characters | `&`, `/`, `"`, `+` are not allowed |
| Category | Required and cannot be changed after publish |
| Search tags | Up to 5 tags; each up to 20 characters |
| Description | Up to 1,200 characters |
| FAQs | Up to 10 FAQs; official blog says 300-character answer limit; UI may enforce 299 |
| Buyer requirements | Free Text, Multiple Answer, Attached File; mandatory or optional |
| Images | 1 required, up to 3; recommended 1280 x 769 px, JPG/PNG, up to 5 MB |
| Video | Up to 1 video, 75 seconds max; mp4 or AVI |
| PDFs | Up to 2 PDFs; only first 3 pages display in gallery |
| Packages | Up to 3 packages or one flat-rate gig |
| Revisions | 0-20 or Unlimited |
| Delivery file | Seller can deliver a single file up to 1 GB |

### Order lifecycle

Fiverr order flow for this service type should be treated as:

```text
Missing details / Requirements Needed
-> In Progress
-> Delivered
-> Revision Requested / In Revision, if applicable
-> Delivered again
-> Completed
```

Side states:

```text
Dispute
Late
Very Late
Cancelled
```

Important timing rules:

- The order timer starts after the buyer submits requirements.
- Seller can nudge the buyer when requirements are missing.
- The seller can skip requirements, but that starts the timer and should be used cautiously.
- Auto-completion occurs 3 days after delivery if the buyer does not request revision or accept manually.
- Extension requests can be sent from the order page; buyer has 48 hours to respond and non-response can auto-approve.
- Buyer can cancel after Late status rules are triggered.

---

## Compliance Rules For SearchClarity

SearchClarity must avoid outcome claims across all Fiverr assets.

Forbidden language examples:

```text
guaranteed page 1 ranking
guaranteed Etsy sales
boost your traffic by X%
rank higher in 7 days
increase revenue by X
get more orders guaranteed
```

Approved positioning:

```text
visibility audit
diagnostic findings
human-reviewed report
recommendations to test
listing visibility factors
Etsy SEO observations
clear action plan
no ranking or sales guarantees
```

Fiverr prohibits promises of outcomes outside the seller's control. SearchClarity must treat ranking, traffic, revenue, and sales as outside its control.

SearchClarity must not request Etsy login credentials for the Etsy Listing Visibility Audit. Public shop/listing URLs and optional Etsy Stats screenshots are enough for the first offer and reduce third-party platform risk.

All customer communication must stay on Fiverr.

---

## Recommended Fiverr Category

Use:

```text
Online Marketing > E-Commerce Marketing > E-Commerce SEO Services > Etsy
```

Before publishing, verify in the live Fiverr UI:

- exact standardized package fields
- category minimum prices
- service type options
- required metadata fields
- delivery-time dropdown options

---

## Initial Title Options

Preferred option:

```text
I will audit your Etsy listing SEO and visibility in a PDF
```

Reason:

- 58 characters
- includes Etsy, SEO, visibility, PDF
- avoids banned title characters
- does not promise rankings or sales

Alternate option:

```text
I will audit your Etsy listing visibility with a pro PDF report
```

Reason:

- clearer premium angle
- slightly longer display risk

Do not publish a title until the slug is approved because the URL slug is locked at first publish.

---

## Recommended Tags

Each tag is under 20 characters:

```text
etsy seo audit
etsy listing audit
etsy shop audit
etsy seo report
etsy listing review
```

Verify Fiverr's tag UI accepts each phrase before publishing.

---

## Recommended Package Structure

Provisional Fiverr launch structure:

| Element | Basic | Standard | Premium |
|---|---:|---:|---:|
| Listings audited | 1 | 3 | 5 |
| Keyword research depth | 10 keywords | 25 keywords | 50 keywords + competitor pull |
| Approx report length | 10 pages | 16 pages | 24 pages |
| Delivery | 3 days | 5 days | 7 days |
| Revisions | 1 | 1 | 2 |
| Provisional price | $45 | $95 | $185 |
| Loom walkthrough | No | No | Yes |

This is a Fiverr-specific launch candidate, not yet the final SearchClarity pricing source of truth.

Pricing must be reconciled against `docs/operations/pricing/pricing-source-of-truth.md` before publishing.

---

## Recommended Gig Extra

Candidate extra:

```text
7-day implementation check-in with Loom + checklist
Price: +$45
Adds: +3 days
```

Purpose:

- monetizes follow-up
- avoids unlimited support
- avoids guaranteeing implementation outcomes

---

## Recommended Buyer Requirements

Initial requirements should be 6-8 questions max.

| # | Question | Type | Required? |
|---:|---|---|---|
| 1 | What is your Etsy shop URL? | Free Text | Yes |
| 2 | Which 1-3 listings should I focus the audit on? Paste the URLs. | Free Text | Yes |
| 3 | What products do you sell? One or two sentences is enough. | Free Text | Yes |
| 4 | Who is your target buyer? | Free Text | Yes |
| 5 | What keywords do you currently believe matter for your shop? | Free Text | No |
| 6 | Optional: upload screenshots of Etsy Stats search terms from the last 30 days. | Attached File | No |
| 7 | Is this for a brand-new shop or established shop? | Multiple Answer | Yes |
| 8 | Are there listings you do not want me to review? | Free Text | No |

Do not ask for Etsy credentials.

---

## Recommended Gallery Assets

Required before publishing:

1. Image 1: thumbnail / main promise
2. Image 2: sample PDF spread or report preview
3. Image 3: what the audit checks
4. PDF sample: first three pages designed to sell

Optional but recommended:

- 60-75 second video
- second PDF showing a sample recommendation excerpt

The sample PDF's first three pages are extremely important because Fiverr only shows the first three pages in the gallery.

---

## Fiverr Unknowns To Verify In Live UI

These must be logged in `ui-verification-log.md`:

- buyer requirement prompt character cap
- buyer free-text answer cap
- buyer attached-file upload cap
- exact FAQ answer cap in current UI
- package description cap
- category-specific minimum price
- standardized package mandatory fields
- delivery-time dropdown options
- whether first gig has extra manual review delay
- whether verification is required before first publish
- exact gig metadata options in E-Commerce SEO Services > Etsy

---

## SearchClarity Operating Implications

Before publishing the first Fiverr gig, SearchClarity needs:

- finished Maplewood sample PDF
- first three pages of sample PDF designed for Fiverr preview
- outcome-guarantee language policy
- Etsy Listing Visibility Audit offer spec
- buyer requirements text
- Fiverr UI verification log
- order flow / delivery SOP
- QC checklist
- pricing source of truth
- revision and cancellation handling rules

---

## Non-Goals

This document does not:

- finalize Fiverr copy
- finalize pricing
- create customer intake forms
- define Neon Ronin workspace onboarding
- define agents or automation
- replace Fiverr UI verification

---

## Next Actions

1. Verify open UI unknowns inside Fiverr.
2. Lock outcome-guarantee language policy.
3. Lock Etsy Listing Visibility Audit offer spec.
4. Finish sample PDF and first three pages.
5. Draft buyer requirements.
6. Draft final Fiverr gig copy only after the above are stable.
