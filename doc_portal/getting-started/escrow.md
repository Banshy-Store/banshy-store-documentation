## Understanding FiveM asset escrow system

The FiveM asset escrow system secures assets by encrypting critical files, ensuring that exclusive Quasar Store assets are protected against unauthorized use or modification. Below is a detailed guide to common errors and solutions, with titled sections for clarity.

### Failed to Verify Protected Resource
This error usually means the files were corrupted during transfer.

**Error**
Failed to verify protected resource (qs-resourceName).

**Cause**
Files were corrupted during transfer.

**Solution**
- Ensure all files, including `.fxap`, are uploaded correctly.
- Use WinSCP instead of FileZilla for transferring files, as FileZilla might skip encrypted components.

### Missing Required Entitlement
This error occurs when your server license key is not linked to the account that purchased the asset.

**Error**
You lack the required entitlement to use qs-resourceName.

**Cause**
Server license key does not match the account that purchased the asset.

**Solution**
- Verify that your server license key in Keymaster matches the one used during purchase.
- Restart your server after installation to apply any changes.

### Syntax Errors
This error can be caused by several factors:

**Error**
Syntax error </1> or similar issues.

**Cause**
Outdated artifacts or attempts to edit encrypted code.

**Solution**
- Update to artifact version 4960 or newer.
- Avoid editing encrypted files, as this will damage the asset.
- Restart your server to resolve initialization issues.

### Recommendations

**Use the Latest Artifacts**
Always run artifact version 4960 or higher to avoid compatibility problems.

**Use Reliable File Transfer Tools**
Switch to WinSCP for file uploads to ensure `.fxap` files and other encrypted components aren't skipped.

**Avoid Editing Encrypted Code**
Never attempt to modify encrypted files. If customizations are needed, refer to documentation or contact support.

**Restart Your Server Regularly**
After installing or updating assets, restart your server to ensure all changes are applied and potential errors are resolved.
