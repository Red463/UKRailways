# Wrench pickup and diagonal signals

Use Create's normal wrench on UK Railways blocks.

- **Sneak + right-click:** pick up the block into your inventory. Overflow drops
  beside you. Sign text, speaker playlists, signal links, board settings, computer
  viewports and applicable crossing settings are retained.
- **Right-click a railway signal or Wide Pole:** rotate through eight horizontal
  directions in 45-degree steps. Poles remain upright. Standard/LED two-, three-
  and four-aspect heads and standard/LED semaphores support this.
- Other signs, speakers and screens use normal Create cardinal rotation. The fixed
  two-block information board turns as a whole. Crossing barriers must be picked
  up and placed again to change their direction, so their reserved sweep remains safe.

For floor/ceiling and integrated pole signal placement, look in the desired
direction; the head faces you, snapping to the nearest supported angle. Wall heads
start aligned to the clicked face, then can be turned with the wrench. Their
wall/girder bracket stays anchored while the head turns. New pole sections inherit
the supporting section's angle, including automatic extension at the top of a pole.
Rotating a pole affects that selected section. An aligned semaphore column rotates
together, retaining its shared link and lower distant arm.

An integrated mount returns its consumed pole once in addition to the attached
item. Either half of the fixed information board returns one complete board.
Wrenching a crossing barrier arm resolves its pedestal, picks up one barrier and
removes its owned auxiliary cells. Display assemblies rebuild after tile removal.
The speaker's current audio stops when it is removed.

Pickup preserves portable configuration, while live animation, playback, borrowed
pole flags and display assembly ownership are rebuilt after placement. New mounting
state comes from the new support. Signal/station links are revalidated at their new
location; station references outside their allowed range/dimension are cleared.
Position-based signal/crossing links moved to a different dimension require relinking.
Existing cardinal placements load with zero additional yaw.

Build and interaction permissions apply to all affected blocks before pickup.
Pickup also respects cancelled NeoForge block-break events. A protected or unloaded
owned part prevents the operation. No neighbouring chunks are loaded to rotate or
pick up these structures.

The linked Create signal still determines the aspect. Turning a UK repeater head
changes its physical facing, without changing the track signal's authority.

