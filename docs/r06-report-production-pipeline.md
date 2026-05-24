# r06 — SearchClarity Report Production Pipeline

**Document purpose:** Define the simplest reliable workflow for turning SearchClarity report markdown into professional customer-facing PDF reports.

**Audience:** Internal SearchClarity team.
**Status:** Working production plan.

---

## 1. Executive Summary

SearchClarity needs a repeatable report production pipeline before launch. The report content can be written in Markdown, but customers should receive polished PDFs and, where relevant, spreadsheets.

The first goal is not automation. The first goal is consistency.

The pipeline should make it easy to produce:

- public sample reports
- paid customer PDF reports
- PDF previews for Fiverr/Upwork galleries
- internal QA copies
- future website downloads

The recommended starting workflow is:

```text
Markdown source
→ SearchClarity report stylesheet
→ PDF export
→ manual QA pass
→ delivery-ready PDF
→ archive source + PDF in customer/report history
```

Do not build a complex app yet. Start with a simple pipeline that can ship real reports cleanly.

---

## 2. Pipeline Goals

The production pipeline must produce reports that are:

- professional enough to justify mid-market pricing
- consistent across customers and report types
- readable on desktop and mobile
- exportable to PDF without broken tables
- easy to revise before delivery
- easy to archive and reference later
- safe to use for fictional samples and paid customer work

The pipeline must prevent:

- random formatting drift
- broken headings
- inconsistent caveats
- missing sample disclaimers
- ugly Fiverr PDF previews
- client reports that look like raw AI output

---

## 3. Recommended Starting Toolchain

Use Markdown as the source format.

Recommended first toolchain:

```text
Markdown (.md)
Pandoc or equivalent converter
HTML/CSS stylesheet
PDF output
```

Why this is the right starting point:

- Markdown is easy to edit.
- Version control works well.
- Templates can be reused.
- CSS gives us brand styling.
- PDF export can be improved over time.
- Neon Ronin agents can later draft or assemble Markdown sections.

Alternative tools are acceptable later, but the first launch should not depend on a heavy publishing system.

---

## 4. Folder Structure

Recommended report production folders:

```text
C:\dev\searchclarity\docs\samples\
C:\dev\searchclarity\docs\templates\
C:\dev\searchclarity\docs\styles\
C:\dev\searchclarity\docs\exports\
C:\dev\searchclarity\docs\archive\
```

Purpose:

| Folder | Purpose |
|---|---|
| `samples` | Public or internal fictional sample reports |
| `templates` | Reusable report templates by service type |
| `styles` | CSS / styling rules for PDF export |
| `exports` | Generated PDF outputs |
| `archive` | Old drafts, backups, retired docs, or prior versions |

---

## 5. Report Source Rules

Every report source file should be Markdown.

Required source rules:

- Use one H1 for the report title.
- Use H2 for major report sections.
- Use H3 for subsections.
- Use plain Markdown tables unless a table is too wide.
- Avoid excessive nested bullets.
- Keep recommendation blocks consistent.
- Do not leave placeholders such as `[TBD]`, `[CLIENT]`, or `[XXX]` in delivery files.
- Use straight quotes unless a style decision says otherwise.
- Put sample disclaimers at the top of all fictional reports.
- Keep caveat language consistent with r04.

---

## 6. Standard Report Export Checklist

Before exporting a PDF, confirm:

- [ ] Cover/title section is present.
- [ ] Prepared-for line is present.
- [ ] Date is present.
- [ ] Sample notice appears if fictional.
- [ ] Scope section is present.
- [ ] Data source disclosure is present.
- [ ] Every recommendation has an implementation direction.
- [ ] Action plan is present.
- [ ] Caveat section is present.
- [ ] No fake ranking or sales promises appear.
- [ ] No accidental client-identifying details appear in fictional samples.
- [ ] No `[placeholder]` text remains.
- [ ] Tables are readable after PDF export.
- [ ] Page breaks do not split important tables badly.
- [ ] Filename follows convention.

---

## 7. File Naming Convention

### Sample reports

```text
SearchClarity_Sample_[ReportType]_[FictionalShop]_[YYYY-MM-DD].pdf
```

Example:

```text
SearchClarity_Sample_EtsyListingVisibilityAudit_MaplewoodCandleCo_2026-05-23.pdf
```

### Paid reports

```text
SearchClarity_[ReportType]_[ShopName]_[YYYY-MM-DD].pdf
```

Example:

```text
SearchClarity_EtsyListingVisibilityAudit_ExampleShop_2026-05-23.pdf
```

### Spreadsheet deliverables

```text
SearchClarity_[ReportType]_[ShopName]_[YYYY-MM-DD].xlsx
SearchClarity_[ReportType]_[ShopName]_[YYYY-MM-DD].csv
```

---

## 8. Minimum Brand Styling

The first stylesheet should be simple.

Use:

- clean sans-serif headings
- readable body font
- strong section spacing
- clear tables
- subtle border lines
- page numbers
- report title in header or footer
- SearchClarity name in footer
- sample watermark or sample label for fictional reports

Avoid:

- loud colors
- stock-photo design garbage
- heavy backgrounds
- huge logo blocks
- cramped tables
- dense walls of text
- overdesigned Fiverr-looking templates

The report should look like a professional analyst document, not a Canva coupon flyer.

---

## 9. First PDF Production Target

The first target report is:

```text
C:\dev\searchclarity\docs\samples\maplewood-candle-co-listing-visibility-audit.md
```

The first output should be:

```text
C:\dev\searchclarity\docs\exports\SearchClarity_Sample_EtsyListingVisibilityAudit_MaplewoodCandleCo_2026-05-23.pdf
```

This first export is a pipeline test, not the final public proof asset.

It should answer:

- Does the Markdown structure export cleanly?
- Are tables readable?
- Does the report feel professional?
- Does the sample disclaimer survive export?
- Is the PDF usable as a Fiverr proof asset?
- What styling needs to change before public use?

---

## 10. Human QA Gate

No report ships directly from Markdown export.

Every report needs a human QA pass after export.

QA reviewer checks:

- content accuracy
- formatting
- missing sections
- broken tables
- weird page breaks
- unsupported claims
- accidental guarantees
- sensitive data exposure
- sample/client labeling
- final filename

Only after this QA pass is the PDF considered delivery-ready.

---

## 11. Relationship to Future Neon Ronin

SearchClarity starts with a manual report production pipeline.

Later, Neon Ronin can support:

- drafting report sections
- assembling reports from templates
- checking required sections
- running QC checklists
- detecting placeholder text
- exporting PDFs
- storing report metadata
- sending generalized market signals to the Observatory

But Neon Ronin should not be required for the first manual launch.

The first version should work with a human, Markdown files, and a PDF export process.

---

## 12. Next Actions

1. Create `styles` and `exports` folders.
2. Create a first simple CSS stylesheet.
3. Export the Maplewood sample report to PDF.
4. Review the PDF for layout issues.
5. Fix the sample report source where needed.
6. Create a reusable Etsy Listing Visibility Audit template in `templates`.
7. Add PDF production steps to the fulfillment SOP.

---

## 13. Final Recommendation

Build the pipeline before creating more sample reports.

One usable sample report exported as a clean PDF is worth more than five markdown drafts sitting in a folder.

The immediate goal is:

```text
One sample report
One repeatable export method
One QA checklist
One delivery-ready PDF
```

That gives SearchClarity a real proof asset and a real production workflow.
