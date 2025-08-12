# Troubleshooting

## No "Pack the bike" option
- Confirm `ox_target` is running and model is supported
- Check `Config.Pack.enable` and distances

## Item not returned
- Inventory capacity (weight/slots) may be full
- Script checks capacity before vehicle deletion

## Duplicate bikes
- Enable anti‑abuse: `Config.Restrictions.singleBikePerPlayer = true`

## Shop does not open
- Ensure `Config.EnableBuiltInShop = true` and zones defined in `Config.Locations`

## Items not usable
- Verify item names match config and inventory snippets were applied
