# How to enable target system

Banshy Store scripts support popular target systems for consistent interactions with entities and objects. This guide explains supported systems, how to enable them, and how to customize or extend the setup.

## Supported target systems
- ox_target - stable and widely adopted "third-eye" targeting.
- qb-target - popular interaction system used in QBCore servers.

Please keep your target resource up to date to avoid compatibility issues.

## How to enable the target system

### 1) Locate the config file
Open the `config.lua` of the Banshy Store asset you want to configure.

### 2) Enable and select the target system
Find the following configuration in `config.lua`:

```lua
Config.UseTarget = false
```

Change the value to your preferred target system name, for example:

```lua
Config.UseTarget = 'ox_target'
-- or
Config.UseTarget = 'qb-target'
```

### 3) Save and restart
Save your changes and restart the resource (or your server) to apply the configuration.

## Editing or customizing your target system
Advanced users can modify or create custom target integrations.

- Location: `client/custom/target/*`
- You can tweak interaction ranges, options, or target zones for objects, entities, or vehicles.
- Use the existing files as templates to build a new target integration if using a non-default system.

### Important warnings
- Edit at your own risk: custom changes can introduce unexpected issues.
- No support for custom changes: we cannot troubleshoot problems caused by custom edits.
- Back up files: always back up the original files before modifying them.

Last updated: today

## Media
- Video: [Placeholder – switching between ox_target and qb-target]
- Screenshots: [Placeholder – config.lua snippet, in-game target prompts]


