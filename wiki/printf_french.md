# [Linux] Bash printf Utilisation : Affichage formaté de texte

## Overview
La commande `printf` en Bash est utilisée pour afficher du texte formaté sur la sortie standard. Elle permet de contrôler précisément la mise en forme des chaînes de caractères, des nombres et d'autres types de données.

## Usage
La syntaxe de base de la commande `printf` est la suivante :

```bash
printf [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `printf` :

- `-v var`: Stocke le résultat dans la variable `var` au lieu de l'afficher.
- `--help`: Affiche l'aide et les options disponibles.
- `--version`: Affiche la version de `printf`.

## Common Examples

### Exemple 1 : Affichage simple
Pour afficher une chaîne de caractères :

```bash
printf "Bonjour, monde!\n"
```

### Exemple 2 : Affichage formaté
Pour afficher un nombre avec un format spécifique :

```bash
printf "Le nombre est : %.2f\n" 3.14159
```

### Exemple 3 : Affichage de plusieurs valeurs
Pour afficher plusieurs valeurs avec des formats différents :

```bash
printf "Nom : %s, Âge : %d\n" "Alice" 30
```

### Exemple 4 : Utilisation de variables
Pour utiliser des variables dans l'affichage :

```bash
nom="Bob"
age=25
printf "Nom : %s, Âge : %d\n" "$nom" "$age"
```

## Tips
- Utilisez `\n` pour ajouter des sauts de ligne dans vos chaînes.
- Soyez attentif aux spécificateurs de format pour garantir que les données sont affichées correctement.
- Vous pouvez utiliser `printf` dans des scripts pour générer des rapports ou des logs formatés.