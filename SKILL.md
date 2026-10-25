---
name: ascii-wireframes
description: Sketches genuinely different layout hypotheses as ASCII wireframes before any hi-fi design work starts - three by default, or the number the user names, anywhere from 2 to 5. Use when a user asks to "show me some layout options", "sketch a few wireframes", "give me 3 versions of this screen", "draw two layout directions for this page", "explore layouts before Figma", or "ascii wireframe this". Do not use for pixel-faithful HTML mockups built from a reference screenshot - use html-mockup for that.
---

# ASCII wireframes

Explore layout directions cheaply, in text, before any pixels get pushed.

## Step 1 - scope the request

Two inputs open the gate: the **screen** and its **primary job**.

If the request already names both (example: "pricing page for a B2B analytics tool, primary job: convert a trial user to a paid plan"), go to Step 2.

If either is missing, ask exactly one clarifying question, covering only what is actually missing - both when both are missing, the job alone when the screen is already settled. Do not guess and do not proceed on a partial brief.

**An attached screenshot settles the screen, never the primary job.** It shows what is on the screen: the elements, the current layout, the content. It cannot show what the screen is for, and the job is what Step 2 needs to tell hypotheses apart from restyles - "lead with a recommended plan" and "lead with an ROI calculator" are only different answers if there is a question. So a screenshot arriving with no stated job still goes to the clarifying question, and that question asks about the job alone rather than about a screen the image already shows.

## Step 2 - decide the hypotheses

Three is the default, and a request that names no number gets three. Each hypothesis is a different answer to: what value proposition does this screen lead with? A hypothesis is not valid if it only changes color, spacing, font, or component style from another one - that is a restyle, not a hypothesis.

Examples of distinct hypotheses for the same screen, at the default count of three:

- Pricing page: (a) lead with a single recommended plan, (b) lead with a feature-comparison table, (c) lead with an ROI calculator.
- Onboarding flow: (a) lead with a guided product tour, (b) lead with a self-seeding empty state, (c) lead with a single setup question.
- Dashboard home: (a) lead with today's tasks, (b) lead with a project-board overview, (c) lead with a single focused item and its context.

Three sets of three illustrate the default, not the band. The same screens at the counts either side of it:

- "Draw a couple of directions for the pricing page" - two, because a word that names a count is a stated count: (a) lead with a single recommended plan, (b) lead with an ROI calculator. The feature-comparison table is the one that goes, and it goes because it sits between the other two rather than because it was third on the list - it asks the user to decide, like the calculator, but out of the page's own content, like the recommended plan.
- "Five options for the dashboard home" - five, because this screen carries five different bets: (a) lead with today's tasks, (b) lead with a project-board overview, (c) lead with a single focused item and its context, (d) lead with the team's activity feed, (e) lead with a summary of delivery metrics.
- "Five options for the onboarding flow" - three, plus the one line saying the count is short. That flow carries the guided tour, the self-seeding empty state and the setup question; a fourth and a fifth would rearrange one of those, and a rearrangement is a restyle.

**A stated count below what the screen carries is filled with the hypotheses furthest apart.** The rule above said a stated number is used as given and said nothing about which ones to draw, so a pricing page carrying three bets and a request for two left the choice unwritten - and the obvious move, taking the first two off the list, is the one that costs the most. Two hypotheses next to each other are the pair closest to being a restyle of each other, which is the single relation the validity rule rejects between hypotheses, so a comparison built out of them shows less spread than the screen actually has while looking complete. Pick for distance on what the screen leads with, and name the dropped direction in one line if the user asks what is missing. Distance is also what the band's floor is protecting: two sketches are only worth comparing when they are two different answers.

**A number the user states is used as given, anywhere from 2 to 5.** Both ends of that band carry a reason, and the reason is said out loud whenever the band bites. Past five a reviewer stops comparing and starts skimming, so a larger request is capped at 5. Below two there is nothing to compare: Step 4 closes by asking which variants move forward, and against a single sketch that question becomes a yes or no about the only thing on the page, which is a direction committed to rather than a direction picked. So a request for one comes back as 2, with that line under it.

**A word states a number only when it names one.** "A couple" and "a pair" name two the way the digit does, and they are used as given. "Some", "a few", "several" and "a handful" name no count at all - they ask for a comparison and leave the size of it open - so they take the default three. The test is whether being wrong about the word would cost the user anything: someone who asked for a couple and got three was handed a variant they did not ask for, while someone who asked for a few and got three got what the word meant.

**A count the screen cannot fill comes back short, never padded.** The validity rule above is what makes this bite: if the screen and its job carry three genuinely different bets and the request asked for five, the fourth and fifth arrive as restyles, and a restyle is not a hypothesis. Draw the ones that are real, and say in one line that the count is short because the screen does not carry more.

**A screen carrying one bet is not a short count, it is the wrong input.** Read alone, the rule above sends a screen with a single genuine bet back as one sketch, which is the state the floor exists to prevent arriving by the other route: the floor's reason is about what ends up on the page, not about what was asked for, so Step 4's closing question collapses into a yes or no about the only thing there whether the count came from the request or from the screen. Padding to two is not the way out, because the floor's own reason is that two sketches are worth comparing only when they are two different answers, so a variant invented to satisfy it fails the rule it was invented for. Neither number is legal, which means the count is not what is wrong. Two things cause it, and the reply names which:

