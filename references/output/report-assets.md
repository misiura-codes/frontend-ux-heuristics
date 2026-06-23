# Report Assets

Use this helper when generating Markdown reports that may include screenshots, annotations, crops, exports, or other supporting files.

- If the report is text-only, a single Markdown file is acceptable.
- If the report includes any image or asset, create a folder named after the report and put `report.md` plus all assets inside it.
- Keep Markdown image links relative to the report folder.
- Keep all source images, annotated images, crops, and exported evidence with the report so the folder can be shared or zipped as one artifact.
- For annotated screenshots, `report.md` should embed the flattened PNG, not an SVG. SVG is allowed as an editable secondary asset only.
- Use stable asset names instead of long one-off names inside the folder:
  - `source.png`
  - `annotated.png` (flattened composite — markers on the screenshot; reference this from `report.md`)
  - `annotated.svg` (editable overlay; screenshot embedded as a base64 data URI, never an external path)
  - `viewport-top.png`
  - `viewport-top-annotated.png`
  - `viewport-top-annotated.svg` (optional editable backup)
  - `viewport-middle.png`
  - `viewport-bottom.png`
  - `finding-01-submit-button.png`
  - `finding-01-submit-button-annotated.png`
  - `finding-01-submit-button-annotated.svg` (optional editable backup)
- For multiple screenshots, name by viewport, region, interaction state, or finding number.
- Avoid storing unrelated reports or shared assets in the same report folder.

Example:

```text
reports/
  dashboard-ux-review/
    report.md
    source.png
    annotated.png
    annotated.svg
    finding-01-current-status-annotated.png
    finding-02-contrast-annotated.png
```
