# Scheduled-train speed limits

Existing Speed Limit Signs can now enforce their displayed number on scheduled trains. Values are MPH (1?200), using one Minecraft block as one metre. Unlinked signs remain decorative. Manual driving is unaffected.

## Link a sign

1. Place a normal Create track signal at the exact limit-change position, oriented for the direction the limit should govern. Iron or brass signals work; retain the normal signalling layout because the signal still controls train permission.
2. Right-click that Create signal with the Railway Linking Tool.
3. Right-click your Speed Limit Sign with the tool. A confirmation identifies the MPH value and linked direction.
4. Edit the sign's number using the existing empty-hand right-click screen.

The sign and selected signal must be in the same dimension and within 128 blocks. The selected signal must be loaded and have a resolved track direction when linking. Sign mounting/facing is decorative: the selected Create signal determines the controlled track direction, including curved or diagonal track. Use separate signs/anchors for the opposite direction. No proximity search chooses parallel tracks.

Sneak-use the linking tool on the sign to unlink it. Sneak-wrench pickup retains the anchor and number; re-placement validates dimension and range. Removing or unlinking a sign removes its rule. Multiple speed signs linked to the same directional boundary use the lowest applicable limit.

## Train behavior

Scheduled trains look ahead on their selected route and brake before lower limits. Limits add a cap to Create's existing target speed; schedule throttle, curve limits, station stops and signal braking can still require a slower speed. Schedules and reservations are not modified.

A lower limit takes effect when the front passes its linked track position. An increase waits until Create's tracked rear endpoint passes it. Several restrictions can overlap a long train: the lowest still-occupied zone wins. Decorative carriage blocks extending beyond Create's tracked endpoints are not measured.

Restrictions and pending increases are saved across restart. Sign chunks need not remain loaded, and rules do not force-load chunks. Graph-boundary recreation retains occupied restrictions conservatively until an appropriate rear clearance. Reversing retains the most restrictive occupied limit until opposite-direction markers replace it.

Trains assembled or first brought under automatic control inside a zone have no invented past route: arrange an entry sign before their departure. After manual driving, an automatic train retains its recorded restriction until a subsequent limit marker replaces it. New limits or edits placed too close to a moving train cannot overcome physical braking distance instantly. Give trains room to slow down.

A higher numbered sign restores speed up to that number; it never exceeds Create's normal limits. Scanning is bounded to 4096 blocks and 256 traversed edges. Dense graphs or unusually high server speed settings may therefore cause conservative slowing to stay within the proven braking horizon.

Persistent data is stored in world data/ukrailways_speed_limits.dat alongside the signs' own block-entity links. Do not delete it to reset a live railway: it contains occupied-zone history.

## Acceptance checks

Use matching updated JARs on server and clients. Test a scheduled train through 80 ? 20 ? 80 signs with enough approach distance, then a long train spanning several changes. Test both directions, parallel tracks, a junction with a different limit on the unused branch, paused/manual schedules, signal stops, sign edits/removal, source replacement, chunk unload and server restart. Automated policy/native-traversal tests and mixin transformation checks do not constitute a driven multiplayer acceptance test.
