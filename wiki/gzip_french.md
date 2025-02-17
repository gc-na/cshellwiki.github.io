# [Linux] Bash gzip Utilisation : Compresser des fichiers

## Overview
La commande `gzip` est utilisée pour compresser des fichiers en utilisant l'algorithme de compression DEFLATE. Elle permet de réduire la taille des fichiers, ce qui est particulièrement utile pour économiser de l'espace de stockage ou pour accélérer le transfert de fichiers sur le réseau.

## Usage
La syntaxe de base de la commande `gzip` est la suivante :

```bash
gzip [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `gzip` :

- `-d` : Décompresse un fichier compressé.
- `-k` : Garde le fichier original après compression.
- `-v` : Affiche des informations détaillées sur le processus de compression.
- `-r` : Compresse récursivement les fichiers dans les sous-répertoires.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `gzip` :

1. **Compresser un fichier :**
   ```bash
   gzip fichier.txt
   ```
   Cela créera un fichier compressé nommé `fichier.txt.gz`.

2. **Décompresser un fichier :**
   ```bash
   gzip -d fichier.txt.gz
   ```
   Cela restaurera le fichier original `fichier.txt`.

3. **Compresser tout le contenu d'un répertoire :**
   ```bash
   gzip -r mon_repertoire/
   ```
   Cela compressera tous les fichiers dans `mon_repertoire` et ses sous-répertoires.

4. **Compresser un fichier tout en gardant l'original :**
   ```bash
   gzip -k fichier.txt
   ```
   Cela créera `fichier.txt.gz` tout en conservant `fichier.txt`.

5. **Afficher les détails de la compression :**
   ```bash
   gzip -v fichier.txt
   ```
   Cela affichera des informations sur la compression, y compris la taille originale et la taille compressée.

## Tips
- Utilisez l'option `-k` si vous souhaitez conserver les fichiers originaux après compression.
- Pour des fichiers très volumineux, envisagez d'utiliser `gzip` en combinaison avec d'autres outils comme `tar` pour une compression plus efficace.
- Vérifiez toujours la taille des fichiers compressés pour vous assurer que la compression a été efficace.