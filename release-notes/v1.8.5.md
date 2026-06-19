# DMT Release Notes

Source: `.agent/IMPLEMENTATION_LEDGER.md` entries on or after the newest published release date 2026-06-19.

These notes intentionally include customer-facing improvements only.

## Theme Library

### Livesync Factory Backup Fallback

- Factory theme backup/restore now refuses identical Dark/Light pairs and only falls back to clean local Ableton backups, with honest partial-restore messaging when none exist.
- Where: DMT startup LiveSync detection; Settings/DRM Factory Revert.
- Note: DMT does not ship Ableton factory assets; users need a clean local Ableton install/source for unrecoverable factory slots.


## Editor

### Editor Reverse Pick Child Group

- `New Group from...` now creates the picked group as a child of the first picked member's existing non-aggregate group, keeping it visually near the source group under alphabetical sorting.
- Where: Theme Editor parameter context menu > `New Group from...`; pick one or more Live UI colours; press Enter to create the group.

### Editor Reverse Pick Group Scroll Reveal

- Confirming `New Group from...` now reveals the newly created child group in the Theme Editor list instead of leaving the viewport where it was.
- Where: Theme Editor parameter context menu > `New Group from...`; press Enter after one or more reverse picks.

### Editor Nested Group Row Alignment

- Parameter swatches inside deeper nested Theme Editor groups now move into the nested lock column instead of sitting one nesting step left of their parent group header lock; direct Master Grade child rows keep their previous positioning.
- Where: Theme Editor expanded nested groups, especially groups created under an existing group by `New Group from...`.

### Editor Move To Group Selection Stick

- Moving parameters from the Theme Editor `Move to Group` / `Remove from Group` context menu now collapses selection to the clicked moved parameter and reveals the destination, preventing stale multi-row selection from sticking after nested moves.
- Where: Theme Editor parameter row context menu > `Move to Group` or `Remove from Group`, especially when moving into a nested group after mixed parameter/group selection.
- Note: The teal filter-result frame remains driven by `searchHighlightIndex` and `resolvedVisibleSearchResultID` still prioritizes highlighted result, then active selected parameter, then selected IDs, then first visible result.

### Editor Nested Group Row Alignment Cascade

- Theme Editor child rows now cascade cleanly with nested group depth: each nested group advances swatches/operators one 16 pt step from its parent's child-row column.
- Where: Theme Editor expanded nested groups, especially child groups created under `Selection` or other Master Grade descendants.


## Macros

### Macro Mode Colourop Profile Recall

- Macro ColourOP setup now uses one shared Standard bank for Simple/Detailed and one isolated Z-Depth bank. Simple macros routed to Detailed ColourOP groups appear in Detailed with the same macro identity and shared edits, while Detailed-only macros stay Detailed-only.


## AutoSetup

### Autosetup Simple Manual Navigation Only

- AutoSetup Simple mode now navigates only manually assigned steps; blank/unassigned Simple steps no longer appear as automatically mapped fallback groups when clicking through the overlay.
- Where: AutoSetup overlay in Simple mode with only some Simple steps mapped, including holes such as only Step 3 assigned.
- Note: The investigated stale-theme-cache hypothesis did not explain the reproduced symptom; the failing proof showed navigation-time fallback produced `totalGroups == 3` when only one Simple step was intentionally assigned.


## Tracks

### Tracks Directive Effective Analysis Sources

- Switching the Tracks colour directive and skipping through themes now refreshes the effective analysis-source set, so non-qualifying parameters are visibly/effectively inactive and the remaining active sliders tune only sources that actually participate.
- Where: Tracks GLOBAL directive cycling/CFG selection; theme navigation while Tracks is visible, including MAN mode; inline/CFG analysis toggles and weight bars.
- Note: The effective profile remains non-destructive: saved user exclusions/weights are preserved, while directive/theme saturation gates determine what is active right now.

### Tracks Analysis Global Vs Effective Refinement

