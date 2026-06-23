# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-23.

## At A Glance

- Right-clicking the idle Tracks CLP chip now repeats the last successful clip-colouring action without reopening the selector.
- Tracks MAP saved-preset recall keeps the Presets list open after applying a preset.
- Settings > Content Updates hides stale manifest-only RED rows when newer local family evidence is installed.
- Theme Library selection is fresh again when switching themes, avoiding stale warmed rows or a hidden mounted tree.

## Theme Library

### Theme Selection Freshness

Theme Library selection now uses the earlier render and cache lifecycle again, so theme switches are based on the visible current library state instead of stale warmed rows.

What changed:
- Theme Library selection uses the pre-merge render/cache lifecycle again, so switching themes is no longer mediated by stale warmed rows or a hidden mounted library tree.

Where to find it:
- Theme Library theme selection and switching between installed themes.

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
