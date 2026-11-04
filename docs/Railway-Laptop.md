# Railway laptop

The **Railway Laptop** is a placeable desk computer for the network map, information screens and editable text boards. Install the same updated mod JAR on the server and every client.

## Craft and use

Craft one laptop in a crafting table:

```text
GEG
IPI
IRI
```

G = glass pane; E = Create electron tube; I = Create iron sheet; P = Create precision mechanism; R = Create redstone link.

Place it on a full-block desktop, with its open screen facing you. Right-click to open the dashboard. The laptop supports Create wrench rotation and sneak-wrench pickup.

## Find and name boards

The dashboard lists Station Information Boards, Railway Computer/map controllers and editable text signs. Search by custom name, type, dimension or coordinates. Unnamed devices have a type-and-coordinate label. Select a device, enter a **Device name** such as `Norwich / Platform 1 / Departures`, then choose **Save**. Names may contain up to 64 characters.

Each list card shows the actual block-item symbol, its management name, its specific type and its availability/distance. Platform signs, wayfinding signs, speed limits, signal nameplates, crossing notices and classic/modern station signs are identified separately. The detail area describes the selected device, its location, current text and service settings where applicable. Refreshes retain unsaved edits; successful saves reload the stored values.

Management names are separate from passenger-facing station headings and displayed sign text. Duplicate names are allowed; the list tooltip shows the dimension and location to distinguish them. Display Tiles belong to their controller rather than appearing as separate devices.

You can also name a device without a laptop: open its ordinary empty-hand editor and choose **Device name**. This is available on text signs, information-board settings and the local Railway Computer/map screen. Enter the management name and save, then return to the same editor with its unfinished text/settings preserved. Naming through a valid display tile names its controller; the server verifies the current assembly and interaction permissions.

Use the page arrows for more devices, scroll within the list to see every row on a page, and choose Refresh to update loaded status or changes made by another player. The saved directory contains up to 8,192 devices, with 12 entries per page.

Existing boards register when their chunks first load after installing this update. The directory survives server restarts and keeps known unloaded boards visible as **Offline**. Remote actions never force-load chunks. Offline devices cannot be renamed or edited until their chunks are loaded normally.

## Highlight a device in the world

Select a device and switch **Highlight: On**. Close the laptop to see a bright outline/locator column plus a HUD readout with the device name, type, coordinates and distance. The outline is visible through surrounding blocks, making screens inside station buildings easier to find. Selecting another laptop entry while highlighting follows that selection. Switch **Highlight: Off** in the laptop to stop it.

The locator remains active after closing the laptop or walking away from the desk. Targets in another dimension show that dimension until you travel there. Offline/unloaded locations remain coordinate markers; the locator never loads chunks. A confirmed removed or replaced device clears its marker, and disconnecting clears the locator. It is a visual aid and does not move the player or alter any blocks.

## Network map

Choose **Network map** to open the existing interactive railway map. Pan, zoom, select trains/stations/signals, switch dimensions and toggle layers as on the Railway Computer. Close the map to return to the laptop dashboard. The map's last view is retained while this laptop session remains open.

Select a Railway Computer/map controller and choose **Map view** to change that screen's saved viewport remotely. Closing its map editor saves the chosen view to that controller. Existing display tiles use the controller's saved view.

## Information screens

Select an information board and choose **Settings** to edit its passenger-facing heading, arrivals/departures/both mode, platform/concourse layout and station group. The station picker uses the board's dimension and its existing 128-block station-link range. A laptop does not enlarge that link range.

For custom notices, set **Text: On**, enter up to four lines of text, and choose **Save**. Each line allows up to 120 characters, with a total limit of 512 UTF-16 characters. The world display uses the existing amber dot lettering. Long messages wrap to the screen width; screens too short for all wrapped lines advance through them every four seconds.

Manual text works on board and map controllers, including their attached display tiles. Set **Text: Off** and save to return to live services or the map. The normal station settings and viewport remain stored while custom text is displayed.

## Text boards and signs

Select a text panel to edit its displayed message and management name. Existing sign rules remain in effect: station/platform/wayfinding signs allow their normal text, crossing notices keep their supported punctuation/line separators, signal nameplates keep their character restrictions, and speed signs require a valid numeric speed. Invalid saves report an error and retain the draft for correction.

Regular empty-hand, on-block editors still work. Custom management names and information-screen messages survive saves and wrench pickup. A newly placed/picked-up device receives a fresh management identity, preventing a stale laptop selection from editing a replacement block.

## Access and validation

Remain within eight blocks of the laptop in the same dimension. Moving away, changing dimension, removing the laptop or letting the session expire revokes access. Editing requires build permission and the normal target interaction/world-border checks. Loaded devices can be managed across dimensions; protected or unavailable targets remain read only.

Automated checks cover directory persistence, names/text limits, bounded packets, amber text rendering, portable configuration, distant edits, target replacement, laptop removal, forged tokens, unloaded targets and same-tick refresh/save behaviour. Live multiplayer UI layout and modpack claim integrations remain gameplay acceptance checks.
