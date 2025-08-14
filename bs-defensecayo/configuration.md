# Configuration

![Banshy](../assets/banshy128.webp)

All options live in `shared/config.lua` and include inline tips. This page describes the main sections and recommended baselines.

## Framework
- `Config.Framework = 'esx' | 'standalone'`

```lua
Config.Framework = 'esx'
```

## Zones
Enable or tune defenses for key areas.
- `Config.Zones.Villa`, `Docks`, `Runway`, `SecondaryEntrance`, etc.
- Each zone can specify: unit count, spawn positions, engagement radius.

```lua
Config.Zones = {
  Villa = { enabled = true, units = 16, engageRadius = 55.0 },
  Docks = { enabled = true, units = 12, engageRadius = 50.0 },
  Runway = { enabled = true, units = 10, engageRadius = 60.0 },
  SecondaryEntrance = { enabled = true, units = 8, engageRadius = 45.0 }
}
```

## Patrols
- Land, Sea, Vehicle patrols with route lists and density.
- `Config.Patrols.Land|Sea|Vehicle`: per‑patrol unit count, route waypoints, loop/cooldowns.

```lua
Config.Patrols = {
  Land = { enabled = true, units = 6, route = 'island_ring', respawnSeconds = 45 },
  Sea = { enabled = true, units = 4, route = 'coastline', respawnSeconds = 60 },
  Vehicle = { enabled = true, units = 4, route = 'main_roads', respawnSeconds = 60 }
}
```

## Guards & Loadouts
- Accuracy, armor, health, and weapon sets (rifles, snipers, RPGs, mounted).

```lua
Config.Guards = {
  Health = 200,
  Armor = 100,
  Accuracy = 60, -- 0..100
  Loadouts = {
    rifle = { 'WEAPON_CARBINERIFLE', 'WEAPON_PISTOL' },
    sniper = { 'WEAPON_SNIPERRIFLE' },
    rpg = { 'WEAPON_RPG' }
  }
}
```

## Heavy Support
- Static emplacements and mobile units (technicals, barracks, armed boats).

```lua
Config.HeavySupport = {
  Mounted = { enabled = true, positions = { /* coordinates */ } },
  Technicals = { enabled = true, units = 2 },
  Boats = { enabled = true, model = 'dinghy5', units = 2 }
}
```

## Respawn & Performance
- Respawn cooldowns, maximum simultaneous units, and debug mode.

```lua
Config.Spawn = {
  MaxUnits = 64,
  RespawnCooldownSeconds = 30
}

Config.Debug = false
```

## Recommended Baseline
```lua
Config.Framework = 'esx'
Config.Zones.Villa.enabled = true
Config.Zones.Docks.enabled = true
Config.Zones.Runway.enabled = true
Config.Patrols.Land.units = 4
Config.Patrols.Sea.units = 2
Config.Patrols.Vehicle.units = 2
Config.Guards.Accuracy = 55
Config.Spawn.MaxUnits = 48
Config.Debug = false
```


