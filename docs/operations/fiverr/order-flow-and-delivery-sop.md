# Fiverr Order Flow And Delivery SOP

## Status

```text
draft
```

## Purpose

This SOP defines the Fiverr-specific order flow for SearchClarity's Etsy Listing Visibility Audit gig.

It supplements the general SearchClarity fulfillment SOP:

```text
../fulfillment/order-fulfillment-sop.md
```

Use this document for Fiverr-specific timing, order status, delivery, revision, cancellation, and communication rules.

---

## Core Fiverr Rules

```text
All customer communication stays on Fiverr.
The order timer starts after buyer requirements are submitted.
No customer-facing delivery happens before QC passes.
No outcome guarantees are included in delivery messages.
```

---

## Fiverr Order Status Flow

Expected order flow:

```text
Requirements Needed / Missing Details
-> In Progress
-> Delivered
-> In Revision, if buyer requests revision
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

---

## Stage 1 - Order Purchased, Requirements Needed

When buyer purchases but has not submitted requirements:

Actions:

- wait for requirements
- do not start the audit
- do not skip requirements unless intentionally approved
- use Fiverr's nudge/reminder if buyer is delayed

Suggested timing:

| Time since purchase | Action |
|---|---|
| 0-24 hours | Wait |
| 24 hours | Use Fiverr nudge or short message asking for requirements |
| 48+ hours | Send polite reminder if platform allows |

Do not ask buyer to email or message off-platform.

---

## Stage 2 - Requirements Submitted, Timer Starts

Once requirements are submitted, the order enters In Progress and the delivery timer starts.

Immediate actions:

- acknowledge order within target of 1 hour where possible
- check URLs and scope
- check package tier
- check required information
- identify missing/unclear intake

Acknowledgement template:

```text
Thanks — I received your requirements and will review the shop/listing details now. If anything is missing or unclear, I’ll ask here in the order thread before starting the audit.
```

---

## Stage 3 - Intake QC

Check:

- shop URL opens
- listing URLs open
- listing count fits package
- product summary is understandable
- target buyer is provided
- optional screenshots are safe to use
- no private buyer/customer data was uploaded
- no login credentials were requested or needed

If information is missing:

```text
Thanks — I can start once I have one missing detail: [specific item]. Please send it here in the order thread so I can keep the audit within scope.
```

If missing info threatens deadline, use Fiverr's extension request flow.

---

## Stage 4 - Work Period

Follow the general fulfillment SOP.

For Fiverr, be extra strict on deadline risk:

- do not wait until the final hours to export PDF
- run QC before delivery day where possible
- request extension early if buyer delay or scope issue creates risk
- do not deliver an incomplete report just to beat the timer

---

## Stage 5 - Delivery Preparation

Before clicking Deliver Now:

- final PDF opens
- file size is below Fiverr delivery limit
- correct package scope delivered
- QC checklist passed
- delivery message prepared
- no off-platform contact included
- no guarantee language included

---

## Stage 6 - Deliver Now

Attach:

```text
final PDF report
```

Optional, if included in package:

```text
Loom walkthrough link or file, only if allowed and channel-compliant
```

Be careful with external links. If using Loom or another tool, verify Fiverr allows it for delivery and that it does not move business off-platform.

If uncertain, do not include external link until verified.

---

## Delivery Message Template

```text
Hi [Name],

Your Etsy Listing Visibility Audit is attached as a PDF.

Start with:
1. The Executive Summary
2. The Priority Action Plan
3. The listing-specific recommendations

A quick reminder: this audit provides diagnostic findings and recommendations to test. I do not guarantee specific Etsy rankings, traffic, or sales because those depend on many factors outside this report.

If anything in the report is unclear, you can use your included revision to ask for clarification within the original scope.

Thank you for choosing SearchClarity.
```

Adjust tone as needed, but do not remove the no-guarantee boundary.

---

## Stage 7 - Revisions

If buyer requests a revision:

Actions:

- read request fully
- decide if in scope
- respond politely
- revise if in scope
- re-deliver through Fiverr

In-scope Fiverr revision examples:

- clarify report wording
- fix missed package-scope listing
- correct formatting/export problem
- expand reasoning for a recommendation

Out-of-scope Fiverr revision examples:

- review new listings not included in package
- implement edits inside Etsy
- rewrite all listing copy unless package includes it
- provide ongoing coaching
- guarantee results

Out-of-scope response template:

```text
Thanks for the note. That request is outside the scope of this audit because it would require [reason]. I can clarify anything inside the delivered report as part of the included revision, but reviewing new listings or doing implementation work would need a separate order/custom scope.
```

---

## Stage 8 - Completion

Fiverr may auto-complete the order after the platform's review window if buyer does not request revision or accept manually.

After completion:

- log final status
- record revision outcome if any
- record buyer feedback if any
- capture raw signal if relevant
- update consent status if buyer permits public use/testimonial/case study

---

## Late Delivery Risk

Avoid Late and Very Late status.

If delivery risk appears:

1. Identify cause.
2. Communicate early on Fiverr.
3. Request extension through Fiverr if justified.
4. Do not promise faster delivery than production reality.
5. Do not deliver low-quality or incomplete work just to stop timer.

Common causes:

- buyer submitted unclear intake
- URLs inaccessible
- scope mismatch
- optional screenshots contain sensitive/private data
- report production took longer than expected
- export issue

---

## Cancellation / Dispute Handling

If cancellation request appears:

- remain polite
- do not argue emotionally
- review whether SearchClarity failed scope/timing
- preserve all communication on Fiverr
- decide whether to accept, revise, or dispute based on facts
- record the reason internally

Potential cancellation reasons to track:

- unclear buyer expectation
- buyer expected guaranteed results
- buyer submitted bad intake
- late delivery risk
- report did not match perceived scope
- buyer wanted implementation, not audit

Use these notes to improve gig description, FAQ, intake, or scope.

---

## Review / Feedback Handling

Do not pressure buyers for positive reviews.

Allowed tone:

```text
If the report was helpful, honest feedback on Fiverr is appreciated.
```

Avoid:

```text
Please leave 5 stars.
I need a good review.
Message me before leaving anything less than 5 stars.
```

---

## Fiverr-Specific Records To Keep

For each Fiverr order, record:

- Fiverr order ID
- buyer username/display name
- package tier
- order date
- requirements submitted date
- due date
- delivery date
- revision count
- cancellation/dispute status
- delivered file name/version
- buyer feedback summary
- raw signal capture status
- consent/testimonial status

---

## Non-Goals

This SOP does not:

- replace Fiverr policies
- define general SearchClarity fulfillment
- define final report template
- define Neon Ronin workflows
- authorize automation
- authorize off-platform contact

---

## Update Triggers

Update this SOP when:

- Fiverr UI changes
- Fiverr policy changes
- first paid order is completed
- first revision occurs
- first cancellation/dispute occurs
- delivery deadline assumptions change
- buyer requirements change
