# Pocket Inquisition

**Dragon Age: Inquisition multiplayer, on servers you run.**

[![Latest release](https://img.shields.io/github/v/release/PocketInquisition/Launcher?include_prereleases&label=release)](https://github.com/PocketInquisition/Launcher/releases)
[![Discord](https://img.shields.io/badge/Discord-Dragon%20Age-5865F2?logo=discord&logoColor=white)](https://discord.com/invite/dragonage)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-support-FFDD00?logo=buymeacoffee&logoColor=black)](https://buymeacoffee.com/lastlink)

Pocket Inquisition is a custom implementation of Dragon Age: Inquisition's multiplayer servers. Host your own private server for the four-player
co-op mode, on your PC, a home server or Docker, and play with your group on it. A Windows launcher and a small in-game plugin point
only the game's multiplayer connection at your server: the game is not changed, and single player and your campaign saves are
untouched.

**Contents:** [Download](#download) · [What works](#what-works-in-060) · [Getting started](#getting-started) ·
[Hosting](#hosting-a-server) · [FAQ](#faq) · [Support](#support-and-community) · [Notice](#ea--bioware-notice)

## Download

Get the latest from **[Releases](https://github.com/PocketInquisition/Launcher/releases)** (also on Nexus Mods).

| File | For |
|---|---|
| `dai-<version>-win-x64.zip` | players and Windows hosts: the launcher, the in-game plugin and the server |
| `dai-<version>-linux-x64` | hosting the server on Linux (players still need Windows) |

**Requirements:** Dragon Age: Inquisition on PC (Steam or the EA app) and Windows 10 or 11. Nothing else to install: no .NET, no
Visual C++ redistributable, no ZeroTier app.

## What works

- **The Multiplayer hub:** signing in, all 17 characters with their ability trees and promotions, crafting, salvage, the store,
  inventory, challenges and leaderboards
- **Matches:** Create Match and Quick Match for up to four players, with map, difficulty (up to Nightmare) and public or private
  lobbies; joining a match in progress, leaving and rejoining; Proving Grounds
- **Rewards:** loot from every container, gold by difficulty, gear drops, medals and XP
- **Your progress:** record your own session on EA's servers, then import your characters, gold, gear and unlocks;
  export and import accounts between servers
- **Playing together:** on a home network, through a Cloudflare tunnel, or over the built-in ZeroTier network (no port forwarding)
- **Voice:** the game's own voice chat
- **Hosting:** join codes, player passwords, invite-only servers, a web manager for admins, Windows, Linux and Docker builds

## Getting started

1. Unzip the release anywhere **outside** the game folder.
2. Run `launcher\DaiLauncher.exe`. The Play page offers a one-minute tour; the **?** button (or F1) explains any page.
3. **To host:** Host page, **Start server**. For friends elsewhere, start a temporary tunnel there or use ZeroTier (Settings).
4. **To join:** on the Play page type the host's address and their join code.
5. With the game closed, press **Play** and go online in the game.

Pressing Play loads the plugin while the game runs and writes nothing to the game folder. To have the game load it every time, use
**Settings > Game and plugin install** (three files; **Uninstall** removes exactly those). To play on EA's servers again, pick
**EA's servers** on the Play page.

## Hosting a server

The launcher hosts a server on your PC with one button. For a dedicated host:

```
server\dai.exe serve --advertise <address players use> --data <folder>
```

Everything runs over one HTTP port (5380), so it works behind a Tunnel or an HTTPS reverse proxy. Useful options:
`--invite-only` with `dai.exe invite create`, a join code, required passwords, and starting or daily platinum. Admins manage
accounts from the web manager at `http://<server>:5380/manage`.

## Support and community

- Questions and match-ups: [Dragon Age Discord](https://discord.com/invite/dragonage)
- Support development: [Buy Me a Coffee](https://buymeacoffee.com/lastlink)

## EA / BioWare notice

Pocket Inquisition is an unofficial fan project. It is not supported, endorsed or provided by Electronic Arts or BioWare, and contains no game
code or assets. Dragon Age and Dragon Age: Inquisition are trademarks of Electronic Arts Inc.
