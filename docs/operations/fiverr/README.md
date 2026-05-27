# Fiverr Operations

## Purpose

This folder contains SearchClarity's Fiverr-specific operating documents.

Use this folder for Fiverr platform rules, gig setup, Fiverr buyer requirements, Fiverr delivery flow, Fiverr UI verification, and Fiverr-specific copy assets.

Fiverr is SearchClarity's likely first launch channel, but it is not the only future channel.

This folder should not become the whole SearchClarity operations system.

---

## What Belongs Here

Use this folder for:

- Fiverr platform operations research
- Fiverr seller profile setup notes
- Fiverr gig setup requirements
- Fiverr category and package rules
- Fiverr UI verification logs
- Fiverr buyer requirements text
- Fiverr order lifecycle notes
- Fiverr delivery and revision handling
- Fiverr cancellation/dispute handling
- Fiverr gig gallery asset requirements
- Fiverr-specific gig copy
- Fiverr-specific compliance notes

---

## What Does Not Belong Here

Do not put these here:

- universal SearchClarity service onboarding rules
- general order fulfillment SOPs that apply across all channels
- SearchClarity-wide QC policy
- SearchClarity-wide pricing source of truth
- SearchClarity-wide recordkeeping and consent policy
- Neon Ronin doctrine
- database architecture
- agent runtime design
- raw customer files
- delivered customer reports
- exported PDFs

Those belong in other operations folders or outside `docs/operations`.

---

## Recommended Files

Near-term Fiverr files:

```text
platform-operations-research.md
ui-verification-log.md
etsy-listing-visibility-audit-gig-setup.md
gig-copy.md
buyer-requirements.md
order-flow-and-delivery-sop.md
```

---

## Relationship To General Operations

Fiverr-specific docs should reference general SearchClarity operations docs when needed.

Examples:

| Fiverr-specific doc | Should reference general doc |
|---|---|
| `buyer-requirements.md` | `../services/etsy-listing-visibility-audit-offer-spec.md` |
| `gig-copy.md` | `../quality-control/outcome-guarantee-language-policy.md` |
| `order-flow-and-delivery-sop.md` | `../fulfillment/order-fulfillment-sop.md` |
| `etsy-listing-visibility-audit-gig-setup.md` | `../pricing/pricing-source-of-truth.md` |

Fiverr docs explain how SearchClarity operates on Fiverr.

General operations docs define SearchClarity's reusable business process.

---

## Operating Rule

Do not publish or update a Fiverr gig unless this folder contains the current Fiverr-specific setup details and the related general SearchClarity operations docs are consistent.

At minimum, a Fiverr gig should have:

- platform rules checked
- offer scope locked
- package/pricing checked
- buyer requirements written
- outcome-guarantee language reviewed
- proof/sample assets ready
- delivery and revision process defined
- UI unknowns logged or resolved
