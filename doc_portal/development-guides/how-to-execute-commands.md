# How to execute commands

The `ExecuteCommand()` function lets you run any FiveM command directly from a script. It’s useful for automating tasks or triggering commands programmatically.

## Run a chat command
Sends a message to chat.

```lua
ExecuteCommand("say Hello, world!")
```

## Trigger a custom command
Runs a custom `/heal` command for player ID 1.

```lua
ExecuteCommand("heal 1")
```

## Create a shortcut command
Creates `/healMe` that heals the player who uses it.

```lua
RegisterCommand("healMe", function()
  ExecuteCommand("heal " .. GetPlayerServerId(PlayerId()))
end, false)
```

That’s it! `ExecuteCommand` is a simple and powerful way to run commands from your scripts.

Last updated: today


