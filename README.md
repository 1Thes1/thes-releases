# Thes

**Windows VPN-клиент со split-tunnel** · VLESS / Reality / Hysteria2 (sing-box)

[![Latest release](https://img.shields.io/github/v/release/1Thes1/thes-releases?label=latest&color=2ea44f)](https://github.com/1Thes1/thes-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/1Thes1/thes-releases/total?color=0969da)](https://github.com/1Thes1/thes-releases/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11%20x64-0078d4)](https://github.com/1Thes1/thes-releases/releases/latest)

---

<p align="center">
  <a href="#-русский"><strong>Русский</strong></a> ·
  <a href="#-english"><strong>English</strong></a> ·
  <a href="https://github.com/1Thes1/thes-releases/releases/latest"><strong>⬇ Скачать / Download</strong></a>
</p>

---

## 🇷🇺 Русский

### Что это

**Thes** — десктопный VPN для Windows на базе [sing-box](https://sing-box.sagernet.org/).  
Работает с обычными подписками (как Happ): VLESS, Reality, Hysteria2 и др.

- **Split-tunnel** — в VPN только выбранные сайты и приложения (YouTube, Discord…), остальное напрямую
- **Full** — весь трафик через VPN + опциональный kill-switch
- **Локальный DNS** (как в Happ) — стабильнее Cursor / Discord, меньше обрывов
- Обновления и откат версии прямо из панели

### Скачать

| | |
|---|---|
| **Последняя версия** | [Releases → Latest](https://github.com/1Thes1/thes-releases/releases/latest) |
| **Файл** | `Thes-Setup-x.x.x.exe` |
| **ОС** | Windows 10 / 11, **x64** |
| **Права** | Нужен запуск **от администратора** (TUN) |

1. Открой [последний релиз](https://github.com/1Thes1/thes-releases/releases/latest)
2. Скачай **`Thes-Setup-….exe`**
3. Установи и согласись с UAC
4. Вставь ссылку подписки → Обновить → выбери сервер → Подключить

Старые версии (откат) — в [списке релизов](https://github.com/1Thes1/thes-releases/releases).

### Быстрый старт

1. **Подписка** — вставь URL от провайдера (или импорт `vless://` / `hy2://`)
2. **Режим Split** — добавь сайты (например `youtube.com`) и/или приложения
3. **Локальный DNS** — лучше оставить включённым
4. **Подключить** — кнопка питания

Настройки хранятся в `%AppData%\Thes` и не сбрасываются при обновлении.

### Режимы

| Режим | Поведение |
|--------|-----------|
| **Split** | VPN только для выбранных сайтов и приложений |
| **Full** | Весь трафик через VPN |
| **Kill-switch** | Только в Full — блок при обрыве туннеля |

### Типичные вопросы

**SmartScreen / антивирус ругается?**  
Установщик пока без код-подписи. «Подробнее → Выполнить в любом случае», либо добавь исключение. Исходники: [1Thes1/thes](https://github.com/1Thes1/thes) (приватный).

**Нужен админ?**  
Да. TUN на Windows требует права администратора.

**Где логи?**  
В панели Thes → Настройки → Логи. Или `%AppData%\Thes`.

**Как откатиться?**  
Настройки → список версий → выбери старый тег → Установить. Или скачай нужный Setup с [Releases](https://github.com/1Thes1/thes-releases/releases).

**YouTube частично мимо VPN?**  
Часто виноват QUIC в браузере. Выключи QUIC или пользуйся доменами из списка сайтов в Split.

### Поддержка протоколов

VLESS (+ Reality / Vision), Hysteria2, и другие, которые отдаёт подписка в формате, понятном sing-box.

### Важно

Это репозиторий **только установщиков**. Исходный код — в отдельном приватном репо.  
Thes не продаёт VPN-серверы: нужна своя подписка / нода.

---

## 🇬🇧 English

### What it is

**Thes** is a Windows VPN client built on [sing-box](https://sing-box.sagernet.org/).  
Works with common subscription links (Happ-style): VLESS, Reality, Hysteria2, and more.

- **Split-tunnel** — only selected sites/apps go through the VPN
- **Full tunnel** — all traffic via VPN, optional kill-switch
- **Local DNS** (Happ-like) — fewer drops for Cursor / Discord
- In-app updates and version rollback

### Download

| | |
|---|---|
| **Latest** | [Releases → Latest](https://github.com/1Thes1/thes-releases/releases/latest) |
| **File** | `Thes-Setup-x.x.x.exe` |
| **OS** | Windows 10 / 11, **x64** |
| **Rights** | Must run as **Administrator** (TUN) |

1. Open the [latest release](https://github.com/1Thes1/thes-releases/releases/latest)
2. Download **`Thes-Setup-….exe`**
3. Install and accept UAC
4. Paste subscription URL → Refresh → pick a server → Connect

Older builds: [all releases](https://github.com/1Thes1/thes-releases/releases).

### Quick start

1. Paste your provider subscription URL (or import `vless://` / `hy2://`)
2. Use **Split** and add sites/apps you want behind the VPN
3. Keep **Local DNS** on unless you know you need remote DoH
4. Hit Connect

Settings live in `%AppData%\Thes` and survive upgrades.

### Modes

| Mode | Behavior |
|------|----------|
| **Split** | VPN only for selected sites and apps |
| **Full** | Everything through the VPN |
| **Kill-switch** | Full mode only — block traffic if the tunnel dies |

### FAQ

**SmartScreen / antivirus warning?**  
The installer is not code-signed yet. Use “More info → Run anyway”, or add an exclusion. Source: [1Thes1/thes](https://github.com/1Thes1/thes) (private).

**Why admin?**  
Windows TUN requires elevated privileges.

**Logs?**  
Thes panel → Settings → Logs, or `%AppData%\Thes`.

**Rollback?**  
Settings → version list → pick an older tag, or grab a Setup from [Releases](https://github.com/1Thes1/thes-releases/releases).

**YouTube sometimes bypasses VPN?**  
Often browser QUIC. Disable QUIC or rely on domain rules in Split.

### Protocols

VLESS (+ Reality / Vision), Hysteria2, and other outbounds your subscription provides for sing-box.

### Note

This repo ships **installers only**. Application source is private.  
Thes does not sell VPN servers — bring your own subscription / node.

---

## Links

| | |
|---|---|
| **Latest download** | https://github.com/1Thes1/thes-releases/releases/latest |
| **All versions** | https://github.com/1Thes1/thes-releases/releases |
| **Source (private)** | https://github.com/1Thes1/thes |

---

<p align="center">
  <sub>Thes · Windows split-tunnel VPN · sing-box</sub>
</p>
