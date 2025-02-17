# [Linux] Bash history Utilisation : Afficher l'historique des commandes

## Overview
La commande `history` dans Bash permet d'afficher la liste des commandes précédemment exécutées dans le terminal. Cela peut être très utile pour retrouver des commandes que vous avez utilisées, sans avoir à les retaper manuellement.

## Usage
La syntaxe de base de la commande `history` est la suivante :

```bash
history [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `history` :

- `-c` : Efface l'historique des commandes.
- `-d offset` : Supprime la commande à l'offset spécifié de l'historique.
- `n` : Affiche les n dernières commandes de l'historique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `history` :

- Afficher l'historique complet des commandes :

```bash
history
```

- Afficher les 10 dernières commandes :

```bash
history 10
```

- Effacer l'historique des commandes :

```bash
history -c
```

- Supprimer une commande spécifique de l'historique (par exemple, la commande à l'offset 5) :

```bash
history -d 5
```

## Tips
- Utilisez `!n` pour exécuter la commande à l'offset n de l'historique. Par exemple, `!42` exécutera la 42ème commande.
- Pour rechercher une commande précédente, utilisez `Ctrl + r` et commencez à taper une partie de la commande.
- Pensez à nettoyer régulièrement votre historique pour éviter d'encombrer votre liste avec des commandes obsolètes.