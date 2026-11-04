# Tickets and Ticket Machine

Rail Tickets have the classic orange-and-cream UK paper-ticket appearance. Every ticket works at every Ticket Barrier; there are no destinations to configure, fares or station restrictions.

## Get tickets

Place a Ticket Machine on solid ground with two blocks of vertical space. Right-click either half to receive one free ticket. You can use it without operator or building permission, subject to normal server interaction protection. A full inventory produces a message and no loose dropped ticket. Space in a partial ticket stack, including the offhand, is used normally.

Both Ticket Machine and Rail Ticket appear in the UK Railways creative tab. You can also craft four tickets from paper beside orange dye, or craft a machine with:

```text
IGI
YRY
IPI
```

I: iron ingot; G: glass; Y: yellow dye; R: redstone dust; P: paper.

## Use a ticket

Hold a ticket in either hand and right-click either half of a closed Ticket Barrier. One ticket is consumed and only that lane opens for five seconds, including its opening animation. Creative players keep their ticket stack.

An already active ticket window or redstone-powered gate does not consume another ticket or extend the timer. Redstone and tickets are independent opening inputs: a powered gate stays open when the ticket expires, while removing power during a valid ticket window leaves it open until expiry.

Timer expiry uses server game time, survives saving/loading and is checked when a gate's chunk loads. A gate does not retain temporary ticket access when picked up with the Create wrench. Existing gates accept tickets automatically after updating the server and clients; no linking or replacement is required.

## Machine wrench support

Normal Create wrench-click rotates the complete machine. Sneak-wrench-click either half picks up one machine item. Breaking either half removes both with one survival drop. Ticket Machines have no stock inventory to refill.

## Acceptance checks

Test main/offhand ticket use, both gate halves, single-lane behavior in a row, repeated use, timed closing and redstone override. Test machine dispensing while holding different items, a full inventory and partial/offhand stacks, spectator/creative/adventure modes, whole-machine wrench pickup, chunk unload/reload and multiplayer. Automated policy/resource checks do not replace native interaction and animation checks.
