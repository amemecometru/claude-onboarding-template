# How It Works — skills, in plain language

You do not need to know this to use the template. It is here so the person
doing the onboarding can answer "how does this actually work?" honestly —
and so a technical reader can see the template is built on the real
mechanics, not on guesswork.

## The model and the harness

An agent product is two things: the model and the harness. The model is the
driver — it perceives, reasons, and decides. The harness is the vehicle —
the code that gives the model an operational environment: tools, knowledge,
observation, action interfaces, and permissions. The model decides; the
harness executes. The harness does not make the model smart. It gives the
model hands, eyes, and a workspace.

That is the job this template serves: building the harness around a team —
the setup, the skills, the permissions, the shared knowledge — and then
getting out of the way.

## How a skill loads

A skill is a folder with a `SKILL.md` file. The file starts with two
fields: a `name` and a `description` of what the skill does and when to use
it. The rest is plain-language instructions.

Claude does not read every skill upfront. It works in two steps:

1. **At startup, it reads the catalog.** Just the names and descriptions
   of every skill — about 100 tokens per skill. That catalog goes in the
   system prompt, so Claude always knows what skills exist.
2. **On demand, it reads the full skill.** When a task matches a skill's
   description, Claude loads the whole `SKILL.md` — the steps, the
   examples, the checks. The body loads only when it is needed.

That is why skills stay short. A long skill that nobody triggers costs
nothing, but a short skill that triggers at the right moment is the whole
point. One repeated job per skill, no longer than a page.

This is the same mechanism in Anthropic's own skill format and in the
reference implementation at
[shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)
(lesson s07, Skill Loading), where a `SkillLoader` scans `skills/*/SKILL.md`,
builds the catalog, and loads full content by name when the model asks for
it.

## Permissions and hooks

- **Permissions come first.** Before Claude gets freedom, decide what can
  run, what must stop, and what needs a human's approval. Sandbox file
  access. Approval for destructive operations. Trust boundaries between the
  agent and external systems.
- **Hooks are extension points, not rewrites.** A hook runs around a tool
  call — before it, or after it — without changing the main loop. Use them
  for formatting, linting, and catching secrets. Never use them to
  substitute hand-written decision trees for the model's own judgment.
- **The loop is simple.** The model reads the messages, decides whether to
  call a tool or answer, the harness runs what it asked for and returns the
  result, and the loop continues until the model stops. Everything else —
  skills, memory, subagents, teams — is a mechanism built around that loop.

## Memory and context

Claude's context fills up over a long session. Two mechanisms handle that:
context compaction (shortening older messages, tool results first) and
memory (keeping what matters across sessions, forgetting what does not).
For a team, the durable memory is the skills themselves and the shared
questions document — written down, versioned, and reviewed like any other
work product.

## Sources

- Agent Skills open standard: https://agentskills.io
- Anthropic's skill reference implementations:
  https://github.com/anthropics/skills
- Harness mechanics, lesson by lesson:
  https://github.com/shareAI-lab/learn-claude-code
