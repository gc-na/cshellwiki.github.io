# [Linux] C Shell (csh) lvcreate : Créer des volumes logiques

## Overview
La commande `lvcreate` est utilisée pour créer des volumes logiques dans un groupe de volumes. Cela permet de gérer l'espace de stockage de manière flexible sur un système Linux utilisant LVM (Logical Volume Manager).

## Usage
La syntaxe de base de la commande `lvcreate` est la suivante :

```bash
lvcreate [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `lvcreate` :

- `-n` : Spécifie le nom du volume logique à créer.
- `-L` : Définit la taille du volume logique.
- `-l` : Définit la taille en unités de "logical extents".
- `-m` : Crée un volume miroir avec le nombre spécifié de copies.
- `-Z` : Permet de créer un volume logique avec des zéros (pour un volume vide).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `lvcreate` :

1. **Créer un volume logique de 10 Go :**
   ```bash
   lvcreate -L 10G -n mon_volume logique_groupe
   ```

2. **Créer un volume logique de 5 extents :**
   ```bash
   lvcreate -l 5 -n mon_volume logique_groupe
   ```

3. **Créer un volume miroir de 20 Go :**
   ```bash
   lvcreate -m 1 -L 20G -n mon_volume_miroir logique_groupe
   ```

4. **Créer un volume logique avec des zéros :**
   ```bash
   lvcreate -L 15G -n mon_volume_zero -Z y logique_groupe
   ```

## Tips
- Assurez-vous d'avoir suffisamment d'espace disponible dans le groupe de volumes avant de créer un volume logique.
- Utilisez des noms descriptifs pour vos volumes logiques afin de faciliter leur identification ultérieure.
- Pensez à vérifier la configuration de votre système LVM avant d'exécuter des commandes `lvcreate` pour éviter des erreurs.