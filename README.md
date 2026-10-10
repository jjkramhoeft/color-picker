# color-picker

An interactive SVG color picker built from hexagons, originally written in June 2004.

- Hover over (or click) a hexagon in the left triangle to choose a hue; click to lock it.
- The right triangle then shows that hue blended toward black and white; hover or click to pick a shade.
- `--` / `++` change the granularity (number of hexagons).

Open `index.html` (or `color.svg` directly) in a browser. The SVG must be viewed directly or
embedded with `<object>`/`<iframe>`; scripts do not run when an SVG is loaded via `<img>`.

## 2026 update

The original script targeted the Adobe SVG Viewer plugin and no longer worked in modern browsers.
Fixes: SVG elements are created with `createElementNS` (plain `createElement` produced
non-SVG elements that never render), `evt.getTarget` → `evt.target`, `textNode.setData()` →
`textNode.data =`, the XML encoding declaration now matches the UTF-8 file, the minimum size is
clamped to avoid a divide-by-zero, and the SVG scales to its container.
