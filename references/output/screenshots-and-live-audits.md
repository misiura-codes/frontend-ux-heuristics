# Screenshots And Live Audits

Use this helper when reviewing a real website or app through a browser, extension, screenshot, or captured page artifact.

## Live Page / Chrome Audit Scope

- State the evidence scope before findings: URL/page name when available, viewport size, device mode, and whether evidence is full page, visible viewport only, or multiple captured states.
- If the page is taller than one screen, do not imply the whole page was reviewed from one viewport.
- Prefer full-page screenshots when the tool can capture them cleanly and the page is not too tall to annotate readably.
- For long pages, capture and review logical viewports or sections such as `top`, `middle`, `bottom`, sticky header, open menu, modal, form error, and mobile state.
- If only one viewport is available, write `Scope: visible viewport only` and avoid findings about unseen content.
- Separate verified live evidence from inference: use `Verified live:` for DOM/computed-style/accessibility/keyboard evidence and `Needs live verification:` for anything not checked.
- Use live evidence to verify contrast, focus order, keyboard access, accessible names, target sizes, hover/focus/active states, disabled reasons, loading, empty, error, and success states when the extension exposes them.
- Do not require every state for every audit. Capture extra states only when they affect the user's task or a material finding.
- When browser/DOM evidence exposes element bounding boxes, prefer targeted element or region annotations over a giant full-page screenshot.
- Use full-page annotations only when the page-level context is necessary to understand the issue, such as hierarchy, navigation, repeated patterns, or scroll-position problems.
- For element-level findings, capture a padded crop around the element or region so developers can see enough neighboring context.
- Name targeted artifacts by finding number or region, such as `finding-01-submit-button-annotated.png` or `pricing-card-region-annotated.svg`.

## Long-Page Annotations

- Use one annotated full-page image only when markers remain readable.
- Otherwise create one annotated image per viewport, section, element, or interaction state, using names like `page-top-annotated.svg`, `page-form-error-annotated.svg`, `submit-button-focus-annotated.svg`, or `page-mobile-annotated.svg`.
- In the report, place each inline annotated image near the relevant findings or under an `Annotated screenshots:` section.
- Keep marker numbering unique across all images in the same report.
- Include a short scope caption for each annotated image, such as `Desktop top viewport, 1440x900` or `Primary CTA region, cropped with 48px padding`.

## Annotated Screenshot Add-On

Use when the user asks for marked screenshots, when spatial findings are hard to explain in text, or when the artifact will be shared with developers, executives, or customers.

- Create the text report first, then add a non-destructive annotated copy of the screenshot.
- Match annotation numbers exactly to report findings.
- Mark only material findings; do not add markers for optional polish or invented issues.
- Keep markers sparse enough that the original UI remains readable.
- Prefer raster output such as `*-annotated.png` when image editing is available.
- If raster editing is unavailable, create an SVG overlay such as `*-annotated.svg`; embed the source screenshot in the SVG when possible so the overlay is self-contained.
- Add an inline `Annotated screenshot:` image near the top of the report, then add an `Annotated markers:` key after the findings.
- If annotation is not possible, add a `Marked locations:` text section instead of pretending an image was generated.

