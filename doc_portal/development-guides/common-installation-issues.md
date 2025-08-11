# Common installation issues

A quick reference for the most frequent setup problems across our scripts.

## Resource won’t start
- Ensure order in `server.cfg` (dependencies before the script)
- Verify folder names are unmodified (for example, `qb-core`, `es_extended`)
- Update to recent artifacts and set a current `sv_enforceGameBuild`

## Missing required entitlement
- Confirm your Keymaster `sv_licenseKey` belongs to the purchasing account
- Fully restart the server after changing the key
- See also: Getting Started → CFX Auth

## ox_lib / oxmysql / ox_target errors
- Confirm they are ensured before the script
- Check versions; update to latest releases
- For `oxmysql`, verify database credentials and connectivity

## No such export / nil value
- Mismatched framework/inventory choice; align `Config/BSConfig` with your stack
- Wrong folder names for framework or inventory

## UI doesn’t show (NUI)
- If you edited `web/`, rebuild: `npm i && npm run build`
- Check client F8 console and browser devtools logs

## SQL / Items missing
- For ESX SQL sources, ensure tables exist and migrations/snippets were applied
- For inventory images (QS), copy images to the correct folder

## Delivery/Interaction not working
- Verify points/zones exist in config and you are within range
- Check server logs; enable Debug to see validations

## Still stuck?
- Gather server logs, client F8 logs, your `server.cfg` ensure order, and relevant config snippets, then open a support request.
