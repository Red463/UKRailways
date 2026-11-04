# Your first UK railway

This guide is for **1.0.0-rc.3**, a release candidate for Minecraft 1.21.1 and
NeoForge. Begin in a creative test world so you can learn the tools before building
in survival. The mod adds to Create's train system; its stations, schedules and
track signals still provide the underlying railway operation.

## 1. Install and find the items

Follow [Installation](Installation.md), including the matching client/server JARs and
Create dependency. In creative, open the **Create: UK Railways** tab. In survival,
use [Crafting](Crafting.md); JEI is optional. Some variants are made in the
Roadworks Workbench and some train components use Create assembly, so they do not
all appear as separate crafting-table recipes.

## 2. Lay a short line

Place **UK Concrete Sleeper Track** with Create's normal track placement tools.
Use a second track placement to form a curve. Add **Railway Ballast** separately
under and beside the rails; the track does not place a ballast bed for you.
Leave space for platforms, signals and the full width of a train.
See [UK concrete track](UK-Concrete-Track.md) and [Ballast](Railway-Ballast.md).

## 3. Add a working signal

Attach an ordinary **Create Track Signal** to your track first. Place a **British
Two-Aspect Signal** facing approaching trains. With the **Railway Linking Tool**,
right-click the Create signal and then the UK head. Keep the Create signal in
place: it controls trains. The UK head displays the linked authority. Start with
this simple head before adding look-ahead, semaphores or shunts.
See [Signals](Signals.md) for the complete sequence and restrictive states.

## 4. Build a platform

Lay retaining blocks, platform paving and coping facing the track. Add tactile
paving and yellow lines behind the edge, or choose Combined Platform Edge pieces.
Add stairs, railings, benches and lamps, then optional shelters or a canopy.
Use a Create wrench for supported rotation and pickup. Furniture such as help
points is decorative; benches provide seats and lamps provide light.
See [Station construction](Station-Construction.md) and the
[canopy build guide](Canopy-Building.md).

## 5. Add and assemble a train

The Class 755 Three-Car kit is a smaller starting formation than the twelve-car
Class 745. Lay a sufficiently long straight track and follow the
[train-kit placement guide](Train-Kits.md) exactly. Kits place stationary vehicles;
you still assemble them at a **Create station**. Supply a normal Create schedule
and conductor for automated running. Use [Train manufacturing](Train-Manufacturing.md)
for survival components and sequenced assembly.

## 6. Add passenger information

Use a Station Information Board for arrival/departure information. A Railway
Computer provides the network map; a Railway Tablet opens a portable read-only
map. A Railway Laptop also manages named screens and supported signs remotely.
See [Information displays](Information-Displays.md), [Tablet](Railway-Tablet.md) and
[Laptop](Railway-Laptop.md) for their distinct setup and access rules.

## Where to go next

| Build | Guide |
| --- | --- |
| Signal bridges and mounting poles | [Gantries](Gantries.md), [Poles](Poles.md) |
| Automatic road crossing | [Level crossings](Level-Crossings.md) |
| MPH limits on scheduled trains | [Speed limits](Speed-Limits.md) |
| Tickets and station entrances | [Tickets](Tickets.md), [Ticket barriers](Ticket-Barriers.md) |
| Road signs and markings | [Roadworks Workbench](Roadworks-Workbench-and-Signs.md), [Road markings](Road-Markings.md) |
| Station names, adverts and announcements | [Station signs](Station-Signs.md), [Advert boards](Station-Adverts.md), [Speakers](Station-Speakers.md) |
| Trackside detail | [Palisades](Palisade-Fencing.md), [Grit bin](Grit-Bin.md), [Tunnel lights](Tunnel-Lighting.md) |

If sleeper detail disappears with shaders, use rc.2 or newer. If showing a
schematic preview causes severe frame drops, use rc.3 or newer; it prevents
preview rendering from clearing the placed-track junction cache. Large previews
still have a rendering cost. See the [investigation](Shader-and-Preview-Troubleshooting.md)
for tested shader versions and reproduction limits.
