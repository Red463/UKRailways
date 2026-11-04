# Station PA speakers

Install the updated UK Railways JAR on the server and every Minecraft client.
**Station PA Speaker** is available in the creative tab and through its recipe
in [CRAFTING.md](Crafting.md). Each speaker operates independently.

## Mount and configure

Place it on a floor, ceiling or wall, or click a horizontal Wide Pole side
without sneaking to mount it in that pole cell. The wall bracket supports the
existing Create-girder mounting arrangement. A survival break returns the speaker
and any pole consumed by an integrated mount.

Empty-hand right-click opens two tabs:

- **Playlist:** Add the available announcement, select an entry, adjust its pause
  after playback (0–3,600 seconds), remove it or move it up/down. Lists hold up to
  32 entries, including repeats. Use the page arrows for longer lists.
- **Playback settings:** choose manual, timer or redstone mode; enable automatic
  starts; select list order or shuffle; set minimum/maximum delays, volume and radius.
  Equal delays give a fixed interval; different delays choose a random inclusive
  value between them. Delays run from 0 to 86,400 seconds and begin after the
  entire playlist, including its final pause. Radius is 4–64 blocks and volume
  is 0–100%, independent of radius. Shuffle visits every entry once per run.

**Done** saves edits and stops any current run before using the new settings.
**Cancel** discards unsaved edits. **Play saved** and **Stop** operate the saved
playlist immediately, without applying draft edits. Stop cancels the current run;
an enabled timer can play again after its normal delay. Disable automatic playback
to prevent that. Manual Play works even with automatic starts disabled.

New speakers start disabled, with one announcement, list order, a five-minute
delay, 70% volume and a 32-block radius. An empty playlist stays idle.

## Redstone and multiplayer

Redstone mode starts on a new low-to-high edge. A signal already high when the
speaker loads or its settings are saved must go low before triggering. Requests
during a playing playlist or its pauses are ignored instead of queued. Separate
speakers can overlap; one speaker never overlaps its own recordings.

Nearby players present when a recording starts hear it as positional **Blocks**
audio. Entering range or loading a speaker midway waits for the next recording.
Leaving range/dimension, removing or unloading the speaker stops its sound.
Settings survive reloads, but interrupted recordings do not resume. After loading,
an enabled timer waits its configured delay; missed announcements never pile up.
Only loaded speakers tick, and redstone sampling does not load neighbouring chunks.

Build permission, interaction permission and an eight-block distance are required
for server-side edits/actions. All Minecraft clients need the same mod version.

## Included audio and artwork

The supplied **See it. Say it. Sorted.** announcement is currently the only clip.
It is bundled as a complete mono Ogg Vorbis recording, approximately 15.66 seconds.
Additional clips require a future mod update; the screen has no upload or URL field.
The default recording's duration drives playlist timing. Resource packs replacing
it should preserve that duration.

Speaker model preview shows the generated
cabinet, inset perforated grille, driver detail and mounting options. Regenerate:
