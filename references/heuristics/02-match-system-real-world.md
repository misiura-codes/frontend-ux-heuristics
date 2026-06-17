# H2 Match Between the System and the Real World

Use when the UI includes copy, field labels, CTAs, icons, product descriptions, information architecture, domain data, dates, units, sorting, control layouts, gestures, mental models, metaphors, or offline-to-digital workflow mapping.

## Check

- Use the user's terms, not internal implementation names.
- Prefer user benefits and outcomes over feature names, branded terms, or implementation details.
- Present fields and steps in the order users naturally expect.
- Use familiar domain examples, units, date formats, and status names.
- Expand acronyms and explain why they matter before relying on abbreviations.
- Make icon meanings obvious or pair icons with labels.
- Align controls with outcomes through natural mapping.
- Place contextual information where users need it in the flow, not in unrelated upfront notices or hidden fine print.
- Match the user's likely mental model of the real-world object, activity, or process without forcing decorative skeuomorphism.
- Keep stimulus and response compatible: the control's position, label, gesture, or movement should correspond to the expected result.

## Language

- Write for the person doing the task, not for the company, system, or feature team.
- Use conversational `you`/`we` framing when it clarifies responsibilities or makes policy copy easier to understand.
- Avoid jargon, business speak, legalese, and domain shorthand unless the target user demonstrably uses it.
- If expert terms are necessary for search or recognition, pair them with plain-language benefits.
- Do not assume the buyer, admin, assistant, or researcher has the same expertise as the final practitioner.

## Natural Mapping

- Put controls where their effects make spatial or procedural sense.
- Use spatial similarity when controls affect visible objects, regions, panels, monitors, seats, products, or steps.
- Use culturally familiar direction, quantity, time, and priority metaphors carefully, especially for localized products.
- Use conceptual similarity when metaphors clarify effects: up means more, down means less, green means go, red means stop, larger means more important.
- Use behavioral similarity when gestures or motion mirror how users would naturally act on the object.
- Make interface objects behave like the real-world or digital convention they resemble.
- Order content by the user's decision process rather than by database shape, org chart, or marketing priority.
- Avoid complex hidden gestures unless their mapping to the goal is obvious, discoverable, and supported by visible alternatives.

## Evidence

Look for domain language from research/support/sales, search-query terms, plain-language definitions, expanded acronyms, localized formats, labels that describe outcomes, familiar metaphors, control layouts that mirror affected objects, gestures that resemble real actions, and grouped fields that match the user's task.

## Failure Patterns

- Backend entity names leak into the UI.
- Users must decode abbreviations before acting.
- Feature names appear without benefits or outcomes.
- Copy speaks about "customers" or the company instead of directly helping the current reader.
- Controls map poorly to the item they affect.
- Information is sorted by system structure rather than task logic.
- Critical contextual guidance appears too early, too late, or outside the step where it matters.
- Icons or visual metaphors resemble real objects but do not behave like users expect.
- Control direction is reversed, arbitrary, or disconnected from the visible result.
- Gesture shortcuts require users to memorize unnatural multi-finger or hidden actions.
- Visual arrangement suggests one relationship, but the system response follows another.
