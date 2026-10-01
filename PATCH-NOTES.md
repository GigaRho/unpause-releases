# Patch notes

What changed in each version of Unpause, newest first, written for players. Each release on the [Releases](https://github.com/GigaRho/unpause-releases/releases)
page carries the same notes, and Settings › Updates shows them under What's new before you install.

## 0.2.0-alpha.4 — the things you told us about alpha.3 (2026‑10‑01)

A day and a half after alpha.3, from one player's list after a day with it. Highlights:

- **Install from the app**: Restart and install quits, installs and comes back; What's new is a short page in the app,
  since the version you had.
- **One card per game**: zipped and unzipped copies, regions, revisions and discs are one card; a PC game's folder is
  one game; arcade games show their titles; search finds "ff6" and "ffvi".
- **A desktop that gets out of your way**: three card sizes, a compact list, grouped Settings, the sidebar tree,
  Ctrl+K and Ctrl+F, a wide game page, whole covers, and a scroll that moves only when you move it.
- **Stop stops**: the library scan and the background passes end when you say so.

Known: Back has no fixed place yet; the letter button does not follow the letter; the start question is a Windows
dialog; ZX Spectrum games now play in RetroArch's Fuse core.

## 0.2.0-alpha.3 — fast on a big library, and a desktop that looks like one (2026‑09‑30)

From one player's real library of 23,000 games: what was slow, what looked wrong and what could be lost. Highlights:

- **A desktop that shows more**: smaller text and controls at a desk, seven columns of games where there were five,
  Settings in about two screens, one status bar that stays put, nothing glowing under your mouse.
- **No more waiting on your folders**: they are read at start once a day instead of every time; search reads a page,
  not the library; details and pictures reach every game in the background, shown on the tray with a stop button.
- **Your library outlives a reinstall**: daily copies in your Documents folder, and a start without a library asks
  first: Restore, or Start fresh. Settings shows the copies and removes them when you ask twice.
- **Steam covers are back**, from Steam's own files under their new name.
- **A slow emulator is starting, not frozen**: "Starting…" until its window answers, and the wait is not counted as play.

Known: the question at start is a Windows dialog a controller cannot answer yet; save backups and captures still go
with "remove app data" (your library copies stay); ZX Spectrum games are not shown yet.

## 0.2.0-alpha.2 — every way a game comes in (2026‑09‑28)

About 130 landed changes in three days, most of them the library telling the truth. Highlights:

- **Home tells the truth.** No more "ready to play" for every game: Home says how many consoles still need setup, never
  offers a game that cannot start, and a Library card says why a game can't start yet.
- **Art and details from what you already have**: pictures beside a game, the ones ES‑DE, RetroBat or Steam already
  downloaded, a PC game's own icon; connect IGDB or change the details source and your existing games are asked again.
- **What's new, since your build**, and a real nightly channel with notes written for you.
- **Family**: Library › Show… by age rating and without the mature content a Steam developer declared.
- **Stores, honestly**: a Steam game says when Steam is updating it or found its files damaged; an Xbox game says it may
  be Game Pass; Epic's Options open the Epic launcher; PS3, 3DS and Vita packages install through their emulators.

Known: a zipped and an unzipped copy of a ROM are still two cards, and PC installers can still show as games (next
entry of the plan). If Unpause says your library was saved by a newer version, install this build.

## 0.2.0-alpha.1 — the first alpha under the name Unpause (2026‑09‑25)

The first alpha under the name Unpause and the first published here; every alpha after it arrives through Settings › Updates on its own. Highlights:

- **Everything you play in one place.** Your Steam, Epic, GOG, Xbox and Battle.net games appear next to your console games,
  with no sign‑in, and Play hands them to their store. EA app, Ubisoft Connect, Amazon Games and itch are **experimental**:
  they have not yet been tried on a real install, so some games may be missing. The programs on your PC can join too.
- **Home tells you what to play tonight**: Continue, a Tonight pick, your Backlog and what's new since last time. Mark each
  game Backlog, Playing, Beaten, Completed or Shelved.
- **Artwork and details without an account**: box art, screenshots and title screens, year, developer, publisher and genre
  for your games, with favorites, tags, collections and filters by console, generation and decade.
- **Save backups before every launch**: Unpause backs up a game's saves (and, for GameCube, Wii, PlayStation, PlayStation 2
  and PSP, its save states) before every launch, and you can restore a backup from the game's Options. A restore can also
  change other games that share the same memory card or save folder, so check before you restore.
- **The Doctor** names the BIOS and firmware files a console needs and checks yours, and looks at this PC for missing
  runtimes, old drivers and power settings. **Get emulators** installs a few open‑source emulators from their official
  releases.
- **Tune for this device** (early): measures your processor, memory and graphics chip in a few seconds. In this preview
  its memory measurement is not reliable, so it rates no console and offers no preset.
- **Windows handhelds** get their own layout, battery warnings and play through sleep (a preview until it has been tested on
  each handheld); **Controller only** mode and more accessibility options.
- **Help & feedback**: report a bug or share an idea from inside Unpause, with the diagnostics shown to you in full first.
- When a game stops, Recovery says what actually happened and what to do next; on Windows set to English, Unpause also
  notices when a game stops responding (other languages of Windows later). On Linux and the Steam Deck a different check
  runs today and can wrongly say "Not responding" (for example with Flatpak emulators); a later update fixes it.
- If you used the RetrUX preview, your library moves over by itself on the first start.

## 0.1.0 — first test build (2026‑09‑20, as RetrUX)

The first installable build, shared with testers before the rename; it was not published here.

- Add a folder, get a library: 48 systems recognized, fast with tens of thousands of titles.
- Settings › Emulators shows which of 61 emulator setups were found, and lets you point at any it missed.
- Supervised launches: crashes are reported in plain language, with diagnostics you can copy.
- Choose the emulator per game; play time and last played on cards; Continue playing and Recently added on Home.
- Text size up to 2×, reduced motion, layouts for desktop, TV and handheld.
- Everything stays on your computer: no accounts, no telemetry.
