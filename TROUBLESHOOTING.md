# Troubleshooting

[Back to the project](README.md) · [User guide](USER_GUIDE.md)

| Symptom | What to check |
| --- | --- |
| The EXE asks for .NET or does not start | Install **.NET 10 Desktop Runtime / Windows / x64** from [Microsoft](https://dotnet.microsoft.com/en-us/download/dotnet/10.0). Extract the ZIP first. |
| The first screen asks for a game folder | Select the folder directly containing `LRFF13.exe`. The tool needs your own Steam game installation. |
| A package is not visible in the import dialog | Use the native `.TGW` filter, or change to the legacy filter for a supported ZIP/`.kflmod` archive. |
| Import says the package is invalid or damaged | Download the package again from its author. Do not rename a ZIP to `.TGW`; changing an extension does not convert a package. |
| Import rejects a duplicate identifier | The identifier already belongs to different or damaged content. Keep the original package and report the exact error. |
| A mod card has no artwork | Right-click it and choose **Set preview image...**. PNG/JPEG images up to 10 MiB are supported. |
| Enabling a card does not change the game immediately | Enable saves the next-session selection. Use **Launch game** for the tool to apply it. |
| Launch is unavailable | Close the running game, finish any operation/recovery, select a valid game folder, and check that the selected mod still exists in the library. |
| Original-file verification fails | The package may target a different game revision, or another mod may already be installed. Restore a previous standalone mod with its own restore procedure. Do not force a mismatched patch. |
| The launcher is waiting after the game exits | It checks briefly for Steam handoffs before restoring originals. Leave it open and wait for **Ready**. |
| Delete mod is disabled | Finish active operations and recovery, and close all `LRFF13` processes. Then reopen the card's context menu. |
| A deleted mod is needed again | Import your original package again, or recover the imported folder from the Windows Recycle Bin. |
| The game or launcher crashed | Close the game, reopen the launcher, and finish **Settings → Restore original** before playing again. |
| Restoration refuses to continue | Preserve the local data/recovery folder. Unexpected external changes, an update, or missing base files may be involved. Do not delete recovery records to dismiss the error. |
| An exported TGW filename already exists | Choose a new filename. The exporter preserves existing files. |
| A card's abilities or effects look wrong in game | Check the package author's known issues and required game version. The launcher does not implement character-specific effects or animations. |

## Data and logs

Normal launches store settings, imported mods, logs, and recovery records in:

```text
%LOCALAPPDATA%\TGWFFLRmodloader
```

Do not remove this folder while recovery is pending. The activity area at the bottom of the window shows recent status. Operation errors may also produce a text file in the local `Logs` subfolder.

## Report an issue

Open an [issue](https://github.com/SawamiKanata/TGWFFLRmodloader/issues) and include:

- Launcher version and Windows version.
- Interface language.
- Mod name, package version, and package source.
- Steps to reproduce and expected behavior.
- Exact error text, plus a relevant screenshot or log excerpt if useful.
- Whether a standalone mod was previously installed and whether recovery is pending.

Review attachments before posting them publicly; remove personal information that is not needed to explain the issue. Do not upload the complete game installation or recovery data unless a maintainer has explained exactly what is needed.
