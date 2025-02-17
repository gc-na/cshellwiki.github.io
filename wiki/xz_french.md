# [Linux] Bash xz : Compresser et décompresser des fichiers

## Overview
La commande `xz` est utilisée pour compresser et décompresser des fichiers en utilisant l'algorithme de compression LZMA. Elle est particulièrement efficace pour réduire la taille des fichiers tout en maintenant une bonne qualité de compression.

## Usage
La syntaxe de base de la commande `xz` est la suivante :

```bash
xz [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `xz` :

- `-d`, `--decompress` : Décompresse un fichier.
- `-k`, `--keep` : Garde le fichier original après compression.
- `-f`, `--force` : Force la compression ou la décompression, même si le fichier de destination existe déjà.
- `-z`, `--compress` : Compresse un fichier (c'est l'option par défaut).
- `-9` : Utilise le niveau de compression le plus élevé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `xz` :

1. **Compresser un fichier :**
   ```bash
   xz fichier.txt
   ```

2. **Décompresser un fichier :**
   ```bash
   xz -d fichier.txt.xz
   ```

3. **Compresser un fichier tout en gardant l'original :**
   ```bash
   xz -k fichier.txt
   ```

4. **Décompresser un fichier avec force :**
   ```bash
   xz -df fichier.txt.xz
   ```

5. **Compresser un fichier avec le niveau de compression maximum :**
   ```bash
   xz -9 fichier.txt
   ```

## Tips
- Pour compresser plusieurs fichiers à la fois, vous pouvez utiliser un joker, par exemple : `xz *.txt`.
- Vérifiez la taille des fichiers avant et après compression pour évaluer l'efficacité.
- Utilisez `man xz` pour accéder à la documentation complète et découvrir d'autres options disponibles.