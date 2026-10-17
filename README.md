# Thes

**Thes** — Windows VPN (sing-box): split по сайтам/приложениям или полный туннель.

**Thes** is a Windows VPN client (sing-box): split by site/app or full tunnel.

| | |
|---|---|
| **Установщики / Installers** | [Releases](https://github.com/1Thes1/thes-releases/releases/latest) |
| **Платформа** | Windows 10/11 · запуск **от администратора** (TUN) |
| **Данные** | `%AppData%\Thes\` (сохраняются при обновлении) |
| **Прозрачность** | [Что внутри](docs/public/INSIDE.md) · [Архитектура](docs/public/ARCHITECTURE.md) · [OSS](docs/public/OPEN-SOURCE.md) · [Privacy](docs/public/PRIVACY.md) |

Исходный код **приложения Thes приватный**. Здесь — публичные Setup.exe, гайды и описание «что внутри», чтобы было понятно, из чего собран клиент (Electron + sing-box и т.д.).

Thes **application source is private**. This repo ships Setup.exe, user guides, and transparency docs (stack, architecture, open-source credits) — not the app source tree.

---

## Русский

### Быстрый старт

1. Скачай `Thes-Setup-*.exe` из [Releases](https://github.com/1Thes1/thes-releases/releases/latest).
2. Установи и запусти **от имени администратора**.
3. **Подписки** → вставь ссылку Happ/Enot → **Подтянуть**.
4. Выбери страну/сервер → **Подключить**.
5. Если мешает Happ — кнопка **Закрыть мешающий VPN** (или трей Happ → Выход).

### Возможности

- **Split / Full** — VPN для выбранных сайтов и программ, или весь трафик
- Подписки Happ / Enot и совместимые панели + HWID
- Бесплатные каталоги нод с авто-failover
- Локальный DNS (как Happ) — стабильнее домашний Wi‑Fi
- Детект конфликтов (Happ, WARP, Clash…) и закрытие мешающего VPN
- Игры (бета), Twitch Drops
- Обновления прямо из этого репозитория

### Важно про Happ

Не запускай Thes и Happ одновременно: два туннеля ломают домашний Wi‑Fi и DNS. Закрой Happ полностью (трей → Выход) или используй кнопку в Thes.

### Типичные проблемы

| Симптом | Решение |
|--------|---------|
| TUN не работает / «без прав» | Запуск от администратора |
| Конфликт Happ | Закрыть мешающий VPN / Выход из Happ |
| Нет стран в списке | HWID в Настройках + обновить подписку |
| После обновления настройки на месте | Да — они в `%AppData%\Thes\` |

### Документация

| | |
|---|---|
| [Индекс](docs/public/INDEX.md) | Все публичные страницы |
| [Что внутри](docs/public/INSIDE.md) | Стек, данные, обновления |
| [Архитектура](docs/public/ARCHITECTURE.md) | Схема без исходников |
| [Open-source](docs/public/OPEN-SOURCE.md) | sing-box, Electron, лицензии |
| [Privacy](docs/public/PRIVACY.md) | Локальные данные и сеть |
| [Возможности](docs/FEATURES.md) | Полный список RU+EN |
| [Гайд](docs/ru/GUIDE.md) | Руководство пользователя |

---

## English

### Quick start

1. Download `Thes-Setup-*.exe` from [Releases](https://github.com/1Thes1/thes-releases/releases/latest).
2. Install and run **as Administrator**.
3. **Subscriptions** → paste Happ/Enot URL → pull.
4. Pick a country/server → **Connect**.
5. If Happ conflicts — **Close conflicting VPN** (or Happ tray → Exit).

### Features

- **Split / Full** — selected sites/apps, or all traffic
- Happ / Enot (and compatible) subscriptions + HWID
- Free node catalogs with auto-failover
- Local DNS (Happ-like) for stable home Wi‑Fi
- Conflict detection (Happ, WARP, Clash…) and one-click close
- Games (beta), Twitch Drops
- In-app updates from this repo

### About Happ

Do not run Thes and Happ together: dual TUN breaks home Wi‑Fi and DNS. Fully quit Happ (tray → Exit) or use the button in Thes.

### Troubleshooting

| Symptom | Fix |
|--------|-----|
| TUN / “no admin” | Run as Administrator |
| Happ conflict | Close conflicting VPN / Exit Happ |
| Empty country list | Set HWID + refresh subscription |
| Settings after update | Kept in `%AppData%\Thes\` |

### Docs

| | |
|---|---|
| [Index](docs/public/INDEX.md) | All public pages |
| [What’s inside](docs/public/INSIDE.md) | Stack, data, updates |
| [Architecture](docs/public/ARCHITECTURE.md) | Design without source |
| [Open-source](docs/public/OPEN-SOURCE.md) | sing-box, Electron, licenses |
| [Privacy](docs/public/PRIVACY.md) | Local data & network |
| [Features](docs/FEATURES.md) | Full RU+EN list |
| [Guide](docs/en/GUIDE.md) | User guide |

---

## Latest release

https://github.com/1Thes1/thes-releases/releases/latest

**License:** MIT applies to the **public materials** in this repository (docs and release packaging notes). The Thes application **source code** remains private and is not licensed by this file. Bundled third-party components (Electron, Chromium, sing-box, …) keep their **own** licenses — see [docs/public/OPEN-SOURCE.md](docs/public/OPEN-SOURCE.md).
