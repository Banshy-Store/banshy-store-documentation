# Troubleshooting

## Catalog is empty
- If `Config.VehicleSource = 'sql'`, ensure ESX `vehicles` table exists and `oxmysql` is configured
- Try `Config.VehicleSource = 'config'` to validate setup quickly

## Cannot sell / buttons disabled
- Your job must match `Config.JobName` and grade meet `Config.Sale.MinSellerGrade`
- Check `Config.UI` and `Config.Keybinds`

## Delivery not triggering
- Check `Config.Sale.DeliveryTypesEnabled` toggles
- Review server logs; enable `Config.Debug = true`

## NUI not opening
- If you modified `web/`, rebuild (`npm i && npm run build`)
- Check client F8 for errors

## Billing not applied
- Set `Config.Integrations.Billing` to `bs-billing` or `esx_billing`, or rely on immediate payment fallback

## Vehicle persistence
- If using ESX persistence, set `Config.VehiclePersistence = 'auto'` and ensure DB tables exist
