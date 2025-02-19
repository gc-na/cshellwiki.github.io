# [Linux] C Shell (csh) df Utilisation : Afficher l'espace disque disponible

## Overview
La commande `df` est utilisée pour afficher l'espace disque disponible sur les systèmes de fichiers montés. Elle fournit des informations sur la capacité totale, l'espace utilisé et l'espace libre de chaque système de fichiers.

## Usage
La syntaxe de base de la commande `df` est la suivante :

```csh
df [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `df` :

- `-h` : Affiche les tailles dans un format lisible par l'homme (par exemple, en Ko, Mo, Go).
- `-T` : Affiche le type de système de fichiers.
- `-a` : Inclut les systèmes de fichiers avec une taille de 0.
- `-i` : Affiche l'utilisation des inodes au lieu de l'espace disque.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `df` :

1. Afficher l'espace disque disponible sur tous les systèmes de fichiers :

   ```csh
   df
   ```

2. Afficher l'espace disque dans un format lisible par l'homme :

   ```csh
   df -h
   ```

3. Afficher les types de systèmes de fichiers avec l'espace disque :

   ```csh
   df -T
   ```

4. Afficher l'utilisation des inodes :

   ```csh
   df -i
   ```

## Tips
- Utilisez l'option `-h` pour rendre les informations plus faciles à lire, surtout si vous travaillez avec de grandes quantités de données.
- Combinez les options pour obtenir des informations plus détaillées, par exemple `df -hT` pour voir à la fois les tailles lisibles et les types de systèmes de fichiers.
- Vérifiez régulièrement l'espace disque disponible pour éviter les problèmes de stockage, surtout sur les serveurs.