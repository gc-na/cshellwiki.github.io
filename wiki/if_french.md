# [Linux] C Shell (csh) if : Évaluer des conditions

## Overview
La commande `if` dans C Shell (csh) est utilisée pour évaluer des conditions et exécuter des commandes en fonction du résultat de cette évaluation. Elle permet d'exécuter des blocs de code conditionnellement, ce qui est essentiel pour le contrôle de flux dans les scripts.

## Usage
La syntaxe de base de la commande `if` est la suivante :

```csh
if (condition) then
    commandes
endif
```

## Common Options
- `then` : Indique le début du bloc de commandes à exécuter si la condition est vraie.
- `endif` : Marque la fin de la structure conditionnelle `if`.

## Common Examples

### Exemple 1 : Vérifier si un fichier existe
```csh
if (-e monfichier.txt) then
    echo "Le fichier existe."
endif
```

### Exemple 2 : Vérifier si une variable est vide
```csh
set maVariable = ""
if ("$maVariable" == "") then
    echo "La variable est vide."
endif
```

### Exemple 3 : Comparer des nombres
```csh
set a = 10
set b = 20
if ($a < $b) then
    echo "$a est inférieur à $b."
endif
```

### Exemple 4 : Utiliser `else`
```csh
if (-e monfichier.txt) then
    echo "Le fichier existe."
else
    echo "Le fichier n'existe pas."
endif
```

## Tips
- Assurez-vous d'utiliser des parenthèses autour de la condition.
- Utilisez des espaces autour des opérateurs pour éviter les erreurs de syntaxe.
- N'oubliez pas de fermer chaque bloc `if` avec `endif` pour éviter des erreurs d'exécution.