# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-19.

## At A Glance

- Factory theme backup and restore is stricter and clearer, avoiding invalid Dark/Light pairs and reporting partial restores honestly.
- Theme Editor group creation, nested row alignment, and move-to-group navigation are more predictable when reorganizing parameters.
- Macro ColourOP setup now separates Standard and Z-Depth profile banks while sharing Simple/Detailed macro identities where appropriate.
- AutoSetup Simple mode now follows only manually assigned steps, keeping blank or unassigned steps out of the overlay sequence.
- Tracks analysis profiles now stay in sync with colour directives, theme changes, PER THEME/GLOBAL modes, and app reloads.
- Inline Tracks analysis controls are clearer and safer: editable sources, directive-disabled sources, and paint gestures now behave distinctly.
- Tracks harmony filtering now follows the theme's surface tone and luminance more closely for ANA, TEMP, and MONO directives.
- Tracks MAP rules can now be generated from current group colours, updated in place, cleared safely, and restored independently per theme.
- Theme Editor keyboard preview, group search, and parameter selection now feel more immediate and predictable during grouping work.
- Window layout changes are more responsive, with fewer repeated resize passes and the HUD waveform retained during transitions.

## Theme Library

### Factory Theme Recovery

Factory restore now behaves more like a trustworthy recovery tool: it rejects bad backup pairs, uses clean local Ableton sources when available, and tells the user when only a partial restore is possible.

What changed:
- Factory theme backup/restore now refuses identical Dark/Light pairs and only falls back to clean local Ableton backups, with honest partial-restore messaging when none exist.

Where to find it:
- Settings > Factory Revert and startup factory restore checks.

Notes:
- DMT does not ship Ableton factory assets; users need a clean local Ableton source for unrecoverable factory slots.

## Editor

### Nested Group Editing

Theme Editor group work is now centered around context: new groups appear near the source group, nested rows line up by depth, and move operations reveal the destination instead of leaving stale selection behind.

What changed:
- Theme Editor parameter rows now offer `New Group from...`, starting a reverse-pick workflow for collecting Live UI colour matches into a new group named after the first picked parameter.
- `New Group from...` now creates the picked group as a child of the first picked member's existing non-aggregate group, keeping it visually near the source group under alphabetical sorting.
- Confirming `New Group from...` now reveals the newly created child group in the Theme Editor list instead of leaving the viewport where it was.
- Parameter swatches inside deeper nested Theme Editor groups now move into the nested lock column instead of sitting one nesting step left of their parent group header lock; direct Master Grade child rows keep their previous positioning.
- Moving parameters from the Theme Editor `Move to Group` / `Remove from Group` context menu now collapses selection to the clicked moved parameter and reveals the destination, preventing stale multi-row selection from sticking after nested moves.
- Theme Editor `New Group from Selection`, group-header `Nest Selection (New Group)`, and reverse-pick group creation now land selection on the created group instead of leaving moved parameter rows orange.
- Theme Editor parameter-row group operation is now named `Pick to Group`; Enter accepts each picked/highlighted parameter and reopens the picker for the next parameter, while Escape finishes the group after at least one pick or cancels before any pick.
- Theme Editor `New Group from Selection` no longer leaves old parameter mirror rows painted orange after grouping; group-header and reverse-pick group creation use the same selection/reveal path.

Where to find it:
- Theme Editor parameter and group context menus, including New Group from..., Pick to Group, Move to Group, and Remove from Group.

### Keyboard Preview and Group Navigation

Theme Editor navigation now separates teal preview from committed yellow/orange selection more clearly. Arrow keys can preview groups and parameters, Enter commits the intended target, Escape cancels preview, and group-search scrolling waits until movement actually needs it.

What changed:
- Theme Editor plain Up/Down now previews parameter rows with the teal outline, and Enter commits the preview into the yellow/orange loaded selection.
- Theme Editor scrolling should no longer hitch when the yellow reveal/selection pulse row comes into view after grouping or reveal actions.
- Theme Editor parameter selection and group expand/collapse should respond immediately again instead of waiting on color-cache rebuilds, history persistence, or animated large row diffs.
- Theme Editor parameter row clicks now publish the yellow/orange selected-row state before active color picker sync work, reducing click-to-selection latency.
- Theme Editor arrow-key preview now moves over group headers as well as parameter rows; pressing Enter on a teal-previewed group expands/collapses it, while Enter on a teal-previewed parameter still commits the single parameter selection and turns it yellow.
- Escape now aborts the teal Theme Editor keyboard preview without changing the committed yellow selection, and post-search arrow navigation no longer immediately snaps the revealed group from top alignment to center.
- Theme Editor group-name search no longer recenters the list on the first Down-arrow. The teal preview can move through the first visible group parameters naturally, then the list scrolls once the preview passes the row-distance knee.
- After confirming a group-name search, the revealed group should stay top-aligned while Down-arrow preview moves through the first rows; the list should only begin moving once the teal preview reaches the scroll knee.
- Theme Editor group-search arrow navigation now advances the teal selection one row at a time, keeps the list still until the preview reaches the configured viewport lock point, then scrolls the list on each keypress while the teal selection remains visually locked at that point.
- After the teal Theme Editor preview reaches the configured knee during group-search navigation, reversing direction with Up keeps the selection pinned at the same knee while the editor list scrolls back up.
- Selecting a group entry from Theme Editor search history now jumps directly to the group instead of replaying the group search and waiting for an Enter confirmation.
- Theme Editor arrow-key preview now avoids making every editor row depend on the moving teal preview, so row bodies stay stable while the selection moves and knee-locked scrolling behavior is preserved.

