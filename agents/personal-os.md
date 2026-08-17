# Agent scenario: Personal OS / Agent-native shell

`personal-os` is the **reference implementation** for applying Graphic Realism to a real, maintainable product UI—not merely to a concept screen.

Reference repository: https://github.com/Kosetor/personal-os

## When to use this scenario

- Personal dashboard / command center
- AI agent control panel (Hermes, Agent Zero, OpenWebUI extensions)
- PWA / local-first workspace
- Knowledge, project, task, integration or memory console
- Multi-pane app with navigation, activity and command layer

Read in this order:

1. `SKILL.md`
2. `tokens/tokens.css`
3. `tokens/personal-os.css`
4. `components/shell.css`
5. `components/agent-console.css`
6. `icons/mgr-geometry/manifest.json`
7. `agents/ui.md`

## Architecture: three visual layers

```text
Layer 1 — Base
  canvas, typography, data, controls, content

Layer 2 — Chrome
  panels, borders, corner cuts, labels, status bars, MGR geometry marks

Layer 3 — FX
  optional scan/hatch/noise/motion effects; must not obscure content
```

Rule: Base is always useful without Chrome/FX. Chrome improves scanability. FX is optional and restrained.

## Shell anatomy

```text
┌ app-shell ──────────────────────────────────────────────────────────────┐
│ topbar: brand/section · global status · utilities · agent presence       │
├───────────────┬─────────────────────────────────────────────────────────┤
│ rail/nav      │ main workspace                                           │
│ - views       │ ┌ section header: label / title / meta / primary CTA ┐  │
│ - queues      │ ├─────────────────────────────────────────────────────┤  │
│ - shortcuts   │ │ panels: telemetry · task queue · memory · activity │  │
│               │ │ one MGR mark per panel as needed                    │  │
│               │ └─────────────────────────────────────────────────────┘  │
├───────────────┴─────────────────────────────────────────────────────────┤
│ status bar: connection · model · queue · sync · build                    │
└─────────────────────────────────────────────────────────────────────────┘
```

### Responsive collapse

| Width | Behavior |
|---|---|
| ≥ 1200 px | Persistent rail + multi-panel workspace |
| 768–1199 px | Compact rail; 2-column content where meaningful |
| < 768 px | Bottom/overlay navigation; one-column cards; status condensed |

Never remove the current task/action just to preserve visual symmetry.

## Product rules learned from personal-os

1. **Config-driven** — themes, accents, agent state and integrations belong in config/tokens; do not scatter raw hex values.
2. **Agent presence is state** — show availability, thinking, queued, blocked, completed or offline with text + visual cue, not color alone.
3. **Action hierarchy** — one main action per view; contextual actions stay inside their panel.
4. **Markdown-safe content** — reserve a readable content surface for markdown, code and tables; never place decorative FX behind code.
5. **Progressive disclosure** — compact dashboard first; expand details on demand.
6. **PWA-ready** — provide connection/offline/sync states and tap targets ≥44px.
7. **Reduced motion** — honor `prefers-reduced-motion`; no ambient animation required to understand status.

## Recommended MGR mapping

| Shell function | Preferred MGR Geometry assets |
|---|---|
| System / workspace | `cube-grid`, `circle-grid`, `radial-square` |
| Agent core / model | `atom`, `sun-rays`, `lightning-bolts` |
| Integrations / web | `globe`, `globe-grid`, `interwoven` |
| Current objective | `crosshair-square`, `diamond`, `diamond-checker` |
| Queue / timeline | `line-circles-v`, `line-circles-h`, `bars` |
| Navigation / routing | `navigation`, `arrow-right-rect`, `arrows-both` |
| Warning / incident | `alert-circle`, `zigzag-band` |

## State language

| State | Text label | Color | Mark |
|---|---|---|---|
| Ready | READY | volt | `sun-rays` / `diamond-checker` |
| Working | WORKING | cyan | `atom` / `bars` |
| Queued | QUEUED | muted | `line-circles-v` |
| Attention | ACTION REQUIRED | amber | `triangle-arrows` |
| Error | BLOCKED / ERROR | signal | `alert-circle` |
| Offline | OFFLINE | faint | `globe` (muted) |

Always include the label. The mark/color is reinforcement, not the only signal.

## Agent output contract

When asked to create a Personal OS screen, return:

1. **Screen intent** and user task
2. **Shell map** (topbar/rail/main/status)
3. **Tokens** and state mapping
4. **MGR Geometry asset choices** with file paths
5. **Component markup / code**
6. **Responsive behavior**
7. **A11y and reduced-motion notes**

## Minimal prompt

```text
Create an agent-native Personal OS screen using Graphic Realism.
Reference: github.com/Kosetor/personal-os
Read: agents/personal-os.md, tokens/personal-os.css,
components/shell.css, components/agent-console.css,
icons/mgr-geometry/manifest.json.
Use MGR Geometry Pack as the primary icon language.
```
