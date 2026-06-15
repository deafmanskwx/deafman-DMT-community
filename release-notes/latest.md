# DMT Release Notes

Source: `.agent/IMPLEMENTATION_LEDGER.md` entries after the newest published release dated 2026-06-14.

These notes intentionally include customer-facing improvements only.

## Theme Library

### Matrix Slot Assignment Persistence

- Matrix slot labels and injected-slot markers now survive quitting and relaunching DMT instead of returning to `Unassigned`.
- Where: Matrix routing picker assignment, editor `Inject to Matrix Slot`, and Matrix slot clear confirmation.
- Note: Matrix persistence records DMT's UI assignment metadata; it does not reapply or rewrite Ableton default theme files on launch.

### Routing Library Filter Decoupling

- Matrix routing no longer loses themes or preselects a pack because the Theme Library browser has active pack filters.
- Where: Theme Library Matrix routing popup, slot click pack selection, and drag/slot theme lookup.


## Settings

### Automatic Update Install Handoff

- Automatic updates can now finish the downloaded update more reliably because DMT leaves the final quit-and-install handoff with the updater.

### Content Updates Local Pack Refresh

- A newly imported manual pack such as `RED_v2.dmt` appears in Settings > Content Updates immediately when the sheet opens, without waiting for a remote manifest sync.
- Where: Import/install a local pack, then open Settings > Content Updates before any background sync runs.
