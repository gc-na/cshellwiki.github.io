# [Linux] Bash test usage : Vérifier des conditions

## Overview
La commande `test` en Bash est utilisée pour évaluer des expressions conditionnelles. Elle permet de vérifier des fichiers, des chaînes de caractères, et des valeurs numériques, facilitant ainsi la prise de décisions dans les scripts.

## Usage
La syntaxe de base de la commande `test` est la suivante :

```bash
test [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `test` :

- `-e [fichier]` : Vérifie si le fichier existe.
- `-d [répertoire]` : Vérifie si le chemin spécifié est un répertoire.
- `-f [fichier]` : Vérifie si le chemin spécifié est un fichier régulier.
- `-z [chaîne]` : Vérifie si la chaîne est vide.
- `-n [chaîne]` : Vérifie si la chaîne n'est pas vide.
- `[valeur1] -eq [valeur2]` : Vérifie si les deux valeurs sont égales.
- `[valeur1] -lt [valeur2]` : Vérifie si la première valeur est inférieure à la seconde.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `test` :

1. Vérifier si un fichier existe :

   ```bash
   test -e mon_fichier.txt && echo "Le fichier existe."
   ```

2. Vérifier si un répertoire existe :

   ```bash
   test -d mon_repertoire && echo "C'est un répertoire."
   ```

3. Vérifier si une chaîne est vide :

   ```bash
   ma_chaine=""
   test -z "$ma_chaine" && echo "La chaîne est vide."
   ```

4. Comparer deux nombres :

   ```bash
   a=5
   b=10
   test $a -lt $b && echo "$a est inférieur à $b."
   ```

5. Vérifier si un fichier est un fichier régulier :

   ```bash
   test -f mon_script.sh && echo "C'est un fichier régulier."
   ```

## Tips
- Utilisez `[` comme une alternative à `test`, par exemple : `[ -e mon_fichier.txt ]`.
- N'oubliez pas d'ajouter des espaces autour des crochets lors de l'utilisation de `[` et `]`.
- Combinez plusieurs tests avec `&&` et `||` pour créer des conditions plus complexes.
- Utilisez des parenthèses pour regrouper des expressions si nécessaire, par exemple : `test \( -e fichier1 -o -e fichier2 \)`.