# [Linux] Bash sort utilisation : Trier les lignes de texte

## Overview
La commande `sort` est utilisée pour trier les lignes de texte dans un fichier ou à partir de l'entrée standard. Elle peut trier les données par ordre alphabétique, numérique, ou selon d'autres critères spécifiés par l'utilisateur.

## Usage
La syntaxe de base de la commande `sort` est la suivante :

```bash
sort [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `sort` :

- `-r` : Trie les lignes dans l'ordre inverse.
- `-n` : Trie les lignes en utilisant un ordre numérique.
- `-k` : Spécifie une clé de tri, permettant de trier selon une colonne spécifique.
- `-u` : Supprime les doublons dans le résultat.
- `-o` : Écrit le résultat dans un fichier spécifié.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `sort` :

1. Trier un fichier par ordre alphabétique :
   ```bash
   sort fichier.txt
   ```

2. Trier un fichier en ordre inverse :
   ```bash
   sort -r fichier.txt
   ```

3. Trier un fichier avec des valeurs numériques :
   ```bash
   sort -n nombres.txt
   ```

4. Trier un fichier en utilisant la deuxième colonne :
   ```bash
   sort -k2 fichier.txt
   ```

5. Écrire le résultat trié dans un nouveau fichier :
   ```bash
   sort fichier.txt -o fichier_trie.txt
   ```

## Tips
- Utilisez l'option `-u` pour obtenir une liste sans doublons, ce qui est utile pour nettoyer des données.
- Combinez `sort` avec d'autres commandes comme `uniq` pour un traitement de données plus avancé.
- Pensez à rediriger la sortie vers un fichier si vous traitez de grandes quantités de données pour éviter de surcharger le terminal.