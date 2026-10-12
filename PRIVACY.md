# Privacy

Unpause works offline, and it never sends your library, play time, saves or settings anywhere. It has no telemetry and
no account. A bug report leaves your computer only when you send it, after you have read every line of it.

## What goes online

Every address Unpause reaches, what it fetches, when, and what stops it. Every request names itself as
`Unpause/<version> (+https://github.com/GigaRho/unpause-releases)`. The table is generated from the app's own list, and
the build fails when the code reaches an address that is not in it.

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
| `www.steamgriddb.com`, `cdn2.steamgriddb.com` | Box art for store games, PC games and apps | After a scan, only with your SteamGridDB key added | Remove the key (Settings › Pictures and details) |
| `api.github.com` | The ideas people asked for on Unpause's feedback board | When you open Help & feedback | Nothing is fetched unless you open it |
<!-- online:end -->

Links Unpause shows you (an emulator's home page, a driver download, a sign-up page) open in your browser; Unpause itself
fetches nothing from them.

## Passwords and keys

Credentials for artwork and details services are kept in your system's credential store, never in Unpause's settings or
logs, and are sent only to the service they belong to.

Unpause is not affiliated with or endorsed by Valve, Microsoft, Sony, Nintendo, Sega, Epic Games, GOG or any other company
whose stores, consoles or services it works with.
