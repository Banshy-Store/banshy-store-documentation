# FAQ

## Do I need to build the UI?
No. Only if you modify `web/`. A built version ships with the resource.

## ESX or QBCore compatible?
Both. Set framework options in `shared/config.lua`. Bridges unify callbacks and identifiers.

## How do I add vehicles?
- `Config.VehicleSource = 'config'`: edit `shared/vehicles.lua`
- `sql`: use ESX `vehicles` table

## Where are logs/webhooks?
Use your own webhook via server events or integrate with a logging script. Dedicated webhook integration may be added later.
