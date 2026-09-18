---
name: ascii-wireframes
description: Sketches three genuinely different layout hypotheses as ASCII wireframes before any hi-fi design work starts. Use when a user asks to "show me some layout options", "sketch a few wireframes", "give me 3 versions of this screen", "explore layouts before Figma", or "ascii wireframe this". Do not use for pixel-faithful HTML mockups built from a reference screenshot - use html-mockup for that.
---

# ASCII wireframes

Explore layout directions cheaply, in text, before any pixels get pushed.

## Step 1 - scope the request

Two inputs open the gate: the **screen** and its **primary job**.

If the request already names both (example: "pricing page for a B2B analytics tool, primary job: convert a trial user to a paid plan"), go to Step 2.

If either is missing, ask exactly one clarifying question, covering only what is actually missing - both when both are missing, the job alone when the screen is already settled. Do not guess and do not proceed on a partial brief.

**An attached screenshot settles the screen, never the primary job.** It shows what is on the screen: the elements, the current layout, the content. It cannot show what the screen is for, and the job is what Step 2 needs to tell three hypotheses apart from three restyles - "lead with a recommended plan" and "lead with an ROI calculator" are only different answers if there is a question. So a screenshot arriving with no stated job still goes to the clarifying question, and that question asks about the job alone rather than about a screen the image already shows.

## Step 2 - decide the hypotheses

Three is the default, and a request that names no number gets three. Each hypothesis is a different answer to: what value proposition does this screen lead with? A hypothesis is not valid if it only changes color, spacing, font, or component style from another one - that is a restyle, not a hypothesis.

Examples of distinct hypotheses for the same screen:

- Pricing page: (a) lead with a single recommended plan, (b) lead with a feature-comparison table, (c) lead with an ROI calculator.
- Onboarding flow: (a) lead with a guided product tour, (b) lead with a self-seeding empty state, (c) lead with a single setup question.
- Dashboard home: (a) lead with today's tasks, (b) lead with a project-board overview, (c) lead with a single focused item and its context.

**A number the user states is used as given, anywhere from 2 to 5.** Both ends of that band carry a reason, and the reason is said out loud whenever the band bites. Past five a reviewer stops comparing and starts skimming, so a larger request is capped at 5. Below two there is nothing to compare: Step 4 closes by asking which variants move forward, and against a single sketch that question becomes a yes or no about the only thing on the page, which is a direction committed to rather than a direction picked. So a request for one comes back as 2, with that line under it.

**A count the screen cannot fill comes back short, never padded.** The validity rule above is what makes this bite: if the screen and its job carry three genuinely different bets and the request asked for five, the fourth and fifth arrive as restyles, and a restyle is not a hypothesis. Draw the ones that are real, and say in one line that the count is short because the screen does not carry more.

## Step 3 - render each hypothesis

For each hypothesis, in order, output exactly this shape:

1. A one-line label: `V<N> - <hypothesis in one phrase>`.
2. A fenced code block containing the ASCII wireframe. Use the legend below, and the width the platform rule picks - see Sizing and platform defaults. Height 8-20 lines.
3. One plain-language line after the code block, stating the value proposition this variant leads with. No "Why:" prefix, no citation, no reference to a heuristic or a book. This phase stays cheap to reject - explanations belong later, in a design review.

Repeat for every hypothesis before moving to Step 4.

## Step 4 - close the loop

After the last variant, ask a single closing question: which variant or variants should move forward. Do not add commentary, a recommendation, or a "best" pick.

**Being asked for a pick does not unlock one.** There is nothing in scope to pick on. Step 1 collects the screen and its primary job, and that is all it collects. The three hypotheses are three different product bets, and which bet is right turns on the users, the business model, and what the team can build - none of which a wireframe carries and none of which this skill asks for. A winner chosen from what is on the page is a preference wearing the word "recommendation", and Step 3 refuses rationale precisely to keep that out.

So when the user asks which one is best, neither refuse flatly nor answer. Both leave them where they started. Instead:

1. Name what each variant is betting on, one line each, in the same plain language as the line under its wireframe. This restates the trade-off; it does not rank it.
2. Ask the single question whose answer would decide it - the fact that separates the bets, not a survey. One question, the same discipline as Step 1.

The call stays with the user, who holds the context. A comparative verdict with reasons behind it is a design-review job, and it belongs after a direction is picked and there is a mockup to review.

## Step 5 - handle the selection

When the user replies with a selection (example: "V1+V3" or "the second one"):

1. Confirm what was picked, in one line.
2. Name the next step - a pixel-faithful HTML mockup, built by the html-mockup skill, with the picked wireframe as the structure to build against.
3. Say which marks in that wireframe are abbreviations rather than measurements, because the receiving skill cannot tell them apart. html-mockup opens by writing a census of its reference - exact item counts, photo regions and their sizes, button fills, the palette - and then treats that census as a contract the render has to satisfy, down to a fourth row where the census says three being a bug it fixes in the render rather than in the census. Three conventions in this skill are shorthand, and they harden into that contract if they travel unmarked:
   - A repeated row drawn as two real rows and a `...` says the list repeats. It never says the list holds two items, so the real count goes over with it.
   - `v v v` says content continues past the frame. A census line about a cut needs the item the frame clips and how much of it stays visible, and the marker carries neither.
   - `[IMG: description]` is a label, not a region. Its size and shape go over with it.

   A borrowed symbol travels the same way: a date picker drawn as `[ 12 Mar 2026 v ]` is a date picker, and only its label says so.
