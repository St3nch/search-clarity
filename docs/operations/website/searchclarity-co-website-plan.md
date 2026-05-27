# SearchClarity.co Website Plan

## Status

```text
draft
```

## Purpose

This document defines the initial plan for `searchclarity.co` as SearchClarity's owned trust hub, SEO/GEO authority asset, blog/content hub, proof library, and future agent-assisted website workspace.

This is a SearchClarity operations document.

It is not Neon Ronin doctrine.

It may later provide requirements for Neon Ronin if/when agents are allowed to support website research, optimization, content suggestions, and repo-based site updates.

---

## Domain

```text
searchclarity.co
```

SearchClarity owns this domain.

The site should become the main public identity for the SearchClarity brand, even if the first paid orders come from Fiverr or other marketplaces.

---

## Core Role Of The Site

SearchClarity.co should serve five jobs:

1. Build trust before a buyer orders on Fiverr, Upwork, or direct.
2. Explain SearchClarity's methodology and caveats.
3. Host sample reports and proof assets.
4. Publish SEO/GEO/marketplace visibility content.
5. Become an owned SEO/GEO/LLM visibility asset that can later be optimized by agents under controlled workflow rules.

The site should not be a giant bloated marketing site at launch.

It should start as a clean, fast, structured authority hub.

---

## Recommended Technical Direction

### Framework

Recommended default:

```text
Next.js
```

Reasons:

- strong fit for static/mostly-static marketing sites
- supports content pages, blog, dynamic metadata, and structured data
- easy deployment to Vercel
- good ecosystem for image optimization, MDX/content, sitemap generation, and analytics
- repo-friendly, which matters for future agent-assisted edits

### Language

Recommended:

```text
TypeScript
```

Reasons:

- safer content/data structures
- easier schema/component typing
- better future agent/code review boundaries

### Styling

Candidate options:

```text
Tailwind CSS
CSS Modules
plain CSS with design tokens
```

Recommended starting point:

```text
Tailwind CSS + small design token file
```

Reason:

Fast to build, easy to maintain, and common for Next.js sites.

### Content

Recommended options:

```text
MDX for pages/posts
Contentlayer or a lightweight custom content loader
plain Markdown with frontmatter
```

Recommended starting point:

```text
MDX or Markdown with frontmatter
```

Reason:

The site should be easy to edit, diff, review, and eventually agent-assist.

### Analytics

Required:

```text
Google Analytics 4
Google Search Console
Bing Webmaster Tools
```

Optional later:

```text
Vercel Analytics
Vercel Speed Insights
Microsoft Clarity
```

Do not add every analytics tool at launch. Keep tracking lightweight and privacy-conscious.

---

## Hosting Options

### Preferred default: Vercel

Vercel is the simplest default for a Next.js site.

Pros:

- first-class Next.js deployment experience
- easy GitHub integration
- preview deployments for pull requests
- simple environment variable handling
- fast enough for the first version
- low friction for solo development

Cons:

- platform lock-in over time
- costs can grow if usage or features expand
- some advanced hosting decisions may need revisiting later

### Alternative: Cloudflare Pages

Pros:

- strong edge/CDN story
- often cost-effective
- good for static sites

Cons:

- Next.js support can require more care depending on features used
- may be less straightforward than Vercel for a full Next.js app

### Alternative: Netlify

Pros:

- good static/marketing-site hosting
- simple deploys

Cons:

- Next.js deployment path is generally less default than Vercel

### Recommendation

Start with:

```text
Next.js + Vercel + GitHub repo
```

Rationale:

Cheap, fast, low-friction, and compatible with future repo-based agent review workflows.

Revisit hosting only if cost, performance, or control becomes a real issue.

---

## Repository Strategy

The website should live in its own repo.

Recommended repo name:

```text
searchclarity-co
```

Possible local path:

```text
C:\dev\searchclarity-co
```

Relationship to current repo:

```text
C:\dev\searchclarity
```

The current `searchclarity` repo holds business docs, operations docs, samples, report templates, and planning.

The future `searchclarity-co` repo should hold the website code, content, components, schema, and deployment config.

Do not mix website implementation code into the business-docs repo unless there is a deliberate reason.

---

## Site Architecture

### URL Architecture Principle

SearchClarity.co should use a two-layer URL model:

```text
/services/{service-slug}      = canonical SearchClarity service page
/fiverr/{service-slug}        = Fiverr-specific buying/support page
/upwork/{service-slug}        = Upwork-specific buying/support page
```

This prevents the site from becoming marketplace-first.

The canonical service page explains the SearchClarity-owned service.

