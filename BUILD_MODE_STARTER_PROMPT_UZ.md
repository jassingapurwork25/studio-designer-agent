# AI Studio Build mode uchun qo'shimcha prompt

Agar keyinchalik Studio Northstar agentiga alohida web-ilova interfeysi (Design Workbench) yaratmoqchi bo'lsangiz, Build mode'ga quyidagini bering. Bu prompt agentni sozlashning o'rnini bosmaydi; faqat agent uchun alohida web-app yasaydi.

---

Create a professional web-based **Design Workbench** for a senior web design agency workflow. It is a workspace for managing website audits, redesign directions, design systems, implementation tasks, and QA reports.

Use the existing AI Studio full-stack environment. Inspect the generated stack before coding. Use React + TypeScript on the frontend and the provided Node.js server runtime for server-side operations. Never expose API keys or secrets to the browser.

Core areas:
1. Projects — project list, URL/repository, target audience, status, owner, last updated.
2. Website Audit — route inventory, findings with P0–P3 severity, evidence links, impact, recommendation and effort.
3. Redesign Direction — visual thesis, typography, semantic color roles, grid, imagery direction, page structure and responsive notes.
4. Design System — semantic tokens, typography scale, spacing, radii, shadows, breakpoints and component variants.
5. Development Tasks — scope, files, status, acceptance criteria, risks and test status.
6. QA Center — responsive, accessibility, performance, SEO and functional checklist.
7. Handoff — changed files, tests, decisions, known issues and next steps.

Design direction: premium editorial workspace, calm neutral canvas, strong typography, precise grid, restrained single accent color, excellent density and readable data tables. Do not use a generic AI dashboard template, giant gradients, decorative blobs, glassmorphism everywhere, or repetitive cards.

Functional requirements:
- Real navigation and working CRUD for project and audit records.
- Useful empty, loading, validation and error states.
- Responsive from mobile to widescreen.
- Keyboard accessible controls and visible focus states.
- Persist data using an appropriate configured backend only after checking which services are enabled. If no backend is configured, use clearly labeled demo data and do not pretend it persists.
- Include export of audit reports to Markdown/JSON.
- Use server-side Gemini calls and the platform's secret management; do not hardcode keys.
- Include realistic sample project data clearly marked as demo.
- Add basic tests and verify build, main flows and responsive behavior.

First return a short architecture plan and inspect the current environment. Then implement the app in small increments and verify it. Do not deploy until explicitly requested.
