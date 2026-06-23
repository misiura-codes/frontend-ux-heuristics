# Accessibility

Use this as one review lens for visual or interactive UI when evidence is available or the user asks. Accessibility failures block real users and are easy to miss in a screenshot, where low contrast or a missing focus state reads as normal. Treat WCAG 2.2 AA as the baseline.

## Check

- Contrast: body and UI text meet AA (4.5:1 for normal text, 3:1 for large text and meaningful icons). De-emphasize with size and weight, not faint gray.
- Color independence: never signal status, errors, selection, or required fields with color alone; add text, icon, shape, or position.
- Visible focus: every interactive element has a clear focus indicator, and focus order follows the visual/reading order.
- Keyboard: all actions are reachable and operable without a mouse; no hover-only affordances; no keyboard traps.
- Target size: interactive controls are at least 24x24 CSS px with adequate spacing between them.
- Names and roles: controls, icon buttons, and inputs have accessible names or labels; images carry alt text or are marked decorative.
- Motion: honor reduced-motion preferences; do not convey meaning through motion without a static equivalent.
- Structure: headings, landmarks, and lists are semantic, not simulated with styling alone.

## Evidence

Look for measured contrast ratios, redundant (non-color) status indicators, visible focus styles, logical tab order, labelled controls and inputs, alt text, adequate target sizes, and reduced-motion handling.

## Failure Patterns

- Low-contrast gray text used to de-emphasize until it becomes hard to read.
- Status or error conveyed by color only.
- Clickable elements with no visible focus state.
- Actions reachable only by hover or only by mouse.
- Icon buttons and inputs with no accessible name.
- Tap or click targets that are tiny or tightly packed.
- Animation or auto-advance with no reduced-motion fallback.
- Headings and structure faked with font size instead of semantic markup.
