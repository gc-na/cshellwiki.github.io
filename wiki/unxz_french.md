# [Linux] Bash unxz : Décompresser des fichiers .xz

## Overview
La commande `unxz` est utilisée pour décompresser des fichiers compressés au format `.xz`. Elle est souvent utilisée pour réduire la taille des fichiers tout en maintenant une bonne qualité de compression.

## Usage
La syntaxe de base de la commande `unxz` est la suivante :

```bash
unxz [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `unxz` :

- `-k`, `--keep` : Conserve le fichier d'origine après la décompression.
- `-f`, `--force` : Force la décompression même si le fichier de destination existe déjà.
- `-v`, `--verbose` : Affiche des informations détaillées sur le processus de décompression.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `unxz` :

1. Décompresser un fichier `.xz` :

   ```bash
   unxz fichier.xz
   ```

2. Décompresser un fichier tout en conservant le fichier d'origine :

   ```bash
   unxz -k fichier.xz
   ```

3. Décompresser un fichier avec affichage des détails :

   ```bash
   unxz -v fichier.xz
   ```

4. Forcer la décompression même si le fichier de destination existe :

   ```bash
   unxz -f fichier.xz
   ```

## Tips
- Assurez-vous d'avoir suffisamment d'espace disque avant de décompresser des fichiers volumineux.
- Utilisez l'option `-k` si vous souhaitez conserver le fichier compressé pour une utilisation future.
- Pour des fichiers compressés en série, vous pouvez utiliser `unxz` sur plusieurs fichiers à la fois en les listant dans la commande.