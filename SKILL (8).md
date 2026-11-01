---
name: responsive-accessibility
description: Review and implement responsive layouts, keyboard interactions, touch usability, semantic markup and accessibility improvements.
---
# Responsive Design and Accessibility

## Responsive workflow
1. Inspect the current breakpoints and layout system.
2. Test at minimum: 360px, 390px, 768px, 1024px, and 1440px widths when tooling permits.
3. Re-compose content for mobile: navigation, columns, tables, forms, dialogs, charts, media and CTAs.
4. Prevent horizontal overflow, clipped content, tiny controls, and hidden essential actions.
5. Ensure touch targets and spacing are comfortable. Do not use hover as the only way to reveal content.
6. Validate landscape and zoom/resizing behavior where practical.

## Accessibility checklist
- Use landmarks, semantic headings, lists, buttons, and links correctly.
- Every input has a programmatic label; errors are associated with fields.
- All interactive elements are keyboard accessible with visible focus.
- Focus order is logical; dialogs manage focus and return it appropriately.
- Contrast meets WCAG 2.2 AA target levels where applicable.
- Do not rely on color alone to communicate state.
- Images have appropriate alternative text; decorative images have empty alt text.
- Motion supports `prefers-reduced-motion`.
- Dynamic status messages are announced where appropriate.
- Tables have headers; charts have text or tabular alternatives.

## Rules
- Treat WCAG conformance as a testable target, not a claim based on appearance.
- State which checks were automated, manual, or not performed.
- Consult the official W3C WCAG 2.2 reference when detailed criteria are needed.
