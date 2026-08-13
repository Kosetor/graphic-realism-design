---
name: graphic-realism-design
description: >
  Apply the Graphic Realism design system for UI, slides, and graphics.
  Use when the user asks for interfaces, dashboards, HUDs, presentations,
  posters, icons, or any visual work in the Graphic Realism / MGR style.
version: 1.0.1
license: MIT
repository: https://github.com/Kosetor/graphic-realism-design
demo: https://kosetor.github.io/graphic-realism-design/
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
3. `rules.md`
4. Сценарий: `agents/ui.md` | `agents/slides.md` | `agents/graphics.md`
5. При необходимости: `design-rules.md`, `DESIGN.md`
6. Ассеты: `icons/`, `decals/`, `backgrounds/`, `components/`
7. Референс: https://kosetor.github.io/graphic-realism-design/

## Design tokens (минимум)

```text
Surfaces:  void #0B0C0E | panel #1A1D24 | white #E8EAEF
Accents:   signal #FF3B4A | volt #C8F542 | cyan #3DE0FF | amber #FFB020
Type:      UI Inter | Display Space Grotesk | Mono IBM Plex Mono
Radius:    2–4px (max 8px cards)
Icon:      24×24, stroke 1.75, square cap, miter join, currentColor
Corner:    clip-path + inset box-shadow (see utilities.css)
```

## Формат ответа агента

1. Intent · 2. Tokens · 3. Layout · 4. SVG · 5. Code · 6. A11y · 7. Sources

## Жёсткие запреты

- Копировать UI/ассеты Bungie / Marathon / Kurppa Hosk
- Primary UI с glitch/noise > 6%
- >1 primary CTA без причины

version: 1.0.1
