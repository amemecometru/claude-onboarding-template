---
name: claude-team-onboarding
description: Set up Claude and Claude Code for a small team of 3 to 10 people, and run the onboarding session so the team actually uses the tools day to day.
---

# Claude Team Onboarding

Set up Claude and Claude Code for a small team of 3 to 10 people,
so the team can actually use the tools day to day.

## Before the first visit

- Ask what the business does and what the team spends its day on, in plain
  words. Write down the three most repeated jobs.
- Ask what AI tools they already pay for, who uses them, and who does not.
  Never sell a second subscription for a job the first one already covers.
- Ask who is on the team, who is comfortable with new software, and who is
  not. The onboarding is built around the least comfortable person, not the
  most.
- Ask what they want Claude to do for them, and what they absolutely do not
  want it touching (client data, money, anything regulated). Write both
  lists down and keep them in front of you during the setup.
- Agree on a single point of contact on their side. That person answers
  questions when you are gone and owns the passwords.

## Install and sign in

- Install on each person's own machine, under their own account. Never
  share one login across the team.
- Claude Desktop: install the desktop app and sign in with each person's
  work email. The desktop app is what lets Claude work with folders on
  their computer. The website alone cannot do that.
- Working with folders (formerly Cowork): Cowork is folded into the main
  Claude app — there is no separate Cowork switch, and any conversation
  can run a multi-step task on your files. Point
  Claude at one dedicated work folder, never your whole Documents folder.
  Create `Claude-Workspace/` with `context/`, `projects/`, and `outputs/`
  inside.
- Claude Code: for anyone who writes code, install Claude Code and sign in
  the same way. It is the terminal version of the same agent.
- Working with folders needs a paid plan (Pro, Max, Team, or Enterprise).
  On Enterprise plans, an owner may need to switch it on first.
- Confirm each install by opening the tool and asking it one real question
  about their work. If it cannot answer, fix the install before moving on.
- On Team and Enterprise plans, Anthropic does not use workspace data to
  train models — that is the default, not a setting. Tell the team that in
  plain words. (On a personal Pro or Max account, the setting is 'Help
  Improve our AI models' under Settings > Privacy.)

## Workspace setup

- Set up one shared place Claude can read: a project folder, a shared drive
  folder, or the team's repo. Nothing else gets read access.
- Put the team's recurring documents in that place: templates, price lists,
  standard replies, job checklists. Claude is only as useful as what it can
  see.
- Keep client data, passwords, and financial records out of the shared
  place. If a document has a password or a bank detail in it, it does not
  go in.
- Write context files in the workspace folder: `about-me.md` (role,
  company, tools), `brand-voice.md` (tone, banned words, examples), and
  `working-preferences.md` (file rules, formats, guardrails). Add these to
  your project instructions so Claude reads them each session.
- Set Instructions for Claude (Settings > Your Claude) for the defaults
  that should hold across every session.
- Write down where the shared place is and who can change it. That note
  goes to the point of contact.

## Write the team's skills

- A skill is a short written guide for one repeated job, in SKILL.md
  format: a name, when to use it, and the steps in order.
- Write one skill per repeated job, starting with the three jobs from the
  first visit. No skill longer than one page.
- Each skill says: what the job is, when Claude should do it, the exact
  steps, and what a good result looks like. End with what to check before
  trusting the output.
- Example shape:

```
# Quote a repair job
Use when: a customer asks for a price on a job like the ones in the price list.
Steps:
1. Read the price list in the shared folder.
2. Ask the customer for the job size, the town, and the date.
3. Draft the quote using the price list only. Never invent a price.
4. Show the draft to the team member before it goes to the customer.
Check: the price matches the price list, and a human read it first.
```

- Save the skills where Claude can read them, and tell the team where they
  live. On Team and Enterprise plans, an owner can provision a skill for
  the whole organization, or a member can publish it to the organization's
  library. Otherwise, share the skill folder itself — a skill is just a
  folder with a SKILL.md file inside.
- Never write a skill that tells Claude to send, post, pay, or publish
  anything on its own. Sending is always a human decision.

## Run the onboarding session

- One session, 60 to 90 minutes, the whole team in the room or on the call.
  Full plan: `docs/session-runbook.md`.
- Leave behind a one page sheet: how to open each tool, where the skills
  live, who the point of contact is, and the rule that nothing gets sent
  without a human reading it first.

## Answer questions afterward

- Hold one 30 minute follow up a week later. Ask what worked, what did
  not, and what they tried that surprised them.
- Keep a shared questions document. Every question the team asks goes in it
  with the answer, so nobody asks the same thing twice.
- When a question shows a gap in a skill, fix the skill that day and tell
  the team what changed.
- When a question shows the tool cannot do something, say so plainly. Never
  promise a feature the tool does not have.
- After a month, check in once more: which of the three jobs is actually
  faster now, and which one is not. Drop the skill for the one that is not,
  and write a skill for whatever replaced it.

## Rules that never change

The full list is in the README: [Rules that never change](../../README.md#rules-that-never-change).
