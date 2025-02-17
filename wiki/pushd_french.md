# [Linux] Bash pushd : [naviguer dans les répertoires]

## Overview
La commande `pushd` est utilisée pour changer de répertoire tout en sauvegardant l'emplacement actuel dans une pile. Cela permet de naviguer facilement entre plusieurs répertoires sans perdre la trace de votre position précédente.

## Usage
La syntaxe de base de la commande `pushd` est la suivante :

```bash
pushd [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `pushd` :

- `+n` : Accède au n-ième répertoire de la pile.
- `-n` : Accède au n-ième répertoire de la pile en partant de la fin.
- `-` : Retourne au dernier répertoire visité.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `pushd` :

1. **Changer de répertoire et sauvegarder l'emplacement actuel :**
   ```bash
   pushd /chemin/vers/nouveau/repertoire
   ```

2. **Accéder à un répertoire spécifique dans la pile :**
   ```bash
   pushd +1
   ```

3. **Revenir au dernier répertoire visité :**
   ```bash
   pushd -
   ```

4. **Afficher la pile des répertoires :**
   ```bash
   dirs
   ```

## Tips
- Utilisez `popd` pour revenir au répertoire précédent et retirer le répertoire actuel de la pile.
- Combinez `pushd` avec des scripts pour automatiser la navigation dans des répertoires complexes.
- Pensez à utiliser `dirs -v` pour afficher la pile avec des numéros, ce qui facilite la navigation avec `pushd +n`.