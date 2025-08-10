## Personnalisation

Tous les paramètres se trouvent dans `shared/config.lua`. Voici les réglages clés pour adapter la ressource à votre économie et vos préférences de gameplay.

### Langue
```lua
-- 'en' ou 'fr' (d’autres langues sont prêtes dans locales)
Config.Locale = 'en'
```

`shared/locales.lua` contient EN/FR + 12 autres langues. La fonction `T(key, ...)` sélectionne automatiquement la langue configurée.

### Inventaire
```lua
-- 'auto' = QS > OX > ESX
Config.Inventory = 'auto' -- 'auto' | 'qs-inventory' | 'ox_inventory' | 'esx'
```

### Boutiqued intégrée
```lua
-- Active la boutique interne (zones ox_target + menu ox_lib)
Config.EnableBuiltInShop = false

-- Compte de paiement
-- ESX: 'money' ou 'bank' | QB/QBX: 'cash' ou 'bank'
Config.PaymentAccount = 'money'

-- Produits et prix
Config.Products = {
  { name = 'bmx',      label = 'BMX',        price = 1000 },
  { name = 'cruiser',  label = 'Cruiser',    price = 1200 },
  { name = 'fixter',   label = 'Fixter',     price = 1500 },
  { name = 'scorcher', label = 'Scorcher',   price = 1500 },
  { name = 'tribike',  label = 'Whippet',    price = 1500 },
  { name = 'tribike2', label = 'Endurex',    price = 1500 },
  { name = 'tribike3', label = 'Tri-Cycles', price = 2000 },
}

-- Emplacements de boutique (zones)
Config.Locations = {
  { coords = vec4(-1223.0, -1435.05, 4.37, 130.0), label = 'Bike Shop' },
}
```

### Spawn du vélo
```lua
Config.Spawn = {
  offset = vector3(2.0, 0.0, 0.3), -- position relative au joueur
  seatInto = true,                  -- asseoir le joueur automatiquement
  platePrefix = 'BIKE',             -- préfixe de plaque
  cooldownSeconds = 3,              -- délai anti‑spam
  safeSpawnCheck = false,           -- si vous avez un checker de zone libre
  safeRadius = 1.5                  -- rayon du checker
}
```

### Rangement (ox_target)
```lua
Config.Pack = {
  enable = true,
  distance = 2.0,       -- distance d’interaction
  ownerOnly = true,      -- seul le propriétaire peut ranger
  maxPackRange = 5.0,    -- distance max joueur ↔ vélo côté serveur
}
```

### Restrictions (anti‑abus)
```lua
Config.Restrictions = {
  singleBikePerPlayer = true, -- limite à 1 item vélo par joueur
  bikeItems = { 'bmx', 'cruiser', 'fixter', 'scorcher', 'tribike', 'tribike2', 'tribike3' }
}
```

Si vous utilisez QS Shops, le serveur applique un contrôle post‑achat et retire l’item en trop en notifiant le joueur.

### Modèles supportés et ciblage ox_target
Les modèles supportés côté client : `bmx`, `cruiser`, `fixter`, `scorcher`, `tribike`, `tribike2`, `tribike3`.

`ox_target` ajoute automatiquement l’option « Ranger le vélo » sur ces modèles, avec contrôle d’appartenance si `ownerOnly = true`.

### Ajout d’un nouveau vélo (exemple)
1) Ajoutez l’item dans votre inventaire (QS/OX/ESX) avec image si QS.
2) Ajoutez son nom dans `Config.Restrictions.bikeItems`.
3) Ajoutez son entrée dans `Config.Products` si vous voulez le vendre via la boutique intégrée.
4) Si le modèle a un autre nom, assurez‑vous de l’utiliser comme `model` de spawn côté client (événement `bs-bikeshop:useBikeItem`).


