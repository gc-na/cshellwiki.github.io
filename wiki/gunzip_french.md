# [Linux] C Shell (csh) gunzip : Décompresser des fichiers gzip

## Overview
La commande `gunzip` est utilisée pour décompresser des fichiers compressés au format gzip. Elle permet de restaurer les fichiers à leur état original, facilitant ainsi leur utilisation.

## Usage
La syntaxe de base de la commande `gunzip` est la suivante :

```
gunzip [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `gunzip` :

- `-c` : Affiche le contenu décompressé sur la sortie standard sans supprimer le fichier d'origine.
- `-f` : Force la décompression, même si le fichier de destination existe déjà.
- `-k` : Conserve le fichier compressé après la décompression.
- `-r` : Décompresse tous les fichiers dans les sous-répertoires.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `gunzip` :

1. Décompresser un fichier simple :
   ```csh
   gunzip fichier.txt.gz
   ```

2. Afficher le contenu décompressé sans supprimer le fichier compressé :
   ```csh
   gunzip -c fichier.txt.gz
   ```

3. Décompresser tout fichier dans un répertoire :
   ```csh
   gunzip *.gz
   ```

4. Décompresser un fichier tout en conservant l'original :
   ```csh
   gunzip -k fichier.txt.gz
   ```

5. Décompresser tous les fichiers dans un répertoire et ses sous-répertoires :
   ```csh
   gunzip -r dossier/
   ```

## Tips
- Toujours vérifier l'espace disque disponible avant de décompresser de gros fichiers pour éviter les erreurs.
- Utiliser l'option `-k` si vous souhaitez garder les fichiers compressés après la décompression.
- Pour les fichiers très volumineux, envisagez d'utiliser `gunzip -c` avec une redirection vers un fichier pour éviter de surcharger la sortie standard.