# Modular signal gantries

Create: UK Railways includes twelve individually placeable gantry blocks. Mix heights and span lengths to build modern portals, heritage lattice bridges and single-sided cantilevers. There is no structural simulation or fixed span limit.

| Block | Use |
|---|---|
| Gantry Concrete Foot | Concrete foundation and narrow socket for box columns. |
| Gantry Lattice Foot | Wider baseplate, four upright shoes and socket rings matching the lattice column. |
| Gantry Box Column | Stackable six-pixel-square modern steel upright. |
| Gantry Lattice Column | Stackable open eight-pixel-square heritage upright. |
| Gantry Solid Beam | One-block-long I girder with a solid web. |
| Gantry Lattice Beam | One-block-long open cross-braced girder. |
| Gantry Knee Brace | Top column section with a continuous diagonal arm supporting the beam above. |
| Gantry Walkway | Shallow open-mesh floor with sixteen physical openings and wrench-configurable edge rails. |
| Gantry Guardrail | Separate railing block for independent structures; walkway edge rails use the wrench. |
| Gantry Access Ladder | Climbable access section; repeat vertically. |
| Gantry Drop Bracket | Full-height signal hanger with top and bottom mounting plates. |
| Gantry Signal Platform | Open-mesh walkway with a raised signal pedestal and configurable edge rails. |

## Building a portal

1. Place Gantry Concrete Feet for box columns or Gantry Lattice Feet for lattice columns, outside the train's swept path. Stack columns above each foot to the required height. Continued columns retain the orientation of the section below.
2. Bridge the columns with repeated solid beams or repeated lattice beams. Beam span is perpendicular to the direction you face when placing; use the Create wrench for a quarter turn. Adjacent beams of the same type and axis remove internal endplates. Exposed ends retain caps. Different beam types remain separately capped.
3. Place walkway or signal-platform modules directly above beams. They align automatically to the beam below; the wrench can adjust them. The floor sits at the bottom of its cell, directly on the beam; the guardrails occupy the space above it within that same cell.
4. With the Create wrench, right-click near a walkway edge to toggle that edge's guardrail. Click the centre to rotate the walkway; sneak-wrench to pick it up with its configured edges. Adjacent tiles have continuous horizontal rail runs and shared corner posts. Toggles require no separate rail item. The separate Gantry Guardrail block remains available for independent structures. When updating an existing gantry, remove its separate guardrail blocks above the deck and configure the walkway edges with the wrench.
5. Use an ordinary signal item directly on the horizontal side of a beam or drop bracket for a wall-mounted head. A small steel connecting plate appears automatically, reaching the existing signal bracket. Beam-end faces already meet their endplates. For a suspended signal, click the underside of a drop bracket; for a floor-mounted signal, click the top of a signal platform. The clicked face selects the mounting mode.
6. Add a column-side ladder in adjacent cells, with its rungs facing the accessible side. Ladder geometry lies near the rear of its block; rotate it to meet the column. It is climbable and can be extended without a full backing wall. Ensure access continues over the deck edge; the ladder does not automatically cut an opening or create a safety gate.

For a cantilever, omit the far column. Replace its top column section with a knee brace directly beneath the first beam; retain a column immediately below it. If the beam and its neighbouring span already exist above, the brace points its diagonal arm into that span automatically. Otherwise use the Create wrench for a quarter turn until the arm points along the beam. The brace is an upright section, rather than a piece to place beside the column. Every block is independently removable. Wrench pickup and rotation work, and all modules support waterlogging. Lattice openings have open physical collision; they are not opaque cubes with painted trusses.

## Signal and train clearance

The mod's existing signal items and configuration/linking controls are reused. Semaphores need extra room for their projecting arms and sweep. Do not place a guardrail or another block in the same cell as a signal. Hanging maintenance cages, new route-indicator boards and overhead electrification are not included in this set.

The assembled beam is one block tall: the initial shallow-beam sketch was deepened so its upper and lower flanges meet standard block-boundary mounting points. This prevents detached hangers with the existing signal models. Walkways now have a shallow physical mesh floor rather than a painted solid slab. Signal platforms include a central pedestal up to the next block boundary, so floor-mounted signals remain supported. Edge rails use fence-style collision to prevent jumping off, with open selection geometry between the rails.

Choose height from the lowest hanging head/bracket and the actual train, including roof equipment. The offline assembled preview demonstrates mesh/material contact, not a guaranteed track-clearance envelope. The native gantry check exercises actual signal-item placement and OBJ model baking. Train-clearance envelopes and shaders still depend on the surrounding build.

## Artwork and regeneration

The mod's displayed name is Create: UK Railways; existing `ukrailways` IDs remain unchanged.

See the native gantry screenshot and open mesh with integrated rails.
