# [Linux] Bash readonly : Définit des variables en lecture seule

## Overview
La commande `readonly` en Bash permet de définir des variables qui ne peuvent pas être modifiées par la suite. Une fois qu'une variable est marquée comme `readonly`, toute tentative de modification de sa valeur entraînera une erreur. Cela est utile pour protéger des valeurs critiques dans vos scripts.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
readonly [options] [arguments]
```

## Common Options
- `-p` : Affiche une liste des variables en lecture seule actuellement définies.

## Common Examples

### Exemple 1 : Définir une variable en lecture seule
```bash
readonly VAR="Valeur fixe"
```
Dans cet exemple, `VAR` est définie comme une variable en lecture seule avec la valeur "Valeur fixe".

### Exemple 2 : Tentative de modification d'une variable en lecture seule
```bash
readonly VAR="Valeur fixe"
VAR="Nouvelle valeur"  # Cela générera une erreur
```
Ici, la tentative de modification de `VAR` entraînera une erreur, car elle est définie comme `readonly`.

### Exemple 3 : Afficher les variables en lecture seule
```bash
readonly -p
```
Cette commande affichera toutes les variables qui ont été définies comme `readonly` dans la session actuelle.

## Tips
- Utilisez `readonly` pour protéger les variables qui contiennent des informations sensibles ou critiques dans vos scripts.
- Pensez à utiliser `readonly` pour les constantes qui ne doivent pas changer, afin d'éviter des erreurs accidentelles.
- Vérifiez régulièrement les variables en lecture seule avec `readonly -p` pour garder une trace de celles qui sont définies dans votre environnement.