Where to find it:
- Theme Editor search field, group-name search, plain Up/Down preview, Enter confirmation, Escape cancellation, and ordinary parameter row clicks.

## Macros

### Macro Setup Profiles

Macro setup now has clearer profile boundaries. Standard Simple/Detailed workflows can share matching macro identity and edits, while Z-Depth keeps its own isolated setup bank.

What changed:
- Macro ColourOP setup now uses one shared Standard bank for Simple/Detailed and one isolated Z-Depth bank. Simple macros routed to Detailed ColourOP groups appear in Detailed with the same macro identity and shared edits, while Detailed-only macros stay Detailed-only.

Where to find it:
- Macro Editor and AutoSetup setup profiles for Simple, Detailed, and Z-Depth layouts.

## AutoSetup

### Simple Mode Step Navigation

AutoSetup Simple mode now respects manual mapping. The overlay moves through assigned steps only, so intentionally blank steps stay out of the live navigation path.

What changed:
- AutoSetup Simple mode now navigates only manually assigned steps; blank/unassigned Simple steps no longer appear as automatically mapped fallback groups when clicking through the overlay.

Where to find it:
- AutoSetup overlay in Simple mode when only some steps are mapped.

## Tracks

### Analysis Profiles and Directive Memory

Tracks analysis is now treated as an effective profile instead of a flat toggle list. Directive changes, theme changes, PER THEME storage, and reloads all reconcile the active sources without destroying saved user intent.

What changed:
- Tracks analysis now treats the colour directive as the effective analysis gate, removes ChA as an active source, keeps SBG/Dsk brightness authority alive, and avoids the PER THEME first-use equal-weight reset.
- Switching the Tracks colour directive and skipping through themes now refreshes the effective analysis-source set, so non-qualifying parameters are visibly/effectively inactive and the remaining active sliders tune only sources that actually participate.
- GLOBAL analysis mode is freely editable again while PER THEME mode shows the current theme's effective qualified sources; SBG/Dsk now behave as a 50/50 inverse brightness mix, and VU/Trn are default-off optional contributors.
- Each Tracks colour directive now remembers its own analysis source toggle/weight state, including PER THEME storage, after directive switches, theme switches, and app reloads.
- Tracks CFG now defaults and falls back to Spectral Descending for track and group colouring instead of silently reverting to Tonal Descending.
- A new track added as the first member of a managed group now inherits from the nearest real member track below instead of taking the parent group header colour.
- New ordinary tracks inside managed groups no longer use foldable group headers as colour sources, even when Live's first snapshot has not settled the new track's grouped flag or parent relation.
- Tracks now flags already-loaded stale DMT-Tracks devices for replacement after the schema-3 maintenance JS changes, instead of silently accepting an old schema-2 Live device.
- Creating a track in Live now triggers track-colour maintenance immediately, so the new track should inherit from the nearest real group member without waiting for the sensitivity slider or another full sync action.
- New tracks created inside managed groups or inserted between ordinary tracks now use the nearest real existing track colour from the before/after insertion context, instead of keeping Live's parent/default creation colour until a sensitivity/full-sync action.
- Rapidly creating several Live tracks in a row should no longer leave intermediate tracks behind; the bridge now treats one to eight quick creations as one accumulated maintenance delta.
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
- Inline Tracks analysis label click/paint now activates a deselected source and automatically turns off only active colliding sources, keeping non-colliding analysis sources active for a richer harmony feed.
- Inline Tracks analysis buttons now distinguish active, manually inactive, and directive-disabled states; the darker `#202322` state means the source is saved on but currently overridden by the colour directive/profile.
- PER THEME SBG/Dsk analysis weight edits now keep the reciprocal surface source active and persisted after release, and directive-disabled inline analysis sources no longer act as user activation targets.
- Directive-deactivated inline Tracks analysis parameters are now inert: clicking or paint-dragging over them no longer turns them into user-disabled parameters.
- Enabling an eligible inline analysis parameter no longer disables other parameters, and cycling colour directives now immediately refreshes the effective/deactivated analysis state from both the inline directive button and CFG GLOBAL rows.
- GLOBAL analysis mode, with PER THEME off, is freely interactive again; directive filtering no longer makes saved-on sources inert or dark in GLOBAL, while PER THEME still marks directive-filtered saved-on sources as directive-disabled and non-clickable.
- PER THEME analysis rows now keep the intended three states: active contributes, inactive is user-excluded but still toggleable, and disabled is directive-disqualified and inert.
- Pulling or counterbalancing Analysis weight sliders can move contribution weights, including opposing white sliders, but it no longer changes which analysis parameters are directive-disabled.

