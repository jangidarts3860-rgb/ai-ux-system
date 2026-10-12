# Accessibility — WCAG 2.2 AA/AAA Compliance

> Non-negotiable. Overrides all aesthetic decisions. Run Layer 8 audit on every screen.
> Version: 3.0 | Updated: 2026-07-12

## WCAG 2.2 Quick Reference

| Principle | Guideline | Level | Key Criteria |
|-----------|-----------|-------|______________|
| **Perceivable** | 1.1 Non-text Content | A | Alt text, icons labeled |
| | 1.3 Adaptable | A | Semantic HTML, heading order |
| | 1.4 Distinguishable | AA | Contrast 4.5:1, resize text, reflow |
| **Operable** | 2.1 Keyboard | A | All functionality keyboard accessible |
| | 2.4 Navigable | A | Focus order, headings, labels |
| **Understandable** | 3.2 Predictable | A | Consistent navigation, no surprise |
| **Robust** | 4.1 Compatible | A | Valid HTML, ARIA, status messages |

## Layer 8 Checklist

### Color & Contrast
- [ ] **8.1** Normal text ≥4.5:1, Large text (≥18pt/14pt bold) ≥3:1 — *WCAG 1.4.3 AA*
- [ ] **8.2** Touch targets ≥44×44px (iOS) / ≥48×48dp (Android) / ≥56×56px preferred for India Tier 2/3 — *WCAG 2.5.8 AA*
- [ ] **8.3** Information NOT conveyed by color alone — add icon, label, pattern, underline — *WCAG 1.4.1 A*
- [ ] **8.4** Body font size ≥16px (14px absolute minimum) — *WCAG 1.4.4 AA*
- [ ] **8.5** Error states: NEVER only red — always icon + text + border — *WCAG 1.4.1 + 3.3.1*
- [ ] **8.6** Interactive elements have accessible labels (aria-label, aria-labelledby, `<label>`) — *WCAG 4.1.2 A*
- [ ] **8.7** Animations respect `prefers-reduced-motion` — *WCAG 2.3.3 AAA*
- [ ] **8.8** Tap targets spaced ≥8px apart — *WCAG 2.5.8*
- [ ] **8.9** Focus order logical (top-left → bottom-right) — *WCAG 2.4.3 A*
- [ ] **8.10** Focus indicator visible, ≥2px, ≥3:1 contrast — *WCAG 2.4.7 AA*
- [ ] **8.11** Language declared (`lang="en"`, `lang="hi"`) — *WCAG 3.1.1 A*
- [ ] **8.12** Heading hierarchy correct (h1→h2→h3, no skipping) — *WCAG 1.3.1 A*

## Focus Management

### Focus Order
1. Top-left → bottom-right (reading order)
2. Modal: Trap focus, first focusable element
3. Page change: Focus main `<h1>` or skip link
4. Toast: Don't steal focus, announce via live region

## Reduced Motion

### CSS Implementation
```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```
