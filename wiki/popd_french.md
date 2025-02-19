# [Linux] C Shell (csh) popd : Gérer la pile de répertoires

## Overview
La commande `popd` dans C Shell (csh) permet de supprimer le répertoire supérieur de la pile de répertoires et de changer le répertoire de travail courant à celui qui se trouve au sommet de cette pile. Cela facilite la navigation entre différents répertoires sans avoir à taper le chemin complet.

## Usage
La syntaxe de base de la commande `popd` est la suivante :

```csh
popd [options]
```

## Common Options
- `-n` : Ne pas changer le répertoire courant, mais afficher le répertoire qui serait sélectionné.
- `+n` : Spécifie un index dans la pile de répertoires à partir du sommet (0 étant le sommet).

## Common Examples

### Exemple 1 : Utilisation de base
Pour revenir au répertoire supérieur dans la pile :

```csh
popd
```

### Exemple 2 : Afficher le répertoire sans changer
Pour afficher le répertoire supérieur sans changer le répertoire courant :

```csh
popd -n
```

### Exemple 3 : Utiliser un index spécifique
Pour changer le répertoire courant au répertoire à l'index 1 de la pile :

```csh
popd +1
```

## Tips
- Assurez-vous d'utiliser `pushd` pour ajouter des répertoires à la pile avant d'utiliser `popd`.
- Utilisez `dirs` pour afficher la pile de répertoires actuelle avant de faire un `popd`, afin de savoir où vous allez.
- Évitez d'utiliser `popd` si la pile est vide, car cela peut générer une erreur.