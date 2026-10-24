# Changelog

## v0.2.4 preview — 2026-10-24

The first public binary release of TGWFFLRmodloader.

- Manage supported character packages in a visual library.
- Import native `.TGW` packages and supported legacy patch archives.
- Select one character package per session and launch from the tool.
- Track preparation, game startup, exit handoff, and file restoration.
- Switch between English and Japanese interfaces.
- Use the refined periwinkle/indigo interface with hover and press animations.
- Right-click cards to set preview artwork, export `.TGW`, or delete imported copies to the Recycle Bin.
- Automatically clear the selected mod when its imported copy is deleted.
- Block deletion during active operations, gameplay, or pending recovery.

### Validation and current limits

28 functional checks passed, including patch/recovery and library-removal tests using isolated synthetic game files. English/Japanese menu deletion, selection persistence, and empty-library refresh were also checked with synthetic imports.

End-to-end gameplay and Steam handoff with this launcher have not yet been fully validated. This release uses temporary on-disk patches and requires a restoration period after gameplay. It supports one character package at a time; general stacking and live switching are not implemented.
