---
name: frontend-development
description: Implement production-minded frontend UI, responsive components, interactions and pages while preserving the existing codebase.
---
# Frontend Development

## Before coding
1. Inspect repository tree, package manager, package scripts, framework, routing, styling, data fetching, state management and existing component conventions.
2. Check Git status and current changes; do not overwrite unrelated user work.
3. Identify the smallest file set that can deliver the requested improvement.
4. Confirm content, assets, data contracts and responsive requirements.

## Implementation rules
- Preserve existing stack and working business logic.
- Use semantic HTML and accessible form controls.
- Keep components focused, composable and typed.
- Avoid giant components, duplicated markup, unnecessary dependencies, inline magic values and brittle selectors.
- Use CSS variables/design tokens for repeated values.
- Use stable keys and handle asynchronous states.
- Add client-side validation for feedback and server-side validation for trust.
- Never place secrets in browser code or public repository files.
- Ensure all visible controls work; remove or clearly disable actions that are not implemented.
- Use real links for navigation and buttons for actions.
- Use responsive images with correct aspect ratios and lazy loading below the fold.
- Respect existing localization and content tone.

## Greenfield default (only when no stack exists)
React + TypeScript, Vite or the platform-provided React runtime, a light token-driven styling system, accessible headless primitives, and a consistent SVG icon library. Keep dependencies lean. For AI Studio Build mode, respect its generated React client and Node.js server environment rather than scaffolding a conflicting second app.

## Work pattern
Implement one coherent slice at a time: structure → tokens → components → page → interaction → responsive pass. After each major slice, run the most relevant check.

## Final report
List changed files, user-visible changes, functional behavior, tests/build/lint actually run, and any remaining limitations.
