# DMT 2.7.1 Release Notes

DMT 2.7.1 improves Auto Setup, theme saving and recovery, and editor navigation. It also reduces repeated calculations in the Perception Map and Tracks.

## Additions

- **Cmd–H** opens edit History; **Escape** closes it.
- **Recover Current Edits** can save the edits shown in the current session when the working copy is unreadable. DMT backs up the unreadable file and preserves the previous readable checkpoint.

## Improvements

- Double-clicking a parameter or group search result confirms it, clears the search, and reveals the selection in the editor.
- The Operators browser remembers the choice between **Factory** and **Custom** operators between sessions.
- The Perception Map reuses unchanged curve and calibration calculations and stops updating while the Engine pane is hidden after its initial layout. Tracks reuses unchanged colour analysis when only palette distribution or sensitivity changes.

## Fixes

- **Reset Slider** in Auto Setup now returns the selected slider to its neutral 50% position. Resetting a Z-Depth group also centres the selected sliders when an assignment can no longer update its target, and reports the incomplete update.
- Auto Setup slider positions and colour edits now remain consistent after saving and reopening a theme.
- Aggressive refresh sends the restored theme to Live once. Valid cached themes retain the immediate refresh; newer saved edits invalidate the old cache. Macro edits keep their refresh when the slider is released.
- Simple Auto Setup controls no longer appear in Detailed mode. Switching modes preserves an existing setup if its saved group layout cannot be restored safely.
- Switching themes no longer carries manual colour adjustments from the previous theme into the newly loaded theme. Switching between Detailed and Z-Depth retains the theme's current colours and keeps each mode's saved controls separate.
- Engine colour edits with Autorefresh enabled refresh Live immediately. Queued updates retain their order so an older edit cannot replace a newer one.
- Restoring a saved theme version now keeps its own controls and colour values, even when another snapshot shares its version number. A version with missing data is left untouched rather than partially restored.
- Switching saved versions saves the edits to the version being left first. If that save fails, DMT keeps the current version open. Older flat-layout snapshots with unused Z-Depth groups can also restore and reopen correctly.
- Creating a snapshot reports whether the snapshot and its History were saved. A failed snapshot write leaves the current edits available for retry without adding an unsaved snapshot to the version list.
- Undo and redo after a manual colour edit retain the preceding macro or operator changes.
- Deleting the active theme version chooses a restorable earlier version when available. Deleted snapshots stay removed when an older source is imported again. Renaming one of several snapshots with the same version number now changes the selected snapshot only.
- Removing an active content pack or clearing an unavailable theme preserves pending edits first and stops if they cannot be saved.
- Shift-dragging a Perception Map calibration marker finishes the edit when the drag ends. Closing the panel also finishes any pending edit.
- The § reverse-search shortcut recognizes the focused parameter search field, while left and right arrows continue to move the text cursor.