Marketplace pages explain how to buy that service through a specific marketplace/channel.

---

### Canonical Service Layer

Use canonical service URLs for long-term SearchClarity services:

```text
/services/etsy-listing-visibility-audit
/services/etsy-title-tag-rewrite
/services/etsy-keyword-research-pack
/services/shopify-product-page-seo-audit
/services/ai-search-readiness-snapshot
```

These pages should work for:

- organic search
- direct buyers
- LinkedIn/referrals
- marketplace-independent sales
- future internal linking
- structured Service/Offer schema
- LLM/entity clarity

The canonical page should answer:

- what the service is
- who it is for
- what is included
- what is not included
- what proof/sample exists
- what caveats apply
- how to buy or inquire

---

### Marketplace / Channel Layer

Use marketplace/channel URLs for platform-specific buyer intent:

```text
/fiverr/etsy-listing-visibility-audit
/upwork/etsy-listing-visibility-audit
/fiverr/etsy-title-tag-rewrite
/upwork/etsy-title-tag-rewrite
```

These pages should answer:

- how buying works on that marketplace
- what packages exist on that marketplace
- buyer requirements for that marketplace
- delivery/revision expectations for that marketplace
- marketplace-specific FAQ
- link to the marketplace listing/gig/project
- link back to the canonical service page

Marketplace pages must be unique and useful. Do not publish thin copy-paste clones.

---

### URL Intent Map

| URL | Primary intent |
|---|---|
| `/services/etsy-listing-visibility-audit` | Etsy listing audit, Etsy SEO audit service, marketplace visibility audit |
| `/fiverr/etsy-listing-visibility-audit` | Fiverr Etsy SEO audit, SearchClarity Fiverr, Etsy listing audit Fiverr |
| `/upwork/etsy-listing-visibility-audit` | Upwork Etsy SEO audit, Etsy audit freelancer, hire Etsy SEO audit |
| `/sample-report` | proof asset and report quality |
| `/methodology` | trust, differentiation, caveats |
| `/blog/...` | educational SEO/GEO content and topical authority |

---

### Minimum Launch Site

Recommended first version:

```text
/
/services
/services/etsy-listing-visibility-audit
/sample-report
/methodology
/about
/blog
/contact
/privacy
/terms
```

### Expanded Site Later

```text
/services/etsy-title-tag-rewrite
/services/etsy-keyword-research-pack
/services/etsy-shop-visibility-report
/services/pinterest-seo-plan
/services/shopify-product-page-seo-audit
/services/ai-search-readiness-snapshot
/samples
/samples/etsy-listing-audit
/resources
/resources/etsy-seo
/resources/marketplace-visibility
/resources/ai-search-readiness
/case-studies
```

---

## Entity-Structured Architecture

The site should be structured around entities, not random pages.

Primary entity:

```text
SearchClarity
```

Core entity types:

- Brand / Organization: SearchClarity
- Service: Etsy Listing Visibility Audit
- Service category: Marketplace visibility reports
- Topic cluster: Etsy SEO
- Topic cluster: marketplace visibility
- Topic cluster: GEO / AI search readiness
- Proof asset: Maplewood Candle Co. sample report
- Methodology: human-reviewed visibility audit methodology
- Canonical service page: SearchClarity-owned service explanation
- Marketplace/channel page: Fiverr, Upwork, direct, or future channel-specific buying page
- Channel: Fiverr, later Upwork/direct

### Entity Page Map

| Entity | Page |
|---|---|
| SearchClarity brand | `/` and `/about` |
| Etsy Listing Visibility Audit service | `/services/etsy-listing-visibility-audit` |
| Fiverr Etsy Listing Visibility Audit channel page | `/fiverr/etsy-listing-visibility-audit` |
| Upwork Etsy Listing Visibility Audit channel page | `/upwork/etsy-listing-visibility-audit` later |
| Methodology | `/methodology` |
| Sample report | `/sample-report` or `/samples/etsy-listing-audit` |
| Etsy SEO topic | `/resources/etsy-seo` later |
| AI search readiness topic | `/resources/ai-search-readiness` later |
| Blog/news | `/blog` |

### Internal Linking Rule

Every content page should link to at least one relevant entity page.

Examples:

- Etsy SEO blog posts link to the Etsy Listing Visibility Audit service page.
- Methodology links to sample report and service page.
- Sample report links to methodology and service page.
- AI/GEO posts link to future AI Search Readiness Snapshot when created.

---

## SEO / GEO / LLM Visibility Requirements

SearchClarity should practice what it sells.

The site should be built for:

