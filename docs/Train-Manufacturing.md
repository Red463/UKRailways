# Train manufacturing

Train kits are manufactured from components using Create deployers and a mechanical press. All seven vehicle sequences have one loop and one guaranteed output; there are no scrap outcomes. Existing kit IDs and placement behaviour are preserved.

## 1. Craft shared components

Every recipe below produces one component. [Crafting-table patterns](Crafting.md) list the exact layouts.

| Component | Ingredients |
|---|---|
| Train Chassis | 4 × Iron Block, 2 × Sturdy Sheet, 2 × Railway Casing, 1 × Shaft |
| Modern Bogie Assembly | 2 × Iron Block, 1 × Iron Sheet, 2 × Shaft, 1 × Railway Casing, 2 × Cogwheel |
| Train Bodyshell | 6 × Iron Sheet, 2 × White Concrete, 1 × Red Dye |
| Compact Train Bodyshell | 4 × Iron Sheet, 2 × White Concrete, 1 × Red Dye |
| Passenger Interior Pack | 3 × Glass, 2 × Red Seat, 1 × White Wool, 3 × Iron Sheet |
| Small Passenger Interior Pack | 2 × Glass, 1 × Red Seat, 1 × White Wool, 2 × Iron Sheet |
| Cab Equipment Pack | 2 × Glass, 1 × Electron Tube, 2 × Brass Sheet, 1 × Precision Mechanism, 2 × Controls, 1 × Redstone Link |
| Traction Equipment Pack | 2 × Copper Block, 2 × Precision Mechanism, 2 × Shaft, 1 × Sturdy Sheet, 2 × Electron Tube |
| Generator Equipment Pack | 2 × Fluid Tank, 1 × Electron Tube, 2 × Precision Mechanism, 1 × Mechanical Bearing, 2 × Copper Block, 1 × Shaft |
| Service Equipment Pack | 2 × Glass, 1 × Fluid Tank, 2 × Smoker, 1 × Crafting Table, 3 × Iron Sheet |

## 2. Configure a vehicle chassis

Craft a shared Train Chassis with the listed equipment. The resulting named chassis selects the exact vehicle assembly; a generic chassis cannot enter these sequences.

| Vehicle chassis | Add to one Train Chassis |
|---|---|
| Class 755 Driving Car | 1 × Cab Equipment Pack, 1 × Red Dye |
| Class 755 Passenger Car | 1 × Passenger Interior Pack, 1 × Red Dye |
| Class 755 Short Passenger Car | 1 × Small Passenger Interior Pack, 1 × White Dye |
| Class 755 Power Module | 1 × Generator Equipment Pack |
| Class 745 Driving Car | 1 × Cab Equipment Pack, 1 × Iron Block |
| Class 745 Passenger Car | 1 × Passenger Interior Pack, 1 × Iron Block |
| Class 745 Service Car | 1 × Service Equipment Pack, 1 × Passenger Interior Pack, 1 × Iron Block |

## 3. Run sequenced assembly

Place the configured chassis on a depot or belt beneath a deployer. Deploy the ingredients below in order, then process it under a mechanical press. Each listed deployment consumes one component; install the two bogie assemblies in two separate deployment operations. A repeated pass beneath a suitably supplied deployer can perform those two operations.

Use a depot/belt under the press, not a basin. Continue the same work-in-progress item through the sequence; do not substitute a fresh chassis. Create displays the native assembly progress bar. There is no additional fuel mechanic.

| Vehicle | Deploy in order, then press once |
|---|---|
| Class 755 Driving Car | Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Passenger Interior Pack → Traction Equipment Pack → Press |
| Class 755 Passenger Car | Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Press |
| Class 755 Short Passenger Car | Compact Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Press |
| Class 755 Power Module | Compact Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Press |
| Class 745 Driving Car | Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Passenger Interior Pack → Traction Equipment Pack → Press |
| Class 745 Passenger Car | Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Press |
| Class 745 Service Car | Train Bodyshell → Modern Bogie Assembly → Modern Bogie Assembly → Press |

## 4. Pack or place vehicles

Every individual vehicle kit can be placed directly on straight Create track. Alternatively combine completed kits in a crafting table:

| Output | Consumed contents |
|---|---|
| Class 755 Three-Car Train Kit | 2 × Class 755 Driving Car Kit, 1 × Class 755 Short Passenger Car Kit, 1 × Class 755 Power Module Kit |
| Class 755 Four-Car Train Kit | 2 × Class 755 Driving Car Kit, 2 × Class 755 Passenger Car Kit, 1 × Class 755 Power Module Kit |
| Class 745 Front Six-Car Pack | 1 × Class 745 Driving Car Kit, 4 × Class 745 Passenger Car Kit, 1 × Class 745 Service Car Kit |
| Class 745 Rear Six-Car Pack | 5 × Class 745 Passenger Car Kit, 1 × Class 745 Driving Car Kit |
| Class 745 Twelve-Car Intercity Train Kit | 1 × Class 745 Front Six-Car Pack, 1 × Class 745 Rear Six-Car Pack |

Packing is shapeless, produces one kit/pack and adds no material surcharge or discount. Six-car packs are inventory bundles, not placeable trains.

**To separate an unplaced complete kit or six-car pack, hold it and Shift-right-click in the air.** The held item is consumed even in Creative mode. Contents enter your inventory; anything that does not fit drops beside you. A complete Class 745 first separates into its front/rear packs; unpack each pack again to obtain all twelve vehicles. Individual vehicle kits cannot be unpacked into components.

This does not dismantle trains in the world. [Placement, assembly and scheduled reversal](Train-Kits.md) still use normal Create stations.

