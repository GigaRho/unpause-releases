# Installing Unpause

Download the file for your computer from the [newest release](https://github.com/GigaRho/unpause-releases/releases) (the table in the [README](https://github.com/GigaRho/unpause-releases/blob/main/README.md) says
which one), then follow the steps for your system below.

## What you need

| | Minimum |
|---|---|
| Windows | Windows 10 or 11, 64‑bit. Unpause uses Microsoft Edge WebView2, which Windows 11 already has; on Windows 10 the installer fetches it if it is missing, so stay online for the first install. |
| macOS | Not available yet: a Mac version comes once it has been tested on a Mac. |
| Linux (**Preview**) | A 64‑bit desktop from 2022 or later (Ubuntu 22.04, Debian 12, Fedora 36 or newer), or a Steam Deck in desktop mode. |
| Space | About 100 MB for Unpause itself; artwork, save backups and captures grow with your library. |
| Games and emulators | Your own. Unpause launches the emulators and stores you already have, and can install a few open‑source emulators from their official releases. |

## Windows

1. Run `Unpause_<version>_x64-setup.exe`.
2. Until Unpause's installers are code‑signed, Windows SmartScreen shows "Windows protected your PC". Choose **More info**,
   then **Run anyway**. (Signed installers are on the way; this step then goes away.)
3. The installer puts Unpause in your Start menu. It installs for your user only and does not need administrator rights.

The `.msi` (the same app for PCs managed by an IT department or installed with a deployment tool) is not offered for
preview and beta builds; it comes with the stable release.

**Windows handhelds** (ROG Ally, Legion Go, MSI Claw), a **Preview** until it has been tested on each handheld: install the
same way in desktop mode. Unpause picks the handheld layout by itself; Settings › Accessibility › Input map has a Handheld map that puts Options and "hide Unpause" on the back paddles.

## macOS

Not available yet. A Mac version comes once it has been tested on a Mac.

## Linux (Preview)

Every Linux package, and the Steam Deck, is a **Preview** until it has been tested on Linux and on a real Deck: it works, but
expect rough edges and tell us about them. Known issue: on Linux and the Steam Deck, Unpause can wrongly say a game is
"Not responding" (for example with Flatpak emulators); a later update fixes it.

**Ubuntu, Debian, Mint, Pop!\_OS** (**Preview**) — install the `.deb`:

```bash
sudo apt install ./Unpause-Preview_<version>_amd64.deb
```

**Fedora, openSUSE** (**Preview**) — install the `.rpm`:

```bash
sudo dnf install ./Unpause-Preview_<version>_x86_64.rpm
```

**Any Linux, or the Steam Deck** (**Preview**) — the AppImage runs without installing:

```bash
chmod +x Unpause-Preview_<version>_amd64.AppImage
./Unpause-Preview_<version>_amd64.AppImage
```

On a Steam Deck, switch to desktop mode, download the AppImage into your home folder, right‑click it › Properties ›
Permissions › **Is executable**, and double‑click it. To see it in Gaming Mode, add it to Steam with **Add a Non‑Steam Game**.

## The first start

Home asks for the folders where your game files are, looks for your emulators, and reads what your stores installed on this
computer (nothing is downloaded and no sign‑in is needed). That's it: pick a game and press Play. If you used Unpause under
its old name, RetrUX, your library, artwork, backups and saved cards move over by themselves on the first start, and the old
folder stays as a backup.

## Where Unpause keeps your things

Your library (with the copies Unpause keeps before each upgrade, `library.sqlite.v*.bak`), settings, artwork, save backups
(`backups`), captures (`captures`), the emulators you installed from Get emulators (`emulators`, **with their own settings and
saves**) and your original emulator settings files that a performance preset replaced (`presets`) live in one folder:

| System | Folder |
|---|---|
| Windows | `%APPDATA%\app.unpause.desktop` |
| Linux and Steam Deck | `~/.local/share/app.unpause.desktop` |

The log Unpause writes (Settings › Help & feedback shows its last lines, scrubbed) is in `%LOCALAPPDATA%\app.unpause.desktop\logs`
on Windows and `~/.local/share/app.unpause.desktop/logs` on Linux.

Passwords and keys you give Unpause for artwork services are not in that folder: they are in your system's credential store
(Windows Credential Manager; on Linux and the Steam Deck, the kernel keyring). On Linux and the Steam Deck they are forgotten
when you restart, until an upcoming fix, so you enter them again after a restart.

Your game files and your stores are never moved or changed. Your emulators' folders are changed in two cases: restoring a
save backup writes into the emulator's save folder, and a performance preset writes the emulator's own settings file for that
game (Revert on the game's Options puts yours back). Before a launch, Unpause copies that game's saves into its `backups`
folder when **Before each launch** is on in a game's Options › Saves & states (on by default) and it knows where that
emulator keeps them. You can restore a backup from the same screen, but restoring can also change other games that share the
same memory card or save folder; check before you restore.

Updating an emulator you installed from Get emulators can leave its saves in the old version folder, and a second update can
delete them; copy its saves out before updating (fixed in an upcoming release).

## Uninstalling

- **Windows**: Settings › Apps › Installed apps › Unpause › Uninstall. Your data folder stays unless you tick "Delete the
  application data" in the uninstaller.
- **Linux**: `sudo apt remove unpause`, `sudo dnf remove unpause`, or delete the AppImage.

Deleting the data folder (or ticking the box) also deletes your save backups, the emulators you installed from Get emulators
**together with their saves**, and the only copy of any emulator settings file a preset replaced; the presets stay applied in
your emulators. Before you do it, revert your presets from each game's Options and copy out `backups` and `emulators` if you
want to keep them. Your games and the emulators you installed yourself are not deleted either way.

## Something went wrong?

See the [FAQ](https://github.com/GigaRho/unpause-releases/blob/main/FAQ.md), or report it in [unpause-feedback](https://github.com/GigaRho/unpause-feedback/issues/new/choose).
If Unpause starts, Settings › Help & feedback fills in the report for you.
