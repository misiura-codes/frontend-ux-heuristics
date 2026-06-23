# Report Assets

Use this helper when generating Markdown reports that may include screenshots, annotations, crops, exports, or other supporting files.

- If the report is text-only, a single Markdown file is acceptable.
- If the report includes any image or asset, create a folder named after the report and put `report.md` plus all assets inside it.
- Keep Markdown image links relative to the report folder.
- Keep all source images, annotated images, crops, and exported evidence with the report so the folder can be shared or zipped as one artifact.
- Use stable asset names instead of long one-off names inside the folder:
  - `source.png`
  - `annotated.svg` or `annotated.png`
  - `viewport-top.png`
  - `viewport-top-annotated.svg`
  - `viewport-middle.png`
  - `viewport-bottom.png`
  - `finding-01-submit-button.png`
  - `finding-01-submit-button-annotated.svg`
- For multiple screenshots, name by viewport, region, interaction state, or finding number.
- Avoid storing unrelated reports or shared assets in the same report folder.

Example:

```text
reports/
  dashboard-ux-review/
    report.md
    source.png
    annotated.svg
    finding-01-current-status.svg
    finding-02-contrast.svg
```

