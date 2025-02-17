# [Linux] Bash split usage : Diviser des fichiers en morceaux

## Overview
La commande `split` permet de diviser un fichier en plusieurs morceaux de taille spécifiée. Cela est particulièrement utile pour gérer de grands fichiers ou pour faciliter leur transfert.

## Usage
La syntaxe de base de la commande `split` est la suivante :

```bash
split [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `split` :

- `-b SIZE` : Divise le fichier en morceaux de la taille spécifiée (par exemple, `-b 1M` pour des morceaux de 1 Mo).
- `-l LINES` : Divise le fichier après un nombre spécifié de lignes.
- `-d` : Utilise des suffixes numériques pour nommer les fichiers de sortie au lieu de suffixes alphabétiques.
- `--additional-suffix=SUFFIX` : Ajoute un suffixe supplémentaire aux fichiers de sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `split` :

1. Diviser un fichier en morceaux de 100 lignes :

    ```bash
    split -l 100 mon_fichier.txt
    ```

2. Diviser un fichier en morceaux de 10 Mo :

    ```bash
    split -b 10M mon_fichier.txt
    ```

3. Diviser un fichier et utiliser des suffixes numériques :

    ```bash
    split -d -b 1M mon_fichier.txt partie_
    ```

4. Diviser un fichier en morceaux de 50 lignes et ajouter un suffixe `.txt` :

    ```bash
    split -l 50 --additional-suffix=.txt mon_fichier.txt partie_
    ```

## Tips
- Lorsque vous utilisez `split`, vérifiez la taille des morceaux pour éviter de créer trop de fichiers.
- Utilisez l'option `-d` si vous préférez des noms de fichiers plus faciles à trier.
- Pensez à utiliser des suffixes supplémentaires pour mieux identifier vos fichiers de sortie.