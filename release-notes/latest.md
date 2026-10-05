# DMT 2.7.4 Release Notes

This release adds Invert and Vibrance colour operators and makes completed Grade edits refresh Ableton Live immediately when Autorefresh is enabled.

## Added

- **Invert** blends colours towards their RGB negative while preserving transparency. Adjust the amount from 0% to 100%; 0% leaves colours unchanged and 100% fully inverts them. Find it below Blend in the operator menu.
- **Vibrance** boosts muted colours more than already saturated accents, while keeping neutral greys neutral. Its -100% to +100% range also lets you reduce colourfulness; 0% leaves colours unchanged and -100% removes colourfulness. Find it alongside the colour operators.
- Both operators show their amounts as percentages and start at 0%, so adding them leaves the current appearance unchanged.

## Fixes

- Completed Grade edits now refresh Live immediately in Ultra, Aggressive, and Conservative refresh modes, matching the Engine colour controls. Changes made during a drag are sent when the edit is finished, without waiting for the automatic-save timer or causing a second delayed refresh.
