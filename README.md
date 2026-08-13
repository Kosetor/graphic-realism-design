# Graphic Realism Design System

Открытая дизайн-система в эстетике **Graphic Realism** для AI-агентов.
Создавай UI, слайды и графику в едином фирменном стиле.

> Вдохновлено визуальным языком Graphic Realism (Bungie Marathon art direction).
> Это **original** система — без копирования IP Bungie / Marathon.

**Repo:** https://github.com/Kosetor/graphic-realism-design

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
├── examples/             # живые HTML-примеры
└── third_party/          # лицензии upstream-паков
```

| Путь | Назначение |
|------|------------|
| `SKILL.md` | Главный skill для агента |
| `tokens/` | Цвета, типографика, spacing, motion |
| `icons/` | UI-иконки 24×24 SVG |
| `decals/` | Декоративные/структурные SVG |
| `backgrounds/` | Бесшовные паттерны |
| `agents/ui.md` | Как собирать интерфейсы |
| `agents/slides.md` | Как собирать слайды |
| `agents/graphics.md` | Постеры, обложки, графика |
| `examples/` | Референс-разметка |

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

## Иконки и декали

- База: original set в `icons/` + `decals/`
- Рекомендуемые upstream (MIT): [Phosphor](https://phosphoricons.com/), [Tabler](https://tabler.io/icons), [Lucide](https://lucide.dev/)
- Правила адаптации: `icons/README.md`
- Лицензии third-party: `third_party/NOTICE.md`

---

## Обновление системы

Репозиторий рассчитан на эволюцию фирменного стиля:

1. Меняй токены → все агенты подхватывают новый look.
2. Добавляй SVG в `icons/`, `decals/`, `backgrounds/`.
3. Расширяй `agents/*.md` новыми сценариями.
4. Версионируй breaking changes в `CHANGELOG.md`.

См. [`CONTRIBUTING.md`](./CONTRIBUTING.md).

---

## Лицензия

- Код и original SVG: **MIT** (см. [`LICENSE`](./LICENSE))
- Не копировать ассеты / UI / брендинг Bungie, Marathon, Kurppa Hosk
- Upstream-иконки — по их лицензиям (MIT / CC BY и т.д.)

---

## Связанные материалы

- Философия: Graphic Realism (Joseph Cross / Marathon art direction) — как **вдохновение**
- Структура skill-репо: по образцу agent design kits (SKILL.md + tokens + examples)
