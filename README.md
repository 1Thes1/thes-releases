# Thes

**Windows VPN** · раздельный туннель по сайтам / приложениям **или** полный VPN · VLESS / Reality / Hysteria2 · платные и бесплатные серверы

[![Latest release](https://img.shields.io/github/v/release/1Thes1/thes-releases?label=latest&color=2ea44f)](https://github.com/1Thes1/thes-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/1Thes1/thes-releases/total?color=0969da)](https://github.com/1Thes1/thes-releases/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11%20x64-0078d4)](https://github.com/1Thes1/thes-releases/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![Free catalogs](https://img.shields.io/badge/free%20VPN-public%20catalogs-orange)](https://github.com/1Thes1/thes-releases#бесплатные-vpn-серверы)

---

<p align="center">
  <a href="#-русский"><strong>Русский</strong></a> ·
  <a href="#-english"><strong>English</strong></a> ·
  <a href="https://github.com/1Thes1/thes-releases/releases/latest"><strong>⬇ Скачать / Download</strong></a>
</p>

---

## 🇷🇺 Русский

### Чем Thes отличается

Большинство клиентов гонят **весь** трафик в VPN. Thes заточен под **раздельный** режим:

| | **Раздельный VPN (Split)** | **Полный VPN (Full)** |
|---|---|---|
| Что в туннеле | Только выбранные **сайты** и/или **программы** | Весь трафик системы |
| Остальное | Идёт напрямую (быстрее, родной IP) | Тоже через VPN |
| Когда удобно | Видео, соцсети, отдельные сервисы — без «тормозов» у всего ПК | Нужна полная маска / всё через ноду |
| Kill-switch | — | Опционально: блок сети при обрыве |

**Уникально для Thes:**

- **Split по сайтам и приложениям** в одном клиенте — не «весь браузер», а конкретные домены + отдельные exe
- **Белый / чёрный список программ** — всегда в VPN или всегда мимо (даже в Full)
- **Локальный DNS** — меньше обрывов, чем у схем «DNS только через прокси»
- **Бесплатные каталоги** встроены: поиск публичных списков + своя ссылка
- **Проверка ноды после подключения** — меньше ситуаций «ONLINE, а сайты мёртвые»
- **Обновление и откат версии** из панели
- Свои **платные** подписки и **бесплатные** публичные серверы — на выбор

Ядро — [sing-box](https://sing-box.sagernet.org/) (VLESS, Reality, Hysteria2 и др.). Thes не продаёт серверы: нужна своя подписка или бесплатный каталог.

### Режимы VPN

#### 1. Раздельный (Split) — по сайтам и приложениям

В VPN попадает только то, что ты указал:

- **Сайты** — домены популярных сервисов (видео, соцсети, мессенджеры, магазины…), которые добавишь в список  
- **Приложения** — конкретные программы целиком  

Всё остальное (банки, госуслуги, локальная сеть, обычный интернет) — **напрямую**, без лишней нагрузки на ноду.

#### 2. Полный (Full)

Весь трафик Windows идёт через VPN. Можно включить **kill-switch**, чтобы при падении туннеля трафик не «утекал» мимо.

### Бесплатные VPN-серверы

Вкладка **«Бесплатно»**:

1. **«Найти доступные»** — проверка публичных каталогов, какие сейчас отдают рабочие ноды  
2. **Подтянуть каталог** — список серверов в панели, пинг и подключение  
3. **Своя бесплатная ссылка** — любой открытый URL подписки  

> ⚠️ Публичные ноды часто медленные или пропадают. Для ежедневной работы лучше своя подписка; бесплатное — чтобы попробовать Thes или открыть нужное без ключа.  
> Импорт бесплатного списка **заменит** текущую подписку в приложении, пока снова не вставишь свой URL.

### Скачать

| | |
|---|---|
| **Последняя версия** | [Releases → Latest](https://github.com/1Thes1/thes-releases/releases/latest) |
| **Файл** | `Thes-Setup-x.x.x.exe` |
| **ОС** | Windows 10 / 11, **x64** |
| **Права** | Запуск **от администратора** (TUN) |
| **Лицензия** | [MIT](./LICENSE) |

1. Открой [последний релиз](https://github.com/1Thes1/thes-releases/releases/latest)  
2. Скачай **`Thes-Setup-….exe`**  
3. Установи (UAC)  
4. Подписка **или** «Бесплатно» → сервер → Подключить  

Старые сборки: [все релизы](https://github.com/1Thes1/thes-releases/releases).

### Быстрый старт

1. URL провайдера *или* **Бесплатно** → «Найти доступные»  
2. Режим **Split** → добавь нужные сайты / программы  
3. **Локальный DNS** лучше оставить включённым  
4. Подключить  

Настройки: `%AppData%\Thes` (сохраняются при обновлении).

### Планы обновлений

Уже есть: стабильный split / full, локальный DNS, откат версии, меньше ложных «мёртвых» нод, аккуратнее автообновление.

**Скоро:**
- Удобнее бесплатные каталоги (фильтры, большие списки без подвисаний)
- Ещё стабильнее dial / failover
- Подпись установщика (меньше SmartScreen), когда будет сертификат

**Дальше:**
- Более понятный интерфейс и онбординг
- Больше готовых пресетов сайтов и приложений
- Android-клиент (отдельно)
- Быстрый обмен профилем

Новости версий: [Releases](https://github.com/1Thes1/thes-releases/releases) (заметки RU + EN).

### Частые вопросы

**SmartScreen?** Установщик пока без код-подписи → «Подробнее → Выполнить в любом случае».  
**Админ?** Да, для TUN.  
**Логи?** Панель → Настройки → Логи, или `%AppData%\Thes`.  
**Откат?** Настройки → список версий, или Setup со страницы релизов.  
**Сайт в Split иногда мимо VPN?** Часто виноват QUIC в браузере — выключи QUIC или проверь домены в списке.

### Лицензия

Программа и материалы этого репозитория распространяются под **[MIT License](./LICENSE)**.  
Можно использовать, копировать и изменять при сохранении уведомления об авторских правах.  
Thes **не** предоставляет VPN-серверы; ответственность за выбранную подписку / публичный каталог — на пользователе.

Исходный код приложения: [1Thes1/thes](https://github.com/1Thes1/thes) (приватный). Здесь — только установщики.

---

## 🇬🇧 English

### What makes Thes different

Most VPN apps force **everything** through the tunnel. Thes is built for **selective** routing:

| | **Split VPN** | **Full VPN** |
|---|---|---|
| Through the tunnel | Only selected **sites** and/or **apps** | All system traffic |
| Everything else | Goes direct (faster, home IP) | Also via VPN |
| Best for | Video, social, specific services — without slowing the whole PC | Full mask / all traffic on the node |
| Kill-switch | — | Optional: block if the tunnel drops |

**What stands out:**

- **Split by site and by app** in one client — not “whole browser”, but chosen domains + specific executables  
- **Always-VPN / always-direct app lists** — even in Full mode  
- **Local DNS** — fewer drops than “DNS only via proxy” setups  
- **Built-in free catalogs** — discover public lists or paste your own free URL  
- **Post-connect dial check** — fewer “ONLINE but sites dead” cases  
- **Update & rollback** from the panel  
- Use **paid** subscriptions or **free** public servers  

Core engine: [sing-box](https://sing-box.sagernet.org/) (VLESS, Reality, Hysteria2, …). Thes does not sell servers.

### VPN modes

#### 1. Split — by sites and apps

Only what you select goes through the VPN:

- **Sites** — domains of popular services you add to the list (video, social, messengers, stores…)  
- **Apps** — entire applications by process  

Everything else (banking, government, LAN, normal browsing) stays **direct**.

#### 2. Full

All Windows traffic uses the VPN. Optional **kill-switch** blocks leaks if the tunnel dies.

### Free VPN servers

**Free** tab:

1. **“Find available”** — probe public catalogs for live nodes  
2. **Import a catalog** — servers appear in the list; ping & connect  
3. **Your own free URL** — any open subscription link  

> ⚠️ Public nodes are often slow or disappear. Prefer a paid subscription for daily use; free mode is for trying Thes or a quick unblock.  
> Importing a free list **replaces** the current subscription in the app until you paste your URL again.

### Download

| | |
|---|---|
| **Latest** | [Releases → Latest](https://github.com/1Thes1/thes-releases/releases/latest) |
| **File** | `Thes-Setup-x.x.x.exe` |
| **OS** | Windows 10 / 11, **x64** |
| **Rights** | Run as **Administrator** (TUN) |
| **License** | [MIT](./LICENSE) |

1. Open the [latest release](https://github.com/1Thes1/thes-releases/releases/latest)  
2. Download **`Thes-Setup-….exe`**  
3. Install (UAC)  
4. Subscription **or** Free tab → connect  

Older builds: [all releases](https://github.com/1Thes1/thes-releases/releases).

### Quick start

1. Provider URL *or* **Free** → “Find available”  
2. **Split** → add sites / apps  
3. Keep **Local DNS** on  
4. Connect  

Settings: `%AppData%\Thes`.

### Roadmap

Shipping now: solid split / full, local DNS, rollback, fewer false-dead nodes, safer auto-update.

**Soon:** better free-catalog UX, stronger dial / failover, signed installer when a cert is available.  

**Later:** UI polish, more presets, Android client, easy profile sharing.

See [Releases](https://github.com/1Thes1/thes-releases/releases) (RU + EN notes).

### FAQ

**SmartScreen?** Not code-signed yet → “More info → Run anyway”.  
**Admin?** Required for TUN.  
**Logs?** Settings → Logs, or `%AppData%\Thes`.  
**Rollback?** In-app version list or Setup from Releases.  
**Site in Split sometimes bypasses VPN?** Often browser QUIC — disable QUIC or check your domain list.

### License

Released under the **[MIT License](./LICENSE)**.  
Use, copy, and modify with the copyright notice retained.  
Thes does **not** provide VPN servers; you are responsible for the subscription or public catalog you use.

App source: [1Thes1/thes](https://github.com/1Thes1/thes) (private). This repo is **installers only**.

---

## Links

| | |
|---|---|
| **Latest download** | https://github.com/1Thes1/thes-releases/releases/latest |
| **All versions** | https://github.com/1Thes1/thes-releases/releases |
| **License** | [MIT](./LICENSE) |
| **Source (private)** | https://github.com/1Thes1/thes |

---

<p align="center">
  <sub>Thes · Split by site/app or full tunnel · MIT · Windows</sub>
</p>
