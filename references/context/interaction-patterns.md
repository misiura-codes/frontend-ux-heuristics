# Interaction Patterns

Use alongside H3, H4, H6, H8, and H10 when reviewing tabs, accordions, dropdown menus, tooltips, icons, overlays, coach marks, or progressive disclosure.

## Tabs

- Use tabs when content has a few clear groups, concise labels, and users need only one panel at a time.
- Do not hide critical content in nondefault tabs; default tabs receive disproportionate attention.
- Keep in-page tabs and navigation tabs behaviorally distinct; do not mix them in one tab set.
- Show selected state with at least two clear indicators when possible: line, font weight, color, size, common region, or icon.
- Keep unselected tabs readable and discoverable; low contrast can make them seem disabled.
- Avoid stacked or carousel tabs unless unavoidable; hidden tabs increase interaction cost and weaken spatial memory.

## Accordions and Disclosure

- Use accordions when users need only a few sections and headings are highly descriptive.
- Prefer one longer scannable page when users likely need most sections or must compare across sections.
- Treat every expand/collapse decision as interaction cost; do not use accordions just to reduce scrolling.
- Make expanded/collapsed state obvious and preserve state when users return.
- Use staged disclosure for advanced or conditional details, not for information required to understand the primary task.

## Tooltips and Contextual Tips

- Use tooltips for brief, nonessential explanations tied to a specific element.
- Keep essential instructions, field requirements, and error messages visible on the page.
- Support mouse and keyboard access; do not rely on hover-only behavior for touch or accessibility.
- Keep tooltip copy short, useful, and nonredundant.
- Position tooltips so they do not cover the content they explain.
- Use arrows or other anchors when several nearby elements could own the tip.

## Icons and Visual Signifiers

- Pair icons with text labels unless the icon is standard, repeatedly learned, and low risk.
- Test icon meaning in context; most icons are ambiguous outside a few established cases.
- Do not rely on hover labels to make navigation icons understandable.
- Preserve clickability signifiers in flat or minimalist styling: shape, underline, affordance, depth, label, or placement.
- Avoid reusing one icon for different meanings or using similar icons for distinct actions.

## Onboarding and Overlays

- Avoid tutorial chains that users must memorize before acting.
- Prefer contextual pull revelations that appear when the user is engaged with the relevant task.
- Make overlays dismissible and retrievable later.
- Use coach marks for one unfamiliar interaction at a time, not to annotate an entire screen.
- Do not teach obvious standard controls; use help for novel, complex, or risky interactions.

## Evidence

Look for clear selected states, readable labels, visible affordances, stateful disclosure, keyboard-accessible tooltips, labeled icons, contextual tips, retrievable tutorials, and progressive disclosure tied to user action.

## Failure Patterns

- Tabs hide content users need to compare.
- A tab behaves like a link or opens a different site.
- Accordions make users click through most sections to understand the page.
- Tooltip content is required to complete the task.
- Icon-only navigation depends on undiscoverable hover labels.
- Onboarding overlays interrupt urgent tasks or cannot be found again.
