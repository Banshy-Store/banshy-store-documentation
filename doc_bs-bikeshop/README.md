## bs-bikeshop — Boutique de vélos (items)

Transformez les vélos en véritables items: achetez, déployez en un clic, rangez via ox_target. Compatible QS Inventory, OX Inventory, et ESX natif. Idéal pour monétiser votre serveur avec une expérience propre, performante et anti‑abus.

### Pourquoi bs-bikeshop ?
- **Inventaire‑agnostique**: QS, OX, ESX natif — sélection automatique ou forcée.
- **Expérience fluide**: l’item spawn le vélo; un ciblage `ox_target` permet de le ranger.
- **Anti‑abus**: contrôle propriétaire + distance; option 1 vélo max par joueur.
- **Boutique intégrée**: zones `ox_target` prêtes à l’emploi (désactivée par défaut).
- **Localisation**: EN/FR inclus (+ 12 langues prêtes dans `shared/locales.lua`).

### Compatibilité
- Framework: ESX, QB/QBX (via bridge argent), standalone (fonctions limitées)
- Inventaires: **qs-inventory**, **ox_inventory**, **ESX natif** (items en SQL)
- Dépendances: `ox_lib`, `ox_target`

### Vue d’ensemble du contenu
- `client/` logique de spawn/pack, `ox_target`
- `server/` vérifications, achats, bridge inventaires et argent
- `shared/config.lua` configuration complète (boutique, produits, spawn, pack…)
- `shared/locales.lua` traductions et helper `T()`
- `install/` snippets d’items QS/OX, SQL ESX, images d’items

### Démarrage rapide (résumé)
1) Placez la ressource et assurez l’ordre dans `server.cfg`:
   - ensure ox_lib
   - ensure ox_target
   - ensure bs-bikeshop
2) Intégrez les items pour votre inventaire (QS/OX/ESX). Les snippets sont dans `install/`.
3) Donnez‑vous un item (ex: `bmx`), utilisez‑le pour spawn, ciblez le vélo pour le ranger.

Aller plus loin:
- Installation pas‑à‑pas: voir [Installation](installation.md)
- Paramètres & personnalisation: voir [Personnalisation](customisation.md)


