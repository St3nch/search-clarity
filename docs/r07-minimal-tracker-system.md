# r07 - Minimal Tracker System

**Document purpose:** Define the day-one SearchClarity tracker used to manage customers, orders, reports, action plans, keyword observations, raw market signals, generalized observations, and consent records.

**Audience:** Internal SearchClarity operations, analysts, and future implementation work.

**Status:** Working operating spec. SearchClarity-only. This document defines what SearchClarity tracks from order #1. It does not define Neon Ronin scoring, observatory architecture, agent queues, or cross-business strategy.

---

## 1. Executive Summary

SearchClarity needs a minimal tracker before taking paid orders.

The tracker is not an app. It is not the observatory. It is not a full CRM. It is a simple operating system for the first paid reports.

The tracker must make sure SearchClarity can:

- know who ordered what
- know which shop/listings/pages were reviewed
- know which report was delivered
- preserve the action plan given to the customer
- reuse prior context for returning customers
- track keyword observations created during paid work
- capture raw market signals without overloading fulfillment
- preserve consent records for testimonials, case studies, or public examples

The tracker should start as a spreadsheet/workbook. A real database can come later once manual tracking becomes painful.

---

## 2. Boundary Rule

SearchClarity tracks operational records and raw observations.

Neon Ronin later handles scoring, cross-business comparison, research queues, opportunity routing, and observatory logic.

Clean split:

| SearchClarity tracker owns | SearchClarity tracker does not own |
|---|---|
| Customer/order/report records | Agent orchestration |
| Report delivery status | Observatory scoring |
| Action plan items | Cross-business opportunity ranking |
| Keyword observations from paid work | Strategy queues |
| Raw market opportunity signals | Multi-business intelligence dashboards |
| Consent records | Shared database architecture |
| Returning customer context | Automated research execution |

The tracker should answer:

> What happened during this paid SearchClarity order, what did we deliver, what should we remember, and what raw signals should be handed off later?

It should not answer:

> Is this a good opportunity across all businesses, and what should agents do about it?

That belongs outside SearchClarity.

---

## 3. Recommended Starting Format

Use one workbook with eight sheets:

1. `Customers`
2. `Orders`
3. `Reports`
4. `Action Plan Items`
5. `Keyword Observations`
6. `Raw Market Signals`
7. `Generalized Observations`
8. `Consent Records`

This matches the minimum tracker called for in the audit action list while keeping SearchClarity focused on paid report fulfillment and capture.

Optional later sheets can be added only after the first workflow proves they are needed.

---

## 4. ID Conventions

Use simple readable IDs.

| Record type | Format | Example |
|---|---|---|
| Customer | `CUST-YYYY-NNN` | `CUST-2026-001` |
| Order | `ORD-YYYY-NNN` | `ORD-2026-001` |
| Report | `RPT-YYYY-NNN` | `RPT-2026-001` |
| Action item | `ACT-YYYY-NNN` | `ACT-2026-001` |
| Keyword observation | `KW-YYYY-NNN` | `KW-2026-001` |
| Raw signal | `SIG-YYYY-NNN` | `SIG-2026-001` |
| Generalized observation | `OBS-YYYY-NNN` | `OBS-2026-001` |
| Consent record | `CONSENT-YYYY-NNN` | `CONSENT-2026-001` |

Do not over-engineer IDs. They only need to be stable and easy to reference.

---

## 5. Sheet 1 - Customers

Purpose: identify the customer and the property/shop/site being served.

This sheet combines customer and property basics so the day-one tracker stays simple.

| Field | Required? | Purpose |
|---|---:|---|
| `customer_id` | Yes | Stable customer ID |
| `date_created` | Yes | First date the customer entered the tracker |
| `customer_name` | Yes | First name or display name only |
| `contact_channel` | Yes | Fiverr, Upwork, direct, referral, etc. |
| `platform_username` | Optional | Fiverr/Upwork username if needed for support |
| `email` | Optional | Only for direct/off-platform customers or explicit opt-in situations |
| `shop_or_site_name` | Yes | Etsy shop, Shopify store, or website name |
| `shop_or_site_url` | Yes | Main property URL |
| `primary_platform` | Yes | Etsy, Shopify, WordPress, Pinterest, etc. |
| `niche_descriptor` | Yes | Short human-readable niche/category |
| `first_order_date` | Yes | First paid SearchClarity order date |
| `total_orders` | Optional | Can be calculated manually at first |
| `customer_status` | Yes | Active / Inactive / Blocked / Do Not Contact |
| `notes` | Optional | Operational notes only; no sensitive private commentary |

