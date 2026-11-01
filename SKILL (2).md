---
name: design-system
description: Create and maintain design tokens, typography, color, spacing, grids, component rules, states and design documentation.
---
# Design System Architecture

## Workflow
1. Audit current CSS variables, components, typography, and repeated patterns.
2. Define foundational tokens: color roles, typography, spacing, radius, border, shadow, motion, breakpoints, z-index.
3. Use semantic color tokens (surface, text, muted, border, primary, accent, success, warning, danger) instead of hardcoded hex values in components.
4. Define type scale, line heights, font weights, and content widths.
5. Define layout grid, container widths, spacing rhythm, and responsive behavior.
6. Specify components with anatomy, variants, states, accessibility, and responsive rules.
7. Consolidate duplicates and migrate incrementally without breaking existing behavior.
8. Document tokens and component usage in `workspace/DESIGN_SYSTEM.md`.

## Component inventory
Buttons, links, inputs, selects, checkboxes, radios, switches, tabs, navigation, breadcrumbs, cards, dialogs, popovers, tables, alerts, badges, tooltips, pagination, empty states, loaders, toasts, charts, and content sections as needed.

## Rules
- Tokens must express intent, not only raw values.
- Create variants only when there is a real use case.
- Maintain predictable focus, hover, active, disabled, loading, error and success states.
- Do not create a component abstraction for a one-off element unless it improves clarity or maintainability.
