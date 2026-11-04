# Stackable semaphore signals

Use **British Semaphore Signal** from the creative tab or its red/white crafting recipe. Arms now reach approximately 1.5 blocks from pivot to tip, with a larger mechanism and continuous full-height post. Place another section on top (or underneath): it inherits facing and mounting style. Arms are one block apart vertically. Remote mounting on Wide Poles, walls, ceilings and girder brackets remains available.

## One link per assembly

A standalone adaptive semaphore is a red stop arm. Stack two or more same-facing sections in a vertical column: the bottom becomes a yellow fishtail distant arm, with red stop arms above it. A different facing or ordinary-wall depth starts a separate group. Adjacent column discovery is limited to 32 members and never loads chunks.

Select a normal Create signal with the Railway Linking Tool, then apply the tool to **any section**. The source applies to the whole assembly. Sneak-use any section to clear the assembly link. Source and all members must share a dimension and be within 128 blocks. Conflicting saved links keep the assembly restrictive until explicitly relinked. Too-long/incomplete columns cannot be linked or cleared as a complete assembly.

Red arms repeat the linked Create authority. The lower yellow arm clears only when that authority and every reachable next forward authority are proven green. Missing/unloaded, restrictive or ambiguous evidence leaves it horizontal at caution. Red above cannot be at stop with yellow below clear. Create's original track signal remains the train authority. This is bounded next-signal look-ahead, not full mechanical station interlocking.

Unlinked new sections inherit a single unambiguous in-range source from their stack. Removing a section recalculates roles and preserves sources on the remaining sections. Gaps separate assemblies. Arms raise 45 degrees for clear over half a second; lower-arm animation is constrained beneath the upper arm to avoid intersecting during changes.

## Existing worlds

Registry IDs and saved links remain readable. An isolated old **British Semaphore Distant Signal** keeps its original yellow/green repeater behaviour, following its explicitly linked source. Applying a new link converts legacy blocks in that assembly to the adaptive semaphore. Mixed legacy assemblies remain restrictive until relinked. Existing distant items can be crafted alone into the primary semaphore. The creative tab has standard and LED semaphore items; the legacy distant item remains hidden.

A section attached to an actual Wide Pole returns that pole when broken. Sections stacked above it inherit the post alignment without producing extra pole items. This ownership survives save/reload.

## Artwork and checks

- Stop / stack preview
- Distant / stack preview

The older static PNG predates the enlarged model; use the interactive previews for current sizing.

Automated checks cover column membership, limits, source conflicts/propagation, restrictive look-ahead, compatibility NBT and recipe conversion, model state coverage, continuous posts and enlarged arm sweep. In-game acceptance remains required: compare size against a train, place/relink/remove from either end of stacks, check all four facings and mounts, unload/reload, survival drops, arm transitions and two clients. Preview browser access was unavailable in the authoring environment, so visual gameplay review has not been completed.

## LED semaphore and matched glass

**British LED Semaphore Signal** uses the same moving arms, roles, mounts,
stack discovery and one-link behaviour as the standard semaphore. Its night lamp
uses the red/yellow/green LED matrix. Standard and LED sections can share a column;
the bottom still becomes the yellow distant arm. Painted arms are unchanged.

Craft one standard **British Semaphore Signal** with one **Glowstone Dust** in
any crafting arrangement to obtain the LED version. Legacy distant items convert
to a standard semaphore first and can then use that upgrade.

Standard signal lamps now use a matched original faceted optical-glass family:
red, yellow, green and unlit share the same dark rim, bevel, facets and highlight.
This covers colour-light heads, semaphore lamps and standard crossing lamps;
existing LED optics are retained. The textures are original comic artwork made
to sit alongside PureBDcraft, without using its assets. Default lamps are 128px;
the optional Comic HD pack includes the matching 256px textures.

The current rebuild includes earlier bracket and information-display fixes.
Replace the mod on both client and server and restart; replace the optional HD
ZIP if installed. Existing placed standard semaphores remain standard.
