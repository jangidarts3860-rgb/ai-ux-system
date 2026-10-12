---
name: analytics-measurement-v2
description: Senior Product Analyst. Defines success metrics, North Star, guardrails, experiment design, A/B test framework, post-launch tracking, funnel analysis, cohort analysis. Trigger: "metrics", "tracking", "analytics".
version: 2.0
---
# Analytics & Measurement v2 — Senior Product Analyst

> **Hierarchy:** Tier 1 = ux-thinking | Tier 2 = design-taste-frontend | Tier 3 = THIS SKILL
> **When to use:** Define metrics BEFORE design. Track AFTER launch. Experiment for decisions.

---

## Metric Hierarchy (Define in Order)

### 1. North Star Metric (The ONE Number)
> The single metric that best captures core value delivered to users.
> **Format:** "[Action] per [User] per [Time]"
> **Examples:**
> - FinTech: "Successful transactions per active user per month"
> - Food Delivery: "Completed orders per user per week"
> - EdTech: "Lessons completed per learner per month"
> - Social: "Daily active users who send ≥1 message"

### 2. Primary Metrics (3-5 max)
> Directly tied to North Star. Move these → North Star moves.
> - Activation: % users completing [key action] within [time]
> - Retention: Day 1 / Day 7 / Day 30 retention
> - Engagement: [Core action] per session
> - Monetization: Revenue per paying user / ARPU

### 3. Guardrail Metrics (Must NOT Get Worse)
> Safety rails. If these regress → stop/rollback.
> - Support ticket volume
> - App crash rate
> - Onboarding drop-off rate
> - Payment failure rate
> - Page load time (LCP)

### 4. Anti-Metrics (Explicitly NOT Optimized)
> "We don't optimize for X because it conflicts with [value]."
> - Session length
> - Page views
> - Notification opens

---

## Final Rule

Measure the user value, not just the screen activity.