Where to find it:
- Tracks tuneables inline analysis labels and weight bars.

### Harmony and Luminance Filtering

Tracks harmony selection now pays closer attention to the theme's surface character. ANA, TEMP, and MONO choices are less likely to be pulled toward unrelated accents when surface tone or luminance says otherwise.

What changed:
- ANA now respects reddish/brown theme surfaces as the theme tone instead of accepting opposite blue/cyan accents as analogous matches.
- Higher Tracks filter settings now gravitate toward theme-luminance-compatible swatches for TEMP and MONO instead of narrowing by hue/temperature alone.
- TEMP now reacts to the theme's overall brightness inside the warm/cool family, and ANA no longer lets neutral/low-chroma swatches outrank real analogous hue matches or collapse light neutral themes into accidental LUMA/desat-only selections.
- Track sort order stays unchanged for healthy palettes, but sparse filtered palettes now repeat currently allowed colours so HUE/SPREAD/PING-PONG have visible distribution differences without re-adding filtered swatches.

Where to find it:
- Tracks global colour directives, especially ANA, TEMP, MONO, and higher filter settings.

### MAP Rule Authoring

MAP authoring is now a real round-trip workflow. DMT can convert current group colours into exact rules, refresh generated rules without touching manual rules, and keep each theme's MAP ruleset separate.

What changed:
- The MAP overlay footer now includes `+CONVERT`, which snapshots the current Live group/grouped-child track colours and appends generated exact MAP rules without replacing or altering existing configured rules.
- `+CONVERT` now uses the same footer button sizing/positioning as `+ADD RULE`, and conversion is unavailable unless the active Live bridge is the current bundled DMT-Tracks device.
- Generated `+CONVERT` rules are now named from their captured target tracks, the MAP footer has a two-click `CLEAR RULES` confirmation, and conversion replaces the previous generated batch instead of appending another batch.
- Tracks MAP rules and MAP `PRESET` ruleset snapshots now restore independently per theme, including each theme's active ruleset preset ID.
- Activating Tracks MAP rules now forces the AUTO/MAN/LOCK control into MAN while MAP is active, then restores the user's prior AUTO or LOCK state when MAP is deactivated.
- Clicking the Tracks MAN refresh control while MAP is blue now deactivates MAP and restores the previously captured AUTO/LOCK refresh state.
- Tracks MAP footer now includes `+UPDATE`, which refreshes generated exact MAP rules from the current Live group/grouped-child colours without touching manual rules.
- MAP rule mode pills now cycle visibly through `AUTO`, `OVER`, and `CFG` instead of hiding CFG routing behind cmd-click.
- Tracks now maintains colours for newly observed Live tracks without redistributing existing track colours; new tracks inherit from same-group siblings first, then neighbours, copied/source-like names, MAP rules, Live's current colour, or the palette fallback.
- MAP mode now keeps converted/generated rules in charge when Live tracks are created or renamed: new tracks are added to the nearest generated exact rule and renamed exact targets refresh their stored display name.
- MAP mode now applies the same nearest-member new-track maintenance colour as MAP-off during the creation command, so a newly created child in a managed group is corrected even if the generated exact rule target misses during Live's create/rename window.
- MAP-active track creation maintenance now continues to run even though MAP intentionally displays/stores the Tracks mode as MAN, so new child tracks can receive the nearest-member MAP maintenance correction immediately.
- MAP-active free-floating track creation now inherits from adjacent free-floating tracks instead of being pulled into a nearby grouped generated exact rule.
- MAP-active new-track colour maintenance now continues while the MAP rules overlay is open, so users can keep viewing rules while creating tracks in Live.

Where to find it:
- Tracks MAP overlay footer, generated MAP rules, CLEAR RULES, and MAP PRESET rulesets.

## Improvements

### Window and HUD Responsiveness

Window transitions avoid repeated synchronous resize work when the requested size has not changed, and the HUD keeps the last warm waveform visible while fresh luma work is deferred.

What changed:
- Expanding from Library to Full opens the window frame immediately and no longer remounts/rebuilds the Theme Editor during the frame resize.
- HUD waveform no longer turns off during window layout transitions, so layout changes and Tweak Mode exit can keep showing the last warm waveform raster while fresh waveform luma work is deferred.
- Repeated resized expand/collapse actions no longer re-enter expensive synchronous `setFrame` work when the requested content size is unchanged.
- Focus/window layout changes keep the Theme Editor and Theme Library visually in sync while avoiding the worst redraw stalls from cold layout/cache work.

Where to find it:
- Focus/Tweak layout changes, Library-to-Full expansion, and HUD waveform display during layout transitions.
