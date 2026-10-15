# DMT 2.7.7 Release Notes

This release improves Tracks colour ordering and responsiveness, clip dimming, and saved AutoSetup controls.

## Improvements

- **Tracks colour ordering** applies your HUE, SPREAD, or PING-PONG order and repetition frequency to tracks and group members, including nested groups. Tonal and spectral schemes retain their direction, and Uniform keeps a single colour.
- **Tracks responsiveness** improves when adjusting palettes and applying colours in Live. The DMT-Tracks device picks up commands sooner and avoids repeated track and clip scans; palette adjustments reuse unchanged theme analysis.

## Fixes

- **Group colour directives** update group headers as well as members when switching directives with automatic group colouring enabled.
- **Clip dimming** updates clips when the dimming amount changes, even if their track already has the requested colour. Repeating an unchanged apply avoids unnecessary colour writes.
- **Saved AutoSetup controls** restore the macro slot that matches the saved operator values when reopening themes or restoring snapshots. Controls such as Temperature show the saved selection without changing the theme's colours or custom edits.
