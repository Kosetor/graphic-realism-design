# Graphic Realism Design System

Open, agent-ready design system for **UI, Personal OS dashboards, slides and graphics** in the Graphic Realism style.

> Product-first: geometric graphic language + engineering clarity + real agent-native states.
> Original system only—do not copy Bungie/Marathon/Kurppa Hosk IP.

**Repository:** https://github.com/Kosetor/graphic-realism-design  
**Product reference:** https://github.com/Kosetor/personal-os  
**Live demo:** https://kosetor.github.io/graphic-realism-design/

## Start here

1. Read [`SKILL.md`](./SKILL.md).
2. Load [`tokens/tokens.css`](./tokens/tokens.css).
3. For an app/PWA shell, also load [`tokens/personal-os.css`](./tokens/personal-os.css).
4. Use [`icons/mgr-geometry/`](./icons/mgr-geometry/) as the primary visual icon/decal language.
5. Pick the appropriate agent scenario in [`agents/`](./agents/).

```text
Apply Graphic Realism from github.com/Kosetor/graphic-realism-design.
Use MGR Geometry Pack (icons/mgr-geometry/manifest.json) as primary icon language.
For app shells read agents/personal-os.md + components/shell.css.
Task: <UI | Personal OS | slides | graphics> — <description>.
Return: intent, tokens/state map, MGR assets, layout, code, responsive and a11y notes.
```

## Recommended icon pack

### MGR Geometry Pack

[`icons/mgr-geometry/`](./icons/mgr-geometry/) is the **recommended default pack** for this system.

It contains **29 SVG** assets for:

- workspace/system marks (`cube-grid`, `atom`, `circle-grid`)
- network and integrations (`globe`, `globe-grid`, `interwoven`)
- objectives and validation (`crosshair-square`, `diamond-*`)
- signal/status (`alert-circle`, `lightning-bolts`, `sun-rays`, `star-8-circle`)
- navigation/flow (`arrow-*`, `arrows-*`, `navigation`)
- telemetry and chrome (`bars`, `line-circles-*`, `radial-square`, `zigzag-band`)

See [`manifest.json`](./icons/mgr-geometry/manifest.json) and [`preview.md`](./icons/mgr-geometry/preview.md).

Fallback for conventional tiny actions: Phosphor Bold / Tabler / Lucide only when an MGR semantic equivalent is absent.

## System model

```text
Base    → content, controls, data, typography
Chrome  → panels, labels, borders, corner cuts, MGR marks
FX      → optional grid/hatch/noise/motion, never essential information
```

## Repository map

```text
graphic-realism-design/
├── SKILL.md                     # agent entrypoint
├── DESIGN.md                    # philosophy + product reference
├── design-rules.md              # full design rules
├── rules.md                     # delivery checklist
├── tokens/
│   ├── tokens.css               # base tokens
│   └── personal-os.css          # agent/PWA shell semantic tokens
├── agents/
│   ├── ui.md                    # generic UI
│   ├── personal-os.md           # agent-native shell scenario
│   ├── slides.md
│   └── graphics.md
├── components/
│   ├── utilities.css
│   ├── shell.css                # topbar / rail / main / status
│   └── agent-console.css        # state, queue, telemetry, Markdown
├── icons/
│   ├── mgr-geometry/            # recommended 29-SVG pack
│   ├── outline/
│   ├── solid/
│   └── sprite.svg
├── decals/                      # structural decals
├── backgrounds/                 # subtle patterns
├── examples/                    # modular + self-contained HTML
└── docs/                        # GitHub Pages demo
```

## Product-reference rules

`personal-os` is the reference for turning this language into a working app:

- config-driven visual decisions
- agent status/queue/activity as first-class UI
- Markdown and code remain readable
- responsive shell and 44px touch targets
- empty/loading/error/offline states exist before FX polish
- reduced-motion support

Full scenario: [`agents/personal-os.md`](./agents/personal-os.md).

## Principles

- One primary action per view
- Maximum two accents per view
- CAPS labels + mono data
- 2–4px radii, 1px hairline, sharp modular geometry
- One strong MGR mark per panel/slide; decorative opacity 4–8%
- State = label + color + mark; never color alone
- Hierarchy over decoration

## License

- Original code/docs/SVG: MIT—see [`LICENSE`](./LICENSE)
- Verify provenance and licenses before redistributing imported MGR Geometry assets.
