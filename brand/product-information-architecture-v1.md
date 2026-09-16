# Product Information Architecture v1

## Customer application

### Overview
Operational command page: licensed agents, active assignments, approvals waiting, spend vs hard limits, incidents and recent outcomes. No vanity metrics.

### Workforce
Profession groups -> licensed agents -> agent detail. Agent detail shows role, capabilities, connected tools, authority policy, active license, cost policy, task history and current status.

### Assignments
Create work from a bounded assignment template. Show objective, evidence/context, agent, authority, budget, deadlines, child-task/fan-out ceilings and expected review point before launch.

### Approvals
A decision queue, not a notification feed. Every approval shows exact proposed external action, canonical request summary, authority evidence, maximum spend, expiry and consequences of approve/deny.

### Activity
Run/task timeline with deterministic states. Provider uncertainty is explicit and cannot look like success or failure until reconciled.

### Usage & Cost
Separate customer usage, included allowance, overage, internal reservation/actual provider cost (only where role permits), and margin. Show hard-stop distance and anomalies.

### Billing
Plan, license period, included units, overage, invoices/receipts when payment provider exists. Never imply an invoice/payment exists before provider confirmation.

### Audit
Searchable immutable evidence view for authority, approval, execution and economic events. Payloads are redacted according to role/privacy policy.

### Integrations
Provider/model/tool connections, health, scopes and last verification. Secret material is never returned to browser.

### Settings
Organization, members/roles, security, notification policy, billing contacts and data controls.

## Owner/Admin application

Owner/Admin is a separate privileged surface and does not inherit customer permissions.

### Tenants
Provisioning status, license state, active agents, economic status and incidents.

### Licenses
Entitlements, periods, seat/agent activation, usage hard stops and lifecycle changes.

### Economic Control
Platform -> tenant -> license -> agent -> run -> task budget accounts. Show reserved, settled, uncertain and remaining authority.

### Kill Switches
Platform, tenant, license and agent emergency stops with reason, actor, timestamp and required step-up/dual approval policy when configured.

### Provider Health
Price-registry freshness, provider health, reconciliation backlog and disabled routes.

### Incidents
Operational/security/economic incidents with state, severity, evidence and operator ledger.

## Responsive model

Desktop is the primary creation/operations surface. Mobile supports monitoring, approval/deny, alerts and safe-stop actions; complex policy authoring remains desktop-first.

## First-run onboarding

1. Create/accept organization.
2. Confirm license.
3. Select included profession/agent.
4. Connect only required integration.
5. Review authority and budget policy.
6. Activate agent seat.
7. Create first bounded assignment.
8. Review exact execution boundary.
9. Launch.
10. Observe outcome + usage receipt.
