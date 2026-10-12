# Cider MV Resolver 1.2.0

This is the local companion required by the Marketplace version of `MV Immersive` to play configured YouTube videos. It does not include the Cider plugin itself.

Version 1.2.0 adds Linux and macOS builds. The Windows build works the same as 1.1.0.

## Downloads

| File | Platform |
| --- | --- |
| `Cider-MV-Resolver-1.2.0-Windows-x64.zip` | Windows (x64) |
| `Cider-MV-Resolver-1.2.0-Linux-x64.zip` | Linux (x64) |
| `Cider-MV-Resolver-1.2.0-macOS-arm64.zip` | macOS (Apple Silicon: M1 or later) |
| `Cider-MV-Resolver-1.2.0-macOS-x64.zip` | macOS (Intel) |

`SHA256SUMS.txt` lists the checksums of the ZIP files.

## Install

1. Install `MV Immersive` from the Cider Marketplace.
2. Extract the ZIP for your platform.
3. Run the installer from the extracted folder:
   - **Windows:** run `install.cmd`.
   - **Linux / macOS:** open a terminal in the folder and run `sh install.sh`.
4. Restart Cider after the installer reports `installed and running`.

Administrator privileges are not required. The resolver starts automatically at sign-in and listens only on local address `127.0.0.1:3060`.

| Platform | Install location |
| --- | --- |
| Windows | `%LOCALAPPDATA%\CiderMvResolver` |
| Linux | `~/.local/share/CiderMvResolver` |
| macOS | `~/Library/Application Support/CiderMvResolver` |

### macOS security

The macOS builds are not notarized by Apple. `install.sh` removes the download quarantine flag and applies an ad-hoc signature so that macOS allows the resolver to run. If macOS still blocks it, open **System Settings > Privacy & Security** and allow `CiderMvResolver`.

## Update

Extract the new ZIP and run the installer again. Existing MV mappings are preserved.

## Uninstall

Run `uninstall.cmd` (Windows) or `sh uninstall.sh` (Linux / macOS). This also removes saved mappings. Back up `mv-urls.json` in the install location first if you want to keep them.

## Notice

The resolver does not save video files. It obtains temporary playable URLs from configured YouTube links. Use videos in accordance with the applicable rights and service terms.

Bundled yt-dlp: version 2026.08.19.
