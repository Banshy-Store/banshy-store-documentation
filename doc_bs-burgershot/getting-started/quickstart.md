# Quick Start

- Start your server and join with an admin account.
- Set your job to `BSConfig.JobName` (default `burgershot`).
- Use ox_target interactions at `BSConfig.Points`.
- Try: cut → cook → assemble → drinks → customer order → pay.
- Toggle language by setting `BSConfig.Locale = 'en'|'fr'`.

## Post-install checklist
- Interactions appear at all configured `BSConfig.Points`.
- Items and recipes load correctly for your chosen inventory backend.
- Boss, outfits, customer menu, and checklist work as configured.
- Webhooks (if configured) receive events.
- No client/server errors with `BSConfig.Debug = true` during a full service flow.

## Support-ready info
When requesting help, include:
- Framework and inventory, artifacts/gamebuild, OS
- `server.cfg` ensure order for dependencies and `bs-burgershot`
- Relevant `shared/config.lua` sections (framework, inventory, points, webhooks)
- Server console + client F8 logs
- Steps to reproduce and what you already tried