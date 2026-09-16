# Product Component Contracts v1

These contracts convert the prototype into an implementation-ready design system. Components consume API data; they do not invent authority, billing or execution state.

## AppShell
Inputs: tenant identity, user role, navigation capabilities, environment. Customer and owner navigation are separate capability sets. Hidden navigation is not authorization.

## AuthorityStrip
Inputs: work_authority, economic_authority, human_approval, execution_state. Each segment requires machine state plus human-readable label. `authorized` is prohibited as a single combined state.

## CostRail
Inputs: reservation maximum, actual provider cost, customer usage units/value, gross contribution, reconciliation state. Currency and unit type are explicit. Unknown actual cost renders unknown/held, never zero.

## AgentCard / AgentDetail
Inputs: licensed seat state, profession, assignment state, authority epochs, current budget scope, last evidence timestamp. Activation/deactivation calls provisioning APIs; invocation UI cannot allocate seats.

## AssignmentCard / AssignmentDetail
Inputs: run/task IDs, agent, work request, limits, current authority, approval requirements, paid-invocation ceiling, lifecycle state. Retry is disabled for unknown paid outcomes until reconciliation clears the invocation.

## ApprovalPanel
Inputs: exact proposed side effect, canonical request summary/hash reference, agent, authority expiry, maximum charge, evidence links. Approve is one-shot and scope-specific. Editing a request invalidates the approval and requires a new authorization.

## BillingMeter
Inputs: plan, included usage, consumed usage, overage units, hard stop, billing period. Internal provider cost is shown only to roles with economics permission.

## KillSwitchControl
Inputs: scope, active state, reason code, actor permissions, effective timestamp. Activation requires explicit confirmation. Clearing requires separate permission and records immutable operational evidence.

## OperationalEventList
Inputs are privacy-minimized event records only. Prompts, customer payloads and model outputs are not accepted by the component contract.

## Error states
Every data component implements loading, empty, stale, denied, unavailable and error states. Authority/economic state that cannot be refreshed is fail-closed and must be visually distinguishable from an ordinary application error.

## Accessibility
All production implementations conform to `accessibility-standard-v1.md`. Prototypes are visual specifications and are not themselves evidence of accessibility conformance.