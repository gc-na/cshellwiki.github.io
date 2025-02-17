# [Linux] Bash free : afficher l'utilisation de la mémoire

## Overview
La commande `free` est utilisée pour afficher des informations sur l'utilisation de la mémoire dans un système Linux. Elle fournit des détails sur la mémoire totale, utilisée, libre, ainsi que sur la mémoire swap.

## Usage
La syntaxe de base de la commande `free` est la suivante :

```
free [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `free` :

- `-h` : Affiche les valeurs dans un format lisible par l'homme (par exemple, en Ko, Mo, Go).
- `-m` : Affiche la mémoire en mégaoctets.
- `-g` : Affiche la mémoire en gigaoctets.
- `-s <seconds>` : Actualise les informations à intervalles réguliers spécifiés en secondes.
- `-t` : Affiche un total de la mémoire utilisée et libre.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `free` :

1. Afficher l'utilisation de la mémoire en format lisible par l'homme :
   ```bash
   free -h
   ```

2. Afficher la mémoire en mégaoctets :
   ```bash
   free -m
   ```

3. Afficher la mémoire en gigaoctets :
   ```bash
   free -g
   ```

4. Actualiser l'affichage toutes les 5 secondes :
   ```bash
   free -s 5
   ```

5. Afficher un total de la mémoire :
   ```bash
   free -t -h
   ```

## Tips
- Utilisez l'option `-h` pour rendre les résultats plus faciles à lire, surtout sur des systèmes avec beaucoup de mémoire.
- Combinez `free` avec d'autres commandes comme `watch` pour surveiller l'utilisation de la mémoire en temps réel :
  ```bash
  watch free -h
  ```
- Vérifiez régulièrement l'utilisation de la mémoire pour identifier des problèmes potentiels de performance sur votre système.