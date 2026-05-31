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
Claude Fiverr operational research reports, May 2026
```

The reports prioritized official Fiverr Help Center / Fiverr policy material where available and separated confirmed platform facts from seller-experience, live-listing observation, third-party claims, or unresolved UI unknowns.

Any Fiverr rule that is not confirmed in the live Fiverr UI must be verified before publishing a gig.

---

## High-Level Summary

Fiverr can support SearchClarity's Etsy Listing Visibility Audit as a professional, human-reviewed PDF report service.

The platform constraints are workable, but they create several operating requirements:

- no outcome guarantees anywhere
- careful title choice before first publish because the gig URL slug is locked
- correct category choice before first publish because category cannot be changed after publish
- strong first three PDF pages because Fiverr only previews the first three pages of gallery PDFs
- clean buyer requirements because the order timer starts after requirements are submitted
- tight delivery/revision discipline because early seller performance matters
- all buyer communication must remain on Fiverr
- no Etsy login credentials should be requested
- no external website/sample-report links should appear on the launch gig page or gallery assets
- video should be launch-candidate only if polished enough to outperform Image 1

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
| DSA / personal-business verification | May be required before publishing / for EU visibility; complete before launch if prompted |
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
| FAQs | Up to 10 FAQs; answer cap must be verified in live UI |
| Buyer requirements | Free Text, Multiple Answer, Attached File; mandatory or optional |
| Buyer requirement count/limits | No official cap found; must be tested in live UI |
| Images | 1 required, up to 3; recommended 1280 x 769 px, JPG/PNG, up to 5 MB |
| Image text | Fiverr image guidance says 10 words or fewer per image |
| Video | Up to 1 video; current guidance recommends 20-60 seconds; older/technical limit references may mention 75 seconds |
| Video file | mp4 or AVI, under live-verified file cap; no contact info |
| PDFs | Up to 2 PDFs; only first 3 pages display in gallery |
| Packages | Up to 3 packages or one flat-rate gig |
| Revisions | 0-20 or Unlimited in some Fiverr/custom-offer contexts; SearchClarity should avoid unlimited revisions |
| Delivery file | Seller can deliver a single file up to 1 GB; large files may use allowed third-party delivery links where appropriate |

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
- Buyer can cancel after Late / Very Late status rules are triggered.

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

For launch, do not place external website/sample-report links on the gig page, in gallery images, in QR codes, or inside gallery assets. Use Fiverr-native proof assets instead.

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

Category cannot be changed after publish. Do not publish until the selected category/subcategory is approved.

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

Pricing is unresolved and blocked pending manual competitor tier verification and live category minimum-price verification.

```text
pricing_status: unresolved / pending manual Fiverr tier verification
```

Candidate package scope:

| Element | Basic | Standard | Premium |
|---|---:|---:|---:|
| Listings audited | 1 | Up to 3 | Up to 5 |
| Primary deliverable | PDF audit | PDF audit | PDF audit |
| Keyword/theme observations | Focused | Expanded | Deeper + competitor/context where scoped |
| Competitor/context observations | No or light | Light where relevant | Included where relevant |
| Video walkthrough | No | No | Future candidate only |
| Revisions | 1 clarification revision | 1 clarification revision | 1 clarification revision |
| Price | Pending | Pending | Pending |

Do not use public page-count promises unless deliberately approved in the offer spec and pricing source of truth.

Do not publish pricing until it is reconciled against `docs/operations/pricing/pricing-source-of-truth.md`.

---

## Follow-Up Services And Gig Extras

No launch gig extra is approved yet.

Do not use the old implementation follow-up extra.

The 60-90 Day Post-Implementation Visibility Review is a future separate gig or custom-offer candidate, not an add-on inside the original audit order.

Reason:

- Fiverr orders auto-complete after the review window.
- Keeping an original order open for 60-90 days is mechanically incompatible with normal Fiverr order flow.
- A delayed review needs separate scope, deadline, and buyer inputs.

---

## Recommended Buyer Requirements

The ideal buyer-requirements doc contains more fields than may be practical for launch.

Launch posture:

- keep the full ideal intake documented internally
- verify actual Fiverr requirement count and character limits in live UI
- publish a trimmed 5-7 mandatory-question version if the ideal set creates too much friction

Possible launch-required fields:

| # | Question | Type | Required? |
|---:|---|---|---|
| 1 | What is your Etsy shop URL? | Free Text | Yes |
| 2 | Which listing(s) should I review? Paste the URLs. | Free Text | Yes |
| 3 | What products do you sell? One or two sentences is enough. | Free Text | Yes |
| 4 | Who is your target buyer? | Free Text | Yes |
| 5 | What is your main goal for this audit? | Free Text or Multiple Answer | Yes |
| 6 | Optional: what keywords/search phrases do you think matter? | Free Text | No |
| 7 | Optional: upload Etsy Stats screenshots if privacy-safe. | Attached File | No |

Do not ask for Etsy credentials.

---

## Recommended Gallery Assets

Required before publishing:

1. Image 1: main thumbnail / polished report-cover mockup
2. Image 2: labeled sample PDF preview/page spread
3. Image 3: package or audit-scope graphic
4. PDF sample: first three pages designed to sell

Optional / launch candidate:

- 40-50 second gig video only if more polished than Image 1
- second PDF sample excerpt if useful later

The sample PDF's first three pages are extremely important because Fiverr only shows the first three pages in the gallery.

Recommended first three PDF pages:

| Page | Purpose |
|---|---|
| 1 | Branded cover with clear SAMPLE / illustrative-data label |
| 2 | Executive summary showing specific, non-generic findings |
| 3 | Priority action plan, preferably with effort/impact matrix |

Gallery asset rules:

- image text should stay at or below 10 words per image
- image/PDF filenames should use relevant keywords before upload
- no external URLs
- no QR codes
- no contact information
- no fake Fiverr badges or ratings
- no ranking/sales/traffic guarantees
- no stock-photo sludge
- sample/fictional report content must be clearly labeled

### Gig Video Posture

A gig video may become the main cover media in search/results. Do not upload video unless it is more polished than Image 1.

If used:

- target 40-50 seconds
- verify current video limits in Fiverr UI
- show the Maplewood sample report
- include no external URLs, QR codes, contact info, or guarantee language
- keep it separate from customer-specific report walkthrough deliverables

---

## Fiverr Unknowns To Verify In Live UI

These must be logged in `ui-verification-log.md`:

- buyer requirement question-count cap
- buyer requirement prompt character cap
- buyer free-text answer cap
- buyer attached-file upload cap
- exact FAQ answer cap in current UI
- package description cap
- category-specific minimum price
- standardized package mandatory fields
- delivery-time dropdown options
- revision-count dropdown options
- whether first gig has extra manual review delay
- whether verification is required before first publish
- exact gig metadata options in E-Commerce SEO Services > Etsy
- current gig video length/file-size limits
- whether video upload changes the visible cover media in current UI

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
- gallery images with 10 words or fewer each
- no external website/sample-report links on gig page or gallery assets

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
4. Finish Maplewood sample PDF and first three preview pages.
5. Draft buyer requirements launch version after UI verification.
6. Draft final Fiverr gig copy only after the above are stable.
