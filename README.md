# Cider MV Resolver 1.0.0 (Windows x64)

This is the local companion required by the Marketplace version of `MV Immersive` to play configured YouTube videos. It does not include the Cider plugin itself.

## Install

1. Install `MV Immersive` from the Cider Marketplace.
2. Right-click this ZIP and select **Extract All**.
3. Run `install.cmd` from the extracted folder.
4. Restart Cider after the installer reports `installed and running`.

Administrator privileges are not required. The files are installed to `%LOCALAPPDATA%\CiderMvResolver`, and the resolver starts automatically at Windows sign-in. It listens only on local address `127.0.0.1:3060`.

## Update

Extract the new ZIP and run `install.cmd` again. Existing MV mappings are preserved.

## Uninstall

Run `uninstall.cmd`. This also removes saved mappings. Back up `%LOCALAPPDATA%\CiderMvResolver\mv-urls.json` first if you want to keep them.

## Notice

The resolver does not save video files. It obtains temporary playable URLs from configured YouTube links. Use videos in accordance with the applicable rights and service terms.
