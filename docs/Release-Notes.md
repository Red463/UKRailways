# Release notes: 1.0.0-rc.3

This is a **prerelease candidate** for Minecraft 1.21.1, NeoForge 21.1.251 and
Create 6.0.10. Existing world data and block/item IDs are preserved.

- Prevent repeated junction geometry rebuilding while a schematic preview is
  visible. Previews use ordinary sleepers; placed junctions retain overlap clipping.
- Includes rc.2 UK curve compatibility rendering for Colorwheel shader backends,
  restoring the reproduced missing sleeper detail with shaders still enabled.
- Includes compact gantry-top mainline signal stems and floor mounting plates.
- Includes Greater Anglia train kits/manufacturing, stations, information displays,
  signs, tickets, crossings, gantries, track and road-building features documented
  in the player guide.

Verification includes 480 Java tests, ten track geometry checks, native rendering
regressions and runtime resource checks. This does not establish compatibility
with every modpack, shader combination or schematic. Extended survival,
interactive and full-pack multiplayer acceptance remain separate checks.

Download the ordinary JAR from GitHub Releases. Do not put GitHub's automatic
source ZIP/TAR or an entire release archive in the mods folder.
