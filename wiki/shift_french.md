# [Linux] Bash shift usage : décaler les paramètres positionnels

## Overview
La commande `shift` en Bash est utilisée pour décaler les paramètres positionnels vers la gauche. Cela signifie que le premier paramètre devient le second, le second devient le troisième, et ainsi de suite. Cela est particulièrement utile dans les scripts où vous devez traiter plusieurs arguments.

## Usage
La syntaxe de base de la commande `shift` est la suivante :

```bash
shift [n]
```

Ici, `n` est le nombre de positions à décaler. Si `n` n'est pas spécifié, il décale par défaut d'une position.

## Common Options
- `n` : Nombre d'arguments à décaler. Si omis, le décalage est de 1.

## Common Examples

### Exemple 1 : Décalage simple
```bash
#!/bin/bash
echo "Avant shift : $1 $2 $3"
shift
echo "Après shift : $1 $2 $3"
```
Dans cet exemple, si vous exécutez le script avec trois arguments, le premier argument sera supprimé après l'exécution de `shift`.

### Exemple 2 : Décalage multiple
```bash
#!/bin/bash
echo "Avant shift : $1 $2 $3"
shift 2
echo "Après shift : $1 $2 $3"
```
Ici, après un décalage de 2, les deux premiers arguments sont supprimés.

### Exemple 3 : Utilisation dans une boucle
```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Traitement de : $1"
    shift
done
```
Cette boucle continue de traiter les arguments tant qu'il en reste, en les décalant à chaque itération.

## Tips
- Utilisez `shift` dans des scripts qui nécessitent le traitement d'une liste d'arguments pour simplifier la gestion des paramètres.
- Soyez prudent avec le nombre de décalages, car décaler plus que le nombre d'arguments fournis peut entraîner des erreurs.
- Combinez `shift` avec d'autres commandes comme `getopts` pour une gestion plus avancée des options de script.