# [Linux] Bash comm : comparer des fichiers ligne par ligne

## Overview
La commande `comm` est utilisée pour comparer deux fichiers triés ligne par ligne. Elle affiche les lignes qui sont uniques à chaque fichier ainsi que les lignes communes. Cela permet de visualiser les différences et les similitudes entre les deux fichiers.

## Usage
La syntaxe de base de la commande `comm` est la suivante :

```bash
comm [options] [fichier1] [fichier2]
```

## Common Options
- `-1` : Supprime les lignes uniques au premier fichier de la sortie.
- `-2` : Supprime les lignes uniques au deuxième fichier de la sortie.
- `-3` : Supprime les lignes communes de la sortie.
- `-i` : Ignore la casse lors de la comparaison des lignes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `comm` :

1. **Comparer deux fichiers et afficher toutes les lignes :**
   ```bash
   comm fichier1.txt fichier2.txt
   ```

2. **Afficher uniquement les lignes uniques au premier fichier :**
   ```bash
   comm -13 fichier1.txt fichier2.txt
   ```

3. **Afficher uniquement les lignes communes :**
   ```bash
   comm -12 fichier1.txt fichier2.txt
   ```

4. **Comparer deux fichiers en ignorant la casse :**
   ```bash
   comm -i fichier1.txt fichier2.txt
   ```

## Tips
- Assurez-vous que les fichiers sont triés avant d'utiliser `comm`, sinon les résultats peuvent être imprévisibles.
- Utilisez `sort` pour trier les fichiers avant la comparaison si nécessaire :
  ```bash
  sort fichier1.txt > fichier1_sorted.txt
  sort fichier2.txt > fichier2_sorted.txt
  comm fichier1_sorted.txt fichier2_sorted.txt
  ```
- Combinez `comm` avec d'autres commandes pour des analyses plus complexes, par exemple en utilisant des pipes pour filtrer les résultats.