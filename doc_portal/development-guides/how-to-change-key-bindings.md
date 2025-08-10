# How to change key bindings

To properly organize your keybinds and optimize your resource, use the FiveM native `RegisterKeyMapping`. This eliminates while-loop key checks and improves performance by triggering a command when the keybind is pressed.

Note: new keybinds apply only to new players or players who reset their keybinds manually.

## Why use RegisterKeyMapping?
- Optimized performance: reduces resource usage by removing frame-by-frame checks.
- Client customization: players can change their own keybinds directly in-game.

## Basic usage example
```lua
-- Create a command your keybind will trigger
RegisterCommand('openMyMenu', function()
  -- open your menu here
end, false)

-- Map the command to a default key (players can customize later)
RegisterKeyMapping('openMyMenu', 'Open My Menu', 'keyboard', 'F10')
```

## How to change keys in-game
1. Open the GTA V Settings menu.
2. Go to Key Bindings.
3. Open the FiveM section.
4. Adjust your keybinds as desired.

## How to reset keybinds
If you need to reset your keybinds, choose one of the following:

### Using console (F8)
- Example to unbind F10:
```text
unbind keyboard f10
```
- Generic syntax:
```text
unbind keyboard [key]
```

### Editing configuration file
1. Go to `C:\Users\[USERNAME]\AppData\Roaming\CitizenFX`.
2. Open `fivem.cfg`.
3. Remove lines related to the resource/command you mapped.
4. Restart FiveM.

Last updated: today

## Media
- Video: [Placeholder – changing keybinds in Settings]
- Screenshots: [Placeholder – FiveM keybind menu]


