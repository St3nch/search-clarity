# Recordkeeping And Consent

## Status

```text
draft
```

## Purpose

This document defines SearchClarity's operational recordkeeping and consent rules.

SearchClarity needs records for customer continuity, fulfillment control, quality review, future service improvement, and later Neon Ronin onboarding evidence.

This document is SearchClarity-owned.

It is not Neon Ronin doctrine.

---

## Core Rules

```text
Keep enough records to understand what was ordered, what was delivered, what was recommended, what was reviewed, and what consent was granted.
```

```text
Do not collect or store sensitive data unless the service truly needs it.
```

```text
No public use of real customer material without consent.
```

---

## Record Categories

SearchClarity should maintain records for:

- customer/channel identity
- order/request
- intake response
- property/listing/page reviewed
- report/deliverable
- QC result
- delivery event
- revision/support event
- raw market signal
- generalized observation
- consent/public-use permission

---

## Customer / Channel Record

Purpose:

- identify repeat customers
- connect orders to a buyer/channel
- avoid losing context

Suggested fields:

| Field | Purpose |
|---|---|
| customer_id | Internal stable ID |
| channel | Fiverr, Upwork, direct, etc. |
| channel_username | Platform username/display name |
| contact_allowed | Whether direct contact is allowed under channel rules |
| shop_or_site_name | Customer property name |
| shop_or_site_url | Main public URL |
| primary_platform | Etsy, Shopify, etc. |
| notes | Operational notes only |

Do not store payment card data, passwords, or unnecessary personal data.

---

## Order Record

Purpose:

- track what was purchased and delivered

Suggested fields:

| Field | Purpose |
|---|---|
| order_id | Internal order ID |
| channel_order_id | Fiverr/Upwork/direct order ID |
| customer_id | Link to customer |
| service_type | What was ordered |
| package_tier | Basic, Standard, Premium, Custom |
| order_date | Date purchased |
| requirements_submitted_date | When intake became usable |
| due_date | Delivery deadline |
| delivered_date | Actual delivery date |
| order_status | Received, In Progress, Delivered, Completed, Cancelled, etc. |
| revision_count | Number of revisions requested |
| notes | Operational notes |

---

## Intake Record

Purpose:

- preserve what the customer submitted
- support scope review
- explain later decisions

Suggested fields:

| Field | Purpose |
|---|---|
| intake_id | Internal intake ID |
| order_id | Linked order |
| submitted_at | Date/time received |
| shop_url | Public shop/site URL |
| listing_urls | URLs in scope |
| product_summary | Customer's product description |
| target_buyer | Customer's buyer description |
| optional_files | Screenshots or files provided |
| intake_status | Complete, Incomplete, Needs Clarification |
| notes | Operational notes |

Sensitive uploads should be reviewed before storage or reuse.

---

## Report / Deliverable Record

Purpose:

- track what was produced and delivered

Suggested fields:

| Field | Purpose |
|---|---|
| report_id | Internal report ID |
| order_id | Linked order |
| report_type | Audit, rewrite, keyword pack, etc. |
| source_file_path | Markdown/source file path |
| final_file_path | Delivered PDF/file path |
| template_version | Template used |
| qc_status | Passed, Failed, Blocked, etc. |
| delivered_version | Final version label |
| delivery_channel | Fiverr, direct, etc. |
| notes | Operational notes |

---

## QC Record

Purpose:

- prove the report was reviewed before delivery

Suggested fields:

| Field | Purpose |
|---|---|
| qc_id | Internal QC ID |
| report_id | Linked report |
| reviewer | Person who reviewed |
| review_date | Date of QC |
| qc_result | Passed, Passed with Notes, Failed, Blocked |
| required_fixes | Fixes needed before delivery |
| delivery_approved | Yes/No |
| notes | Operational notes |

---

## Delivery Record

Purpose:

- track when and how work was sent to the customer

Suggested fields:

