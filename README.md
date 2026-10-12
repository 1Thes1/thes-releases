# Thes

**Thes** — Windows VPN (sing-box): split по сайтам/приложениям или полный туннель.

**Thes** is a Windows VPN client (sing-box): split by site/app or full tunnel.

| | |
|---|---|
| **Установщики / Installers** | [Releases](https://github.com/1Thes1/thes-releases/releases/latest) |
| **Платформа** | Windows 10/11 · запуск **от администратора** (TUN) |
| **Данные** | `%AppData%\Thes\` (сохраняются при обновлении) |

Исходный код **приватный**. Здесь — только публичные Setup.exe и пользовательская документация.

Source code is **private**. This repo ships public Setup.exe installers and user docs only.

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

Подробнее: [docs/ru/GUIDE.md](docs/ru/GUIDE.md) · [docs/FEATURES.md](docs/FEATURES.md)

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

More: [docs/en/GUIDE.md](docs/en/GUIDE.md) · [docs/FEATURES.md](docs/FEATURES.md)

---

## Latest release

https://github.com/1Thes1/thes-releases/releases/latest

License: MIT (this releases repo).
