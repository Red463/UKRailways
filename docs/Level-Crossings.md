# Automatic half-barrier crossings

Five items are in the UK Railways creative tab:

- Level Crossing Controller
- Level Crossing Warning Lights
- Level Crossing LED Warning Lights
- Level Crossing Half Barrier
- Crossing Notice Sign

All artwork is included in the mod. The optional Comic HD pack supplies higher
resolution versions. Preview the components and active/inactive artwork.

## Build and link

1. Place a controller within64blocks of the lights and barriers.
2. Place the half-barrier pedestals on opposite road approaches, looking in the
   direction each lowered boom should extend. Each boom is3blocks long. Keep a
   four-by-four vertical sweep plane clear of blocks; placement reserves15 empty
   cells around each pedestal. Stagger opposing barriers so their sweeps do not overlap.
3. Place standard or LED warning lights facing road traffic. They support the
   same floor, ceiling, wall and direct-pole mounting as the railway heads.
4. Choose TWO normal Create signals bounding the approach/crossing section. They can face the same direction, as on an ordinary one-way line. Keep their facing correct for normal train operation. Do not put extra Create signals inside this protected zone.

```text
Create signal ->  approach -- road crossing -- approach  Create signal ->
                  one shared protected Create signal block
```

5. With the Railway Linking Tool, right-click the first Create signal then the
   controller. Repeat with the signal at the other end, then the controller. Endpoints
   are paired in selection order:1+2 for track1,3+4 for track2, and so on, up to8pairs.
   Sources must be within512blocks of the controller and in the same dimension.
6. Right-click the controller with the tool to select it, then right-click each
   road light and barrier to bind it. A visible boom section also resolves to its pedestal.

The controller finds the single valid Create group shared by both signal boundaries, independent of which way their physical heads face. No shared group, or two shared groups on an ambiguous loop, keeps it closed.
If the cabinet remains active with empty track, check incomplete
pairs, extra interior signals and loaded chunks. Sneak-use the linking tool on the
controller to clear its endpoints, then configure valid pairs again. An armed
controller stays closed while its configuration is incomplete. Sneak-use on a
component explicitly unlinks it.

Place approach boundaries far enough away to provide at least 8 seconds of travel
time before a train reaches the road, plus the controller's configured delay and margin.
By default barriers start lowering immediately when detection triggers, with flashing
red warnings, and take 8 seconds to lower fully.
The controller does not brake trains. Reservations
can trigger closure earlier. The track's protected zone must actually contain the
crossing; matching group IDs cannot prove where the road was built.

## Operation

| Phase | Duration | Road lights | Barrier |
|---|---|---|---|
| Clear | Until demand | Off | Raised |
| Optional delay | Configured 0–30 seconds (default 0) | Alternate reds | Raised |
| Lowering | Immediately on demand; 8 seconds | Alternate reds | Moving down |
| Closed | While any zone occupied/reserved | Alternate reds | Down |
| Clear confirmation | 2consecutive seconds | Alternate reds | Down |
| Raising | 8seconds | Alternate reds | Moving up |

These are explicit game timings at20ticks/s. Lights switch red sides every10ticks.
The controller plays the selected Alarm or Yodalarm recording on a positional loop
while active, including any delay, lowering and raising. Minecraft's Blocks volume
slider controls the volume. Muted controllers remain silent. Sound changes and mute
stop the previous recording promptly; leaving the world or unloading/removing the
controller also stops its loop.

Create's occupancy lasts until the rear of the train leaves the far approach
boundary. Either direction activates the same zone. Multiple trains or tracks
keep the crossing active until every configured zone is clear. Another demand
while raising reverses the barrier smoothly and keeps the red lights flashing.

Empty-hand right-click on the controller opens its settings. Select Alarm, Yodalarm
or Muted; enter a whole-number barrier delay from 0 to 30 seconds; optionally toggle
Manual closure; then select Done to save. Cancel discards edits. Settings are per
controller, persist through reloads and synchronize to players. Delay changes apply
to the next closure cycle; a started delay is not extended by editing settings.
Faults and renewed demand while raising bypass the delay and close immediately.
Redstone power also requests closure. Releasing manual/redstone closure cannot open
an occupied crossing. Once a
warning cycle starts it completes its closure sequence before reopening.

## Validation still needed in Minecraft

Automated checks cover sequence boundaries, overlapping train occupancy, faults,
restart state, distinct clear ticks, movement reversal, sweep geometry and cleanup
ownership. Build/model loading has also been checked. Test actual scheduled trains
from both directions, multiple tracks/trains, live barrier collision, reloads and
multiplayer synchronization before using a crossing in the main ATM10 world.
## Crossing notice signs

Place a Crossing Notice Sign on an empty section of signal pole to clamp it directly
onto the pole. Floor, wall and ceiling placement are also supported. This is a visual
sign and does not need linking to a controller.

The white plate defaults to KEEP / CROSSING / CLEAR on three centred lines. Right-click
with an empty hand to edit it. Use up to 64 characters; text is converted to uppercase.
Words wrap automatically, or enter `|` to choose line breaks (at most three lines),
for example `KEEP|CROSSING|CLEAR`. Longer wording is scaled to fit. Text is saved with
the block and sent to other players.

Standard and LED crossing lights now have a wider, lower backboard and more widely
spaced red lamps. Restart the client to load the new models; saved links are retained.

Barrier animation now uses a client-local tick timeline with frame interpolation. Server world-time corrections cannot rewind an ongoing visual movement. New viewers join the synchronized pose, direction reversals remain continuous, and forced closure still applies immediately. Server crossing logic and collision timing remain authoritative.

## Long Crossing Barrier

The standard arm reaches three blocks; the Long Crossing Barrier reaches five. Craft the long version shapelessly from one standard barrier and two iron ingots. Link it to a controller with the Railway Linking Tool as usual. Both use the same eight-second movement and smooth animation.

The long version requires a clear six-by-six vertical swing envelope, including its base cell (35 reserved cells plus the pedestal). Its moving collision reaches the full five blocks. Sneak-wrench the pedestal or any owned arm cell to pick it up; the whole reservation must be loaded and editable. Existing three-block barriers retain their size and links.
