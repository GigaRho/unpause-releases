# Questions players ask

## What Unpause is

**What does Unpause do?**
It gathers everything you play into one library: game files for consoles and computers (Atari 2600 onward, plus
arcade and DOS), your Steam, Epic, GOG and Xbox games (Battle.net, EA app, Ubisoft Connect, Amazon Games, itch, Heroic,
Lutris and Bottles are experimental until they have been tried on a real install), and the programs on your PC. Play starts each one the right
way: the matching emulator for a game file, the store's own client for a store game. It tracks play time, backs up saves
before a launch, and tells you in plain words why something did not start.

**Does Unpause come with games, BIOS files or keys? Can it get them for me?**
No, and it never will. Unpause does not include, download, link to or explain how to obtain game files, BIOS or firmware
files, or keys. Use games and files you own. Settings › Doctor can tell you which files a console needs by name and whether
your copies are good, and nothing more.

**Which emulators does it work with?**
RetroArch and its cores, and standalone emulators such as Dolphin, PCSX2, DuckStation, PPSSPP, melonDS, mGBA, Flycast, xemu
and ares, among others. Settings › Emulators shows which ones it found. It can install a few open‑source emulators for you,
from each project's own official release, after showing you the license and release notes.

**Does it replace my stores?**
No. Unpause reads what Steam, Epic and the others installed on this computer, without signing in, and hands the game to the
store when you press Play. Buying, downloading and updating games stay in the store.

**Does it run on a PC or a handheld with an Arm processor?**
Not yet. Unpause is built for Intel and AMD 64‑bit processors. Windows on Arm (Snapdragon) PCs and Linux on Arm (a Raspberry Pi,
an Arm handheld) have not been tested, so nothing is promised there.

**Does it cost anything?**
Unpause is free, and the free app works fully offline. Optional paid extras may come later; they add things and are never
required to play.

## Privacy

**Do I need an account or an internet connection?**
No. Your library lives on your computer, and Unpause works offline. When it is online, it checks for a new version of
itself and of the emulators it can install, downloads what you ask it to, and, once you say yes, looks up pictures and
game details by each game's title. Your library, play time, saves and settings are never sent anywhere.

**What exactly goes online?**
Every address Unpause reaches, what it fetches, when, and what stops it. Every request names itself as Unpause and its
version. This table is generated from the app's own list, and the build fails when the code reaches an address that is
not in it. [PRIVACY.md](https://github.com/GigaRho/unpause-releases/blob/main/PRIVACY.md) has the same table.

<!-- online:begin -->
| Address | What Unpause fetches | When | What stops it |
|---|---|---|---|
| `github.com` | Whether a new version of Unpause is out, and the new version itself | 30 seconds after Unpause starts, then every 6 hours; Check in Settings › Updates and privacy | Pause updates, or turn Unpause updates off (Settings › Updates and privacy) |
| `github.com`, `mednafen.github.io`, `purei.org`, `redream.io` | The release pages of the emulators Unpause can install, to tell you when one has a new version | Once a day, the first time 30 seconds after Unpause starts; Check feeds now | Pause updates, or turn Emulator updates off (Settings › Updates and privacy) |
| `github.com`, `buildbot.libretro.com` | An emulator you chose to install | When you press Install | Nothing is fetched unless you press it |
| `buildbot.libretro.com` | The RetroArch core a game needs, when RetroArch does not have it | When you press Play on that game | Pause updates |
| `objects.githubusercontent.com`, `release-assets.githubusercontent.com` | Where GitHub serves the downloads above from | With the downloads above | As above |
| `thumbnails.libretro.com` | Covers and screenshots, looked up by each game's title | After a scan, once you said yes to looking things up online | Pictures source: off (Settings › Pictures and details) |
| `api.screenscraper.fr`, `*.screenscraper.fr` | Covers and screenshots from ScreenScraper | After a scan, only with your ScreenScraper credentials connected | Pictures source: off, or disconnect ScreenScraper |
| `raw.githubusercontent.com` | Year, developer, publisher and genre from libretro-database | After a scan, once you said yes to looking things up online | Details source: off (Settings › Pictures and details) |
| `query.wikidata.org`, `en.wikipedia.org` | A Steam game's other platforms and review scores from Wikidata, and its Wikipedia summary | When you open a Steam game's page, at most once a month per game, once you said yes to looking things up online | Details source: off (Settings › Pictures and details) |
| `id.twitch.tv`, `api.igdb.com`, `images.igdb.com` | Details, a synopsis and covers from IGDB | After a scan, and when you search for a match, only with your Twitch application connected | Details source: off, or disconnect IGDB |
| `cdn.cloudflare.steamstatic.com` | A Steam game's own library art and cover from Steam's image servers, by its app id | After a scan, once per game, once you said yes to looking things up online | Pictures source: off (Settings › Pictures and details) |
| `api.steampowered.com` | The Steam games your account owns, with your own Steam Web API key, to show the ones this PC has not installed | At each scan, only with your key added | Remove the key (Settings › Pictures and details) |
| `www.steamgriddb.com`, `cdn2.steamgriddb.com` | Box art for store games, PC games and apps | After a scan, only with your SteamGridDB key added | Remove the key (Settings › Pictures and details) |
| `api.itch.io` | The games your itch.io account owns, to show the ones this PC has not installed (itch.io support is experimental) | Only after you sign in to itch.io | Nothing is fetched unless you sign in to itch.io |
| `api.github.com` | The ideas people asked for on Unpause's feedback board | When you open Help & feedback | Nothing is fetched unless you open it |
<!-- online:end -->

**Does Unpause collect data about me?**
No telemetry. A bug report is only sent when you send it, and you see every line of it first; folder paths and your user
name are replaced, and your games' titles and file names are hidden. Read it before you send it: a report you
submit on GitHub is public.

**Where are my passwords for artwork services kept?**
In your system's credential store (Windows Credential Manager; on Linux and the Steam Deck™, your desktop's keyring, such as
GNOME Keyring or KWallet), never in Unpause's settings or logs, and they are kept across restarts. Where no keyring is
running, Unpause says it could not save them rather than forgetting them later.

