# [Linux] Bash bunzip2 : Décompresser des fichiers .bz2

## Overview
La commande `bunzip2` est utilisée pour décompresser des fichiers compressés au format .bz2. Elle est souvent utilisée pour réduire la taille des fichiers afin de faciliter le stockage et le transfert.

## Usage
La syntaxe de base de la commande `bunzip2` est la suivante :

```bash
bunzip2 [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `bunzip2` :

- `-k` : Conserve le fichier d'origine après la décompression.
- `-f` : Force la décompression, même si le fichier de destination existe déjà.
- `-v` : Affiche des informations détaillées sur le processus de décompression.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `bunzip2` :

1. **Décompresser un fichier .bz2** :
   ```bash
   bunzip2 fichier.bz2
   ```

2. **Décompresser un fichier tout en conservant l'original** :
   ```bash
   bunzip2 -k fichier.bz2
   ```

3. **Décompresser plusieurs fichiers .bz2 à la fois** :
   ```bash
   bunzip2 fichier1.bz2 fichier2.bz2
   ```

4. **Décompresser un fichier et forcer l'écrasement du fichier existant** :
   ```bash
   bunzip2 -f fichier.bz2
   ```

5. **Afficher des informations détaillées lors de la décompression** :
   ```bash
   bunzip2 -v fichier.bz2
   ```

## Tips
- Toujours vérifier l'espace disque disponible avant de décompresser de gros fichiers pour éviter les erreurs.
- Utilisez l'option `-k` si vous souhaitez conserver le fichier compressé original pour une utilisation future.
- Pour décompresser des fichiers dans un script, envisagez d'utiliser l'option `-f` pour éviter les interruptions dues à des fichiers existants.