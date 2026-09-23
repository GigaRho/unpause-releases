# Questions players ask

## What Unpause is

**What does Unpause do?**
It gathers everything you play into one library: game files for consoles and computers (48 systems, Atari 2600 onward, plus
arcade and DOS), your Steam, Epic, GOG, Xbox and Battle.net games (EA app, Ubisoft Connect, Amazon Games and itch are
experimental until they have been tried on a real install), and the programs on your PC. Play starts each one the right
way: the matching emulator for a game file, the store's own client for a store game. It tracks play time, backs up saves
before a launch, and tells you in plain words why something did not start.

**Does Unpause come with games, BIOS files or keys? Can it get them for me?**
No, and it never will. Unpause does not include, download, link to or explain how to obtain game files, BIOS or firmware
files, or keys. Use games and files you own. Settings › Doctor can tell you which files a console needs by name and whether
your copies are good, and nothing more.

**Which emulators does it work with?**
RetroArch and its cores, and standalone emulators such as Dolphin, PCSX2, DuckStation, PPSSPP, melonDS, mGBA, Flycast, xemu
and ares: 61 setups in all. Settings › Emulators shows which ones it found. It can install a few open‑source emulators for you,
from each project's own official release, after showing you the license and release notes.

**Does it replace my stores?**
No. Unpause reads what Steam, Epic and the others installed on this computer, without signing in, and hands the game to the
store when you press Play. Buying, downloading and updating games stay in the store.

**Does it cost anything?**
Unpause is free, and the free app works fully offline. Optional paid extras may come later; they add things and are never
required to play.

## Privacy

**Do I need an account or an internet connection?**
No. Your library lives on your computer. The internet is only used for things you can see and turn off: artwork and game
details, checking for updates, installing an emulator you picked.

**Does Unpause collect data about me?**
No telemetry. A bug report is only sent when you send it, and you see every line of it first; game names, folders and your
user name are replaced before you see them.

**Where are my passwords for artwork services kept?**
In your system's credential store (Windows Credential Manager; on Linux and the Steam Deck, the kernel keyring), never in
Unpause's settings or logs. On Linux and the Steam Deck they are forgotten when you restart, until an upcoming fix, so you
enter them again after a restart.

## Playing

**Can I use a controller?**
Yes. You can use a controller, a keyboard or a mouse, and switch between them at any time. In this build pad navigation can
still skip past several items on one press; a keyboard is the reliable choice until that fix ships. Hold **Back for 5
seconds** (or **Esc for 3**) anywhere to return to Home with the default controls.

**Does it work on my handheld?**
Support for the Steam Deck and for the ROG Ally, Legion Go and MSI Claw is being built for the beta. Until each has been
tested on the real device, its download will be labeled Preview. On the Deck, the AppImage runs in desktop mode (see
[INSTALL.md](https://github.com/GigaRho/unpause-releases/blob/main/INSTALL.md)).

**A game won't start. What now?**
The Recovery screen says what happened (a missing BIOS file, a missing core, the emulator was not found, it crashed on
start…) and what to do next. From a game's Options, **Check this system** runs the Doctor for that console. If that does not
help, **Report this** on the Recovery screen fills in a bug report for you.

**Are my saves safe?**
Unpause does not change your saves while you play. Before a launch, when **Before each launch** is on in a game's Options ›
Saves & states (on by default), it copies that game's saves (and, for GameCube, Wii, PlayStation, PlayStation 2 and PSP
games, its save states) into its own backups folder, keeping the last 10 by default. The same **Saves & states** screen
restores any of them, after backing up what is there first. A restore writes into the emulator's save folder and can also
change other games that share the same memory card or save folder, so check before you restore.

**Where do my screenshots go?**
Screenshots you take while playing through Unpause (RetroArch, Dolphin, PCSX2, DuckStation, PPSSPP, mGBA and Xbox Game Bar)
are copied into the game's Gallery when you stop playing. Your originals stay where they were.

## Updates and versions

**How do I update?** On the previews published so far, by hand: install the newest release over the one you have (your
library and settings are kept); updates from inside Unpause are off until builds are signed. Then it is Settings › Updates.
See [UPDATING.md](https://github.com/GigaRho/unpause-releases/blob/main/UPDATING.md).

**What changed in this version?** [PATCH-NOTES.md](https://github.com/GigaRho/unpause-releases/blob/main/PATCH-NOTES.md), or What's new in Settings › Updates.

**Why does Windows warn me when I install?**
Early builds are not code‑signed yet. [INSTALL.md](https://github.com/GigaRho/unpause-releases/blob/main/INSTALL.md) shows the one extra click; signed installers are on the way.

## Help

**I found a bug, or I have an idea.**
Settings › Help & feedback, or [unpause-feedback](https://github.com/GigaRho/unpause-feedback): bugs and crashes as issues,
ideas, thoughts and questions in Discussions. Every report gets a first answer within a week.
