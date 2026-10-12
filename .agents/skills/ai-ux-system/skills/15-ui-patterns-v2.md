---
name: product-patterns-v2
description: Product Pattern Library — Real-world patterns by industry. FinTech, Food Delivery, E-commerce, SaaS, Social, Health, EdTech. Onboarding, checkout, search, settings, notifications, empty states, trust patterns.
version: 2.0
---
# Product Patterns v2 — Industry Battle-Tested Patterns

> **Source:** 100+ product analyses, canonical UX laws (`references/ux-laws.md`), Indian market reality (`references/indian-patterns.md`).
> **Use:** Don't invent. Apply. Adapt only with evidence.

---

## FinTech Patterns (India Context)

### Onboarding (KYC + Trust)
```text
FLOW: Splash → Language → Value Prop → Phone → OTP → KYC (PAN/Aadhaar) → MPIN → Success
PATTERNS:
- Progressive disclosure: One question per screen
- Auto-read OTP (SMS Retriever API) + manual fallback
- DigiLocker / CKYC integration for instant KYC
- MPIN creation: 6-digit, confirm, biometric opt-in
- Trust signals throughout: "RBI Licensed", "₹1L insurance", "10M+ users"
```

### Money Transfer (UPI-First)
```text
FLOW: Amount → Recipient (UPI ID/Contact/QR) → Review → UPI PIN → Success
PATTERNS:
- UPI apps detected → show logos (GPay, PhonePe, Paytm, BHIM)
- Amount visible BEFORE UPI app switch
- Recipient verification: Name + last 4 of UPI ID
- "Request Money" as separate flow (not mixed)
- Failure: Specific error ("Insufficient balance") + retry
```

---

## Final Rule

Patterns are templates, not magic. Adapt them to real context and evidence.
