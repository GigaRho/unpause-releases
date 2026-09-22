# Unpause

**One launcher for every generation of games.** Unpause puts your console games, your Steam, Epic, GOG, Xbox, Battle.net,
EA, Ubisoft, Amazon and itch games, and the programs on your PC in one library, and starts each of them with the right
emulator or store in one press. It is fast with tens of thousands of titles, works with a controller, a keyboard or a mouse,
from a desk, a couch or a handheld, and explains in plain words when something goes wrong.

Unpause works with the emulators and stores you already have. It does not include, download or point to games, BIOS files
or keys.

## Download

Open the [newest release](https://github.com/GigaRho/unpause-releases/releases) and pick the file for your computer:

| Your computer | The file to download | Notes |
|---|---|---|
| Windows 10 or 11 (64‑bit) | `Unpause_<version>_x64-setup.exe` | The usual choice. `…_x64_en-US.msi` is the same app for IT‑managed PCs. |
| Windows handheld (ROG Ally, Legion Go, MSI Claw) | `Unpause_<version>_x64-setup.exe` | Unpause switches to its handheld layout by itself. |
| Mac (Apple silicon or Intel) | `Unpause_<version>_universal.dmg` | One download for both kinds of Mac. |
| Ubuntu, Debian, Mint, Pop!\_OS | `Unpause_<version>_amd64.deb` | |
| Fedora, openSUSE | `Unpause-<version>-1.x86_64.rpm` | |
| Steam Deck, or any other Linux | `Unpause_<version>_amd64.AppImage` | Runs without installing. |

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
4. **Lost?** Hold Back on a controller for 5 seconds, or Esc for 3, from anywhere: you are back on Home with the default
   controls.

## Keeping Unpause up to date

Settings › Updates checks for new versions, shows what's new first, and installs only when you say so, never while a game is
running. You choose how new you like it: **stable**, **beta** or **nightly**. See **[UPDATING.md](https://github.com/GigaRho/unpause-releases/blob/main/UPDATING.md)**.

## Help and news

- **[FAQ.md](https://github.com/GigaRho/unpause-releases/blob/main/FAQ.md)**: what Unpause does and does not do, privacy, controllers, saves.
- **[PATCH-NOTES.md](https://github.com/GigaRho/unpause-releases/blob/main/PATCH-NOTES.md)**: what changed in every version, written for players. Each release on the
  [Releases](https://github.com/GigaRho/unpause-releases/releases) page carries its own notes too.
- **Found a problem or have an idea?** Settings › Help & feedback in Unpause fills in the report for you. You can also go
  straight to [unpause-feedback](https://github.com/GigaRho/unpause-feedback).

## About this page

Everything here is published by Unpause's release process: the installers, their signatures, and the `channels` release,
whose `stable.json`, `beta.json`, `nightly.json` and `packs.json` are what Settings › Updates reads. Please do not rely on
those files' contents; they change with every release.
