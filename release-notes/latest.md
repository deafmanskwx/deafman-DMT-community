# DMT 2.7.0 Release Notes

DMT 2.7.0 adds HELMLAB colour editing and multi-point editing in the Perception Map. It also improves group organisation, version navigation, and the handling of saved themes.

## Additions

- **HELMLAB** is now available alongside OKLCH and HLS, with its own hue, chroma, and lightness controls. Hue and saturation operators also support the space, and undo restores the colour mode with the edit. The HUD shows HELMLAB values for the displayed colour.
- The **Perception Map** supports selecting and moving several curve points together. Shift-drag the background to select points, then drag the selection or press Delete to remove it. Individual points can also be removed with a right-click.

## Improvements

- Perception curves retain their existing control-point layout as brightness changes, avoiding extra points between saved calibrations.
- Collapsing the Perception Map stops its editor from recalculating during colour-slider adjustments, reducing unnecessary work.
- **New Group from Selection** now creates the group inside the source group, keeping the selected parameters within their existing hierarchy.
- Adding or dropping a colour operator into a group from search results now clears the search and reveals the edited group.
- Soloing a macro in Auto Setup expands it and collapses the other macros in that step, while keeping their headers available. Clicking another macro's header transfers Solo to it.
- Matrix pack labels now indicate which packs supply themes to assigned slots.
- Engine settings collapse when switching to a layout that hides the Engine pane.
- In the Library, **Shift–Up/Down** loads the previous or next theme.
- In Library-only view, **Shift–Left/Right** switches between saved versions without first clicking back into the theme list. Text fields retain their normal keyboard behaviour.
- User snapshots and theme revisions can now be deleted while active when a replacement state is available. DMT restores a remaining snapshot or recoverable factory state. Locally deleted revisions stay removed after later imports and saves.

## Fixes

- Fixed an issue that prevented **Custom ColourOPs** from being saved or edited. Saved operators appear in the Custom library and can be reopened in the Macro Editor.
- Switching colour modes or changing **Red to 0°** preserves the current colour instead of reinterpreting its slider values.
- **Clamp** now limits the Chroma slider's range without reducing the stored chroma when hue or lightness changes. The separate **sRGB** setting controls how colours outside the sRGB range are rendered.
- Perception calibration markers remain at the same lightness when hue or chroma changes.
- Editor search confirms the selected group consistently. Arrow keys in text fields no longer trigger unrelated editor navigation or hue changes.
- Distinct groups with the same name survive theme switches and reloads. Loading another theme also clears the previous theme's locked-group filter.
- Renaming an imported-theme folder preserves its themes' working and recovery state. Deleting imported themes also removes their associated recovery data.
- Imports retain separate theme revisions with identical colours instead of discarding them as duplicates.
- **Autorefresh** remembers its setting between sessions, and turning it off cancels a pending automatic save.
- Content updates remember intentionally uninstalled pack versions after restarting DMT, avoiding unwanted downloads.
