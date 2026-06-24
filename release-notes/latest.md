# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-24.

## At A Glance

- Tracks CFG Analysis now trims the expanded panel height, removing unnecessary empty space at the bottom.
- Matrix slot-picker popup padding dashes now sit centered above and below the available theme rows instead of hugging the left edge.
- Theme Library folders no longer auto-expand when pack-version shortcuts, filters, reloads, or selection sync rebuild the tree; expansion changes stay tied to folder-row clicks and the existing Cmd-click bulk folder action.
- Clicking Theme Library pack filters now forces the current filtered folder tree open by default instead of leaving folders collapsed.
- Theme Library now seeds the first loaded library tree fully expanded again, while later pack-version switches and refreshes still preserve the user's explicit folder expansion state.

## Theme Library

### Matrix Slot Popup Padding Dash Alignment

Matrix slot-picker popup padding dashes now sit centered above and below the available theme rows instead of hugging the left edge.

What changed:
- Matrix slot-picker popup padding dashes now sit centered above and below the available theme rows instead of hugging the left edge.

Where to find it:
- Matrix view > click a slot to open the theme picker popup with fewer rows than the fixed picker window.

### Theme Library Expansion User Intent

Theme Library folders no longer auto-expand when pack-version shortcuts, filters, reloads, or selection sync rebuild the tree; expansion changes stay tied to folder-row clicks and the existing Cmd-click bulk folder action.

What changed:
- Theme Library folders no longer auto-expand when pack-version shortcuts, filters, reloads, or selection sync rebuild the tree; expansion changes stay tied to folder-row clicks and the existing Cmd-click bulk folder action.

Where to find it:
- Theme Library browser > collapse pack folders > click an inline `vN` pack-version shortcut, change filters, or trigger a library refresh.

### Theme Library Pack Filter Default Open

Clicking Theme Library pack filters now forces the current filtered folder tree open by default instead of leaving folders collapsed.

What changed:
- Clicking Theme Library pack filters now forces the current filtered folder tree open by default instead of leaving folders collapsed.

Where to find it:
- Theme Library browser > click any pack filter chip (`USR`, `RED`, `3RD`, etc.) after folders were collapsed or after the filter rebuild produced a new visible tree.

### Theme Library Startup Default Expansion

Theme Library now seeds the first loaded library tree fully expanded again, while later pack-version switches and refreshes still preserve the user's explicit folder expansion state.

What changed:
- Theme Library now seeds the first loaded library tree fully expanded again, while later pack-version switches and refreshes still preserve the user's explicit folder expansion state.

Where to find it:
- Launch DMT/open Theme Library; then manually collapse folders and switch pack versions or reload the library.

## Tracks

### CFG Analysis Layout

The expanded Tracks CFG Analysis section now ends at the useful controls instead of leaving an extra blank tail below the final row.

What changed:
- Tracks CFG `ANALYSIS (ADV)` now ends one collapsed-tab height sooner, removing the unnecessary empty space at the bottom of the expanded Analysis section.

Where to find it:
- Tracks view > CFG overlay > ANALYSIS (ADV) expanded section.
