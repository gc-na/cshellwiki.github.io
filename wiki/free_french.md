# [Linux] C Shell (csh) free : Afficher l'utilisation de la mémoire

## Overview
La commande `free` est utilisée pour afficher l'état de la mémoire dans un système Linux. Elle fournit des informations sur la mémoire totale, utilisée, libre et échangée, ce qui est essentiel pour surveiller les performances du système.

## Usage
La syntaxe de base de la commande `free` est la suivante :

```csh
free [options] [arguments]
```

## Common Options
- `-h` : Affiche les valeurs dans un format lisible par l'homme (par exemple, en Ko, Mo).
- `-m` : Affiche les valeurs en mégaoctets.
- `-g` : Affiche les valeurs en gigaoctets.
- `-s [seconds]` : Rafraîchit l'affichage toutes les [seconds] secondes.
- `-t` : Affiche la mémoire totale utilisée et libre.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `free` :

1. Afficher l'utilisation de la mémoire en format lisible par l'homme :
   ```csh
   free -h
   ```

2. Afficher l'utilisation de la mémoire en mégaoctets :
   ```csh
   free -m
   ```

3. Afficher l'utilisation de la mémoire toutes les 5 secondes :
   ```csh
   free -s 5
   ```

4. Afficher la mémoire totale, utilisée et libre :
   ```csh
   free -t
   ```

## Tips
- Utilisez l'option `-h` pour obtenir une lecture plus facile des informations de mémoire.
- Pour une surveillance continue, combinez `free` avec `watch` pour mettre à jour l'affichage à intervalles réguliers :
  ```csh
  watch free -h
  ```
- Vérifiez régulièrement l'utilisation de la mémoire pour éviter les problèmes de performance sur votre système.