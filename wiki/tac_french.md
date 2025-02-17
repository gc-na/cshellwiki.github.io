# [Linux] Bash tac Utilisation : Inverser le contenu des fichiers

## Overview
La commande `tac` est utilisée pour afficher le contenu d'un fichier en inversant l'ordre des lignes. Contrairement à la commande `cat`, qui affiche les lignes dans l'ordre normal, `tac` les affiche de la dernière à la première.

## Usage
La syntaxe de base de la commande `tac` est la suivante :

```bash
tac [options] [arguments]
```

## Common Options
- `-b`, `--before`: Ajoute une ligne vide avant chaque ligne.
- `-r`, `--regex`: Interprète les séparateurs de lignes comme des expressions régulières.
- `-s`, `--separator=STRING`: Définit un séparateur de lignes personnalisé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `tac` :

1. **Inverser le contenu d'un fichier :**
   ```bash
   tac fichier.txt
   ```

2. **Inverser le contenu d'un fichier et ajouter une ligne vide avant chaque ligne :**
   ```bash
   tac -b fichier.txt
   ```

3. **Utiliser un séparateur personnalisé :**
   ```bash
   tac -s ";" fichier.txt
   ```

4. **Inverser le contenu de plusieurs fichiers :**
   ```bash
   tac fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez `tac` en combinaison avec d'autres commandes, comme `grep`, pour filtrer le contenu avant de l'inverser.
- Pensez à rediriger la sortie vers un nouveau fichier si vous souhaitez enregistrer le résultat :
  ```bash
  tac fichier.txt > fichier_inverse.txt
  ```
- Soyez prudent avec les fichiers très volumineux, car `tac` peut consommer beaucoup de mémoire en fonction de la taille du fichier.