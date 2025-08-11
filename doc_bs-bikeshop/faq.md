# FAQ

## Which inventories are supported?
QS Inventory, OX Inventory, and native ESX (SQL items). Auto selection or forced via `Config.Inventory`.

## Can I limit one bike per player?
Yes: `Config.Restrictions.singleBikePerPlayer = true`.

## Do I need QS images?
Only if you use QS Inventory. Copy from `install/items/` to your QS images folder.

## How do I add a new bike?
Add the item to your inventory, include it in `Config.Restrictions.bikeItems`, and optionally in `Config.Products` for the built‑in shop.
