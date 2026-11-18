# 01 — Microsoft 365 Copilot Enterprise Rollout Runbook

**Purpose:** provide a gated, adaptable lifecycle for planning and operating a Microsoft 365 Copilot rollout. This is a planning template, not a prescribed Microsoft deployment sequence. The client owns tenant decisions and approvals.

## Engagement record

- Client / tenant: [Fill in]
- Business sponsor: [Fill in]
- Engagement lead: [Fill in]
- Tenant / licensing administrator: [Fill in]
- Security / privacy owner: [Fill in]
- Data / information owner(s): [Fill in]
- Change and enablement lead: [Fill in]
- Service desk / operations owner: [Fill in]
- Planned review dates: [Fill in]
- Document version / approver: [Fill in]

## Working principles

1. **Readiness before reach.** Review identity, licensing, data access, security, support, and use-case suitability before increasing access.
2. **Least privilege and existing permissions matter.** Copilot experiences operate within the Microsoft 365 service and permissions context. The client must review whether existing content access is appropriate; do not imply that a license alone fixes oversharing.
3. **Use a bounded pilot.** Pick a cohort, approved scenarios, support route, and evaluation method before enabling the pilot.
4. **Agree evidence and thresholds in advance.** Usage is not the same as value, and neither proves accuracy or safe use.
5. **Keep a human accountable.** People remain responsible for reviewing outputs and taking consequential actions under client policy.
6. **Verify current behavior.** Confirm product availability, licensing, admin steps, and reports in current Microsoft documentation and the client tenant.

## Phase 0 — Intake and outcomes

**Purpose:** establish why the client is considering Copilot and what must remain out of scope.

### Activities

- Identify the sponsor, affected business groups, tenant/admin owners, data owners, security/privacy stakeholders, change lead, and support owner.
- Capture current tools, workflows, pain points, and existing AI policies. Avoid duplicating a capability the organization already has without a reason.
- Select a small number of candidate work scenarios. For each, record the user, task, expected benefit, source information, risk level, human check, and excluded data/actions.
- Establish a baseline plan: what is measured, by whom, at what granularity, and what is not collected.
- Identify constraints: licensing/budget, geography, accessibility, records retention, works council or labor requirements, regulatory obligations, and change windows as applicable.

### Gate 0 — sponsor and scope approval

**Proceed only when:** sponsor and accountable owners are named; intended outcomes and out-of-scope uses are written; candidate scenarios have business and data owners; privacy/data collection boundaries are agreed.

**Record:** approved scope, unresolved questions, risks, and decision-maker sign-off in the decision log in `02-readiness-and-governance.md`.

## Phase 1 — Tenant and organizational readiness

**Purpose:** validate prerequisites and control posture before assigning pilot access.

### Activities

- Confirm product and license eligibility, user prerequisites, supported apps/clients, network/device requirements, and current admin steps using Microsoft documentation and the tenant.
- Review identity, authentication, user lifecycle, group membership, license assignment, and access review procedures with the client’s identity and tenant administrators.
- Review SharePoint, OneDrive, Teams, and other in-scope content access and sharing with content owners and security. Prioritize overshared or sensitive content remediation according to client policy.
- Review applicable information protection, retention, audit, DLP, eDiscovery, and conditional access settings with authorized security/compliance owners. Availability and configuration vary; do not assume a control is licensed, enabled, or suitable.
- Confirm acceptable-use guidance, incident/reporting route, support coverage, user communications, and accessibility accommodations.
- Define the pilot cohort and comparison/baseline method; document selection criteria and any limitations.

### Gate 1 — readiness approval

**Proceed only when:** authorized tenant/security/data owners approve the scoped readiness findings; blocking risks have an owner and disposition; license and support arrangements are confirmed; pilot scenarios, cohort, measurement, and stop conditions are approved.

**No-go examples:** unclear data access ownership; unresolved high-impact oversharing; no approved use policy; no incident/support route; no agreement on participant privacy or measurement; required tenant controls not verified.

## Phase 2 — Configure and prepare the pilot

**Purpose:** prepare a limited, supportable experience and test the end-to-end onboarding.

### Activities

