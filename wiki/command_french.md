# [Linux] Bash command Utilisation : [afficher le contenu d'un fichier]

## Overview
La commande `cat` est utilisée pour afficher le contenu d'un fichier texte dans le terminal. Elle peut également être utilisée pour concaténer plusieurs fichiers et les afficher ou les écrire dans un nouveau fichier.

## Usage
La syntaxe de base de la commande `cat` est la suivante :

```bash
cat [options] [fichiers]
```

## Common Options
- `-n` : Numérote toutes les lignes de la sortie.
- `-b` : Numérote seulement les lignes non vides.
- `-E` : Affiche un symbole `$` à la fin de chaque ligne.
- `-s` : Supprime les lignes vides supplémentaires.

## Common Examples
Voici quelques exemples pratiques de la commande `cat` :

1. Afficher le contenu d'un fichier :
   ```bash
   cat fichier.txt
   ```

2. Afficher le contenu de plusieurs fichiers :
   ```bash
   cat fichier1.txt fichier2.txt
   ```

3. Créer un nouveau fichier en concaténant plusieurs fichiers :
   ```bash
   cat fichier1.txt fichier2.txt > nouveau_fichier.txt
   ```

4. Afficher le contenu d'un fichier avec la numérotation des lignes :
   ```bash
   cat -n fichier.txt
   ```

5. Supprimer les lignes vides supplémentaires lors de l'affichage :
   ```bash
   cat -s fichier.txt
   ```

## Tips
- Utilisez `cat` pour rapidement visualiser le contenu d'un fichier sans l'ouvrir dans un éditeur de texte.
- Pour des fichiers très longs, envisagez d'utiliser `less` ou `more` pour une navigation plus facile.
- Combinez `cat` avec d'autres commandes en utilisant des pipes pour des traitements avancés.