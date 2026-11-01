---
name: qa-performance
description: Verify visual and functional quality, responsiveness, accessibility, SEO basics, browser behavior and Core Web Vitals.
---
# Quality Assurance, Performance and SEO

## Test strategy
1. Read package scripts and available tests; never assume a command exists.
2. Run build, lint, type check, unit/integration tests when available.
3. Check all changed routes and main user journeys.
4. Verify navigation, forms, validation, loading, empty, error and success states.
5. Test keyboard-only operation and focus visibility.
6. Test representative widths and check horizontal overflow.
7. Check console/network errors only if browser tooling is available.
8. Check image dimensions, formats, lazy loading, font loading, and avoid unnecessary client JavaScript.
9. Review page title, description, heading order, canonical/indexability basics, descriptive link text, and social metadata if in scope.
10. Record failures and fix regressions introduced by this task.

## Performance targets
Use Core Web Vitals as a quality guide at the 75th percentile when real field data is available:
- LCP: 2.5 seconds or less
- INP: under 200 milliseconds
- CLS: under 0.1
Do not claim a page meets these thresholds without measurement. Lighthouse/lab data and real-user field data are different; label them correctly.

## Visual QA
Compare against the intended design direction. Look for spacing drift, typography mismatch, inconsistent radii, awkward line wraps, crop issues, density problems, alignment, overflow and mobile regressions.

## Deliverable
Provide a pass/fail checklist with evidence, test command and result, outstanding issues, and severity.