- traditional search discoverability
- entity clarity
- structured information extraction
- clear citations and source references where appropriate
- strong internal linking
- clean metadata
- clear service descriptions
- human-readable methodology
- content that can be cited or summarized by LLMs

### Page-Level Requirements

Every important page should include:

- clear title tag
- clear meta description
- canonical URL
- one primary H1
- logical H2/H3 structure
- concise above-the-fold explanation
- internal links to related service/topic pages
- structured data where appropriate
- last updated date for informational pages
- author/publisher clarity for blog posts

### LLM-Friendly Content Rules

Content should:

- define terms clearly
- use direct answers before nuance
- include methodology and caveats
- avoid fake certainty
- include examples
- provide structured sections and tables where useful
- make SearchClarity's services and limits easy to understand
- avoid vague marketing fluff

---

## Schema Strategy

Use JSON-LD where appropriate.

Potential schema types:

| Page type | Candidate schema |
|---|---|
| Home/About | Organization, WebSite |
| Service page | Service, Offer, BreadcrumbList |
| Blog post | Article, BlogPosting, BreadcrumbList |
| Sample report page | CreativeWork, Report, BreadcrumbList |
| FAQ sections | FAQPage, only if the page actually has visible FAQs and current search guidelines support it |
| Contact page | Organization, ContactPoint where appropriate |

Rules:

- Schema must match visible page content.
- Do not add fake reviews or aggregate ratings.
- Do not invent offers or prices not visible on the page.
- Do not over-markup every block just because it is possible.
- Validate structured data before deployment.

---

## Blog / Content Strategy

The blog should support SearchClarity's services and entity footprint.

Initial categories:

```text
Etsy SEO
Marketplace Visibility
SearchClarity News
AI Search / GEO Readiness
Report Methodology
```

Early post types:

- explanatory posts
- methodology posts
- sample report breakdowns
- caveat/expectation posts
- buyer education posts
- platform update commentary
- SearchClarity service updates

Do not create generic AI content sludge.

Every post should support a real SearchClarity service, method, or buyer question.

### Initial Blog Ideas

- What an Etsy Listing Visibility Audit Actually Reviews
- Why Etsy SEO Audits Cannot Guarantee Sales
- Etsy Title Tags and Buyer Intent: What Sellers Often Miss
- How To Read a Marketplace Visibility Report
- What SearchClarity Means By Human-Reviewed SEO Recommendations
- SEO vs GEO vs Marketplace Visibility: A Plain-English Guide
- Why Sample Reports Matter Before Buying an SEO Service

---

## Initial Page Requirements

### Home

Purpose:

- explain SearchClarity quickly
- show first service
- link to sample report
- link to methodology
- link to Fiverr or waitlist/contact when ready

Must include:

- what SearchClarity is
- who it helps
- first offer
- no-guarantee positioning
- proof/sample CTA

### Services

Purpose:

- list active and future services
- clearly separate available vs planned

Must include:

- Etsy Listing Visibility Audit as active/first
- future services marked as planned, not available if not ready

### Etsy Listing Visibility Audit

Purpose:

- sell/explain the first offer

Must include:

- package overview
- what is reviewed
- what buyer receives
- what is not included
- no ranking/sales guarantee
- sample report link
- CTA

### Sample Report

Purpose:

- prove quality

Must include:

- preview of Maplewood report
- clear fictional-sample note
- download/view PDF link if available
- methodology explanation
- CTA to service page

### Methodology

Purpose:

- differentiate SearchClarity from keyword dumps

Must include:

- human-reviewed process
- evidence and observation approach
- recommendation structure
- caveats
- what SearchClarity does not promise

### About

Purpose:

- build trust

Must decide:

- founder identity level
- brand-only vs named analyst
- LinkedIn/profile proof

### Blog

Purpose:

- publish structured topical content

Must include:

- category pages or tags eventually
- author/date/updated date
- internal links

### Contact

Purpose:

- allow direct inquiry later

Must not conflict with Fiverr off-platform communication rules for Fiverr buyers.

### Privacy / Terms

Purpose:

- explain data handling and service boundaries

Required before serious direct sales.

---

## Google Analytics And Search Tools

Minimum setup:

- Google Analytics 4
- Google Search Console
- Bing Webmaster Tools
- XML sitemap
- robots.txt

Analytics requirements:

- track page views
- track service page visits
- track sample report CTA clicks
- track outbound Fiverr CTA clicks if used
- track contact form submissions if used

Avoid overtracking early.

Do not collect sensitive customer data through analytics events.

---

## Agent-Assisted Website Operations - Future Requirements

