# Frontend UX Heuristic Reference

Use this as the entry point for the heuristic reference helpers. Read only the heuristic files relevant to the current frontend task, unless the user asks for a full heuristic evaluation.

## Quick Review Procedure

1. Name the main user task and likely failure mode.
2. Scan the "When it applies" condition in the relevant helper files.
3. Inspect evidence in UI state, copy, layout, controls, and error paths.
4. Prioritize high-cost user harm first: lost work, irreversible action, blocked completion, data misunderstanding, repeated effort.
5. Convert each issue into a concrete UI change, not a vague principle.

## Heuristic Helpers

- [H1 Visibility of System Status](heuristics/01-visibility-of-system-status.md)
- [H2 Match Between the System and the Real World](heuristics/02-match-system-real-world.md)
- [H3 User Control and Freedom](heuristics/03-user-control-and-freedom.md)
- [H4 Consistency and Standards](heuristics/04-consistency-and-standards.md)
- [H5 Error Prevention](heuristics/05-error-prevention.md)
- [H6 Recognition Rather Than Recall](heuristics/06-recognition-rather-than-recall.md)
- [H7 Flexibility and Efficiency of Use](heuristics/07-flexibility-and-efficiency-of-use.md)
- [H8 Aesthetic and Minimalist Design](heuristics/08-aesthetic-and-minimalist-design.md)
- [H9 Help Users Recognize, Diagnose, and Recover from Errors](heuristics/09-error-recognition-and-recovery.md)
- [H10 Help and Documentation](heuristics/10-help-and-documentation.md)

## Context Helpers

- [Complex Applications](context/complex-applications.md): enterprise tools, domain-specific software, nonlinear workflows, dense data, trained users, high-impact decisions.
- [Forms and Inputs](context/forms-and-inputs.md): forms, validation, date input, radio buttons, checkboxes, dropdowns, constrained choices.
- [Interaction Patterns](context/interaction-patterns.md): tabs, accordions, dropdown menus, tooltips, icons, overlays, coach marks, progressive disclosure.
- [Search and Findability](context/search-and-findability.md): site/app/docs search, suggestions, scoped search, filters, no-results recovery, large information spaces.

## Review Prioritization

1. Lost work, irreversible action, or security/privacy/billing risk.
2. Blocked task completion or unrecoverable error.
3. Misleading state, status, or domain meaning.
4. Repeated effort for common workflows.
5. Visual clutter, unclear hierarchy, or unnecessary learning cost.
