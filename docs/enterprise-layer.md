# Enterprise Layer — rolling Claude out team by team

The small-team setup in the main skill works for 3–10 people. This page is
for the larger rollout: a whole department, or a whole organization. Same
template, same session — with the admin and governance layer added.

## Plans and provisioning

- **Team plan** (2 to 150 seats): start here for a company with up to
  150 people. One Primary Owner, plus Owners and Admins. Owners handle
  billing, connectors, and sharing; Admins invite and remove people.
- **Enterprise plan** (from 20 seats): step up when you pass Team's
  150-seat cap, or when you need SCIM/SAML provisioning, data-loss
  controls, or content scanning on custom skills.
- **Provisioning:** an owner can provision a skill for all users, a member
  can share a skill with specific people, or a member can publish a skill
  to the organization's library. A custom skill is uploaded as a ZIP of
  its folder.
- **Identity:** configure SSO/SAML with your identity provider (Entra ID /
  Azure AD, Okta, Ping, Google Workspace). On Enterprise plans, an owner
  may need to switch folder access on before users see it.
- **Caution:** custom skills do not sync between claude.ai, the API, and
  Claude Code. A firm using more than one manages its skills in each
  place. One exception: in Cowork and cloud sessions, and in a terminal
  session signed in with a claude.ai account, Claude Code loads the skills
  enabled for that account automatically. When two skills share a name,
  Enterprise wins over Personal over Project over Plugin.

## Phased rollout

Roll out in phases. A phased approach reduces blast radius, builds internal
champions, and gives the security team time to validate controls at each
step.

- **Phase 0 — Foundation (weeks 1–2).** Create the org account. Configure
  SSO/SAML. Buy the pilot seats (start with 10). Set up billing alerts.
  Write the CLAUDE.md and custom-instruction templates.
- **Phase 1 — Pilot squad (weeks 3–5).** Pick one team. Deploy the custom
  skills, configure the MCP servers they need, collect feedback, and fix
  the skills the same day gaps appear.
- **Phase 2 — Department rollout (weeks 6–10).** Bulk-invite users. Run
  two 60-minute onboarding workshops per team (the session in
  `session-runbook.md`). Enable SCIM auto-provisioning. Add audit logging.
- **Phase 3 — Org-wide (weeks 11–16).** Roll out team by team with the
  same session. Keep the shared questions document going.
- **Phase 4 — Optimise (ongoing).** Monthly check: which jobs are actually
  faster, which skills are unused. Drop the dead ones, write skills for
  what replaced them. Evaluate the Enterprise tier if seats or control
  requirements grow past Team.

## Governance

- **Skills live in Git.** Every change to a skill goes through a pull
  request with a reviewer, like a code change. Audit which skills are
  active per team.
- **Hooks are guardrails, not the workflow.** Admin-enforced hooks in
  managed settings cannot be overridden by users. Use them for formatting,
  linting, and blocking secrets from leaving — never as a substitute for
  the model deciding how to do the work.
- **Permissions first.** Set boundaries before granting freedom: sandbox
  file access, approval for destructive operations, trust boundaries
  between the agent and external systems. The model decides; the harness
  enforces.
- **Audit logging and access governance** map to SOC 2 / ISO 27001
  expectations: who used what, when, and what changed. Keep the logs.
- **Content scanning:** Enterprise organizations can turn on scanning for
  custom skills uploaded in claude.ai. Audit any skill that
  comes from someone you do not know before relying on it.

## How this connects to the small-team template

Nothing in the main skill changes. The enterprise layer is additive: same
install steps, same session, same skills — plus provisioning, SSO, phased
rollout, and governance. A client on the Team plan and a client on the
Enterprise plan use the same template; the enterprise client just has more
of this page switched on.
