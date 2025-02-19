# [Linux] C Shell (csh) pushd : [changer de répertoire avec une pile]

## Overview
La commande `pushd` dans C Shell (csh) permet de changer de répertoire tout en sauvegardant le répertoire actuel dans une pile. Cela facilite la navigation entre plusieurs répertoires, car vous pouvez revenir rapidement au répertoire précédent.

## Usage
La syntaxe de base de la commande `pushd` est la suivante :

```csh
pushd [options] [arguments]
```

## Common Options
- `+n` : Accède au n-ième répertoire de la pile.
- `-` : Retourne au répertoire précédent dans la pile.

## Common Examples

### Exemple 1 : Changer de répertoire
Pour changer de répertoire et sauvegarder le répertoire actuel :
```csh
pushd /chemin/vers/nouveau/repertoire
```

### Exemple 2 : Accéder à un répertoire dans la pile
Pour accéder au deuxième répertoire de la pile :
```csh
pushd +2
```

### Exemple 3 : Retourner au répertoire précédent
Pour revenir au répertoire précédent :
```csh
pushd -
```

## Tips
- Utilisez `dirs` pour afficher la liste des répertoires dans la pile.
- Combinez `pushd` avec `popd` pour naviguer facilement entre plusieurs répertoires.
- Pensez à utiliser `pushd` lorsque vous travaillez sur plusieurs projets pour garder une trace de vos répertoires de travail.