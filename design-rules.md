# Design Rules — Graphic Realism (full)

## 1. Color

### Surfaces
| Token | Hex | Use |
|-------|-----|-----|
| `--mgr-bg-void` | `#0B0C0E` | App canvas |
| `--mgr-bg-base` | `#12141A` | Secondary canvas |
| `--mgr-bg-panel` | `#1A1D24` | Cards / panels |
| `--mgr-bg-elevated` | `#242832` | Elevated surfaces |
| `--mgr-bg-white` | `#E8EAEF` | Light panels on void |
| `--mgr-bg-frost` | `#F4F5F7` | Highest light surface |

### Ink
| Token | Hex |
|-------|-----|
| `--mgr-ink-primary` | `#0B0C0E` |
| `--mgr-ink-on-dark` | `#F4F5F7` |
| `--mgr-ink-muted` | `#8B919C` |
| `--mgr-ink-faint` | `#5A606C` |

### Accents (max 2 per view)
| Token | Hex | Role |
|-------|-----|------|
| `--mgr-accent-signal` | `#FF3B4A` | Interactive path / danger |
| `--mgr-accent-volt` | `#C8F542` | Ready / go / primary CTA |
| `--mgr-accent-cyan` | `#3DE0FF` | Data / link / tech |
| `--mgr-accent-amber` | `#FFB020` | Warning |
| `--mgr-accent-violet` | `#A78BFA` | Special / rare |

### Rules
1. Color encodes function, not ornament.
2. Never rely on color alone — pair with icon/label.
3. WCAG AA minimum; HUD critical text prefer AAA.
4. Light panels on dark void = signature move.

## 2. Typography

```
UI:      Inter / IBM Plex Sans / system-ui
Display: Space Grotesk / Chakra Petch / DIN Condensed
Mono:    IBM Plex Mono / JetBrains Mono
```

| Role | Size | Weight | Case |
|------|------|--------|------|
| Display | 28–40 | 700 | Title/CAPS |
| Title | 20–28 | 600–700 | Title |
| Body | 14–16 | 400–500 | Sentence |
| Label | 11–12 | 600 | ALL CAPS + tracking 0.08em |
| Data | 12–14 mono | 500 | as-is |

**Forbidden:** >3 type styles in one block; decorative outline/glitch fonts in primary UI.

## 3. Space & shape

- Grid base **8px** (4px micro)
- Radius: 0 / 2 / 4 / 8 max (pill only for chips)
- Border: 1px default, 2px strong controls
- Optional clip-path corner cut 8–12px
- Min hit target 44px

## 4. Materials (pick 1–2 per component)

Allowed: flat fill · hairline · accent bar 4px · hazard stripe · hard shadow `4px 4px 0 #000` · mono inset strip · noise ≤6% on lore only.

Forbidden: heavy glass stack · soft 24px shadows · rainbow gradients · photo noise on primary UI.

## 5. Motion

- Fast 120ms · UI 180ms · Panel 280ms
- Ease: `cubic-bezier(0.2, 0.8, 0.2, 1)`
- Enter: fade + 8–12px slide
- Hover: border/accent change, not scale 1.05
- Loading: segmented bar + mono %, not soft endless spinner

## 6. Components

### Panel
Dark or light surface, 1px line, CAPS header label, optional left accent bar, optional corner cut.

### Button
| Variant | Style |
|---------|-------|
| Primary | solid volt/signal, CAPS, 700 |
| Secondary | 2px outline |
| Ghost | text + icon |
| Danger | signal fill |
| Ready | volt fill |

### Tabs
CAPS · active = 2px underline OR filled chip — not both + glow.

### Telemetry
Mono value · CAPS xs label above · rectangular progress.

### HUD
Corners of viewport · critical only · mono + status color on alert.

## 7. Icons

- ViewBox 24×24, safe 2px
- Stroke 1.75 (1.5–2.0), `currentColor`
- `stroke-linecap: square`, `stroke-linejoin: miter`
- Outline default · solid active
- Readable at 16px
- Naming: `ic-{domain}-{name}-{outline|solid}.svg`

Full rules: `icons/README.md`.

## 8. Decals

Required kit: hazard 45° · corner registration · accent bar · tick ruler · status pip · bracket frame · diagonal hatch (≤8% opacity).

Full rules: `decals/README.md`.

## 9. Slides

- 1 idea per slide
- Large display type
- Void or white field + one accent
- Decals as edge chrome, not center noise
- See `agents/slides.md`

## 10. A11y

- Focus ring 2px accent
- Contrast AA+
- `aria-` labels on icon-only controls
- Don’t convey state by color only
- Prefer `prefers-reduced-motion`

## 11. IP

Original work only. No Bungie/Marathon/Kurppa Hosk assets, logos, or UI clones.
