# [Linux] C Shell (csh) fdisk Utilisation : Gérer les partitions de disque

## Overview
La commande `fdisk` est utilisée pour manipuler les tables de partitions sur les disques durs. Elle permet de créer, supprimer, redimensionner et gérer les partitions de disque, ce qui est essentiel pour la gestion des systèmes de fichiers.

## Usage
Voici la syntaxe de base de la commande `fdisk` :

```bash
fdisk [options] [arguments]
```

## Common Options
- `-l` : Liste toutes les partitions sur tous les disques.
- `-u` : Utilise des unités de secteurs pour afficher les informations.
- `-n` : Crée une nouvelle partition.
- `-d` : Supprime une partition existante.
- `-s` : Affiche la taille d'une partition.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fdisk` :

1. **Lister les partitions sur un disque spécifique** :
   ```bash
   fdisk -l /dev/sda
   ```

2. **Créer une nouvelle partition** :
   ```bash
   fdisk /dev/sda
   ```
   Ensuite, dans l'interface interactive, utilisez `n` pour créer une nouvelle partition.

3. **Supprimer une partition** :
   ```bash
   fdisk /dev/sda
   ```
   Dans l'interface interactive, utilisez `d` pour supprimer une partition.

4. **Afficher la taille d'une partition** :
   ```bash
   fdisk -s /dev/sda1
   ```

## Tips
- Toujours sauvegarder vos données avant de modifier les partitions pour éviter toute perte de données.
- Utilisez `man fdisk` pour accéder à la documentation complète et aux options avancées.
- Soyez prudent lorsque vous supprimez des partitions, car cette action est irréversible.