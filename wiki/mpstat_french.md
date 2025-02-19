# [Linux] C Shell (csh) mpstat Utilisation : surveiller l'utilisation du processeur

## Overview
La commande `mpstat` permet de surveiller l'utilisation du processeur sur un système. Elle affiche des statistiques sur l'activité des processeurs, ce qui est utile pour analyser la performance et identifier les goulets d'étranglement.

## Usage
La syntaxe de base de la commande `mpstat` est la suivante :

```csh
mpstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mpstat` :

- `-P ALL` : Affiche les statistiques pour tous les processeurs.
- `-u` : Affiche l'utilisation du processeur en pourcentage.
- `-r` : Affiche les statistiques de l'utilisation de la mémoire.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `mpstat` :

1. Afficher les statistiques d'utilisation du processeur pour tous les cœurs :
   ```csh
   mpstat -P ALL
   ```

2. Afficher l'utilisation du processeur en pourcentage :
   ```csh
   mpstat -u
   ```

3. Afficher les statistiques de mémoire :
   ```csh
   mpstat -r
   ```

4. Afficher les statistiques toutes les 5 secondes :
   ```csh
   mpstat 5
   ```

## Tips
- Utilisez l'option `-P ALL` pour obtenir une vue d'ensemble de l'utilisation de tous les cœurs de votre processeur.
- Combinez `mpstat` avec d'autres outils comme `grep` pour filtrer les résultats et obtenir des informations spécifiques.
- Pensez à exécuter `mpstat` avec des privilèges d'administrateur pour accéder à des informations plus détaillées sur le système.