# Quickstart

![Banshy](../assets/banshy128.webp)

1) Install dependencies
- Start `ox_lib` before `bs-defensecayo` (optional but recommended)

2) Configure
- Open `shared/config.lua`
- Enable desired zones: villa, docks, runway, secondary entrance
- Set patrol density, respawn timers, guard loadouts, and accuracy/armor

3) Start resource
- Add to `server.cfg`: `ensure bs-defensecayo`

4) Test
- Approach each zone; confirm patrols spawn and engage properly
- Validate respawn works and counts stay within your configured limits

## Post‑install checklist
- Zones enabled and spawning correctly
- Patrols active (land/sea/vehicle) without over‑spawning
- Guard weapons and armor aligned with your server’s balance
- Respawn cooldowns tuned for performance and fairness
- Debug disabled for production use

## Support‑ready info
When requesting help, include:
- Artifacts/gamebuild and OS
- `server.cfg` ensure order
- Relevant parts of `shared/config.lua`
- Server console + client F8 logs
- Steps to reproduce and what you already tried


