# Keeping Unpause up to date

Everything happens in **Settings › Updates**. Unpause never installs anything behind your back.

## Channels: how new you like it

| Channel | What you get | For |
|---|---|---|
| **stable** (default) | Finished versions only (`1.2.0`). | Everyone. |
| **beta** | Previews of the next version (`1.3.0-beta.1`) a week or more before it is final, plus every stable version. | Players who like new things early and tell us what broke. |
| **nightly** | A build of the latest work, most days. | Testers. Things will break. |

Switch channels in the first row of Settings › Updates. You are only ever offered a version newer than the one you have; a
stable player never gets a beta or a nightly.

## How an update happens

1. Unpause checks your channel 30 seconds after it starts and every 6 hours after that, or when you press **Check now**.
   A check asks one small file what the newest version is; nothing downloads.
2. When there is something new, you see **What's new** first: the patch notes for that version.
3. **Install and restart** downloads the update, checks its signature while it downloads (a file that does not match is
   thrown away and you are told so), installs it and starts Unpause again. Your library and settings stay as they are.

Unpause does not install:

- while a game is running;
- on battery below the level you set on the Updates screen;
- when you pressed **Pause updates**, or chose **Not this version** for that version.

You can also cap the download speed. Every check and install is listed on the Updates screen's timeline, with what happened
and why.

**Download the installer instead** opens the [Releases](https://github.com/GigaRho/unpause-releases/releases) page, for when you would rather install by hand. Running
a newer installer over your current Unpause is an update too; your data is kept.

## Data packs

Between versions, Check now can also bring a **data pack**: an updated list of consoles, emulator cores and default emulators.
It is verified before use and switched in without a restart; the Updates screen says which pack is in force.

## Going back to an earlier version

Download the older installer from the [Releases](https://github.com/GigaRho/unpause-releases/releases) page and install it over the current one. Before any version
changes how your library is stored, Unpause keeps a copy of the library file next to it (`library.sqlite.v<number>.bak` in the
data folder listed in [INSTALL.md](https://github.com/GigaRho/unpause-releases/blob/main/INSTALL.md)). If the older version says it can't open your library, close Unpause, rename
`library.sqlite` to keep it, rename the newest `.bak` copy to `library.sqlite`, and start again. Play time and changes made
since that copy are not in it.

## "Updates are not signed on this build yet"

Early preview builds were published before Unpause's signing key existed. They can't verify an update, so they never
install one: download the newest installer from the [Releases](https://github.com/GigaRho/unpause-releases/releases) page once, and from then on Settings › Updates
does it for you.
