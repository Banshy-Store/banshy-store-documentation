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

