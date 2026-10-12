---
name: ai-ux-system
description: Coordinated UI/UX design, research, audit, and validation framework. Activates on UI/UX reviews, heuristic audits, design audits, product flows, and screen styling requests.
---

# AI UX System: Master Instructions
Version: 3.0 | Updated: 2026-07-18 | 16 active skills + 16 references

## What this is
This package turns any capable AI into a coordinated UX product team. Skills are workflow modules. References are knowledge modules. The AI must self-route: read this file, detect intent, and load[...]the matched skills, then only the matched references.

## Absolute start rule
On ANY design, UX, UI, research, product, or frontend request:
1. Silently read this file.
2. Read `skills/00-ux-orchestrator-v2.md` (or `.agents/skills/ai-ux-system/skills/00-ux-orchestrator-v2.md`).
3. Classify the request using the Auto-Trigger Map below.
4. Load only the matched skills, then only the matched references.
5. Execute. Run the final QA gate before delivery.

Do not ask the user which skill to use. Do not load everything. The right context beats more context.

## The 16 active skills
Core workflow (stored at `skills/` or `.agents/skills/ai-ux-system/skills/`):
- `00-ux-orchestrator-v2` : routing, shared context, conflict resolution, final gates
- `01-ux-research-v2` : research, evidence, personas, journeys
- `02-product-strategy-v2` : scope, IA, flows, metrics, assumptions
- `03-ux-audit-v2` : heuristics, safety, accessibility, consistency review
- `04-design-system-v2` : tokens, components, governance
- `05-ui-execution-v2` : screens, Figma, responsive UI
- `06-interaction-v2` : motion, gesture, haptics, prototype behavior
- `07-ux-validation-v2` : usability, comprehension, accessibility testing

Specialists (stored at `skills/` or `.agents/skills/ai-ux-system/skills/`):
- `08-ux-writing-v2` : labels, errors, empty states, financial copy, error resilience, empty state copy formulas
- `09-final-design-qa-v2` : final consistency and truthfulness gate
- `10-technical-feasibility-v2` : can it be built and is the claim true
- `11-analytics-measurement-v2` : events, funnels, metrics, experiments
- `12-content-design-v2` : information hierarchy, taxonomy, content models
- `13-ai-design-critic-v2` : anti-generic, distinctiveness gate

Pattern packs (stored at `skills/` or `.agents/skills/ai-ux-system/skills/`):
- `14-product-patterns-v2` : IA/navigation, onboarding, trust/safety, privacy/consent, retention, service journey
- `15-ui-patterns-v2` : responsive, forms/auth, search, data viz, notifications, developer handoff

## 16+ references (load on demand)
Located in `references/` (or `.agents/skills/ai-ux-system/references/`):
`ux-laws`, `ux-audit-checklist`, `laws-by-screen`, `design-tokens`, `accessibility`, `platform-ios`, `platform-android`, `platform-specific`, `indian-patterns`, `fintech`, `components`, `motion`, and more.

## Global quality rules
- Never present assumptions as facts. Label confirmed, inferred, or unknown.
- Never invent research, approval, certification, integrations, or product capability.
- Do not force every law, state, edge case, or animation into every task.
- Prefer familiar platform behavior unless evidence supports deviation.
- Avoid generic AI UI: card soup, nested cards, random glow, copied brands, gradient text, emoji icons, category-cliche palettes.
- One clear primary action per state.
- Always test real content, long text, loading, error, permission denial, interruption, and accessibility where relevant.
