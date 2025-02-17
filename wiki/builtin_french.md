# [Linux] Bash builtin : Affiche les commandes intégrées

## Overview
Le builtin `type` permet de déterminer comment une commande est interprétée par le shell. Il peut indiquer si une commande est intégrée, un alias, une fonction ou un fichier exécutable.

## Usage
La syntaxe de base de la commande `type` est la suivante :

```bash
type [options] [arguments]
```

## Common Options
- `-t` : Affiche uniquement le type de la commande (builtin, alias, file, etc.).
- `-a` : Affiche toutes les occurrences de la commande, y compris les alias et les fonctions.
- `-p` : Affiche le chemin complet de la commande si elle est un fichier exécutable.

## Common Examples

### Exemple 1 : Vérifier le type d'une commande
Pour vérifier si `ls` est une commande intégrée ou un fichier exécutable :

```bash
type ls
```

### Exemple 2 : Afficher le type d'une commande intégrée
Pour vérifier le type de la commande `cd` :

```bash
type cd
```

### Exemple 3 : Afficher toutes les occurrences d'une commande
Pour afficher toutes les occurrences de `echo`, y compris les alias :

```bash
type -a echo
```

### Exemple 4 : Obtenir le chemin d'une commande
Pour obtenir le chemin d'accès à la commande `grep` :

```bash
type -p grep
```

## Tips
- Utilisez `type` pour éviter les conflits entre les commandes intégrées et les fichiers exécutables.
- Combinez `type` avec d'autres commandes pour diagnostiquer des problèmes de commande dans vos scripts.
- N'hésitez pas à utiliser l'option `-a` pour avoir une vue d'ensemble complète des définitions de commande.