# [Linux] C Shell (csh) comm : Comparer des fichiers ligne par ligne

## Overview
La commande `comm` est utilisée pour comparer deux fichiers triés ligne par ligne. Elle affiche les lignes qui sont présentes dans le premier fichier, celles qui sont présentes dans le second, et celles qui sont communes aux deux fichiers.

## Usage
La syntaxe de base de la commande `comm` est la suivante :

```csh
comm [options] [fichier1] [fichier2]
```

## Common Options
- `-1` : Supprime les lignes uniques au premier fichier.
- `-2` : Supprime les lignes uniques au second fichier.
- `-3` : Supprime les lignes communes aux deux fichiers.
- `-i` : Ignore la casse lors de la comparaison des lignes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `comm` :

1. Comparer deux fichiers et afficher toutes les lignes :
   ```csh
   comm fichier1.txt fichier2.txt
   ```

2. Afficher uniquement les lignes présentes dans le premier fichier :
   ```csh
   comm -13 fichier1.txt fichier2.txt
   ```

3. Afficher uniquement les lignes présentes dans le second fichier :
   ```csh
   comm -12 fichier1.txt fichier2.txt
   ```

4. Comparer deux fichiers en ignorant la casse :
   ```csh
   comm -i fichier1.txt fichier2.txt
   ```

## Tips
- Assurez-vous que les fichiers sont triés avant d'utiliser `comm`, sinon les résultats peuvent ne pas être corrects.
- Utilisez des redirections pour enregistrer la sortie de la commande dans un fichier pour une analyse ultérieure.
- Combinez `comm` avec d'autres commandes comme `sort` pour des comparaisons plus complexes.