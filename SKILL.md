---
name: ascii-wireframes
description: Sketches three genuinely different layout hypotheses as ASCII wireframes before any hi-fi design work starts. Use when a user asks to "show me some layout options", "sketch a few wireframes", "give me 3 versions of this screen", "explore layouts before Figma", or "ascii wireframe this". Do not use for pixel-faithful HTML mockups built from a reference screenshot - use html-mockup for that.
---

# ASCII wireframes

Explore layout directions cheaply, in text, before any pixels get pushed.

## Step 1 - scope the request

If the request already names a screen and its primary job (example: "pricing page for a B2B analytics tool, primary job: convert a trial user to a paid plan"), go to Step 2.

If either the screen or its primary job is missing, ask exactly one clarifying question covering both. Do not guess and do not proceed on a partial brief.

## Step 2 - decide three hypotheses

Pick three genuinely different hypotheses for the same screen. Each one is a different answer to: what value proposition does this screen lead with? A hypothesis is not valid if it only changes color, spacing, font, or component style from another one - that is a restyle, not a hypothesis.

Examples of distinct hypotheses for the same screen:

- Pricing page: (a) lead with a single recommended plan, (b) lead with a feature-comparison table, (c) lead with an ROI calculator.
- Onboarding flow: (a) lead with a guided product tour, (b) lead with a self-seeding empty state, (c) lead with a single setup question.
- Dashboard home: (a) lead with today's tasks, (b) lead with a project-board overview, (c) lead with a single focused item and its context.

If the user asks for more than 5 variants, cap at 5 and say why: past five, a reviewer stops comparing and starts skimming.

## Step 3 - render each hypothesis

For each hypothesis, in order, output exactly this shape:

1. A one-line label: `V<N> - <hypothesis in one phrase>`.
2. A fenced code block containing the ASCII wireframe. Use the legend below. Width 60-80 characters. Height 8-20 lines.
3. One plain-language line after the code block, stating the value proposition this variant leads with. No "Why:" prefix, no citation, no reference to a heuristic or a book. This phase stays cheap to reject - explanations belong later, in a design review.

Repeat for every hypothesis before moving to Step 4.

## Step 4 - close the loop

After the last variant, ask a single closing question: which variant or variants should move forward. Do not add commentary, a recommendation, or a "best" pick unless the user asks for one directly.

## Step 5 - handle the selection

When the user replies with a selection (example: "V1+V3" or "the second one"):

1. Confirm what was picked, in one line.
2. Tell the user the natural next step is a pixel-faithful HTML mockup built against a reference screenshot, and point at the html-mockup skill for that.
3. Do not generate HTML yourself in this skill, even if asked directly - say so plainly and suggest html-mockup instead.

## Wireframe legend

Use this legend consistently within one response, so the variants are easy to compare side by side:

- Border: `+`, `-`, `|`
- Section divider inside a frame: a full-width row of `-`
- Secondary button: `[ Label ]`
- Primary or CTA button: `[[ Label ]]`
- Text input: `[.....................]`
- Checkbox unchecked / checked: `[ ]` / `[x]`
- Icon: `(icon-name)`, for example `(search)`, `(bell)`, `(menu)`
- Image or photo region: a bordered box labeled `[IMG: description]` in its center - a label is enough at this fidelity, never draw decorative characters to simulate a photo
- Active nav or tab item: wrap the label in `*asterisks*`; inactive items stay plain

Reuse the same legend across all variants in one response. Do not invent new symbols mid-response.

## Sizing and platform defaults

- Width: 60-80 characters. Height: 8-20 lines. This range keeps a wireframe inside a chat pane or terminal without wrapping, and it forces the sketch to omit detail that belongs in hi-fi.
- If the user does not state a platform, default to mobile proportions: a narrower box (55-65 characters), taller relative to its width, mirroring a 390x844 mobile screen.
- If the user states desktop, tablet, or a specific width, use a wider, shorter box and honor it.

## Failure modes

| Situation | Response |
|---|---|
| Request names no screen, or no primary job | Ask one clarifying question covering both. Never guess. |
| User asks for more than 5 variants | Cap at 5. State the reason: more than five slows down comparison. |
| User asks for a citation, rationale, or "why" mid-sketch | Decline for this phase. Rationale belongs in a design review, once a direction is picked. |
| User asks for HTML or code directly | Do not produce it here. Name html-mockup as the next step and stop. |
| User attaches a screenshot instead of describing the screen | Treat the screenshot as the reference for the screen's content and layout, but still produce three hypotheses - do not just describe what is in the image. |

## Notes for the agent

- Keep the entire reply to the labeled wireframes plus the closing question. No preamble before the first variant, no summary paragraph after the last one.
- Every hypothesis must be defensible as a different product decision, not a different visual treatment of the same decision.
- The 60-80 / 8-20 ranges are guardrails for judgment, not something to visibly count out loud in the reply.