- Client tenant administrator configures the approved tenant settings and assigns licenses/access according to client change controls. Record who made the change, approval, date, and rollback/disable process.
- Validate configuration with authorized test accounts and approved content. Never use a real person’s account without authorization.
- Run a scenario test log before launch: expected task, approved data source, prompt/task instructions, observed output, human review result, issue, owner, and disposition. Test representative success and failure cases.
- Prepare end-user materials, office hours or help route, champion/support contacts, communications, and accessibility support.
- Train pilot participants on capabilities, limitations, data handling, output verification, reporting, and the difference between a draft and an approved business action.
- Capture baseline data before exposure where feasible and approved. Document missing baseline data rather than reconstructing it from memory.

### Gate 2 — pilot launch approval

**Proceed only when:** test findings are reviewed; critical issues are resolved or explicitly excluded; users and support staff have received appropriate orientation; success thresholds and stop conditions are written; the client’s designated approver authorizes pilot launch.

## Phase 3 — Bounded pilot and evaluation

**Purpose:** learn whether the selected use cases are usable, acceptable, and worth further investment in this tenant and cohort.

### Activities

- Run for the agreed duration and with the agreed cohort and scenarios. Track access, support requests, participation, and test/feedback evidence consistent with privacy policy.
- Hold regular feedback sessions; provide a clear route to report inaccurate, unsafe, inaccessible, or unexpected behavior.
- Review adoption/usage data only if the client has approved access and the metric’s definition and limitations are understood. Do not use usage counts as a proxy for productivity or business value.
- Compare results to the baseline and pre-agreed thresholds. Separate observed facts, participant perceptions, and inferred impact.
- Review incidents, data handling, user experience, access changes, support burden, and scenario suitability with the appropriate owners.

### Gate 3 — 30-day review

Review initial adoption, onboarding completion, support themes, scenario test outcomes, early risks, and data quality. Decide: continue unchanged, remediate and continue, narrow scope, pause, or stop. Do not scale based only on enthusiasm or logins.

### Gate 4 — 60-day review

Review repeat use, workflow/task outcomes versus baseline, participant feedback, support trends, control exceptions, and unresolved issues. Confirm that the pilot still meets its thresholds and that the measurement is credible. Decide whether to prepare a controlled expansion or continue/revise the pilot.

### Gate 5 — 90-day review

Review the complete agreed evaluation window. The sponsor and accountable owners decide: scale, extend with revised hypotheses, hold, or stop. Record evidence, limitations, cost/operating considerations if available, control status, and approval. A scale decision does not mean every business group or use case is approved.

## Phase 4 — Controlled expansion

**Purpose:** extend only to approved groups and scenarios with capacity to support them.

- Stage expansion by business unit, role, or use case; set a cohort size and release window for each wave.
- Recheck permissions, content readiness, licenses, support capacity, training, and current product behavior before each wave.
- Communicate what is changing, who is included, where to get help, and how to opt out or report a concern under client policy.
- Compare each wave with the original pilot while noting changes in cohort, task mix, and environment.
- Require a named owner and gate approval for each expansion.

## Phase 5 — Ongoing service and review

- Assign owners for tenant administration, license/access lifecycle, security and compliance controls, content/data governance, user support, enablement, measurement, and vendor-change review.
- Review usage and outcome measures at the agreed cadence; remove unused access and update training or controls as approved.
- Re-test priority scenarios after material changes in product behavior, configuration, policy, source content, or workflow.
- Maintain release/change records, known issues, support articles, incident handling, and decisions.
- Review whether the service remains useful and within the approved risk posture; retire or pause scenarios that no longer meet the criteria.

## Required records checklist

- [ ] Scope and use-case inventory
- [ ] Stakeholder / role assignment
- [ ] Readiness and risk decisions
- [ ] Licensing and tenant verification record
- [ ] Pilot cohort and communications plan
- [ ] Baseline and measurement plan
- [ ] Scenario test log
- [ ] Training and support materials
- [ ] 30/60/90-day review records
- [ ] Expansion approvals and change records
- [ ] Operations owner and review cadence

## Evidence and attribution note

This runbook describes a proposed process. It is not evidence that any phase has been completed. In a portfolio or application, distinguish the design of the process from work performed in a client environment and from measured outcomes.
