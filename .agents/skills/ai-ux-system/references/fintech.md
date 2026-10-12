# Fintech UX and Trust Reference
Version: 3.0 | Updated: 2026-09-09

## First principle
Financial UX must be truthful, precise, reversible where possible, and technically feasible. Never let visual confidence imply a guarantee the product cannot provide.

## Capability language
Distinguish clearly:
- Detected: the system noticed a signal.
- Flagged: the system recommends review.
- Verified: defined checks passed at a stated time.
- Authorized: user or institution approved an action.
- Processed: the product or partner executed it.
- Protected/guaranteed: use only when contractually and technically true.

Do not say "RBI certified," "bank grade," "AI guaranteed," "blocked," "cancelled," or "works offline" without verified scope and authorization.

## Money clarity
- Show exact amount, currency, payer, payee, account, fees, schedule, and timestamp before confirmation.
- Use one canonical data source so amounts and statuses match across screens.
- Separate available balance, due amount, projected cost, savings, and historical spend.
- Format Indian currency correctly and localize dates/times.

## Transaction states
Design distinct states for draft, authentication required, processing, pending, successful, failed, reversed/refunded, expired, and duplicated request.

## Indian Rupee (₹) Optical Typography & Currency Math

### 1. Lakh & Crore Grouping System
Never format Indian Rupees using standard Western million/billion groupings:
- **Correct (Indian System):** `₹1,23,456.78` | `₹12,34,567.00` | `₹1,23,45,678.50`
  - Pattern: First comma after 3 digits from right, subsequent commas after every 2 digits.
- **Incorrect (Western System):** `₹123,456.78` | `₹1,234,567.00` | `₹12,345,678.50`

### 2. Typographic Hierarchy for Financial Balances
- **The Currency Symbol (₹):** Set at 75%–85% of the integer font size. Optically align to the cap-height of numbers.
- **Paisa Decimals:** If `.00`, either omit in high-level dashboards or mute color at 60%–70% size.
- **Negative Balances & Debits:** Never rely on red color alone. Always prefix with a minus sign or explicit label: `-₹450.00` or `Debited ₹450.00`.
