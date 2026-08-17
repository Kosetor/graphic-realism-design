# Icons

## Recommended hierarchy

1. **MGR Geometry Pack** — `icons/mgr-geometry/`  
   Primary identity, navigation motifs, telemetry, system marks, objectives, signals and decals.
2. **Original UI icons** — `icons/outline/`, `icons/solid/`, `icons/sprite.svg`  
   Small UI controls already defined by this repository.
3. **Utility fallback** — Phosphor Bold / Tabler / Lucide  
   Only when the required conventional action has no meaningful MGR equivalent.

Read [`mgr-geometry/README.md`](./mgr-geometry/README.md) and its [`manifest.json`](./mgr-geometry/manifest.json) before selecting icons.

## MGR Geometry Pack rule

- Use one dominant MGR mark per panel/slide.
- Do not normalize these source SVGs to a 24px/1.75px stroke template—preserve their original viewBox and geometry.
- Use CSS `width`, `height`, `color`, `opacity` and `currentColor` wrappers only where source SVG permits.
- For marks used as background chrome, keep opacity between 4% and 8%.

## Original UI icon spec

```text
Grid:     24×24
Safe:     2px padding (content 20×20)
Stroke:   1.75
Linecap:  square
Linejoin: miter
Color:    currentColor
Style:    geometric, industrial-sport, readable at 16px
```

## Naming

```text
ic-{domain}-{name}-{outline|solid}.svg
```

Domains: `nav`, `status`, `action`, `system`, `media`, `user`.

## Upstream adaptation

Preferred utility sources: Phosphor Bold, Tabler, Lucide, Radix, Heroicons.

Pipeline: normalize 24 → stroke 1.75 → square/miter → currentColor → SVGO (keep viewBox).

## Checklist

- [ ] Checked MGR Geometry Pack first
- [ ] Mark reads at target rendered size
- [ ] One icon language in the focal component
- [ ] No hardcoded hex for original UI icons (except approved multi-color brand assets)
- [ ] Outline + solid pair for toggles when applicable
- [ ] Source license verified for any imported asset
