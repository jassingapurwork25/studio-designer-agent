---
name: project-discovery
description: Clarify a digital product brief, users, goals, constraints, scope and success criteria before audit or design work.
---
# Project Discovery

## Trigger
Use for new website/app projects, unclear briefs, redesign kickoffs, and when requirements are scattered across messages or files.

## Workflow
1. Inspect supplied files, current website, screenshots, design references, and existing code before asking questions.
2. Extract: product purpose, audience, top tasks, conversion/action, content, page list, language, brand constraints, accessibility needs, device priorities, integrations, deadlines, technical stack, and acceptance criteria.
3. Classify each item as **confirmed**, **assumed**, or **unknown**.
4. Identify the highest-risk unknowns. Ask no more than one essential question at a time; otherwise proceed with clearly stated assumptions.
5. Create or update `workspace/PROJECT_BRIEF.md` from `templates/project-brief.md` if filesystem access is available.
6. Propose a scoped plan with deliverables and explicit out-of-scope items.

## Output
- Project summary
- Primary audience and top user journeys
- Sitemap/page inventory
- Functional and content requirements
- Brand and technical constraints
- Confirmed facts vs assumptions
- Success criteria and acceptance tests
- Risks, dependencies, and next step

## Rules
- Do not invent business goals, audience research, analytics, or customer evidence.
- Do not ask for details already present in the conversation or uploaded material.
- Avoid premature technology decisions; inspect the existing project first.
