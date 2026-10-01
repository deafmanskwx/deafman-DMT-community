# DMT 2.7.3 Release Notes

This hotfix removes the delay before colour-operator and blend edits reach Ableton Live when Autorefresh is enabled.

## Fixes

- Colour-operator slider edits now refresh Live as soon as the slider is released, without waiting for the automatic-save timer.
- Blend-value edits now refresh Live immediately, matching the Engine colour controls. This applies in Ultra, Aggressive, and Conservative refresh modes.
- Rapid consecutive operator and blend edits keep the latest state without a second, delayed refresh from the save timer.
- If saving an edit fails, DMT retains the edited state, reports the error, and keeps the scheduled save retry.
