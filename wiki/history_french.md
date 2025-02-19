# [Linux] C Shell (csh) history : Affiche les commandes précédemment exécutées

## Overview
La commande `history` dans C Shell (csh) permet d'afficher la liste des commandes précédemment exécutées dans la session actuelle. Cela peut être très utile pour retrouver des commandes que vous avez déjà saisies sans avoir à les retaper.

## Usage
La syntaxe de base de la commande `history` est la suivante :

```csh
history [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `history` :

- `-c` : Efface l'historique des commandes.
- `n` : Affiche les `n` dernières commandes de l'historique.
- `!n` : Exécute la commande numéro `n` de l'historique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `history` :

1. Afficher toutes les commandes précédemment exécutées :
   ```csh
   history
   ```

2. Afficher les 10 dernières commandes :
   ```csh
   history 10
   ```

3. Exécuter la commande numéro 5 de l'historique :
   ```csh
   !5
   ```

4. Effacer l'historique des commandes :
   ```csh
   history -c
   ```

## Tips
- Utilisez `history` régulièrement pour retrouver des commandes que vous avez utilisées, ce qui peut vous faire gagner du temps.
- Faites attention lorsque vous utilisez `!n`, car cela exécutera immédiatement la commande correspondante, ce qui peut entraîner des erreurs si vous ne vérifiez pas d'abord l'historique.
- Pensez à effacer l'historique si vous travaillez avec des informations sensibles pour éviter que d'autres utilisateurs ne puissent les voir.