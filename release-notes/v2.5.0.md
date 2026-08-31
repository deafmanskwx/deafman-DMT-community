# DMT 2.5.0 Release Notes

DMT 2.5.0 updates Auto Setup, Perception editing, colour operators and theme refresh behaviour.

## Auto Setup

- Auto Setup now uses a revised Expert layout with direct navigation between its areas.
- Tracks can be opened without changing the current position in the Library.
- Hue strips can now be adjusted alongside the existing group, macro and depth controls.
- Auto Setup presentation and window changes have been adjusted to reduce delays, including with larger theme libraries.
- In-app guidance now explains how Auto Setup works with the Perception Map.

## Perception Editing

- A Perception setup can now be previewed while editing before it is applied to the theme.
- The compensated-only HUD view shows colours after appearance compensation.
- Fixed issues with dark-theme compensation and editing Perception curves.
- HLS hue controls and their displayed gradients now remain aligned across the editing range.

## Colour Operators

- Added the **Selective Hue** operator, which limits adjustments to a selected hue range.
- Added the **Suppress** operator, which reduces the effect of selected colours.
- Operator selections are stored per theme.
- Grade changes remain available in the undo history.

## Ableton Refresh and Library State

- Added an Ultra refresh option for cases where the standard Ableton theme refresh does not update the displayed theme.
- Ableton refresh now uses rendered theme artifacts.
- Fixed mirror-source and version selection when switching between related themes.
- Library availability and Auto Setup readiness now update sooner after content changes.
