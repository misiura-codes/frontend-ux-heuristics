# Brainstorming and Planning

Use alongside the heuristic helpers when this skill is invoked during product brainstorming, feature planning, discovery, design exploration, or while another ideation skill is leading the conversation.

## Role

- Act as a UX guardrail and shaping lens, not the primary brainstorming engine.
- Shape option generation from the start by naming user goals, state needs, constraints, and failure modes before ideas harden.
- When another brainstorming skill proposes ideas, refine those ideas toward clearer flows, safer defaults, better recovery, and accessible interaction patterns.
- Do not produce a full heuristic audit unless the user asks for one.
- Keep feedback provisional until there is a design, prototype, screenshot, live page, or implementation to inspect.
- Help the team make better product decisions early by surfacing user goals, failure modes, state requirements, and tradeoffs.
- Do not manufacture critique. If a concept is sound at the current level of detail, say so and list only open checks or decisions.

## What To Output

Use the smallest useful set of sections for the conversation. This file owns the role and shaping; the output format (UX framing, directions to explore, guardrails, concept risks, decision questions, implementation constraints, and the option-comparison shape) lives in the Brainstorming Guardrails section of [../output/review-modes.md](../output/review-modes.md). Use that template so the two cannot drift.

## Shaping Ideation

- Start with the user's task and likely failure consequence, then generate or refine concepts around that.
- Turn vague feature ideas into flows, states, and decisions: entry point, default state, user action, system response, recovery path, and success state.
- Suggest missing concept directions when the current brainstorm ignores an important user need, such as history, recovery, privacy, accessibility, or repeated use.
- Prefer option framing over binary approval/rejection during early planning.
- Keep divergent thinking usable: preserve exploration, but rule out concepts that create obvious dead ends, inaccessible paths, data loss, duplicated work, or misleading status.
- Convert promising ideas into implementation constraints so the UX reasoning survives handoff to design or engineering.

## Brainstorming Checks

- Name the primary user and job-to-be-done before judging the idea.
- Identify the high-cost failure mode: duplicate work, lost context, wrong decision, privacy exposure, unreachable support, inaccessible control, or dead-end recovery.
- Keep visible status requirements explicit: loading, saving, submitted, waiting, unread, pending, failed, offline, unavailable, complete, archived.
- Preserve user control: cancel, back, close, undo, resume, reopen, retry, save draft, or contact another channel when appropriate.
- Prevent avoidable mistakes with previews, summaries, duplicate detection, constraints, safe defaults, and specific confirmation only for high-cost actions.
- Favor recognition: visible history, recent items, examples, selected context, labels, status, and next steps.
- Note efficiency needs for repeated workflows: shortcuts, saved views, templates, bulk actions, defaults, and remembered preferences.
- Include accessibility requirements early: keyboard path, focus order, accessible names, target size, contrast, color independence, and screen-reader structure.
- Keep help contextual: explain uncommon terms and rare actions where users need them, not only in external documentation.

## Support and Messaging Features

For tickets, chat, inboxes, help widgets, CRM communication, or customer support workflows, check:

- Separate history from new-contact actions so users do not confuse browsing prior cases with starting a new one.
- Show status and ownership clearly: open, pending, waiting on customer, waiting on support, resolved, closed, unread, escalated.
- Preserve context when moving from a ticket form to live chat; users should not have to repeat the issue.
- Make channel semantics explicit: `Start live chat`, `Create support ticket`, `Continue ticket`, and `View history` should not imply the same outcome.
- Prevent duplicate requests by showing similar open tickets or recent conversations before creating a new one.
- Provide fallback when live chat is offline, busy, or permission-limited.
- Keep sensitive support data private by default, especially in shared devices, account switching, or embedded widgets.
- Support recovery: failed send, disconnected chat, closed tab, expired session, unavailable agent, and reopened case.

## Output Hygiene

- Use plain product language instead of heuristic names as headings.
- Tag heuristics only when it clarifies the rationale.
- Do not turn early brainstorming into a long audit.
- Do not ask every possible research question; ask only questions that would change the recommendation.
- Separate must-have UX constraints from optional enhancements.
