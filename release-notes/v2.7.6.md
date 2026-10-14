# DMT 2.7.6 Release Notes

This release improves saved theme setups, content updates, and Tracks colour matching.

## Fixes

- **Saved setups** retain their groups, preset selections, and macro assignments when exported, imported, and reopened. Standard and Z-Depth layouts keep their own saved state.
- **Batch copies** retain the latest saved edits after reopening, including when a background history save was still pending.
- **Group renaming** keeps the selected preset and working preset attached to the renamed group.
- **Content updates** retain your setup edits when installing updated packs and preserve the existing managed library when an update cannot be completed. Incomplete imports report a failure instead of appearing successful.
- **Tracks settings** keep a separate saved setup for each colour directive, including analysis-source weights and palette choices.
- **Tracks colour matching** takes the theme's brightness into account and keeps the closest available colour at maximum sensitivity. Disabled swatches and colour-family filters are respected.
- **Tracks background refresh** keeps your global setting when switching themes, colour directives, or presets.
- **Tracks analysis controls** respond more smoothly when dragging across source labels, applying the completed stroke together.
- **Colour operator insertion** clears the active text or colour search and brings the added operator into view, whether added from a menu or dragged from the Library.
