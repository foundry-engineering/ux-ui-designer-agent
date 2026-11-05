# Product Accessibility & Interaction Standard v1

Status: normative for customer and owner surfaces.

Target: WCAG 2.2 AA minimum. High-risk operational controls should additionally meet the stronger focus appearance and 44x44 target guidance where practical.

## Keyboard and focus
- Every interactive control is keyboard operable in meaningful DOM order.
- Focus is always visible and must not be hidden by sticky navigation, dialogs or overlays.
- Destructive and economic-authority actions never trigger on focus or selection alone.
- Dialog focus is trapped only while the dialog is modal and returns to the invoking control on close.

## Targets and input
- Product controls target at least 44x44 CSS px; never below WCAG 2.2 AA minimum without a documented exception.
- Drag-only interactions are prohibited. Every reordering or assignment action has a click/keyboard alternative.
- Pointer, keyboard and assistive technology paths expose equivalent authority and cost information.

## Authentication
- Authentication must support password managers and copy/paste where passwords are used.
- No cognitive puzzle is the sole authentication path.
- Passkeys are preferred when the identity boundary supports them.

## Semantics
- One page-level h1. Sections use hierarchical headings.
- Status is never conveyed by color alone: text or icon labels are mandatory.
- Tables use actual table semantics in implementation, not visual div grids.
- Live operational changes use appropriately scoped aria-live regions; routine telemetry must not spam screen readers.

## Economic and authority UX
- Paid actions show maximum authorized charge before irreversible dispatch when human approval is required.
- Reserved, actual, customer usage and margin are distinct labels; they must never be collapsed into one ambiguous `cost` number.
- Work Authority and Economic Authority are independently represented.
- Emergency stop is visually distinct, requires confirmation and states exact scope/effect.
- Unknown provider outcomes are displayed as `Reconciliation required`, never as `Failed` or `Refunded` until evidence exists.

## Motion and visual system
- Motion respects prefers-reduced-motion.
- No flashing operational indicators.
- Critical status uses label + shape/icon + color.
- Text and non-text controls must meet applicable WCAG contrast requirements.

## Responsive behavior
- Customer workflows support 320 CSS px width without horizontal page scrolling, except intrinsically two-dimensional data where an accessible alternate representation is provided.
- Desktop density must not be achieved by shrinking controls below interaction requirements.

## Verification
Accessibility is a release gate: keyboard walkthrough, automated accessibility scan, zoom/reflow check, screen-reader smoke test for onboarding, approval, economic hard-stop and emergency-stop flows, plus manual contrast/focus review.