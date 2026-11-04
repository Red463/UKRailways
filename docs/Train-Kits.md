# Greater Anglia pre-built train kits

Create: UK Railways supplies custom Greater Anglia Class 755 and Class 745 bodywork as complete train kits and individual vehicle kits. They place stationary carriages with Create bogeys using a custom modern appearance, passenger seats, cab controls and separate glue regions. Assemble them at a Create station to obtain an ordinary Create train. FramedBlocks is not required.

## Available kits

| Complete kit | Passenger cars | Physical segments | Total length | Bogeys |
|---|---:|---:|---:|---:|
| Class 755 Three-Car | 3 | 4, including power module | 57 blocks | 8 |
| Class 755 Four-Car | 4 | 5, including power module | 71 blocks | 10 |
| Class 745 Twelve-Car Intercity | 12 | 12 | 205 blocks | 24 |

Individual kits provide Class 755 driving, standard passenger, short passenger and power vehicles, plus Class 745 driving, standard passenger and service vehicles. The service vehicle has the matching body/door shell; its initial interior uses standard Create seats rather than a detailed restaurant fit-out.

Passenger bodies are 51/16 blocks wide (3.1875), and the short 755 power module is 53/16 blocks (3.3125). These nominal envelopes derive from the real vehicle-to-gauge ratio, measured against Create 6.0.10's standard track. Raised trim adds only a small amount. They occupy five grid columns when centred, with narrow custom geometry in the outer columns. New kit placements use continuous OBJ shells, raked windscreens, curved roofs, large framed glazing, destination displays, Greater Anglia lettering and dedicated inset red door blocks. The original body part IDs remain available for older placed trains; place a fresh kit to use compact shells and dynamic destinations.

The real FLIRT's shared articulated bogies are adapted to **two independent Create bogeys per vehicle**. This keeps each carriage compatible with Create's assembly and curve-following rules. Vehicle lengths are deliberately compressed by about a quarter for Minecraft curves; their width still follows the track-based scale. Driving cars are 18 blocks, 755 passenger cars 12 (11 for the short variant), power modules 7, 745 passenger cars 16 and service cars 14. One-block coupling gaps keep the Create carriages independent. Each end of a complete formation has an outward-facing cab.

## Placing and assembling

1. Prepare continuous straight Create track. Put a linked station in assembly mode, with enough highlighted track for every bogey. Keep the station and all surrounding builds outside the five-column, six-block-high placement envelope; the front nose extends three track blocks before the first bogey marker.
2. Hold a complete train kit and use it on the **first blue bogey position**. The station determines orientation. The kit checks loaded chunks, track shape, free space, world borders, protection permissions, existing glue and Create's assembly limits.
3. The first click reports length, front direction and endpoint coordinates. It places nothing and consumes nothing. Use the same kit on the same position again within 30 seconds to confirm. Every condition is checked again before placing.
4. Assemble the train through the station's normal Create interface. The kit does not create or alter the station, tracks, world settings or any schedules.
5. Open the passenger doors, board a cab, right-click the appropriate controls, and drive using Create. Passenger seats are actual red Create seats. Vehicle end gangways remain open. Dedicated red double-leaf doors respond to manual operation and redstone; moving doors register Create's native station-side door controls. Their leaves change between closed and slid-open models rather than using a separate animation block entity.

Individual vehicle kits can be placed on straight track without forcing the station direction. Their front follows the player's direction along the track axis, so turn to place an outward-facing rear cab. The clicked track is the vehicle's first bogey measured from its own nose; its body extends three blocks before that point (one for the power module). Placement preview reports the chosen direction. Leave one empty block between independent vehicle bodies and match both bogeys to valid station markers.

If a block or glue entity cannot be placed, or a protection mod cancels a block-place event, the kit rolls back its newly placed blocks and glue and is not consumed. Occupied interiors and existing glue are rejected. The hidden body-part block is not an obtainable item and drops no loose parts. To recover a whole vehicle, disassemble the moving train at a station, stand beside its shell and **sneak-right-click with a Create wrench twice within 30 seconds**. The first click previews recovery; the second returns that vehicle kit and removes only its recognised blocks and internal glue. Track stays in place. Repeat for each carriage.

Recovery requires a complete, unmodified vehicle on straight track with all chunks loaded and building permission throughout. Remove additions, passengers and glue connecting outside the carriage first; clear any manual destination override. Damaged or altered vehicles are refused safely. Historical full-length templates are also recognised, including after moving and disassembling a train. Recovered kits place the new compact dimensions. Individual shell cells cannot be rotated with a wrench.

