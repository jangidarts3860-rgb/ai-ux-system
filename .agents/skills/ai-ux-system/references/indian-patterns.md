# India Market Patterns — UX for Bharat

> Mobile-first, Tier 2/3 optimized, trust-first, bilingual-ready patterns.
> Version: 3.0 | Updated: 2026-07-12

## Market Reality

| Metric | Value | Implication |
|--------|-------|-------------|
| Mobile Traffic | 85%+ | Mobile-first ALWAYS |
| Android Share | 95%+ | Optimize for budget Android (2GB RAM, 720p) |
| Network | 4G dominant, 2G/3G fallback | Offline-first, skeleton screens, <100KB critical path |
| Languages | 22 official, 100+ spoken | Hindi + English minimum, regional for Tier 2/3 |
| Literacy | ~77% overall, lower digital | Icon + text, voice, simple flows |
| Payment | UPI 75%+ of digital | UPI-first, never card-only |
| Trust | Low for new apps | Social proof, badges, transparency |

## Tier-Based Design Strategy

### Tier 1 (Metros: Delhi, Mumbai, Bangalore, etc.)
- English comfortable
- High-end devices (iPhone, flagship Android)
- 5G/strong 4G
- Can handle density, advanced features

### Tier 2 (State capitals, 1M+ pop)
- Bilingual (Hindi + English)
- Mid-range Android (6-8GB RAM)
- 4G mostly reliable
- Need Hindi labels, voice support

### Tier 3 (Small towns, <1M pop)
- Hindi/regional primary
- Budget Android (2-4GB RAM, 720p)
- Patchy network, frequent offline
- Voice, icons, minimal text, offline-first
- Larger touch targets (56px)

## UPI Payment Flow (Critical)

### Standard UPI Flow
```
[Amount Screen] → [UPI App Selector] → [UPI App Opens] → [PIN Entry] → [Success/Fail] → [App Returns]
```

## Bilingual Layout (Hindi + English)

### Text Expansion Rules
| Language | Expansion Factor | Line Height |
|----------|------------------|-------------|
| English | 1.0x (base) | 1.5 |
| Hindi | 1.3-1.5x | 1.6-1.8 |

### Implementation Rules
- [ ] **Never auto-translate** — human-verified Hindi only
- [ ] **Technical terms stay English**: OTP, UPI, PIN, KYC, App, Login, Settings, Notification
- [ ] **Action/emotional copy in Hindi**: "भुगतान करें" not "Pay ₹1,299"
- [ ] **Numbers**: Indian format `₹1,23,456` (lakhs/crores)
- [ ] **Date**: DD/MM/YYYY (not MM/DD/YYYY)
- [ ] **Font**: Noto Sans Devanagari Variable (Google Fonts, free)
- [ ] **Line height**: Hindi 1.6x minimum
- [ ] **Test at 200% zoom** — Hindi wraps differently
