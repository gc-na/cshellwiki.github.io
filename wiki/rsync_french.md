# [Linux] Bash rsync utilisation : Synchroniser des fichiers et des répertoires

## Overview
La commande `rsync` est un outil puissant utilisé pour synchroniser des fichiers et des répertoires entre différents emplacements, que ce soit sur la même machine ou entre des machines distantes. Elle est particulièrement appréciée pour sa capacité à ne transférer que les fichiers modifiés, ce qui la rend efficace en termes de bande passante et de temps.

## Usage
La syntaxe de base de la commande `rsync` est la suivante :

```bash
rsync [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `rsync` :

- `-a` : Archive, qui préserve les permissions, les timestamps, et les liens symboliques.
- `-v` : Verbose, pour afficher des informations détaillées sur le processus de synchronisation.
- `-z` : Compression, pour compresser les fichiers pendant le transfert.
- `-r` : Récursif, pour copier des répertoires de manière récursive.
- `--delete` : Supprime les fichiers dans le répertoire de destination qui ne sont pas présents dans le répertoire source.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `rsync` :

1. **Synchroniser un répertoire local avec un autre répertoire local :**

   ```bash
   rsync -av /chemin/vers/source/ /chemin/vers/destination/
   ```

2. **Synchroniser un répertoire local avec un répertoire distant :**

   ```bash
   rsync -av /chemin/vers/source/ utilisateur@serveur:/chemin/vers/destination/
   ```

3. **Synchroniser un répertoire distant avec un répertoire local :**

   ```bash
   rsync -av utilisateur@serveur:/chemin/vers/source/ /chemin/vers/destination/
   ```

4. **Synchroniser en compressant les fichiers :**

   ```bash
   rsync -avz /chemin/vers/source/ utilisateur@serveur:/chemin/vers/destination/
   ```

5. **Synchroniser en supprimant les fichiers obsolètes dans le répertoire de destination :**

   ```bash
   rsync -av --delete /chemin/vers/source/ /chemin/vers/destination/
   ```

## Tips
- Toujours utiliser l'option `-n` (dry run) pour simuler la commande avant de l'exécuter réellement. Cela permet de voir ce qui sera transféré sans effectuer de modifications.
- Pensez à utiliser des chemins relatifs pour éviter des erreurs de destination.
- Pour des transferts fréquents, envisagez d'utiliser un script pour automatiser le processus avec `cron`.