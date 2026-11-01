# Interface patterns reference

Choose patterns based on user tasks and content. These are options, not mandatory templates.

## Marketing / institutional websites
- Header: clear identity, concise primary navigation, visible priority action; mobile navigation must remain keyboard operable.
- Hero: specific value proposition, relevant proof/context, and one primary action. Avoid vague slogans.
- Content sections: use varied layouts (editorial split, process, stats only when verified, feature explanation, case study, FAQ).
- Trust: cite verified credentials, policy, team, partners, or outcomes; do not invent logos or claims.
- Footer: contact, legal, key navigation and institutional details.

## SaaS / product interfaces
- App shell: clear workspace identity, navigation hierarchy, account/context controls.
- Dashboard: surface only high-value KPIs; explain metric meaning and period; support empty and loading states.
- Data tables: meaningful columns, clear sorting/filtering, pagination, responsive alternative, row actions with labels.
- Forms: group fields, provide examples where useful, inline errors, preserve entered values, clear success confirmation.
- Search/filter: show active filters and provide a reset path.
- Settings: group by user mental model; warn before destructive changes.

## Student / education portals
- Separate information by role where needed: student, parent, tutor, faculty/admin.
- Show the next important action and current status, not every available metric at once.
- Academic data needs labels, dates, source, and definitions.
- Attendance, grades, and personal records require authorization and privacy controls.
- Notification states need clear priority and delivery status.

## Common states every component may need
Default, hover, focus-visible, active, disabled, loading, success, warning, error, empty, selected, read-only. Add only relevant states, but never omit a needed state because it is visually inconvenient.

## Interaction rules
- Links navigate; buttons perform actions.
- Provide feedback after a meaningful action.
- Confirm destructive actions and explain consequences.
- Avoid hidden gestures and hover-only actions.
- Preserve user input after recoverable errors.
- Make focus order match visual/logical order.
