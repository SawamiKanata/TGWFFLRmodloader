# User guide

[Back to the project](README.md) · [Use cases](USE_CASES.md) · [Troubleshooting](TROUBLESHOOTING.md)

## 1. Download and install

1. Open the project's [Releases](https://github.com/SawamiKanata/TGWFFLRmodloader/releases).
2. Select the version you want and download its **`TGWFFLRmodloader-v<VERSION>-win-x64.zip`** asset. The current preview is **v0.2.4**.
3. Extract the entire archive. Do not run the program from inside the ZIP.
4. Install **.NET 10 Desktop Runtime, Windows x64** from [Microsoft](https://dotnet.microsoft.com/en-us/download/dotnet/10.0) if it is not already installed. The SDK and the plain console runtime are not required substitutes for the Desktop Runtime.
5. Run `TGWFFLRmodloader.exe` from the extracted folder.

You can keep the launcher outside the game directory. The first launch asks you to select the folder containing `LRFF13.exe`. Select that folder, rather than the executable itself or the parent `steamapps` directory. Steam's **Browse installed files** option can help locate it.

The program does not request administrator elevation. Both the game directory and the tool's local data directory must be writable by your Windows account.

## 2. Prepare the game

- Start Steam and close any running instance of LIGHTNING RETURNS.
- Use original game files matching the chosen mod package.
- If you previously installed a standalone character mod, restore it using that package's own `Restore.cmd` before using this launcher. Its backups and this tool's recovery data are separate.
- Avoid applying another patcher to the same game files during a launcher-managed session.

A mismatch is handled as a compatibility error. Do not rename files or bypass verification to force an incompatible package to load.

## 3. Import a mod

1. Open **Mods**.
2. Choose **Import mod** at the upper right.
3. Select a native `.TGW` package. Do not extract it or rename it to ZIP.
4. Wait for the import to finish. A card will show the package name, author, version, description, and preview image if supplied.

For a supported legacy ZIP or `.kflmod` archive, select the legacy-package filter in the file picker. The launcher imports compatible metadata and patch data; it does not run installer scripts bundled with an archive.

Character packages are distributed separately from the launcher. Import support does not imply that every mod archive or every game revision is compatible.

## 4. Choose a character

Choose **Enable** on the card you want to use. The selected card is marked **Enabled**. Choosing another card replaces the selection, because only one character package is active at a time.

To clear the selection, click the selected card's **Enabled** button. Selection changes only save a preference; game files are patched when you launch a modded session from the tool.

Do not change characters during a running session. Exit, wait for restoration, and then choose the next character.

## 5. Launch and finish a session

1. Confirm the desired card is enabled.
2. Choose **Launch game**.
3. Follow the preparation panel. It shows the current operation, filename where available, progress, and elapsed time.
4. Keep the launcher open or minimized while playing.
5. Exit the game normally.
6. Wait for the launcher to finish its exit checks and restore the original files.
7. Once the status returns to **Ready**, you can close the tool, launch an original-game session through Steam, or choose a different character.

A percentage refers to the file check currently being measured, rather than the complete startup. During game startup and Steam handoffs, the progress bar may animate without a percentage.

After the game closes, the tool allows a short grace period of up to 15 seconds to detect Steam restarts before restoration. Do not start another game session until restoration completes.

## 6. Manage the library

### Set preview artwork

Right-click a card and choose **Set preview image...**. Select a PNG or JPEG image up to 10 MiB. The image is saved with the imported copy in the library; the original package is not changed.

Cards without artwork show a labeled placeholder. The launcher does not fetch screenshots automatically.

### Export a package

Right-click a card and choose **Export TGW package...**. Choose a new `.TGW` filename. The tool preserves existing destination files, so select another filename if one already exists.

This is useful for converting a supported legacy import into a native `.TGW` package or exporting an imported package after adding artwork. Obtain permission from the original author before redistributing their mod content.

### Delete an imported mod

Right-click the card and choose **Delete mod**. The imported folder is moved to the Windows **Recycle Bin**, and the card disappears from the library. If it was the selected mod, the saved selection is cleared.

The original `.TGW`/ZIP download, other imported mods, game files, and recovery records are kept. To use the mod again, import the original package again. The deleted imported folder can also be recovered through the Recycle Bin.

Deletion is unavailable while a file operation is active, while the game is running, or while recovery is pending. Finish the session or recovery first. Deletion remains available even if a game folder has not been selected.

## 7. Settings

- **Language:** choose English or Japanese. The selection is saved automatically.
- **Game folder:** change the folder containing `LRFF13.exe` when no session or recovery is active.
- **Session recovery:** use **Restore original** when the tool reports an unfinished session.
- **Replay startup animation:** replay the opening sequence without launching the game.

The **Information** page shows the developer, version, project information, and GitHub link.

## 8. Recover after a crash or interruption

1. Close every running instance of LIGHTNING RETURNS.
2. Reopen the launcher.
3. Open **Settings** and choose **Restore original** when recovery is pending.
4. Keep the launcher open until restoration succeeds and the status returns to **Ready**.
5. Only then launch the game again through Steam or begin another modded session.

The local data folder is `%LOCALAPPDATA%\TGWFFLRmodloader`. It contains settings, imported mods, logs, and recovery data. **Keep this folder while a session needs recovery.** Deleting the launcher EXE does not perform restoration.

If verification fails, preserve the recovery data and error text. Another modification, a game update, or missing base files may require attention before restoration can proceed. Compact recovery data cannot recreate an entire deleted base archive or executable. See [Troubleshooting](TROUBLESHOOTING.md).

## 9. Update or remove the launcher

Before updating or removing the tool, close the game and finish any pending restoration.

To update, extract the new official release to a folder and run its EXE. Normal launches use the same per-user local data folder, so the imported library and settings are separate from the EXE folder.

To remove the launcher, delete its extracted application folder after the status is **Ready**. Keep local data if you want to retain the library and settings. Remove that local data only after confirming there is no pending recovery.

## 10. Checksums

Releases provide `SHA256SUMS.txt`. You can compare a downloaded archive in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\TGWFFLRmodloader-v0.2.4-win-x64.zip
```

Compare the resulting hash with the matching filename in the checksum file. Download the archive from this project's official release page.
