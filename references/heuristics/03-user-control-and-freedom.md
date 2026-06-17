# H3 User Control and Freedom

Use when the UI includes modals, drawers, overlays, wizards, edit flows, destructive actions, uploads, downloads, filters, bulk edits, navigation, drafts, carts, or irreversible or multi-step tasks.

## Check

- Provide clear Cancel, Back, Close, Undo, Redo, or Restore paths as appropriate.
- Preserve work when users navigate away accidentally.
- Make exits discoverable and consistently placed.
- Support browser Back behavior when feasible; never trap users by disabling or hijacking it.
- Make Back return one step in the user's path, not unexpectedly cancel the whole flow or jump up the IA.
- Let users recover from accidental filter, selection, or edit changes.
- Avoid Reset buttons on ordinary forms; they usually add clutter and risk wiping user work by mistake.
- Use Cancel sparingly on simple web pages, but provide it for multi-step, high-commitment, long-running, or anxiety-producing tasks.
- Provide a way to interrupt long-running actions such as uploads, downloads, imports, generation, or processing.
- Make Undo discoverable, not only hidden behind a shortcut or a short-lived transient message.

## Exit Semantics

- `Back`: return to the previous page, screen, view, overlay state, or step without losing work.
- `Close`: dismiss a view, drawer, modal, or overlay and return to the underlying context.
- `Cancel`: abandon the current task or multi-step process; clarify whether work is discarded, saved as draft, or kept.
- `Undo`: revert the last change to system state; use Redo or multi-level Undo when users make many quick edits.
- `Reset`: restore safe defaults only for repeated-entry workflows or complex parameter exploration; do not use it to clear ordinary forms.

## Forms and Flows

- Prefer editable fields, neutral radio/menu options, clear/remove item controls, and Undo over full-form Reset.
- Include explicit default or "none" options for radio groups and select menus so users can return to the original state.
- If browser Back could lose work or break form logic, warn first and let users cancel the navigation.
- In multi-step flows, provide both local Back and global Cancel when their outcomes differ.
- When Cancel would discard work, offer save draft, continue editing, or discard choices when appropriate.

## Evidence

Look for undo snackbar, visible Undo/Redo commands, draft save, unsaved-change guard, escape key behavior, close button in modal header, labeled Cancel, reset filters, neutral field options, remove-from-cart control, restore deleted item, cancellable upload/download, and stepper back button.

## Failure Patterns

- Modal traps the user.
- Cancel and destructive actions are visually or spatially confused.
- Users lose form input on navigation.
- Back button exits the app instead of the current flow.
- Browser Back closes more than the current overlay or step.
- Reset sits next to Submit and can erase form work by mistake.
- Cancel is represented only by an ambiguous `X` when it discards progress.
- Undo is available only through an undisclosed keyboard shortcut, gesture, or disappearing snackbar.
- Users can start a long-running operation but cannot stop it.
