# Changelog

## [1.2.0] - 2026-08-13

- Fixed the contradiction that governed every screenshot request. Step 1 requires both the screen and its primary job before sketching and says not to proceed on a partial brief, while the failure-modes table told the skill to take a screenshot and produce three hypotheses anyway. A screenshot supplies the screen and never the job, so the two rules gave opposite instructions on the most common way this skill is invoked - drop an image, ask for options.
- Step 1 now states that a screenshot settles the screen, not the job, with the reason: the job is what separates three hypotheses from three restyles. A screenshot with no stated job goes to the clarifying question, and that question asks about the job alone rather than re-asking what the image already shows.
- The clarifying question is now scoped to what is actually missing, instead of always covering both inputs.
- Rewrote the screenshot failure-mode row to give both branches, and added a row for "redesign this" or "make it better" offered as the job - an outcome, not a job, answered by offering 2-3 plausible jobs read off the image so the user picks rather than writes a brief.

## [1.1.0] - 2026-08-07

- Extended the wireframe legend to the controls real screens are built from: radios, dropdowns, toggles, repeated list or table rows, a below-the-fold marker, and modals drawn with `=` borders so the layer underneath stays readable. The legend previously stopped at buttons, inputs, checkboxes, icons, images, and active tabs, which left no way to sketch a settings screen or a data table.
- Resolved the deadlock between that gap and the "do not invent new symbols mid-response" rule. A control the legend does not name now borrows the nearest symbol it does and lets the label carry the meaning, with a failure-mode row that also forbids dropping the control to sidestep the problem, since a missing control changes the layout being judged.

## [1.0.0] - 2026-07-12

- Initial release: three-hypothesis ASCII wireframe generation with a fixed legend and size guardrails (60-80 characters wide, 8-20 lines tall).
- Adds a mobile-default sizing rule (390x844 proportions) for requests that do not state a platform.
- Adds a five-variant cap with a stated reason, and a one-question clarification path for under-specified requests.
- Adds handoff guidance to the html-mockup skill once a variant is picked, without generating HTML in this skill.
