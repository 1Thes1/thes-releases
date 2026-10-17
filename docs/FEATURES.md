# Возможности Thes / Features

Текущая линейка: **1.0.62+**.

---

## Русский

### Подключение
- Режим **split** — в VPN только выбранные сайты и приложения; остальное напрямую
- Режим **full** — весь трафик через ноду (опционально kill-switch)
- Протоколы: VLESS / Reality, Trojan, Hysteria2 и другие, которые отдаёт подписка
- Выбор страны и конкретного сервера, избранное, запрет автоподключения к ноде
- **Лучший сервер** / **Лучший + подключить** — проба и dial
- Авто-failover при мёртвой ноде (можно отключить)
- Live-пинг и скорость (↓/↑) в шапке

### Подписки и HWID
- Ссылка подписки Happ / Enot / совместимые панели
- HWID отправляется при обновлении списка (нужен для панелей вроде Enot)
- Трафик и срок подписки в интерфейсе

### Split
- Список сайтов (домены) и программ (`.exe`)
- Пресеты пакетов, сканер установленных приложений
- Force-proxy / force-direct для отдельных процессов
- Браузеры целиком в VPN не форсятся — только выбранные сайты (как задумано)

### DNS и сеть
- **Локальный DNS** (по умолчанию, как Happ) — меньше обрывов домашнего Wi‑Fi
- Опционально DoH через ноду
- TUN `thes-tun` (172.19.0.1/30), stack `mixed`, MTU 1280, LAN в `route_exclude_address`
- `strict_route` только с kill-switch (без драйвера Mullvad, как у Happ, иначе режется DNS)

### Конфликты с другими VPN
- Детект Happ, `happ-tun`, WARP, Clash, WireGuard, Outline, Hiddify…
- **Блок подключения**, пока активен Happ / `happ-tun` (два TUN ломают домашний Wi‑Fi)
- Кнопка **«Закрыть мешающий VPN»** — гасит Happ/happd/xray и отключает `happ-tun`
- При конфликте на «Подключить» — диалог: закрыть и подключиться
- Нужны права администратора (как для TUN)

### Бесплатные каталоги
- Публичные списки нод, прогресс поиска, soft-keep / dial-ban мёртвых хостов

### Игры (бета)
- Библиотека Steam / Epic, категории, запуск
- Совместимость с игровыми бустерами (GearUP и др. — info, не блок)

### Twitch Drops
- Кампании, прогресс, уведомления; антиспам повторных claim

### Обслуживание
- Обновления из `thes-releases`
- Диагностика, flush маршрутов, проверка IP / утечек / скорости
- Автозапуск (планировщик, elevated)

### Данные
- `%AppData%\Thes\` — настройки переживают обновление Setup

---

## English

### Connection
- **Split** — only selected sites/apps via VPN; rest direct
- **Full** — all traffic via the node (optional kill-switch)
- Protocols from your subscription (VLESS/Reality, Trojan, Hysteria2, …)
- Country/server pick, favorites, no-failover pins
- **Best server** / **Best + connect** with probe + dial
- Auto-failover on dead nodes (toggleable)
- Live ping and throughput in the header

### Subscriptions & HWID
- Happ / Enot / compatible panel URLs
- HWID sent when refreshing the list
- Traffic quota and expiry in the UI

### Split routing
- Sites (domains) and apps (`.exe`)
- Pack presets, installed-app scanner
- Per-process force-proxy / force-direct
- Whole browsers are not forced onto VPN — selected sites only

### DNS & network
- **Local DNS** by default (Happ-like) for stable home Wi‑Fi
- Optional DoH via the proxy node
- TUN `thes-tun` (172.19.0.1/30), `mixed` stack, MTU 1280, LAN excluded from tunnel
- `strict_route` only with kill-switch

### Conflicting VPNs
- Detects Happ, `happ-tun`, WARP, Clash, WireGuard, Outline, Hiddify, …
- **Blocks connect** while Happ / `happ-tun` is up (dual TUN breaks home Wi‑Fi)
- **Close conflicting VPN** kills Happ/happd/xray and disables `happ-tun`
- Connect dialog can resolve then reconnect
- Requires Administrator (same as TUN)

### Free catalogs
- Public node lists, search progress, dial-ban for dead hosts

### Games (beta)
- Steam / Epic library, categories, launch
- Game boosters (GearUP, etc.) coexist as info, not block

### Twitch Drops
- Campaigns, progress, notifications; claim spam dedupe

### Maintenance
- Updates from `thes-releases`
- Diagnostics, route flush, IP / leak / speed checks
- Autostart (Task Scheduler, elevated)

### Data
- `%AppData%\Thes\` survives installer updates
