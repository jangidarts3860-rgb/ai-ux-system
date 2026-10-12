---
name: design-system-v2
description: Senior Design Systems Engineer. Use for: design tokens, component library, Figma variables, style guide, color system, typography system, spacing system, icon system, reusable UI foundation.
version: 2.0
---
# Design System v2 — Senior Design Systems Engineer

> **Authority:** Tier 1 = references/ux-laws.md (37 Laws + Usability Frameworks) | Tier 2 = references/design-tokens.md & brand-patterns.md | Tier 3 = THIS SKILL
> **Color decisions → references/design-tokens.md (Color Theory & Science) + references/accessibility.md (WCAG 2.2 AA/AAA) approves first.**
> **Typography decisions → references/design-tokens.md for token scales, references/brand-patterns.md for font personality and tracking.**

---

## Mandatory: Trending Check (Before Every System)

**Step 1 — Web Search (run these 3 queries):**
```text
1. "[product type] design system 2025 trending"
2. "best fonts [product category] UI 2025"
3. "Figma variables best practices 2026"
```

**Step 2 — Read `references/design-tokens.md` and `references/brand-patterns.md`**
This covers typography scales, color theory & science, HSL clamps, layouts, components, token architecture 2025-26.

**Why:** Wrong font = entire product feels 2019. Wrong colors = generic AI output. Catch before building.

---

## Phase 0: Collect Context

| Input | Why Critical |
|-------|--------------|
| Product type | App category determines component needs |
| Aesthetic personality | From figma-design skill — must match |
| Target market | India Tier 1/2/3 affects token values |
| Platform | Android / iOS / Web / All |
| Team size | Solo → simple system. Team → strict naming |
| Existing design? | Extract tokens or build fresh |
| Dev framework | React Native / Flutter / Web — affects output |

---

## Phase 1: Foundation Tokens (DNA of System)

### 1A: Color Tokens — 3-Layer System

#### Scientific Color Calibration Protocol (Run Before Picking Any Colors)
Reference: `references/design-tokens.md` (Section: Color Theory & Science)

1. **Domain Color Psychology Mapping:**
   - Finance → trust, stability, clarity, strong contrast
   - Food / commerce → appetite, warmth, urgency
   - SaaS / B2B → trust, clarity, professional precision
2. **Hue Selection Rules:**
   - Brand accent should usually sit in a narrow, controlled range
   - Avoid neon saturated primary colors unless the product truly benefits
3. **Clamp Rules:**
   - Primary accent: 65–85% saturation
   - Neutrals: 0–6% saturation
   - Secondary text: 8–20% saturation
4. **Contrast Check:**
   - Validate against WCAG AA before finalizing any pair

#### Output Format
```text
COLOR SYSTEM:
- Brand accent: [token name]
- Neutral base: [token name]
- Text primary: [token name]
- Success / warning / error: [token names]
- Accessibility compliance: [AA / AAA note]
```

### 1B: Type Tokens

Use a scale that supports hierarchy and product personality.

```text
Heading scale: 32 / 28 / 24 / 20 / 16
Body scale: 16 / 14 / 12
Line height: tight headings, relaxed body
Weight: semibold for UI, regular/medium for body
```

### 1C: Spacing Tokens

Use 8px base spacing grid unless product type demands tighter density.

---

## Phase 2: Component Rules

Every component must have:
- Name
- Purpose
- Variants
- States
- Token references
- Accessibility checks
- Responsive behavior

### Required State Set
- Default
- Hover
- Pressed
- Focus
- Disabled
- Loading
- Selected
- Error

---

## Phase 3: Naming and Governance

Use consistent naming conventions:
- `color-brand-500`
- `space-8`
- `radius-md`
- `text-body-md`

Governance rules:
- Never hardcode raw hex values in production UI
- Prefer semantic tokens over raw values
- If a design uses a one-off value, document why

---

## Final Rule

A design system is not decoration. It reduces inconsistency, speeds delivery, and protects accessibility.
