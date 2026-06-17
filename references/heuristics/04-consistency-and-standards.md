# H4 Consistency and Standards

Use when the UI includes new components, routes, navigation, icons, copy, menus, tables, forms, modals, keyboard behavior, platform conventions, domain conventions, omnichannel touchpoints, or design-system additions.

## Check

- Reuse established product components and interaction patterns.
- Use one term for one concept across the product.
- Follow web, platform, ecosystem, and domain conventions unless there is a deliberate user benefit to diverge.
- Keep action placement, icon meaning, validation style, and keyboard behavior predictable.
- Prefer local design-system patterns, tokens, components, and usage guidance over one-off variants.
- Preserve learned behavior across a product family: similar tasks should work similarly across products, pages, and channels.
- Reduce extraneous cognitive load by building on existing mental models instead of forcing users to learn custom mechanics.
- Keep learnability and efficiency in balance: preserve obvious standard paths for novices and add accelerators without replacing them.
- Keep core workflows, data, tone, and visual identity consistent across web, app, email, support, and offline touchpoints.

## Layers

- Internal consistency: same component, term, icon, placement, shortcut, validation pattern, and state behavior within the product.
- External consistency: standard web, OS, accessibility, ecommerce, form, and domain conventions users bring from other products.
- Cross-product consistency: shared patterns across a suite or brand family while allowing context-specific task details.
- Omnichannel consistency: same core functionality, current customer data, terminology, tone, and visual story across channels.
- Design-system consistency: use documented components, examples, checklists, tokens, templates, and code rather than local clones.

## Breaking Conventions

- Break a standard only when user research or task evidence shows the convention is failing this audience.
- Require a concrete benefit: fewer errors, faster expert work, better accessibility, clearer domain fit, or materially lower effort.
- Do not break conventions to be clever, branded, novel, or visually distinct.
- If divergence is necessary, make the new pattern self-evident, label it clearly, and apply it consistently everywhere it appears.
- Test icons and unfamiliar patterns at realistic sizes and contexts; visual consistency must not make distinct actions hard to tell apart.

## Governance

- Add or change design-system patterns only when reuse is likely; otherwise compose existing primitives.
- Include examples, usage rules, accessibility notes, and do/don't guidance for new reusable patterns.
- Review cross-team changes for standards drift, especially rarely used states and edge-case components.
- Treat recurring one-off variants as UX debt unless they encode a validated contextual difference.

## Evidence

Look for shared components, stable button hierarchy, consistent table controls, predictable icon labels, same wording for same states, familiar platform shortcuts, standard utility navigation, consistent field formatting, matching channel data, design-system references, and documented exceptions.

## Failure Patterns

- "Save", "Apply", "Update", and "Done" mean the same thing in nearby contexts.
- A common icon is repurposed for an uncommon meaning.
- A component behaves differently on one page without explanation.
- A custom pattern replaces an industry convention with no user benefit.
- Navigation, search, account, cart, or homepage links appear in unexpected places.
- Forms ask for standard data in nonstandard formats or vary required-field/validation behavior by page.
- Button order changes across modals, forms, or wizard steps.
- A branded term replaces a standard term users already know.
- Visual consistency makes distinct products, actions, or icons too similar to recognize.
- A flow, price, status, customer record, or policy differs across channels with no explanation.
- A design-system component is forked locally instead of extended through documented rules.
