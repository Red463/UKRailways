# UK concrete sleeper track

UK Concrete Sleeper Track is a new standard-gauge Create track material. It uses precast concrete sleepers, dark fastening clips, weathered brown rail sides and polished steel running surfaces. All train movement, connections, placement tools and station mechanics use Create's native track implementation.

Find it in the Create: UK Railways creative tab near Railway Ballast. Place and connect it using the normal Create track item: select an existing track end, then select the destination to create a straight or curved connection. Normal slopes, diagonals, crossings, girders, waterlogging and wrench interactions remain available. It connects to ordinary Create track without a transition piece and accepts existing Create trains and Greater Anglia kits.

**Ballast remains separate.** Place existing [Railway Ballast](Railway-Ballast.md) under and beside the track for the bed and shoulders. The track itself contains no ballast mesh or block.

## Manufacturing

Use the same Create sequenced-assembly machine order as regular track:

1. Start with **one Light Gray Concrete**.
2. A Deployer applies **one Iron Nugget**.
3. A second Deployer application uses **one Iron Nugget**.
4. A Mechanical Press completes **one UK Concrete Sleeper Track**.

There is one loop and one guaranteed output. No zinc or alternate rail ingredient is used for this variant. The incomplete track is a temporary processing item, not an additional crafting component to make separately. The recipe unlocks after obtaining Light Gray Concrete; see [the complete crafting guide](Crafting.md).

Breaking ordinary track returns its matching track item; Create manages curved-track recovery and its normal track costs. Both curve ends save the `ukrailways:uk_concrete` material, so saving/reloading preserves the concrete variant. Existing Create tracks and recipes remain unchanged.

## Crossings and junctions

At curve crossings, shared-endpoint forks and straight-through turnouts, overlapping sleeper and fastening volumes are trimmed while retaining their original sprites and interpolated UVs. New cut walls close the mesh. Native rail and girder partials, track placement, train movement and manufacturing remain unchanged. The fallback renderer and Flywheel use the same geometry. Branch edits queue native visual updates; model reload and logout clear the bounded caches.

Discovery uses the curve's two loaded endpoints, a small static-track corridor (eight blocks along an endpoint axis and two laterally), and an index of already-discovered UK curves. Expanded tie samples occupy 16-block spatial cells, allowing independent curved crossings to find each other. The index holds at most 2,048 curves and 256 cells per curve; loaded-owner and block-state checks refresh within five ticks. It does not search the world or force-load chunks. Open or concave replacement meshes that cannot be safely subtracted retain their existing rendering.

