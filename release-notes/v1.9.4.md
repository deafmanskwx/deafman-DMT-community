# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-24.

## At A Glance

- Tracks MAP rules can now be generated from current group colours, updated in place, cleared safely, and restored independently per theme.
- Tracks CFG Analysis now trims the expanded panel height, removing unnecessary empty space at the bottom.
- AutoSetup keeps the user's moved sheet position when AutoSetup controls update; the existing sheet presentation, dimmed backdrop, rounded styling hooks, hide/show DMT button, and controls are preserved.
- AutoSetup `#` reverse colour search now stays within the currently selected AutoSetup category (`Simple`, `Detailed`, or `Z-Depth`) instead of jumping across categories to whichever routed match exists elsewhere.
- AutoSetup `#` reverse colour search now jumps to a routed AutoSetup step even when the matching ColourOP-compensated parameter is outside the editor's top-seven colour-search results.
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

## Editor

### Autosetup Reverse Search Current Category

AutoSetup `#` reverse colour search now stays within the currently selected AutoSetup category (`Simple`, `Detailed`, or `Z-Depth`) instead of jumping across categories to whichever routed match exists elsewhere.

What changed:
- AutoSetup `#` reverse colour search now stays within the currently selected AutoSetup category (`Simple`, `Detailed`, or `Z-Depth`) instead of jumping across categories to whichever routed match exists elsewhere.

Where to find it:
- AutoSetup overlay > selected category tab > `#` > pick a Live UI colour that also has routes or configured steps in another AutoSetup category.

### Autosetup Reverse Search Routed Colourop Match

AutoSetup `#` reverse colour search now jumps to a routed AutoSetup step even when the matching ColourOP-compensated parameter is outside the editor's top-seven colour-search results.

What changed:
- AutoSetup `#` reverse colour search now jumps to a routed AutoSetup step even when the matching ColourOP-compensated parameter is outside the editor's top-seven colour-search results.

Where to find it:
- AutoSetup overlay > `#` > pick a Live UI colour from a ColourOP-processed group whose routed parameter is not present in the editor's capped reverse-search result list.

## AutoSetup

### Autosetup Sheet Position Snapback

AutoSetup keeps the user's moved sheet position when AutoSetup controls update; the existing sheet presentation, dimmed backdrop, rounded styling hooks, hide/show DMT button, and controls are preserved.

What changed:
- AutoSetup keeps the user's moved sheet position when AutoSetup controls update; the existing sheet presentation, dimmed backdrop, rounded styling hooks, hide/show DMT button, and controls are preserved.

Where to find it:
- AutoSetup overlay > hide DMT window title-bar button > drag the sheet header > operate AutoSetup mode/navigation/slider/slot controls.

## Tracks

### MAP Rule Authoring

MAP authoring is now a real round-trip workflow. DMT can convert current group colours into exact rules, refresh generated rules without touching manual rules, and keep each theme's MAP ruleset separate.

What changed:
- Tracks MAP rule mode pills no longer shrink when cycling to `CFG`; `CFG` reserves the same four-character footprint as `AUTO` and `OVER`.

Where to find it:
- Tracks MAP overlay footer, generated MAP rules, CLEAR RULES, and MAP PRESET rulesets.

### CFG Analysis Layout

The expanded Tracks CFG Analysis section now ends at the useful controls instead of leaving an extra blank tail below the final row.

What changed:
- Tracks CFG `ANALYSIS (ADV)` now ends one collapsed-tab height sooner, removing the unnecessary empty space at the bottom of the expanded Analysis section.

Where to find it:
- Tracks view > CFG overlay > ANALYSIS (ADV) expanded section.
