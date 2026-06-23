# Review Modes

Use this helper to choose report depth, tone, and structure after the relevant heuristic and context helpers are loaded.

## Depth Modes

Choose depth from the user's prompt:

- High-impact only: report only issues likely to cause blocked completion, wrong decisions, accessibility failure, repeated effort, or loss of trust. Skip minor polish and obvious strengths.
- Detailed review: check the whole visible surface, including consistency, hierarchy, accessibility, copy, controls, missing states, and edge cases. Still prioritize findings instead of dumping everything in screen order.
- Balanced review: default when the user asks for general feedback. Include highest-impact fixes first, then meaningful strengths worth preserving.
- Positive-only review: include only what works and what to preserve.
- Issues-only review: include only friction, risk, confusion, missing states, or likely failure paths.
- Brainstorming guardrails: use when another ideation/design skill is leading, or when the user is exploring a feature before there is a UI artifact.
- Implementation guidance: turn heuristics into concrete component, state, copy, accessibility, and interaction requirements for coding.
- Formal heuristic evaluation: organize by H1-H10 only when explicitly requested.

If the prompt does not specify depth, default to balanced review grouped by impact, with high-impact findings first.

## Impact Labels

Use plain impact labels instead of product-process shorthand:

- High impact: likely to block completion, cause wrong decisions, create accessibility failure, hide critical state, cause data loss, or damage trust.
- Medium impact: creates repeated effort, slows scanning, causes hesitation, weakens confidence, or makes common tasks less efficient.
- Low impact: polish, minor clarity, or consistency improvements that do not materially affect task completion.

When a report includes multiple impact levels, group findings under `High impact`, `Medium impact`, and `Low impact` headings. Skip empty groups. Do not repeat the impact label inside each finding title.

Do not invent findings to make the report feel useful. If the reviewed UI has no material issues, say so plainly and include only meaningful strengths, verification gaps, or optional polish under clearly labeled sections.

## Shared Finding Shape

```text
N. Issue title
   Why it matters: impact on completion, decisions, accessibility, effort, or trust.
   Fix: concrete UI, copy, layout, state, or interaction change, with a short example when it helps.
   Evidence: what is visible (include for live/Chrome audits or when a claim needs grounding).
```

## Shared Report Template

Skip empty groups.

```text
Quick read:
One sentence naming the screen, the likely task, and the biggest UX risk.

High impact:
1. <finding>

Medium impact:
1. <finding>

Low impact:
1. <finding>

What's working:
- Meaningful strengths worth preserving. Skip obvious praise.

Unseen states:
- Loading, empty, no results, filtered, failed request, disabled/permission, mobile, hover/focus, keyboard, success.

Heuristics used:
H# list only, no long explanation unless requested.
```

## Mode Matrix

| Mode (when to use) | Impact tiers | What's working | Closing section | Length |
| --- | --- | --- | --- | --- |
| Balanced - default; screenshots, Chrome audits, general "give feedback" | High, Medium; Low only if notable | yes | `Unseen states` | medium |
| High-impact only - "top fixes", "priority", "quick audit" | High only | no | `Not covered:` - medium/low items, heuristic scoring, and unseen states unless they affect a top risk | 3-5 findings; if none, write `No high-impact issues visible in this state` and stop |
| Detailed - "check everything", "comprehensive audit" | High, Medium, Low | yes | `Unseen states and tests` - state to verify plus why | thorough, never repeat a finding across sections |
| Issues-only - "what's bad/broken/risky" | High, Medium | no compliments | `Open checks` - states not visible | medium |

If there are no material issues, use this shorter structure instead of padding a mode with low-value critique:

```text
Quick read:
No material usability issues are visible in this screenshot/page state. State the main task and any important screenshot-only caveat.

What's working:
- Meaningful strength worth preserving.

Optional polish:
- Minor improvement only if it is genuinely useful; omit when there is none.

Open checks:
- Live states or accessibility behaviors that cannot be verified from the screenshot/page state.

Heuristics used:
H# list only, no long explanation unless requested.
```

## Positive-Only Review

Use when the user asks what is good or what to preserve.

```text
Strengths to keep:
- What works, why it helps the task, and what implementation detail should be preserved.
```

Do not dilute positive-only mode with critique unless there is a serious risk the user must know.

## Brainstorming Guardrails

Use when the user is planning a feature, comparing concepts, or using this skill alongside another brainstorming/design skill. Do not produce a full audit unless requested.

```text
UX framing:
- User, job-to-be-done, context, and highest-cost failure mode.

Directions to explore:
- Concept direction shaped by UX constraints.

UX guardrails:
- Concrete requirement the concepts should preserve.

Concept risks:
- Material confusion, error, delay, accessibility, trust, or recovery risk. Omit if none are visible at this stage.

Decision questions:
- Product or technical decision that would change the UX recommendation.

Implementation constraints:
- Concrete behavior, state, copy, accessibility, and interaction requirements for the build.
```

When comparing options:

```text
Option A: short name
UX read: benefit, risk, and best-fit condition.

Option B: short name
UX read: benefit, risk, and best-fit condition.

Recommendation:
Pick only when the available evidence supports it; otherwise name the decision criteria.
```

Keep this mode provisional. If an idea is sound at the current fidelity, say so and list only open checks or decisions.

## Implementation Guidance

Use when the user is coding or asks to keep heuristics in mind while implementing.

```text
UX constraints:
- User-facing behavior, copy, state, accessibility, and interaction requirements to preserve.

Implementation checklist:
- Concrete component/state requirements.

UX coverage: one compact sentence summarizing the heuristics covered and any remaining risk.
```

## Formal Heuristic Evaluation

Use only when the user explicitly asks for a heuristic evaluation.

```text
H# Heuristic Name
Finding: issue or decision.
Why it matters: user confusion, error, delay, or recovery risk.
Fix: concrete UI, copy, state, or interaction change.
```

Only include heuristics with meaningful evidence.

## Output Hygiene

- State each issue once.
- Do not force a finding. A clean review with no material issues is a valid outcome.
- Lead with the action or risk, not the heuristic.
- Put heuristic tags in a footer or compact field unless the user requested formal heuristic evaluation.
- Do not expose loaded helper files unless the user is testing the skill or asks for process details.
- Mark screenshot-only inferences as needing live verification, especially contrast, clickability, focus, keyboard behavior, disabled states, and hover-only interactions.
- Separate optional polish from real issues so developers, CTOs, and customers can tell what matters.
- Avoid "next steps" lists that merely repeat the findings.
