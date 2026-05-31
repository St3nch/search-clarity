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
No public use of real customer material without explicit asset-specific consent.
```

```text
Do not store live customer records in public repo docs.
```

---

## Temporary Manual Record Storage Rule

Until SearchClarity has a dedicated records system or is onboarded into a proper Neon Ronin-supported workflow, operational records may be kept manually.

Temporary acceptable options:

- private local project folder
- private spreadsheet/tracker
- private platform/order notes where allowed by the channel
- private secure document folder

Do not store real customer records, private customer files, screenshots, order details, or consent artifacts inside public repository documentation.

The repo may contain:

- templates
- example schemas
- fictional samples
- sanitized examples
- process docs

The repo must not contain:

- live customer intake
- real customer report artifacts unless intentionally approved and private
- private screenshots
- platform order IDs tied to customer identities
- real customer consent records
- private buyer/customer data

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
- revision event
- SearchClarity correction event
- video/transcript event, if applicable
- sample/proof asset
- financial/order payout summary
- raw market signal
- generalized observation
- consent/public-use permission
- customer deletion/removal request

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
| communication_channel_allowed | Where communication is allowed under channel rules |
| shop_or_site_name | Customer property name |
| shop_or_site_url | Main public URL |
| primary_platform | Etsy, Shopify, etc. |
| notes | Operational notes only |

For Fiverr, customer communication stays on Fiverr unless Fiverr rules explicitly allow otherwise.

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
| revision_count | Number of customer revisions requested |
| correction_count | Number of SearchClarity corrections made |
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
| main_audit_goal | Customer's primary goal for the audit |
| biggest_concern | Customer's concern if provided |
| optional_files | Screenshots or files provided |
| intake_status | Complete, Incomplete, Needs Clarification |
| notes | Operational notes |

Sensitive uploads should be reviewed before storage or reuse.

Optional screenshots should not include private buyer/customer data.

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
| video_included | Yes/No |
| video_file_or_reference | Video file/link/reference if applicable |
| transcript_file_or_reference | Internal transcript file/reference if applicable |
| transcript_qc_status | Not Applicable, Pending, Passed, Failed |
| captions_or_accessible_text_status | Not Applicable, Available, Missing, Needs Review |
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
| video_qc_status | Not Applicable, Pending, Passed, Failed |
| transcript_qc_status | Not Applicable, Pending, Passed, Failed |
| sample_or_gallery_asset_qc_status | Not Applicable, Pending, Passed, Failed |
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
| video_delivery_reference | Video file/link/reference if applicable |
| transcript_delivered | Yes/No/Not Applicable |
| status | Delivered, Redelivered, Failed |
| notes | Operational notes |

The transcript is internal by default unless a customer-facing transcript option is intentionally offered later.

---

## Revision Record

Purpose:

- understand customer-requested revision causes
- improve intake, gig copy, and report clarity

A customer revision is a buyer-requested clarification or adjustment within the original scope.

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

Customer revisions do not include fixing SearchClarity mistakes.

---

## SearchClarity Correction Record

Purpose:

- track quality fixes caused by SearchClarity error
- separate corrections from customer revision usage
- improve templates, QC, and fulfillment process

A SearchClarity correction is a fix for a SearchClarity mistake.

SearchClarity corrections do not count against the buyer's included revision count.

Correction examples:

- wrong listing reviewed
- promised section missing
- PDF export broken
- incorrect URL/reference
- formatting issue that makes the report hard to read
- typo/error that changes meaning
- video link/file issue if video was included
- missing transcript/caption QC if video workflow required it internally

Suggested fields:

| Field | Purpose |
|---|---|
| correction_id | Internal correction ID |
| order_id | Linked order |
| report_id | Linked report/deliverable |
| discovered_at | Date/time discovered |
| discovered_by | Customer, QC, operator, platform issue, etc. |
| correction_type | Wrong URL, missing section, export issue, formatting issue, video issue, other |
| correction_summary | What was wrong |
| fixed_at | Date/time fixed |
| redelivered_at | Date/time redelivered if applicable |
| counted_against_revision | Should be No |
| root_cause | Intake, template, QC miss, export issue, operator error, other |
| prevention_note | What should change to prevent repeat |
| notes | Operational notes |

---

## Sample / Proof Asset Record

Purpose:

- track sample reports, Fiverr gallery assets, website samples, and proof assets
- prove whether an asset is fictional, anonymized, or consented-real
- avoid accidentally publishing customer material without permission

Suggested fields:

| Field | Purpose |
|---|---|
| asset_id | Internal asset ID |
| asset_type | Sample PDF, gallery image, gallery video, website sample, social graphic, etc. |
| source_type | Fictional, anonymized, consented-real |
| source_report | Related report/sample if applicable |
| allowed_locations | Fiverr, website, LinkedIn, portfolio, internal only, etc. |
| sample_label_present | Yes/No |
| external_url_removed | Yes/No/Not Applicable |
| customer_identity_removed | Yes/No/Not Applicable |
| consent_id | Linked consent record if real material is used |
| qc_status | Pending, Passed, Failed, Retired |
| active_status | Draft, Active, Retired |
| notes | Operational notes |

Default rule:

```text
Use fictional samples by default.
```

Real customer material may be used only with explicit, asset-specific consent.

Fiverr launch assets should use Fiverr-native proof assets and should not include SearchClarity.co URLs, QR codes, contact information, fake badges, fake ratings, or ranking/sales/traffic guarantees.

---

## Financial / Order Payout Record

Purpose:

- track basic revenue and payout information without storing sensitive payment data
- support monthly bookkeeping and future accounting workflows

Suggested fields:

| Field | Purpose |
|---|---|
| financial_record_id | Internal financial record ID |
| order_id | Linked order |
| channel | Fiverr, Upwork, direct, etc. |
| gross_amount | Amount customer paid before platform fees |
| platform_fee | Fiverr/Upwork/payment processor fee if available |
| net_payout | Amount received after fees |
| payout_status | Pending, Cleared, Paid Out, Refunded, Cancelled |
| payout_date | Date funds cleared or paid out |
| refund_amount | Amount refunded if any |
| notes | Operational notes |

Do not store payment card numbers, bank account numbers, buyer payment details, or private payment credentials.

For marketplace channels, rely on platform exports/statements where possible.

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
- no exact listing URL
- no order ID
- no screenshots
- no exact private report text
- no verbatim customer report excerpts
- no customer-specific strategy
- no customer-identifying details
- no scoring inside SearchClarity

Raw signals should be generalized aggressively enough that a customer, shop, order, or report cannot be reconstructed from the signal.

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
| consent_channel | Fiverr message, email, form, platform message, etc. |
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

Consent may be captured through Fiverr message, email, form, or platform message if the channel allows it.

Consent must identify the exact approved text, screenshot, report excerpt, testimonial, asset, or use case.

Do not rely on vague consent such as:

```text
sure, use it
```

Fictional samples do not require consent, but they must be clearly fictional.

---

## Customer Deletion / Removal Request Record

Purpose:

- track customer requests to delete, remove, anonymize, or stop using their material
- preserve evidence of how SearchClarity handled the request

Suggested fields:

| Field | Purpose |
|---|---|
| request_id | Internal request ID |
| customer_id | Linked customer if known |
| order_id | Linked order if applicable |
| requested_at | Date/time request was received |
| request_channel | Fiverr, Upwork, email, form, etc. |
| request_summary | What the customer asked to remove/delete |
| scope_verified | Yes/No |
| action_taken | Removed, Deleted, Anonymized, Retained with reason, Pending |
| action_date | Date action was taken |
| retained_records_reason | Accounting, platform record, legal, dispute, operational minimum, etc. |
| notes | Operational notes |

Handling rule:

1. Record the request.
2. Verify the scope of what the customer wants removed or deleted.
3. Remove, delete, anonymize, or stop using material where reasonable and allowed.
4. Retain only records needed for legal, accounting, platform, dispute, or operational minimum reasons.
5. Document the action taken.

Do not promise instant total deletion if platform, legal, accounting, or dispute records must be retained.

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
- customer files inside public repo docs
- screenshots that expose private customer/buyer data

---

## Retention Notes

SearchClarity should keep enough records for:

- customer support
- revisions
- SearchClarity corrections
- repeat orders
- quality improvement
- consent proof
- financial/bookkeeping review
- future platform onboarding evidence

SearchClarity should not keep unnecessary sensitive customer data indefinitely.

Formal retention windows are an open decision.

Until retention windows are finalized, minimize sensitive data and keep customer-facing artifacts in private storage only.

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
- How should customer deletion/removal requests be handled in each channel?
- What monthly financial export process should be used for Fiverr and future marketplaces?
