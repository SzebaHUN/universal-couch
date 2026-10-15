<p align="center">
  <img src="docs/logo.png" width="220" alt="Universal Couch 64 logo">
</p>

<h1 align="center">Universal Couch 64</h1>

<p align="center"><b>Remote couch co-op, without making your friend build the couch.</b></p>

<p align="center">
Universal Couch 64 lets you host multiplayer games from your Windows PC and invite friends to play remotely using their own controllers.<br>
Supports Project64 and experimental, validated <code>.uc64</code> game packages created with compatible external conversion tools.
</p>

## Download

### **[⬇ Download Universal Couch 64 v0.6.3 for Windows](https://github.com/SzebaHUN/universal-couch/releases/tag/v0.6.3)**

Under **Assets**, download **`Universal Couch_0.6.3_x64-setup.exe`**, run it, and follow the installer.
(Your browser saves it as `Universal.Couch_0.6.3_x64-setup.exe`. GitHub replaces the space with a dot.)
The release also lists `SHA256SUMS.txt` so you can check the download.

> [!IMPORTANT]
> **v0.6.3 is the recommended version.** Everyone in a room should use a compatible version: the host and every
> friend install **Universal Couch 64 v0.6.3**. Older releases stay available on the
> [releases page](https://github.com/SzebaHUN/universal-couch/releases) as part of the project's history.

> [!NOTE]
> GitHub also lists **"Source code (zip)"** and **"Source code (tar.gz)"** on every release. Those archives contain only this page's documentation. They are **not** the app. You only need the `x64-setup.exe` installer.

Everyone who plays installs Universal Couch 64: the host and every friend who joins. Windows 10/11 (x64) is required.

## See It in Action

<table>
  <tr>
    <td width="50%"><img src="docs/screenshots/07-four-player-room.png" alt="A full four-player room"><br><sub>A full room: host + 3 remote players</sub></td>
    <td width="50%"><img src="docs/screenshots/08-game-stream.png" alt="Guest view of a split-screen game"><br><sub>Guest view of a split-screen game, with Fit / Fill and Whole picture / My screen</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/screenshots/04-controllers.png" alt="Player/controller assignment"><br><sub>Player/controller assignment</sub></td>
    <td width="50%"><img src="docs/screenshots/01-home.png" alt="Universal Couch home screen"><br><sub>Universal Couch home screen</sub></td>
  </tr>
</table>

More screenshots: [host setup](docs/screenshots/02-host-room.png) · [room ready](docs/screenshots/03-session.png) · [settings](docs/screenshots/05-settings.png) · [join](docs/screenshots/06-join.png). Game images and private details are blurred.

## What Universal Couch 64 Does

- **HOST / JOIN with a room code.** Rooms use a code and an optional password. There's no port forwarding and no IP addresses to type.
- **Remote multiplayer for up to 4 player seats.** The host is Player 1, and up to 3 friends take Player 2–4. Extra people can join as **watchers**.
- **Streaming video and audio.** Friends see and hear the host's game over a direct, encrypted connection.
- **Controller input and assignment.** Each seat is a fixed controller port (P1–P4). The host decides who plays and who watches, and can remove players. Each player can remap buttons, and the mapping is saved per controller.
- **Guests need no game.** Friends don't need the ROM, the game package, Project64 or your save. They play with their own controller.
- **Project64 support.** One click downloads the official Project64 and applies tested settings for known games. Supported multiplayer games show as **UC verified** or **UC curated**.
- **Fit / Fill and split-screen viewing.** **Fit** shows the whole picture, **Fill** fills the screen. With **My screen**, each player zooms into their own part of a split-screen game, even in fullscreen; **Whole picture** shows everything. Players can also hold **Z + START + R** for 2 seconds to switch.
- **Stream quality.** Choose **Responsive**, **Balanced** or **Sharp**, or leave it on **Auto**, which picks a setting for your PC based on its hardware video encoders.
- **Save handling and game switching.** Pause, restart or change the game without anyone leaving the room. Universal Couch offers to save first, and save states are kept per game.
- **Test ROM locally** to check a game and your controller before inviting anyone.
- **Reconnects automatically** if a guest's connection drops.
- **Public or private rooms.** Rooms are private by default. Public rooms appear in **Browse Rooms**.
- **Discord integration** (optional) for friends, one-click invites and status.
- **8 languages:** both the app and the installer are fully available in English, Español, Português (Brasil), Français, Deutsch, Italiano, Magyar and Polski.
- **Experimental `.uc64` game packages.** See [Game packages](#game-packages-uc64-experimental).

## What is Universal Couch 64?

Universal Couch 64 brings the "everyone on one sofa" experience to friends who are far away.

- **The host** runs the game on their own PC, with their own game files and their own save.
- **Friends** join the host's room from their own PCs. They see and hear the game, and their controller is plugged straight into the host's game as the next player.

Friends don't need the game, the ROM, an emulator or the host's save. Everything game-related stays on the host's PC.

## How It Works

```
 HOST PC                                               FRIEND'S PC
 ┌──────────────────────────────┐                     ┌──────────────────────────┐
 │ your game (Project64 or a    │   game video/audio  │ Universal Couch 64       │
 │ .uc64 package)    ▲          │ ──────────────────▶ │  - sees & hears the game │
 │                   │ P2/3/4   │                     │                          │
 │ Universal Couch 64 (host)    │ ◀────────────────── │  - controller = Player 2 │
 └──────────────────────────────┘   controller input  └──────────────────────────┘
          direct, encrypted connection: no port forwarding, no IP addresses to type
```

- Rooms use a **room code** and an optional **password**. You don't need to set up IP addresses, open router ports or use tunnels.
- Video, audio and controller input go **directly between the PCs**, encrypted.
- Each person in the room has a role: **Player**, who gets a controller slot on the host's game, or **Watcher**, who watches the stream. The host decides who plays, and player roles map to fixed controller slots.

## Quick Start

1. **Everyone:** install **Universal Couch 64 v0.6.3** from the [release page](https://github.com/SzebaHUN/universal-couch/releases/tag/v0.6.3). Accept the Terms on first launch.
2. **Host:** open **Host Game** and pick your game, then start the room.
   - **N64:** let Universal Couch set up Project64 (it downloads it from the official Project64 website) and pick your ROM.
   - **`.uc64` package:** pick a package you made with a compatible converter (see [Game packages](#game-packages-uc64-experimental)). Project64 is not needed.
3. **Host:** share the **room code** (and password) with your friend, or send an invite through the app's optional Discord connection.
4. **Friend:** open **Join Game**, enter the room code and password, and plug in a controller.
5. Play. The friend's controller is the next player on the host's game.

## Host

- You need: Windows 10/11, your own legally obtained game file, and a controller if you want to play too.
- For N64 games, Universal Couch sets up and uses **its own copy of Project64**, downloaded from the official Project64 website. Alternatively, you can choose a Project64 installation yourself.
- **Private room** (default): only people with the code, password or your invite can join.
- **Public room**: your room appears in **Browse Rooms** for other Universal Couch players. Public joiners start as **Watchers**, and you choose who gets promoted to Player.
- Your game files, ROMs, `.uc64` packages, saves and Project64 settings never leave your PC.

## Guest

- You need: Windows 10/11, Universal Couch 64, a controller, and a decent internet connection.
- You do **not** need the game, a ROM, a `.uc64` package, Project64 or the host's save. Use a version compatible with the host's (v0.6.3 recommended).
- There are three ways to join:
  - enter a **room code + password** under **Join Game**;
  - pick a room from **Browse Rooms**;
  - accept a **Discord invite**.

## Game packages (`.uc64`, experimental)

A `.uc64` file is a **game package**, not an N64 ROM. It is made on the host's PC from the host's **own** game files by a
separate, compatible conversion tool, and it carries everything that game needs to run. Universal Couch 64 checks every
package before using it (file checksums, an approved game profile, and an approved runtime build) and refuses anything it
does not recognise. Universal Couch 64 itself does not include game files or game-specific runtimes, and no extra runtime
has to be installed.

Compatible converters and project-specific integrations are published in our other GitHub repositories:

- **[GoldenEye XBLA Co-op Converter](https://github.com/SzebaHUN/goldeneye-xbla-coop-converter)**: two-player co-op for
  the *GoldenEye 007* Xbox Live Arcade version. Introduced with Universal Couch 0.6.2; from v0.6.3 the converter builds
  the game's runtime on your PC and produces one self-contained package. Controls, setup and known issues are in its README.
- [More projects on GitHub](https://github.com/SzebaHUN?tab=repositories)

## Discord & Public Rooms

**Community Discord coming soon.** A Universal Couch community server for finding players, voice chat, support and release news is planned. The link will be added here when it opens.

What already works (since v0.5.8):

- **Private sessions don't need Discord.** Room code + password play works without it.
- **Optional Discord connection in the app:** link your Discord account to see your Discord friends, send and accept session invites directly from Universal Couch, and show a "Universal Couch 64" status.
- **Public rooms:** the app's **Browse Rooms** list shows rooms that hosts have chosen to make public. Anyone with Universal Couch can join them as a Watcher, and the host promotes players.

## Supported Setup

For v0.6.3:

| | |
|---|---|
| Operating system | Windows 10/11, x64 |
| N64 games | **Project64**, set up by Universal Couch or chosen by the host; Nintendo 64 games that support local multiplayer |
| Game packages | Experimental `.uc64` packages from compatible converters ([see above](#game-packages-uc64-experimental)) |
| Players | Host + up to 3 friends (4 seats), plus watchers |
| Version | Everyone in a room uses a compatible Universal Couch 64 version (v0.6.3 recommended) |
| App languages | English, Español, Português (Brasil), Français, Deutsch, Italiano, Magyar, Polski (all fully translated) |
| Installer languages | The same 8 languages |

Project64 is the only supported N64 emulator.

## What's new in v0.6.3

- Improved experimental `.uc64` game-package compatibility, including self-contained packages generated by compatible external converters.
- Game-specific runtimes are no longer part of the Universal Couch 64 installer; a package carries what its game needs.
- Improved package verification, executable integrity checks and error messages.
- Smaller, simpler main installer.
- Remote multiplayer, controller assignment, streaming, Project64 and game switching are unchanged.

Release history: [v0.6.2-rc.6](https://github.com/SzebaHUN/universal-couch/releases/tag/v0.6.2-rc.6) introduced experimental
`.uc64` packages (GoldenEye XBLA co-op), game-only stream audio and Main-first H.264 encoding;
[v0.5.8](https://github.com/SzebaHUN/universal-couch/releases/tag/v0.5.8) introduced Discord and public rooms. See the
[releases page](https://github.com/SzebaHUN/universal-couch/releases) for full notes.

## Current Status

Universal Couch 64 is actively developed. Core hosting and remote-player functionality is working; `.uc64` game-package support is experimental.

- Things may change between releases.
- Network environments differ. A connection that works on one network may behave differently on another.
- Controller-, game- or emulator-specific bugs may remain.
- Public testing is genuinely valuable. Please report what you find.

## Known Limitations

- **Windows only.** N64 games through Project64, plus experimental `.uc64` packages. No other emulators yet.
- **`.uc64` packages are experimental.** Game-specific issues are listed in each converter's README (for GoldenEye, see its [known issues](https://github.com/SzebaHUN/goldeneye-xbla-coop-converter#known-issues)).
- **Some restrictive networks may fail to connect.** Gameplay uses a direct connection between PCs, and there is currently no relay server for networks that block direct connections (for example some mobile or carrier-grade NAT connections).
- **Input lag depends on your internet connection.** Mobile connections such as 4G/5G can add noticeable delay compared with home broadband.
- **Use compatible versions.** Different Universal Couch versions may not be able to join each other's rooms, so keep up to date.
- The installer is **not code-signed** yet, so Windows SmartScreen may warn on first run. Click *More info*, then *Run anyway*. Never disable your antivirus or add exclusions for Universal Couch.

## Troubleshooting

- **Friend can't connect:** check that you both run v0.6.3. Try another network (for example a home connection instead of mobile data). Make sure the room code and password were typed exactly.
- **Controller not working:** reconnect it before joining, and check whether the host has made you a *Player* rather than a *Watcher*.
- **Laggy picture or input:** wired or 5 GHz Wi-Fi helps. Mobile data often adds delay.
- **A `.uc64` package is refused:** make it again with the latest version of its converter. Packages made for v0.6.2 must be remade for v0.6.3.
- **Logs:** Universal Couch writes a log at `%LOCALAPPDATA%\UniversalCouch\Logs\uc64.log`. Paste that path into Explorer's address bar. The log stays on your PC unless you choose to share it.

## Reporting Bugs

Please [open an issue](https://github.com/SzebaHUN/universal-couch/issues/new/choose) using the **Bug report** template. Useful details:

- Windows version (host and guest)
- controller type
- Project64 version, if you chose your own copy
- the game (for a `.uc64` package: the converter and its version, and what each player was doing)
- the Universal Couch version on every PC
- whether the host and guest connected at all
- what you expected and what happened
- screenshots, and `uc64.log` if it helps

**Never post ROMs, game files, `.uc64` packages, saves, room passwords or private invite links in an issue.**

## Support / Community

Universal Couch is free. Support is optional and helps fund development and testing.

- [More projects on GitHub](https://github.com/SzebaHUN?tab=repositories)
- [Buy Me a Coffee](https://buymeacoffee.com/szebahun)
- [Patreon](https://www.patreon.com/cw/SzebaHUN)

## Credits

- **Universal Couch 64** by **SzebaHUN**.
- Built with third-party open-source software and the Discord Social SDK. See [Third-Party Notices](THIRD_PARTY_NOTICES.md).
- Project64 is a separate program by the Project64 team, under its own licence. Universal Couch downloads it from the official Project64 website and does not include it.
- The GoldenEye XBLA runtime that was installed with v0.6.2-rc.6 is built on the open-source **rexglue** recompilation toolkit (including portions of **Xenia**) and **FFmpeg** (LGPL-2.1), among others; see [its notices](THIRD_PARTY_NOTICES-goldeneye-runtime.txt). From v0.6.3 that runtime ships with the [GoldenEye XBLA Co-op Converter](https://github.com/SzebaHUN/goldeneye-xbla-coop-converter), which carries its notices.

Universal Couch is an independent project. It is not affiliated with, endorsed by or sponsored by Nintendo, Rare, Microsoft, 4J Studios, Discord, Cloudflare, the Project64 team, the Xenia or rexglue projects or any game publisher.

## Disclaimer

Universal Couch is unofficial, independent software provided **as-is**. It does **not** provide, sell, host or distribute ROMs or other copyrighted game content. You are responsible for the games and software you use with it. See the full [Disclaimer](DISCLAIMER.md).

## Legal / Privacy

- [Terms of Use](TERMS.md)
- [Privacy Policy](PRIVACY.md)
- [Disclaimer](DISCLAIMER.md)
- [Community Guidelines](COMMUNITY_GUIDELINES.md)
- [Third-Party Notices](THIRD_PARTY_NOTICES.md)
- [License](LICENSE)

Universal Couch is proprietary software that is free to use. This repository contains documentation only; the application source code is not public.
