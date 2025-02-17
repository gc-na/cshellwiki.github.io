# [Linux] Bash lvcreate Utilisation : Créer des volumes logiques

## Overview
La commande `lvcreate` est utilisée pour créer des volumes logiques dans un groupe de volumes sous Linux. Cela fait partie de la gestion des systèmes de fichiers et permet de gérer l'espace de stockage de manière flexible.

## Usage
La syntaxe de base de la commande `lvcreate` est la suivante :

```bash
lvcreate [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `lvcreate` :

- `-n, --name <nom>` : Spécifie le nom du volume logique à créer.
- `-L, --size <taille>` : Définit la taille du volume logique.
- `-l, --extents <nombre>` : Définit la taille en étendues (extents) du volume logique.
- `-m, --mirrors <nombre>` : Crée des miroirs du volume logique.
- `-Z, --zeroing <mode>` : Définit si le volume doit être initialisé à zéro.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `lvcreate` :

1. **Créer un volume logique de 10 Go :**
   ```bash
   lvcreate -L 10G -n mon_volume mon_groupe
   ```

2. **Créer un volume logique avec une taille spécifiée en étendues :**
   ```bash
   lvcreate -l 100 -n mon_volume_etendu mon_groupe
   ```

3. **Créer un volume logique avec des miroirs :**
   ```bash
   lvcreate -m 1 -L 5G -n mon_volume_miroir mon_groupe
   ```

4. **Créer un volume logique et le formater en ext4 :**
   ```bash
   lvcreate -L 20G -n volume_ext4 mon_groupe
   mkfs.ext4 /dev/mon_groupe/volume_ext4
   ```

## Tips
- Toujours vérifier l'espace disponible dans le groupe de volumes avant de créer un volume logique.
- Utilisez des noms descriptifs pour vos volumes logiques afin de faciliter leur identification.
- Pensez à utiliser des miroirs pour la redondance si la disponibilité des données est critique.