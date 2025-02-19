# [Linux] C Shell (csh) @ Utilisation : Exécute des calculs arithmétiques

## Overview
La commande `@` dans C Shell (csh) est utilisée pour effectuer des calculs arithmétiques simples. Elle permet d'assigner des valeurs à des variables et de réaliser des opérations mathématiques de base.

## Usage
La syntaxe de base de la commande `@` est la suivante :

```csh
@ [options] [arguments]
```

## Common Options
- `-v` : Affiche la valeur de la variable après l'opération.
- `-n` : N'exécute pas la commande, mais affiche ce qui serait exécuté.

## Common Examples

### Exemple 1 : Addition
Pour additionner deux nombres et assigner le résultat à une variable :

```csh
set a = 5
set b = 10
@ c = $a + $b
echo $c  # Affiche 15
```

### Exemple 2 : Soustraction
Pour soustraire un nombre d'un autre :

```csh
set x = 20
set y = 8
@ z = $x - $y
echo $z  # Affiche 12
```

### Exemple 3 : Multiplication
Pour multiplier deux nombres :

```csh
set p = 4
set q = 7
@ r = $p * $q
echo $r  # Affiche 28
```

### Exemple 4 : Division
Pour diviser un nombre par un autre :

```csh
set num = 30
set denom = 6
@ result = $num / $denom
echo $result  # Affiche 5
```

## Tips
- Utilisez des parenthèses pour contrôler l'ordre des opérations, par exemple : `@ result = ($a + $b) * $c`.
- Assurez-vous que les variables sont initialisées avant de les utiliser dans des calculs.
- Pour éviter les erreurs, vérifiez que vous ne divisez pas par zéro.