Do not store payment data, home addresses, phone numbers, private analytics credentials, supplier information, or the customer's customer data.

---

## 6. Sheet 2 - Orders

Purpose: track each paid engagement.

| Field | Required? | Purpose |
|---|---:|---|
| `order_id` | Yes | Stable order ID |
| `customer_id` | Yes | Links to Customers |
| `order_date` | Yes | Date order was received |
| `source_channel` | Yes | Fiverr, Upwork, direct, etc. |
| `source_order_id` | Optional | Fiverr/Upwork/platform order ID |
| `service_type` | Yes | Etsy Listing Visibility Audit, Keyword Pack, etc. |
| `package_tier` | Yes | Basic / Standard / Premium / Custom |
| `property_url` | Yes | Shop/site/page/listing URL being reviewed |
| `listing_count_or_page_count` | Optional | Scope count |
| `intake_status` | Yes | Not Sent / Sent / Incomplete / Complete |
| `order_status` | Yes | Received / In Progress / Waiting on Customer / Delivered / Closed / Cancelled |
| `due_date` | Yes | Delivery deadline |
| `delivered_date` | Optional | Actual delivery date |
| `revision_status` | Yes | None / Requested / In Progress / Complete |
| `internal_owner` | Optional | Analyst initials |
| `notes` | Optional | Operational notes only |

Order status should be updated at least once per work session.

---

## 7. Sheet 3 - Reports

Purpose: track the deliverable file and report metadata.

| Field | Required? | Purpose |
|---|---:|---|
| `report_id` | Yes | Stable report ID |
| `order_id` | Yes | Links to Orders |
| `customer_id` | Yes | Links to Customers |
| `report_type` | Yes | Service/report type |
| `report_version` | Yes | v1, v2, revision, etc. |
| `template_version` | Optional | Template used, if known |
| `source_file_path` | Yes | Markdown/source path |
| `pdf_file_path` | Optional | Delivered PDF path |
| `spreadsheet_file_path` | Optional | Delivered spreadsheet path if relevant |
| `delivery_message_used` | Optional | Delivery template name or short label |
| `executive_summary_short` | Yes | 3-4 line summary for returning-customer context |
| `key_findings_count` | Optional | Number of major findings |
| `action_items_count` | Optional | Number of action plan items |
| `qc_status` | Yes | Not Started / Needs Review / Passed / Failed |
| `delivered_date` | Optional | Date delivered |
| `notes` | Optional | Internal notes |

The report row is the fastest way to answer: what did we deliver, when, and where is the file?

---

## 8. Sheet 4 - Action Plan Items

Purpose: preserve the customer's recommended next steps and make returning-customer work better.

| Field | Required? | Purpose |
|---|---:|---|
| `action_item_id` | Yes | Stable action item ID |
| `report_id` | Yes | Links to Reports |
| `order_id` | Yes | Links to Orders |
| `customer_id` | Yes | Links to Customers |
| `target_url_or_listing` | Optional | Listing/page/shop section affected |
| `priority` | Yes | Do First / Do Next / Test Later / Avoid |
| `action_item` | Yes | The actual recommended action |
| `reasoning_short` | Yes | Why this item matters |
| `implementation_status` | Yes | Unknown / Not Implemented / Partially Implemented / Implemented |
| `outcome_label` | Yes | Unknown / No Data Yet / Positive Signal / Mixed Signal / Negative Signal |
| `confidence` | Yes | Low / Medium / High |
| `followup_needed` | Yes | Yes / No |
| `notes` | Optional | Internal notes |

This sheet is the backbone for returning customers.

When a customer comes back, open this sheet before starting the next report.

---

## 9. Sheet 5 - Keyword Observations

Purpose: preserve keyword findings from paid research so future reports do not start cold.