- GLOBAL analysis mode is freely editable again while PER THEME mode shows the current theme's effective qualified sources; SBG/Dsk now behave as a 50/50 inverse brightness mix, and VU/Trn are default-off optional contributors.
- Where: Tracks inline analysis rows, CFG > ANALYSIS (ADV), PER THEME storage switch, SBG/Dsk weight sliders, theme/directive changes with saturated or low-chroma accent sources.
- Note: The profile still keeps directive filtering non-destructive: user exclusions/weights are saved preferences, while per-theme effective activation is recomputed from directive, saturation, collision, and source contribution.

### Tracks Analogous Surface Tone Anchor

- ANA now respects reddish/brown theme surfaces as the theme tone instead of accepting opposite blue/cyan accents as analogous matches.
- Where: Tracks ANA directive, theme navigation while PER THEME/effective analysis is visible, and harmony distance scoring for swatch selection.

### Tracks Analysis Paint Collision Replacement

- Inline Tracks analysis label click/paint now activates a deselected source and automatically turns off only active colliding sources, keeping non-colliding analysis sources active for a richer harmony feed.
- Where: Tracks tuneables inline analysis source labels; click or drag-paint over inactive analysis sources.

### Tracks Analysis Directive Disabled Button State

- Inline Tracks analysis buttons now distinguish active, manually inactive, and directive-disabled states; the darker `#202322` state means the source is saved on but currently overridden by the colour directive/profile.
- Where: Tracks tuneables inline analysis source labels when PER THEME/current directive filtering suppresses a source that remains enabled in user intent.

### Tracks Per Theme Analysis Submit To Directive

- PER THEME SBG/Dsk analysis weight edits now keep the reciprocal surface source active and persisted after release, and directive-disabled inline analysis sources no longer act as user activation targets.
- Where: Tracks tuneables inline analysis weight bars and analysis labels in PER THEME mode, especially SBG/Dsk and directive-filtered accent sources.
- Note: CFG overlay toggles were not changed; directive-filtered inline rows are still visibly represented by the directive-disabled state.

### Tracks Directive Deactivated Inline Toggle Inert

- Directive-deactivated inline Tracks analysis parameters are now inert: clicking or paint-dragging over them no longer turns them into user-disabled parameters.
- Where: Tracks tuneables inline analysis labels and weight bars when the current colour directive/profile filters an otherwise enabled source.
- Note: CFG overlay toggles remain unchanged; directive ownership is enforced only for the inline analysis block requested here.

### Tracks Analysis Toggle Directive Refresh

- Enabling an eligible inline analysis parameter no longer disables other parameters, and cycling colour directives now immediately refreshes the effective/deactivated analysis state from both the inline directive button and CFG GLOBAL rows.
- Where: Tracks tuneables inline analysis label click/paint, inline directive cycling, CFG > GLOBAL directive rows.

### Tracks Global Analysis Interaction Free

- GLOBAL analysis mode, with PER THEME off, is freely interactive again; directive filtering no longer makes saved-on sources inert or dark in GLOBAL, while PER THEME still marks directive-filtered saved-on sources as directive-disabled and non-clickable.
- Where: Tracks tuneables inline analysis labels and weight bars when PER THEME is toggled off/on.

### Tracks Directive Luminance Filtering

- Higher Tracks filter settings now gravitate toward theme-luminance-compatible swatches for TEMP and MONO instead of narrowing by hue/temperature alone.
- Where: Tracks global colour directives, sensitivity slider/filtering, theme navigation/reanalysis.
- Note: No Max/M4L palette fallback or write-path logic changed, preserving the filtered-index constraints from prior Tracks fixes.

### Tracks Analysis Directive Persistence

- Each Tracks colour directive now remembers its own analysis source toggle/weight state, including PER THEME storage, after directive switches, theme switches, and app reloads.
- Where: Tracks tuneables/CFG analysis toggles, GLOBAL colour directive cycling, PER THEME/GLOBAL analysis storage, theme switching, and palette state load/save.
