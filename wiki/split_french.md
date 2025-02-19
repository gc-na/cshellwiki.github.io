# [Linux] C Shell (csh) split : Diviser des fichiers en morceaux

## Overview
La commande `split` permet de diviser un fichier en plusieurs morceaux de taille spécifiée. Cela peut être utile pour gérer de grands fichiers ou pour faciliter le transfert de données.

## Usage
La syntaxe de base de la commande `split` est la suivante :

```csh
split [options] [arguments]
```

## Common Options
- `-b SIZE` : Divise le fichier en morceaux de la taille spécifiée (par exemple, `-b 1M` pour des morceaux de 1 Mo).
- `-l LINES` : Divise le fichier après un nombre spécifié de lignes.
- `-d` : Utilise des suffixes numériques pour nommer les fichiers de sortie au lieu de lettres.
- `--additional-suffix=SUFFIX` : Ajoute un suffixe supplémentaire aux fichiers de sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `split` :

1. Diviser un fichier en morceaux de 1000 lignes :
   ```csh
   split -l 1000 mon_fichier.txt
   ```

2. Diviser un fichier en morceaux de 5 Mo :
   ```csh
   split -b 5M mon_fichier_grand.txt
   ```

3. Diviser un fichier et nommer les morceaux avec des suffixes numériques :
   ```csh
   split -d -b 1M mon_fichier.txt
   ```

4. Diviser un fichier en morceaux de 200 lignes et ajouter un suffixe `.part` :
   ```csh
   split -l 200 --additional-suffix=.part mon_fichier.txt
   ```

## Tips
- Vérifiez la taille de vos fichiers de sortie pour vous assurer qu'ils correspondent à vos attentes.
- Utilisez l'option `-d` si vous préférez des noms de fichiers numériques pour éviter toute confusion.
- Pensez à combiner `split` avec d'autres commandes comme `cat` pour recombiner les fichiers si nécessaire.