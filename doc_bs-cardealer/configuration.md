# Configuration

![Banshy](../assets/banshy128.webp)

All options live in `shared/config.lua` and include inline tips. This page explains every setting with examples.

## Locale
- `Config.Locale`: 'en' | 'fr'

Example:
```lua
Config.Locale = 'en'
```

## Job
- `Config.JobName`: Framework job name authorized to sell
```lua
Config.JobName = 'cardealer'
```

## UI & Keybinds
- `Config.UI`: Command and key mapping toggle
- `Config.Keybinds`: Centralized binds buyers can remap in FiveM settings

```lua
Config.UI = {
  EnableCommand = true,
  OpenCommand = 'catalogue',
  EnableKeyMapping = true,
  OpenKey = 'F6'
}

Config.Keybinds = {
  CatalogOpen = { command = 'catalogue', defaultKey = 'F6', description = 'Open vehicles catalog' },
  CatalogClose = { command = 'closecatalog', defaultKey = 'F7', description = 'Close vehicles catalog' },
  TestDriveCancel = { command = 'canceldrive', defaultKey = 'X', description = 'Cancel test drive' }
}
```

## Sale Rules
- `Config.Sale`:
  - `DefaultCommissionRate`, `MinCommission`, `MaxCommission`
  - `MinSellerGrade`: minimal job grade to sell
  - `MinPrice`, `MaxPrice`
  - `DeliveryTypesEnabled`: toggle features

```lua
Config.Sale = {
  DefaultCommissionRate = 0.10,
  MinCommission = 0.00,
  MaxCommission = 0.30,
  MinSellerGrade = 0,
  MinPrice = 100,
  MaxPrice = 5_000_000,
  DeliveryTypesEnabled = {
    automatic = true,
    pickup = true,
    import = true,
    container = true
  }
}
```

## Timings
- `Config.DeliveryDelaySeconds`: auto delivery ETA after invoice
- `Config.ImportPreparationSecondsMin/Max`: pickup preparation window
- `Config.TestDriveSeconds`: test drive duration

## Debug
- `Config.Debug`: verbose logs both client/server

## Integrations
- `Config.Integrations`:
  - `Billing`: 'auto' | 'bs-billing' | 'esx_billing' (fallback immediate payment if none)
  - `Inventory`: 'auto' | 'ox_inventory' | 'qs-inventory' | 'qb-inventory' | 'esx'
  - `Keys`: 'auto' | 'sna' | 'none'

## Showroom & Interaction Points
- `Config.Showroom`: vehicle positions and tablets
- `Config.SalePoints`: points to start/cancel sale
- `Config.DeliveryPoints`: dealership delivery spots
- `Config.PickupPoints`: importer pickup spots
- `Config.FlatbedSpawn`, `Config.FlatbedTarget`: flatbed spawn and interact zone
- `Config.ContainerDelivery`: port/handler flow

## Server Toggles
- `Config.ServerSpawnVehicles`: false by default; vehicles spawned client-side with server validations
- `Config.DeliveryCheckRadius`: zone radius for server-side checks
- `Config.VehiclePersistence`: 'auto' (ESX owned_vehicles) | 'none'
- `Config.VehicleSource`: 'sql' (ESX `vehicles` table) | 'config' (`shared/vehicles.lua`)

## Recommended Baseline
```lua
Config.Locale = 'en'
Config.VehicleSource = 'config'
Config.VehiclePersistence = 'none'
Config.Sale.MinSellerGrade = 1
Config.Sale.DeliveryTypesEnabled.container = false
Config.Debug = false
```

