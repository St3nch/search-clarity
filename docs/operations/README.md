# SearchClarity Operations Docs

## Purpose

This folder contains SearchClarity business-operation documents.

Use this folder for practical processes, playbooks, checklists, operating rules, and channel-specific procedures that help SearchClarity create, sell, fulfill, review, and improve paid services.

This is SearchClarity-owned material.

It is not Neon Ronin doctrine.

---

## Folder Structure

Recommended structure:

```text
docs/operations/
  README.md
  fiverr/
  marketplaces/
  services/
  fulfillment/
  quality-control/
  records-and-consent/
  pricing/
  website/
```

Current active channel folder:

```text
docs/operations/fiverr/
```

Use channel-specific folders for platform rules and setup details.

Use general operations folders for SearchClarity processes that apply across channels.

---

## Channel-Specific vs General Operations

### Channel-specific docs

Channel-specific docs belong under a platform/channel folder such as:

```text
docs/operations/fiverr/
docs/operations/upwork/
docs/operations/searchclarity-co/
docs/operations/linkedin/
```

Use these for:

- platform field limits
- marketplace rules
- profile setup
- gig/project/listing setup
- channel-specific buyer requirements
- channel-specific delivery flow
- channel-specific revision/dispute rules
- platform UI verification logs
- channel-specific copy assets

### General SearchClarity operations docs

General operations docs should live in topic folders such as:

```text
docs/operations/services/
docs/operations/fulfillment/
docs/operations/quality-control/
docs/operations/records-and-consent/
docs/operations/pricing/
docs/operations/website/
```

Use these for:

- reusable new-service onboarding
- offer/package design
- report fulfillment process
- QC/review rules
- outcome-guarantee language policy
- pricing source of truth
- consent/testimonial/case-study handling
- customer/report recordkeeping
- post-order improvement loops

---

## What Belongs Here

Use this folder for docs such as:

- platform/channel operations research
- new gig/service onboarding workflow
- offer/package setup checklists
- buyer intake process
- order fulfillment SOPs
- QC/review checklists
- revision/refund/dispute handling
- pricing source-of-truth notes
- consent/testimonial/case-study handling
- delivery message standards
- post-order improvement loops
- business records and operational logging rules
- platform UI verification logs

---

## What Does Not Belong Here

Do not put the following in this folder:

- Neon Ronin platform doctrine
- Neon Ronin universal workspace onboarding rules
- agent runtime architecture
- database architecture
- Observatory scoring models
- cross-business strategy queues
- generic multi-business operating doctrine
- raw customer files
- delivered customer reports
- exported PDFs

Those belong elsewhere.

---

## Relationship To Root SearchClarity Docs

The numbered root docs define major SearchClarity strategy, report system, history/signal capture, and production concepts.

This folder holds the operational documents that make those concepts usable in day-to-day work.

Root docs should remain relatively stable.

Operational docs can change as SearchClarity learns from real orders, platform UI checks, customer questions, revisions, delivery friction, and channel rules.

---

## Relationship To Neon Ronin

SearchClarity operations docs may later provide evidence for Neon Ronin workspace onboarding.

However:

```text
SearchClarity operations define how SearchClarity works.
Neon Ronin doctrine defines how the platform supports many workspaces.
```

Do not promote SearchClarity-specific process details into Neon Ronin core unless they pass a separate reusable-capability review.

---

## Suggested Initial Docs

### Fiverr channel docs

```text
docs/operations/fiverr/platform-operations-research.md
docs/operations/fiverr/ui-verification-log.md
docs/operations/fiverr/etsy-listing-visibility-audit-gig-setup.md
docs/operations/fiverr/gig-copy.md
docs/operations/fiverr/buyer-requirements.md
docs/operations/fiverr/order-flow-and-delivery-sop.md
```

### General SearchClarity operations docs

```text
docs/operations/services/new-service-onboarding-checklist.md
docs/operations/services/etsy-listing-visibility-audit-offer-spec.md
docs/operations/quality-control/outcome-guarantee-language-policy.md
docs/operations/quality-control/qc-checklist.md
docs/operations/fulfillment/order-fulfillment-sop.md
docs/operations/records-and-consent/recordkeeping-and-consent.md
docs/operations/pricing/pricing-source-of-truth.md
```

These filenames are intentionally not root-level `rXX` docs. They are operational assets.

---

## Operating Rule

No new SearchClarity gig/service should be published until its operations docs answer:

- what is being sold
- who it is for
- what the buyer must provide
- what SearchClarity delivers
- how the work is fulfilled
- what QC checks are required
- what claims are forbidden
- what records are kept
- what raw signals may be captured
- what is out of scope
- what must be verified in the sales platform UI

If those answers are missing, the gig is not ready.
