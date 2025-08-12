# How to change notifications

Configuring notifications in Banshy Store assets is simple. Notifications display information, success, and error messages in-game. They are centralized via a helper so you can switch systems without editing many files.

## Where to edit
- Files: `client/custom/framework/*.lua`
- Function: `SendTextMessage(message, messageType)`

This function is called by scripts whenever a notification is needed.

## Steps
1. Back up the original file.
2. Locate `SendTextMessage`.
3. Replace the current logic with your preferred notification export.
4. Save and test thoroughly.

## Template implementation
Adapt the export name/signature to your chosen notification resource.

```lua
function SendTextMessage(message, messageType)
  if messageType == 'inform' then
    exports['notify']:Send(message, 'info', 5000)
  elseif messageType == 'error' then
    exports['notify']:Send(message, 'error', 5000)
  elseif messageType == 'success' then
    exports['notify']:Send(message, 'success', 5000)
  else
    exports['notify']:Send(message, 'info', 5000)
  end
end
```

## Example using ox_lib

```lua
function SendTextMessage(message, messageType)
  local mappedType = 'inform'
  if messageType == 'error' then mappedType = 'error' end
  if messageType == 'success' then mappedType = 'success' end
  lib.notify({ description = message, type = mappedType, duration = 5000 })
end
```

## Good practices
- Keep the function name/signature the same.
- Centralize styling here; avoid calling exports across many files.
- Ensure the notification resource starts before dependent scripts.
- Test `inform`, `error`, and `success` branches.

Last updated: today


