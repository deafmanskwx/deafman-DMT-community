# DMT Release Notes

Source: `.agent/IMPLEMENTATION_LEDGER.md` entries on or after the newest published release date 2026-06-15.

These notes intentionally include customer-facing improvements only.

## Theme Library

### Theme Library Live Target Offset

- Theme Library toolbar Live target buttons sit 5pt farther right while retaining their centered overlay behavior.
- Where: Theme Library toolbar > Live installation target buttons.
- Note: This is a visual alignment adjustment only; target selection behavior is unchanged.


## Editor

### Editor Group Setup Menu Right Edge

- The Editor sort header Group Setup menu extends 1px farther to the right without moving its left edge or adjacent controls.
- Where: Editor > sort header > Group Setup menu.
- Note: Build/test execution was not run because this is a one-line visual width nudge and project instructions avoid broader checks unless needed.


## Settings

### Automatic Update Install Handoff

- Automatic updates can now finish the downloaded update more reliably because DMT leaves the final quit-and-install handoff with the updater.

### Content Updates Local Pack Refresh

- A newly imported manual pack such as `RED_v2.dmt` appears in Settings > Content Updates immediately when the sheet opens, without waiting for a remote manifest sync.
- Where: Import/install a local pack, then open Settings > Content Updates before any background sync runs.

### App Update Restart Handoff

- Downloaded app updates now close open Settings surfaces before restarting, so installation can finish reliably even if Settings was left open.
- Where: Settings window or attached sheet open during downloaded app update installation.

### Alert Sound Global Setting

- The save-success alert now uses the macOS Jump sound, and the loudspeaker control lives in Settings > Global as the Alert Sound section between Startup and Software Updates.
- Where: Save-success chime; Settings > Global > Alert Sound.
- Note: The setting label is positive ("Play alert sound") while the persisted preference key remains `muteChime` for compatibility.

### Remote Test Mode Toolbar Override

- Dev Remote Test Mode content scenarios now override a real Software Update availability state while active.
- Where: Software Update still wins when content remote test mode is not active.


## Improvements

### Git Main Worktree Rectification

- Switching the primary workspace to `main` no longer fails because the previous `main` checkout has been moved to a preservation branch.
- Where: Pre-existing generated/untracked workspace artifacts were left untouched.
