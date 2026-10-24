# Use cases

[Back to the project](README.md) · [Complete user guide](USER_GUIDE.md)

## Play a compatible character replacement

**Situation:** You have a compatible Caius, Noel, Snow, or another supported character package and want to try it without managing installer scripts for every session.

**Workflow:** Import the package, enable its card, and choose **Launch game**. Leave the launcher open while playing. After leaving the game, wait for the tool to restore the original files and report **Ready**.

**Result:** The selected character package is used for that launcher-managed session. Its abilities, animations, and visual behavior depend on the package itself. The launcher does not add features that the package does not contain.

## Keep several characters ready for different sessions

**Situation:** You want to alternate between character packages without searching through downloads each time.

**Workflow:** Import each compatible package into the library. Enable one card before launching. To switch, finish the current session, wait for restoration, enable another card, and launch again.

**Result:** The library retains your imports while the next-session selection changes. Only one character package is enabled at a time; the tool does not merge conflicting packages or switch characters live.

## Record a showcase or make a tutorial

**Situation:** You want a repeatable setup for capturing a character's appearance, abilities, or animations.

**Workflow:** Note the launcher version and package version, enable the intended character, and launch through the tool. Capture your gameplay. When the recording session ends, close the game and let restoration finish before preparing another character.

**Result:** Your capture setup has an explicit package selection and a clear session boundary. In-game effects, missing animations, and other package-specific limitations still need to be documented by the video creator.

## Organize a mod library

**Situation:** You have several imported packages and want the collection to be easier to browse.

**Workflow:** Use the right-click menu to add preview artwork. Remove an unused card with **Delete mod**; its imported copy goes to the Recycle Bin. Keep the original package if you may want to import it again later.

**Result:** The library is easier to scan, and removing a card does not remove your original download or edit the game. Deleting the selected card also clears its selection.

## Export a compatible package for distribution

**Situation:** You created a supported patch package or have permission to distribute one and want to provide it in the native `.TGW` format.

**Workflow:** Import the supported package, add artwork if appropriate, right-click its card, and choose **Export TGW package...**. Select a new filename and verify the exported package by importing it into a separate test setup before distributing it.

**Result:** You get a native `.TGW` package containing the supported mod data and metadata. Export is a packaging workflow; it does not create character replacements from models, animations, or arbitrary game assets. Permission to use this launcher is separate from permission to redistribute someone else's mod.

## Return to an original-game session

**Situation:** You finished a modded session and want to play the original game through Steam.

**Workflow:** Exit the modded game and wait for the launcher to finish restoration and report **Ready**. You can then close the tool and launch through Steam. If the previous session was interrupted, reopen the tool and complete **Settings → Restore original** first.

**Result:** Original files are restored before the next original-game launch. The tool does not restore files instantly at the moment the game window disappears.

## When another tool or workflow is needed

This preview is not designed for arbitrary mod stacking, merging conflicting patches, live character switching, memory injection, multiplayer compatibility guarantees, or creating mods from raw assets. It also cannot reconstruct a deleted full-size base archive from compact recovery data.

Use packages designed for the supported game files, and test the preview with a setup you can restore. Save-file backup is separate from this launcher's patch/recovery workflow.