| Field | Required? | Purpose |
|---|---:|---|
| `keyword_observation_id` | Yes | Stable keyword observation ID |
| `report_id` | Yes | Source report |
| `order_id` | Yes | Source order |
| `keyword` | Yes | Keyword or phrase |
| `keyword_cluster` | Yes | Cluster/group label |
| `buyer_intent` | Yes | Informational / Comparison / Gift / Purchase / Local / Other |
| `platform` | Yes | Etsy, Google, Pinterest, Shopify, etc. |
| `niche` | Yes | Niche/category context |
| `source` | Yes | Manual observation, eRank, Google Trends, SERP provider, etc. |
| `source_date` | Yes | Date observed/researched |
| `demand_note` | Optional | Human note, not fake precision |
| `competition_note` | Optional | Human note |
| `recommended_use` | Optional | Title, tag, description, content, avoid, etc. |
| `confidence` | Yes | Low / Medium / High |
| `notes` | Optional | Internal note |

Do not pretend estimated keyword data is exact. Store the source and date.

---

## 10. Sheet 6 - Raw Market Signals

Purpose: capture commercially interesting observations from paid work without turning SearchClarity into the observatory.

This is the most important boundary-sensitive sheet.

SearchClarity captures the raw signal. Neon Ronin scores later.

| Field | Required? | Purpose |
|---|---:|---|
| `signal_id` | Yes | Stable raw signal ID |
| `date_observed` | Yes | Date the signal was noticed |
| `source_report_type` | Yes | Which service/report surfaced it |
| `source_context` | Yes | General context without private client details |
| `niche` | Yes | Broad niche/category |
| `product_category` | Optional | Product/service category |
| `marketplace` | Yes | Etsy, Shopify, Pinterest, Google, Fiverr, etc. |
| `buyer_intent` | Optional | What buyers appear to want |
| `keyword_cluster` | Optional | Main keyword group |
| `why_it_stood_out` | Yes | Analyst explanation |
| `evidence_summary` | Yes | High-level evidence without private client details |
| `routing_label` | Yes | Ignore / Watch / Research Later / Research Next / Urgent Review |
| `confidence` | Yes | Low / Medium / High |
| `recommended_next_step` | Yes | Ignore / Watch / Hand Off / Recheck Later |
| `handoff_status` | Yes | Not Logged / Logged / Sent to Neon Ronin / Accepted / Rejected / Converted |
| `notes` | Optional | Internal notes |

Hard rules:

- Do not include customer name.
- Do not include shop URL.
- Do not copy customer-specific titles, tags, descriptions, photos, designs, or private strategy.
- Do not store sensitive customer data.
- Do not score the opportunity here.
- Do not turn the signal into a product decision inside SearchClarity.

Good raw signal example:

> Retirement gift searches seem to split strongly by profession, with visible demand for teacher, nurse, boss, coworker, police, and firefighter variants. Several visible listings appear generic and weakly optimized. Worth later public-data research.

Bad raw signal example:

> Client X's exact product/title/tags are weak, so we should copy that niche.

---

## 11. Sheet 7 - Generalized Observations

Purpose: record safe, abstracted observations that improve SearchClarity methodology.

This is not the Neon Ronin observatory. This is a lightweight SearchClarity working sheet for service improvement.

| Field | Required? | Purpose |
|---|---:|---|
| `observation_id` | Yes | Stable observation ID |
| `date_created` | Yes | Date created |
| `observation` | Yes | Abstracted, non-client-identifying pattern |
| `source_type` | Yes | Report pattern / revision pattern / keyword pattern / customer question / outcome pattern |
| `supporting_count` | Optional | Number of times observed, if known |
| `niches_seen` | Optional | Broad niches only |
| `status` | Yes | Emerging / Confirmed / Deprecated / Sent to Neon Ronin |
| `methodology_impact` | Optional | Template update, checklist update, gig copy update, etc. |
| `notes` | Optional | Internal notes |

Use this sheet for SearchClarity service improvement only.

If an observation becomes broader strategy, hand it off through the raw signal/generalized handoff process.

---

## 12. Sheet 8 - Consent Records

Purpose: prove what a customer allowed SearchClarity to use publicly.

