# [Linux] Bash vipw usage : Édition sécurisée des fichiers de mots de passe

## Overview
La commande `vipw` est utilisée pour éditer le fichier des mots de passe de manière sécurisée. Elle verrouille le fichier pour éviter les modifications simultanées, ce qui permet de prévenir les corruptions de données.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
vipw [options]
```

## Common Options
Voici quelques options courantes pour `vipw` :

- `-s` : Utilise un éditeur de texte spécifique, défini par la variable d'environnement `EDITOR`.
- `-u` : Édite le fichier des mots de passe pour un utilisateur spécifique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `vipw` :

1. Éditer le fichier des mots de passe par défaut :
   ```bash
   vipw
   ```

2. Éditer le fichier des mots de passe en utilisant un éditeur spécifique (par exemple, `nano`) :
   ```bash
   EDITOR=nano vipw
   ```

3. Éditer le fichier des mots de passe pour un utilisateur spécifique :
   ```bash
   vipw -u username
   ```

## Tips
- Assurez-vous d'avoir les permissions nécessaires pour modifier le fichier des mots de passe.
- Utilisez `vipw` plutôt que `vi /etc/passwd` pour éviter les problèmes de concurrence.
- Faites toujours une sauvegarde du fichier avant de le modifier, surtout si vous travaillez sur un système de production.