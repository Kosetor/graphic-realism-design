# Graphic Realism Design System

Открытая дизайн-система в эстетике **Graphic Realism** для AI-агентов.
Создавай UI, слайды и графику в едином фирменном стиле.

> Вдохновлено визуальным языком Graphic Realism (Bungie Marathon art direction).
> Это **original** система — без копирования IP Bungie / Marathon.

**Repo:** https://github.com/Kosetor/graphic-realism-design  
**Live demo:** https://kosetor.github.io/graphic-realism-design/

| Demo | URL |
|------|-----|
| Index | https://kosetor.github.io/graphic-realism-design/ |
| UI Panel | https://kosetor.github.io/graphic-realism-design/ui-panel.html |
| Slide | https://kosetor.github.io/graphic-realism-design/slide.html |

---

## Для агента (быстрый старт)

1. Прочитай [`SKILL.md`](./SKILL.md) — главная инструкция.
2. Примени токены из [`tokens/tokens.css`](./tokens/tokens.css).
3. Бери иконки / декали / фоны из папок ниже.
4. Следуй [`design-rules.md`](./design-rules.md) и сценариям в [`agents/`](./agents/).

```text
Примени Graphic Realism из https://github.com/Kosetor/graphic-realism-design
Прочитай SKILL.md и tokens/tokens.css.
Задача: <UI | slides | graphics> — <описание>.
Иконки: icons/ + decals/. Без копирования IP Bungie.
Выдай: tokens used, layout, SVG/HTML/CSS, a11y notes.
```

---

## Структура

```text
graphic-realism-design/
├── SKILL.md              # entrypoint для агента
├── DESIGN.md             # философия стиля
├── design-rules.md       # полные правила
├── rules.md              # краткий чеклист
├── tokens/               # CSS + JSON design tokens
├── agents/               # сценарии: UI / slides / graphics
├── icons/                # SVG-иконки (outline / solid / sprite)
├── decals/               # hazard, corners, brackets, marks
├── backgrounds/          # паттерны и фоны SVG
├── components/           # CSS-утилиты и примитивы
├── examples/             # HTML-примеры (+ self-contained/)
├── docs/                 # GitHub Pages live demo
└── third_party/          # лицензии upstream-паков
```

---

## Примеры локально

```bash
git clone https://github.com/Kosetor/graphic-realism-design.git
cd graphic-realism-design

# modular
open examples/ui-panel.html
open examples/slide.html

# single-file (CSS inlined)
open examples/self-contained/ui-panel.html
open examples/self-contained/slide.html
```

---

## Принципы (1 экран)

- **Graphic Realism** = плакатный язык + инженерная ясность
- Максимум **2 акцента** на view + semantic states
- Острые углы (2–4px), hairline 1px, accent bar 4px
- CAPS labels + mono telemetry
- Иконки: geometric bold outline, stroke 1.75, grid 24
- Иерархия важнее декора (no fontslop)

Подробнее: [`DESIGN.md`](./DESIGN.md)

---

## Токены (фрагмент)

```css
--mgr-bg-void:       #0B0C0E;
--mgr-bg-panel:      #1A1D24;
--mgr-bg-white:      #E8EAEF;
--mgr-accent-signal: #FF3B4A;
--mgr-accent-volt:   #C8F542;
--mgr-accent-cyan:   #3DE0FF;
```

Полный набор: [`tokens/tokens.css`](./tokens/tokens.css) · [`tokens/tokens.json`](./tokens/tokens.json)

---

## GitHub Pages

Сайт собирается из папки `docs/` workflow’ом [`.github/workflows/pages.yml`](./.github/workflows/pages.yml).

Если Pages ещё не активен: **Settings → Pages → Source: GitHub Actions** (один раз).

---

## Лицензия

- Код и original SVG: **MIT** (см. [`LICENSE`](./LICENSE))
- Не копировать ассеты / UI / брендинг Bungie, Marathon, Kurppa Hosk
