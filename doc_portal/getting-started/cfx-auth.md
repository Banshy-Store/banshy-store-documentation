# CFX Auth

CFX Auth est le système d’authentification/entitlements de Cfx.re (FiveM). Il relie vos achats et les permissions serveur à votre compte via Keymaster. Les ressources protégées (escrow) nécessitent une licence serveur valide appartenant au compte propriétaire.

## Comment ça marche
- Un achat crée un entitlement sur votre compte Cfx.re.
- Votre serveur s’identifie avec une clé Keymaster `sv_licenseKey`.
- Au démarrage d’une ressource protégée, la plateforme vérifie que la clé serveur correspond aux entitlements du propriétaire.

## Prérequis
- Une clé serveur Keymaster valide sur le compte acheteur
- Le `server.cfg` configuré avec cette clé
- Une connectivité internet côté serveur

## Mise en place rapide
1. Créez (ou récupérez) votre clé serveur dans Keymaster depuis le compte acheteur.
2. Dans `server.cfg`, ajoutez:

```cfg
sv_licenseKey YOUR_KEYMASTER_KEY
```

3. Redémarrez complètement le serveur (pas uniquement la ressource).

## Dépannage: Missing Required Entitlement
Si vous voyez « You lack the required entitlement to use <resource> »:
- Vérifiez que la clé serveur appartient bien au compte qui a acheté la ressource.
- Mettez à jour `sv_licenseKey` si la clé a changé, puis redémarrez le serveur.
- Voir aussi: [Understanding FiveM asset escrow system](escrow.md)

## Médias
- Captures: [Placeholder – Keymaster, ajout de la clé]
