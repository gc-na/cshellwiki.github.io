# [Linux] C Shell (csh) iostat Utilisation : Surveillance des statistiques d'entrée/sortie

## Overview
La commande `iostat` est utilisée pour surveiller les statistiques d'entrée/sortie des systèmes de fichiers et des périphériques de stockage. Elle fournit des informations sur l'utilisation du CPU ainsi que sur les performances des disques, ce qui est essentiel pour diagnostiquer les goulets d'étranglement et optimiser les performances du système.

## Usage
La syntaxe de base de la commande `iostat` est la suivante :

```csh
iostat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `iostat` :

- `-c` : Affiche uniquement les statistiques du CPU.
- `-d` : Affiche uniquement les statistiques des périphériques de stockage.
- `-x` : Affiche des statistiques étendues pour les périphériques, incluant des informations détaillées sur l'utilisation.
- `-t` : Affiche l'heure et la date avec les statistiques.
- `interval` : Définit l'intervalle de temps entre les rapports, en secondes.
- `count` : Définit le nombre de rapports à afficher.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `iostat` :

1. Afficher les statistiques de CPU et de périphériques toutes les 5 secondes :

   ```csh
   iostat 5
   ```

2. Afficher uniquement les statistiques du CPU :

   ```csh
   iostat -c
   ```

3. Afficher des statistiques détaillées sur les périphériques de stockage :

   ```csh
   iostat -dx
   ```

4. Afficher les statistiques avec date et heure, toutes les 10 secondes, pour 3 rapports :

   ```csh
   iostat -t 10 3
   ```

## Tips
- Utilisez l'option `-x` pour obtenir des informations plus détaillées sur les performances des disques, ce qui peut aider à identifier les problèmes de performance.
- Combinez `iostat` avec d'autres outils comme `vmstat` et `mpstat` pour obtenir une vue d'ensemble complète des performances du système.
- Surveillez régulièrement les statistiques d'entrée/sortie, surtout lors de l'exécution d'applications intensives en ressources, pour anticiper les problèmes potentiels.