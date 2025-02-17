# [Linux] Bash xargs : Exécuter des commandes avec des arguments

## Overview
La commande `xargs` est utilisée pour construire et exécuter des commandes à partir de l'entrée standard. Elle permet de passer des arguments à d'autres commandes, ce qui est particulièrement utile lorsque vous avez une liste d'éléments à traiter.

## Usage
La syntaxe de base de la commande `xargs` est la suivante :

```bash
xargs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `xargs` :

- `-n N` : Limite le nombre d'arguments passés à la commande à N.
- `-d DELIM` : Utilise un délimiteur spécifique pour séparer les entrées.
- `-0` : Attend des entrées séparées par des caractères null (utile avec `find`).
- `-p` : Demande une confirmation avant d'exécuter chaque commande.
- `-I {}` : Remplace `{}` par l'entrée lue.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `xargs` :

1. **Supprimer des fichiers listés dans un fichier :**
   ```bash
   cat fichiers.txt | xargs rm
   ```

2. **Compresser plusieurs fichiers :**
   ```bash
   ls *.txt | xargs tar -czf archive.tar.gz
   ```

3. **Trouver et supprimer des fichiers vides :**
   ```bash
   find . -type f -empty | xargs rm
   ```

4. **Compter le nombre de mots dans plusieurs fichiers :**
   ```bash
   ls *.txt | xargs wc -w
   ```

5. **Utiliser un délimiteur spécifique :**
   ```bash
   echo -e "fichier1.txt\nfichier2.txt" | xargs -d '\n' cat
   ```

## Tips
- Utilisez l'option `-0` avec `find` pour gérer les noms de fichiers contenant des espaces ou des caractères spéciaux.
- Soyez prudent avec `rm` et d'autres commandes destructrices ; utilisez l'option `-p` pour confirmer avant d'exécuter.
- Combinez `xargs` avec d'autres commandes pour des opérations en chaîne efficaces.