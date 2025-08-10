# Installation

1) Ensure order in server.cfg:
- ensure ox_lib
- ensure ox_target
- ensure bs-burgershot

2) Framework selection (optional):
- In `shared/config.lua`, set `BSConfig.Framework = 'auto'|'esx'|'qb'|'qbox'` (auto recommended).

3) Inventory:
- QS: merge `install/qs_inventory_items.lua` into qs-inventory items; copy `install/images/` to your inventory UI images.
- OX: merge `install/ox_inventory_items.lua` into ox_inventory data items.
- QB: qb-inventory supported (auto-detected in bridge).
- ESX native: import `install/items_burgershot_esx_weight.sql`.

4) Database (job/society):
- Ensure job name and society match `BSConfig.JobName` / `BSConfig.SocietyName`.
