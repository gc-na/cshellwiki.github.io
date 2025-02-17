# [Linux] Bash wc utilisation : Compter les lignes, mots et caractères

## Overview
La commande `wc` (word count) est utilisée dans les systèmes Unix et Linux pour compter le nombre de lignes, de mots et de caractères dans un fichier ou une entrée standard. C'est un outil pratique pour obtenir des statistiques sur le contenu des fichiers texte.

## Usage
La syntaxe de base de la commande `wc` est la suivante :

```bash
wc [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `wc` :

- `-l` : Compte uniquement le nombre de lignes.
- `-w` : Compte uniquement le nombre de mots.
- `-c` : Compte uniquement le nombre de caractères.
- `-m` : Compte le nombre de caractères (en tenant compte des caractères multibytes).
- `-L` : Affiche la longueur de la ligne la plus longue.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `wc` :

1. Compter le nombre de lignes dans un fichier :

   ```bash
   wc -l fichier.txt
   ```

2. Compter le nombre de mots dans un fichier :

   ```bash
   wc -w fichier.txt
   ```

3. Compter le nombre de caractères dans un fichier :

   ```bash
   wc -c fichier.txt
   ```

4. Compter le nombre de lignes, de mots et de caractères en une seule commande :

   ```bash
   wc fichier.txt
   ```

5. Compter les lignes d'une entrée standard (par exemple, avec `echo`) :

   ```bash
   echo -e "Ligne 1\nLigne 2\nLigne 3" | wc -l
   ```

## Tips
- Vous pouvez combiner plusieurs options pour obtenir des résultats plus complets. Par exemple, `wc -lw fichier.txt` vous donnera à la fois le nombre de lignes et de mots.
- Pour traiter plusieurs fichiers à la fois, il suffit de les lister après la commande. `wc fichier1.txt fichier2.txt` affichera les résultats pour chaque fichier ainsi qu'un total.
- Utilisez `wc` en combinaison avec d'autres commandes via des pipes pour analyser des données en temps réel. Par exemple, `cat fichier.txt | wc -l` pour compter les lignes d'un fichier.