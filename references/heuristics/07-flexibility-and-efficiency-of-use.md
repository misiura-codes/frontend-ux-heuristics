# H7 Flexibility and Efficiency of Use

Use when the UI includes repeated tasks, expert users, admin tools, data tables, bulk operations, keyboard-heavy workflows, gestures, macros, automation, personalization, customization, saved views, saved preferences, recent items, or shortcuts.

## Check

- Keep the novice path visible and safe.
- Add optional accelerators for frequent or expert tasks without replacing the standard path.
- Support bulk actions, saved filters/views, keyboard shortcuts, gestures, macros, command palettes, recent items, and repeat-last settings when they reduce repeated effort.
- Let users customize high-frequency views without making setup mandatory or using customization to hide a weak default experience.
- Use personalization to streamline content or functionality only when the system has reliable data and users retain control.
- Make accelerators discoverable over time through menus, tooltips, command palettes, contextual hints, or shortcut sheets.
- Provide feedback, undo, and recovery for fast actions that can be triggered accidentally.

## Accelerators

- Treat accelerators as alternate methods for existing actions, not separate features.
- Add accelerators only for routine, repeated, or high-volume actions where the learning cost pays off.
- Reveal shortcuts gradually and contextually after users have used the standard action.
- Display keyboard shortcuts inline next to menu or command labels when appropriate.
- Keep accelerators unobtrusive: novices should be able to ignore them and still complete the task.
- Do not override common platform shortcuts such as copy, paste, select all, save, print, or browser navigation.
- Keep shortcuts and gestures consistent across platforms where the same product behavior exists.

## Multiple Paths

- Provide guided paths for novices and faster paths for experienced users.
- Avoid prescriptive flows when users may validly approach the same goal in different ways.
- Support batch selection, bulk edit, duplicate, templates, import/export, saved queries, macros, and automations for repeated work.
- Keep advanced setup proportional to task frequency; do not require automation configuration for one-off tasks.
- Let expert controls live in menus, panels, or settings where they are available but not visually dominant.

## Personalization and Customization

- Personalization is system-driven; customization is user-driven.
- Use personalization to remember recent actions, frequent selections, known user data, role-specific tools, saved progress, and cross-device continuation.
- Let users edit autofilled or personalized values and switch out of role-based or inferred views when needed.
- Review personalization data, roles, and rules regularly; stale or over-specific assumptions degrade efficiency.
- Use customization when users know their own priorities, such as pinned links, saved columns, dashboard modules, topics, shortcuts, or display preferences.
- Keep customization reversible and maintainable; users' needs change over time.
- Do not rely on personalization or customization to prune an overloaded interface; fix the base IA and workflow first.

## Evidence

Look for keyboard shortcut labels, command palette, contextual shortcut hints, saved table preferences, bulk edit, duplicate action, recent templates, repeat-last settings, macros, automation, undo after accelerator actions, personalized recent/frequent items, editable autofill, role switcher, default filters, and user-level settings.

## Failure Patterns

- The shortcut is the only path.
- Expert options clutter the novice flow.
- Repetitive work requires one-by-one interaction.
- Customization is offered before the base workflow is clear.
- Accelerators exist for rarely used actions but not for high-frequency work.
- Keyboard shortcuts or gestures are hidden, undocumented, or inconsistent with platform norms.
- A gesture or shortcut causes destructive change without feedback or undo.
- Personalization hides useful content, tools, or alternate roles with no way out.
- Personalization is based on stale, narrow, or unreliable data.
- Users must repeatedly reconfigure the same view, filters, columns, sort order, or template.
- Customization requires high setup cost for low-value or one-off tasks.
