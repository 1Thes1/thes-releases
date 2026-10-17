# Что внутри Thes / What’s inside

Прозрачное описание продукта **без исходного кода**. Исходники приложения приватны; здесь — что именно ставится и как устроено.

Thes application source is **private**. This page explains what ships in the installer and how it works.

---

## Русский

### Стек

| Слой | Технология |
|------|------------|
| Оболочка UI | **Electron** (Chromium + Node.js) |
| Локальный API | Express на `127.0.0.1` (панель в браузере приложения) |
| VPN-ядро | **sing-box** (в комплекте установщика) |
| Туннель | Windows TUN (`thes-tun`, адрес `172.19.0.1/30`) |
| Установщик | NSIS (`Thes-Setup-*.exe`) |

### Режимы

- **Split** — в VPN только выбранные сайты (домены) и программы (`.exe`); остальной трафик напрямую.
- **Full** — весь трафик через ноду; опционально kill-switch.
- Протоколы берутся из вашей подписки (часто VLESS/Reality, Trojan, Hysteria2 и др.).

### Подписки

- Ссылка Happ / Enot / совместимой панели.
- При обновлении списка может отправляться **HWID** (нужен многим панелям).
- Thes **не является** VPN-провайдером: серверы и трафик — от вашей подписки или публичных каталогов.

### DNS и Wi‑Fi

- По умолчанию **локальный DNS** (подход как у Happ) — меньше нагрузки на домашний роутер.
- Опционально DoH через ноду.
- Не запускайте Thes и Happ одновременно (два TUN ломают DNS/Wi‑Fi). В приложении есть детект и кнопка «Закрыть мешающий VPN».

### Данные на диске

Всё пользовательское — в **`%AppData%\Thes\`** (JSON и служебные файлы):

- настройки split / режим / DNS;
- кэш подписки (список нод);
- HWID (если задан);
- настройки лаб (Games / Drops), если включали.

Обновление Setup **не стирает** эту папку. Удаление Thes через «Программы и компоненты» обычно тоже оставляет AppData (можно удалить вручную).

### Обновления

Приложение проверяет **релизы этого репозитория** (`1Thes1/thes-releases`) и предлагает скачать новый `Thes-Setup-*.exe`.

### Чего здесь нет

- Исходников UI/сервера Thes (private).
- Вашей ссылки подписки и паролей в git/релизе.
- Отдельного «облака Thes» для слежки за трафиком — маршрутизация идёт через выбранную ноду подписки.

### Лаборатории (бета)

- **Игры** — библиотека Steam/Epic, привязка к VPN.
- **Twitch Drops** — кампании, прогресс, автоклейм готовых наград (нужен вход в Twitch в приложении).

---

## English

### Stack

| Layer | Tech |
|-------|------|
| UI shell | **Electron** (Chromium + Node.js) |
| Local API | Express on `127.0.0.1` |
| VPN core | Bundled **sing-box** |
| Tunnel | Windows TUN (`thes-tun`, `172.19.0.1/30`) |
| Installer | NSIS (`Thes-Setup-*.exe`) |

### Modes

- **Split** — only selected sites/apps via VPN.
- **Full** — all traffic via the node; optional kill-switch.
- Protocols come from your subscription.

### Subscriptions

- Happ / Enot / compatible panel URL.
- **HWID** may be sent when refreshing the list.
- Thes is **not** a VPN provider; servers come from your sub or public catalogs.

### Data

User data lives in **`%AppData%\Thes\`** and survives Setup updates.

### Updates

In-app update checks **this** public repo’s GitHub Releases.

### Not included here

- Thes app source code (private).
- Your subscription URL or secrets in the installer.
- A Thes “cloud” that inspects your traffic.

### Labs (beta)

Games (Steam/Epic) and Twitch Drops helpers.

---

См. также: [ARCHITECTURE.md](ARCHITECTURE.md) · [OPEN-SOURCE.md](OPEN-SOURCE.md) · [PRIVACY.md](PRIVACY.md) · [FEATURES.md](../FEATURES.md)
