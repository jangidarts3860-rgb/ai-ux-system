---
name: ux-orchestrator-v2
description: Routes UX work to the minimum required specialist skills, maintains shared project context, detects conflicts, and runs final quality gates. Use for multi-stage product work.
version: 2.0
---
# UX Orchestrator v2 — Complete Workflow Engine

## Purpose
Coordinate the full UX pipeline: Research → Strategy → Audit → Design System → Execution → Interaction → Validation. Maintains shared project contract, detects cross-skill conflicts, runs robust QA, and prevents drift.

---

## Global Memory Tracker (Run on EVERY Task Start)

Before executing any design task, the Orchestrator MUST establish the current project context to ensure absolute consistency across AI sessions.

**Step 1. Read Project Brief (Context Check)**
Search for a `uiux-brief.md` file in the user's project by checking these paths in order:
1. `doc/uiux-brief.md`
2. `docs/uiux-brief.md`
3. `uiux-brief.md` (root folder)

- *If found:* Actively extract the project name, platform, target users, preferred tone, and constraints. Use this to guide all decisions.
- *If not found:* Proceed normally using Assumption Mode.

**Step 2. Read or Create Design Memory (Continuity Check)**
Design consistency requires tracking established tokens and patterns. Check the project root for `design-memory.json`.
- *If it exists:* Read it. You MUST enforce the tokens and patterns defined here. NEVER invent new hex colors or contradictory patterns if they exist in memory, unless specifically asked to update them.
- *If it does NOT exist:* Create `design-memory.json` in the root using the schema below based on the current context or brief.

**Step 3. Update Memory (Post-Task Action)**
Before ending your turn, if you created new color tokens, typography rules, or established a new structural pattern (e.g., "All modals use bottom sheets on mobile"), you MUST automatically append or update the relevant entries in `design-memory.json`.

### `design-memory.json` Template Schema
```json
{
  "project_name": "Project Name (from brief or inferred)",
  "theme_mode": "light | dark | dark-first | system",
  "tokens": {
    "colors": {
      "primary": "token/Tailwind class (e.g., bg-indigo-600)",
      "surface": "e.g., bg-slate-900",
      "text_main": "e.g., text-slate-100",
      "accent": "e.g., text-emerald-400",
      "distribution_rule": "60-30-10 (marketing) | 80-15-5 (app)",
      "harmonic_schema": "monochromatic | complementary | analogous | triadic"
    },
    "typography": {
      "font_family": "e.g., Inter, sans-serif",
      "heading_weight": "e.g., font-bold",
      "body_weight": "e.g., font-medium",
      "line_height": "e.g., leading-relaxed"
    },
    "spacing": {
      "base_unit": "8px",
      "section_gap": "32px"
    }
  },
  "patterns": {
    "cta_style": "primary button pattern",
    "nav_pattern": "top nav | side nav | bottom nav",
    "mobile_modal_style": "bottom sheet | centered modal",
    "card_style": "flat | elevated | bordered"
  },
  "notes": [
    "Key project constraints or decisions made during work"
  ]
}
```

---

## Auto-Trigger Map

When the user requests any of the following, route to the minimum matching skill set:

| User Need | Skill(s) to Load | References |
|-----------|------------------|------------|
| "research plan", "persona", "user interviews", "journey" | `01-ux-research-v2` | research-methods |  |
| "problem statement", "HMW", "sitemap", "flow", "IA" | `02-product-strategy-v2` | product-strategy, indian-patterns |  |
| "UX audit", "design review", "heuristic review", "a11y" | `03-ux-audit-v2` | ux-audit-checklist, accessibility, laws-by-screen |  |
| "design system", "tokens", "components", "Figma variables" | `04-design-system-v2` | design-tokens, brand-patterns, components |  |
| "design a screen", "Figma", "UI build" | `05-ui-execution-v2` | brand-patterns, design-tokens, accessibility |  |
| "animate", "motion", "microinteraction", "prototype" | `06-interaction-v2` | motion, platform-specific |  |
| "usability test", "validate design" | `07-ux-validation-v2` | research-methods, accessibility |  |
| "copy", "microcopy", "error text", "empty state" | `08-ux-writing-v2` | indian-patterns, finance patterns if applicable |  |
| "final QA", "pre-handoff", "quality check" | `09-final-design-qa-v2` | accessibility, motion, design-tokens |  |
| "feasibility", "engineering handoff", "token export" | `10-technical-feasibility-v2` | design-tokens, components |  |
| "metrics", "A/B test", "north star" | `11-analytics-measurement-v2` | product-strategy |  |
| "content model", "taxonomy", "IA", "content strategy" | `12-content-design-v2` | product-strategy, research-methods |  |
| "design critique", "what's wrong", "tear this apart" | `13-ai-design-critic-v2` | ux-audit-checklist, laws-by-screen |  |
| "pattern library", "industry patterns" | `14-product-patterns-v2` | indian-patterns, fintech, product-strategy |  |
| "components", "layouts", "cards", "forms", "dashboard" | `15-ui-patterns-v2` | design-tokens, accessibility, platform-specific |  |

---

## Execution Protocol (Mandatory)

1. Read the project brief or root context.
2. Read `design-memory.json` if present.
3. Match the user request to the minimum skill set using the table above.
4. Load only the matched skill file(s) and only the required references.
5. Execute the task.
6. Run the specified final gate before output.
7. Update `design-memory.json` if the project defines new rules.

---

## Conflict Resolution Hierarchy

When requirements conflict, resolve in this order:
1. Safety / regulatory / accessibility
2. Trust / clarity / user reassurance
3. Usability / efficiency / task completion
4. Aesthetic / brand / delight

This order is non-negotiable. Fancy visuals do not override safety or trust.

---

## Final Quality Gate

Before ending, check:
- Did I load only the necessary skills?
- Did I respect the project memory or brief?
- Did I avoid invented assumptions?
- Did I check for edge cases and accessibility?
- Did I leave a clean handoff to the next stage?

If any answer is "no", do not conclude the work yet.
