# garrison-plugin-zomboid

> Project Zomboid RCON plugin for [Garrison](https://github.com/ProfessorZ/garrison) — the multi-game server management dashboard.

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/ProfessorZ/garrison-plugin-zomboid/releases)
[![Garrison API](https://img.shields.io/badge/garrison--api-v1-green)](https://github.com/ProfessorZ/garrison)

## Features

- **Player management** — list online players, kick, ban, unban
- **Server status** — online/offline detection, player count
- **Server options** — live `showoptions` parsing with `changeoption` support
- **59 RCON commands** — full schema across 7 categories (Player, Admin, Server, World, Mods, Safehouse, Debug)
- **Command autocomplete** — full structured command definitions with parameter hints

## Requirements

- [Garrison](https://github.com/ProfessorZ/garrison) with Plugin API v1+
- Project Zomboid dedicated server (Build 41+, Unstable supported)
- RCON enabled on your PZ server

## Installation

### Via Garrison Plugin Installer

```bash
garrison plugin install https://github.com/ProfessorZ/garrison-plugin-zomboid
```

### Manual

Clone this repository into your Garrison plugins directory:

```bash
git clone https://github.com/ProfessorZ/garrison-plugin-zomboid \
  ~/.garrison/plugins/garrison-plugin-zomboid
```

Then restart Garrison.

## Enabling RCON on Project Zomboid

In your server config (`servertest.ini`):

```ini
RCONPort=27015
RCONPassword=yourpassword
```

Or via the in-game admin panel: **Options → Server → RCON**.

## Default Ports

| Type | Port |
|------|------|
| Game | 16261 (UDP) |
| RCON | 27015 (TCP) |

## Command Categories

| Category | Commands |
|----------|----------|
| Player Management | players, kick, ban, unban, adduser, setaccesslevel |
| Admin | save, quit, reloadoptions, changeoption, showoptions |
| World | chopper, gunshot, startrain, stoprain, startthunder |
| Mods | additem, addvehicle, addxp, godmode, invisible |
| Safehouse | createhorde, releasesafehouse |
| Server | servermsg, sendpulse, checkModsNeedUpdate |
| Debug | debuglog, getinfo |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT
