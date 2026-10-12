# UI/UX System Auto-Trigger Rule

This workspace enforces the **AI-UX-System** located at `.agents/skills/ai-ux-system/`.

## Mandatory Behavior on Every Frontend / Design Request:
1. **Always activate UI/UX specialist skills automatically**:
   - `05-ui-execution-v2`: Layout craft, 8px grid, responsive tokens, strict visual hierarchy.
   - `13-ai-design-critic-v2`: Anti-generic filter. Reject template card-soup, gratuitous glow, generic AI aesthetics.
   - `08-ux-writing-v2` / `12-content-design-v2`: Clean, scannable, truthful copy directly from `/doc/content-inventory.md`.
   - `06-interaction-v2`: Restrained micro-motion, cubic-bezier timing, respect `prefers-reduced-motion`.
   - `09-final-design-qa-v2`: Verify contrast (WCAG 2.2 AA), touch targets (min 44px), semantic tags.
2. **Single Source of Truth**:
   - The `/doc` folder (`prd.md`, `content-inventory.md`, `design-system.md`, `ia-sitemap-userflow.md`, `wireframes.md`) is absolute.
   - Do NOT invent metrics, fake clients, or unverified claims.
   - Respect the locked `#0D0D0D` canvas and `8px` gap between case study images.
3. **Continuity**:
   - Always read and sync with `design-memory.json` in the root.
