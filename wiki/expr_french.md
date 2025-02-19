# [Linux] C Shell (csh) expr Utilisation : Évaluer des expressions

## Overview
La commande `expr` dans C Shell (csh) est utilisée pour évaluer des expressions arithmétiques, logiques et de chaîne. Elle permet de réaliser des calculs simples et de manipuler des chaînes de caractères directement dans le terminal.

## Usage
La syntaxe de base de la commande `expr` est la suivante :

```csh
expr [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `expr` :

- `+` : Additionne deux nombres.
- `-` : Soustrait un nombre d'un autre.
- `*` : Multiplie deux nombres.
- `/` : Divise un nombre par un autre.
- `%` : Calcule le reste de la division entière.
- `=` : Évalue si deux chaînes ou nombres sont égaux.
- `!=` : Évalue si deux chaînes ou nombres ne sont pas égaux.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `expr` :

### Addition de deux nombres
```csh
set result = `expr 5 + 3`
echo $result  # Affiche 8
```

### Soustraction de deux nombres
```csh
set result = `expr 10 - 4`
echo $result  # Affiche 6
```

### Multiplication de deux nombres
```csh
set result = `expr 7 \* 6`
echo $result  # Affiche 42
```

### Division de deux nombres
```csh
set result = `expr 20 / 4`
echo $result  # Affiche 5
```

### Vérification d'égalité
```csh
set is_equal = `expr 10 = 10`
echo $is_equal  # Affiche 1 (vrai)
```

### Vérification de non-égalité
```csh
set is_not_equal = `expr 10 != 5`
echo $is_not_equal  # Affiche 1 (vrai)
```

## Tips
- Utilisez des backticks (`` ` ``) pour encapsuler la commande `expr` afin de capturer la sortie dans une variable.
- Évitez d'utiliser des espaces autour des opérateurs pour éviter des erreurs de syntaxe.
- Pour les multiplications, n'oubliez pas d'échapper l'astérisque (`\*`) pour qu'il soit interprété correctement par le shell.