# DMT Release Notes

Source: `.agent/IMPLEMENTATION_LEDGER.md` entries on or after the newest published release date 2026-06-15.

These notes intentionally include customer-facing improvements only.

## Settings

### Automatic Update Install Handoff

- Automatic updates can now finish the downloaded update more reliably because DMT leaves the final quit-and-install handoff with the updater.

### Content Updates Local Pack Refresh

- A newly imported manual pack such as `RED_v2.dmt` appears in Settings > Content Updates immediately when the sheet opens, without waiting for a remote manifest sync.
- Where: Import/install a local pack, then open Settings > Content Updates before any background sync runs.

### App Update Restart Handoff

- Downloaded app updates now close open Settings surfaces before restarting, so installation can finish reliably even if Settings was left open.
- Where: Settings window or attached sheet open during downloaded app update installation.
