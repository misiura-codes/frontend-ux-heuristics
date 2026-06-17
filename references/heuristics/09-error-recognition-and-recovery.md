# H9 Help Users Recognize, Diagnose, and Recover from Errors

Use when the UI includes validation, failed network requests, blocked permissions, empty/no-result states, offline mode, partial failure, import errors, submission failures, unavailable actions, diagnostics, or technical/professional workflows.

## Check

- Make the error visible and close to its source.
- Use accessible indicators; do not rely on color alone.
- Explain what happened in plain, human-readable language.
- State the exact fix, next best action, or available workaround.
- Preserve user input and reduce correction effort.
- Match severity to presentation: inline message, banner, toast, modal, or blocking page.
- Avoid premature errors while users are still exploring.
- Help users diagnose without exposing raw implementation details as the main message.
- Keep expert-facing errors concise and plain; experts also prefer scannable, jargon-free guidance.
- Use a positive, nonjudgmental tone that does not blame users.

## Visibility

- Put field errors next to the affected field and provide an error summary when multiple fields need attention.
- Use redundant indicators such as text, icon, border, heading, and ARIA state rather than color alone.
- Reserve modals and blocking pages for severe errors that require immediate resolution.
- Use banners, inline messages, or persistent notices for recoverable issues that affect a region or task.
- Avoid disappearing toasts for errors that require reading, decision-making, or action.
- Time validation carefully: validate immediately for error-prone formatted inputs, but do not punish exploratory focus/blur.

## Communication

- Describe the specific problem, object, field, limit, status, or failed condition.
- Avoid generic copy such as `Something went wrong` unless paired with a next step and diagnostics path.
- Avoid obscure codes, stack traces, abbreviations, branded terms, and backend names in the primary message.
- Include technical diagnostics only as secondary, copyable detail for support or expert troubleshooting.
- Avoid humor for frequent, serious, costly, or user-blocking errors.
- Use terms users search for and understand, not internal service names.

## Recovery

- Preserve all user input, selections, uploads, filters, and progress unless unsafe.
- Offer direct fixes: retry, edit field, change filter, choose suggested value, restore draft, reconnect, request access, or contact support.
- Reduce correction work by suggesting likely fixes, matching values, allowed formats, or alternative options.
- Explain whether the user can continue, must change something, should wait, or needs help from another role.
- Link to deeper help only after giving the short recovery instruction in place.
- For total service failure, acknowledge the issue, protect user work, and provide status or retry timing.

## Evidence

Look for inline validation, field-level messages, accessible error summary, persistent banners for task-level failures, retry action, "change filter" action, preserved form values, suggested corrections, draft restore, copyable diagnostics for technical users, support escalation path, and status/retry timing.

## Failure Patterns

- "Something went wrong" with no next step.
- Error code appears without user-facing explanation.
- Toast disappears before the user can act.
- A failed submission clears the form.
- Error is far from the field or object that caused it.
- Error copy blames the user with words like invalid, illegal, wrong, or forbidden when a neutral explanation would work.
- Expert-facing messages use jargon, branded names, or dense prose that slows diagnosis.
- The UI identifies the problem but gives no recovery action.
- Multiple errors appear with no summary or path to the first issue.
- Validation appears before users have had a reasonable chance to answer.
- The UI hides recoverable alternatives, such as changing a filter, selecting a suggested match, saving a draft, or retrying later.
