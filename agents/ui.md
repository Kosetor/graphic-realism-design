# Agent scenario: UI

## Goal

Собрать интерфейс (dashboard, panel, HUD, settings, agent console) в Graphic Realism.

## Read first

`SKILL.md` → `tokens/tokens.css` → `rules.md` → this file → `components/utilities.css` → `icons/` + `decals/`

## Layout grammar

```
┌ void canvas ─────────────────────────────────────────┐
│  [LABEL]                              meta mono      │
│  ┌ panel ──────────────┐  ┌ panel ────────────────┐  │
│  │ accent│ title       │  │ telemetry grid        │  │
│  │ bar   │ body        │  │ 12.4  READY           │  │
│  │       │ [CTA]       │  │ ████░░ 62%            │  │
│  └─────────────────────┘  └───────────────────────┘  │
│  hazard strip (optional, 8–12px)                     │
└──────────────────────────────────────────────────────┘
```

## Build steps

1. Canvas = `--mgr-bg-void`
2. Panels = `--mgr-bg-panel` or light `--mgr-bg-white`
3. One accent language per view (volt OR signal primary)
4. Header labels CAPS xs muted
5. Numbers mono
6. Icons from `icons/outline` (default) / `solid` (active)
7. Decals: accent-bar, corner-registration, hazard only as thin chrome
8. Primary button: volt fill CAPS
9. Secondary: outline
10. Focus rings 2px accent

## Component recipes

### Panel
```html
<section class="mgr-panel mgr-accent-bar">
  <header class="mgr-panel__label">System</header>
  <h2 class="mgr-title">Deploy queue</h2>
  <p class="mgr-body">...</p>
</section>
```

### Button row
```html
<button class="mgr-btn mgr-btn--primary">Deploy</button>
<button class="mgr-btn mgr-btn--secondary">Cancel</button>
```

### Telemetry cell
```html
<div class="mgr-telem">
  <span class="mgr-panel__label">Latency</span>
  <span class="mgr-mono">42ms</span>
</div>
```

## HUD rules

- Pin to corners, not center
- Only critical: status, resource, objective, team
- Alert color only when state ≠ nominal

## Output

Intent · Tokens · ASCII wire · HTML/CSS · SVG refs · A11y · Sources

## Anti-patterns

- Centered gamey clutter
- Multiple competing CTAs
- Glitch overlays on ops screens
- Mixing thin & bold icon sets
