# Forms and Inputs

Use alongside H2, H4, H5, H6, and H9 when reviewing forms, validation, date input, radio buttons, checkboxes, dropdowns, constrained choices, or high-cost data entry.

## Control Choice

- Use radio buttons for mutually exclusive choices where exactly one answer is expected.
- Use checkboxes for independent options where zero, one, or many selections are valid.
- Use a single checkbox for one on/off option; make opt-in choices explicit and unchecked by default when consent or marketing is involved.
- Avoid dropdowns when users need to compare options, see all choices, or choose from a small set that could be shown directly.
- Use dropdowns when space is constrained and legal choices are known; keep labels visible before and after selection.
- Do not mix command menus, navigation menus, and form-value dropdowns without clear visual and behavioral distinction.

## Date and Structured Input

- Choose the input pattern by task: calendar pickers for near dates and ranges, typed input for birthdays or distant dates, short lists for few valid dates.
- Allow typing even when a picker exists if users may know the exact value.
- Accept common date separators, missing leading zeros, and localized formats where feasible; normalize instead of rejecting.
- Show format examples and constraints before submission.
- Disable unavailable dates only when the reason is clear or recoverable.
- Avoid split dropdowns for month/day/year unless the constrained list is genuinely useful.

## Validation

- Prefer inline validation after the user has finished a field; use immediate validation for complex fields such as passwords.
- Do not validate empty fields merely because users explored or moved focus.
- Show success indicators only when they add useful confidence for complex or availability-dependent fields.
- Keep field-level error messages adjacent to the field and visible while the user fixes it.
- Use validation summaries for global orientation, not as the only error indicator.
- Never hide form errors in tooltips; critical correction instructions must remain visible.

## Evidence

Look for correct radio/checkbox semantics, visible field labels, safe consent defaults, direct option display for small sets, accepted flexible formats, date-range constraints, inline validation timing, field-level messages, useful success indicators, and preserved input after failure.

## Failure Patterns

- Mutually exclusive choices use checkboxes, allowing invalid combinations.
- Consent, billing, privacy, or marketing defaults silently favor the business.
- Users must select simple values through long dropdowns or scrolling pickers.
- Date fields reject natural input without examples or suggestions.
- Error summaries force users to memorize errors while fixing fields.
- Tooltip-only validation hides required correction details.
