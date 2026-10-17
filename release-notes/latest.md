# DMT 2.8.2 Release Notes

Automatic clip colouring can now retain different clip colour groups. This release also adds reverse harmony-directive cycling and screen-picker mode indicators.

## Preserve clip colour groups

In Tracks, open **CFG > CLIP COLOURING** and enable **PRESERVE EDITS**. Use it with automatic clip colouring, enabled by **Command-clicking CLP**.

The most common existing clip colour becomes the main group and follows the track colour. Other colour groups receive the treatment you choose:

- **ANALOGOUS:** lighter and darker shades of the track colour.
- **COMPLEMENTARY:** contrasting hues opposite the track colour.
- **LUMA:** greyscale colours.
- **RAND:** consistent random colours for each group.

Clips that shared a source colour stay together as you recolour Session and Arrangement clips. These choices are saved per theme and stay the same when switching harmony directives. Clip updates with PRESERVE EDITS enabled also run in smaller steps to keep Live responsive.

PRESERVE EDITS is off by default. Enable it before recolouring to retain existing colour groups; it cannot recover differences that have already been flattened to one colour.

## Cycle harmony directives in either direction

**Click** the Tracks harmony-directive label to cycle forwards. **Shift-click** to cycle backwards through ANA, COMP, TEMP, MONO and DESAT.

## Screen-picker modes

The screen picker now shows **P** when finding a parameter from a sampled colour, or **C** when choosing a colour to apply.

## Live device update

Replace the **DMT-Tracks Max for Live device** in your Live set with the device included in this version to use the new clip-colouring controls.
