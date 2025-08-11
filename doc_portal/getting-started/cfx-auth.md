# CFX Auth

CFX Auth is the Cfx.re (FiveM) authentication/entitlements system. It links your purchases and server permissions to your account via Keymaster. Protected resources (escrow) require a valid server license belonging to the owner account.

## How it works
- A purchase creates an entitlement on your Cfx.re account.
- Your server identifies with a Keymaster key `sv_licenseKey`.
- When a protected resource starts, the platform checks that the server key matches the owner's entitlements.

## Prerequisites
- A valid Keymaster server key on the buyer's account
- `server.cfg` configured with this key
- Internet connectivity on the server side

## Quick setup
1. Create (or retrieve) your server key in Keymaster from the buyer's account.
2. In `server.cfg`, add:

```cfg
sv_licenseKey YOUR_KEYMASTER_KEY
```

3. Fully restart the server (not just the resource).

## Troubleshooting: Missing Required Entitlement
If you see "You lack the required entitlement to use <resource>":
- Verify that the server key belongs to the account that purchased the resource.
- Update `sv_licenseKey` if the key changed, then restart the server.
- See also: [Understanding FiveM asset escrow system](escrow.md)

## Media
- Screenshots: [Placeholder – Keymaster, adding the key]
