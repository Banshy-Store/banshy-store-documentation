# How to set RTC Server

Set up real-time communication (RTC) for in-game voice or other features used by your server resources.

## Choose your voice solution
- pma-voice, mumble-voip, or third‑party solutions. Follow their official setup docs.

## Configure server convars
- In `server.cfg`, set the convars required by your chosen voice resource (for example, endpoints, ws/udp ports, sample rates).

## Open firewall/ports
- Allow the UDP/TCP ports your voice/RTC stack requires on your host and provider panel.

## Verify client connection
- Join the server and ensure the voice HUD/indicators show connected.
- Check console logs for connection or ICE errors.

## Troubleshooting
- Update to recent artifacts and use OneSync.
- Confirm no conflicting voice resources are running simultaneously.
- Validate that ports are not blocked by firewall or host.

Last updated: today


