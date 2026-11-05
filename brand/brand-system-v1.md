# Product Brand System v1

Status: BRAND NAME PENDING FORMAL CLEARANCE
Internal engineering codename: Foundry (must never ship as customer-facing brand)

## Brand posture

The product is an enterprise operating layer for governed AI workforces. The identity must communicate controlled capability, authority, accountability and economic precision. It must not inherit any ETERNIMA visual language, palette, typography, motifs or naming logic.

## Visual principles

1. Institutional precision over AI spectacle.
2. Dense operational information must remain calm and legible.
3. Authority state is visible before action state.
4. Cost and risk are first-class UI information, never hidden in settings.
5. No robots, brains, neural-network illustrations, glowing orbs, infinity marks, hexagon clichés or decorative pseudo-data.
6. Motion explains state transitions; it is never ornamental.
7. Customer surfaces are light-first with controlled dark command surfaces where density benefits from it.

## Core palette

The palette is intentionally unrelated to ETERNIMA black/gold.

- Ink 950: `#10151B` — primary text / command surfaces
- Slate 800: `#26313D` — secondary command surfaces
- Paper 050: `#F6F8F7` — application background
- Paper 000: `#FFFFFF` — elevated surfaces
- Line 200: `#D9E0DF` — structural borders
- Signal Cyan 600: `#007C91` — primary interactive/action color
- Signal Cyan 100: `#DDF3F5` — selected/active wash
- Authority Violet 600: `#6257A8` — authority/approval semantics only
- Success 600: `#19704B`
- Warning 600: `#9A6500`
- Danger 650: `#A63838`

Never use semantic colors as decorative brand gradients.

## Typography

Use a neutral, high-legibility grotesk for product UI and a restrained display grotesk for marketing headings. The implementation must use legally licensed/self-hostable fonts or system fallbacks; font files are not committed until licensing is confirmed.

Product stack: `Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.
Monospace stack: `"IBM Plex Mono", "SFMono-Regular", Consolas, monospace`.

## Geometry

- 4 px base grid.
- Radius: 6 px controls, 10 px cards, 14 px large panels. No pill-everything UI.
- Borders carry structure; shadows are minimal.
- Primary app shell uses a 248 px navigation rail and a contextual right inspector where needed.
- Data tables use 44 px standard rows and 36 px compact rows.

## Product navigation

Primary customer navigation:
- Overview
- Workforce
- Assignments
- Approvals
- Activity
- Usage & Cost
- Billing
- Audit
- Integrations
- Settings

Owner/Admin adds:
- Tenants
- Licenses
- Economic Control
- Kill Switches
- Provider Health
- Reconciliation
- Incidents
- System Audit

## Signature interface language

The distinctive product pattern is the **Authority Strip**: every consequential task/action can expose four adjacent states in a consistent order:

`WORK AUTHORITY | ECONOMIC AUTHORITY | HUMAN APPROVAL | EXECUTION`

Each state uses text + icon + status; color alone is never sufficient. This is a functional identity element derived from the product architecture rather than a decorative AI motif.

The second signature pattern is the **Cost Rail**: reservation, actual cost, included customer usage, margin state and anomaly state are shown as separate values. Internal provider cost is never mislabeled as customer billing.

## Accessibility

- WCAG 2.2 AA minimum target.
- Keyboard-complete application flows.
- Visible focus states.
- No status conveyed only by color.
- Reduced-motion support.
- Minimum 44x44 px touch target on mobile surfaces.

## Brand-name release gate

No candidate becomes the production brand until all are complete:
1. broad web/company/product collision search;
2. exact + fuzzy + phonetic trademark search in relevant classes;
3. EUIPO/TMview/WIPO plus priority national registers;
4. domain and social-handle review;
5. professional similarity/pre-check for target jurisdictions;
6. legal decision on registrability and conflict risk.

The Austrian Patent Office explicitly recommends searches for identical and similar prior rights; registration itself does not establish that no conflicting earlier right exists. Therefore UI code must consume a central `brandName` token until clearance is complete.
