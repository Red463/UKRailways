# Railway information displays

Use the [Railway Laptop](Railway-Laptop.md) to search named boards/screens, edit service settings, write custom messages and access the network map from a desk. Existing direct editors continue to work.

Install the same UK Railways JAR on the server and all Minecraft clients. The information system reads Create stations, schedules, track graphs and signal boundaries; displays do not control trains.

For editable station/platform signs and the fixed two-block freestanding Local
Railway Information Board, see [Station signs](Station-Signs.md).

For independent station announcement playlists and speaker mounting, see
[Station PA speakers](Station-Speakers.md).

All UK Railways blocks support Create wrench pickup; railway signals and poles
support eight-way placement. See [Wrench and rotation](Wrench-and-Rotation.md).

For the modern train-mounted arrival/manual horn, see [Train Air Horn](Train-Air-Horn.md).

## Station information board

Place **Station Information Board** with its screen facing passengers. Select a Create station block with the **Railway Linking Tool**, then use the tool on the board. Stations must be in the same dimension and within 128 blocks, including height. Sneak-use the tool on the board to clear the station link. Removing and replacing a station creates a new identity and requires a new link.

Empty-hand right-click opens settings. Set a display name, arrivals/departures/both, and a layout. Platform layout shows the next service; concourse layout lists services. Both alternates every eight seconds on a compact board and uses separate columns on a wider board. Add up to 16 nearby stations with optional platform labels (16 characters each). Editing requires build permission and being within eight blocks of the controller.

The original amber dot lettering scrolls long names. Estimates use Create predictions and are labelled estimates, rather than guaranteed timetable times. Arrival and departure estimates are separate. Timed waits can supply a departure estimate; cargo, passenger, redstone or otherwise indefinite waits show **Awaiting departure**. Origins come from observed departures, or remain unknown. Manual/paused trains can appear at a platform without a promised departure. Wildcard and ambiguous station names do not create invented calls.

## Railway computer

Place **Railway Computer** and right-click it empty-handed. Drag to pan, wheel or +/- to zoom, use arrow keys to pan, and use **Fit network** or **Dimension**. Select trains, stations, signals and linked UK heads for details. A builder's viewport is saved on closing and is also used by an attached world screen.

Track uses Minecraft X/Z geography without terrain. Solid amber sections are occupied; dashed blue sections are reserved. A train can occupy multiple signal groups. Directional authorities show G/Y/R/? and protected group IDs. Linked UK heads are separate repeater markers with an authority ID when available. Portal endpoints are markers, not lines drawn between dimensions.

## Larger screens

Build a flat rectangle from **Display Tiles** plus exactly one board or computer controller. Every block must face the same direction, with no holes. The controller can sit anywhere in the rectangle. Adjacent placement inherits the facing of the existing display. A board controller makes a larger board; a computer controller makes a larger map. Right-click any linked tile to access its controller.

Default maximum size is 16 blocks wide by 8 high; server settings can raise this to 32 by 16. Extra controllers, holes or oversized structures show a status instead of a working image. Partial chunk loading shows an incomplete/unavailable state and never forces chunks to load. The blocks remain in place when the assembly is invalid.

## Freshness and limits

Dynamic data refreshes about once per second; geometry about every five seconds. Collection is incremental with a default two millisecond soft budget per tick. Individual Create operations can exceed that budget. Stale data is marked after five seconds. During a rebuild the previous geometry remains visible; configured limits produce an explicit partial-data state.

Configuration is in `config/ukrailways-server.toml` on the dedicated server (NeoForge generates it on first startup). Limits can be lowered from 50,000 track segments, 2,048 trains and 16,384 combined station/directional signal records. These are also hard safety ceilings for this version. Snapshot transfer is capped at 8 MiB. No Minecraft chunks are force-loaded by the information system.

Remote browser setup: [NETWORK_VIEWER.md](Browser-Network-Viewer.md).

## Validation status

## Display troubleshooting

A board or computer is itself a controller and works as a standalone 1x1 display.
Display Tiles require a board/computer in the same complete rectangle. The live
assembly-sync fix ensures newly placed controllers and resized screens update
without a chunk reload. Custom information screens suppress Minecraft's late
background-blur pass so their map, headings and settings text remain sharp.
After replacing the mod JAR, restart both client and server to load the new code.

## Map readability

