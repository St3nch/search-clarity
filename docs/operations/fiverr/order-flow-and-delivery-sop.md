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
No customer-facing delivery happens without human approval.
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

- acknowledge the order as soon as practical, ideally within the same business day or within the response-time standard chosen for Fiverr
- check URLs and scope
- check package tier
- check required information
- identify missing/unclear intake

Acknowledgement template:

```text
Thanks - I received your requirements and will review the shop/listing details now. If anything is missing or unclear, I will ask here in the order thread before starting the audit.
```

---

## Stage 3 - Intake QC

Check:

- shop URL opens
- listing URLs open
- listing count fits package
- product summary is understandable
- target buyer is provided
- main audit goal is provided
- biggest current concern is reviewed if provided
- optional current title/tags are reviewed if provided
- optional competitor/context links are reviewed if provided
- optional screenshots are safe to use
- no private buyer/customer data was uploaded
- no login credentials were requested or needed
- no off-platform contact information was requested or needed
- no trademark/IP-risky keyword request is being made
- listings are active/publicly viewable

If information is missing:

```text
Thanks - I can start once I have one missing detail: [specific item]. Please send it here in the order thread so I can keep the audit within scope.
```

If missing info threatens deadline, use Fiverr's extension request flow.

---

## Stage 4 - Work Period

Follow the general fulfillment SOP.

For Fiverr, be extra strict on deadline risk:

- create the internal work packet before research begins
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
- no public page-count promise used unless explicitly approved
- short video report walkthrough is included only if active for the package/channel
- if video is included, outline/talking points were reviewed
- if video is included, internal transcript was generated and reviewed
- if video is included, captions or equivalent accessible text option is available
- if video is included, video link/file works
- if video is included, Fiverr allows the link/file delivery method

---

## Stage 6 - Deliver Now

Attach:

```text
final PDF report
```

Optional, if active for the package/channel and verified as Fiverr-compliant:

```text
short video report walkthrough link or file
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

Optional sentence if video is included:

```text
If your package includes a short video walkthrough, I included the video link/file as well.
```

Adjust tone as needed, but do not remove the no-guarantee boundary.

---

## Stage 7 - Revisions And Corrections

A customer revision is a buyer-requested clarification or adjustment within the original scope.

A SearchClarity correction is a fix for a SearchClarity mistake.

SearchClarity corrections do not count against the buyer's included revision count.

### Customer Revisions

If buyer requests a revision:

Actions:

- read request fully
- decide if in scope
- respond politely
- revise if in scope
- re-deliver through Fiverr

In-scope Fiverr revision examples:

- clarify report wording
- explain a recommendation more clearly
- adjust wording within the originally purchased scope

Out-of-scope Fiverr revision examples:

- review new listings not included in package
- implement edits inside Etsy
- rewrite all listing copy unless package includes it
- provide ongoing coaching
- guarantee results
- add new competitor research beyond package scope

Out-of-scope response template:

```text
Thanks for the note. That request is outside the scope of this audit because it would require [reason]. I can clarify anything inside the delivered report as part of the included revision, but reviewing new listings, adding new research, or doing implementation work would need a separate order/custom scope.
```

### SearchClarity Corrections

Correction examples:

- wrong listing reviewed
- promised section missing
- PDF export broken
- incorrect URL/reference
- formatting issue that makes the report hard to read
- typo/error that changes meaning
- video link/file issue if video was included

Correction handling:

1. Apologize briefly and professionally.
2. Fix the issue.
3. Redeliver through Fiverr.
4. Record the correction reason and outcome.
5. Do not count the correction against the buyer's included revision count.

---

## Stage 8 - Completion

Fiverr may auto-complete the order after the platform's review window if buyer does not request revision or accept manually.

After completion:

- log final status
- record revision outcome if any
- record correction outcome if any
- record buyer feedback if any
- capture raw signal if relevant
- update consent status if buyer permits public use/testimonial/case study
- capture lessons learned or operational notes if useful

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
- video walkthrough production issue, if video is included

---

## Cancellation / Dispute Handling

If cancellation request appears:

- remain polite
- do not argue emotionally
- review whether SearchClarity failed scope/timing
- preserve all communication on Fiverr
- decide whether to accept, revise, correct, or dispute based on facts
- record the reason internally

Potential cancellation reasons to track:

- unclear buyer expectation
- buyer expected guaranteed results
- buyer submitted bad intake
- late delivery risk
- report did not match perceived scope
- buyer wanted implementation, not audit
- buyer expected title/tag rewrite when only audit was purchased
- buyer misunderstood revision scope
- video/link delivery issue, if video was included

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
- revision outcome if any
- correction status/outcome if any
- cancellation/dispute status
- delivered file name/version
- video delivery reference if any
- transcript QC status if video was included
- buyer feedback summary
- raw signal capture status
- consent/testimonial status
- lessons learned / operational notes if any

---

## Non-Goals

This SOP does not:

- replace Fiverr policies
- define general SearchClarity fulfillment
- define final report template
- define Neon Ronin workflows
- authorize automation
- authorize off-platform contact
- authorize autonomous customer delivery

---

## Update Triggers

Update this SOP when:

- Fiverr UI changes
- Fiverr policy changes
- first paid order is completed
- first revision occurs
- first SearchClarity correction occurs
- first cancellation/dispute occurs
- first video walkthrough test occurs
- first Fiverr link/delivery issue occurs
- delivery deadline assumptions change
- buyer requirements change
