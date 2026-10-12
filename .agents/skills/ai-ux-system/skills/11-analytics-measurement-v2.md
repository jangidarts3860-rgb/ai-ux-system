---
name: technical-feasibility-v2
description: Senior Design Engineer. Developer handoff specs, token JSON/CSS export, component anatomy, Figma-to-code mapping, implementation feasibility review. Trigger: "dev handoff", "token JSON", "component spec".
version: 2.0
---
# Technical Feasibility v2 — Developer Handoff Specs

> **Hierarchy:** Tier 1 = ux-thinking | Tier 2 = design-taste-frontend | Tier 3 = THIS SKILL
> **This skill produces developer-ready specs.** No ambiguity.

---

## Component Anatomy Spec (Every Component)

```text
COMPONENT: [Name]

ANATOMY:
├── Container (bg, border, radius, padding)
├── Label (typography token, color token)
├── Icon (optional, size, position)
└── [Other parts]

TOKEN REFERENCES:
├── background: [semantic token]
├── text: [semantic token]
├── border: [semantic token]
└── [all visual properties → token names]

AUTO LAYOUT:
Direction: Row / Column
Gap: [space token]
Padding: T[space] R[space] B[space] L[space]
Sizing: Hug / Fill / Fixed [px]

INTERACTIONS:
Hover:   [change] | [duration] | [easing]
Press:   [change] | [duration] | [easing]
Focus:   [focus ring + color + size]
Loading: [skeleton / spinner / progress]

ACCESSIBILITY:
Role: [ARIA role]
Label: [aria-label pattern]
Keyboard: [Tab / Enter / Space / Escape]
Min touch target: [44px / 56px]
```

---

## Final Rule

If it cannot be implemented clearly, it is not yet ready.
