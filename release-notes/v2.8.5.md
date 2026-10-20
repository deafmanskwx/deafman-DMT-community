# DMT 2.8.5 Release Notes

## Track and group colouring

- Choose **TONAL** or **SPECTRAL** in **Tracks > CFG > SETUP** as the default automatic colouring mode for tracks and groups in Tracks and Tweek. Selecting a mode also applies it to the current track and group colouring settings.
- The default is saved across theme changes and app restarts. Existing themes retain their saved colouring schemes when recalled. **TONAL** is the initial default.

## Detailed AutoSetup and macros

- Detailed AutoSetup now provides **Exposure**, **Contrast** and **Saturation** controls for Grade operators, and separate **Red**, **Green** and **Blue** controls for Override operators.
- Custom macro ranges, response curves, inversion and Flip settings are retained when editing, reopening AutoSetup and reloading a theme.
- Override colour channels can be assigned to macros and included in custom colour operators.

## Macro bypass

- Removing a bypassed macro or its last route restores the affected operators to their previous enabled state. Operators that were already disabled stay disabled.
- When several macros bypass the same operator, it stays bypassed until the last bypass is released.

## Library responsiveness

Switching between Library, Tracks and Matrix is more responsive on return visits, and each tab retains its scroll position.
