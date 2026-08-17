---
name: graphic-realism-design
description: >
  Apply the Graphic Realism design system for product UI, Personal OS shells,
  agent consoles, slides and graphics. Use MGR Geometry Pack as the default
  visual icon/decal language.
version: 1.1.0
license: MIT
repository: https://github.com/Kosetor/graphic-realism-design
demo: https://kosetor.github.io/graphic-realism-design/
reference_implementation: https://github.com/Kosetor/personal-os
recommended_icon_pack: icons/mgr-geometry
---

# SKILL: Graphic Realism Design System

You apply **Graphic Realism (MGR)** as a product-ready visual system: strong geometric graphic language, engineering clarity and agent-native usability.

## Activate for

- UI / dashboard / PWA / settings / Personal OS / agent console
- AI agent queues, state, telemetry, Markdown/codex panels
- Slides, pitch decks, posters, thumbnails, graphics
- Icons, decals, backgrounds and brand marks (original work)
- Requests for Marathon-like / Graphic Realism / MGR aesthetics

## Required reading order

1. `SKILL.md`
2. `tokens/tokens.css`
3. `tokens/personal-os.css` for applications/shells
4. `rules.md`
5. Scenario:
   - generic UI → `agents/ui.md`
   - Personal OS / agent product → `agents/personal-os.md`
   - slides → `agents/slides.md`
   - graphics → `agents/graphics.md`
6. `components/shell.css` and `components/agent-console.css` when applicable
7. `icons/mgr-geometry/manifest.json`
8. Optional deep rules: `design-rules.md`, `DESIGN.md`

## Core rule

**Base → Chrome → FX**

- Base: content, controls, typography and data; must work alone.
- Chrome: panel borders, labels, corner cuts, status strips, MGR geometry.
- FX: optional hatch/grid/noise/motion; never contains required information.

## Tokens (minimum)

```text
Surfaces: void #0B0C0E | base #12141A | panel #1A1D24 | white #E8EAEF
Accents:  signal #FF3B4A | volt #C8F542 | cyan #3DE0FF | amber #FFB020
Type:     UI Inter | Display Space Grotesk | Mono IBM Plex Mono
Shape:    2–4px radius (8px cards max), 1px hairline, 2px strong control
Icon:     MGR Geometry Pack first; fallback Phosphor Bold / Tabler only for utility gaps
Motion:   120–280ms; respect reduced motion
```

## MGR Geometry Pack

Path: `icons/mgr-geometry/`  
Catalog: `icons/mgr-geometry/manifest.json`

Use it as the default identity layer:

| Intent | Preferred assets |
|---|---|
| Workspace/system | `cube-grid`, `circle-grid` |
| Agent/model | `atom`, `sun-rays`, `lightning-bolts` |
| Web/integrations | `globe`, `globe-grid`, `interwoven` |
| Focus/objective | `crosshair-square`, `diamond`, `diamond-checker` |
| Queue/telemetry | `bars`, `line-circles-v`, `line-circles-h` |
| Alert | `alert-circle`, `zigzag-band` |

One dominant mark per panel or slide. Structure=muted; data=cyan; action/ready=volt; error=signal.

## Agent-native product rules

- Model agent state with readable labels: READY, WORKING, QUEUED, ACTION REQUIRED, BLOCKED, OFFLINE.
- Pair every status color with label and mark/shape.
- One primary action per view.
- Preserve readable surfaces for Markdown, code and tables.
- Define empty/loading/error/offline states before polishing FX.
- Mobile: targets ≥44px; shell/nav collapses but current action remains accessible.

## Output contract

1. **Intent** — user task + screen purpose
2. **Shell map** — topbar/rail/main/status if app-like
3. **Tokens and state map**
4. **MGR Geometry asset choices** with paths
5. **Layout** — ASCII wireframe
6. **Code** — HTML/CSS or React/Vue/SVG
7. **Responsive behavior**
8. **A11y / reduced-motion notes**
9. **Sources** — repo paths and external licenses

## Hard restrictions

- Do not copy UI, assets, logos or faction marks from Bungie / Marathon / Kurppa Hosk.
- Do not use FX as a substitute for hierarchy.
- Do not mix unrelated icon languages in a focal component.
- Do not use `ic-q-logo.svg` without checking its origin/license and identity fit.
- Do not put critical status only in color or only in animation.

## One-shot prompt

```text
Apply Graphic Realism from github.com/Kosetor/graphic-realism-design.
For an app shell read: agents/personal-os.md, tokens/personal-os.css,
components/shell.css, components/agent-console.css.
Use icons/mgr-geometry/manifest.json as the primary icon language.
Task: <describe screen/product>.
Stack: HTML/CSS | React | Vue | SVG.
Return: intent, shell map, tokens/state map, MGR assets, code, responsive and a11y notes.
```
