# Installation

![Banshy](../assets/banshy128.webp)

Follow this guide to install and verify `bs-defensecayo` on your FiveM server.

## 1) Prerequisites
- Framework: **ESX** (standalone friendly)
- FiveM server with a valid Keymaster license and recent artifacts

Recommended start order in your `server.cfg`:

```cfg
ensure ox_lib
ensure bs-defensecayo
```

> If you do not use `ox_lib`, you can still run the script; adjust dependencies accordingly.

## 2) Drop the resource
Place the `bs-defensecayo` folder inside your server `resources` directory. Keep the folder name as‑is.

## 3) Configure the script
Open `shared/config.lua` and review key settings:
- `Config.Framework = 'esx' | 'standalone'`
- `Config.Zones` (villa, docks, runway, secondary entrance, etc.)
- `Config.Patrols` (land/sea/vehicle), unit counts, routes, respawn cooldowns
- `Config.Guards` loadouts (rifles, snipers, RPGs), armor/health
- `Config.HeavySupport` (mounted/static weapons, technicals, armed boats)

Save the file after adjustments.

## 4) Start the resource
Add (or confirm) in `server.cfg`:

```cfg
ensure bs-defensecayo
```

Restart your server.

## 5) Verify in game
1. Fly to Cayo Perico.
2. Approach any configured defense zone (e.g., villa or docks).
3. Confirm patrol presence, guard engagement, and respawn behavior.

## 6) Troubleshooting quick tips
- No AI spawns: validate `Config.Zones` are enabled and your island IPLs are loaded.
- Guards not aggressive: check accuracy/armor settings and engagement distance.
- Performance spikes: reduce unit counts or patrol density and disable debug.

