# Changelog, CentiGuard

Alle nennenswerten Änderungen an diesem Plugin.
Format orientiert sich an [Keep a Changelog](https://keepachangelog.com/).

## [1.1.1], 23.09.2026

### Fixed
- **Config-Crash behoben:** Eine fehlerhafte `config.yml` beim Serverstart führte zu einer
  `NullPointerException` und das Plugin lud nicht. Die kaputte Datei wird jetzt als
  `config.yml.invalid` gesichert und automatisch durch eine Standard-Config ersetzt.
  Beim `/cg reload` bleiben weiterhin die alten, gültigen Werte erhalten.
- **Anti-Join-Flood kickte legitime Spieler:** Der Zähler war global, dadurch flogen Spieler
  z. B. nach `/cg restart` mit "Zu viele Verbindungen" raus. Neu:
 , Limit **pro IP-Adresse** (`max-joins-per-ip`) als eigentlicher Bot-Schutz
 , **Bekannte Spieler** (waren schon einmal auf dem Server) zählen nicht mehr gegen das
    globale Limit (`exempt-known-players`)
- **MiniMessage-Injection:** `/cg wl add|remove|list` haben Spieler-Eingaben direkt in
  MiniMessage-Strings eingesetzt. Jetzt wird `Component.text()` verwendet.
- **Doppelte Nachricht:** `/cg restart cancel` sendete die Abbruch-Meldung zweimal.

### Changed
- Alle `ConfigManager`-Felder sind jetzt `volatile` (saubere Sichtbarkeit für asynchrone Events).
- `/cg wl add|remove` validieren den Namen (1-32 Zeichen, keine Steuerzeichen).
  Bedrock/Geyser-Namen mit Sonderzeichen bleiben möglich.
- Neue Config-Keys sind rückwärtskompatibel, bestehende `config.yml` läuft ohne Anpassung weiter.

### Added
- Config-Keys: `centiguard.anti-flood.max-joins-per-ip`, `centiguard.anti-flood.exempt-known-players`

## [1.1.0], 2026

### Added
- `/cg info`, Server-Version, Java, TPS (1m/5m/15m), MSPT, RAM, Spieler, Uptime
- Eigene CentiGuard-Whitelist (`whitelist.yml`) mit `/cg wl on|off|add|remove|list`
- Permission `centiguard.whitelist.bypass`

## [1.0.0], 2026

### Added
- MOTD-System: 5 konfigurierbare Slots mit Rotation und MiniMessage
- Wartungsmodus mit Whitelist und `centiguard.maintenance.bypass`
- Restart-Countdown (`/cg restart <zeit>` / `cancel`) mit Chat, Title und Actionbar
- Anti-Join-Flood-Schutz
- Hot-Reload (`/cg reload`) mit YAML-Fehlerabfang
