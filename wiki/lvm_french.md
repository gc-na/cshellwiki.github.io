# [Linux] Bash lvm : Gestion des volumes logiques

## Overview
La commande `lvm` (Logical Volume Manager) est utilisée pour gérer les volumes logiques dans un système Linux. Elle permet de créer, supprimer, redimensionner et gérer des volumes logiques, offrant ainsi une flexibilité dans la gestion de l'espace de stockage.

## Usage
La syntaxe de base de la commande `lvm` est la suivante :

```bash
lvm [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `lvm` :

- `create`: Crée un nouveau volume logique.
- `remove`: Supprime un volume logique existant.
- `extend`: Augmente la taille d'un volume logique.
- `reduce`: Diminue la taille d'un volume logique.
- `lvdisplay`: Affiche les informations sur les volumes logiques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lvm` :

### Créer un volume logique
```bash
lvcreate -n mon_volume -L 10G mon_groupe
```
Cet exemple crée un volume logique nommé `mon_volume` de 10 Go dans le groupe de volumes `mon_groupe`.

### Supprimer un volume logique
```bash
lvremove /dev/mon_groupe/mon_volume
```
Cette commande supprime le volume logique `mon_volume` du groupe de volumes `mon_groupe`.

### Étendre un volume logique
```bash
lvextend -L +5G /dev/mon_groupe/mon_volume
```
Ici, nous augmentons la taille du volume logique `mon_volume` de 5 Go.

### Réduire un volume logique
```bash
lvreduce -L -3G /dev/mon_groupe/mon_volume
```
Cette commande réduit la taille de `mon_volume` de 3 Go.

### Afficher les volumes logiques
```bash
lvdisplay
```
Cette commande affiche les informations détaillées sur tous les volumes logiques disponibles.

## Tips
- Avant de réduire un volume logique, assurez-vous de sauvegarder les données importantes et de réduire le système de fichiers à l'intérieur du volume.
- Utilisez `lvscan` pour vérifier l'état de tous les volumes logiques avant d'effectuer des opérations.
- Pensez à utiliser des snapshots pour sauvegarder l'état d'un volume logique avant de faire des modifications importantes.