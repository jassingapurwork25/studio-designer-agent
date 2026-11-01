---
name: design-audit
description: Perform evidence-based UX, UI, content, responsive, accessibility, performance and technical audits of existing websites.
---
# Design Audit

## Trigger
Use for website reviews, design critique, usability analysis, redesign assessment, or a request to score a site.

## Audit coverage
Review as many of these as the supplied access permits:
- Global navigation, page hierarchy, wayfinding and search
- Homepage/landing page message, value proposition and CTA
- Key user journeys and interaction states
- Typography, spacing, alignment, grid and visual hierarchy
- Color, contrast, imagery, icons and brand consistency
- Forms, validation, tables, dashboards, empty/loading/error states
- Responsive behavior: narrow phone, large phone, tablet, desktop
- Accessibility: semantics, keyboard, focus, labels, contrast, touch targets, reduced motion
- Performance: image weight, render-blocking assets, layout shift, script weight
- SEO/content: title, metadata, heading order, link clarity, indexability basics
- Engineering: component reuse, code consistency, errors, dependency risk and security basics

## Workflow
1. Identify routes and select representative pages by task importance.
2. Inspect live pages or code/screenshots. State the inspection method and limitations.
3. For each issue, record: evidence, user impact, severity, recommendation, effort estimate (S/M/L).
4. Use severity: P0 critical blocker/security; P1 major task/accessibility/mobile failure; P2 meaningful friction/inconsistency; P3 polish.
5. Separate visual issues from functional bugs and content gaps.
6. Score only using `knowledge/06-audit-scoring.md`; explain the rubric and confidence.
7. Save a report using `templates/audit-report.md` when files can be created.

## Output
Executive summary, route coverage, prioritized findings, score breakdown (if requested), quick wins, strategic fixes, risks, and evidence links/file locations.

## Rules
- Do not infer conversion rates, bounce rates, user satisfaction, or accessibility conformance from appearance alone.
- Never claim a site is WCAG-compliant based only on visual inspection.
- Mark uninspected pages and states explicitly.
