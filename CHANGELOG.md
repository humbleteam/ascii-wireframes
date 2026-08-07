# Changelog

## [1.1.0] - 2026-08-07

- Extended the wireframe legend to the controls real screens are built from: radios, dropdowns, toggles, repeated list or table rows, a below-the-fold marker, and modals drawn with `=` borders so the layer underneath stays readable. The legend previously stopped at buttons, inputs, checkboxes, icons, images, and active tabs, which left no way to sketch a settings screen or a data table.
- Resolved the deadlock between that gap and the "do not invent new symbols mid-response" rule. A control the legend does not name now borrows the nearest symbol it does and lets the label carry the meaning, with a failure-mode row that also forbids dropping the control to sidestep the problem, since a missing control changes the layout being judged.

## [1.0.0] - 2026-07-12

- Initial release: three-hypothesis ASCII wireframe generation with a fixed legend and size guardrails (60-80 characters wide, 8-20 lines tall).
- Adds a mobile-default sizing rule (390x844 proportions) for requests that do not state a platform.
- Adds a five-variant cap with a stated reason, and a one-question clarification path for under-specified requests.
- Adds handoff guidance to the html-mockup skill once a variant is picked, without generating HTML in this skill.
