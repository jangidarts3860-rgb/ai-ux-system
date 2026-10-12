# Design Tokens — Complete Reference

> Single source of truth for all design decisions. Used by Figma Variables, CSS, JSON, React Native.
> Version: 3.0 | Updated: 2026-07-12

## Token Architecture — 3-Layer System

```
┌─────────────────────────────────────────────────────────────┐
│  LAYER 3: COMPONENT TOKENS (Specific)                       │
│  button-primary-bg, input-border-focus, card-shadow-hover   │
│  ↑ aliases ↑                                                │
│  LAYER 2: SEMANTIC TOKENS (Purpose-driven)                  │
│  color-action-primary, color-surface-card, space-4, radius-md │
│  ↑ aliases ↑                                                │
│  LAYER 1: PRIMITIVE TOKENS (Raw values)                     │
│  color-brand-500, color-neutral-900, space-16, radius-8     │
└─────────────────────────────────────────────────────────────┘

RULE: Components ONLY use Layer 3. Layer 3 aliases Layer 2. Layer 2 aliases Layer 1.
```

## Spacing Tokens (8pt Grid — Strict)

| Token | Value | Rem | Usage |
|-------|-------|-----|-------|
| `space-1` | `4px` | `0.25rem` | Micro: icon+label gap |
| `space-2` | `8px` | `0.5rem` | Small: list item gap, icon padding |
| `space-3` | `12px` | `0.75rem` | Compact padding |
| `space-4` | `16px` | `1rem` | **Medium: component padding** |
| `space-6` | `24px` | `1.5rem` | **Large: card padding** |
| `space-8` | `32px` | `2rem` | **XL: section gap** |

## Border Radius Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | `0px` | Sharp corners, dividers |
| `radius-sm` | `4px` | Badges, tags, small chips |
| `radius-md` | `8px` | **Buttons, inputs, small cards** |
| `radius-lg` | `12px` | **Cards, dropdowns, popovers** |
| `radius-xl` | `16px` | **Modals, drawers, bottom sheets** |
| `radius-full` | `9999px` | Pills, avatars, FABs, tags |
