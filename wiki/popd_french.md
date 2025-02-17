# [Linux] Bash popd : Gérer les répertoires de la pile

## Overview
La commande `popd` est utilisée dans un environnement Bash pour supprimer le répertoire supérieur de la pile de répertoires et se déplacer vers ce répertoire. Elle permet de naviguer facilement entre plusieurs répertoires sans avoir à taper les chemins complets.

## Usage
La syntaxe de base de la commande `popd` est la suivante :

```bash
popd [options]
```

## Common Options
- `-n` : Ne pas changer de répertoire, juste afficher la pile.
- `+N` : Aller au N-ième répertoire de la pile, en commençant par 0 pour le sommet.

## Common Examples

### Exemple 1 : Utilisation de base
Pour revenir au répertoire supérieur de la pile :

```bash
popd
```

### Exemple 2 : Afficher la pile sans changer de répertoire
Pour afficher la pile actuelle sans changer de répertoire :

```bash
popd -n
```

### Exemple 3 : Accéder à un répertoire spécifique dans la pile
Pour accéder au deuxième répertoire de la pile :

```bash
popd +1
```

## Tips
- Utilisez `pushd` avant `popd` pour ajouter des répertoires à la pile, ce qui rend la navigation plus fluide.
- Vérifiez régulièrement la pile de répertoires avec `dirs` pour garder une trace de votre position.
- Combinez `popd` avec des scripts pour automatiser la navigation dans des projets avec plusieurs sous-répertoires.