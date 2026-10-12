# Components — Complete Specification & Database

> Deep component specs with exact tokens, states, responsive rules, and Indian market patterns.
> Version: 3.0 | Updated: 2026-07-12

## Component Contract (Every Component Must Have)

| Field | Required | Description |
|-------|----------|-------------|
| **Name** | ✅ | Unique identifier (kebab-case) |
| **Purpose** | ✅ | One-sentence: what it does |
| **Anatomy** | ✅ | Visual parts with token refs |
| **Variants** | ✅ | Type × Size × State matrix |
| **Tokens** | ✅ | All visual properties → design tokens |
| **States** | ✅ | All 8 states with exact token changes |
| **Auto Layout** | ✅ | Direction, gap, padding, sizing |
| **Content Limits** | ✅ | Max chars, truncation rules, localization |
| **Responsive** | ✅ | Breakpoint behavior |
| **Accessibility** | ✅ | Role, labels, focus, touch target, ARIA |
| **Interaction** | ✅ | Hover, press, focus, loading, keyboard |
| **Owner** | ✅ | Design / Dev owner |
| **Code Counterpart** | ✅ | React/Vue/Flutter component name |

## Breakpoints

| Name | Width | Columns | Gutter | Margin | Use Case |
|------|-------|---------|--------|--------|----------|
| Mobile | 320-479px | 4 | 16px | 16px | Default (India mobile-first) |
| Mobile Large | 480-639px | 4 | 16px | 20px | Large phones |
| Tablet | 640-1023px | 8 | 24px | 24px | Tablets, foldables |
| Desktop | 1024-1439px | 12 | 24px | 32px | Laptops |
| Desktop Large | 1440px+ | 12 | 32px | 48px | Monitors |

## Final Rule

Components should be reusable, accessible, and system-aware.
