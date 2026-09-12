# DMT 2.6.0 Release Notes

DMT 2.6.0 adds reusable custom colour operators and a continuous, brightness-linked Perception Map. It also improves editing and navigation, reduces interface delays, and fixes issues with theme loading, font installation, and history storage.

## Additions

- Macros can now be saved as **Custom ColourOPs** and reused in other theme groups. The Operators browser supports folders, favourites, search, and comments, with drag-and-drop insertion into a group.
- Factory colour operators can also be browsed in the engine pane, with category filters, search, favourites, and drag-and-drop insertion into groups.
- The **Perception Map** now morphs continuously with brightness, replacing the fixed tone bands. Curves can be edited at any lightness, and calibration markers can be moved with Shift-drag or removed. Existing saved curves are carried forward.
- Swatches now have three display sizes, with separate scroll positions retained for History and Memory.
- The new **Clamp** option limits chroma to the usable sRGB range as hue and lightness change.
- Title-bar controls provide direct access to **Always on Top** and the **Ultra, Aggressive, and Conservative** refresh modes. They remain available in the two-pane layout.

## Improvements

- In the Library, **Shift–Up/Down** loads the previous or next theme, and **Shift–Left/Right** switches between saved versions.
- After **Cmd–F**, **Tab** switches between parameter and group search while retaining the query. Pressing **Enter** on a highlighted editor group now selects it as well as expanding or collapsing it.
- Editor group headers now have a **+** menu for adding colour operators. **Move to Group** menus follow the editor's ordering and show nested groups with indentation.
- Clicking a **MACRO** badge opens the Macro Editor. Soloed macros keep their **S** control visible when collapsed.
- **Selective Hue** and **Suppress** can target the selected parameter's hue at the operator's input, making targeting easier when other operators change the displayed colour.
- Auto Setup hides duplicate controls when they are already available in an operator's inline hue strip.
- Colour sliders, Perception Map updates, Tracks sensitivity adjustments, and opening or closing Version View are more responsive.
- Theme and snapshot loads now open Master Grade with the other groups collapsed, reducing initial editor redraws.

## Fixes

- Manual edits and colour operators now distinguish identically named parameters in different groups. Slider positions remain stable when moving between manual edits and operators, including hue adjustments on neutral colours.
- **Pick to Swap** now confirms the clicked search match and provides a **Swap** button for the highlighted result.
- Themes can be loaded by double-clicking in the Library while Version View is open. Clicking the same theme's version indicators again closes Version View.
- Font installation now recognises compatible original-font backups after an Ableton Live update, avoiding unnecessary reinstall prompts.
- History saves no longer create a new recovery backup for every edit, limiting further disk growth while preserving factory state and saved snapshots.
- Expanding and collapsing panels better preserves window position, and focus changes restore the intended layout more reliably, including the return to Library-only view.
- Theme-loading progress bars no longer remain filled after their animation finishes.
