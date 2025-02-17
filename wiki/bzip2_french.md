# [Linux] Bash bzip2 : Compression de fichiers

## Overview
La commande `bzip2` est utilisée pour compresser des fichiers afin de réduire leur taille. Elle utilise l'algorithme de compression Burrows-Wheeler, qui est efficace pour obtenir un taux de compression élevé. Les fichiers compressés avec `bzip2` ont généralement l'extension `.bz2`.

## Usage
La syntaxe de base de la commande `bzip2` est la suivante :

```bash
bzip2 [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `bzip2` :

- `-d` : Décompresse un fichier `.bz2`.
- `-k` : Garde le fichier original après compression.
- `-f` : Force la compression, même si le fichier de destination existe déjà.
- `-v` : Affiche des informations détaillées sur le processus de compression.
- `-z` : Compresse un fichier (c'est l'option par défaut).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `bzip2` :

1. **Compresser un fichier** :
   ```bash
   bzip2 fichier.txt
   ```
   Cela créera un fichier compressé nommé `fichier.txt.bz2`.

2. **Décompresser un fichier** :
   ```bash
   bzip2 -d fichier.txt.bz2
   ```
   Cela restaurera le fichier original `fichier.txt`.

3. **Compresser tout le contenu d'un répertoire** :
   ```bash
   bzip2 -k *.txt
   ```
   Cela compressera tous les fichiers `.txt` dans le répertoire tout en conservant les fichiers originaux.

4. **Afficher des informations détaillées lors de la compression** :
   ```bash
   bzip2 -v fichier.log
   ```
   Cela affichera des informations sur le processus de compression du fichier `fichier.log`.

## Tips
- Utilisez l'option `-k` si vous souhaitez conserver les fichiers d'origine après compression.
- Pour des fichiers très volumineux, envisagez d'utiliser `pbzip2`, qui permet une compression parallèle et peut accélérer le processus sur des systèmes multi-core.
- Vérifiez toujours l'intégrité des fichiers après décompression pour vous assurer qu'aucune donnée n'a été perdue.