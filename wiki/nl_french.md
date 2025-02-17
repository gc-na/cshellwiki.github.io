# [Linux] Bash nl Utilisation : Numérote les lignes d'un fichier

## Overview
La commande `nl` est utilisée pour numéroter les lignes d'un fichier texte. Elle permet d'ajouter des numéros de ligne à chaque ligne du fichier, ce qui est particulièrement utile pour la lecture et l'analyse de fichiers longs.

## Usage
La syntaxe de base de la commande `nl` est la suivante :

```bash
nl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `nl` :

- `-b` : Définit le type de numérotation (par exemple, `-b a` pour numéroter toutes les lignes).
- `-f` : Ignore les lignes vides dans la numérotation.
- `-n` : Définit le format de numérotation (par exemple, `-n ln` pour numéroter à gauche).
- `-w` : Définit la largeur des numéros de ligne (par exemple, `-w 4` pour une largeur de 4 caractères).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `nl` :

1. Numéroter les lignes d'un fichier texte simple :
   ```bash
   nl fichier.txt
   ```

2. Numéroter toutes les lignes en ignorant les lignes vides :
   ```bash
   nl -f fichier.txt
   ```

3. Changer le format de numérotation pour aligner à droite :
   ```bash
   nl -n rn fichier.txt
   ```

4. Spécifier une largeur de numéro de ligne :
   ```bash
   nl -w 5 fichier.txt
   ```

5. Numéroter uniquement les lignes non vides :
   ```bash
   nl -b a fichier.txt
   ```

## Tips
- Utilisez `nl` avec d'autres commandes comme `cat` pour afficher un fichier numéroté directement dans le terminal.
- Combinez `nl` avec des redirections pour enregistrer la sortie numérotée dans un nouveau fichier :
  ```bash
  nl fichier.txt > fichier_numéroté.txt
  ```
- Explorez les différentes options pour personnaliser la numérotation selon vos besoins spécifiques.