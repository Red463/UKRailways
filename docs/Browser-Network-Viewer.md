# Remote read-only railway viewer

The viewer is bundled with the mod and disabled by default. Friends use a normal browser; they do not need Minecraft installed to view it. Minecraft players still need the mod. This repository does not configure or deploy your server automatically.

## Production setup

Use a hostname with HTTPS through your existing reverse proxy. The example below assumes a Linux VPS running Nginx. Keep the mod listener on loopback; only the HTTPS proxy should be publicly reachable.

1. Start the modded server once to generate `<world>/serverconfig/ukrailways-server.toml`, then stop it. This is a NeoForge per-world server configuration; replace `<world>` with the server's world directory. In singleplayer it is inside that save's `serverconfig` folder.
2. Set the following section, substituting your real HTTPS hostname:

```toml
[webViewer]
enabled = true
loopbackDevelopment = false
bindAddress = "127.0.0.1"
port = 8765
publicOrigin = "https://rail.example.com"
```

3. Point DNS at the VPS and configure a valid TLS certificate and reverse proxy. An adaptable [Nginx example](../examples/viewer.nginx.conf) is included. It replaces incoming forwarded-client headers with the actual peer address so login rate limiting can use it safely. Use the public hostname in the forwarded Host header.
4. Restart Minecraft and open `https://rail.example.com`. Confirm the sign-in form appears and `/api/snapshot` returns HTTP 401 before login. Do not expose port 8765 externally. No terrain files, world files or administrative endpoints are served.

Production requires an HTTPS public origin and a loopback bind. An invalid web configuration leaves Minecraft running with the optional listener disabled; inspect the UK Railways startup log. Changing listener settings requires a server restart.

For a local-only test, explicitly set `loopbackDevelopment = true`, keep a loopback bind, and use `http://127.0.0.1:8765`. Development cookies are separate from production Secure cookies.

## Invite friends

An in-game operator with permission level 2 runs:

```text
/ukrailways web invite Alex
/ukrailways web invite Alex 14
/ukrailways web list
/ukrailways web revoke <invitation-UUID>
```

The default invitation lasts seven days; the optional days value selects its lifetime. The invitation token appears once in a private Minecraft screen, with an explicit Copy token button. Give your friend the viewer homepage and token privately. Tokens are pasted into the sign-in form, never put in a URL. Console invitation creation is deliberately unavailable because console output is logged; listing and revoking are available to operators/console.

Each friend should have their own invitation for individual revocation. Successful login creates an HttpOnly, SameSite=Strict, Secure production cookie lasting up to 12 hours, bounded by invitation expiry. Logout clears the session. Revocation immediately invalidates that invitation's sessions; the next poll returns to sign-in. Restarting the server invalidates sessions; an unexpired invitation can sign in again.

Only invitation hashes and metadata are persisted in `config/ukrailways-viewer-auth.json`; sessions are memory-only. Keep that file private when copying server configuration. Tokens are not written to Minecraft chat, console logs, block NBT or browser local storage.

## What friends can see

The geographic map includes track, stations, directional signals, linked UK heads, live train and carriage symbols, occupied and reserved signal groups, and station arrivals/departures. It separates dimensions and marks portal endpoints. Panning, zooming, selection, a dimension selector and a keyboard-accessible entity picker are available. The browser polls every two seconds and marks stale/partial data. All data comes from detached server snapshots; HTTP workers never access Minecraft objects.

The service exposes no train controls, block editing or command execution. Login uses bounded POST requests, origin/host validation and rate limiting. API endpoints require authentication and support conditional snapshot requests.

## Acceptance on the VPS

Confirm HTTPS and Secure cookies in browser developer tools; verify unauthenticated API rejection; invite two friends separately; revoke one and check only that friend loses access; restart Minecraft and verify re-login; check stale status when the server stops. Test from outside the server network. Local automated tests do not prove DNS, your certificate, proxy or firewall configuration.

At detail zoom, carriage symbols follow their own track headings, with a distinct
leading end. Zoomed out, each train becomes one compact icon per visible dimension.
Train names stay in hover/selection details and the train picker instead of moving
text badges. Refresh an already-open viewer after updating the server JAR.

## Map controls

Use **World / dimension** to choose a named world. Vanilla worlds show Overworld, The Nether and The End; custom worlds include the full resource ID to distinguish similar names. Switching worlds fits that world's network and clears selection.

The **Layers** panel independently controls trains/carriages, Create signals, UK signals (repeaters), stations, names/labels and occupied/reserved track. Hiding a layer also removes its entities from hover and inspector lists. Names can be hidden while retaining marker hover details, and track occupancy remains independent of train visibility. Hidden selections clear automatically. The panel supports normal keyboard checkbox navigation and Escape/outside-click dismissal.

Preferences are remembered in browser local storage as visibility booleans only. This does not change authentication or store invitation tokens. Reload the page after installing the updated server JAR to load the controls. Minecraft clients also need the updated JAR for native computer/tablet controls.
