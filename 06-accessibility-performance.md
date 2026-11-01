# Accessibility and performance reference

## Accessibility target
Aim for WCAG 2.2 AA unless the product brief or applicable regulation requires more. Official reference: https://www.w3.org/TR/WCAG22/

Important practical checks:
- Text contrast: generally 4.5:1 for normal text and 3:1 for large text.
- Non-text contrast: meaningful UI boundaries and graphical indicators should be distinguishable.
- Keyboard: all functionality reachable; logical focus order; visible focus; no keyboard traps.
- Focus: do not hide focused elements under sticky headers/dialogs.
- Pointer: avoid tiny targets; allow enough spacing and alternatives for complex gestures.
- Labels and errors: programmatic labels, instructions, error identification, and helpful correction hints.
- Reflow: content remains usable at narrow widths and zoom without unnecessary two-dimensional scrolling.
- Motion: respect reduced-motion settings and avoid flashing content.
- Status: announce important asynchronous updates to assistive technology.

## Core Web Vitals targets
Use these as targets, not claims:
- LCP ≤ 2.5 seconds
- INP < 200 milliseconds
- CLS < 0.1
Official Google reference: https://developers.google.com/search/docs/appearance/core-web-vitals

Measure at the 75th percentile using field data when available. Lab tools are useful for diagnosis but do not equal real-user field data. Label measurements and their test conditions.

## Practical performance tactics
- Resize/compress images and use modern formats when supported.
- Set intrinsic width/height or aspect ratio to reduce layout shift.
- Lazy-load non-critical below-the-fold images.
- Avoid shipping unnecessary JavaScript and large animation libraries.
- Use code splitting for large routes when beneficial.
- Avoid loading multiple font families/weights without a clear reason.
- Prevent repeated requests and layout thrashing.
- Set caching headers appropriately when deployment context allows.
