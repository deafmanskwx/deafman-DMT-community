# DMT 2.7.5 Release Notes

This release improves colour swapping, reverse search, and AutoSetup navigation.

## Fixes

- **Colour swapping** now exchanges the displayed colours, including transparency, when colour operators are active. Existing operators and group locks are preserved, and the swap can be undone as one change. If a swap cannot be completed, DMT explains why and leaves both colours unchanged.
- **Reverse search** now works while either the Colours or Blend search field has focus. Starting reverse search from Blend returns to Colours and opens the colour picker.
- **AutoSetup macro selection** now follows the saved step when loading another theme, including an intentionally empty step. The panel updates without retaining the previous theme's selection.
- The Engine status bar now remains fully visible after returning from AutoSetup.
