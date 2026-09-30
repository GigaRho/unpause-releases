# Keeping Unpause up to date

From 0.2.0‑alpha.1 on, Unpause updates itself: a new version downloads in the background, is checked against Unpause's
own signature, and installs when you quit. The next time you start Unpause, **What's new** is the first thing you see.
Earlier preview builds were not signed and never update themselves: install a new version by hand from the
[Releases](https://github.com/GigaRho/unpause-releases/releases) page once (see "Updates are not signed on this build yet"
below); your library and settings are kept.

## Channels: how new you like it

| Channel | What you get | For |
|---|---|---|
| **stable** (default) | Finished versions only (`1.2.0`). | Everyone. |
| **beta** | Previews of the next version (`1.3.0-beta.1`) a week or more before it is final, plus every stable version. | Players who like new things early and tell us what broke. |

Switch channels in the first row of Settings › Updates. You are only ever offered a version newer than the one you have; a
stable player never gets a beta.

## How an update happens (signed builds)

1. Unpause checks your channel 30 seconds after it starts and every 6 hours after that, or when you press **Check now**.
   An alpha or beta build always follows at least the beta channel, so it is offered the next alpha or beta.
2. When there is something new, Unpause downloads it in the background and checks its signature while it downloads (a
   file that does not match is thrown away and the Updates screen says so).
3. When you quit Unpause, the installer runs by itself (a small progress window, no questions). Your library and settings
   stay as they are.
4. The next start opens **What's new** over the first screen: the notes for the version you now have. One press closes it,
   and it does not come back.
5. If the installer ran but Unpause starts on the old version, it says the update did not install and offers **Get the
   installer**, the page with that version's installer.

In Settings › Updates you can read What's new before the update installs, **Install and restart** at once, or choose
**Not this version**.

Unpause does not install:

- while a game is running;
- on battery below the level you set on the Updates screen;
- when you pressed **Pause updates**, or chose **Not this version** for that version.

You can also cap the download speed. Every check and install is listed on the Updates screen's timeline, with what happened
and why.

**Download the installer instead** opens the [Releases](https://github.com/GigaRho/unpause-releases/releases) page, for when you would rather install by hand. Running
a newer installer over your current Unpause is an update too; your data is kept.

## Data packs

A **data pack** is an updated list of consoles, emulator cores and default emulators that could arrive between versions.
Data packs are **off** until they are signed and Unpause checks the signature before using one; until then Unpause uses
only the lists built into the version you installed, and you get new lists by installing a new version.

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
