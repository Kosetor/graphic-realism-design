# Contributing

## Goals

Держать систему **динамичной**: токены, иконки и agent-skills обновляются без ломки структуры папок.

## How to extend

### Tokens
1. Edit `tokens/tokens.css` and mirror in `tokens/tokens.json`.
2. Note breaking changes in `CHANGELOG.md`.
3. Bump version in `SKILL.md` frontmatter if agent contract changes.

### Icons
1. Add SVG to `icons/outline/` and matching `icons/solid/` when needed.
2. Follow `icons/README.md` (24 grid, stroke 1.75, currentColor).
3. Rebuild/update `icons/sprite.svg`.
4. Name: `ic-{domain}-{name}-{outline|solid}.svg`.

### Decals / backgrounds
1. Seamless patterns where tiled.
2. Document opacity guidance in folder README.
3. Keep primary UI decals non-animated.

### Agent skills
1. Update `agents/*.md` scenarios.
2. Keep `SKILL.md` as single entrypoint.

## PR checklist

- [ ] MIT-compatible assets only
- [ ] No Bungie/Marathon IP
- [ ] Tokens synced CSS ↔ JSON
- [ ] Example still renders if components change
- [ ] CHANGELOG updated

## License of contributions

By contributing, you license your work under the MIT License of this repo.
