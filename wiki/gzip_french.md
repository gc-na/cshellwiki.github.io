# [Linux] C Shell (csh) gzip Utilisation : Compresser des fichiers

## Overview
La commande `gzip` est utilisée pour compresser des fichiers afin de réduire leur taille. Elle utilise l'algorithme de compression DEFLATE et est souvent utilisée pour économiser de l'espace de stockage ou pour accélérer le transfert de fichiers sur le réseau.

## Usage
La syntaxe de base de la commande `gzip` est la suivante :

```csh
gzip [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `gzip` :

- `-d` : Décompresse un fichier compressé.
- `-k` : Conserve le fichier d'origine lors de la compression.
- `-v` : Affiche des informations détaillées sur le processus de compression.
- `-r` : Compresse tous les fichiers dans un répertoire de manière récursive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `gzip` :

1. Compresser un fichier :
   ```csh
   gzip fichier.txt
   ```

2. Décompresser un fichier :
   ```csh
   gzip -d fichier.txt.gz
   ```

3. Conserver le fichier d'origine lors de la compression :
   ```csh
   gzip -k fichier.txt
   ```

4. Compresser tous les fichiers d'un répertoire :
   ```csh
   gzip -r mon_repertoire/
   ```

5. Afficher des informations détaillées lors de la compression :
   ```csh
   gzip -v fichier.txt
   ```

## Tips
- Assurez-vous de vérifier l'espace disponible sur votre disque avant de compresser de gros fichiers.
- Utilisez l'option `-k` si vous souhaitez conserver l'original sans le supprimer.
- Pour décompresser plusieurs fichiers à la fois, vous pouvez utiliser un joker, par exemple `gzip -d *.gz`.