# Narrow and Wide Poles

Both sizes use the same eight-sided silver model and accept the same existing pole-mounted railway fittings and road signs.

| Pole | Diameter | Crafting |
|---|---|---|
| Narrow Pole (formerly Traffic Pole) | 2.5 model pixels | Three vertical iron nuggets make six |
| Wide Pole (formerly Railway Pole) | 4 model pixels | Three vertical iron ingots make four |

Stack pole sections normally. Use a railway fitting on the side of an empty section to mount it directly; it retains that section's width. Supported fittings include standard/LED mainline signals, shunt signals, semaphores, crossing lights, speakers, station/platform/wayfinding signs, speed signs, nameplates, crossing notices and Stop Look Listen boards.

Use a configured road sign from the [Roadworks Workbench](Roadworks-Workbench-and-Signs.md) on either pole at the desired height. Several road signs may share a section when their shapes fit. Railway fittings occupy their own section; put further fittings at another height. Existing attachments and occupied sign space cannot be silently replaced.

Create-wrench rotation retains the selected width and settings. Wrench recovery and mining return the matching pole and its owned items once. A stacked semaphore member that borrows its shaft from the assembly does not create an extra pole item.

Existing railway poles and integrated fittings remain Wide. Existing road-sign poles remain Narrow. Item IDs and recipes are unchanged; custom text, variants, links and saved settings are retained. A pole section keeps its own width in a mixed-width column.

The shafts are baked eight-sided meshes, with at most twenty quads per bare pole. Both sizes reuse the existing silver atlas. No extra surface segments or moving shaft renderer are needed.

Actual native views: overview, railway signs, side clearance, road signs on both widths.