## Destination displays

Fresh driving-car kits have a live amber destination display above the windscreen. After station assembly, automatic mode shows the next scheduled station; while waiting at a platform it advances to the following call. Both cabs use the same next call, including a reversed rear cab. A missing or completed schedule shows `Not in service`. Wildcard station instructions show the actual station once Create has selected the navigation target; an unresolved wildcard shows `Not in service` rather than a later unrelated call.

To override the text, disassemble the train at a station and right-click the destination housing above the windscreen with an empty hand. Enter up to 64 characters and select **Done**. Select **Automatic**, or leave the field blank, to restore the schedule display. Manual text survives saving, assembly and disassembly. Editing requires building permission and a position within eight blocks of the housing. Historical placed shells retain their original artwork; place a fresh kit for the live display.

## Scheduled reversal

Each cab has a conductor seat between two inward-facing Create train controls, aligned along the train axis. This permits the **same non-player conductor** to operate in either direction. Manual players are not treated as schedule conductors by Create.

Seat a suitable non-player Create conductor at a cab's central driver seat and give it a schedule using Create's normal interaction. Build the route, stations and signals so Create can find a valid path for both journeys. A terminus timetable should visit the opposite terminal, wait, then return; the train does not need a turning loop. A player may also drive manually from either end. The kit does not teleport a driver between cabs or introduce a new scheduling engine.

Native server tests verify that a single seated conductor is detected for both directions after actual carriage assembly. A full end-to-end scheduled round trip with platforms/signals and visual cab driving remains a gameplay acceptance check.

## Class 745 limits

The twelve-car Class 745 exceeds the current Create defaults of **128 assembly blocks and 20 bogeys**. The complete kit reports a requirement of at least **200 scanned assembly blocks and 24 bogeys**, and rejects placement before changing the world if either configured limit is insufficient. Body overhangs account for the difference between 200 scanned blocks and 205 overall blocks.

Server operators can review Create's `trains.maxAssemblyLength` and `trains.maxBogeyCount` settings if a full twelve-car unit is wanted. The mod never raises those values automatically. Individual vehicle kits support custom shorter formations, which should not be described as an authentic twelve-car unit.

## Modern bogies and detail

Visual repair update: exterior lettering uses Minecraft's native viewing orientation, and open doors slide on the outside of the shell. The body generator removes duplicate oriented surfaces and closes the cab cheek/window seams. Retained part IDs receive compatible repairs in place; existing Class 755/745 front cell positions/IDs are unchanged. Restart both client and server with the updated JAR. Older body variants remain available rather than being reassigned to new cells.

Headlights, roof markers and tail markers use selective fullbright OBJ materials; live destination text uses a fullbright font renderer. Only their body cells emit block light. Paint and glazing retain ordinary lighting. Create preserves these optics and internal lighting on moving trains. Projected beams/world illumination from moving vehicles require a dynamic-light/shader feature; fullbright lenses alone do not provide terrain beams. See the actual repaired door/cab meshes and reduced-ambient optics study, both offline previews.

Fresh kits apply the dedicated `ukrailways:modern_flirt` style to Create small bogey block entities. The style is saved with the bogie and captured when the carriage assembles. Both fallback rendering and Flywheel use the same original welded frames and rotating wheelsets. Axleboxes, springs, airbags, dampers, brake discs, motor housings and pipework replace the stock steam-style appearance. Create still supplies the attachment block, wheelbase, tracking and carriage mechanics; this is an inspired appearance rather than a change to shared Jacobs articulation.

The carriage body now mounts one block lower. The native bogey anchor supplies the two central floor cells at its positions, avoiding overlapping body blocks and visually detached running gear. Raised wheel arches expose the suspension and brake fittings; equipment cabinets stop short of these openings. Wheels remain at their native track contact height. Their visual rotation compensates for the custom tread radius.

The body includes wipers, gaskets, cab cameras/mirrors and grabrails, recessed lights/coupler, gangway ribs, HVAC fans/fins, roof conduits and underframe service fittings. Compact rear-facing camera/mirror pods remain within the reserved five-column placement envelope. Bellows and threshold plates project into the coupling gaps while remaining part of their own carriage; coupling heads and service hoses detail the vehicle ends; roof-profile end caps close the former opening above the rear wall.
