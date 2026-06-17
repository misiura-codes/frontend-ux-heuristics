---
name: frontend-ux-heuristics
description: "Use when designing, implementing, or reviewing user-facing UI through a usability lens - applying 10 heuristics to customer-facing or internal product flows, forms, navigation, loading/empty/error states, dashboards, components, copy clarity, status visibility, error recovery, recognition vs. recall, or efficiency tradeoffs."
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
2. Use the Condition Map to find the heuristics relevant to the surface under review, and load the matching helpers.
3. Lead findings with user impact, tagged by heuristic (for example `H5 Error Prevention`). Close with material risks needing research or product input.

## Condition Map

| Heuristic | Use this condition when the UI includes... |
| --- | --- |
| H1 Visibility of System Status | async actions, loading, saving, selected state, progress, navigation state, background sync, permission changes |
| H2 Match System and Real World | labels, copy, CTAs, icons, domain concepts, ordering, formats, units, controls, gestures, mental models, workflows mapped from offline behavior |
| H3 User Control and Freedom | modals, overlays, wizards, destructive actions, editing, uploads, downloads, filters, navigation, cancel/reset/undo behavior |
| H4 Consistency and Standards | new components, routes, actions, icons, keyboard behavior, web/platform/domain conventions, design-system variants, omnichannel touchpoints |
| H5 Error Prevention | forms, destructive or irreversible actions, constrained input, defaults, confirmations, high-cost choices, admin/security workflows |
| H6 Recognition Rather Than Recall | menus, search, filters, multi-step flows, cross-screen context, settings, comparison, history, dense task surfaces |
| H7 Flexibility and Efficiency | repeated work, power-user flows, bulk operations, search/filtering, keyboard/touch shortcuts, accelerators, personalization, customization, saved preferences |
| H8 Aesthetic and Minimalist Design | dashboards, page hierarchy, dense data, visual styling, scanability, content prioritization, affordances, decorative elements |
| H9 Error Recognition and Recovery | validation, failed requests, empty/no-result states, blocked states, partial failure, diagnostics, offline or permission errors, recovery actions |
| H10 Help and Documentation | complex, rare, new, or setup-heavy tasks; onboarding; permissions; imports; troubleshooting; searchable help/docs |

## Reference

Start with [index.md](references/index.md), then load only the helper files matching the task. Heuristic helpers live under `references/heuristics/`; context helpers under `references/context/`. Load all H1–H10 helpers only for a full heuristic evaluation.

Also load a context helper when the task matches:

- [complex-applications.md](references/context/complex-applications.md): enterprise tools, nonlinear workflows, dense data products, high-impact decision systems.
- [forms-and-inputs.md](references/context/forms-and-inputs.md): forms, validation, structured input, date fields, radio/checkbox/dropdown choices.
- [interaction-patterns.md](references/context/interaction-patterns.md): tabs, accordions, dropdowns, tooltips, icons, overlays, coach marks, progressive disclosure.
- [search-and-findability.md](references/context/search-and-findability.md): search, suggestions, scoped search, filters, no-results states, large information spaces.

## Output Pattern

For design or review output:

```text
H# Heuristic: finding or decision
Impact: user confusion, error, delay, or recovery risk
Action: concrete UI, copy, state, or interaction change
```

Example:

```text
H5 Error Prevention: "Delete project" has no confirmation and no undo path.
Impact: irreversible data loss from a single misclick on a high-cost action.
Action: require typed confirmation and surface a 10s undo toast after delete.
```

For implementation summaries, use one compact `UX coverage:` sentence.

## Common Mistakes

- Do not use help text to compensate for unclear labels, mapping, or options.
- Reserve confirmations for high-cost or hard-to-reverse actions.
- Do not hide essential task information for the sake of minimalism.
- Never rely on color alone for status or errors.
