# Design Rules — Graphic Realism (v1.1)

## 1. Product baseline

Before visual work, define:

- Primary user task and the single primary action for this view.
- Required states: loading, empty, working, ready, warning, error, offline.
- Content type: UI controls, telemetry, Markdown, code, table, media.
- Responsive behavior: desktop, compact, mobile.

A design that has no state model is not an agent-native Graphic Realism screen.

## 2. Three-layer rule

| Layer | Purpose | Constraints |
|---|---|---|
| Base | Content, data, controls, typography | Must work by itself |
| Chrome | Borders, labels, panels, corner cuts, MGR marks | Supports hierarchy and scanning |
| FX | Hatch, grid, noise, scan, motion | Optional; max ~8% background opacity |

Never put required text or a primary control only in FX.

## 3. Color

### Surfaces
| Token | Hex | Use |
|---|---|---|
| `--mgr-bg-void` | `#0B0C0E` | App canvas |
| `--mgr-bg-base` | `#12141A` | Shell / navigation |
| `--mgr-bg-panel` | `#1A1D24` | Cards / panels |
| `--mgr-bg-elevated` | `#242832` | Active/elevated surface |
| `--mgr-bg-white` | `#E8EAEF` | Light panel / content contrast |

### State map
| State | Token | Default MGR mark |
|---|---|---|
| Ready | `--mgr-state-ready` | `sun-rays`, `diamond-checker` |
| Working | `--mgr-state-working` | `atom`, `bars` |
| Queued | `--mgr-state-queued` | `line-circles-v` |
| Attention | `--mgr-state-attention` | `triangle-arrows` |
| Error | `--mgr-state-error` | `alert-circle` |
| Offline | `--mgr-state-offline` | muted `globe` |

Rules:

1. Use maximum two accents per view, beyond semantic state reinforcement.
2. Color encodes function, never ornament alone.
3. Pair every state color with a text label and, where helpful, shape/icon.
4. WCAG AA minimum; critical HUD/status text should prefer AAA.

## 4. Typography

```text
UI:      Inter / IBM Plex Sans / system-ui
Display: Space Grotesk / Chakra Petch / DIN Condensed
Mono:    IBM Plex Mono / JetBrains Mono
```

| Role | Size | Weight | Case |
|---|---|---|---|
| Display | 28–40 | 700 | Title/CAPS |
| Title | 20–28 | 600–700 | Title |
| Body / Markdown | 14–16 | 400–500 | Sentence |
| Label | 11–12 | 600 | ALL CAPS + tracking 0.08em |
| Data | 12–14 mono | 500 | as-is |

Markdown and code must have a dedicated readable surface. Never use display type for long responses.

## 5. Shell and responsive behavior

Recommended shell: topbar + rail + main + statusbar. Use `components/shell.css`.

| Width | Layout |
|---|---|
| ≥1200px | Rail + 12-column workspace |
| 768–1199px | Icon rail + compact grid |
| <768px | Bottom/overlay nav + one-column main |

- Touch target: ≥44px.
- Current task/action must stay visible on mobile.
- Support offline/sync/connection status in app-shell products.

## 6. Shape and materials

- Grid base: 8px, 4px micro.
- Radius: 0 / 2 / 4 / 8 max; pill only for compact state chips.
- Border: 1px default, 2px strong controls.
- Corner cut: use `clip-path` + inset shadow; do not leave a torn border.
- Pick 1–2 materials per component: flat fill, hairline, accent bar, MGR mark, hazard strip, mono data strip.

## 7. MGR Geometry Pack

Primary pack: [`icons/mgr-geometry/`](./icons/mgr-geometry/).

Use it for the system’s visual vocabulary before utility libraries:

| Need | First choice |
|---|---|
| Workspace/system | `cube-grid` |
| AI/model | `atom` |
| Network/integration | `globe-grid`, `interwoven` |
| Focus/target | `crosshair-square` |
| Verification | `diamond-checker` |
| Timeline/queue | `line-circles-v`, `bars` |
| Activation | `lightning-bolts`, `sun-rays` |
| Error | `alert-circle` |
| Dividers/chrome | `zigzag-band`, `radial-square` |

- One dominant mark per panel/slide.
- Data/mark color: cyan; action/ready: volt; alert: signal; structure: muted.
- Background mark opacity: 4–8%.
- Use conventional utility icons from Phosphor/Tabler only when MGR lacks the semantic control.

## 8. Motion and FX

- Fast 120ms · UI 180ms · Panel 280ms.
- Enter: fade + 8–12px slide.
- Hover: border/accent change, not big scale.
- FX opacity: grid ≤5%, hatch ≤6%, noise ≤3%, max general background decoration ≤8%.
- Honor `prefers-reduced-motion`.
- Never place moving/animated FX behind code, text inputs or critical telemetry.

## 9. Agent components

Use `components/agent-console.css` for:

- Presence chip with named state
- Task/queue rows
- Telemetry grid
- Markdown surface
- Low-opacity panel mark

Primary agent view should answer in 1–2 seconds:

1. What is the agent doing now?
2. Is user action required?
3. What is the next useful action?

## 10. A11y and IP

- Visible 2px focus ring.
- Labels for icon-only controls.
- Color is never the only state signal.
- Respect reduced motion.
- Create original work; do not copy Bungie/Marathon/Kurppa Hosk assets, logos or UI.
- Verify source licenses before distributing assets from `icons/mgr-geometry/`.
