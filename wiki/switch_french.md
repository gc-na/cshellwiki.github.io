# [Unix] C Shell (csh) switch : Changer de valeur d'une variable

## Overview
La commande `switch` dans C Shell (csh) est utilisée pour effectuer des comparaisons conditionnelles. Elle permet de tester une variable contre plusieurs valeurs possibles et d'exécuter des commandes en fonction de la correspondance trouvée.

## Usage
La syntaxe de base de la commande `switch` est la suivante :

```csh
switch (expression)
    case valeur1:
        commandes1
        breaksw
    case valeur2:
        commandes2
        breaksw
    default:
        commandes_par_defaut
end
```

## Common Options
- `case`: Définit une valeur à comparer avec l'expression.
- `breaksw`: Met fin à l'exécution des cas dans le switch.
- `default`: Spécifie les commandes à exécuter si aucune des valeurs ne correspond.

## Common Examples

### Exemple 1 : Utilisation basique
```csh
set fruit = "pomme"
switch ($fruit)
    case "pomme":
        echo "C'est une pomme."
        breaksw
    case "banane":
        echo "C'est une banane."
        breaksw
    default:
        echo "Fruit inconnu."
end
```

### Exemple 2 : Comparaison de plusieurs valeurs
```csh
set jour = "lundi"
switch ($jour)
    case "lundi":
    case "mardi":
        echo "C'est le début de la semaine."
        breaksw
    case "samedi":
    case "dimanche":
        echo "C'est le week-end."
        breaksw
    default:
        echo "C'est un jour de semaine."
end
```

### Exemple 3 : Utilisation avec des variables d'environnement
```csh
set status = $1
switch ($status)
    case "success":
        echo "L'opération a réussi."
        breaksw
    case "failure":
        echo "L'opération a échoué."
        breaksw
    default:
        echo "Statut inconnu."
end
```

## Tips
- Utilisez `breaksw` pour éviter d'exécuter des cas supplémentaires après une correspondance.
- Assurez-vous que les valeurs dans les cases sont bien définies pour éviter des résultats inattendus.
- N'oubliez pas de terminer votre structure `switch` avec `end` pour indiquer la fin des conditions.