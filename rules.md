# Rules — quick checklist (v1.1)

## Product first

- [ ] Primary task and one primary CTA are explicit
- [ ] Ready / working / queued / warning / error / offline states considered
- [ ] Markdown and code have readable surfaces
- [ ] Mobile behavior and 44px targets are defined

## Visual system

- [ ] Tokens only; no arbitrary hex values
- [ ] Base works without chrome/FX
- [ ] ≤2 accents per view
- [ ] CAPS labels + mono for data/IDs
- [ ] Radius ≤8px; prefer 2–4px
- [ ] One dominant MGR Geometry mark per panel/slide
- [ ] Background mark/FX ≤8% opacity
- [ ] Text label + color + mark for states

## Icons

- [ ] First choice: `icons/mgr-geometry/`
- [ ] Use Phosphor/Tabler only for absent utility semantics
- [ ] Do not mix visual icon languages in one focal component
- [ ] `ic-q-logo.svg` only if source/license/brand context permits

## Quality

- [ ] Contrast AA+
- [ ] Focus states visible
- [ ] `prefers-reduced-motion` respected
- [ ] No decorative FX behind code or primary text
- [ ] No copied Bungie/Marathon IP

## Agent output

Intent → Shell map → Tokens/state map → MGR assets → Code → Responsive → A11y → Sources
