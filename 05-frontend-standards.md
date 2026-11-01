# Frontend engineering standards

## First rule: preserve the project
Inspect before editing. Keep the current framework, package manager, router, data layer, auth, conventions, and tests unless there is a strong user-approved reason to change them.

## Code quality
- TypeScript where the project already uses it or greenfield needs justify it.
- Small components with clear responsibilities.
- Typed props, data models and API responses.
- Avoid `any` unless a boundary requires it and is documented.
- Keep state close to where it is used; avoid global state without need.
- Separate presentation from data/business logic.
- Reuse existing utilities before adding dependencies.
- Avoid unnecessary useEffect chains and derived state duplication.
- Handle rejected requests, loading, empty and error states.

## CSS and styling
- Use design tokens and semantic class names.
- Avoid `!important` as a routine fix.
- Avoid global selectors that unexpectedly affect unrelated pages.
- Prefer layout systems (grid/flex) over positioning hacks.
- Test long content, translations, and dynamic data.

## Security
- Never expose credentials in browser bundles or source control.
- Validate and authorize on the server; client-side checks are not security controls.
- Sanitize untrusted HTML and avoid unsafe DOM injection.
- Avoid logging personal data or access tokens.
- Use least-privilege access to APIs and databases.

## AI Studio Build mode notes
Google AI Studio Build mode currently generates a React frontend by default and a Node.js server runtime for server-side operations. It can provision Firebase Authentication and Firestore, use npm packages, manage secrets server-side, and sync with GitHub. Respect the generated structure and verify what was actually provisioned in the current project before assuming a service exists.
