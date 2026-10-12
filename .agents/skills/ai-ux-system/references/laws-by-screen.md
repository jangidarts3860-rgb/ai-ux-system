# Laws by Screen Type — Auto-Activation + Checklists

> **Read this when starting any screen design.** Auto-activates relevant laws from `ux-laws.md`.
> Version: 3.0 | Updated: 2026-07-12

## Quick Reference: Screen Type → Laws

| Screen Type | Primary Laws (Auto-Activate) | Secondary Laws |
|-------------|------------------------------|----------------|
| **Navigation / Menu** | Hick's, Serial Position, Jakob's, Progressive Disclosure, Paradox of Choice | Fitts's (tap targets), Closure (scroll hint), Similarity (consistent style) |
| **Button / CTA** | Fitts's, Affordance, Von Restorff, Color Psychology, Weber's Law | Doherty (feedback <100ms), Microinteractions, Aesthetic-Usability |
| **Form** | Miller's, Tesler's, Error Prevention (Nielsen H5), Postel's, Cognitive Load | Zeigarnik (progress), Goal Gradient (completion), Dual Coding (labels+icons) |
| **Onboarding** | Zeigarnik, Goal Gradient, Fogg (M×A×P), Doherty, Peak-End, Dual Coding | Serial Position (first/last screens), Social Proof, Hook Model Trigger |
| **Product Listing** | Proximity, Similarity, Common Region, Closure, Social Proof, Paradox of Choice | Fitts's (card tap), Serial Position (top items), Figure-Ground (card separation) |
| **Checkout / Payment** | Tesler's, Error Prevention, Doherty, Shneiderman Closure, Trust Signals, Goal Gradient | Fitts's (pay button), Color Psychology (green=success), Weber's (state changes) |
| **Empty State** | Fogg Model (Prompt), Zeigarnik (incomplete), Affordance, Dual Coding | Peak-End (delight), Social Proof (others' content), Progressive Disclosure |
| **Notification** | Hook Model Trigger, Fogg Prompt, Scarcity (honest only) | Doherty (immediate), Peak-End (tone), Color Psychology (red=urgent) |
| **Dashboard** | Miller's (7±2 widgets), Proximity, Figure-Ground, F-Pattern, Aesthetic-Usability, Dual Coding | Serial Position (top-left priority), Von Restorff (1 highlight), Closure (scroll) |
| **Error Screen** | Nielsen H9, Don Norman Feedback, Postel's, Cognitive Load | Fitts's (retry button), Color Psychology, Dual Coding |
| **Fintech Screen** | Trust Signals, Tesler's, Error Prevention, Cognitive Load, Scarcity (honest) | Color Psychology (Green=UPI/money), Goal Gradient, Dual Coding, Serial Position |

## Activation Protocol for Agents

```
WHEN USER SAYS: "Design a [screen type]"
1. LOOK UP screen type in table above
2. LOAD primary laws + secondary laws from ux-laws.md
3. RUN screen-specific checklist
4. OUTPUT: Law-backed decisions with Severity + Brain Note
5. FLAG any conflicts → resolve via Conflict Hierarchy
```
