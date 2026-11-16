# Release notes: 1.0.0-rc.5

This is a **prerelease candidate** for Minecraft 1.21.1, NeoForge 21.1.251 and
Create 6.0.10. Existing world data and block/item IDs are preserved.

- Add automatic sliding station doors with attachable proximity sensors, optional
  chimes and synchronized double-width entrances. Includes redstone operation,
  occupancy protection, separate sensor recovery and original UK-style glass-door
  artwork. See [Automatic Doors](https://github.com/Red463/UKRailways/wiki/Automatic-Doors).
- Cache shader-compatible UK curve geometry on the GPU, avoiding repeated Iris
  vertex preparation while retaining distant sleeper detail. Reduce rail-cap
  vertices, preserve intact junction quads and retain dense same-tick cache entries.
- Prevent repeated junction geometry rebuilding while a schematic preview is
  visible. Previews use ordinary sleepers; placed junctions retain overlap clipping.
- Includes rc.2 UK curve compatibility rendering for Colorwheel shader backends,
  restoring the reproduced missing sleeper detail with shaders still enabled.
- Includes compact gantry-top mainline signal stems and floor mounting plates.
- Includes Greater Anglia train kits/manufacturing, stations, information displays,
  signs, tickets, crossings, gantries, track and road-building features documented
  in the player guide.

This release passes 503 Java tests, 84 server GameTests and three door asset
checks. Native door rendering, paired operation and delayed closure were checked
with six captured views. Existing track rendering fixes are retained. Two-client
door synchronization, real chunk-unload boundaries, subjective chime quality and
shader-pack transparency remain separate acceptance checks; compatibility with
every modpack has not been established.

Download the ordinary JAR from GitHub Releases. Do not put GitHub's automatic
source ZIP/TAR or an entire release archive in the mods folder.
