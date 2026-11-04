# British mainline signals

Standard and LED two-, three- and four-aspect heads repeat the state of existing
Create track signals. **Keep the original Create signal installed:** it controls
train movements. A UK head is a linked display, not a replacement track boundary.

## Place and link your first head

1. Build connected Create-compatible track and attach an ordinary Create signal.
2. Craft a British Two-Aspect Signal and the **Railway Linking Tool**. Find the
   recipes in [Crafting](Crafting.md), or use the Create: UK Railways creative tab.
3. Place the UK head with its lamps facing approaching trains. Unlinked heads are red.
4. Right-click the Create signal with the tool, then right-click the UK head.
5. Test with a train and retain the Create signal and its track connection.
6. Sneak-right-click the UK head with the tool to clear its link.

Source and head must be in the same dimension and within **128 blocks**, including
vertical separation. The tool keeps its selected source for linking further heads.
Links survive saves and restarts. Linked chunks are never force-loaded; missing,
unloaded or invalid dependencies give restrictive indications.

## Choosing a head

| Head | Indications | When to use it |
| --- | --- | --- |
| Two-aspect | Red, green | A simple stop/proceed repeater |
| Three-aspect | Red, yellow, green | One signal of automatic look-ahead |
| Four-aspect | Red, yellow, double yellow, green | Two signals of automatic look-ahead |
| LED variants | Same rules as their standard counterparts | An alternative lamp appearance |

Place Create signals along the route and link each UK head to its corresponding
boundary. Three/four-aspect heads find the next directional Create authorities
automatically; there are no separate look-ahead links to configure.

| Proven Create authorities, starting at the linked signal | Three-aspect | Four-aspect |
| --- | --- | --- |
| Linked source red, unavailable or invalid | Red | Red |
| Linked brass source mixed/conditional (Create yellow) | Yellow | Yellow |
| Only the linked source proven green | Yellow | Yellow |
| Linked source and next source proven green | Green | Double yellow |
| Linked source and next two sources proven green | Green | Green |

Two-aspect heads require green directional authority to clear. A conditional
Create yellow remains red on a two-aspect head. On three/four-aspect heads it
becomes single yellow and never gains a higher aspect through look-ahead.
Single yellow uses the lower yellow lamp; double yellow lights both.

At junctions the head uses the least proven clearance across travel-compatible
forward branches. Unknown or missing downstream signals, unloaded dependencies,
loops, interdimensional edges and traversal limits stop further clearance proof.
An open-ended line with no downstream signal can therefore remain yellow.
Look-ahead is bounded to three authorities per path, 256 examined edges across
branches and 2,048 track blocks per path. It never grants Create route permission.

## Mounting and editing

Click a top face for floor mounting, a horizontal side for wall mounting, or an
underside for ceiling mounting. Place the head against an empty Narrow or Wide
Pole section to integrate it with the pole. Each railway fitting needs its own
pole section. See [Poles](Poles.md) and [Gantries](Gantries.md) for complete builds.
Gantry-top heads use a compact floor stem and foot plate.

Use a Signal Nameplate for an identifier; empty-hand right-click opens its editor.
Nameplates accept up to 16 letters, digits, spaces, `/` and `-`; lowercase becomes
uppercase. `ES692` and `ES 692` display `ES` above `692`. The nameplate is decorative
and does not establish a signal link. Create wrench operations are described in
[Wrench and rotation](Wrench-and-Rotation.md).