SearchClarity should eventually allow controlled agent assistance for the website.

Possible agent-supported tasks later:

- audit internal links
- suggest blog topics
- suggest service page updates
- identify stale content
- compare SERP/GEO observations to page content
- propose schema updates
- propose metadata improvements
- flag thin pages
- flag broken links
- suggest FAQ additions from buyer questions
- draft content updates for human review

Agents should not initially:

- push directly to production
- publish posts without review
- change service claims without review
- change pricing without review
- add schema without validation
- use customer data in public content
- make unsupported ranking/sales claims

### Repo-Based Workflow Idea

Future controlled flow:

```text
agent observes site/content issue
-> agent drafts local change or recommendation
-> human reviews diff
-> tests/build run
-> preview deployment reviewed
-> human approves merge
-> production deploy
```

This implies the website repo should support:

- local development
- clear content files
- reviewable diffs
- preview deployments
- automated lint/build checks
- structured metadata/schema files
- content status fields

---

## SERP / GEO Data And Neon Ronin Boundary

SearchClarity may need SERP, ranking, marketplace, and LLM visibility data for its own site.

Examples:

- target queries for service pages
- citations/mentions of SearchClarity
- competitor service pages
- LLM answer inclusion/exclusion observations
- marketplace-service SERP positions
- blog topic gaps
- internal linking opportunities

Boundary:

```text
SearchClarity defines what site data and visibility questions it needs.
Neon Ronin later manages agent tasks, data storage, audit, and scoring if/when authorized.
```

Do not build Neon Ronin integration from this document.

This document only states SearchClarity website requirements and future support needs.

---

## Website Launch Phases

### Phase 1 - Planning

- [ ] create website plan
- [ ] choose tech stack
- [ ] choose hosting
- [ ] define initial pages
- [ ] define schema strategy
- [ ] define analytics requirements
- [ ] define repo strategy

### Phase 2 - Proof Assets

- [ ] finish Maplewood sample report
- [ ] export sample PDF
- [ ] create sample report page copy
- [ ] create methodology copy
- [ ] create first service page copy

### Phase 3 - Build MVP Site

- [ ] initialize Next.js repo
- [ ] add layout/navigation/footer
- [ ] add home page
- [ ] add service page
- [ ] add sample report page
- [ ] add methodology page
- [ ] add about/contact/privacy/terms placeholders
- [ ] add blog scaffold
- [ ] add metadata and sitemap
- [ ] add analytics

### Phase 4 - SEO/GEO Hardening

- [ ] add structured data
- [ ] add internal linking map
- [ ] add canonical URLs
- [ ] add Open Graph/Twitter metadata
- [ ] add sitemap/robots
- [ ] validate schema
- [ ] run Lighthouse/basic performance checks
- [ ] submit Search Console/Bing Webmaster Tools

### Phase 5 - Content Expansion

- [ ] publish first methodology post
- [ ] publish Etsy SEO educational post
- [ ] publish sample report breakdown
- [ ] publish no-guarantee SEO expectations post
- [ ] publish SearchClarity launch/news post

### Phase 6 - Agent-Assisted Optimization Later

- [ ] define safe agent website permissions
- [ ] define repo review workflow
- [ ] define allowed data sources
- [ ] define content update review gate
- [ ] define schema update validation gate
- [ ] define SERP/GEO observation logging

---

## Immediate Decisions Needed

| Decision | Current Recommendation | Status |
|---|---|---|
| Framework | Next.js | proposed |
| Language | TypeScript | proposed |
| Hosting | Vercel | proposed |
| Styling | Tailwind CSS | proposed |
| Content | MDX/Markdown with frontmatter | proposed |
| Analytics | GA4 + Search Console + Bing Webmaster Tools | proposed |
| Repo | separate `searchclarity-co` repo | proposed |
| Blog | yes | proposed |
| Schema | JSON-LD where appropriate | proposed |
| Agent site work | future, human-reviewed only | proposed |

---

## Non-Goals

This document does not:

- build the site
- create the website repo
- choose a final hosting contract
- define Neon Ronin agent implementation
- authorize agents to edit or publish the website
- replace SearchClarity offer specs
- replace legal/privacy policy drafting
- define all blog content

---

## Next Actions

1. Review and approve this website plan.
2. Decide whether website repo should be created now or after sample PDF is complete.
3. Finish Maplewood sample report and PDF.
4. Draft first service page copy from the offer spec.
5. Draft methodology page from report/QC standards.
6. Create `searchclarity-co` repo when ready.
7. Build MVP site only after page content and proof assets are stable enough.
