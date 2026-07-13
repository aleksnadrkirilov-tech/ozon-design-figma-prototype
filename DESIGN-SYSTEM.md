# Ozon Design — структура и визуальная система

## Архитектура экранов

- Foundations: цвета, типографика, сетка, радиусы, разделители.
- Navigation: desktop header, mobile/tablet header, burger menu.
- Discovery: hero, category card, search, sort, filter group, selected chip.
- Content: project card, company card, editorial step, product card.
- Detail: project hero, facts, materials, palette, gallery, company panel.
- Feedback: favorite state, empty state, bottom-sheet filters, gallery lightbox, product modal.
- Navigation states: desktop, mobile и tablet существуют как отдельные SVG-фреймы.

## Цветовые токены

| Token | HEX | Назначение |
|---|---:|---|
| Blue / Primary | `#005BFF` | Основные действия, ссылки, выбранные фильтры |
| Blue / Soft | `#EEF4FF` | Подложки и информационные блоки |
| Pink / Accent | `#F43F8C` | Избранное и вторичный акцент |
| Pink / Soft | `#FFF0F6` | Фон кнопок избранного |
| Ink | `#13151A` | Основной текст и тёмные секции |
| Ink / Secondary | `#363A43` | Текст описаний |
| Gray | `#6C717C` | Метаинформация |
| Line | `#E7E9ED` | Разделители и обводки |
| Surface | `#F5F6F8` | Нейтральные поверхности |

## Типографика

- Основной шрифт: Onest.
- Резервный шрифт: Inter.
- Display: 40–64 px на desktop, 32–52 px на tablet, 28–40 px на mobile.
- Interface: 12–18 px.
- Используются веса 430, 550, 650, 700 и 760.

## Сетка

| Viewport | Ширина | Поля | Базовая раскладка |
|---|---:|---:|---|
| Desktop | 1440 px | 80 px | Контент 1280 px, 3–6 колонок |
| Tablet | 768 px | 32 px | 2 колонки |
| Mobile | 390 px | 16 px | 1 колонка |

## Состояния компонентов

- Favorite: default → favorited; меняются подпись, заливка, иконка и счётчик.
- Filters: default → category → space → fully filtered → empty.
- Gallery: 6 полноэкранных состояний с previous, next и close.
- Product: collection → informational modal → collection или project.
- Navigation: desktop header, mobile menu и отдельные стартовые точки для каждого viewport.

Все ключевые состояния представлены отдельными импортируемыми SVG, поэтому Smart Animate можно настроить вручную без платных функций.
