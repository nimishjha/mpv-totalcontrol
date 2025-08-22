# mpv-totalcontrol

## Manage shaders, equalizer presets, and easy seeking using keyboard shortcuts, without any intrusive GUI elements

## Installation

Place `mpv_totalcontrol.lua` in `~/.config/mpv/scripts`.

## Usage

### Shaders

Organize your shaders in subfolders in `~/.config/mpv/shaders`. Modify the `shaderGroupsByKey` table in the Lua script to map keyboard shortcuts to your shader subfolders. Then in mpv, press that key plus the two-digit index (starting at zero) of the shader file. I.e, if you have key `d` mapped to `Denoise` directory in `~/.config/mpv/shaders`, then pressing `d00` in sequence will load the first shader file (alphabetically sorted) in that subdirectory. `d99` will load the 100th file. Pressing `[` and `]` will switch to the previous and next shader, respectively. Keyboard shortcuts are case sensitive, so if you use all 26 keys and both cases you can manage 5,200 shaders using this script.

Two passes are available. Select pass 1 using `;`, pass 2 using `'`. Clear pass 1 using `:` and pass 2 using `"`.

`F1` to `F12` can be used to save presets. `Shift-F<n>` saves a preset, `F<n>` loads it.

### Equalizer presets

By default, `E` is mapped to equalizer presets (note: case is important). `E00` will load the first preset, `E01` the second, and so on. Use `[` and `]` for the previous and next presets.

### Seeking

Default key is `j`. `j01` will seek to 1 percent, `j27` to 27 percent, and so on. `[` and `]` will decrement/increment the seek position.
