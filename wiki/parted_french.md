# [Linux] C Shell (csh) parted : Gestion des partitions de disque

## Overview
La commande `parted` est utilisée pour gérer les partitions de disque sur les systèmes Linux. Elle permet de créer, supprimer, redimensionner et manipuler des partitions de manière efficace.

## Usage
La syntaxe de base de la commande `parted` est la suivante :

```bash
parted [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `parted` :

- `-l` : Liste toutes les partitions disponibles.
- `mkpart` : Crée une nouvelle partition.
- `rm` : Supprime une partition existante.
- `resizepart` : Redimensionne une partition existante.
- `print` : Affiche la table des partitions.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `parted` :

### Lister les partitions
```bash
parted -l
```

### Créer une nouvelle partition
```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Supprimer une partition
```bash
parted /dev/sda rm 1
```

### Redimensionner une partition
```bash
parted /dev/sda resizepart 1 200MiB
```

### Afficher la table des partitions
```bash
parted /dev/sda print
```

## Tips
- Toujours sauvegarder vos données avant de modifier les partitions pour éviter toute perte.
- Utilisez `parted` avec précaution, car des erreurs peuvent rendre vos données inaccessibles.
- Vérifiez le type de partition et le système de fichiers avant de créer ou de redimensionner des partitions.