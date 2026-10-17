# Конфиденциальность / Privacy

Кратко: **Thes не продаёт ваш трафик**. Маршрутизация идёт через ноды **вашей** подписки или выбранного публичного каталога.

Thes does **not** sell your traffic. Routing goes through **your** subscription nodes or a public catalog you choose.

---

## Русский

### Что хранится локально (`%AppData%\Thes\`)

- URL подписки (который вы вставили);
- кэш списка серверов;
- HWID (если используете панели, которым он нужен);
- списки сайтов/приложений для split;
- флаги режима (split/full, DNS, failover…);
- данные лаб (Games / Drops), если включали — в т.ч. токены сессии Twitch для Drops.

Эти файлы **не** отправляются в git и **не** входят в Setup.

### Что уходит в сеть

| Куда | Зачем |
|------|--------|
| Ваш VPN-провайдер / панель | Обновление подписки, HWID (как требует панель) |
| Выбранная нода | Зашифрованный VPN-трафик приложений/сайтов в split/full |
| GitHub (`thes-releases`) | Проверка версии / скачивание обновления |
| Twitch (только если Drops) | Логин и API дропсов |
| Steam/Epic (локально/если лабы) | Чтение библиотеки на этом ПК |

Thes **не** имеет отдельного «телеметрического бэкенда Thes» для просмотра вашего трафика.

### Чего мы не контролируем

Провайдер подписки видит метаданные соединения с нодой (как у любого VPN-клиента). Политика приватности — у **вашего** провайдера, не у этого репозитория установщиков.

---

## English

### Local storage

Settings and subscription cache live in `%AppData%\Thes\` only on your PC.

### Network

- Subscription panel (refresh + HWID if required)
- Chosen VPN node (tunneled traffic)
- GitHub Releases (updates)
- Twitch only if you use Drops
- No Thes-operated traffic-spying backend

### Not under our control

Your VPN provider’s privacy policy applies to the tunnel endpoint.
