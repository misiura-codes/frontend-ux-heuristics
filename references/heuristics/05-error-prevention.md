# H5 Error Prevention

Use when the UI includes forms, destructive actions, high-cost choices, defaults, confirmations, permissions, billing, admin/security changes, imports, data transformation, search, precision input, or constrained inputs.

## Check

- Prevent high-cost errors before lower-cost annoyances.
- Separate slips from mistakes: slips are right intent with wrong action; mistakes are wrong intent from incomplete or incorrect understanding.
- Use constraints, defaults, masks, suggestions, and forgiving formatting to reduce slips.
- Help users form the right goal by showing context, previews, representative examples, and consequences.
- Confirm only serious, destructive, expensive, unusual, or hard-to-reverse actions; avoid routine confirmation fatigue.
- Disable invalid actions only when the reason and remedy are visible.
- Prefer prevention and undo over asking users to be more careful.

## Prevent Slips

- Constrain impossible choices when rules are clear, such as invalid date ranges, incompatible options, or unavailable actions.
- Offer suggestions, autocomplete, search predictions, and selectable presets to reduce typing and memory burden.
- Format precise input as users type so values are easy to scan and verify.
- Accept forgiving formats and normalize behind the scenes instead of rejecting natural input.
- Make the active field, selected object, and pending target obvious before users act.

## Prevent Mistakes

- Explain domain concepts, tradeoffs, and consequences before users commit to an inappropriate goal.
- Show previews, summaries, affected object names, counts, costs, permissions, recipients, or irreversible effects.
- Detect unusual choices relative to the user's history or task context and add friction only there.
- Use progressive disclosure for consequences that matter but would overload the main flow.
- Avoid relying on training, help docs, or post-submit errors to compensate for a misleading workflow.

## Defaults

- Use helpful defaults because users often keep them.
- Choose defaults from likely user goals, common values, context, or safe values, not arbitrary first options.
- Use defaults as just-in-time examples that teach expected format or typical scope.
- Avoid self-serving defaults that silently increase cost, privacy exposure, commitment, or risk.
- Make non-default choices available and visible when user needs vary.

## Confirmations

- Make confirmation copy specific: name the object, scope, consequence, reversibility, and relevant count or amount.
- Use action-labeled buttons such as `Delete file` and `Keep file`, not generic `Yes` and `No`.
- Do not default focus to the dangerous confirmation action; often use no default or a safe default.
- For rare, severe actions, require a nonstandard confirmation step, such as typing the object name or a keyword.
- Keep confirmation text scannable and expose secondary detail through progressive disclosure.
- Offer undo or delayed execution where possible; confirmations reduce errors but do not eliminate them.

## Evidence

Look for date-range constraints, disabled impossible combinations with visible reasons, input formatting, forgiving parsing, autocomplete suggestions, previews, safe defaults, duplicate detection, attachment reminders, role-change summaries, anomaly warnings, and destructive confirmation with object name, count, consequence, and action-labeled buttons.

## Failure Patterns

- All prevention is deferred to an error message after submit.
- A confirmation dialog appears for every minor action.
- Invalid combinations can be selected freely.
- Users can submit irreversible changes without seeing the target object or consequences.
- A default is arbitrary, self-serving, risky, or likely to be accepted without thought.
- Confirmation asks "Are you sure?" without saying what will happen.
- The dangerous confirmation action is visually primary, focused by default, or labeled generically.
- The UI rejects natural formatting instead of accepting and normalizing it.
- Users must remember which object, date, recipient, permission, or mode they are changing.
- High-risk workflows rely on documentation or training instead of constraints, summaries, and previews.
