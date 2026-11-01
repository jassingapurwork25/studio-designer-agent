# Website audit rubric (100 points)

This is an expert heuristic score. It is not a usability study, analytics report, or compliance certification.

| Category | Weight | What to inspect |
|---|---:|---|
| UX and task completion | 20 | User journeys, clarity, friction, feedback, errors |
| Visual hierarchy and craft | 15 | Typography, composition, spacing, grids, contrast, consistency |
| Information architecture | 10 | Navigation, labels, page structure, findability |
| Responsive behavior | 10 | Mobile layout, overflow, touch, reflow |
| Accessibility | 15 | Semantics, keyboard, focus, labels, contrast, motion |
| Content and trust | 10 | Accuracy, clarity, useful proof, metadata, language |
| Performance | 10 | Loading, image strategy, interaction responsiveness, layout stability |
| Engineering quality | 10 | Reuse, maintainability, error handling, security basics |

## Scoring scale
- 0–2 out of 5 per criterion: critical/mostly missing
- 3 out of 5: partially works, notable friction
- 4 out of 5: strong with limited gaps
- 5 out of 5: consistently excellent and verified

Calculate weighted points transparently. If a category cannot be inspected, mark it **Not assessed** and do not silently give it a zero or assume it is good. Either report a score over assessed categories only (with coverage disclosed) or provide no total score.

## Severity
- P0 — Critical: security issue, data loss, blocked key task, severe accessibility barrier.
- P1 — High: key task difficult/broken, mobile failure, major navigation or form problem.
- P2 — Medium: meaningful inconsistency, unclear content, repeated friction, missing state.
- P3 — Low: polish, micro-spacing, minor visual refinement.

## Finding format
- ID and severity
- Page/route and viewport
- Evidence (screenshot, element, behavior, source location)
- User impact
- Recommended fix
- Effort estimate (S/M/L)
- Dependencies or risks

## Report integrity
Do not invent performance measurements, analytics, test results, conversion rates, survey findings, or user quotes. Make clear whether an observation is from code, screenshot, live browser, search result, or inference.
