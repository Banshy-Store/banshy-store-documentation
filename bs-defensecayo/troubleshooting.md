# Troubleshooting

## No AI spawns
- Ensure zones are enabled in `Config.Zones` and you are within the engage radius
- Confirm island IPLs are loaded and the resource is started after map loading

## Guards do not engage
- Increase `Config.Guards.Accuracy` and verify `engageRadius` for zones
- Check relationships/hostility settings inside the script (debug logs)

## Over‑spawning or performance drops
- Lower `units` per zone/patrol and increase respawn cooldowns
- Reduce `Config.Spawn.MaxUnits` and disable unused zones

## Boats or vehicles not appearing
- Verify spawn coordinates and water/ground checks in your config
- Reduce counts if areas are crowded or colliding with other resources

## Respawn not happening
- Ensure `RespawnCooldownSeconds` is not set too high
- Verify that cleanup/respawn handlers are enabled in your configuration

## Getting logs for support
- Enable `Config.Debug = true` and reproduce once
- Share server console + client F8 logs and relevant config sections


