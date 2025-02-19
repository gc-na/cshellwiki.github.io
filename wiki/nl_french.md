# [Linux] C Shell (csh) nl : numéroter les lignes d'un fichier

## Overview
La commande `nl` est utilisée pour numéroter les lignes d'un fichier texte. Elle permet d'ajouter des numéros de ligne à chaque ligne d'entrée, ce qui est particulièrement utile pour la lecture ou le traitement de fichiers.

## Usage
La syntaxe de base de la commande `nl` est la suivante :

```csh
nl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `nl` :

- `-b` : Définit le type de numérotation des lignes (par exemple, `-b a` pour numéroter toutes les lignes).
- `-f` : Ignore les lignes vides lors de la numérotation.
- `-n` : Définit le format de numérotation (par exemple, `-n ln` pour un numéro de ligne à gauche).
- `-w` : Définit la largeur du numéro de ligne (par défaut, c'est 6).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `nl` :

1. Numéroter toutes les lignes d'un fichier :

   ```csh
   nl fichier.txt
   ```

2. Numéroter uniquement les lignes non vides :

   ```csh
   nl -f fichier.txt
   ```

3. Utiliser un format de numérotation à droite :

   ```csh
   nl -n rn fichier.txt
   ```

4. Spécifier la largeur des numéros de ligne :

   ```csh
   nl -w 4 fichier.txt
   ```

## Tips
- Utilisez l'option `-b` pour contrôler quelles lignes sont numérotées, ce qui peut être utile pour des fichiers avec des sections spécifiques.
- Combinez `nl` avec d'autres commandes comme `grep` pour filtrer le contenu avant de le numéroter.
- Pensez à rediriger la sortie vers un nouveau fichier si vous souhaitez conserver le résultat :

   ```csh
   nl fichier.txt > fichier_numéroté.txt
   ```