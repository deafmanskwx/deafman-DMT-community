# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-22.

## At A Glance

- Tracks analysis profiles now stay in sync with colour directives, theme changes, PER THEME/GLOBAL modes, and app reloads.
- Inline Tracks analysis controls are clearer and safer: editable sources, directive-disabled sources, and paint gestures now behave distinctly.
- Tracks harmony filtering now follows the theme's surface tone and luminance more closely for ANA, TEMP, and MONO directives.
- Right-clicking the idle Tracks CLP chip now repeats the last successful clip-colouring action without reopening the selector.
- Tracks MAP saved-preset recall keeps the Presets list open after applying a preset.
- Settings > Content Updates hides stale manifest-only RED rows when newer local family evidence is installed.
- Theme Library selection is fresh again when switching themes, avoiding stale warmed rows or a hidden mounted tree.
- The Theme Editor Rename Group modal text field now uses the fixed `#151515` dark fill, matching the existing Save Group Setup and Save Lock Group modal inputs.

## Theme Library

### Theme Selection Freshness

Theme Library selection now uses the earlier render and cache lifecycle again, so theme switches are based on the visible current library state instead of stale warmed rows.

What changed:
- Theme Library selection uses the pre-merge render/cache lifecycle again, so switching themes is no longer mediated by stale warmed rows or a hidden mounted library tree.

Where to find it:
- Theme Library theme selection and switching between installed themes.

## Editor

### Editor Rename Group Input Background

The Theme Editor Rename Group modal text field now uses the fixed `#151515` dark fill, matching the existing Save Group Setup and Save Lock Group modal inputs.

What changed:
- The Theme Editor Rename Group modal text field now uses the fixed `#151515` dark fill, matching the existing Save Group Setup and Save Lock Group modal inputs.

Where to find it:
- Theme Editor group row context menu > Rename Group; Group Setup menu > Save Group Setup.

## Settings

### Content Updates Version Display

Content Updates now reconciles remote manifest rows with installed local family evidence, so older manifest-only RED versions do not appear as unavailable updates when a newer bundled or restored family version is already present.

What changed:
- Settings > Content Updates no longer shows the stale manifest-only `RED | Light v3` row when installed local evidence shows RED v2 plus a bundled/restored RED v4 family version.

Where to find it:
- Settings > Content Updates pack rows for installed and available content.

## Tracks

### Analysis Profiles and Directive Memory

Tracks analysis is now treated as an effective profile instead of a flat toggle list. Directive changes, theme changes, PER THEME storage, and reloads all reconcile the active sources without destroying saved user intent.

What changed:
- Tracks sensitivity LOCK is now toggled from the colour directive text button with right-click or Cmd-click; the AUTO/MAN button no longer owns that shortcut.
- Tracks CLP grey output now uses the loaded theme's `SurfaceBackground` brightness to choose one fitting Ableton grey, instead of varying grey brightness from each track's palette row.
- Tracks CLP GREY now favors clearer separation by choosing the next brighter Ableton grey after the SurfaceBackground-nearest match, clamping at white when there is no brighter grey.
- PER THEME analysis rows no longer let saved exclusions make sources such as RDF look inactive, and clicking source labels/CFG rows cannot disable sources while PER THEME is on.
- PER THEME directive filtering no longer disables an adjacent yellow `SelectionBackground` beside a bright green `ChosenDefault`; neighbouring source colours remain qualified instead of being treated as incompatible.
- PER THEME analysis controls now remain usable unless the active colour directive can prove a source colour is incompatible; neutral/low-chroma sources and hue-neighbour/counterbalance peers no longer disappear just because they are not the strongest current contributor.
- Analysis weight sliders now behave as variation controls: raising one source reciprocally lowers opposing/counterbalancing sources, and lowering it raises them back, without changing analysis source enablement.
- Sparse cross-hue filtered palettes now keep distinct HUE/SPREAD/PING-PONG track assignments in Live instead of being regrouped back into the same order by the M4L track scheme sorter.

Where to find it:
- Tracks tuneables and CFG analysis controls, including GLOBAL/PER THEME analysis storage and colour directive changes.

### Inline Analysis Editing

The inline Tracks analysis block now separates editable user choices from directive-owned state. Paint gestures, disabled states, and weight edits behave consistently with what is currently allowed to participate.

What changed:
- PER THEME analysis rows now keep the intended three states: active contributes, inactive is user-excluded but still toggleable, and disabled is directive-disqualified and inert.
- Pulling or counterbalancing Analysis weight sliders can move contribution weights, including opposing white sliders, but it no longer changes which analysis parameters are directive-disabled.

Where to find it:
- Tracks tuneables inline analysis labels and weight bars.

### Harmony and Luminance Filtering

Tracks harmony selection now pays closer attention to the theme's surface character. ANA, TEMP, and MONO choices are less likely to be pulled toward unrelated accents when surface tone or luminance says otherwise.

What changed:
- TEMP now reacts to the theme's overall brightness inside the warm/cool family, and ANA no longer lets neutral/low-chroma swatches outrank real analogous hue matches or collapse light neutral themes into accidental LUMA/desat-only selections.
- Track sort order stays unchanged for healthy palettes, but sparse filtered palettes now repeat currently allowed colours so HUE/SPREAD/PING-PONG have visible distribution differences without re-adding filtered swatches.

Where to find it:
- Tracks global colour directives, especially ANA, TEMP, MONO, and higher filter settings.

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
