# [Linux] Bash iostat Utilisation : Surveillance des performances des disques

## Overview
La commande `iostat` est utilisée pour surveiller les performances des systèmes d'entrée/sortie, en fournissant des statistiques sur l'utilisation des disques et des partitions. Elle aide les administrateurs à comprendre comment les ressources de stockage sont utilisées et à identifier les goulets d'étranglement.

## Usage
La syntaxe de base de la commande `iostat` est la suivante :

```bash
iostat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `iostat` :

- `-x` : Affiche des statistiques étendues pour chaque périphérique.
- `-m` : Affiche les statistiques en mégaoctets par seconde.
- `-p [device]` : Affiche les statistiques pour un périphérique spécifique ou ses partitions.
- `-t` : Affiche l'heure et la date dans la sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `iostat` :

1. Afficher les statistiques d'entrée/sortie par défaut :
   ```bash
   iostat
   ```

2. Afficher des statistiques étendues :
   ```bash
   iostat -x
   ```

3. Afficher les statistiques en mégaoctets par seconde :
   ```bash
   iostat -m
   ```

4. Afficher les statistiques pour un périphérique spécifique (par exemple, `/dev/sda`) :
   ```bash
   iostat -p /dev/sda
   ```

5. Afficher les statistiques avec des timestamps :
   ```bash
   iostat -t
   ```

## Tips
- Utilisez `iostat` avec d'autres outils comme `vmstat` ou `mpstat` pour obtenir une vue d'ensemble complète des performances du système.
- Exécutez `iostat` à intervalles réguliers pour surveiller les tendances d'utilisation des disques au fil du temps.
- Combinez `iostat` avec des scripts pour automatiser la surveillance et l'analyse des performances de votre système.