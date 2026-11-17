# UK Railways 1.0.0-rc.6 installation

## Requirements

- Minecraft **1.21.1**, Java **21**.
- NeoForge **21.1.251 or newer compatible 21.1.x**; tested against 21.1.251.
- Create **6.0.10** for Minecraft 1.21.1, with Create's normal dependencies.
  This build explicitly accepts Create versions from 6.0.10 up to, but excluding,
  6.0.11. Other Create versions have not been validated.
- JEI is optional. Workbench recipe-viewer integration requires JEI **19.50 or newer** for Minecraft 1.21.1; tested with 19.70.0.469.
- Install the **same UK Railways JAR on the server and every player's client**.
  This is a content mod with custom blocks and networking, not a server-only plugin.

The development baseline was taken from ATM10 8.2. Compare your installed Minecraft,
NeoForge and Create versions before adding the mod; a full ATM10 server pack has
not been automatically tested here. Do not change your modpack's dependencies merely
to force an incompatible version to load.

## Install or update

1. Stop the server and close Minecraft clients.
2. Back up the server world before first installing or updating this mod.
3. Remove any older `ukrailways-*.jar` from the server's `mods` folder.
4. Copy `ukrailways-1.0.0-rc.6.jar` into that folder.
5. Put that same JAR in each player's Minecraft instance `mods` folder, removing
   their previous UK Railways JAR too. Keep only one UK Railways version installed.
6. Start the server and clients. Check the server log for UK Railways loading errors
   or dependency/version warnings before testing in a disposable area.

HD artwork is included in the mod by default. No companion resource pack is needed.
Disable older Comic HD and signal-preview packs, which can override current models.
PureBDcraft is not required.

## First use

- Craft blocks and the Railway Linking Tool using [CRAFTING.md](Crafting.md).
  Basic recipes unlock after acquiring iron; upgrades after acquiring their base item.
- Keep ordinary Create signals installed and connected to track. Use the linking
  tool to select a Create signal and then a UK signal; Create still controls trains.
- Crossing setup, detection-zone spacing and settings: [CROSSINGS.md](Level-Crossings.md).
  Empty-hand right-click on a controller selects sound/mute, delay and manual closure.
- Semaphores and distant warning setup: [SEMAPHORES.md](Semaphores.md).

## Release candidate limits

Crafting costs are initial balance. Crossing/distant placement must be configured
correctly: crossings do not brake trains, and distant semaphores repeat one stop
ahead rather than providing full mechanical interlocking. Keep required detector
chunks loaded; the mod intentionally never force-loads them. Feathers remain deferred.
Full ATM10 multiplayer acceptance and extended survival testing remain to be performed.

The public player release provides the ordinary JAR and `SHA256SUMS.txt` for that
JAR. A maintainer release bundle may additionally include documentation and its
own checksums. Never install a source/sources JAR or put an entire ZIP inside
`mods`; use the ordinary `.jar`. GitHub's automatic source ZIP/TAR is not a mod.

## Information displays and remote viewer

See [INFORMATION.md](Information-Displays.md) for station boards, computers and display tiles.
The browser viewer is optional and disabled by default; see [NETWORK_VIEWER.md](Browser-Network-Viewer.md)
for HTTPS reverse-proxy configuration and per-friend invitations on the VPS.

Sneak-right-click in the air with the Railway Linking Tool to reset all saved signal, station and crossing selections. Sneak-clicking a linked block keeps its existing unlink behaviour. Existing tools retain their item ID and recipes.
