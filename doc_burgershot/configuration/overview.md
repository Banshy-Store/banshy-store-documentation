# Configuration Overview

All config is in `shared/config.lua`.

- Framework: `BSConfig.Framework` ('auto'|'esx'|'qb'|'qbox')
- Inventory backend: `BSConfig.Inventory` ('auto'|'qs'|'ox'|'qb'|'esx')
- Payments: `BSConfig.Payments = { mode, share }`
- Points/Target/Blip: `BSConfig.Points`, `BSConfig.TargetZones`, `BSConfig.Blip`
- Menus/Recipes/Items/Times: `BSConfig.Menus`, `BSConfig.Recipes`, `BSConfig.ItemsMap`, `BSConfig.CookingTimes`
- Customer menu & checklist: `BSConfig.CustomerMenu`, `BSConfig.ChecklistRecipes`, `BSConfig.ItemLabels`
- Outfits & Boss: `BSConfig.Outfits`, `BSConfig.BossMenu`
- Webhooks: `BSConfig.Webhooks`
