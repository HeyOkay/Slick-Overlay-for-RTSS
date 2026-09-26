# Slick Overlay

A clean, frosted-glass performance overlay for **RivaTuner Statistics Server (RTSS)**, in four layouts: from a compact single line to a full vertical panel.

[Русская версия](README.ru.md)

![Slick Overlay: all layouts](previews/slick-overlay-all.jpg)

## Layouts

| Layout | Size (px) | Best for |
|---|---|---|
| **Vertical Panel** | 330 × 470 | Full stats in a screen corner |
| **Wide 3 Rows** | 1214 × 122 | Top or bottom edge of the screen |
| **Compact 2x2** | 644 × 234 | Everything, in a small footprint |
| **Single Line** | 2279 × 44 | Minimal strip across the screen |

<details>
<summary>Previews</summary>

**Vertical Panel**

![Vertical Panel](previews/vertical-panel.jpg)

**Wide 3 Rows**

![Wide 3 Rows](previews/wide-3-rows.jpg)

**Compact 2x2**

![Compact 2x2](previews/compact-2x2.jpg)

**Single Line**

![Single Line](previews/single-line.jpg)

</details>

## What it shows

- **FPS:** current, average, 1% low, 0.1% low
- **GPU:** name, load, core clock, memory clock, temperature, VRAM usage
- **CPU:** name, load, clock, package power, temperature, RAM usage
- **Frametime graph** (0–40 ms) and the graphics API in use
- **Driver version**, filled in automatically

All values come from RTSS's built-in hardware monitoring (HAL). MSI Afterburner and HWiNFO are not required.

## Requirements

- RivaTuner Statistics Server 7.3.x with the **OverlayEditor** plugin (it ships with RTSS)
- The **Adderley Bold** font, included in [`fonts/Adderley`](fonts/Adderley) (free, SIL Open Font License 1.1)

## Installation

1. Download `SlickOverlay-vX.Y.Z.zip` from [Releases](../../releases) and unpack it.
2. Install the font: right-click `Adderley_Bold.ttf` and choose **Install for all users**. Restart RTSS if it was running.
3. Copy all `.ovl` and `.png` files to
   `C:\Program Files (x86)\RivaTuner Statistics Server\Plugins\Client\Overlays`
   Every `.ovl` needs the `.png` with the same name next to it.
4. In RTSS, open **Setup → Plugins**, enable **OverlayEditor.dll** and double-click it.
5. Choose **Layouts → Load** and pick a layout.
6. In the main RTSS window, set **On-Screen Display rendering mode** to **Raster 3D** and keep the **OSD zoom** at about **1**.

## Notes

- **AVG / 1% / 0.1%** fill in once you start RTSS benchmark recording (Setup → Benchmark hotkey).
- **Moving the overlay:** drag it in the main RTSS window. Don't drag individual layers in OverlayEditor, or the elements will shift apart.
- **Blurry or pixelated text:** use Raster 3D and OSD zoom 1. Scaling the OSD up stretches the rasterized font.
- **Broken background after replacing a `.png`:** RTSS caches embedded images by file name, so restart RTSS completely (quit it from the tray).
- **Long GPU/CPU name:** edit the `GPU - Value - Name` / `CPU - Value - Name` layer and type a short name instead of the macro.

## Customization

Open the layout in OverlayEditor and double-click a layer.

| What | Where |
|---|---|
| Frametime graph range | Layer `FT - Graph`, tag `<G=Frametime,W,22,1,0,40,0>`: `0,40` is the min/max in ms. Auto-scaling is available in the graph's own settings (the **…** button). |
| Title above the FPS counter | Layer `Header - FPS` |
| Colors | `TextColor` is ARGB hex. Accent beige is `FFD6C6A1`, white is `FFFFFFFF`. |
| Panel opacity | Layer `BG - Frost Base` color alpha, or edit the `.png` |

## Credits

Icons, panel graphics and layouts are original work for this project.

Font: **Adderley** by gorohovskiy / [Dharma Type](http://dharmatype.com), licensed under the [SIL Open Font License 1.1](fonts/Adderley/OFL.txt). It is included unmodified.

## License

Overlays, graphics and docs: [MIT](LICENSE). The font in `fonts/` keeps its own license: [SIL OFL 1.1](fonts/Adderley/OFL.txt).
