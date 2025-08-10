# bs-cardealer

A modern, secure, tri-framework car dealership resource for FiveM.

- Framework-ready: ESX, QBCore, QBX (via internal Bridge)
- Zero hard dependency on billing (auto/esx_billing/bs-billing/fallback)
- Configurable catalog (SQL or config file), locales (EN/FR), keybinds
- Seller workflow with multiple delivery modes and robust server validations

## Highlights

- Config-first: see `shared/config.lua` with inline tips
- Tri-framework: server callbacks, jobs, identifiers unified via Bridge
- Secure by default: cooldowns, zone re-check server-side, model validation
- Optional persistence: ESX `owned_vehicles` or disabled
- NUI built with React, shipped via `web/build`

## Requirements

- ox_lib
- oxmysql
- ox_target
- FiveM (Cfx.re) server

Optional: esx_billing, bs-billing, sna-vehiclekeys, ox_inventory / qs-inventory / qb-inventory

## Getting Help

Use Troubleshooting and FAQ pages, or open an issue with logs and config.

