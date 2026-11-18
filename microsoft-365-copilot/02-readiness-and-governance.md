# 02 — Readiness and Governance Workbook

**Use:** complete this with the client’s authorized owners before a pilot or rollout. This workbook is a prompt for assessment, not an audit, certification, or guarantee of compliance.

## A. Readiness checklist

For each item, record **Status** (Not assessed / In progress / Ready / Blocked / Not applicable), evidence or link, owner, and review date.

| Area | Readiness question | Status / evidence / owner |
|---|---|---|
| Business outcome | Is there a specific workflow and user group with a documented need and accountable business owner? | [Fill in] |
| Scope | Are approved scenarios, excluded tasks/data, and intended participants documented? | [Fill in] |
| Licensing | Has the tenant administrator verified current eligibility, licenses, and user prerequisites for the intended experience? | [Fill in] |
| Apps and devices | Are supported apps, clients, devices, and network requirements verified for the cohort? | [Fill in] |
| Identity | Are identity, authentication, group membership, user lifecycle, and access review owners identified? | [Fill in] |
| Content access | Have content owners reviewed relevant SharePoint, OneDrive, Teams, and other in-scope permissions/sharing? | [Fill in] |
| Sensitive data | Have data classification, information protection, DLP, retention, and records requirements been reviewed by authorized owners where applicable? | [Fill in] |
| Privacy | Are telemetry, surveys, interviews, retention, access, and reporting boundaries approved? | [Fill in] |
| Security | Has the security owner reviewed the proposed configuration and threat/risk considerations? | [Fill in] |
| Policy | Is acceptable use clear, current, discoverable, and consistent with client policy? | [Fill in] |
| Human review | Are required human checks and approvals defined for outputs and downstream actions? | [Fill in] |
| Accessibility | Are user accommodations and accessible training/support routes identified? | [Fill in] |
| Change | Are sponsor, communications, timing, training, champion, and feedback plans ready? | [Fill in] |
| Support | Is there a help route, escalation owner, and incident/reporting procedure? | [Fill in] |
| Measurement | Are baseline, measures, thresholds, collection owners, and review gates agreed before launch? | [Fill in] |
| Operations | Is there an owner for licenses, access, configuration changes, product updates, documentation, and periodic review? | [Fill in] |

## B. Control and responsibility matrix

Assign actual people/teams and approval paths; titles below are role prompts, not mandatory Microsoft role names. A technology feature is not the same as an operational control. Confirm actual admin role permissions and separation of duties with the tenant owner.

| Control / work area | Accountable client owner | Responsible operator | Evidence / cadence | Notes / dependency |
|---|---|---|---|---|
| Business goals and use-case approval | [Business sponsor] | [Business owner] | Approved scope; review at gates | The client sets acceptable use and business risk. |
| Tenant configuration and licenses | [M365 service owner] | [Authorized tenant admin] | Change record; each release | Verify current licensing and available settings in tenant. |
| Identity, groups, lifecycle, access review | [Identity owner] | [Identity/admin team] | Provisioning and access-review records | Do not assume a Copilot license defines data permissions. |
| SharePoint/OneDrive/Teams content access | [Information owner] | [Site/content owners] | Permission review and remediation record | Copilot may surface content users already have access to; review inappropriate access. |
| Security, privacy, compliance | [Security/privacy/compliance owner] | [Assigned control operators] | Approved assessment and control evidence | Applicability and features depend on tenant, licensing, configuration, and policy. |
| Acceptable-use and human review policy | [Policy owner] | [Business and risk stakeholders] | Published policy; acknowledgement if required | Set rules for sensitive, regulated, and consequential work. |
| Pilot measurement and reporting | [Sponsor] | [Evaluation lead] | Approved plan and 30/60/90 reviews | Limit access to identifiable feedback and telemetry. |
| User enablement / champions | [Change lead] | [Trainer/champions] | Attendance, materials, feedback themes | Avoid reporting named employee usage unless specifically approved. |
| Support / incidents | [Service owner] | [Help desk/security escalation] | Ticket and incident process | Define route for inaccurate output, data exposure, or access issue. |
| Release/change management | [Service owner] | [Change manager/admin] | Release notes, test, approval, rollback | Product changes may alter user experience. |
| Records and retention | [Records owner] | [Compliance/admin team] | Retention and disposition evidence | Confirm requirements and capabilities for the tenant. |

## C. Use-case risk record

Create one record per scenario.

- Scenario name: [Fill in]
- Business owner and users: [Fill in]
- Task and expected benefit: [Fill in]
- Approved information sources: [Fill in]
- Data classification / sensitivity: [Fill in]
- Excluded data or actions: [Fill in]
- Human reviewer and required expertise: [Fill in]
- Consequence if the output is wrong: [Fill in]
- How output will be checked against authoritative sources: [Fill in]
- Whether output may enter a business record or external communication: [Fill in]
- Required approvals before downstream action: [Fill in]
- Evaluation measure and baseline: [Fill in]
- Owner / review date / go-no-go decision: [Fill in]

## D. Decision log

| Date | Decision / issue | Options considered | Evidence reviewed | Decision owner | Outcome and conditions | Follow-up owner / due date |
|---|---|---|---|---|---|---|
| [Fill in] | [Fill in] | [Fill in] | [Fill in] | [Fill in] | [Fill in] | [Fill in] |

## E. No-go and pause conditions

Agree client-specific conditions. Consider pausing access or a scenario when there is an unapproved data exposure, unresolved security/privacy issue, material output error in a consequential workflow, missing human-review control, unapproved use, failed tenant prerequisite, or insufficient support. Record who can pause, who investigates, who approves resumption, and how affected users are notified.

## F. Scope caveat

Microsoft 365 Copilot uses the Microsoft 365 environment and is subject to tenant configuration, permissions, service behavior, licensing, and applicable client policies. This template does not assert that any specific control is enabled, that a tenant is compliant, or that a vendor control satisfies a client obligation. The client’s authorized security, privacy, legal, records, and technology owners make those determinations.