Station and portal names use dark-backed, collision-checked labels. Train names appear on hover or selection. When a map is
too crowded, it keeps the symbols and hides labels that cannot fit. Signals and
linked UK heads use compact symbols rather than repeated text. Hover a marker or
name badge for details; click to keep its details below the map. Station names
have first label priority, followed by portals. Grid contrast is lower
than track contrast. The computer uses a separate two-line key and status area;
world screens use the compact embedded key. Label placement is deterministic and
bounded, and hover targets are cached until data, viewport or screen size changes.

## Slim station cabinets

Information boards now use a wide, shallow black cabinet: one section is one
block wide, half a block high and roughly a quarter-block deep, with recessed
amber glass and a narrow bezel. The computer and tiles share the slim profile so
mixed-controller screens align. All three keep their existing IDs and settings.

Place against a wall for rear brackets, beneath a ceiling for two suspension
rods, or on a floor for short feet. Wall attachment to a Wide Pole or Create
metal girder uses an extended rear bracket. Adjacent information sections inherit
facing and mounting style. Their planar connections remove internal bezels;
joined rows extend to meet each other and make one continuous larger screen.
Suspension rods and feet appear only at the outside ends of an assembly.

Existing station links and board settings are preserved. Existing blocks default
to floor mounting and refresh their connected edges when loaded; new placements
choose mounting from the clicked surface. Chunk boundaries never force chunks to
load. Continue to use exactly one board/computer controller per rectangle.

## Train and carriage symbols

Native maps, world screens and the browser now show individual carriage symbols
instead of moving train-name badges. The leading vehicle has a brighter pointed
nose, while other carriages use outlined bars with a window stripe. Every symbol
uses its carriage's actual bogey endpoints and follows the local track heading,
including curves. Reversing changes the leading end. This indicates the leading
vehicle, not an inferred locomotive type from the player's contraption design.

Above two blocks per pixel, the map collapses each train to one compact icon per
visible dimension. Portal fragments are separated; unavailable headings have no
invented direction arrow. Names, destinations and occupied/reserved groups remain
on hover/selection, and clicking any carriage selects the whole train. Browser
users can still select trains by name from the entity picker. Station labels
avoid carriage bodies as well as other labels.

Collection reads at most 128 physical carriages per train and exports at most
256 per-dimension fragments, with an explicit partial-data state on truncation.
Older snapshots without carriage metadata fall back to a single train symbol.
Update both client and server, restart Minecraft and refresh an open viewer page.

## Clear service layout

The small amber lettering is retained. A board has one full-width station heading,
then clearly separated arrivals/departures sections. Platform layout shows a
labelled next-service card: Train, From/To, optional Service and Platform, and
Arrival/Departure estimate or waiting state. Wide concourse sections use aligned
Train, From/To, PL. and timing columns, with subtle rules between services.

Redundant service titles are omitted when they repeat the train name or route
(case and whitespace ignored). Unknown origins/destinations explicitly show
Unknown instead of substituting a train name. A train and destination may have
the same name; their separate labels make the meaning clear. Existing estimates
remain estimates; at-platform indefinite waits still say Awaiting departure.

Long values scroll inside their own cells while labels stay fixed. Sparse boards
keep spare space rather than enlarging text. Narrow/short panels use a compact
first-service summary based on the fields that can fit. Both mode keeps its
side-by-side/alternating behaviour and station links/settings are unchanged.

Train symbols use pale blue carriage bodies with dark outlines/window stripes and
a near-white leading vehicle. Detailed bodies are nine pixels wide (ten for the
compact overview icon), keeping them distinct from amber occupied track.

The [Railway Tablet](Railway-Tablet.md) opens this same live map from either hand,
anywhere, without a computer link. Each tablet saves its own view.

## Map layers and world selection

Computer and Railway Tablet maps have a Layers panel with independent controls for Trains, Create signals, UK signals (repeaters), Stations, Names/labels and Occupancy/reservations. Track geometry stays visible. Hiding trains keeps occupied/reserved track visible unless its separate layer is disabled. Hidden entities are excluded from hover and selection; hiding names retains marker icons and hover details.

The world button displays the current dimension name and opens a list instead of cycling dimensions. Overworld, The Nether and The End have friendly names; custom dimensions include their resource IDs, available in a tooltip for long names. Use arrows/Tab and Enter/Space in an open panel, scroll long lists, and Escape or an outside click to dismiss. Choosing a world clears selection and fits its network.

Layer preferences are local to the Minecraft client, shared between its computer/tablet views and remembered in config/ukrailways-map-layers.json. All layers start enabled. They do not alter other players' views or world display blocks. Tablet live updates continue while panels are open.
