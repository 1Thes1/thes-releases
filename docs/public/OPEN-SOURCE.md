# Открытые компоненты / Open-source components

Thes **собирает** известные open-source проекты. Их лицензии сохраняются; благодарности авторам ниже.

Thes **bundles** well-known open-source projects. Their licenses still apply.

---

## Основные зависимости / Core

| Компонент | Назначение | Типичная лицензия |
|-----------|------------|-------------------|
| [sing-box](https://github.com/SagerNet/sing-box) | VPN / proxy ядро | GPL-3.0 (см. upstream) |
| [Electron](https://www.electronjs.org/) | Оболочка Windows-приложения | MIT |
| [Chromium](https://www.chromium.org/) (через Electron) | Рендер UI | BSD-style / Chromium terms |
| [Node.js](https://nodejs.org/) (через Electron) | Локальная логика | MIT |
| [Express](https://expressjs.com/) | Локальный HTTP API панели | MIT |
| [js-yaml](https://github.com/nodeca/js-yaml) | Разбор YAML | MIT |
| electron-builder / NSIS | Сборка установщика | MIT / zlib |

Точные тексты лицензий также лежат рядом с бинарником Electron (`LICENSE.electron.txt`, `LICENSES.chromium.html` в каталоге установки).

Exact license texts also ship next to the Electron binary in the install folder.

---

## Что открыто здесь / What’s public here

В репозитории [`thes-releases`](https://github.com/1Thes1/thes-releases):

- установщики `Thes-Setup-*.exe`;
- пользовательские гайды и описание архитектуры;
- лицензия материалов репозитория (см. корневой `LICENSE`).

**Не открыт:** исходный код клиента Thes (отдельный private-репозиторий). Это не скрывает использование sing-box/Electron — они указаны прямо и видны в составе Setup.

**Not open:** Thes client source (private repo). That does **not** hide sing-box/Electron — they are documented and present in the install tree.

---

## Проверка «что внутри Setup» / Inspecting the installer

После установки можно увидеть, например:

- `resources\bin\sing-box.exe` — ядро;
- `resources\app.asar` — упакованное приложение Electron;
- файлы лицензий Chromium/Electron в корне установки.

Распаковка asar технически возможна (как у любого Electron-приложения). Секреты подписки в установщик **не** кладутся — только в `%AppData%\Thes\` на вашем ПК.

---

## Сообщить о проблеме лицензий / License issues

Если считаете, что атрибуция неполная: откройте Issue в этом репозитории или напишите maintainer’у GitHub org **1Thes1**.
