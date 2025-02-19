# [Linux] C Shell (csh) vgcreate : Créer un groupe de volumes

## Overview
La commande `vgcreate` est utilisée pour créer un groupe de volumes dans le système de gestion de volumes logiques (LVM) sous Linux. Cela permet de regrouper plusieurs volumes physiques en une seule unité logique, facilitant ainsi la gestion de l'espace de stockage.

## Usage
La syntaxe de base de la commande `vgcreate` est la suivante :

```bash
vgcreate [options] [nom_du_groupe] [disques]
```

## Common Options
Voici quelques options courantes pour la commande `vgcreate` :

- `-s, --stripes <nombre>` : Définit le nombre de bandes à utiliser pour le groupe de volumes.
- `-p, --max-pv <nombre>` : Spécifie le nombre maximal de volumes physiques pouvant être ajoutés au groupe.
- `-f, --force` : Force la création du groupe de volumes, même si des erreurs sont détectées.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `vgcreate` :

1. **Créer un groupe de volumes simple :**
   ```bash
   vgcreate mon_groupe /dev/sda1 /dev/sda2
   ```

2. **Créer un groupe de volumes avec des options :**
   ```bash
   vgcreate -s 64K mon_groupe /dev/sdb1 /dev/sdb2
   ```

3. **Forcer la création d'un groupe de volumes :**
   ```bash
   vgcreate -f mon_groupe /dev/sdc1
   ```

## Tips
- Assurez-vous que les disques que vous ajoutez au groupe de volumes sont non montés et non utilisés par d'autres systèmes de fichiers.
- Utilisez la commande `vgs` pour vérifier l'état de vos groupes de volumes après leur création.
- Pensez à documenter vos groupes de volumes pour une gestion future plus facile.