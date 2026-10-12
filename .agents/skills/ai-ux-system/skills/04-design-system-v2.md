---
name: ux-audit-v2
description: Senior UX Auditor. Run 8-layer heuristic audit on any design. Use for: "UX audit karo", "design review", "heuristic check", "accessibility audit", "dark pattern check", "design kya galat hai".
version: 2.0
---
# UX Audit v2 — 8-Layer Heuristic Audit

> **Source of Truth:** `references/ux-laws.md` (37 Laws + 4 Frameworks + Conflict Hierarchy)
> **This skill executes audits.** Laws come from `references/ux-laws.md`. Anti-patterns and complete 8-layer checklists come from `references/ux-audit-checklist.md`.

---

## Activation Protocol

When user says: "UX audit karo", "design review", "check accessibility", "dark pattern check":
1. **CONTEXT**: Identify Platform, Industry, Screen type, User type, Goal.
2. **LAWS**: Activate laws specific to that screen type.
3. **CONFLICT**: Resolve any clashes strictly by the Priority Hierarchy (P1 Safety > P2 Trust > P3 Usability > P4 Aesthetic).
4. **VALIDATE**: Run the full 8-layer checklist below.
5. **OUTPUT**: Present using the strict Law-Backed Findings format.

**Output Format:** Every finding must use:
```text
FINDING: [What's wrong]
SEVERITY: Critical (blocks task) | High (damages UX) | Medium (friction) | Low (polish)
EFFORT: Quick win (<1hr) | Medium (1 day) | Big change (1 week+)
LAW: [Specific law from ux-thinking — e.g., "Law 5: Doherty Threshold"]
SCREEN: [Screen ID or description]
FIX: [Exact change — no vague words]
BRAIN NOTE: [1-sentence psychology — why user brain responds this way]
```

---

## Context Identification Matrix (Before Audit)

| Check | Variants | Impact on Audit |
|-------|----------|-----------------|
| **Platform** | Mobile / Web / Tablet | Mobile needs 44px targets, Web needs F-pattern/Hover. |
| **Industry** | Food / E-commerce / Fintech | Fintech demands extra trust + zero-ambiguity checks. |
| **Screen Type** | Form / Nav / View / Dashboard | Dictates which laws are actively scrutinized. |
| **User Type** | Novice / Power User / Elderly | Need for shortcuts, dual-coding, or huge text. |
| **Mode** | Regular / Case Study / Portfolio | If Case Study, justify each fix with "Decision Justification" format. |

---

## Layer 1: Speed & Efficiency

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 1.1 | Nav items ≤5? Progressive disclosure for more? | Hick's Law | Critical | | |
| 1.2 | Primary CTA = full-width, thumb zone (bottom 1/3), 56px height mobile? | Fitts's Law | Critical | | |
| 1.3 | Loading states for ALL async ops? Skeleton screens? No blank >400ms? | Doherty Threshold | Critical | | |
| 1.4 | Options causing paralysis? Reduced to essentials + smart defaults? | Paradox of Choice | High | | |
| 1.5 | Top 20% tasks reachable in ≤3 taps from home? | Pareto Principle | High | | |
| 1.6 | Search/filter available when list >20 items? | Hick's Law | Medium | | |

---

## Layer 2: Memory & Brain

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 2.1 | Max 7 items per section/group? Forms broken into steps ≤7 fields? | Miller's Law | Critical | | |
| 2.2 | Progress visible in multi-step flows (stepper, bar, % complete)? | Zeigarnik Effect | Critical | | |
| 2.3 | Suggestions/recents shown? No blank inputs requiring pure recall? | Recognition > Recall | Critical | | |
| 2.4 | Extraneous complexity removed? Smart defaults set (location, currency, language)? | Cognitive Load Theory | High | | |
| 2.5 | Critical info = text + visual together (icon, illustration, chart)? | Dual Coding Theory | High | | |
| 2.6 | Chunking used for long numbers (phone: +91 98765 43210, card: 1234 5678 9012 3456)? | Miller's Law | Medium | | |

---

## Layer 3: Visual Organization (Gestalt)

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 3.1 | Related elements grouped tightly (8px internal gap, 24px between groups)? | Proximity | Critical | | |
| 3.2 | Same function = same visual style (primary buttons, cards, icon weights)? | Similarity | Critical | | |
| 3.3 | Cards/borders/backgrounds define clear groups? No floating elements? | Common Region | Critical | | |
| 3.4 | Visual hierarchy obvious? One main action, one object of focus? | Figure-Ground | High | | |
| 3.5 | Data tables/forms aligned in rows/cols? | Continuity | Medium | | |
| 3.6 | User reading scan matches layout logic? | F-pattern / Z-pattern | Medium | | |

---

## Layer 4: Content & Language

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 4.1 | Labels clear and specific? No jargon without context? | Plain Language | Critical | | |
| 4.2 | Error text explains cause + next step? | Error Prevention | Critical | | |
| 4.3 | Empty states instructive, not blank? | Fogg / Supportive UI | High | | |
| 4.4 | Copy matches mental model of user? | Cognitive Alignment | High | | |
| 4.5 | Yes/No labels not confusing? | Lexical Clarity | Medium | | |

---

## Layer 5: Trust & Safety

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 5.1 | Money or sensitive action states clear? | Trust Signals | Critical | | |
| 5.2 | No hidden costs or fees? | Transparency | Critical | | |
| 5.3 | Users can cancel / undo / recover? | Reversibility | High | | |
| 5.4 | No scary or manipulative urgency? | Scarcity / Pressure | High | | |
| 5.5 | Security/privacy language honest and specific? | Trust & Safety | Medium | | |

---

## Layer 6: Accessibility & Inclusion

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 6.1 | Contrast meets WCAG 2.2 AA? | WCAG | Critical | | |
| 6.2 | Tap targets >=44px; 56px preferred? | Fitts's / WCAG | Critical | | |
| 6.3 | Focus states visible and keyboard operable? | Focus Order | Critical | | |
| 6.4 | Labels for inputs, not just placeholders? | Accessible Name | High | | |
| 6.5 | Reduced motion respected? | Motion Safety | High | | |

---

## Layer 7: Dark Patterns & Manipulation Check

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 7.1 | Is there forced continuity or deceptive urgency? | Dark Pattern Detection | Critical | | |
| 7.2 | Misleading default states or hidden costs? | Transparency | Critical | | |
| 7.3 | No pressure to act without understanding? | Consent + Clarity | High | | |
| 7.4 | Claims not misleading / unverified? | Truthfulness | High | | |

---

## Layer 8: Final QA & Handoff Readiness

| # | Check | Law | Severity | Screen | Notes |
|---|-------|-----|----------|--------|-------|
| 8.1 | Edge states designed: loading / empty / error / success? | Error Prevention | Critical | | |
| 8.2 | Core flow tested for mobile and desktop behavior? | Responsive Design | High | | |
| 8.3 | Design tokens and component consistency applied? | Consistency | High | | |
| 8.4 | Developer handoff notes are complete? | Handoff Clarity | Medium | | |

---

## Final Rule: Do Not Ship Broken UX

If a design fails any critical layer, the audit cannot be passed. Fix the problem before final handoff.
