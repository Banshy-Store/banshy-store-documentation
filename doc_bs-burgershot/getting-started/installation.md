# Installation

Follow this step-by-step guide to install and verify `bs-burgershot`.

## 1) Prerequisites
- Framework: ESX, QB, or QBOX
- Dependencies: `ox_lib`, `ox_target`
- Inventory backend: QS, OX, QB, or native ESX

Start order in `server.cfg`:

```cfg
ensure ox_lib
ensure ox_target
ensure bs-burgershot
```

## 2) Framework selection (optional)
Open `shared/config.lua` and set:

```lua
BSConfig.Framework = 'auto' -- or 'esx' | 'qb' | 'qbox'
```

Auto mode is recommended.

## 3) Inventory setup
- QS: merge `install/qs_inventory_items.lua` into QS items; copy `install/images/` to your inventory UI images
- OX: merge `install/ox_inventory_items.lua` into `ox_inventory` data items
- QB: supported automatically by the bridge
- ESX native: import `install/items_burgershot_esx_weight.sql`

## 4) Database and society
Ensure your job and society match the config:

```lua
BSConfig.JobName = 'burgershot'
BSConfig.SocietyName = 'society_burgershot'
```

## 5) Verify in game
1. Join with an admin account.
2. Set your job to `BSConfig.JobName`.
3. Interact with `BSConfig.Points` via `ox_target`.
4. Run a full flow: cut → cook → assemble → drinks → customer order → payment.

## 6) Troubleshooting
- Interactions missing: confirm `ox_target` is started and your points/zones exist in config.
- Items missing: verify your inventory integration from step 3 and that images/snippets were copied.
- Society money not updating: check `BSConfig.SocietyName` and framework logs.
- Language: toggle with `BSConfig.Locale = 'en'|'fr'`.
