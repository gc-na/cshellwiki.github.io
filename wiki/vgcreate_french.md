# [Linux] Bash vgcreate : Créer un groupe de volumes

## Overview
La commande `vgcreate` est utilisée pour créer un groupe de volumes dans le système de gestion de volumes logiques (LVM) sous Linux. Un groupe de volumes permet de regrouper plusieurs volumes physiques, facilitant ainsi la gestion de l'espace de stockage.

## Usage
La syntaxe de base de la commande `vgcreate` est la suivante :

```bash
vgcreate [options] [nom_du_groupe_de_volumes] [volumes_physiques...]
```

## Common Options
Voici quelques options courantes pour `vgcreate` :

- `-s, --stripes <nombre>` : Définit le nombre de bandes pour le groupe de volumes.
- `-p, --max-pv <nombre>` : Définit le nombre maximum de volumes physiques dans le groupe.
- `-y, --yes` : Accepte automatiquement toutes les confirmations.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `vgcreate` :

1. **Créer un groupe de volumes simple :**
   ```bash
   vgcreate mon_groupe /dev/sda1 /dev/sda2
   ```

2. **Créer un groupe de volumes avec des options :**
   ```bash
   vgcreate -s 64K -p 10 mon_groupe /dev/sdb1
   ```

3. **Créer un groupe de volumes en acceptant automatiquement les confirmations :**
   ```bash
   vgcreate -y mon_groupe /dev/sdc1
   ```

## Tips
- Assurez-vous que les volumes physiques que vous ajoutez au groupe de volumes sont correctement initialisés avec `pvcreate`.
- Vérifiez l'espace disponible dans les volumes physiques avant de créer un groupe de volumes pour éviter les erreurs.
- Utilisez `vgdisplay` après la création pour vérifier les détails du groupe de volumes créé.