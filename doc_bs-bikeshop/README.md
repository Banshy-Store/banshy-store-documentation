# BS-BikeShop

![Banshy Store](../assets/banshy400.webp)

Turn bikes into real items: buy, spawn with one click, pack via ox_target. Compatible with QS Inventory, OX Inventory, and native ESX. Ideal to monetize your server with a clean, performant, and abuse‑resistant experience.

### Why bs-bikeshop?
- Inventory‑agnostic: QS, OX, native ESX - auto‑select or force.
- Smooth experience: the item spawns the bike; an `ox_target` option lets you pack it.
- Anti‑abuse: owner + distance checks; optional 1 bike per player.
- Built‑in shop: ready‑to‑use `ox_target` zones (disabled by default).
- Localization: EN/FR included (+ 12 languages ready in `shared/locales.lua`).

### Compatibility
- Framework: ESX, QB/QBX (via money bridge), standalone (limited features)
- Inventories: **qs-inventory**, **ox_inventory**, **native ESX** (items in SQL)
- Dependencies: `ox_lib`, `ox_target`

### Overview of contents
- `client/` spawn/pack logic, `ox_target`
- `server/` validations, purchases, inventory and money bridges
- `shared/config.lua` full configuration (shop, items, spawn, pack…)
- `shared/locales.lua` translations and helper `T()`
- `install/` QS/OX item snippets, ESX SQL, item images

### Quickstart (summary)
1) Place the resource and ensure order in `server.cfg`:
   - ensure ox_lib
   - ensure ox_target
   - ensure bs-bikeshop
2) Integrate the items for your inventory (QS/OX/ESX). The snippets are in `install/`.
3) Give yourself an item (e.g., `bmx`), use it to spawn, target the bike to pack.

Go further:
- Step‑by‑step setup: see [Installation](installation.md)
- Settings & customization: see [Customisation](customisation.md)


