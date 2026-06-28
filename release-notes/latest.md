# DMT Release Notes

Generated from customer-facing implementation ledger entries on or after 2026-06-27.

## At A Glance

- Tracks MAP rules can now be generated from current group colours, updated in place, cleared safely, and restored independently per theme.
- AutoSetup keeps the user's moved sheet position when AutoSetup controls update; the existing sheet presentation, dimmed backdrop, rounded styling hooks, hide/show DMT button, and controls are preserved.
- AutoSetup `#` reverse colour search now stays within the currently selected AutoSetup category (`Simple`, `Detailed`, or `Z-Depth`) instead of jumping across categories to whichever routed match exists elsewhere.
- AutoSetup `#` reverse colour search now jumps to a routed AutoSetup step even when the matching ColourOP-compensated parameter is outside the editor's top-seven colour-search results.

## Editor

### Autosetup Reverse Search Current Category

AutoSetup `#` reverse colour search now stays within the currently selected AutoSetup category (`Simple`, `Detailed`, or `Z-Depth`) instead of jumping across categories to whichever routed match exists elsewhere.

What changed:
- AutoSetup `#` reverse colour search now stays within the currently selected AutoSetup category (`Simple`, `Detailed`, or `Z-Depth`) instead of jumping across categories to whichever routed match exists elsewhere.

Where to find it:
- AutoSetup overlay > selected category tab > `#` > pick a Live UI colour that also has routes or configured steps in another AutoSetup category.

### Autosetup Reverse Search Routed Colourop Match

AutoSetup `#` reverse colour search now jumps to a routed AutoSetup step even when the matching ColourOP-compensated parameter is outside the editor's top-seven colour-search results.

What changed:
- AutoSetup `#` reverse colour search now jumps to a routed AutoSetup step even when the matching ColourOP-compensated parameter is outside the editor's top-seven colour-search results.

Where to find it:
- AutoSetup overlay > `#` > pick a Live UI colour from a ColourOP-processed group whose routed parameter is not present in the editor's capped reverse-search result list.

## AutoSetup

### Autosetup Sheet Position Snapback

AutoSetup keeps the user's moved sheet position when AutoSetup controls update; the existing sheet presentation, dimmed backdrop, rounded styling hooks, hide/show DMT button, and controls are preserved.

What changed:
- AutoSetup keeps the user's moved sheet position when AutoSetup controls update; the existing sheet presentation, dimmed backdrop, rounded styling hooks, hide/show DMT button, and controls are preserved.

Where to find it:
- AutoSetup overlay > hide DMT window title-bar button > drag the sheet header > operate AutoSetup mode/navigation/slider/slot controls.

## Tracks

### MAP Rule Authoring

MAP authoring is now a real round-trip workflow. DMT can convert current group colours into exact rules, refresh generated rules without touching manual rules, and keep each theme's MAP ruleset separate.

What changed:
- Tracks MAP rule mode pills no longer shrink when cycling to `CFG`; `CFG` reserves the same four-character footprint as `AUTO` and `OVER`.

Where to find it:
- Tracks MAP overlay footer, generated MAP rules, CLEAR RULES, and MAP PRESET rulesets.