4. Say what the sketch never carried at all: palette, type, spacing, real copy. With a reference screenshot html-mockup reads those off it. Without one it builds anyway and marks every value it had to guess in its census, for correcting in one pass. So if the product exists anywhere already - a live page, a brand site - naming it now costs less than correcting a built mockup, and extract-design-tokens turns it into the palette and type scale the census would otherwise assume.
5. Do not generate HTML yourself in this skill, even if asked directly - say so plainly and suggest html-mockup instead.

## Wireframe legend

Use this legend consistently within one response, so the variants are easy to compare side by side:

- Border: `+`, `-`, `|`
- Section divider inside a frame: a full-width row of `-`
- Secondary button: `[ Label ]`
- Primary or CTA button: `[[ Label ]]`
- Text input: `[.....................]`
- Checkbox unchecked / checked: `[ ]` / `[x]`
- Radio unselected / selected: `( )` / `(o)`
- Dropdown or select: `[ Label v ]` - the trailing `v` is what separates it from a button
- Toggle off / on: `[o--]` / `[--o]`
- Icon: `(icon-name)`, for example `(search)`, `(bell)`, `(menu)` - an icon always carries a name inside the parentheses, which is how it stays distinct from a radio
- Image or photo region: a bordered box labeled `[IMG: description]` in its center - a label is enough at this fidelity, never draw decorative characters to simulate a photo
- Active nav or tab item: wrap the label in `*asterisks*`; inactive items stay plain
- Repeated rows (a list, a table, a feed): draw two real rows, then one row holding `...`. Never draw ten rows to prove a list is long
- Content continues below the fold: the last row inside the frame is `v v v`
- Modal, sheet, or overlay above the page: a nested box whose horizontal borders use `=` instead of `-`, so the layer it sits on stays readable behind it

Reuse the same legend across all variants in one response. Do not invent new symbols mid-response: when a screen needs a control this legend does not name, use the nearest symbol it does name and let the label carry the meaning - a date picker is `[ 12 Mar 2026 v ]`, a stepper is `[ - ] 3 [ + ]`. Add one plain line under the wireframe only when the borrowed symbol would otherwise be read as the wrong control.

## Sizing and platform defaults

- The envelope for every width this skill picks for itself: 55-80 characters wide, 8-20 lines tall. It keeps a wireframe inside a chat pane or terminal without wrapping, and it forces the sketch to omit detail that belongs in hi-fi. A width the user names is the one thing that overrides it.
- **The platform picks the width inside that envelope, and it always picks exactly one range.** No platform stated - mobile proportions: 55-65 characters, taller relative to its width, mirroring a 390x844 mobile screen. Mobile is the default because it is the harder constraint: a layout that survives 60 characters usually survives 80, and the reverse is not true.
- Desktop or tablet stated with no number: 66-80 characters, shorter relative to its width. A specific width stated as a number is used as given - if it falls outside 55-80, say in one line that it will wrap in a narrow pane, then draw it anyway.
- The two ranges do not overlap on purpose. One request has one width, and every variant in the response uses it - variants drawn at different widths cannot be compared down a column, which is the whole reason to sketch them in text.

## Failure modes

| Situation | Response |
|---|---|
| Request names no screen, or no primary job | Ask one clarifying question, covering only what is missing. Never guess. |
| User names a variant count between 2 and 5 | Draw that many. Three is the default only for a request that names no number. |
| User asks for more than 5 variants | Cap at 5. State the reason: more than five slows down comparison. |
| User asks for a single variant | Draw 2 and say why in one line: one sketch leaves the closing question nothing to choose between, which is committing to a direction rather than comparing two. |
| The screen carries fewer genuinely different bets than the count asked for | Draw the ones that are real and say in one line that the count is short. A variant added to reach the number is a restyle, which Step 2 does not accept as a hypothesis. |
| User asks for a citation, rationale, or "why" mid-sketch | Decline for this phase. Rationale belongs in a design review, once a direction is picked. |
| User asks which variant is best, or for a recommendation | Do not name one, and do not refuse flatly. Restate what each variant bets on in one line each, then ask the single question that would decide it. Step 1 collects the screen and its job, so nothing in scope ranks the variants as product bets - a pick made anyway is a preference in a recommendation's clothes. |
| User asks for HTML or code directly | Do not produce it here. Name html-mockup as the next step and stop. |
| User attaches a screenshot instead of describing the screen | The screenshot settles the screen, not its job. Job stated too - go to Step 2 and treat the image as the reference for the screen's content and layout. Job not stated - ask for it, in one question about the job alone. Either way the deliverable is the hypotheses, never a description of what is in the image. |
| Screenshot attached and the job is stated as "redesign this" or "make it better" | That names an outcome, not a job. Ask which of 2-3 plausible jobs the screen is for, drawn from what the image shows, so the user picks instead of writing a brief. |
| The screen needs a control the legend does not name | Borrow the nearest legend symbol and let the label do the work, per the legend's fallback rule. Never invent a symbol, and never drop the control from the sketch to avoid the problem - a missing control changes the layout being judged. |

## Notes for the agent

- Keep the entire reply to the labeled wireframes plus the closing question. No preamble before the first variant, no summary paragraph after the last one.
- Every hypothesis must be defensible as a different product decision, not a different visual treatment of the same decision.
- The width and height ranges are guardrails for judgment, not something to visibly count out loud in the reply.
