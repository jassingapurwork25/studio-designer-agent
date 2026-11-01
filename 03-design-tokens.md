# Design tokens and visual system

Use tokens as a coherent starting point and adapt after reviewing brand and content. Values below are example scales, not fixed prescriptions.

## Example semantic color roles
```css
:root {
  --color-canvas: #f7f8fa;
  --color-surface: #ffffff;
  --color-surface-muted: #eef1f5;
  --color-text: #17212f;
  --color-text-muted: #5b6675;
  --color-border: #dce2e9;
  --color-primary: #174ea6;
  --color-primary-strong: #103b80;
  --color-accent: #14a38b;
  --color-success: #16835d;
  --color-warning: #a96500;
  --color-danger: #b42318;
  --color-focus: #286de0;
}
```

## Spacing scale
An 8-point rhythm is a useful starting point: 4, 8, 12, 16, 24, 32, 40, 48, 64, 80, 96. Use smaller increments for dense controls and optical corrections only when needed.

## Type scale example
- Display: 48–72px desktop, responsive down to 36–48px
- H1: 36–48px
- H2: 28–36px
- H3: 22–28px
- Body large: 18–20px
- Body: 16px
- Small: 14px
- Caption/metadata: 12–13px only when still readable

These are ranges, not a rule to make every interface large. Data-heavy tools may need a compact scale with strong contrast and spacing.

## Layout
- Define a maximum content width appropriate to the product (often 1120–1360px for wide desktop layouts).
- Use a grid that adapts to content; do not force 12 columns on every page.
- Keep form and reading widths narrower than dashboards where appropriate.
- Define breakpoints from content pressure, not device names alone.

## Radius, border and elevation
- Use 2–3 radius levels, not a different radius for every component.
- Prefer borders and subtle surface shifts for structure; use shadows to communicate elevation, not decoration.
- Keep shadow styles consistent across the system.

## Component specification
For each reusable component record: purpose, anatomy, variants, dimensions, typography, colors, spacing, states, responsive behavior, keyboard behavior, and examples of correct/incorrect use.
