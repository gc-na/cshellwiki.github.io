# [Linux] Bash parted Utilisation : Gestion des partitions de disque

## Overview
La commande `parted` est un outil puissant utilisé pour gérer les partitions de disque sous Linux. Il permet de créer, supprimer, redimensionner et manipuler les partitions de manière efficace, tout en prenant en charge différents systèmes de fichiers.

## Usage
La syntaxe de base de la commande `parted` est la suivante :

```bash
parted [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `parted` :

- `-s` : Exécute `parted` en mode silencieux, sans afficher d'invite.
- `mkpart` : Crée une nouvelle partition.
- `rm` : Supprime une partition existante.
- `resizepart` : Redimensionne une partition existante.
- `print` : Affiche la table des partitions du disque.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `parted` :

### 1. Afficher la table des partitions
Pour afficher la table des partitions d'un disque spécifique (par exemple `/dev/sda`), utilisez :

```bash
parted /dev/sda print
```

### 2. Créer une nouvelle partition
Pour créer une nouvelle partition de type ext4 qui commence à 1 Go et fait 5 Go de long :

```bash
parted /dev/sda mkpart primary ext4 1GB 6GB
```

### 3. Supprimer une partition
Pour supprimer la partition numéro 2 sur le disque `/dev/sda` :

```bash
parted /dev/sda rm 2
```

### 4. Redimensionner une partition
Pour redimensionner la partition numéro 1 pour qu'elle occupe 10 Go :

```bash
parted /dev/sda resizepart 1 10GB
```

## Tips
- Toujours sauvegarder vos données avant de modifier les partitions, car des erreurs peuvent entraîner une perte de données.
- Utilisez l'option `-s` pour automatiser des scripts sans interaction utilisateur.
- Vérifiez l'intégrité de votre système de fichiers après avoir effectué des modifications avec `fsck`.

En suivant ces conseils, vous pourrez utiliser `parted` de manière efficace et sécurisée pour gérer vos partitions de disque.