| Field | Purpose |
|---|---|
| delivery_id | Internal delivery ID |
| order_id | Linked order |
| report_id | Linked deliverable |
| delivered_at | Date/time sent |
| delivery_channel | Fiverr, Upwork, direct, etc. |
| delivery_message | Template or message reference |
| delivered_file | File name/version |
| status | Delivered, Redelivered, Failed |
| notes | Operational notes |

---

## Revision / Support Record

Purpose:

- understand revision causes
- improve intake, gig copy, and report clarity

Suggested fields:

| Field | Purpose |
|---|---|
| revision_id | Internal revision ID |
| order_id | Linked order |
| requested_at | Date/time requested |
| request_summary | What buyer asked for |
| in_scope | Yes/No |
| resolution | Revised, Clarified, Declined, Custom Offer Suggested |
| redelivered_at | Date/time redelivered if applicable |
| notes | Operational notes |

---

## Raw Market Signal Record

Purpose:

- capture interesting market/service observations from paid work

Suggested fields:

| Field | Purpose |
|---|---|
| signal_id | Internal signal ID |
| date_observed | Date noticed |
| source_order_type | Service type that surfaced it |
| source_context | Generalized context only |
| niche | Broad niche/category |
| marketplace | Etsy, Shopify, Pinterest, Google, etc. |
| keyword_cluster | Optional keyword group |
| why_it_stood_out | Analyst explanation |
| evidence_summary | High-level evidence only |
| routing_label | Ignore, Watch, Research Later, Research Next |
| confidence | Low, Medium, High |
| handoff_status | Not Logged, Logged, Sent Later, Parked |
| notes | Internal notes |

Rules:

- no customer name
- no customer URL
- no exact private report text
- no customer-specific strategy
- no scoring inside SearchClarity

---

## Consent Record

Purpose:

- prove what customer material SearchClarity may use publicly

Consent is required before using real customer material in:

- testimonials
- case studies
- website samples
- Fiverr gallery examples
- LinkedIn posts
- anonymized public examples if still traceable

Suggested fields:

| Field | Purpose |
|---|---|
| consent_id | Internal consent ID |
| customer_id | Linked customer |
| order_id | Linked order |
| consent_date | Date granted |
| consent_channel | Fiverr message, email, form, etc. |
| consent_scope | Testimonial, case study, screenshot, anonymized example, named example |
| approved_asset_or_quote | Exact approved text/asset or reference |
| allowed_locations | Fiverr, website, LinkedIn, portfolio, etc. |
| revocable | Yes/No |
| status | Active, Revoked, Expired |
| notes | Operational notes |

Default rule:

```text
No public use without consent.
```

Fictional samples do not require consent, but they must be clearly fictional.

---

## What Not To Store

Do not store:

- Etsy passwords
- 2FA codes
- payment card data
- private buyer/customer data from the seller's shop
- unnecessary analytics exports
- supplier details
- private revenue/profit screenshots unless explicitly needed and consented
- private personal contact data unless direct channel requires it
- customer files unrelated to the service

---

## Retention Notes

SearchClarity should keep enough records for:

- customer support
- revisions
- repeat orders
- quality improvement
- consent proof
- future platform onboarding evidence

SearchClarity should not keep unnecessary sensitive customer data indefinitely.

Formal retention windows are an open decision.

---

## Relationship To Neon Ronin

These records describe what SearchClarity needs operationally.

Later, Neon Ronin may model some records through platform/workspace schemas.

For now:

```text
SearchClarity defines the business record need.
Neon Ronin later decides how reusable platform records support it.
```

---

## Non-Goals

This document does not:

- define a database schema
- define Neon Ronin records
- authorize automation
- replace privacy/legal review
- store actual customer records

---

## Open Questions

- What exact system will hold operational records before Neon Ronin onboarding?
- What retention window should be used for delivered reports?
- Should real customer samples ever be public, or only fictional samples?
- What exact consent language should be used for testimonials?
- How should customer deletion/removal requests be handled?
