# Rules — quick checklist

Use before shipping any UI / slide / graphic.

## Always

- [ ] Tokens from `tokens/tokens.css` only (no random hex)
- [ ] ≤2 accent colors on the view
- [ ] CAPS labels + mono for numbers/IDs
- [ ] Radius ≤8px; prefer 2–4px
- [ ] Icons 24 grid, stroke ~1.75, `currentColor`
- [ ] One primary CTA
- [ ] Contrast AA+
- [ ] Focus states visible
- [ ] Original assets only (no Bungie IP)

## Never

- [ ] Fontslop (4+ type styles mashed)
- [ ] Glass + blur + gradient + stripe all at once
- [ ] Neon everywhere
- [ ] Soft huge shadows as primary depth
- [ ] Thin 1px icons mixed with bold set
- [ ] Continuous decorative animation on decals

## Assets path map

```text
icons/outline/     default
icons/solid/       active
decals/            chrome marks
backgrounds/       patterns ≤8% opacity
components/        utilities.css
```

## Agent output shape

Intent → Tokens → Wire → SVG → Code → A11y → Sources
