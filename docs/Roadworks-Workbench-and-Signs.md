# UK road signs and Roadworks Workbench

Craft a **Roadworks Workbench**, **Blank Road Sign** and **Narrow Poles**. Put the sign into the workbench, search or filter its illustrated catalogue, choose a face and edit any available destination, route, speed, measurement or text fields. Take the configured result. Default text retains the official reference artwork; changed fields replace only their labelled regions. Welsh place names are supported.

Every conversion consumes one input for one output. Reconfigure existing signs at the same bench. No dye, power or additional blank is needed. Signs are decorative: they do not control vehicles or replace functional railway signals.

The workshop interface separates the searchable catalogue from a larger, full-colour preview. Select a design to see its name, labelled settings and available variants. Use the arrow controls or mouse wheel over the settings panel to reach additional fields. Custom text updates the preview; invalid fields block the output until corrected.

Both catalogues can be browsed without material. Use **Blocks** and **Slabs** to choose a road-marking family. Your sign, block and slab selections remain independent when switching tabs. Incompatible material does not lock the catalogue: the conversion strip explains which material is needed, and no output is available until it matches. The whole interface fits the available GUI area, including its inventory controls.

See the actual sign editor, empty-material road catalogue and fitted interface at a larger GUI scale. Sign thumbnails show the default catalogue design; the larger preview shows your edited values. Paired marking halves show the complete symbol in the larger preview, with an orange outline identifying the half being made.

Stack Narrow or Wide Poles, then use a configured sign on either width at the desired height. Your facing sets its direction in 45-degree steps. Attach supplementary plates lower down and signs on opposite faces. Use a sign against a solid wall for a wall mount. Large signs need clear space around the pole; placement refuses occupied or protected cells.

Use the Create wrench to rotate a pole-mounted sign. Sneak-wrench the face to recover that sign with its configuration. Sneak-wrench the exposed pole to recover its section and attachments. Mining also returns the owned pieces; adjacent pole sections remain in place. Wall signs drop when their support is removed.

The Road Markings tab accepts plain or existing marked asphalt. All 35 marking styles remain available as full blocks and slabs. Each family converts freely between its designs and plain asphalt; full blocks and slabs cannot convert into one another. Craft plain slabs normally before decorating them. Saved road blocks and inventories retain their existing IDs, rotation, slab merging, waterlogging and automatic end bars.

The creative catalogue shows the equipment and base materials. When JEI is installed, the individual marked-asphalt ingredients are hidden from its main list; the workbench conversion category explains their use. JEI is optional. The integration uses JEI 19.50 or newer for Minecraft 1.21.1 and is verified with 19.70.0.469.

See [mounting details](Road-Sign-Mounting.md), [road marking layouts](Road-Markings.md) and [crafting recipes](Crafting.md). Source artwork, provenance and catalogue coverage are retained with the generated assets. Official sign illustrations contain public sector information licensed under the Open Government Licence v3.0; Crown copyright is acknowledged in the source manifest.

The workbench has **36 everyday sign choices**, spread over two pages and five categories:

- **Rules and speed (9):** editable speed limit, national speed limit, Give Way, Stop, No Entry, One Way, Keep Left/Right, mandatory turn and No Through Road.
- **Warnings (8):** roundabout, traffic lights, pedestrian crossing, children/school, bend, double bend, road narrows and editable low bridge.
- **Directions (5):** white local, green primary, blue motorway, brown tourist and multi-destination junction signs.
- **Roadworks (9):** roadworks, temporary signals, Road Closed, Road Ahead Closed, Diversion, Diverted Traffic, End of Diversion, End of Roadworks and lane closure.
- **Parking and information (5):** Parking, No Waiting, No Stopping, Bus Stop and an editable supplementary plate.

Select a sign, then use its variant control for available arrow directions, narrowing sides or lane layouts. Edit the labelled fields for speed, clearance, destinations, routes, bus stop details or supplementary text. The 64 underlying variants occupy only 36 catalogue tiles.

Only the 64 current variant textures and their definitions ship in the mod. The unused 1,169-design catalogue and its runtime textures have been removed; no legacy sign compatibility or migration is retained.

In-game variant controls and an edited sign placed in the world.

Narrow Poles use eight broad sides and a simple collision box. Signs still rotate in 45-degree steps. Diagonal collision uses a small set of conservative strips rather than a dense voxel grid; identical sign geometry shares cached shapes regardless of text or item identity.

Street furniture uses compact sizes: the Bus Stop is 0.375 by 0.5 blocks, speed/restriction discs are approximately 0.625 blocks across, warnings are 0.75 blocks high, and direction boards are at most 1.5 blocks wide. Existing current designs adopt these dimensions; stored text and choices are preserved. Their auxiliary occupied cells reconcile automatically while loaded.

Both pole widths use the same eight-sided silver mesh and accept all existing pole-mounted railway fittings and road signs. See [Narrow and Wide Poles](Poles.md) for crafting, placement and recovery.
