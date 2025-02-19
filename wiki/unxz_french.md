# [Linux] C Shell (csh) unxz : Décompresser des fichiers .xz

## Overview
La commande `unxz` est utilisée pour décompresser des fichiers compressés au format `.xz`. Elle permet de restaurer les fichiers à leur état original après compression, facilitant ainsi l'accès aux données.

## Usage
La syntaxe de base de la commande `unxz` est la suivante :

```csh
unxz [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `unxz` :

- `-k` : Garde le fichier d'origine après décompression.
- `-f` : Force la décompression, même si le fichier de destination existe déjà.
- `-v` : Affiche des informations détaillées sur le processus de décompression.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `unxz` :

1. Décompresser un fichier `.xz` :

   ```csh
   unxz fichier.xz
   ```

2. Décompresser un fichier et garder l'original :

   ```csh
   unxz -k fichier.xz
   ```

3. Forcer la décompression d'un fichier existant :

   ```csh
   unxz -f fichier.xz
   ```

4. Afficher des informations détaillées lors de la décompression :

   ```csh
   unxz -v fichier.xz
   ```

## Tips
- Assurez-vous d'avoir suffisamment d'espace disque avant de décompresser de gros fichiers.
- Utilisez l'option `-k` si vous souhaitez conserver l'archive compressée après la décompression.
- Vérifiez toujours les fichiers décompressés pour vous assurer qu'ils sont intacts et complets.