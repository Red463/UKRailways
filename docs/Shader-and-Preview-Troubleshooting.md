# Troubleshooting and compatibility

## Before you start

Use Minecraft 1.21.1, Java 21, NeoForge 21.1.251 and Create 6.0.10. Install the
same UK Railways JAR on the server and every client. Keep only one version in
each mods folder. This is **1.0.0-rc.6**, a release candidate, not the final 1.0.
Back up worlds before updating. Full ATM10 multiplayer acceptance remains pending.

## Missing curved sleepers with shaders

rc.2 added compatibility rendering for UK curves when Colorwheel is the active
Flywheel backend. Shaders and other Create optimized visuals can remain enabled.
rc.4 caches native curve geometry on the GPU to avoid repeated Iris vertex
processing. The client tracks.shaderCompatibilityRendering option restores CPU
rendering after a restart if needed. Testing used Iris 1.8.14-beta.1,
Colorwheel 1.3.0-beta3, Complementary Unbound 5.9.3 and Euphoria Patches 1.10.5;
other combinations and every schematic have not been verified.

## Frame drops when showing a schematic preview

Update to rc.6. It includes the rc.3 fix that prevents schematic previews from repeatedly clearing the
placed-track junction geometry cache. Previews use ordinary sleepers; placed
junctions retain detailed overlap clipping. Large previews still cost rendering
time. The regression replay verified cache reuse; it is not a full-pack FPS test.

## Signals stay red or yellow

Retain and check the original Create signal, its track connection and direction.
Check loaded chunks and downstream signals. Missing evidence gives restrictive
indications. The UK head never grants train movement authority.

## Train kit placement or assembly fails

Check the clear placement envelope, straight track length and Create's assembly
limits. Follow [Train Kits](Train-Kits.md). A kit places stationary vehicles;
assemble them at a Create station and use a normal Create conductor/schedule.

## Artwork looks outdated

Disable older Comic HD/signal-preview resource packs. Current artwork is bundled;
no companion resource pack is required.

## Reporting a problem

Open an issue with the mod, Minecraft, NeoForge and Create versions, reproduction
steps and relevant errors. State the shader/renderer versions when applicable.
Redact invitation tokens, account/session details, IP addresses and other private
server information before attaching logs or screenshots. Never upload world saves
or authentication configuration just to report a rendering problem.
