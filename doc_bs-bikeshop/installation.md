## Installation

Ce guide couvre l’installation complète de `bs-bikeshop` pour QS Inventory, OX Inventory ou ESX natif, ainsi que l’activation optionnelle de la boutique intégrée.

### 1) Prérequis
- Framework: ESX, QB ou QBX (standalone possible, mais l’argent/back‑office nécessite un framework)
- Dépendances: `ox_lib`, `ox_target`

Dans `server.cfg` (ordre d’ensure):

```cfg
ensure ox_lib
ensure ox_target
ensure bs-bikeshop
```

### 2) Déposer la ressource
Placez le dossier `bs-bikeshop` dans votre répertoire de ressources, puis ajoutez les lignes ci‑dessus dans `server.cfg`.

### 3) Intégrer les items selon votre inventaire

Sélection d’inventaire dans `shared/config.lua`:

```lua
-- 'auto' tentera QS, puis OX, sinon ESX
Config.Inventory = 'auto' -- valeurs: 'auto' | 'qs-inventory' | 'ox_inventory' | 'esx'
```

#### QS Inventory
1. Ouvrez `qs-inventory/shared/items.lua`.
2. Copiez le snippet depuis `install/qs_inventory_items.lua`.
3. Copiez les images depuis `install/items/` vers `qs-inventory/html/images/`.
4. Redémarrez `qs-inventory` puis `bs-bikeshop`.

Notes QS:
- Les items sont marqués `unique = true` et `useable = true`.
- Les noms utilisés par le script: `bmx`, `cruiser`, `fixter`, `scorcher`, `tribike`, `tribike2`, `tribike3`.

#### OX Inventory
Option A: fusionner dans `ox_inventory/data/items.lua` les entrées du snippet `install/ox_inventory_items.lua`.

Option B: si vous gérez vos items via un fichier séparé, adaptez la structure (label, weight, stack, consume) à votre schéma existant.

Redémarrez `ox_inventory` puis `bs-bikeshop`.

#### ESX natif (items en SQL)
1. Choisissez votre schéma: poids ou limite.
   - Schéma poids: importez `install/items_bikes_esx_weight.sql`
   - Schéma limite: importez `install/items_bikes_esx_limit.sql`
2. Redémarrez l’inventaire / le serveur.

### 4) Vérifier en jeu
1. Donnez‑vous un item (ex: via commande admin ou panel) `bmx`.
2. Utilisez l’item: un vélo spawn à côté de vous, plaque aléatoire.
3. Ciblez le vélo avec `ox_target` → « Ranger le vélo » pour récupérer l’item.

### 5) Activer la boutique intégrée (optionnel)
La boutique intégrée utilise `ox_target` pour afficher un menu `ox_lib` contextuel.

Dans `shared/config.lua`:

```lua
Config.EnableBuiltInShop = true

-- Produits (prix et noms d’items)
Config.Products = {
  { name = 'bmx',      label = 'BMX',        price = 1000 },
  { name = 'cruiser',  label = 'Cruiser',    price = 1200 },
  { name = 'fixter',   label = 'Fixter',     price = 1500 },
  { name = 'scorcher', label = 'Scorcher',   price = 1500 },
  { name = 'tribike',  label = 'Whippet',    price = 1500 },
  { name = 'tribike2', label = 'Endurex',    price = 1500 },
  { name = 'tribike3', label = 'Tri-Cycles', price = 2000 },
}

-- Emplacements (zones ox_target)
Config.Locations = {
  { coords = vec4(-1223.0, -1435.05, 4.37, 130.0), label = 'Bike Shop' },
}
```

Compte de paiement (serveur):

```lua
-- ESX: 'money' ou 'bank' | QB/QBX: 'cash' ou 'bank'
Config.PaymentAccount = 'money'
```

### 6) Dépannage rapide
- Aucun bouton « Ranger le vélo » ? Vérifiez `ox_target` et que le modèle est supporté (liste dans `client/client.lua`).
- Item non rendu lors du rangement ? L’inventaire doit pouvoir porter l’item (poids/slots). Le script vérifie la capacité avant suppression du véhicule.
- Achat boutique impossible ? Vérifiez fonds (`Config.PaymentAccount`) et le framework détecté côté serveur.
- Doublons de vélos ? L’option anti‑abus limite 1 vélo par joueur (voir Personnalisation pour ajuster).


