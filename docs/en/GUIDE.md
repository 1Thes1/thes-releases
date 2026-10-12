# Thes — user guide

## Install

1. Download the latest `Thes-Setup-*.exe`:  
   https://github.com/1Thes1/thes-releases/releases/latest  
2. Install. User data lives in `%AppData%\Thes\` and **survives** updates.
3. Run Thes **as Administrator** — otherwise TUN will not start.

## First connect

1. Open **Subscriptions**.
2. Paste your subscription URL (Happ, Enot, …) → pull/refresh.
3. If the country list is empty — set **HWID** in Settings (some panels require it).
4. On **Servers**, pick a country/node → **Connect**.

Recommended: **split** mode + **local DNS** (on by default) for stable home Wi‑Fi.

## Split: sites & apps

**Split** tab:

- add domains (e.g. `youtube.com`) — those go via VPN;
- add `.exe` apps if needed;
- you do not need to put the whole browser on VPN — sites are enough.

## Happ and other VPNs

Do **not** run Thes and Happ at the same time: dual TUN (`happ-tun` + `thes-tun`) breaks DNS and home Wi‑Fi.

If Thes reports a Happ conflict:

1. Click **Close conflicting VPN** on the banner, **or**
2. On Connect, confirm close-and-connect, **or**
3. Quit Happ manually: tray → **Exit** (not just closing the window).

Thes must run as Administrator or Windows may refuse to kill Happ.

## Free nodes

**Free** tab — public catalogs. Quality varies: use **Best + connect** and wait for dial. Dead nodes are temporarily banned; failover rotates.

## Updates

**Settings → Updates → Check for updates**.  
Installers come from public `thes-releases`. Settings in `%AppData%\Thes\` are kept.

You can pick an older version from the list and install (rollback).

## Games & Drops (beta)

Tabs may be enabled in settings / flags:

- **Games** — Steam/Epic library, launch, VPN hints.
- **Drops** — Twitch Drops campaigns and claim notifications.

## Troubleshooting

| Symptom | Action |
|--------|--------|
| “No admin — TUN won’t work” | Right-click Thes → Run as administrator |
| Happ / happ-tun conflict | Close conflicting VPN or Exit Happ |
| Home Wi‑Fi drops | Never run two VPNs; reboot the router if needed |
| Empty country list | Fix HWID + refresh subscription |
| Stuck on “Connecting…” | Cancel → another server / Best + connect |
| Settings “gone” after update | Check `%AppData%\Thes\` — never store settings only under Program Files |

## Paths

| Path | Contents |
|------|----------|
| `%AppData%\Thes\` | settings, subscription, pings, update.json |
| Install dir | usually `Program Files\Thes` |
| Logs | app data / Diagnostics in Settings |

Full feature list: [../FEATURES.md](../FEATURES.md).

Public copy of this guide (no source access needed): https://github.com/1Thes1/thes-releases
