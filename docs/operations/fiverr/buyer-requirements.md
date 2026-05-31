# Fiverr Buyer Requirements - Etsy Listing Visibility Audit

## Status

```text
draft / subject_to_fiverr_ui_limits
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

Do not ask for private buyer/customer data.

The ideal intake set below may need to be reduced during live Fiverr setup if Fiverr question limits, prompt limits, answer limits, or upload limits are too restrictive.

---

## Buyer-Facing Safety Note

Include this note if Fiverr allows enough space:

```text
Please do not send Etsy login credentials, passwords, 2FA codes, private buyer/customer data, or off-platform contact information. I only need public Etsy URLs and any optional screenshots or listing details you choose to provide.
```

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
Please paste your Etsy shop URL. Please make sure the shop is public/viewable.
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
Please paste the Etsy listing URL(s) you want reviewed. Basic covers 1 listing, Standard covers up to 3, and Premium covers up to 5. Please make sure the listings are active/publicly viewable.
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

### Requirement 5 - Main audit goal

Type:

```text
Multiple Choice or Free Text
```

Required:

```text
Yes
```

Prompt:

```text
What is your main goal for this audit?
```

Suggested options if Fiverr supports them:

```text
Improve listing clarity
Review keyword/tag coverage
Understand why a listing may not be getting views
Compare visible marketplace positioning
Get prioritized next steps
Not sure / I want a general audit
Other
```

Purpose:

- makes the report feel more specific to the buyer
- helps prioritize the executive summary and recommendations
- reduces generic report risk

---

### Requirement 6 - Biggest current concern

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
Optional: What is your biggest concern with these listings right now? For example: low views, low favorites, low sales, unsure about keywords, unsure about title/tags, unsure about photos/thumbnail, new shop/no data yet, etc.
```

Purpose:

- gives context for the report
- helps address the buyer's real concern without promising outcomes

---

### Requirement 7 - Current keyword assumptions

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

### Requirement 8 - Current title and tags

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
Optional: If you want tag-specific feedback, paste the current title and tags for each listing. This is helpful if tags are not visible from the public listing.
```

Purpose:

- avoids needing shop login
- improves tag-specific feedback when public data is incomplete
- helps the audit stay accurate

---

### Requirement 9 - Etsy Stats screenshots

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

### Requirement 10 - Competitor or similar listings for context

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
Optional: Are there 1-3 competitor or similar listings you admire or want considered for context? I will not copy competitors. This only helps understand positioning and buyer expectations.
```

Purpose:

- gives marketplace context
- supports competitor/context observations where package scope allows
- prevents competitor copying expectations

---

### Requirement 11 - Shop stage

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

### Requirement 12 - Listings or topics to avoid

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

### Requirement 13 - Trademark/IP reminder

Type:

```text
Checkbox or Multiple Choice
```

Required:

```text
Yes if Fiverr supports it cleanly
```

Prompt:

```text
Please confirm you will not ask SearchClarity to recommend trademarked brand, character, celebrity, or franchise keywords unless you have the right to use them.
```

Purpose:

- discourages trademark-risky keyword requests
- supports the outcome-guarantee and safety policy
- protects report quality

---

## Backup Short Version

If Fiverr UI limits prevent the full requirement set, use this shorter set:

1. Etsy shop URL
2. Listing URL(s) to review
3. What products do you sell?
4. Who is the target buyer?
5. Main goal / biggest concern
6. Shop stage
7. Optional screenshots or title/tags

If even shorter is required, keep these minimum fields:

1. Etsy shop URL
2. Listing URL(s) to review
3. Product summary
4. Target buyer
5. Main goal for the audit

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
- login access to Etsy or any third-party tool

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
- [ ] Listings are active/publicly viewable
- [ ] Product type is understandable
- [ ] Target buyer is provided
- [ ] Main audit goal is provided
- [ ] No credentials were requested
- [ ] No off-platform contact was requested
- [ ] Optional screenshots do not expose private customer data
- [ ] Optional competitor/context links do not create copying expectations
- [ ] Trademark/IP reminder is included or intentionally omitted due to Fiverr UI limits

---

## Live UI Verification Needed

Before publishing, verify in `ui-verification-log.md`:

- buyer requirement prompt character limits
- buyer free-text answer limits
- attached-file upload limits
- multiple-answer option limits
- checkbox/acknowledgment support
- whether all 13 ideal questions fit cleanly
- whether the backup short version is required
- whether required/optional settings behave as expected

---

## Non-Goals

This document does not:

- define the full fulfillment SOP
- define final Fiverr gig copy
- approve publishing
- replace the offer spec
- define Neon Ronin intake schema
