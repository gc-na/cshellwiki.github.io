# [Linux] Bash else : Exécuter une commande alternative

## Overview
La commande `else` dans un script Bash est utilisée dans les structures conditionnelles. Elle permet d'exécuter un bloc de code lorsque la condition précédente est fausse. Cela est particulièrement utile pour gérer des scénarios où plusieurs chemins d'exécution sont nécessaires.

## Usage
La syntaxe de base de la commande `else` est la suivante :

```bash
if [ condition ]; then
    # commandes si la condition est vraie
else
    # commandes si la condition est fausse
fi
```

## Common Options
La commande `else` n'a pas d'options spécifiques, car elle fait partie d'une structure conditionnelle. Cependant, elle est souvent utilisée avec les commandes suivantes :
- `if` : pour vérifier une condition.
- `elif` : pour ajouter des conditions supplémentaires avant d'atteindre le bloc `else`.

## Common Examples

### Exemple 1 : Vérification d'un fichier
```bash
if [ -f "mon_fichier.txt" ]; then
    echo "Le fichier existe."
else
    echo "Le fichier n'existe pas."
fi
```

### Exemple 2 : Vérification d'une variable
```bash
nombre=10
if [ $nombre -gt 20 ]; then
    echo "Le nombre est supérieur à 20."
else
    echo "Le nombre est inférieur ou égal à 20."
fi
```

### Exemple 3 : Utilisation avec `elif`
```bash
note=15
if [ $note -ge 18 ]; then
    echo "Mention Très Bien"
elif [ $note -ge 14 ]; then
    echo "Mention Bien"
else
    echo "Mention Passable"
fi
```

## Tips
- Utilisez des parenthèses pour grouper des conditions complexes.
- N'oubliez pas de toujours fermer vos blocs conditionnels avec `fi`.
- Testez vos scripts avec différentes conditions pour vous assurer qu'ils fonctionnent comme prévu.