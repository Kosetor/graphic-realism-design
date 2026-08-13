# Icons

## Structure

```text
icons/
├── outline/     # default state
├── solid/       # active / selected
├── sprite.svg   # <symbol> sprite
└── README.md
```

## Spec

```
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
ic-{domain}-{name}-outline.svg
ic-{domain}-{name}-solid.svg
```

Domains: `nav`, `status`, `action`, `system`, `media`, `user`

## Template

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"
     fill="none" stroke="currentColor" stroke-width="1.75"
     stroke-linecap="square" stroke-linejoin="miter" aria-hidden="true">
  <!-- paths -->
</svg>
```

Solid: `fill="currentColor" stroke="none"`.

## Upstream adaptation

Preferred sources (MIT/ISC): Phosphor Bold, Tabler, Lucide, Radix, Heroicons.

Pipeline: normalize 24 → stroke 1.75 → square/miter → currentColor → SVGO (keep viewBox).

## Checklist

- [ ] Clear at 16px
- [ ] Unique silhouette in set
- [ ] No hardcoded hex (except multi-color brand — discouraged)
- [ ] Outline + solid pair when used as toggle