| Field | Required? | Purpose |
|---|---:|---|
| `consent_id` | Yes | Stable consent record ID |
| `customer_id` | Yes | Links to Customers |
| `order_id` | Optional | Links to relevant order |
| `report_id` | Optional | Links to relevant report |
| `consent_date` | Yes | Date consent was granted |
| `consent_channel` | Yes | Fiverr message, email, form, etc. |
| `consent_scope` | Yes | Testimonial, case study, screenshot, anonymized example, named example, etc. |
| `approved_language_or_asset` | Yes | Exact approved quote/asset or file reference |
| `allowed_locations` | Yes | Fiverr, SearchClarity.co, LinkedIn, portfolio, etc. |
| `revocable` | Yes | Yes / No |
| `revoked_date` | Optional | Date revoked, if any |
| `status` | Yes | Active / Revoked / Expired |
| `notes` | Optional | Internal notes |

Default rule:

> No public use without a consent record.

Fictional samples do not need consent because they are fictional. Real client examples do.

---

## 13. Minimal Status Values

Use controlled values so the tracker does not rot into free-text soup.

### Order status

- Received
- In Progress
- Waiting on Customer
- Delivered
- Revision Requested
- Closed
- Cancelled

### QC status

- Not Started
- Needs Review
- Passed
- Failed

### Routing label

- Ignore
- Watch
- Research Later
- Research Next
- Urgent Review

### Handoff status

- Not Logged
- Logged
- Sent to Neon Ronin
- Accepted
- Rejected
- Converted

### Outcome label

- Unknown
- No Data Yet
- Positive Signal
- Mixed Signal
- Negative Signal

### Confidence

- Low
- Medium
- High

---

## 14. Day-One Workflow

### New order

1. Add or update customer row.
2. Add order row.
3. Mark intake status.
4. Add report row once report production begins.
5. Track QC and delivery status.

### Report production

1. Capture keyword observations as research happens.
2. Add action plan items as the report is finalized.
3. Add raw market signals only if something commercially interesting appears.
4. Do not force a signal entry if nothing stood out.
5. Finish report QC.
6. Deliver report.
7. Update delivered date and report file path.

### Post-report closeout

Before closing the order:

1. Confirm report row is complete.
2. Confirm action plan items are entered.
3. Confirm raw signals are logged or intentionally skipped.
4. Confirm consent record exists if any testimonial/example/public-use asset was approved.
5. Mark order closed.

---

## 15. What Not To Track

Do not track:

- payment/card details
- customer home addresses
- customer phone numbers
- platform passwords
- API keys
- private analytics credentials
- Etsy buyer personal data
- customer supplier info
- private revenue/profit screenshots unless a specific paid scope requires it
- customer photos/design files unless directly needed and permission is clear
- competitor screenshots unless permission/source rules are clear
- exact client-specific strategy in raw signal rows

If the report does not need it, the tracker probably does not need it.

---

## 16. Future Upgrade Path

The tracker can stay manual for the first 20-50 customers.

Upgrade only when one of these becomes painful:

- too many orders to track manually
- returning-customer history is hard to retrieve
- report files are hard to locate
- raw signals are getting lost
- action plan follow-up becomes valuable enough to productize
- manual data entry causes repeated mistakes

Future upgrades may include:

- Airtable/Notion prototype
- SQLite/Postgres workspace table
- SearchClarity admin dashboard
- automated ID generation
- report file registry
- controlled dropdowns
- export/import into Neon Ronin

Do not build the app before the first paid workflow proves what the tracker actually needs.

---

## 17. Immediate Build Checklist

Create the actual tracker workbook with these sheets:

- [ ] Customers
- [ ] Orders
- [ ] Reports
- [ ] Action Plan Items
- [ ] Keyword Observations
- [ ] Raw Market Signals
- [ ] Generalized Observations
- [ ] Consent Records

Add dropdowns for:

- [ ] order_status
- [ ] qc_status
- [ ] routing_label
- [ ] handoff_status
- [ ] outcome_label
- [ ] confidence

Then test the tracker by entering the fictional Maplewood Candle Co. sample report as a mock order.

---

## 18. Final Recommendation

Build the tracker before launching the first gig.

A simple workbook used consistently is enough. A complex app used inconsistently is worse than useless.

The correct first version is boring:

```text
One workbook.
Eight sheets.
Controlled status values.
Raw signal capture.
No scoring.
No observatory.
No app yet.
```

That is enough to support SearchClarity's first paid reports and preserve the market learning that paid work creates.
