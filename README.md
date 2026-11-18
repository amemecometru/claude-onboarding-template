# Claude Onboarding Template

Start using Claude in one session — the app and Claude Code — so people
actually use it every day.

## Who this is for

- **A small team (3–10 people)** that wants Claude set up properly, with
  the tools pointed at their real work.
- **A larger organization** rolling Claude out team by team — see
  `docs/enterprise-layer.md` for provisioning, access, and the phased
  rollout.
- **Anyone onboarding new people to Claude** — a new hire, a new team, a
  new client.

## How to use it — three steps

**1. Before the first visit — ask questions.**
Read `docs/session-runbook.md` (the "Before the first visit" section).
Find out what the team does all day, what they already pay for, who is
comfortable with new software and who is not, and what the AI must never
touch. Write down their three most repeated jobs. The whole setup is built
around the least comfortable person, not the most.

**2. Set up Claude on each person's machine.**
Install Claude Desktop (and Claude Code, for anyone who writes code) under
each person's own work email — never one shared login. Put the team's
recurring documents in the shared folder — the team's shared drive folder,
project folder, or repo — one place Claude can read. The point of contact
controls who can change it. Write one short skill per repeated job (see
below). Full steps: `skills/claude-team-onboarding/SKILL.md`.

**3. Run the session.**
One session, 60 to 90 minutes, the whole team in the room or on the call.
Full plan: `docs/session-runbook.md`. Leave behind the one-page sheet
in `docs/leave-behind.md`.

## What's inside

```
claude-onboarding-template/
  README.md                                # this file
  skills/
    claude-team-onboarding/SKILL.md        # the onboarding skill (Claude and Claude Code)
    template/SKILL.md                      # blank skill — copy it for each repeated job
  docs/
    session-runbook.md                     # the 60–90 minute session, step by step
    leave-behind.md                        # one-page sheet to leave with the team
    enterprise-layer.md                    # Team/Enterprise provisioning, access, phased rollout
    how-it-works.md                        # how Claude skills actually load, in plain language
```

Under skills/ there are two folders, each holding one file called SKILL.md: claude-team-onboarding is the finished onboarding skill, and template is the blank to copy for each new skill.

## How a skill works (the short version)

A skill is a folder with a `SKILL.md` file: a name, a short description of
when to use it, and the steps in order. Claude keeps only the names and
descriptions loaded. When a task matches a skill, it reads the full
instructions — the body loads on demand, not upfront. That is why skills
stay short: one repeated job per skill, no longer than a page.

Write skills for the team's real repeated jobs, starting with the three from
the first visit. Each one says what the job is, when Claude should do it,
the exact steps, and what a good result looks like. End with what to check
before trusting the output. Never write a skill that tells Claude to send,
post, pay, or publish anything on its own — sending is always a human
decision.

## Rules that never change

- Never put a password, API key, or secret in chat, in a file, or in a
  prompt. Secrets live in the tool's own settings or a password manager.
- Never let Claude send an email, post a message, pay a bill, or change a
  record without a human reading it first.
- Never present Claude's output as verified fact. Check it against the
  price list, the document, or the person who knows, then send it.
- Speak plainly. If the team cannot repeat back what the tool does in one
  sentence, the setup is not done.
- The goal is a team that completes one real job alone within a week. If
  they still need you for the same task after a month, the skill or the
  setup is wrong, not the team.

## Sources

Built from Anthropic's own skill format and reference implementations
([anthropics/skills](https://github.com/anthropics/skills), Apache 2.0),
the Agent Skills open standard ([agentskills.io](https://agentskills.io)),
and the harness mechanics taught in
[shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)
(MIT) — including how skill loading, permissions, and hooks actually work.
The onboarding method comes from hands-on work with Claude, Copilot, and
Gemini — building skills and watching what a new user trips over.
