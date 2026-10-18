# DMT 2.8.3 Release Notes

Shift hue selectively by saturation or lightness, and keep manually chosen clip colours when tracks are recoloured.

## Selective Property colour operator

Add **Selective Property** from a group's colour-operator menu or the Library's **Selective** colour-operator filter.

- **Saturation:** shift more saturated colours while leaving muted colours below the threshold unchanged.
- **Luma:** select by perceptual lightness to shift brighter colours while leaving darker colours below the threshold unchanged.
- **Shift:** rotate the selected colours' hue by up to 180 degrees in either direction.
- **Threshold and spread:** drag the solid cursor to set the threshold and the right bracket to adjust the soft spread. Colours at or below the threshold stay unchanged; spread fades the hue shift in above it.

Shift, Threshold and Spread support macro control. Selective Property can also be included in custom colour operators.

## Keep current clip edit colours

In Tracks, open **CFG > CLIP COLOURING**, enable **PRESERVE EDITS** and choose **KEEP CURRENT**. Use it with automatic clip colouring, enabled by **Command-clicking CLP**.

The main clip colour group follows the track colour. Other groups keep their current colours, including later manual edits, across Session and Arrangement clips.

KEEP CURRENT is the initial preservation choice. Existing saved choices are retained, and switching PRESERVE EDITS off and on remembers your last selection. ANALOGOUS, COMPLEMENTARY, LUMA and RAND remain available when you want to recolour the other groups.

PRESERVE EDITS remains off by default. Enable it before recolouring to retain existing colour differences; it cannot recover differences that have already been flattened to one colour.

## Live device update

Replace the **DMT-Tracks Max for Live device** in your Live set with the device included in this version to use KEEP CURRENT.
