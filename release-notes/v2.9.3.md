# DMT 2.9.3 Release Notes

In Tracks, you can capture a Live set’s group colours, try another scheme in MAP, and return to the captured colours. Quick Start now adapts its lessons to the controls visible in your window.

**If you use Tracks, replace the DMT-Tracks Max for Live device in your set after updating.** Drag the new device from the **amxd** handle in Tracks to use the updated MAP modes and palette sorting.

## MAP rules

- **CONVERT** captures the Live colours of group headers and members, including nested groups. Converted rules start in **AUTO**. Choose **OVER** to try a manual swatch, then switch back to **AUTO** to restore the capture. Returning to **OVER** recalls your edit. Use **UPDATE** when you want the current Live colours to become the new capture.
- Set a group header to **CFG** to colour the header and its **AUTO** members using the current group settings in **Options**. Members set to **OVER** keep their manual swatches. Changes in Options reapply while MAP is active.
- Click a rule to select it. **COL** and **EXP** keep that selection as you collapse and expand the list. Selecting a group header highlights its group outline. Selecting a member highlights just its row, even in a nested group.

## Tracks

- With **AUTO** and **ALL** active, **PING-PONG** moves across the selected **FACTORY** or **GRADED** palette one row at a time, reversing direction on alternate rows and skipping disabled swatches. **SPREAD** starts at the first enabled swatch and picks the colour farthest from those already chosen. If two colours are equally far away, their order in the grid decides which comes next.
- In **Options**, use the **ENABLED** or **DISABLED** row under **TRACK COLOUR** or **GROUP COLOUR** to toggle colouring. With **AUD** or **MID** on, choose **LINK TO TRACK** to make groups follow the track colour scheme and **UNIFORM** setting. Unlink to restore your separate group settings. You can assign these controls to any of the four shortcut slots.
- For horizontal clip ranges, choose **LINEAR**, **REVERSE** or **CYCLE** in **CFG > CLIP SORT ORDER**. Existing clip sort shortcuts still work.

## Quick Start, swatches and help

- Start Quick Start from **Settings** while you’re working in Tracks. The tour keeps the Tracks panel open at your current window size.
- When a Quick Start lesson needs a loaded theme, click **Choose a theme** and double-click a theme in the Library. The tour resumes at the same lesson when the theme loads. Choose **Continue without a theme** to visit the remaining controls that work without one.
- The source and destination swatches show transparent colours over a checkerboard, so you can see the opacity of the original colour alongside your edit.
- Search the in-app help for **custom operator** or **Custom OP** to find the guide to saving a single-group colour macro as a reusable operator. The shortcut reference, manual and UI Atlas now use the same terms. The save command is **Save as Custom ColourOP**.
