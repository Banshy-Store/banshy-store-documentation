## What is CFX Auth?

CFX Auth is the authentication and entitlement system used by Cfx.re (FiveM). It ties your purchased assets and server permissions to your Cfx.re account via Keymaster. Protected resources (escrowed assets) require that the server running them has a valid license key associated with the account that owns the entitlement.

### How it works (at a glance)
- Your purchase creates an entitlement on your Cfx.re account.
- Your server uses an `sv_licenseKey` (Keymaster) to authenticate.
- When a protected resource starts, the platform verifies the server's license key against the owning account's entitlements.

### Requirements
- A valid server license key created in Keymaster under the owning account
- The server configured with `sv_licenseKey` matching that key
- Internet connectivity so the server can validate entitlements

### Verify your setup
1. In Keymaster, confirm the server license key exists under the same Cfx.re account that purchased the asset.
2. In your `server.cfg`, set `sv_licenseKey` to that exact key (no spaces, no quotes).
3. Restart the server entirely (not just a resource restart) to refresh entitlements.

### Common issue: Missing Required Entitlement
If you see “You lack the required entitlement to use <resource>”:
- Ensure the server license key belongs to the account that purchased the asset.
- If you moved ownership or changed the key, restart the server after updating `sv_licenseKey`.
- See also: [Understanding FiveM asset escrow system](escrow.md).


