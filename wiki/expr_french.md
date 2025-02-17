# [Linux] Bash expr Utilisation : Évaluer des expressions

## Overview
La commande `expr` est utilisée pour évaluer des expressions arithmétiques, des chaînes de caractères et des comparaisons dans un environnement Bash. Elle permet d'effectuer des calculs simples et de manipuler des chaînes de manière efficace.

## Usage
La syntaxe de base de la commande `expr` est la suivante :

```bash
expr [options] [arguments]
```

## Common Options
- `+` : Additionne deux nombres.
- `-` : Soustrait un nombre d'un autre.
- `*` : Multiplie deux nombres (doit être échappé avec un antislash `\`).
- `/` : Divise un nombre par un autre.
- `%` : Calcule le reste de la division.
- `=` : Évalue l'égalité entre deux valeurs.
- `!=` : Évalue l'inégalité entre deux valeurs.
- `>` : Vérifie si la première valeur est supérieure à la seconde.
- `<` : Vérifie si la première valeur est inférieure à la seconde.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `expr` :

### Exemple 1 : Addition
```bash
expr 5 + 3
```
*Sortie :* `8`

### Exemple 2 : Soustraction
```bash
expr 10 - 4
```
*Sortie :* `6`

### Exemple 3 : Multiplication
```bash
expr 4 \* 2
```
*Sortie :* `8`

### Exemple 4 : Division
```bash
expr 20 / 5
```
*Sortie :* `4`

### Exemple 5 : Comparaison
```bash
expr 5 \> 3
```
*Sortie :* `1` (vrai)

### Exemple 6 : Longueur d'une chaîne
```bash
expr length "Bonjour"
```
*Sortie :* `7`

## Tips
- Utilisez des parenthèses pour contrôler l'ordre des opérations, par exemple : `expr \( 5 + 3 \) \* 2`.
- Évitez d'utiliser `expr` pour des calculs complexes ; préférez les constructions arithmétiques intégrées de Bash comme `$(( ))`.
- N'oubliez pas d'échapper les opérateurs comme `*` pour éviter des erreurs de syntaxe.