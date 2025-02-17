# [Linux] Bash fc Utilisation : Gérer l'historique des commandes

## Overview
La commande `fc` est utilisée pour manipuler l'historique des commandes dans un shell Bash. Elle permet d'afficher, de modifier et de réexécuter des commandes précédemment exécutées.

## Usage
La syntaxe de base de la commande `fc` est la suivante :

```bash
fc [options] [arguments]
```

## Common Options
- `-l` : Liste les commandes de l'historique.
- `-r` : Inverse l'ordre des commandes lors de l'affichage.
- `-s` : Exécute une commande sans l'afficher.
- `-n` : N'affiche pas les numéros de ligne lors de la liste des commandes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fc` :

### Afficher les dernières commandes
Pour afficher les 10 dernières commandes de l'historique, utilisez :

```bash
fc -l -10
```

### Modifier une commande spécifique
Pour modifier la commande numéro 42 dans l'historique, utilisez :

```bash
fc 42
```

### Exécuter la dernière commande
Pour exécuter la dernière commande sans l'afficher, utilisez :

```bash
fc -s
```

### Inverser l'affichage des commandes
Pour afficher les 5 dernières commandes dans l'ordre inverse, utilisez :

```bash
fc -lr -5
```

## Tips
- Utilisez `fc` pour corriger rapidement des erreurs dans vos commandes précédentes.
- Combinez `fc` avec des éditeurs de texte comme `nano` ou `vim` pour une modification plus avancée.
- Familiarisez-vous avec les numéros de commande dans l'historique pour une utilisation efficace de `fc`.