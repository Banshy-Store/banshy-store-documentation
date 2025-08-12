# Installation

![Banshy](../assets/banshy128.webp)

Follow this step-by-step guide to install and verify `bs-cardealer` on your FiveM server.

## 1) Prerequisites
- Framework: ESX or QBCore/QBX (standalone is not recommended; sales, jobs, and money features rely on a framework)
- Dependencies: `ox_lib`, `oxmysql`, `ox_target`
- Optional (billing): `esx_billing` or `bs-billing` for real invoices; otherwise the script can fallback to immediate payment
- FiveM server with a valid Keymaster license and recent artifacts/gamebuild

Ensure start order in your `server.cfg`:

```cfg
ensure ox_lib
ensure oxmysql
ensure ox_target
ensure bs-cardealer
```

## 2) Drop the resource
Place the `bs-cardealer` folder inside your server `resources` directory. Keep the folder name as-is.

## 3) Configure the script
Open `shared/config.lua` and review these key settings:
- `Config.Locale = 'en' | 'fr'`
- `Config.JobName` for the dealership job
- `Config.VehicleSource = 'config' | 'sql'` (use `'config'` to avoid SQL setup; `'sql'` uses ESX `vehicles` table)
- `Config.Integrations.Billing = 'auto' | 'bs-billing' | 'esx_billing'` (falls back to immediate payment if none)
- `Config.Keybinds` and `Config.UI` as desired
- `Config.Sale` rules (commission, price limits, delivery types)

Save the file after adjustments.

## 4) Optional: NUI build
Only needed if you modify the React UI under `web/`.

```bash
cd web
npm i
npm run build
```

The built assets are shipped by default; you do not need to build if you don't change the UI.

## 5) Start the resource
Add (or confirm) in `server.cfg`:

```cfg
ensure bs-cardealer
```

Restart your server.

## 6) Verify in game
1. Set your player job to `Config.JobName` (e.g., via admin tool).
2. Go to the showroom/tablets and open the catalog.
3. Start a sale, choose a delivery type, and complete payment (billing or fallback).
4. Verify vehicle delivery according to the chosen delivery mode.

## 7) Troubleshooting
- NUI does not open: if you edited `web/`, run a fresh `npm run build`; check client console for errors.
- No vehicles listed: if `Config.VehicleSource = 'sql'`, ensure ESX `vehicles` table exists and `oxmysql` is configured; try `'config'` to validate quickly.
- Cannot sell: make sure your job matches `Config.JobName` and your grade meets `Config.Sale.MinSellerGrade`.
- Delivery does not trigger: verify `Config.Sale.DeliveryTypesEnabled` toggles and check server logs; enable `Config.Debug = true` temporarily.
- Billing not found: set `Config.Integrations.Billing` appropriately or use fallback immediate payment.

If issues persist, capture server/client logs and your `shared/config.lua` (sensitive values redacted) when requesting support.


