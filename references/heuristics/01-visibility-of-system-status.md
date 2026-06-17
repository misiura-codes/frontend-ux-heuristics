# H1 Visibility of System Status

Use when the UI includes async work, pending mutations, loading, saving, selected state, filters, active navigation, progress, background sync, external changes, inventory/availability, permissions, or disabled controls.

## Check

- Show immediate feedback that the system received the user action.
- Show current state close to the affected control or content, not only in a global toast.
- Distinguish loading, empty, partial, success, saved, unsaved, failure, disabled, selected, stale, and permission states.
- Explain automatic, time-based, or external changes instead of silently mutating or removing UI.
- Surface backstage state only when it changes user decisions, trust, or next actions.
- For long tasks, show progress, queue position, remaining work, last update time, or a useful fallback.
- Preserve user control after state changes: let users review, undo, retry, remove, or keep changed items when relevant.

## Feedback Timing

- Direct manipulation needs visible response on every meaningful interaction: press, select, drag, reorder, submit, save, upload, or delete.
- If work takes longer than an instant, replace ambiguous silence with pending state, busy affordance, skeleton, spinner, or progress.
- Prevent duplicate effort by disabling or changing submitted controls only when the UI also explains what is happening.
- For screenless, voice, or background actions, provide at least a visible, audible, or haptic acknowledgement that the command was heard.

## What to Surface

- Current location or scope: active nav, selected tab, selected row, active filters, current step.
- Transaction state: saving, saved, unsaved changes, failed save, sync conflict, last synced.
- Process state: queued, processing, progress, partial completion, retrying, complete.
- Availability state: low stock, sold out, unavailable option, permission denied, feature unavailable.
- External change state: item changed elsewhere, removed from source, expired session, stale data, background refresh.

## Evidence

Look for skeletons or progress indicators, selected-row state, active nav, visible selected controls, "saved" or "last synced" status, disabled reasons, optimistic state with rollback, upload progress, low-stock or unavailable-item messaging, and background refresh indicators.

## Failure Patterns

- Button click appears to do nothing.
- Data disappears or changes with no explanation.
- Toast is the only evidence of a durable state change.
- Disabled actions have no visible reason.
- Long-running work gives no progress, fallback, or confidence that the system is still working.
- The UI hides a user-relevant backstage state, such as unavailable inventory, stale data, permission loss, or sync failure.
- Feedback exists but is detached from the affected object, so users cannot tell what changed.