## Playing

**Can I use a controller?**
Yes. You can use a controller, a keyboard or a mouse, and switch between them at any time. Hold **Back for 5 seconds** (or
**Esc for 3**) while Unpause is in front to return to Home with the default controls. While a game runs, the hold resets
Unpause's controls where they are, and while the game has the focus it does not reach Unpause at all.

**Does it work on my handheld?**
Support for the Steam Deck and for the ROG Ally, Legion Go and MSI Claw is being built for the beta. Until each has been
tested on the real device, its download will be labeled Preview. On the Deck, the AppImage runs in desktop mode (see
[INSTALL.md](https://github.com/GigaRho/unpause-releases/blob/main/INSTALL.md)).

**A game won't start. What now?**
The Recovery screen says what happened (a missing BIOS file, a missing core, the emulator was not found, it crashed on
start…) and what to do next. From a game's Options, **Check this system** runs the Doctor for that console. If that does not
help, **Report this** on the Recovery screen fills in a bug report for you.

**Are my saves safe?**
Unpause does not change your saves while you play. Before and after each game (on by default), it copies that game's
saves, and its save states where the emulator names them for the game, into its own `Save backups` folder in
`Documents\Unpause`, keeping the last 10 by default. A game of several discs (a `.m3u` playlist) brings the states of each
disc. Save states of games in CD and DVD `.chd` images are found too; those of a Dreamcast `.chd` or a game inside a
`.zip` or `.7z` are not yet, though their saves are. The game's
**Saves & states** screen restores any backup, after backing up what is there first. A memory card or folder several
games share goes back only when you ask, since it holds other games' saves too.

**I sync my saves with OneDrive, Syncthing, Dropbox or Steam Cloud. What happens when I restore?**
Unpause puts the backup's files back in the folder and keeps a copy of what was there in `Save backups`. The service you
use then syncs that folder as it always does: the restored saves go to your other devices on its next sync, or it asks
which copy to keep. The game's **Saves & states** screen says when it sees one of these services on its folder.

**Where do my screenshots go?**
Screenshots you take while playing through Unpause (RetroArch, Dolphin, PCSX2, DuckStation, PPSSPP, mGBA and Xbox Game Bar)
are copied into the game's Gallery when you stop playing. Your originals stay where they were.

## Updates and versions

**How do I update?** You do not have to. From 0.2.0‑alpha.1 on, Unpause downloads a new version in the background, checks
its signature and installs it when you quit, never while a game is running; the next start opens **What's new**. Settings ›
Updates lets you install at once, pause updates or skip a version. Earlier previews cannot update
themselves: install the newest release over the one you have once (your library and settings are kept). See
[UPDATING.md](https://github.com/GigaRho/unpause-releases/blob/main/UPDATING.md).

**What changed in this version?** [PATCH-NOTES.md](https://github.com/GigaRho/unpause-releases/blob/main/PATCH-NOTES.md), or What's new in Settings › Updates.

**Why does Windows warn me when I install?**
The installers are not code‑signed yet. SmartScreen's "Windows protected your PC" has a way through
([INSTALL.md](https://github.com/GigaRho/unpause-releases/blob/main/INSTALL.md) shows it). If Windows says **Smart App
Control** blocked it, there is no way through: Smart App Control refuses unsigned programs, so this preview cannot run on
that PC until signed installers ship.

## Help

**I found a bug, or I have an idea.**
Settings › Help & feedback, or [unpause-feedback](https://github.com/GigaRho/unpause-feedback): bugs and crashes as issues,
ideas, thoughts and questions in Discussions. Every report gets a first answer within a week.

## Trademarks

Unpause is not affiliated with or endorsed by Valve, Microsoft, Sony, Nintendo, Sega, Epic Games, GOG, Blizzard, ASUS,
Lenovo or MSI. Steam and Steam Deck are trademarks of Valve Corporation; Xbox is a trademark of the Microsoft group of
companies; other names are trademarks of their owners.
