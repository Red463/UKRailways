# Ticket barriers

The Ticket Barrier is a UK station gate with steel housings, dark paddles, a yellow ticket reader and a red/green lane indicator. Open it with redstone or a Rail Ticket. Ticket openings consume one ticket in survival; the Ticket Machine supplies tickets for free. It does not charge currency.

## Placement and joining

Place one item on solid ground to create a complete lane. It occupies one block across and two blocks high; leave the upper cell clear. Face along the direction passengers will walk when placing it. Place more lanes directly beside it with the same facing to form a row. Matching housings join automatically; removing a lane restores exposed end trims. Gates facing different directions do not join.

## Redstone

Power opens a lane; removing power closes it unless an active ticket window keeps it open. Supply redstone power to either its lower or upper cell, for example from a powered solid block below it. Each lane reads its own redstone input. Joining does not pass power between gates.

Minecraft redstone can still power several neighbours through ordinary wiring. Use separate inputs and suitable wire isolation when controlling neighbouring lanes independently. The indicator turns green for an opening/open target and red for a closing/closed target. Paddles take about 0.6 seconds to travel fully; passage collision clears near the end of opening and returns early in closing. The housings always remain solid.

## Wrench and removal

Normal Create wrench-click rotates a standalone lane by 90 degrees. Separate it from its row first; rotation also refuses an orientation that would join another lane. Sneak-wrench-click either half to pick up the whole lane as one item. Breaking either half removes both and yields one item in survival. Pistons cannot move it.

## Crafting

```text
IYI
BRB
I I
```

I: iron ingot; Y: yellow dye; B: iron bars; R: redstone dust. Makes one complete lane.

## In-game acceptance

On matching server and client JARs, place a standalone gate and a row of three. Power only the middle lane, including via its upper half, and verify animation, indicators and walking collision. Test rapid power reversals, breaking/picking up either half, neighbour removal, four headings, reload and multiplayer. Automated geometry/resource tests are not a substitute for these native checks.

## Tickets

A [Rail Ticket](Tickets.md) opens the clicked lane for five seconds. The Ticket Machine dispenses tickets for free. No ticket is spent while a lane is already open by ticket or redstone.
