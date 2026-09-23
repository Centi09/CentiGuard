# CentiGuard

**All-in-one admin toolkit for Paper & Purpur servers**, rotating MOTDs, maintenance mode, restart countdown and anti-join-flood protection. No NMS, no dependencies, no bloat.

[![Discord](https://img.shields.io/badge/Discord-Join%20the%20server-5865F2?style=for-the-badge)](https://discord.gg/NgwZYSXnED)
[![Website](https://img.shields.io/badge/Website-centi09.de-a855f7?style=for-the-badge)](https://centi09.de)

> ⚠️ **This repository is documentation-only.** CentiGuard is closed source, the compiled plugin is distributed via [Releases](../../releases) and [centi09.de](https://centi09.de/plugins/centiguard). No source code lives here.

---

## ✨ Features

| Feature | What it does |
| --- | --- |
| 🎭 **MOTD System** | Up to 5 configurable MOTD slots, individually switchable, automatic rotation, full MiniMessage (hex colors + gradients) |
| 🚧 **Maintenance Mode** | Toggle with one command, whitelist with configurable kick message, bypass permission for staff |
| ⏰ **Restart Countdown** | `/cg restart 10m`, live action bar, title and chat broadcasts at defined intervals, never spams |
| 🌊 **Anti-Join-Flood** | Per-IP and global limits. Players who already played are exempt from the global limit, so legit rejoin waves after a restart are not blocked, bots still are |
| 🛡️ **Built-in Whitelist** | Independent of Minecraft's own whitelist, stored in `whitelist.yml`, never overwritten by a reload |
| 🔄 **Hot Reload** | `/cg reload` reloads the config live. Broken YAML is caught, backed up and the server keeps running |
| 📊 **Server Info** | `/cg info`, server & Java version, TPS (1m/5m/15m), MSPT, RAM, player count, uptime |

## 📦 Installation

1. Download `CentiGuard-1.1.1.jar` from [Releases](../../releases)
2. Drop it into your `/plugins` folder
3. Restart the server
4. Edit `plugins/CentiGuard/config.yml`
5. `/cg reload`, done

**Requirements:** Java 21+ · Paper or Purpur 1.21+ (Spigot/Bukkit also work)

## ⌨️ Commands

| Command | Permission | Description |
| --- | --- | --- |
| `/cg reload` | `centiguard.admin` | Reload config live |
| `/cg info` | `centiguard.admin` | Show server status |
| `/cg maintenance on\|off` | `centiguard.admin` | Toggle maintenance mode |
| `/cg motd list` | `centiguard.admin` | Show all 5 MOTD slots |
| `/cg motd preview <1-5>` | `centiguard.admin` | Preview one MOTD slot |
| `/cg restart <time>` | `centiguard.admin` | Start a restart countdown |
| `/cg restart cancel` | `centiguard.admin` | Cancel the countdown |
| `/cg wl on\|off` | `centiguard.admin` | Enable/disable the whitelist |
| `/cg wl add\|remove <name>` | `centiguard.admin` | Manage whitelist entries |
| `/cg wl list` | `centiguard.admin` | List all entries |

| Permission | Description |
| --- | --- |
| `centiguard.admin` | All commands (default: op) |
| `centiguard.maintenance.bypass` | Join during maintenance |
| `centiguard.whitelist.bypass` | Join despite active whitelist |

## 💬 Support & Community

Bug reports, questions or custom plugin work, the Discord is where everything happens:

**→ https://discord.gg/NgwZYSXnED**

- 🌐 Website: https://centi09.de
- 📖 Documentation: https://centi09.de/plugins/centiguard

If CentiGuard saves you a plugin slot, a ⭐ on GitHub means a lot.

---

## 🇩🇪 Deutsch

**CentiGuard** ist ein schlankes Verwaltungs- und Schutzsystem für Paper- und Purpur-Server, alles Wesentliche in einem Plugin statt fünf verschiedenen.

5 rotierende MOTD-Slots (MiniMessage/Gradienten) · Wartungsmodus mit Whitelist · Restart-Countdown mit Chat-, Title- und Actionbar-Anzeige · Anti-Join-Flood-Schutz (pro IP + global, bekannte Spieler ausgenommen) · eigene Whitelist · Hot-Reload mit YAML-Fehlerabfang · `/cg info` für TPS, MSPT, RAM und Uptime.

**Voraussetzungen:** Java 21+, Paper oder Purpur ab 1.21.
**Support:** https://discord.gg/NgwZYSXnED

> Dieses Repository enthält **nur Dokumentation**. Das Plugin selbst ist closed source, Downloads über Releases, oder centi09.de.

---

© 2026 Centi09, All Rights Reserved. See [LICENSE](LICENSE).
