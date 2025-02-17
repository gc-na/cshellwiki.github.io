# [Linux] Bash type usage : identifier le type d'une commande

## Overview
La commande `type` en Bash est utilisée pour déterminer le type d'une commande ou d'un programme. Elle peut indiquer si une commande est un alias, une fonction, un script, ou une commande intégrée.

## Usage
La syntaxe de base de la commande `type` est la suivante :

```bash
type [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `type` :

- `-t` : Affiche uniquement le type de la commande sans autres informations.
- `-a` : Affiche toutes les occurrences de la commande, y compris les alias et les fonctions.
- `-p` : Affiche le chemin complet de la commande si elle est un fichier exécutable.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `type` :

1. Pour vérifier le type d'une commande intégrée :
   ```bash
   type echo
   ```

2. Pour afficher toutes les occurrences d'une commande :
   ```bash
   type -a ls
   ```

3. Pour obtenir le chemin d'une commande exécutable :
   ```bash
   type -p python
   ```

4. Pour vérifier le type d'un alias :
   ```bash
   alias ll='ls -l'
   type ll
   ```

## Tips
- Utilisez `type -t` pour obtenir une sortie concise, ce qui est utile dans des scripts où vous avez besoin d'une vérification rapide.
- Combinez `type` avec d'autres commandes comme `grep` pour filtrer les résultats si vous vérifiez plusieurs commandes à la fois.
- Rappelez-vous que `type` ne renvoie pas d'erreur si la commande n'existe pas, mais vous pouvez vérifier cela en utilisant `command -v` pour une vérification plus stricte.