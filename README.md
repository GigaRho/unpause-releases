# Unpause

**One launcher for every generation of games.** Unpause puts your console games, your Steam, Epic, GOG and Xbox
games (Battle.net, EA app, Ubisoft Connect, Amazon Games, itch, Heroic, Lutris and Bottles are experimental until tried on a real install), and the programs on
your PC in one library, and starts each of them with the right
emulator or store in one press. It is fast with tens of thousands of titles, is being built so that a keyboard, a mouse, a
controller and touch each work on their own, at a desk, on a couch or on a handheld (in the previews, a few settings still
need a keyboard or a mouse), and explains in plain words when something goes wrong.

Unpause works with the emulators and stores you already have. It does not include, download or point to games, BIOS files
or keys.

## Download

Open the [newest release](https://github.com/GigaRho/unpause-releases/releases) and pick the file for your computer:

| Your computer | The file to download | Notes |
|---|---|---|
| Windows 10 or 11 (64‑bit) | `Unpause_<version>_x64-setup.exe` | The usual choice. The `.msi` for IT‑managed PCs comes with the stable release, not with previews and betas. |
| Windows handheld (ROG Ally, Legion Go, MSI Claw) | `Unpause_<version>_x64-setup.exe` | **Preview** until it has been tested on each handheld. |
| Mac (Apple silicon or Intel) | none yet | A Mac version comes once it has been tested on a Mac. |
| Ubuntu, Debian, Mint, Pop!\_OS | `Unpause-Preview_<version>_amd64.deb` | **Preview.** |
| Fedora, openSUSE | `Unpause-Preview_<version>_x86_64.rpm` | **Preview.** |
| Steam Deck, or any other Linux | `Unpause-Preview_<version>_amd64.AppImage` | Runs without installing. **Preview** until it has been tested on a real Deck and on Linux. |

Versions starting with `0.`, and any `-alpha` or `-beta`, are previews: they work, but expect rough edges and tell us about
them.

Step‑by‑step instructions for each system are in **[INSTALL.md](https://github.com/GigaRho/unpause-releases/blob/main/INSTALL.md)**.

## Your first five minutes

1. **Add a folder.** Home walks you through it: pick the folders where your game files live. Unpause recognizes 48
   consoles and computers from the Atari 2600 onward, plus arcade, DOS and PC games. Your store games appear on their own.
2. **Check your emulators.** Settings › Emulators shows which of 61 emulator setups Unpause found on your computer. Point it
   at any it missed, or install one of the emulators it offers from the project's own official release.
3. **Play.** Enter (or A) starts a game. When something does not start, the Recovery screen says why and what to try next;
   Settings › Doctor tells you which BIOS or firmware files a console needs and whether yours are good copies.
4. **Lost?** Hold Back on a controller for 5 seconds, or Esc for 3, while Unpause is in front: you are back on Home with
   the default controls. While a game runs, the hold resets Unpause's controls where they are, and does not reach Unpause at
   all while the game has the focus.

## Keeping Unpause up to date

From 0.2.0‑alpha.1 on, Unpause updates itself: it checks for a new version in the background, on the **stable** or **beta**
channel you choose, downloads it, checks its signature and installs it when you quit, never while a game is running.
**What's new** is the first thing you see after an update. Settings › Updates lets you read what's new first, install and
restart at once, pause updates or skip a version; while updates are paused, nothing downloads or installs. Earlier previews cannot update
themselves: install a newer version over them by hand from the
[newest release](https://github.com/GigaRho/unpause-releases/releases) once; your library and settings are kept. See
**[UPDATING.md](https://github.com/GigaRho/unpause-releases/blob/main/UPDATING.md)**.

## Help and news

- **[FAQ.md](https://github.com/GigaRho/unpause-releases/blob/main/FAQ.md)**: what Unpause does and does not do, privacy, controllers, saves.
- **[PATCH-NOTES.md](https://github.com/GigaRho/unpause-releases/blob/main/PATCH-NOTES.md)**: what changed in every version, written for players. Each release on the
  [Releases](https://github.com/GigaRho/unpause-releases/releases) page carries its own notes too.
- **Found a problem or have an idea?** Settings › Help & feedback in Unpause fills in the report for you. You can also go
  straight to [unpause-feedback](https://github.com/GigaRho/unpause-feedback).

## About this page

Everything here is published by Unpause's release process: the installers, their signatures, and the `channels` release,
whose `stable.json` and `beta.json` are what Settings › Updates reads. Please do not rely on those files' contents; they
change with every release.

## Trademarks

Unpause is not affiliated with or endorsed by Valve, Microsoft, Sony, Nintendo, Sega, Epic Games, GOG, Blizzard, ASUS,
Lenovo or MSI. Steam and Steam Deck are trademarks of Valve Corporation; Xbox is a trademark of the Microsoft group of
companies; other names are trademarks of their owners.
