# DESIGN — Graphic Realism

## Definition

**Graphic Realism** is a visual language where:

1. **Graphic language:** a reduced universal system of geometry, expressive functional color, limited materials and poster-like scanability.
2. **Realism:** credible proportions, implied function, modularity and product-grade usability.

It creates interfaces that feel like a **branded scientific utility / sport-tech operating environment**, not generic cyberpunk and not a static concept render.

## Reference implementation

[`Kosetor/personal-os`](https://github.com/Kosetor/personal-os) is the current **reference implementation** of this system in a working product context.

It establishes additional expectations:

- A real app/PWA shell, not an isolated card.
- Config-driven theming and behavior rather than scattered visual values.
- Agent presence, queues, activity and connection states as first-class UI.
- Markdown-safe content surfaces for agent responses, code and data.
- A controlled FX layer that is subordinate to function and readable without animation.
- Responsive, touch-friendly and reduced-motion behavior.

Read [`agents/personal-os.md`](./agents/personal-os.md) when designing agent-native dashboards or Personal OS applications.

## Three visual layers

```text
Base    → typography, content, controls, data, layout
Chrome  → panels, hairlines, labels, corner cuts, MGR geometry marks
FX      → optional hatch/grid/noise/scan; never carries required information
```

A screen must remain understandable with Chrome and FX removed.

## Icon language

**MGR Geometry Pack** at [`icons/mgr-geometry/`](./icons/mgr-geometry/) is the **recommended default visual icon/decal pack**.

- MGR Geometry first: identity, navigation motifs, telemetry, objectives, signals, decorative chrome.
- Phosphor Bold / Tabler / Lucide second: small conventional utility controls that do not exist in MGR.
- Never treat the pack as wallpaper: one dominant geometric mark per panel/slide is normally enough.

## Inspiration (do not copy)

- Graphic Realism art direction (Marathon / Joseph Cross) — as a term and a design principle
- The Designers Republic / Wipeout — branding and maximalist minimalism
- Mirror’s Edge — white futurism and color-as-navigation
- Metal Gear Solid 2 — tactical chrome and codex hierarchy
- F1 telemetry and athletic technical equipment
- Industrial wayfinding, warning tape and scaffolding

## Pillars

### 1. Product-first composition

The design has to survive real use: loading, errors, long Markdown, empty states, offline mode, narrow screens and frequent actions.

### 2. Limited materials

Flat panel · hairline stroke · solid accent bar · MGR geometry mark · hazard strip · hard offset shadow (optional) · mono data strip.

### 3. Color is function

Signal = attention/error. Volt = ready/action. Cyan = data/link. Amber = attention/warning.

Use one primary accent and, if needed, one semantic status accent per view.

### 4. Typography discipline

One UI face + mono for data; display face only for titles/hero moments. CAPS labels with tracking. No fontslop.

### 5. Agent-native state language

State must be communicated through a **label + color + mark/shape**. Never through color alone.

### 6. Geometric iconography

Prefer MGR Geometry Pack. Use its marks deliberately as system vocabulary: cube = workspace, atom = model/core, globe = integration/world, crosshair = objective, diamond = state.

### 7. Modularity and config

Treat components as blocks and visual decisions as tokens/configuration. One source of truth for color, density, motion and states.

### 8. Hierarchy over decoration

If a mark, FX or animation does not help a user scan the product in 1–2 seconds, reduce or remove it.

## Emotional tone

- Confident, technical, athletic, industrial
- Cold neutral base with functional high-energy accent
- Capable equipment, not magic
- Clean operational future—not a neon alley-cyberpunk scene

## Anti-goals

- Photo-real skeuomorphism
- Soft candy UI / large continuous radius
- Rainbow gradients
- Decorative glitch behind text/code
- Copying Bungie/Marathon visual assets or UI
- Screens that work only as screenshots
