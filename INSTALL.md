# Installing Unpause

Download the file for your computer from the [newest release](https://github.com/GigaRho/unpause-releases/releases) (the table in the [README](https://github.com/GigaRho/unpause-releases/blob/main/README.md) says
which one), then follow the steps for your system below.

## What you need

| | Minimum |
|---|---|
| Windows | Windows 10 or 11, 64‑bit. Unpause uses Microsoft Edge WebView2, which Windows 11 already has; on Windows 10 the installer fetches it if it is missing, so stay online for the first install. |
| macOS | macOS 10.15 or newer, Apple silicon or Intel. |
| Linux | A 64‑bit desktop from 2022 or later (Ubuntu 22.04, Debian 12, Fedora 36 or newer), or a Steam Deck in desktop mode. |
| Space | About 100 MB for Unpause itself; artwork, save backups and captures grow with your library. |
| Games and emulators | Your own. Unpause launches the emulators and stores you already have, and can install a few open‑source emulators from their official releases. |

## Windows

1. Run `Unpause_<version>_x64-setup.exe`.
2. Until Unpause's installers are code‑signed, Windows SmartScreen shows "Windows protected your PC". Choose **More info**,
   then **Run anyway**. (Signed installers are on the way; this step then goes away.)
3. The installer puts Unpause in your Start menu. It installs for your user only and does not need administrator rights.

The `.msi` is the same app for PCs managed by an IT department or installed with a deployment tool.

**Windows handhelds** (ROG Ally, Legion Go, MSI Claw): install the same way in desktop mode. Unpause picks the handheld layout
by itself; Settings › Accessibility › Input map has a Handheld map that puts Options and "hide Unpause" on the back paddles.

## macOS

1. Open `Unpause_<version>_universal.dmg` and drag **Unpause** into **Applications**.
2. Until Unpause is notarized by Apple, the first start says Unpause "cannot be opened because the developer cannot be
   verified". In Finder, **right‑click (or Control‑click) Unpause › Open**, then **Open** again. You only do this once. On
   macOS 15 and newer, open **System Settings › Privacy & Security** and choose **Open Anyway** next to the Unpause line.

## Linux

**Ubuntu, Debian, Mint, Pop!\_OS** — install the `.deb`:

```bash
sudo apt install ./Unpause_<version>_amd64.deb
```

**Fedora, openSUSE** — install the `.rpm`:

```bash
sudo dnf install ./Unpause-<version>-1.x86_64.rpm
```

**Any Linux, or the Steam Deck** — the AppImage runs without installing:

```bash
chmod +x Unpause_<version>_amd64.AppImage
./Unpause_<version>_amd64.AppImage
```

On a Steam Deck, switch to desktop mode, download the AppImage into your home folder, right‑click it › Properties ›
Permissions › **Is executable**, and double‑click it. To see it in Gaming Mode, add it to Steam with **Add a Non‑Steam Game**.

## The first start

Home asks for the folders where your game files are, looks for your emulators, and reads what your stores installed on this
computer (nothing is downloaded and no sign‑in is needed). That's it: pick a game and press Play. If you used Unpause under
its old name, RetrUX, your library, artwork, backups and saved cards move over by themselves on the first start, and the old
folder stays as a backup.

## Where Unpause keeps your things

Your library, settings, artwork, save backups (`backups`) and captures (`captures`) live in one folder:

| System | Folder |
|---|---|
| Windows | `%APPDATA%\app.unpause.desktop` |
| macOS | `~/Library/Application Support/app.unpause.desktop` |
| Linux and Steam Deck | `~/.local/share/app.unpause.desktop` |

The log Unpause writes (Settings › Help & feedback shows its last lines, scrubbed) is in `%LOCALAPPDATA%\app.unpause.desktop\logs`
on Windows, `~/Library/Logs/app.unpause.desktop` on macOS and `~/.local/share/app.unpause.desktop/logs` on Linux.

Passwords and keys you give Unpause for artwork services are not in that folder: they are in your system's credential store
(Windows Credential Manager, the macOS Keychain, the Linux keyring).

Your game files, your emulators' own save folders and your stores are never moved or changed. Before a launch, Unpause
copies that game's saves into its `backups` folder, so a bad save can be undone from the game's Options › Saves & states.

## Uninstalling

- **Windows**: Settings › Apps › Installed apps › Unpause › Uninstall. Your data folder stays unless you tick "Delete the
  application data" in the uninstaller.
- **macOS**: drag Unpause from Applications to the Trash.
- **Linux**: `sudo apt remove unpause`, `sudo dnf remove unpause`, or delete the AppImage.

To remove everything, delete the data folder above as well. Your games and emulators are not touched either way.

## Something went wrong?

See the [FAQ](https://github.com/GigaRho/unpause-releases/blob/main/FAQ.md), or report it in [unpause-feedback](https://github.com/GigaRho/unpause-feedback/issues/new/choose).
If Unpause starts, Settings › Help & feedback fills in the report for you.
