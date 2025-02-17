# [Linux] Bash df Utilisation : Afficher l'espace disque disponible

## Overview
La commande `df` (disk free) est utilisée pour afficher des informations sur l'espace disque utilisé et disponible sur les systèmes de fichiers montés. Elle fournit un aperçu rapide de la capacité de stockage de votre système.

## Usage
La syntaxe de base de la commande `df` est la suivante :

```bash
df [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `df` :

- `-h` : Affiche les tailles dans un format lisible par l'homme (par exemple, Ko, Mo, Go).
- `-T` : Affiche le type de système de fichiers.
- `-a` : Inclut tous les systèmes de fichiers, même ceux avec une taille de 0.
- `-i` : Affiche l'utilisation des inodes au lieu de l'espace disque.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `df` :

1. Afficher l'espace disque disponible dans un format lisible par l'homme :

   ```bash
   df -h
   ```

2. Afficher les informations sur tous les systèmes de fichiers, y compris ceux de taille 0 :

   ```bash
   df -a
   ```

3. Afficher le type de système de fichiers pour chaque point de montage :

   ```bash
   df -T
   ```

4. Afficher l'utilisation des inodes :

   ```bash
   df -i
   ```

## Tips
- Utilisez l'option `-h` pour rendre les résultats plus faciles à lire, surtout sur des systèmes avec de grandes capacités de stockage.
- Combinez les options pour obtenir des informations plus détaillées, par exemple `df -hT` pour voir à la fois la taille et le type de système de fichiers.
- Vérifiez régulièrement l'espace disque disponible pour éviter les problèmes de stockage, surtout sur les serveurs et les systèmes critiques.