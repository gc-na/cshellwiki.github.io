# [Linux] Bash gunzip : Décompresser des fichiers gzip

## Overview
La commande `gunzip` est utilisée pour décompresser des fichiers compressés au format gzip. Elle permet de restaurer les fichiers à leur état original, facilitant ainsi leur utilisation.

## Usage
La syntaxe de base de la commande `gunzip` est la suivante :

```bash
gunzip [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `gunzip` :

- `-c` : Affiche le contenu décompressé sur la sortie standard sans supprimer le fichier d'origine.
- `-f` : Force la décompression, même si le fichier d'origine existe déjà.
- `-k` : Garde le fichier d'origine après la décompression.
- `-r` : Décompresse les fichiers dans les sous-répertoires de manière récursive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `gunzip` :

1. Décompresser un fichier :
   ```bash
   gunzip fichier.gz
   ```

2. Afficher le contenu décompressé sans supprimer le fichier d'origine :
   ```bash
   gunzip -c fichier.gz
   ```

3. Décompresser un fichier tout en gardant le fichier d'origine :
   ```bash
   gunzip -k fichier.gz
   ```

4. Décompresser tous les fichiers `.gz` dans un répertoire et ses sous-répertoires :
   ```bash
   gunzip -r *.gz
   ```

## Tips
- Vérifiez toujours l'espace disque disponible avant de décompresser des fichiers volumineux pour éviter les erreurs.
- Utilisez l'option `-c` pour visualiser le contenu d'un fichier gzip sans le décompresser physiquement, ce qui peut être utile pour des fichiers de grande taille.
- Pensez à utiliser `gzip -t` pour tester l'intégrité d'un fichier gzip avant de le décompresser.