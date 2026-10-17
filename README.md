# Thes

[![Latest release](https://img.shields.io/github/v/release/1Thes1/thes-releases?label=latest&color=2fd3a2)](https://github.com/1Thes1/thes-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/1Thes1/thes-releases/total?label=downloads&color=66c0f4)](https://github.com/1Thes1/thes-releases/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%2F%2011-0078D4?logo=windows&logoColor=white)](https://github.com/1Thes1/thes-releases/releases/latest)
[![Core](https://img.shields.io/badge/core-sing--box-orange)](docs/public/OPEN-SOURCE.md)

**Thes** — клиент VPN для Windows: пускает в туннель только нужные сайты и программы (**split**) или весь трафик (**full**). Ядро — **sing-box**, оболочка — **Electron**.

**Thes** is a Windows VPN client: tunnel only selected sites/apps (**split**) or everything (**full**). Core: **sing-box**, shell: **Electron**.

| | |
|---|---|
| **Скачать** | [**Thes-Setup (latest)**](https://github.com/1Thes1/thes-releases/releases/latest) |
| **Что это** | VPN-клиент под вашу подписку Happ / Enot / совместимую панель |
| **Не это** | Не VPN-провайдер — серверы и трафик от вашей подписки |
| **Данные** | `%AppData%\Thes\` — настройки не сгорают при обновлении |
| **Исходники** | Приватные; здесь — Setup + понятные доки «что внутри» |

---

## За 1 минуту / 1-minute start

1. Скачай **[Thes-Setup-*.exe](https://github.com/1Thes1/thes-releases/releases/latest)** → установи.
2. Запусти **от имени администратора** (нужно для TUN).
3. Вкладка **Подписки** → вставь ссылку Happ/Enot → **Подтянуть**.
4. Выбери страну или сервер → **Подключить**.
5. Если мешает **Happ** — **Закрыть мешающий VPN** (или трей Happ → Выход). Два TUN вместе ломают Wi‑Fi.

```
Setup.exe  →  Админ  →  Подписка  →  Подключить
```

---

## Что умеет / Features

| | RU | EN |
|---|----|----|
| Режимы | Split (сайты + `.exe`) или Full + опциональный kill-switch | Split or Full + optional kill-switch |
| Подписки | Happ / Enot / панели + HWID | Happ / Enot / panels + HWID |
| Сеть | Локальный DNS (бережнее к домашнему Wi‑Fi), failover нод | Local DNS (Wi‑Fi friendly), node failover |
| Конфликты | Детект Happ, WARP, Clash… и кнопка закрыть | Detects Happ, WARP, Clash… one-click close |
| Лабы | Игры (Steam/Epic), Twitch Drops (бета) | Games (Steam/Epic), Twitch Drops (beta) |
| Обновления | Из этого репозитория | From this repository |

Подробнее: [FEATURES.md](docs/FEATURES.md) · [Что внутри](docs/public/INSIDE.md)

---

## Мини-инструкция / Mini guide

### Split (рекомендуется дома)

1. Режим **Split** в настройках.
2. Добавь сайты (например `youtube.com`) и/или программы (`discord.exe`).
3. Подключись — в VPN только они, остальное напрямую.

### Full

1. Режим **Full** — весь трафик через ноду.
2. Kill-switch — по желанию (строже, но жёстче к сети).

### После обновления

Настройки остаются в `%AppData%\Thes\`. Новый Setup ставится поверх.

### Типичные проблемы

| Симптом | Что сделать |
|--------|-------------|
| «Нужны права» / TUN не встаёт | Запуск **от администратора** |
| Нет стран / пустой список | HWID в Настройках → снова **Подтянуть** подписку |
| Интернет/Wi‑Fi «поплыл» | Закрой Happ полностью, в Thes — «Закрыть мешающий VPN» |
| SmartScreen ругается | Обычный unsigned Setup — «Подробнее» → выполнить всё равно |

Полные гайды: [RU](docs/ru/GUIDE.md) · [EN](docs/en/GUIDE.md)

---

## Прозрачность / Transparency

Исходники клиента **не** публикуются. Зато открыто написано, из чего собран продукт:

| Документ | Содержание |
|----------|------------|
| [INSIDE](docs/public/INSIDE.md) | Стек, режимы, что на диске, обновления |
| [ARCHITECTURE](docs/public/ARCHITECTURE.md) | Схема без исходников |
| [OPEN-SOURCE](docs/public/OPEN-SOURCE.md) | Electron, Chromium, sing-box и лицензии |
| [PRIVACY](docs/public/PRIVACY.md) | Локальные данные и куда ходит сеть |
| [INDEX](docs/public/INDEX.md) | Все публичные страницы |

В установке видно `sing-box.exe` и Electron/Chromium license-файлы — это нормально для такого стека.

---

## Релизы / Releases

- Актуальная версия: **[Releases → Latest](https://github.com/1Thes1/thes-releases/releases/latest)**
- Счётчик скачиваний на бейдже выше (сумма по всем `Thes-Setup-*.exe` в Releases)
- Описание каждого релиза — **на русском и английском**

---

## Лицензия / License

MIT — на **публичные материалы** этого репозитория (доки, оформление релизов).  
Исходники приложения Thes — **private**.  
Сторонние компоненты (Electron, Chromium, sing-box…) — **свои** лицензии: [OPEN-SOURCE.md](docs/public/OPEN-SOURCE.md).
