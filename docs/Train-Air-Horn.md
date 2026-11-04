# Train Air Horn

Install the updated UK Railways JAR on the server and all Minecraft clients.
Craft **Train Air Horn** using [CRAFTING.md](Crafting.md), or find it in the UK
Railways creative tab. Place its mounting base on the locomotive roof or another
block that will become part of the train, then assemble normally at a Create station.
Face the twin trumpets along the train. Normal Create wrench-click rotates it;
sneak-wrench-click picks it up.

The horn joins Create's normal station-arrival instrument queue. It also responds
to the driver's normal Create horn control. Each new manual press plays one full
blast. Holding the control does not stack or restart it; release rearms the next
press. Presses while a blast is playing are ignored. Arrival and manual requests
share one non-overlap window per train, including trains carrying multiple air horns.

The supplied recording is approximately **2.68 seconds**, played at its original
pitch. Release does not cut it short. It follows the moving carriage and uses
Create's **Neutral / Friendly Creatures** sound category, with an 80-block audible
radius. Removing/unloading its carriage or leaving its dimension stops the sound.
There is no stationary steam requirement, redstone action or speaker-style settings
screen; an unassembled horn is decorative.

For mixed instruments, selection follows Create 6.0.10: the first eligible whistle
in each carriage's arrival queue, then the last eligible available carriage for
manual horn selection. Ordinary steam-whistle activations retain their normal
audio. To choose the modern horn consistently, use it as the train's whistle
instrument. Train assembly/disassembly preserves the installed block normally.

