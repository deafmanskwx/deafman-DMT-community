# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-23.

## At A Glance

- Right-clicking the idle Tracks CLP chip now repeats the last successful clip-colouring action without reopening the selector.
- Tracks MAP saved-preset recall keeps the Presets list open after applying a preset.
- Tracks CFG Analysis now trims the expanded panel height, removing unnecessary empty space at the bottom.
- Settings > Content Updates hides stale manifest-only RED rows when newer local family evidence is installed.
- Theme Library selection is fresh again when switching themes, avoiding stale warmed rows or a hidden mounted tree.
- Matrix slot-picker popup padding dashes now sit centered above and below the available theme rows instead of hugging the left edge.
- Theme Library folders no longer auto-expand when pack-version shortcuts, filters, reloads, or selection sync rebuild the tree; expansion changes stay tied to folder-row clicks and the existing Cmd-click bulk folder action.
- Theme Library now seeds the first loaded library tree fully expanded again, while later pack-version switches and refreshes still preserve the user's explicit folder expansion state.

## Theme Library

### Theme Selection Freshness

Theme Library selection now uses the earlier render and cache lifecycle again, so theme switches are based on the visible current library state instead of stale warmed rows.

What changed:
- Theme Library selection uses the pre-merge render/cache lifecycle again, so switching themes is no longer mediated by stale warmed rows or a hidden mounted library tree.

Where to find it:
- Theme Library theme selection and switching between installed themes.

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

### Theme Library Startup Default Expansion

Theme Library now seeds the first loaded library tree fully expanded again, while later pack-version switches and refreshes still preserve the user's explicit folder expansion state.

What changed:
- Theme Library now seeds the first loaded library tree fully expanded again, while later pack-version switches and refreshes still preserve the user's explicit folder expansion state.

Where to find it:
- Launch DMT/open Theme Library; then manually collapse folders and switch pack versions or reload the library.

## Settings

### Content Updates Version Display

Content Updates now reconciles remote manifest rows with installed local family evidence, so older manifest-only RED versions do not appear as unavailable updates when a newer bundled or restored family version is already present.

What changed:
- Settings > Content Updates no longer shows the stale manifest-only `RED | Light v3` row when installed local evidence shows RED v2 plus a bundled/restored RED v4 family version.

Where to find it:
- Settings > Content Updates pack rows for installed and available content.

## Tracks

### CLP Replay Shortcut

Tracks CLP now remembers the last successful clip-colouring function and scope for quick repeat use. RANGE still opens the palette selector so stale range choices are not replayed accidentally.

What changed:
- Right-clicking the idle Tracks `CLP` chip now repeats the last successfully applied clip-colouring function and ALL/SEL scope; RANGE reopens the normal palette range selector instead of replaying stale indices.

Where to find it:
- Tracks CLP chip right-click replay, ALL/SEL scope, and RANGE palette selection.

### MAP Preset Recall

MAP preset recall now stays in the preset browser after applying a saved ruleset, making it easier to compare or apply another preset without reopening the list.

What changed:
- Tracks MAP saved-preset recall now keeps the Presets list open instead of returning to the keyword rules list.

Where to find it:
- Tracks MAP overlay Presets list and saved ruleset rows.

### CFG Analysis Layout

The expanded Tracks CFG Analysis section now ends at the useful controls instead of leaving an extra blank tail below the final row.

What changed:
- Tracks CFG `ANALYSIS (ADV)` now ends one collapsed-tab height sooner, removing the unnecessary empty space at the bottom of the expanded Analysis section.

Where to find it:
- Tracks view > CFG overlay > ANALYSIS (ADV) expanded section.
