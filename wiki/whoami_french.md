# [Linux] Bash whoami : Identifier l'utilisateur actuel

## Overview
La commande `whoami` est utilisée pour afficher le nom de l'utilisateur actuellement connecté au terminal. C'est un moyen rapide de vérifier sous quel compte utilisateur vous travaillez, ce qui peut être particulièrement utile dans des environnements multi-utilisateurs ou lors de l'exécution de scripts.

## Usage
La syntaxe de base de la commande `whoami` est la suivante :

```bash
whoami [options] [arguments]
```

## Common Options
La commande `whoami` est assez simple et n'a pas beaucoup d'options. Voici les options les plus courantes :

- `--help` : Affiche l'aide et les options disponibles pour la commande.
- `--version` : Affiche la version de la commande `whoami`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `whoami` :

1. **Afficher le nom de l'utilisateur actuel :**
   ```bash
   whoami
   ```

2. **Afficher l'aide pour la commande :**
   ```bash
   whoami --help
   ```

3. **Afficher la version de la commande :**
   ```bash
   whoami --version
   ```

## Tips
- Utilisez `whoami` dans des scripts pour vérifier l'utilisateur avant d'exécuter des commandes sensibles.
- Combinez `whoami` avec d'autres commandes comme `sudo` pour confirmer que vous avez les droits nécessaires.
- Pensez à utiliser `id -un` comme alternative pour obtenir le même résultat, tout en ayant plus d'options disponibles.