- **The job already contains the bet.** "Convert the trial user by leading with the recommended plan" leaves one hypothesis able to answer it, because the answer is inside the question. Restating the job one level up - "convert the trial user" - opens the screen again, so ask for that, in one question, the same as Step 1.
- **The screen has one shape.** A 404, a confirmation, a loading state, a single-field form. Draw the one structure and label it for what it is rather than numbering it `V1`, which would announce a set that does not exist. Say the screen carries one bet and name it, then ask the one question whose answer would open a second. That question is also the honest version of Step 4's close, since there is nothing to pick between.

**A request for one variant on a screen that carries one bet is those two rules colliding, and the one-bet rule wins.** The band's floor sends a request for one back as 2. The paragraph above says a second sketch on a one-bet screen is a restyle. Both describe this input, they give opposite answers, and the floor is the rule a reader meets first. It loses on its own reasoning: the floor protects what ends up on the page rather than the number in the request, and the reason it gives for refusing a single sketch - that Step 4's closing question needs two different answers to choose between - is the same reason the padded second sketch fails. Drawing 2 here keeps the floor's words and breaks the thing it exists for. So the reply is the one-bet reply, and the user who asked for one does not get one either: name the bet, say the count is not what is wrong, and ask whether the job already contains the bet or the screen has one shape. The line under it is the honest version of the floor's own line - not "here are two" but "one is what this screen carries, and here is the question that would make it two".

**A stated count inside the band meets the same wall, and the stated number loses for a different reason.** The paragraph above settles a request for one, which is the floor's case - one is outside the band, so the band is what has to give way. A request for two on a one-bet screen is not that case at all: two is legal, the band never bites, and the rule that a stated number is used as given says nothing about what the screen can carry. Two rules reach for this input and both arrive somewhere illegal. Used-as-given draws a second sketch, which is the restyle the validity rule rejects. The short-count rule draws the ones that are real and says the count is short, which lands on the single sketch the floor exists to prevent and on a sentence the paragraph above already denies, since a one-bet screen is not a short count. Used-as-given loses because it was never absolute: the short-count rule is already its exception, written for the screen carrying three when five were asked for, and a one-bet screen is only that exception at the end of its range, where going short arrives at a number no rule here will print. So the one-bet reply is the answer for any stated count from two to five, the same reply a stated one gets, and the same reply a request naming no number gets. Only the closing line moves with the request: a user who asked for two is told the screen carries one bet, never that it carries one of the two.

## Step 3 - render each hypothesis

For each hypothesis, in order, output exactly this shape:

1. A one-line label: `V<N> - <hypothesis in one phrase>`.
2. A fenced code block containing the ASCII wireframe. Use the legend below, and the width the platform rule picks - see Sizing and platform defaults. Height 8-20 lines.
3. One plain-language line after the code block, stating the value proposition this variant leads with. No "Why:" prefix, no citation, no reference to a heuristic or a book. This phase stays cheap to reject - explanations belong later, in a design review.

Repeat for every hypothesis before moving to Step 4.

## Step 4 - close the loop

After the last variant, ask a single closing question: which variant or variants should move forward. Do not add commentary, a recommendation, or a "best" pick.

**Being asked for a pick does not unlock one.** There is nothing in scope to pick on. Step 1 collects the screen and its primary job, and that is all it collects. The hypotheses are different product bets, and which bet is right turns on the users, the business model, and what the team can build - none of which a wireframe carries and none of which this skill asks for. A winner chosen from what is on the page is a preference wearing the word "recommendation", and Step 3 refuses rationale precisely to keep that out.

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
| User names a variant count between 2 and 5 | Draw that many. Three is the default only for a request that names no number. Unless the screen carries one bet, in which case no count is drawn and the one-bet row governs. |
| Request says "a couple" or "a pair" | A word that names a count is a stated count: draw 2. "Some", "a few", "several" and "a handful" name no count and take the default three. |
| User asks for more than 5 variants | Cap at 5. State the reason: more than five slows down comparison. |
| User asks for a single variant | Draw 2 and say why in one line: one sketch leaves the closing question nothing to choose between, which is committing to a direction rather than comparing two. Unless the screen itself carries one bet, in which case 2 is not drawn and the one-bet row governs. |
| The screen carries fewer genuinely different bets than the count asked for | Draw the ones that are real and say in one line that the count is short. A variant added to reach the number is a restyle, which Step 2 does not accept as a hypothesis. This row stops at two: if the real count is one, going short lands on a single sketch, so a one-bet screen is not a short count and the one-bet row governs instead. |
| The screen carries exactly one genuinely different bet | Not a short count. One sketch leaves the closing question nothing to choose between, and a padded second one is a restyle, so neither number is legal. Say the screen carries one bet and name it. Ask whether the job was stated so narrowly that it already contains the bet, in which case restating it one level up opens the screen. If the screen truly has one shape, draw that structure unnumbered rather than as `V1` and ask the one question that would open a second bet. |
| The user states a count - one, or anything from 2 to 5 - and the screen carries exactly one bet | The one-bet row wins over whichever rule the stated number reached for. A stated one is the floor's case, and the floor loses on its own reasoning: it protects what reaches the page rather than the number in the request, and its reason for refusing one sketch is the reason a padded second fails, so drawing 2 would keep its words and break what it is for. A stated 2 to 5 is the used-as-given rule's case, and that rule was already bounded by what the screen carries - the short-count row is its exception - so a one-bet screen is where the bound ends rather than a count to honour. Give the one-bet reply either way and say the count is not what is wrong. Never that it is short: the screen carries one bet, not one of the number asked for. |
| The screen carries more genuinely different bets than the count asked for | Draw the ones furthest apart on what the screen leads with, never the first ones off the list. The nearest pair is the closest thing to a restyle of each other, which Step 2 rejects between hypotheses, so it hands back less spread than the screen has while looking complete. |
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
