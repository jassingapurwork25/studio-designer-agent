# Web Design Agent — Professional / Agency Level

Bu paket Google AI Studio'dagi **Playground → Agents** rejimiga moslab tayyorlangan web design agent konfiguratsiyasidir.

Agentning vazifasi: mavjud web-saytni audit qilish, UX/UI redesign strategiyasini ishlab chiqish, frontend kodga joriy etish va sifatini tekshirish.

## Ichidagi fayllar

```text
.agents/
  AGENTS.md
  skills/
    project-discovery/SKILL.md
    research-benchmark/SKILL.md
    design-audit/SKILL.md
    ux-architecture/SKILL.md
    creative-direction/SKILL.md
    design-system/SKILL.md
    frontend-development/SKILL.md
    responsive-accessibility/SKILL.md
    qa-performance/SKILL.md
    handoff/SKILL.md
knowledge/
  00-knowledge-index.md ... 09-security-privacy.md
templates/
  project-brief.md
  audit-report.md
  design-review.md
  acceptance-checklist.md
prompts/
  audit, redesign, implementation, responsive QA, polish, handoff prompts
AI_STUDIO_SETUP_UZ.md
```

## Tez boshlash
1. ZIP'ni oching.
2. Google AI Studio → Playground → Agents'ga o'ting.
3. Google Search, URL Context, Code Execution va Filesystem Tools'ni yoqing.
4. Environment → Add Sources orqali `.agents/` fayllari, `knowledge/`, `templates/`, `prompts/`'ni ulang.
5. Birinchi xabarni `AI_STUDIO_SETUP_UZ.md` dagi test prompt bilan yuboring.
6. Sayt auditi uchun `prompts/01-audit-existing-site.md` dan boshlang.

To'liq o'rnatish va xavfsizlik yo'riqnomasi: `AI_STUDIO_SETUP_UZ.md`.
