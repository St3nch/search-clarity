# Fiverr Manual UI Verification Checklist

## Status

```text
draft / required_before_publish
```

## Purpose

This checklist captures the Fiverr items that must be verified manually in the live Fiverr seller UI before SearchClarity publishes the Etsy Listing Visibility Audit gig.

It complements:

```text
ui-verification-log.md
etsy-listing-visibility-audit-gig-setup.md
platform-operations-research.md
```

The UI verification log records results.

This checklist defines what must be checked.

---

## Core Rule

```text
Do not publish the Fiverr gig until every launch-blocking manual UI check is confirmed or explicitly recorded as a blocker.
```

If a Fiverr field, limit, category, package setting, or asset behavior cannot be confirmed from official docs, verify it in the live UI before relying on it.

---

## Verification Status Values

Use these values when recording results in `ui-verification-log.md`:

```text
not_checked
confirmed
changed_from_research
not_visible_in_ui
blocked_by_account_status
needs_recheck
```

---

## Launch-Blocking Checks

These checks block publishing until resolved.

| Area | Check | Why It Matters | Result Location |
|---|---|---|---|
| Seller account | Confirm seller account can create gigs from desktop | Fiverr requires desktop gig creation | `ui-verification-log.md` |
| Seller verification | Confirm whether personal/business/DSA verification is required before publish | Verification can block publication or visibility | `ui-verification-log.md` |
| Category | Confirm exact category path exists | Category cannot be changed after publish | `ui-verification-log.md` |
| Category | Confirm exact Etsy/E-Commerce SEO subcategory options | Wrong category could damage discoverability and package fields | `ui-verification-log.md` |
| Category | Confirm category-specific minimum price | Pricing is blocked until UI and competitor pricing are verified | `ui-verification-log.md` |
| Package fields | Confirm standardized package fields for the chosen category | Package table must match what Fiverr actually allows | `ui-verification-log.md` |
| Package descriptions | Confirm package description character limit | Final package copy must fit | `ui-verification-log.md` |
| Delivery | Confirm delivery-time dropdown options | Delivery promises must match allowed values | `ui-verification-log.md` |
| Revisions | Confirm revision-count dropdown options | Revision policy must match package UI | `ui-verification-log.md` |
| Buyer requirements | Confirm max number of requirement questions if any | Ideal intake may be too long | `ui-verification-log.md` |
| Buyer requirements | Confirm prompt character limits | Requirement prompts must fit without losing clarity | `ui-verification-log.md` |
| Buyer requirements | Confirm free-text answer behavior/limits if visible | Intake quality affects fulfillment | `ui-verification-log.md` |
| Buyer requirements | Confirm attached-file requirement behavior | Etsy Stats screenshots may be optional | `ui-verification-log.md` |
| Buyer requirements | Confirm mandatory vs optional settings behave correctly | Timer and scope depend on required fields | `ui-verification-log.md` |
| Gallery image | Confirm image upload size/format behavior | Assets must upload cleanly | `ui-verification-log.md` |
| Gallery PDF | Confirm sample PDF upload behavior | Sample PDF is a core proof asset | `ui-verification-log.md` |
| Gallery PDF | Confirm first 3 pages display as expected | First 3 pages must sell the report | `ui-verification-log.md` |
| Gallery video | Confirm current video upload limits | Video is launch-candidate only if compliant | `ui-verification-log.md` |
| Gallery video | Confirm whether uploaded video becomes search/gallery cover media | Bad video could hurt first impression | `ui-verification-log.md` |
| Title | Confirm title is accepted and slug-safe | URL slug locks at first publish | `ui-verification-log.md` |
| Tags | Confirm all 5 tags are accepted | Tags affect discoverability | `ui-verification-log.md` |
| Description | Confirm 1,200 character limit and formatting behavior | Final copy must fit and read cleanly | `ui-verification-log.md` |
| FAQs | Confirm FAQ answer limits | Scope/no-guarantee FAQs must fit | `ui-verification-log.md` |

---

## Pricing Verification Checks

Pricing remains blocked until manual competitor tier verification and live UI verification are complete.

Check:

- [ ] chosen category minimum price
- [ ] Basic price field accepts planned value
- [ ] Standard price field accepts planned value
- [ ] Premium price field accepts planned value
- [ ] delivery time options support the planned tier structure
- [ ] revision options support the planned tier structure
- [ ] package fields do not force misleading deliverables
- [ ] competitor Basic/Standard/Premium screenshots or notes are gathered separately

Pricing status until complete:

```text
unresolved / pending manual Fiverr tier verification
```

---

## Buyer Requirement Verification Checks

Check whether the ideal buyer intake set fits cleanly.

If it does not, use a trimmed launch version.

Launch target:

```text
5-7 mandatory questions plus optional fields where useful
```

Verify:

- [ ] number of requirement questions allowed
- [ ] prompt character limit
- [ ] free-text answer behavior
- [ ] multiple-answer behavior
- [ ] attached-file behavior
- [ ] mandatory checkbox behavior
- [ ] buyer requirement preview screen if available
- [ ] whether requirements appear too heavy for a buyer

Do not ask for:

- Etsy passwords
- Etsy 2FA codes
- off-platform contact information
- private buyer/customer data

---

## Gallery Asset Verification Checks

Verify live UI behavior for:

- [ ] image upload count
- [ ] image dimensions accepted
- [ ] image file-size limit
- [ ] sample PDF upload count
- [ ] sample PDF preview pages
- [ ] video upload availability
- [ ] video review behavior
- [ ] whether video becomes cover media

Gallery launch rule:

```text
Use Fiverr-native proof assets. Do not link to SearchClarity.co sample pages in the launch gig or gallery assets.
```

Asset rules:

- [ ] no QR codes
- [ ] no external URLs
- [ ] no contact information
- [ ] no fake Fiverr badges
- [ ] no ranking/sales/traffic guarantees
- [ ] no stock-photo sludge
- [ ] sample/fictional data clearly labeled
- [ ] image text stays at or below 10 words per image

---

## Video Verification Checks

There are two separate video concepts:

| Video Type | Purpose | Launch Status |
|---|---|---|
| Fiverr gallery intro video | Marketing/proof asset | launch candidate only if polished |
| Customer report walkthrough | Paid deliverable feature | not active at launch |

Verify:

- [ ] current allowed video length
- [ ] current file-size limit
- [ ] accepted file formats
- [ ] whether video becomes cover media
- [ ] whether video review delays publish
- [ ] whether captions/on-screen text render well

Do not upload a gallery video unless it is more polished than Image 1.

---

## Publication Readiness Decision

Before publish, record:

| Field | Value |
|---|---|
| Verification reviewer |  |
| Verification date |  |
| Category approved? | yes / no |
| Pricing unblocked? | yes / no |
| Buyer requirements fit UI? | yes / no |
| Gallery assets accepted? | yes / no |
| Sample PDF preview works? | yes / no |
| Video included at launch? | yes / no |
| Seller verification complete or not required? | yes / no |
| Publish approved? | yes / no |
| Remaining blockers |  |

---

## Non-Goals

This checklist does not:

- define final gig copy
- define final pricing
- replace the UI verification log
- replace the offer spec
- replace Fiverr policy review
- authorize publishing by itself
