<div align="center">

<h1>ASCII wireframes</h1>

**Sketch three genuinely different layout hypotheses as ASCII wireframes before opening Figma or writing a line of HTML - built for design teams who want to compare directions, not commit to one too early.**

[![CI](https://img.shields.io/github/actions/workflow/status/humbleteam/ascii-wireframes/validate.yml?branch=main&style=for-the-badge&logo=github&label=CI)](https://github.com/humbleteam/ascii-wireframes/actions/workflows/validate.yml)
[![GitHub stars](https://img.shields.io/github/stars/humbleteam/ascii-wireframes?style=for-the-badge&logo=github&color=181717)](https://github.com/humbleteam/ascii-wireframes/stargazers)
[![Last commit](https://img.shields.io/github/last-commit/humbleteam/ascii-wireframes?style=for-the-badge&color=339933)](https://github.com/humbleteam/ascii-wireframes/commits/main)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude_Code-skill-D97757?style=for-the-badge&logo=anthropic&logoColor=white)](https://github.com/humbleteam/ascii-wireframes/blob/main/SKILL.md)

</div>

Explore three layout directions for a screen in plain text, compare them side by side, and pick one before any hi-fi work starts. The skill takes a screen name and its primary job as input, and returns three monospace ASCII wireframes, each answering a different version of "what does this screen lead with" - not three palette variations of the same layout. A fixed legend keeps buttons, inputs, and active states readable the same way across all three.

## Table of contents

- [What it does](#what-it-does)
- [Quick start](#quick-start)
- [Usage](#usage)
- [Example output](#example-output)
- [How it works](#how-it-works)
- [How is this different from just asking the model?](#how-is-this-different-from-just-asking-the-model)
- [FAQ](#faq)
- [Related skills](#related-skills)
- [Who maintains this](#who-maintains-this)

## What it does

- Generates three distinct layout hypotheses for one screen, each a different answer to what value proposition the screen leads with.
- Renders each hypothesis as a monospace ASCII wireframe, 60-80 characters wide and 8-20 lines tall, in a fenced code block that displays correctly in any chat or terminal.
- Uses one fixed legend per response - buttons, inputs, checkboxes, icons, and active tabs always use the same symbols, so the variants are easy to compare.
- Asks exactly one clarifying question when the screen or its primary job is unclear, instead of guessing.
- Caps output at five variants and states why: more options slow a decision down instead of speeding it up.
- Skips citations and rationale in this phase on purpose - a wireframe is only useful while it stays cheap to throw away.

## Quick start

Install for yourself, across every project:

```bash
git clone https://github.com/humbleteam/ascii-wireframes ~/.claude/skills/ascii-wireframes
```

Install for one project only, checked into that repo:

```bash
git clone https://github.com/humbleteam/ascii-wireframes .claude/skills/ascii-wireframes
```

Use with another agent: this skill is plain markdown, in the Agent Skills format. Paste the contents of [`SKILL.md`](SKILL.md) into the system prompt of Cursor, Codex, or any other LLM agent that accepts custom instructions.

Restart Claude Code after installing, then ask it what skills it has available, or check `~/.claude/skills/` (personal) or `.claude/skills/` (project) directly - `ascii-wireframes` should be listed either way.

## Usage

- "Give me 3 layout directions for a pricing page for a B2B analytics tool." Returns three ASCII wireframes, each leading with a different pricing strategy: a single recommended plan, a feature-comparison table, and an ROI calculator.
- "Sketch some options for a mobile onboarding flow before we open Figma." Defaults to mobile proportions and returns three onboarding structures: a guided tour, a self-seeding empty state, and a single setup question.
- "I need 3 different hero section approaches for our marketing homepage." Asks one clarifying question first if the homepage's primary conversion goal is not stated, then renders three hero directions once it has an answer.

## Example output

Prompt: "Give me 3 layout directions for a task dashboard home screen."

**V1 - Today's tasks first**

```
+------------------------------------------------------------+
| (menu)  TaskFlow                    (search) (bell) (AB)   |
+------------------------------------------------------------+
| Today - Tue Jul 14                          [[ + Task ]]   |
| ------------------------------------------------------------ |
| [ ] Ship pricing page copy      9:00am   Design    High    |
| [ ] Review PR #482              11:30am  Eng       Med     |
| [x] Sync with client onboarding 1:00pm   PM        Low     |
| [ ] Draft Q3 roadmap            3:00pm   PM        Med     |
|                                                              |
| Up next: 4 tasks tomorrow, 2 overdue                        |
+------------------------------------------------------------+
```

Leads with what's due today, so the first thing a user sees is what to act on right now.

**V2 - Project board overview**

```
+------------------------------------------------------------+
| (menu)  TaskFlow                                  (AB)     |
+------------------------------------------------------------+
| BACKLOG (6)   | IN PROGRESS (3) | REVIEW (2)   | DONE (8)  |
| -------------- | ---------------- | -------------- | --------- |
| [ Card ]       | [ Card ]         | [ Card ]       | [ Card ] |
| [ Card ]       | [ Card ]         | [ Card ]       | [ Card ] |
| [ Card ]       | [ Card ]         |                | ...      |
| [ Card ]       |                  |                |          |
| [ Card ]       |                  |                |          |
| [ Card ]       |                  |                |          |
+------------------------------------------------------------+
```

Leads with the shape of all work in flight, so a user orients on the whole project before picking a task.

**V3 - Single task, focused**

```
+------------------------------------------------------------+
| (back)  Ship pricing page copy                    (AB)     |
+------------------------------------------------------------+
| Status: In progress    Assignee: You     Due: Today         |
| ------------------------------------------------------------ |
| Description                                                 |
| Rewrite hero and pricing table copy for the new plan tiers. |
|                                                              |
| Subtasks (2/4)                                              |
| [x] Draft hero copy                                         |
| [x] Draft pricing table copy                                |
| [ ] Get design review                                       |
| [ ] Ship to staging                                         |
|                                                              |
| Activity: 3 comments                    [[ Mark done ]]     |
+------------------------------------------------------------+
```

Leads with one task and its context, so a user lands already inside the thing they came to finish.

Which variant(s) should move forward?

## How it works

- Every hypothesis has to be a different product decision, not a different visual treatment. Changing only color, spacing, or font between two variants makes them the same hypothesis twice.
- A fixed ASCII legend - borders, buttons, inputs, checkboxes, icons, active-tab markers - stays identical across every variant in one response, so the eye compares structure instead of relearning symbols each time.
- The 60-80 character width and 8-20 line height are a guardrail, not a suggestion. That range fits inside a chat pane or terminal without wrapping, and it forces the sketch to leave out detail that belongs in a hi-fi mockup.
- Mobile proportions (narrower, taller box, mirroring a 390x844 screen) are the default when no platform is stated.
- The skill asks one clarifying question, never more, when a request under-specifies the screen or its primary job, instead of guessing.
- Rationale, citations, and "why" explanations are absent from this phase on purpose. A low-fidelity sketch earns its value by being cheap to throw away; a citation makes a reviewer defend a choice instead of reacting to it.
- Once a variant is picked, the skill hands off to a pixel-faithful HTML build rather than doing both jobs in one pass - see [html-mockup](https://github.com/humbleteam/html-mockup) for that step.

## How is this different from just asking the model?

A bare prompt for "3 wireframe options" tends to return three versions of the same layout with different colors or spacing, not three different product decisions. It also sneaks in hi-fi opinions - font choices, exact colors - before a direction is picked, and it produces wireframes of inconsistent width and symbol use that are hard to scan side by side. This skill forces three distinct value propositions, pins one legend and one size range for the whole response, and refuses citations or rationale at this stage on purpose, because a low-fidelity sketch only earns its keep if it costs nothing to reject.

## FAQ

**Why wireframe in ASCII?**
Plain text renders identically in any chat window, terminal, or markdown viewer, with no image tooling required. It is also fast to produce and easy to diff against a follow-up revision.

**How many design variants should I explore?**
Three is the default - enough to force genuinely different value propositions without spreading a reviewer's attention too thin. The skill caps at five if asked for more, and explains why: past five, comparison turns into skimming.

**Can Claude generate wireframes?**
Yes. This skill has Claude produce monospace ASCII wireframes directly in a chat reply, using a fixed legend for buttons, inputs, and active states so output stays consistent across variants.

**What is low-fidelity wireframing for AI agents?**
A deliberately cheap, text-only sketching step that happens before any hi-fi mockup or code, so a team aligns on structure and value proposition first.

**How wide should an ASCII wireframe be?**
This skill targets 60-80 characters wide and 8-20 lines tall - a range that fits a typical chat pane or terminal without line wrapping, and stays narrow enough to force the sketch to stay high-level.

**What happens after I pick a variant?**
The skill confirms your selection in one line, then points to the [html-mockup](https://github.com/humbleteam/html-mockup) skill for turning the chosen wireframe into a pixel-faithful HTML mockup against a reference screenshot. It does not generate HTML itself.

**Does this skill write any HTML or code?**
No. It is scoped to the ASCII sketching phase only. If asked for HTML mid-sketch, it names html-mockup as the next step instead of producing code.

## Related skills

Part of a 10-skill open-source kit for design teams by Humbleteam.

- [design-review](https://github.com/humbleteam/design-review) - structured UX critique with a 0-4 score, before/after/why fixes, and a citation for every claim.
- [html-mockup](https://github.com/humbleteam/html-mockup) - census-first HTML mockups that match a reference screenshot: exact palette, item counts, component states.
- [extract-design-tokens](https://github.com/humbleteam/extract-design-tokens) - pull palette, type, spacing, radii, and shadows from a URL or screenshot into CSS variables and JSON.
- [audit-design-tokens](https://github.com/humbleteam/audit-design-tokens) - find token drift in a codebase: raw hex values, off-scale spacing, near-duplicate colors.
- [design-qa](https://github.com/humbleteam/design-qa) - a pre-ship design QA gate: states, contrast, touch targets, breakpoints, keyboard paths.
- [design-handoff](https://github.com/humbleteam/design-handoff) - turn a finished mockup into a dev-ready spec: tokens, states, accessibility annotations, open questions.
- [accessibility-audit](https://github.com/humbleteam/accessibility-audit) - WCAG 2.2-grounded accessibility review with success-criterion citations and severity levels.
- [ux-writing](https://github.com/humbleteam/ux-writing) - interface copy that reads human: plain-verb microcopy rules and an AI-tell strip pass.
- [design-brief](https://github.com/humbleteam/design-brief) - extract a 5-bullet design brief from messy project inputs, with a gap report for what is missing.

## Who maintains this

Maintained by [Humbleteam](https://humbleteam.com/ai), a design and AI-engineering studio that builds AI infrastructure for design teams. This skill is distilled from the internal playbooks we run on client work. Issues and PRs welcome.

MIT - see [LICENSE](LICENSE).
