# Changelog

## [1.0.1] - 2026-09-26

- GPU field changed from memory clock to GPU power draw (bolt icon, watts), matching the CPU power field
- Frametime label now also shows the current frametime value in ms, next to the graph and API
- Single Line layout widened slightly to fit the new frametime value without crowding the graph

## [1.0.0] - 2026-09-26

First release.

- Four layouts: Vertical Panel, Wide 3 Rows, Compact 2x2, Single Line
- FPS (current / avg / 1% low / 0.1% low), GPU and CPU stats, RAM, VRAM
- Frametime graph (0–40 ms) with the graphics API, driver version
- Frosted-glass background with rounded corners; original line icons
- Adderley Bold font (SIL OFL 1.1) bundled in `fonts/` and in the release zip, tuned for Raster 3D rendering
