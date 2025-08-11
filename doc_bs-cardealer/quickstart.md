# Quick Start

1) Install dependencies
- Ensure `ox_lib`, `oxmysql`, `ox_target` are started before `bs-cardealer`
- Optional: `esx_billing` or `bs-billing` for real invoices (not required)

2) Configure
- Open `shared/config.lua`
- Set `Config.Locale` (`en` or `fr`)
- Choose `Config.VehicleSource = 'config'` (no SQL) or `'sql'` (ESX `vehicles`)
- Set job name, delivery modes, keybinds, and toggles

3) Start resource
- Add to server.cfg: `ensure bs-cardealer`

4) Build NUI (only if you edit web/src)
- cd `web` → `npm i` → `npm run build`

5) Test
- Use the showroom and tablets, start a sale, pay invoice (or fallback), verify delivery

## Post-install checklist
- Job is correctly set to `Config.JobName` and seller grade meets `Config.Sale.MinSellerGrade`.
- Catalog opens and lists vehicles from your chosen source (`config` or `sql`).
- All delivery types you enabled in `Config.Sale.DeliveryTypesEnabled` work end‑to‑end.
- Billing integration behaves as expected or falls back to immediate payment.
- Keybinds (open/close, cancel test drive) are recognized.
- No client/server errors with `Config.Debug = true` during a smoke test.

## Support-ready info
When requesting help, include:
- Framework and versions, artifacts/gamebuild, OS
- `server.cfg` ensure order for dependencies and `bs-cardealer`
- Relevant parts of `shared/config.lua`
- Server console + client F8 logs
- Steps to reproduce and what you already tried

