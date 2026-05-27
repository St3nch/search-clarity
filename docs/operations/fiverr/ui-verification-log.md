# Fiverr UI Verification Log

## Status

```text
draft
```

## Purpose

This log records Fiverr UI facts that must be verified inside the live Fiverr gig editor before SearchClarity publishes or updates a gig.

Claude's Fiverr research identified several constraints that are confirmed in official documentation and several that require live UI confirmation.

This log is the place to record the live checks.

---

## Operating Rule

```text
If Fiverr documentation does not clearly confirm a field limit or category rule, verify it in the live Fiverr UI before relying on it.
```

Do not build final gig copy, buyer requirements, package descriptions, or asset specs on unverified assumptions.

---

## Verification Status Values

Use these values:

```text
not_checked
confirmed
changed_from_research
not_visible_in_ui
blocked_by_account_status
needs_recheck
```

---

## Verification Table

| Item | Expected / researched value | Live UI result | Status | Checked date | Notes |
|---|---|---|---|---|---|
| Buyer requirement prompt character cap | Not officially documented | TBD | not_checked |  |  |
| Buyer free-text answer cap | Not officially documented | TBD | not_checked |  |  |
| Buyer attached-file upload cap | Not officially documented | TBD | not_checked |  |  |
| FAQ answer cap | 300 official blog / 299 reported in UI | TBD | not_checked |  |  |
| Package description cap | 100 reported by third-party sources | TBD | not_checked |  |  |
| E-Commerce SEO > Etsy category minimum price | Category-specific minimum may exist | TBD | not_checked |  |  |
| Standardized package mandatory fields | Category-specific | TBD | not_checked |  |  |
| Delivery-time dropdown options | Category-specific | TBD | not_checked |  |  |
| Service type options | Category-specific | TBD | not_checked |  |  |
| Gig metadata fields | Category-specific | TBD | not_checked |  |  |
| First gig extra manual review delay | Seller-experience reports only | TBD | not_checked |  |  |
| ID verification before first publish | Triggered if Fiverr requests it | TBD | not_checked |  |  |
| Personal/business information verification prompt | May appear for DSA/trader status | TBD | not_checked |  |  |
| Gig URL slug editability | Title edit does not update slug | TBD | not_checked |  |  |
| Image upload validation | 1280 x 769 recommended, JPG/PNG, max 5 MB | TBD | not_checked |  |  |
| PDF gallery behavior | Up to 2 PDFs, first 3 pages displayed | TBD | not_checked |  |  |
| Video upload review behavior | 75 sec max, review may delay video | TBD | not_checked |  |  |
| Gig extra fields | Title, description, price, extra days | TBD | not_checked |  |  |
| Extra fast delivery rules | Must be shorter than package delivery | TBD | not_checked |  |  |
| Revision options | 0-20 or Unlimited | TBD | not_checked |  |  |

---

## Fiverr Account Setup Checks

| Item | Result | Status | Checked date | Notes |
|---|---|---|---|---|
| Seller account created on desktop | TBD | not_checked |  |  |
| Email verified | TBD | not_checked |  |  |
| Profile photo/logo accepted | TBD | not_checked |  |  |
| Display name finalized | TBD | not_checked |  |  |
| Professional title accepted | TBD | not_checked |  |  |
| Bio accepted | TBD | not_checked |  |  |
| Skills entered | TBD | not_checked |  |  |
| Languages entered | TBD | not_checked |  |  |
| Payout method connected | TBD | not_checked |  |  |
| Phone verification complete | TBD | not_checked |  |  |
| Tax form / W-9 complete if needed | TBD | not_checked |  |  |
| Personal/business info verification complete if prompted | TBD | not_checked |  |  |

---

## Etsy Audit Gig Setup Checks

| Item | Result | Status | Checked date | Notes |
|---|---|---|---|---|
| Category path available | Online Marketing > E-Commerce Marketing > E-Commerce SEO Services > Etsy | not_checked |  |  |
| Title accepted | TBD | not_checked |  |  |
| Tags accepted | TBD | not_checked |  |  |
| Description accepted | TBD | not_checked |  |  |
| Package fields accepted | TBD | not_checked |  |  |
| Buyer requirements accepted | TBD | not_checked |  |  |
| Gallery images accepted | TBD | not_checked |  |  |
| Sample PDF accepted | TBD | not_checked |  |  |
| Video accepted, if used | TBD | not_checked |  |  |
| Gig published | TBD | not_checked |  |  |
| Automatic review result | TBD | not_checked |  |  |
| Manual review delay observed | TBD | not_checked |  |  |

---

## Recheck Rules

Recheck Fiverr UI constraints when:

- Fiverr changes the seller UI
- the gig category changes
- SearchClarity adds a new Fiverr gig
- SearchClarity edits package tiers
- buyer requirements change
- Fiverr rejects a field or asset
- Fiverr policy updates

---

## Non-Goals

This log does not:

- define SearchClarity offer scope
- replace final Fiverr copy
- replace buyer requirements text
- replace QC review
- authorize publishing

It only records what the live Fiverr UI allows or blocks.
