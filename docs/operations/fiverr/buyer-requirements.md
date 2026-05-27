# Fiverr Buyer Requirements - Etsy Listing Visibility Audit

## Status

```text
draft
```

## Purpose

This document drafts the Fiverr buyer requirements for the Etsy Listing Visibility Audit gig.

These are Fiverr-specific intake questions shown to the buyer after purchase.

General offer scope is defined in:

```text
../services/etsy-listing-visibility-audit-offer-spec.md
```

---

## Intake Principle

Ask only for what is needed to begin the audit.

Do not overwhelm the buyer.

Do not ask for Etsy login credentials.

Do not ask for off-platform contact information.

---

## Recommended Requirement Set

### Requirement 1 - Etsy shop URL

Type:

```text
Free Text
```

Required:

```text
Yes
```

Prompt:

```text
Please paste your Etsy shop URL.
```

Purpose:

- confirms the shop exists
- gives the analyst starting context
- avoids credentials

---

### Requirement 2 - Listing URLs in scope

Type:

```text
Free Text
```

Required:

```text
Yes
```

Prompt:

```text
Please paste the Etsy listing URL(s) you want reviewed. Basic covers 1 listing, Standard covers up to 3, and Premium covers up to 5.
```

Purpose:

- locks scope
- reduces revision disputes
- ties package tier to deliverable

---

### Requirement 3 - Product summary

Type:

```text
Free Text
```

Required:

```text
Yes
```

Prompt:

```text
What products do you sell? One or two sentences is enough.
```

Purpose:

- gives product context
- helps interpret buyer intent
- helps avoid irrelevant keyword assumptions

---

### Requirement 4 - Target buyer

Type:

```text
Free Text
```

Required:

```text
Yes
```

Prompt:

```text
Who is the target buyer for these listings? For example: brides, teachers, pet owners, new parents, gift buyers, small business owners, etc.
```

Purpose:

- clarifies buyer language
- supports recommendation quality

---

### Requirement 5 - Current keyword assumptions

Type:

```text
Free Text
```

Required:

```text
No
```

Prompt:

```text
Optional: What keywords or search phrases do you currently think matter most for your shop or listings?
```

Purpose:

- reveals buyer assumptions
- helps compare current targeting against visible listing structure

---

### Requirement 6 - Etsy Stats screenshots

Type:

```text
Attached File
```

Required:

```text
No
```

Prompt:

```text
Optional: Upload screenshots of Etsy Stats search terms from the last 30 days if you want them considered. Please do not upload private buyer/customer data.
```

Purpose:

- gives directional search-term evidence when available
- keeps screenshots optional
- warns against private buyer data

---

### Requirement 7 - Shop stage

Type:

```text
Multiple Answer
```

Required:

```text
Yes
```

Prompt:

```text
Which best describes your shop?
```

Options:

```text
Brand new
0-6 months old
6-24 months old
24+ months old
```

Purpose:

- helps calibrate recommendations
- sets realistic context

---

### Requirement 8 - Listings to avoid

Type:

```text
Free Text
```

Required:

```text
No
```

Prompt:

```text
Optional: Are there any listings, products, or topics you do NOT want me to review or reference?
```

Purpose:

- avoids accidental scope conflict
- helps with sensitive or discontinued products

---

## Backup Short Version

If Fiverr UI limits prevent the full requirement set, use this shorter set:

1. Etsy shop URL
2. Listing URL(s) to review
3. Product summary
4. Target buyer
5. Shop stage
6. Optional Etsy Stats screenshots

---

## What Not To Ask

Do not ask for:

- Etsy password
- 2FA codes
- email address
- phone number
- WhatsApp/Discord/Slack/Zoom contact
- payment information
- private buyer/customer data
- supplier details
- profit margins
- full analytics exports unless clearly needed and privacy-safe

---

## Missing Intake Handling

If required intake is incomplete:

1. Message the buyer on Fiverr order page.
2. Ask only for the missing detail.
3. Do not start analysis until scope is clear.
4. If missing information affects delivery time, consider requesting a delivery extension through Fiverr.
5. Do not ask buyer to communicate off-platform.

---

## QC Checks Before Starting Work

- [ ] Shop URL opens
- [ ] Listing URLs open
- [ ] Listing count matches package scope
- [ ] Product type is understandable
- [ ] Target buyer is provided
- [ ] No credentials were requested
- [ ] No off-platform contact was requested
- [ ] Optional screenshots do not expose private customer data

---

## Live UI Verification Needed

Before publishing, verify in `ui-verification-log.md`:

- buyer requirement prompt character limits
- buyer free-text answer limits
- attached-file upload limits
- multiple-answer option limits
- whether all 8 questions fit cleanly

---

## Non-Goals

This document does not:

- define the full fulfillment SOP
- define final Fiverr gig copy
- approve publishing
- replace the offer spec
- define Neon Ronin intake schema
