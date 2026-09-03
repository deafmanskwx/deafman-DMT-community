# DMT 2.5.4 Release Notes

DMT 2.5.4 improves Live target reliability for Ableton Live installations on external volumes and keeps editor selection clear when moving from Auto Setup into Expert.

## Fixes

- External Live installations are now detected when a volume is mounted, without requiring DMT to be restarted.
- The selected **Live Target** now remains stable while installations are being discovered and falls back safely when an external volume is disconnected.
- Switching to a different Live installation now clears stale working theme files so they cannot carry over to the newly selected target.
- Opening the Expert layout from Auto Setup now restores the editor's previous selection so multiple group selection frames do not remain visible.
