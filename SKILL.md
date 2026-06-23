---
name: frontend-ux-heuristics
description: "Use when designing, implementing, or reviewing user-facing UI through a usability lens. Applies 10 heuristics, plus accessibility considerations, to product flows, forms, navigation, dashboards, components, and loading/empty/error states."
---

# Frontend UX Heuristics

## Overview

Apply the 10 core usability heuristics as a design, implementation, and review lens. Use them to surface concrete UI changes, not as a scorecard.

## When NOT to Use

- Pure backend, infra, build, or dependency changes with no UI surface.
- Copy or content edits unrelated to a UI control or state.
- Pure styling tweaks that do not change behavior or information.

## Workflow

1. Identify the user, task, context, and failure consequence; state assumptions if unclear.
2. Use the Condition Map to find the heuristics relevant to the surface under review, and load the matching helpers and any matching context helper.
3. For screenshots or browser audits, state the evidence scope: full page, visible viewport only, multiple viewports, element/region crops, and any live DOM/accessibility/keyboard evidence. Do not imply unseen page regions were reviewed. Quote on-screen labels, product names, menu items, and copy exactly from the evidence; if you cannot read a string clearly, refer to it generically (for example "the platform" or "the active nav item") and mark it unverified. Never approximate a name or invent a plausible one.
4. Sweep for consistency: list each repeated element (columns, rows, buttons, fields, nav items, icons) and check that every instance matches. A single instance that breaks the pattern is a finding, not a strength.
5. Consider accessibility as one review lens for visual or interactive UI when evidence is available: contrast, color independence, focus, keyboard access, target size, accessible names, and motion.
6. Use the prompt to choose the smallest useful response shape. Load [output/index.md](references/output/index.md) only when formatting guidance is needed: structured audits, screenshot/page reviews, annotated screenshots, Markdown report assets, or explicit review modes.
7. Lead with the plain-language product/design point a person can act on. Use heuristic tags as supporting evidence, not as the main structure, unless the user asks for a formal heuristic evaluation.
8. For every material issue, include at least one concrete fix example, copy example, layout pattern, state pattern, or best-practice alternative. State each issue once; do not pad.
9. For Markdown reports with images or supporting files, use a per-report folder with `report.md` and relative asset links.
10. Do not manufacture findings. If there are no material issues, say that plainly and separate optional polish from real risks.
11. Close with material risks, missing states, or research/product questions only when they would change the recommendation.

## Condition Map

| Heuristic | Use this condition when the UI includes... |
| --- | --- |
| H1 Visibility of System Status | async actions, loading, saving, selected state, progress, navigation state, background sync, permission changes |
| H2 Match Between the System and the Real World | labels, copy, CTAs, icons, domain concepts, ordering, formats, units, controls, gestures, mental models, workflows mapped from offline behavior |
| H3 User Control and Freedom | modals, overlays, wizards, destructive actions, editing, uploads, downloads, filters, navigation, cancel/reset/undo behavior |
| H4 Consistency and Standards | new components, routes, actions, icons, keyboard behavior, web/platform/domain conventions, design-system variants, omnichannel touchpoints |
| H5 Error Prevention | forms, destructive or irreversible actions, constrained input, defaults, confirmations, high-cost choices, admin/security workflows |
| H6 Recognition Rather Than Recall | menus, search, filters, multi-step flows, cross-screen context, settings, comparison, history, dense task surfaces |
| H7 Flexibility and Efficiency of Use | repeated work, power-user flows, bulk operations, search/filtering, keyboard/touch shortcuts, accelerators, personalization, customization, saved preferences |
| H8 Aesthetic and Minimalist Design | dashboards, page hierarchy, dense data, visual styling, scanability, content prioritization, affordances, decorative elements |
| H9 Help Users Recognize, Diagnose, and Recover from Errors | validation, failed requests, empty/no-result states, blocked states, partial failure, diagnostics, offline or permission errors, recovery actions |
| H10 Help and Documentation | complex, rare, new, or setup-heavy tasks; onboarding; permissions; imports; troubleshooting; searchable help/docs |

## Reference

Use the Condition Map above to identify relevant heuristics, then start with [index.md](references/index.md) to load only the matching helper files. Load all H1-H10 helpers only for a full heuristic evaluation.

## Output Pattern

Apply H8 to your own report: state each issue once, lead with the action, keep it scannable. Load [output/index.md](references/output/index.md) when the prompt needs structured report templates, depth modes, screenshot annotation guidance, or report assets.

For issue-level detail, the full shape is below. Drop any line that would only restate the finding, and tag heuristics by number (`H5`), not full name, to avoid drift and clutter:

```text
Finding: plain-language observation or decision
Why it matters: user confusion, error, delay, or recovery risk
Fix: concrete UI, copy, state, or interaction change
Impact: high | medium | low (optional; see the review-modes.md impact labels)
Heuristic: H# (optional)
```

Example:

```text
Finding: "Delete project" has no confirmation and no undo path.
Why it matters: irreversible data loss from a single misclick.
Fix: require typed confirmation, then a 10s undo toast after delete.
Impact: high
Heuristic: H5
```

## Common Mistakes

- Do not use help text to compensate for unclear labels, mapping, or options.
- Reserve confirmations for high-cost or hard-to-reverse actions.
- Do not hide essential task information for the sake of minimalism.
- Never rely on color alone for status or errors.
- Do not pad the report: state each issue once and never restate a finding as a separate next step.
- Do not force a critique to please the reviewer. A clean review with no material findings is a valid result.
- Do not mix optional polish with material issues; label it separately or omit it.
- Do not treat one viewport as a full-page audit. Say `visible viewport only` unless full-page or multi-viewport evidence was captured.
- Do not default to full-page annotated screenshots when a browser can identify the affected element or region. Prefer targeted crops when they explain the finding with less noise.
- Do not scatter report screenshots and crops beside unrelated reports. Use a report folder when assets are present.
- Do not guess about sticky headers, menus, modals, mobile, hover, focus, keyboard, loading, empty, or error states that were not captured or inspected.
- Do not claim accessibility findings without evidence; mention accessibility only when visible, inspectable, or requested.
- Do not invent or paraphrase product names, menu items, labels, or copy. Quote on-screen text exactly; if a string is unreadable in the evidence, use a generic reference and flag it as unverified instead of guessing. A hedge like "appears to be X" is still a guess: drop the name, not the hedge.
