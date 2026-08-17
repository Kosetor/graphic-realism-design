# Agent scenario: UI

## Goal

Build interfaces—dashboards, panels, HUDs, settings, agent consoles—in product-ready Graphic Realism.

For Personal OS / PWA / agent dashboards, use the deeper scenario: [`personal-os.md`](./personal-os.md).

## Read first

`SKILL.md` → `tokens/tokens.css` → `rules.md` → this file → `icons/mgr-geometry/manifest.json`.

For app shells also read: `tokens/personal-os.css`, `components/shell.css`, `components/agent-console.css`.

## Layout grammar

```text
┌ void/base canvas ──────────────────────────────────────────────────────┐
│ [SECTION LABEL]                    AGENT STATE · meta · primary CTA     │
│ ┌ panel: MGR mark + title + body ┐ ┌ panel: telemetry / queue ───────┐ │
│ │  one mark, low-opacity chrome  │ │ READY · 42ms · 62% · status      │ │
│ │  meaningful content             │ │ [one contextual action]          │ │
│ └─────────────────────────────────┘ └─────────────────────────────────┘ │
│ status strip / hazard only if semantically meaningful                    │
└────────────────────────────────────────────────────────────────────────┘
```

## Build order

1. Define intent, primary task and required states.
2. Create Base: canvas, readable content, controls, data and Markdown/code regions.
3. Add Chrome: 1px panels, CAPS labels, status strip, one MGR Geometry mark where it improves scanning.
4. Add functional color: primary action (usually volt) + state reinforcement.
5. Add FX only if it remains useful at 0% opacity.
6. Define compact/mobile behavior and reduced-motion behavior.

## MGR Geometry selection

| UI need | First choice |
|---|---|
| System/workspace | `ic-cube-grid.svg` |
| AI/model/state | `ic-atom.svg`, `ic-sun-rays.svg` |
| Link/network | `ic-globe-grid.svg`, `ic-interwoven.svg` |
| Current target | `ic-crosshair-square.svg` |
| Success/verify | `ic-diamond-checker.svg` |
| Queue/history | `ic-line-circles-v.svg`, `ic-bars.svg` |
| Run/activate | `ic-lightning-bolts.svg` |
| Error | `ic-alert-circle.svg` |
| Divider | `ic-zigzag-band.svg` |

Paths are relative to `icons/mgr-geometry/`.

## Component rules

### Panel

- Flat dark/light surface; 1px line; optional 4px accent bar.
- One mark at title scale (32–48px) or background scale (48–104px at 4–8% opacity), not both by default.
- Preserve long Markdown/code readability.

### State presence

```html
<span class="mgr-agent-presence mgr-agent-presence--working">
  <span class="mgr-agent-presence__dot" aria-hidden="true"></span>
  Working
</span>
```

Use explicit label + color + diamond dot.

### Button

- Primary: solid volt, CAPS, clear verb.
- Secondary: outline.
- One primary CTA per view.
- No gradients and no oversized rounded corners.

### Telemetry

- Mono values; CAPS label; tabular numerals.
- Cyan = data/link, not every number.
- Use `bars` / `line-circles-*` as a contextual data mark, not decoration.

## Output

Intent → Shell map (if applicable) → Tokens/state map → MGR assets → ASCII wire → code → responsive → a11y → sources.

## Anti-patterns

- Screenshot-only UI with no empty/error/offline states.
- Decorative MGR symbols scattered across each card.
- FX/grid/noise behind text, code or form fields.
- Multiple competing primary CTAs.
- Using MGR symbols plus a different decorative icon pack in the same focal panel.
