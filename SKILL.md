---
name: graphic-realism-design
description: >
  Apply the Graphic Realism design system for UI, slides, and graphics.
  Use when the user asks for interfaces, dashboards, HUDs, presentations,
  posters, icons, or any visual work in the Graphic Realism / MGR style.
version: 1.0.0
license: MIT
repository: https://github.com/Kosetor/graphic-realism-design
---

# SKILL: Graphic Realism Design System

Ты применяешь фирменный визуальный язык **Graphic Realism (MGR)** из этого репозитория.

## Когда активировать

- UI / dashboard / HUD / settings / agent panels
- Слайды, презентации, pitch decks
- Постеры, обложки, thumbnail, social graphics
- Иконки, декали, паттерны, brand marks (original)
- «Сделай в стиле Marathon / Graphic Realism / MGR»

## Обязательный порядок чтения

1. Этот файл (`SKILL.md`)
2. `tokens/tokens.css` (или `tokens/tokens.json`)
3. `rules.md` (краткий чеклист)
4. Сценарий:
   - UI → `agents/ui.md`
   - Слайды → `agents/slides.md`
   - Графика → `agents/graphics.md`
5. При необходимости: `design-rules.md`, `DESIGN.md`
6. Ассеты: `icons/`, `decals/`, `backgrounds/`, `components/`

## Суть стиля

**Graphic Realism** = упрощённый плакатный дизайн-язык + выразительный цвет
+ ограниченные материалы **И** реалистичные пропорции, инженерная логика, читаемость.

| Делай | Не делай |
|-------|----------|
| 1–2 акцента на экран | Неон на всём |
| Hairline panels, accent bar | Glassmorphism + blur stack |
| CAPS labels + mono data | 4+ шрифтовых стиля (fontslop) |
| Geometric bold icons 24 grid | Thin doodle / 3D isometric mix |
| Иерархия > декор | Копировать IP Bungie/Marathon |

## Design tokens (минимум)

```text
Surfaces:  void #0B0C0E | panel #1A1D24 | white #E8EAEF
Accents:   signal #FF3B4A | volt #C8F542 | cyan #3DE0FF | amber #FFB020
Type:      UI Inter/Plex Sans | Display Space Grotesk/Chakra Petch | Mono IBM Plex Mono
Radius:    2–4px (max 8px cards)
Icon:      24×24, stroke 1.75, square cap, miter join, currentColor
Space:     4/8/12/16/24/32/48
Motion:    120–280ms, ease cubic-bezier(0.2, 0.8, 0.2, 1)
```

Полные токены: `tokens/tokens.css`.

## Ассеты

| Папка | Использование |
|-------|----------------|
| `icons/outline/` | Default UI icons |
| `icons/solid/` | Active / selected |
| `icons/sprite.svg` | SVG symbol sprite |
| `decals/` | Hazard, corners, brackets, pips |
| `backgrounds/` | Subtle patterns (opacity ≤ 8%) |
| `components/utilities.css` | Готовые utility-классы |

Если нужной иконки нет — создай original SVG по `icons/README.md` (grid 24, stroke 1.75).
Можно адаптировать Phosphor Bold / Tabler / Lucide → привести к MGR rules.

## Формат ответа агента

1. **Intent** — экран/носитель
2. **Tokens used**
3. **Layout** (ASCII wireframe)
4. **SVG** (icons/decals) — inline или пути из repo
5. **HTML/CSS или React/Vue**
6. **A11y** — contrast, focus, labels
7. **Sources** — файлы repo + license upstream

## Жёсткие запреты

- Копировать UI, ассеты, логотипы, faction marks Bungie / Marathon / Kurppa Hosk
- Выдавать чужие brand marks за original
- Primary UI с glitch/scanline/noise > 6% opacity
- Более одного primary CTA на view без причины

## One-shot prompt

```text
Примени Graphic Realism (github.com/Kosetor/graphic-realism-design).
SKILL.md + tokens/tokens.css + agents/<ui|slides|graphics>.md
Задача: ...
Стек: HTML/CSS | React | Vue | SVG
Выдай полный артефакт + rationale.
```

## Версионирование

- `version` в frontmatter этого файла = skill API version
- Breaking token changes → bump minor/major + `CHANGELOG.md`
- Агенты всегда тянут `main` unless pinned to tag
