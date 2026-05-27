# SearchClarity Order Fulfillment SOP

## Status

```text
draft
```

## Purpose

This SOP defines the general SearchClarity order fulfillment workflow for paid report services.

It is channel-neutral. Fiverr-specific steps belong in:

```text
../fiverr/order-flow-and-delivery-sop.md
```

This SOP should be usable for Fiverr, Upwork, direct website orders, and future channels with channel-specific adjustments.

---

## Core Rule

```text
No customer-facing report is delivered until intake is complete, scope is confirmed, QC is passed, and delivery materials are prepared.
```

---

## Standard Fulfillment Flow

```text
order/request received
-> intake reviewed
-> scope confirmed
-> research/observations completed
-> report drafted
-> QC completed
-> final deliverable exported
-> delivery message prepared
-> delivery sent
-> revision handled if needed
-> records updated
-> raw signal captured if relevant
-> order closed
```

---

## Stage 1 - Order Received

Actions:

- confirm service/package purchased
- confirm channel
- confirm due date/deadline
- confirm buyer submitted required intake or requirements
- create/update order record
- assign internal work status

Do not start analysis until required intake is usable.

Output:

```text
order accepted for intake review
```

---

## Stage 2 - Intake Review

Review:

- buyer name/platform username
- shop/site URL
- listing/page URLs
- purchased package scope
- target buyer context
- product/category context
- optional screenshots/files
- any stated buyer goals
- any red flags

Checks:

- URLs open
- scope matches package
- no credentials requested
- no private customer/buyer data accidentally submitted
- buyer is not asking for guaranteed ranking, sales, or platform manipulation

If intake is incomplete:

1. Ask for the missing information on the platform/order channel.
2. Keep the message short and specific.
3. Do not move to analysis until scope is clear.
4. Request extension if the delay threatens deadline.

Output:

```text
intake accepted / intake needs clarification / order should be declined or cancelled
```

---

## Stage 3 - Scope Confirmation

Confirm:

- number of listings/pages included
- exact URLs in scope
- service package tier
- delivery format
- revision count
- expected delivery date
- out-of-scope requests

If buyer requests extra work, decide whether to:

- include it as goodwill
- offer paid add-on/custom offer
- decline as out of scope
- recommend a separate service

Output:

```text
scope locked
```

---

## Stage 4 - Research And Observations

Perform the service-specific review.

For Etsy Listing Visibility Audit, likely observations include:

- listing title structure
- tag/keyword coverage, if available/provided
- description clarity
- buyer language alignment
- visible photos/thumbnail issues
- shop trust/context notes
- marketplace/search observations
- competitor pattern observations where included
- customer-provided Etsy Stats screenshots if provided

Record observations in a way that separates:

- customer-specific report notes
- reusable/generalized market observations
- raw signals that might be captured later

Output:

```text
research notes / observation notes complete
```

---

## Stage 5 - Draft Report

Use the correct service template.

For each major recommendation, prefer:

```text
Observation:
Why it matters:
Recommendation:
How to implement:
Caveat:
```

Draft report must include:

- scope
- methodology
- executive summary
- findings
- recommendations
- prioritized action plan
- caveats
- next steps

Output:

```text
draft report ready for QC
```

---

## Stage 6 - QC Review

Use:

```text
../quality-control/qc-checklist.md
../quality-control/outcome-guarantee-language-policy.md
```

QC must check:

- package scope satisfied
- no outcome guarantees
- no fake precision
- recommendations are actionable
- caveats present
- customer information handled safely
- trademark/IP-risky suggestions avoided
- formatting is professional
- report file opens correctly

If QC fails:

- fix the report
- rerun QC
- do not deliver until pass

Output:

```text
QC passed / QC failed with required fixes
```

---

## Stage 7 - Final Deliverable Export

Prepare final deliverable.

Checks:

- correct filename
- correct version
- PDF opens
- links, tables, and headings render correctly
- page count roughly matches package promise
- file size is acceptable for channel
- no draft comments remain

Output:

```text
final deliverable ready
```

---

## Stage 8 - Delivery Message

Delivery message should include:

- thank-you line
- what is attached
- 3-bullet summary of what to look at first
- reminder that recommendations are diagnostic, not guaranteed outcomes
- revision instructions if relevant
- polite feedback/review request if allowed by channel rules

Do not include:

- off-platform contact requests
- guarantees
- pressure for positive reviews
- upsell spam

Output:

```text
delivery message ready
```

---

## Stage 9 - Delivery

Deliver through the correct channel.

For Fiverr, use Deliver Now and attach the PDF.

For direct website orders, use the approved direct delivery process once defined.

Record:

- delivery date/time
- delivered file/version
- delivery message used
- channel/order ID

Output:

```text
order delivered
```

---

## Stage 10 - Revisions

If revision is requested:

1. Read the request fully.
2. Decide whether it is in scope.
3. If in scope, revise and redeliver.
4. If out of scope, explain politely and offer appropriate next step.
5. Record revision reason and outcome.

In-scope revision examples:

- correcting unclear wording
- clarifying a recommendation
- fixing missing listing covered by package
- correcting a formatting/export issue

Out-of-scope examples:

- reviewing a new listing not originally included
- implementing changes inside Etsy
- rewriting entire listings unless purchased
- providing guaranteed ranking plan
- ongoing strategy support

Output:

```text
revision completed / revision declined as out of scope / custom follow-up offered
```

---

## Stage 11 - Records Update

After delivery and/or completion, update records:

- order status
- delivered file path/version
- QC status
- delivery date
- revision status
- buyer feedback if any
- raw signals captured if any
- consent status if any public use is requested

Output:

```text
order record updated
```

---

## Stage 12 - Raw Signal Capture

If the report surfaced a generalizable pattern, log a raw market signal.

Examples:

- repeated weak title pattern in a niche
- unclear buyer language in product category
- keyword cluster worth watching
- competitor pattern observed across multiple results
- possible future service opportunity

Rules:

- do not include customer name
- do not include customer URL
- do not include exact private strategy
- do not score the opportunity
- do not turn signal into a business decision

Output:

```text
raw signal logged / no signal captured
```

---

## Stage 13 - Order Closeout

Before closing:

- [ ] report delivered
- [ ] QC passed
- [ ] delivery record updated
- [ ] revision status known
- [ ] raw signal capture reviewed
- [ ] consent status recorded if relevant
- [ ] customer follow-up action noted if needed

Output:

```text
order closed
```

---

## Non-Goals

This SOP does not:

- replace channel-specific SOPs
- define final report templates
- define Neon Ronin workflows
- define agent automation
- define database implementation
- authorize off-platform delivery

---

## Update Rule

Update this SOP after:

- first complete mock order
- first paid order
- first revision request
- first cancellation/dispute
- first direct website order
- any major channel policy change
