# MGR Geometry Pack

**Status:** Recommended default icon/decal pack for the Graphic Realism Design System.  
**Location:** `icons/mgr-geometry/`  
**Assets:** 29 SVG files.

This is the system’s **primary visual-symbol layer** for agent consoles, personal dashboards, PWA shells, slides and graphic compositions. Its geometric, radial, grid, directional and signal-based language is aligned with the `personal-os` reference implementation.

## Agent rule

> Use **MGR Geometry Pack first** for visual identity, navigation cues, section markers, telemetry, objectives, empty states, dashboard panels and slides.  
> Use Phosphor Bold / Tabler only as a **utility fallback** when a conventional control icon is absent here (for example: trash, edit, copy, calendar, file).

Do not mix three visual languages in the same component. If an MGR icon is used as a panel mark, keep nearby icons from MGR too; use fallback icons only for small secondary actions.

## Use modes

| Mode | Use | Typical size | Example assets |
|---|---|---:|---|
| **Mark** | Section/faction/system identity | 32–96 px | `cube-grid`, `globe-grid`, `atom` |
| **Navigation** | Direction, routing, view changes | 16–32 px | `arrow-*`, `arrows-*`, `navigation` |
| **Telemetry** | Data, scope, state, coordinates | 16–40 px | `line-circles-*`, `bars`, `circle-grid` |
| **Objective** | Focus, selection, target/action | 20–64 px | `crosshair-square`, `diamond-*`, `triangle-arrows` |
| **Signal** | Attention, activation, warning | 20–64 px | `lightning-bolts`, `alert-circle`, `sun-rays`, `star-8-circle` |
| **Decal** | Edge chrome/background motif | 8–160 px | `zigzag-band`, `interwoven`, `radial-square` |

## Color and placement

- SVG must inherit `currentColor` whenever its source supports it; otherwise preserve source treatment and wrap it in a themed container.
- Default: muted ink for structural marks; cyan for data/link; volt for action/ready; signal red for alert only.
- One dominant mark per panel/slide. Do not scatter decorative symbols randomly.
- Background/decal opacity: **4–8%**; active mark: 100%; disabled: 35–45%.
- Place marks on the panel edge, title block, card corner, status strip or empty state—not in the middle of a dense data table.
- Retain source `viewBox`; do not rasterize SVG or apply arbitrary stroke normalization to this pack.

## Asset catalog

See [`manifest.json`](./manifest.json) for a machine-readable catalog and [`preview.md`](./preview.md) for Markdown previews.

## License / provenance

Record the exact origin and applicable license in `third_party/NOTICE.md` before redistributing or publishing this pack outside the current project. This repository documents usage rules; it does not alter source-asset licenses.
