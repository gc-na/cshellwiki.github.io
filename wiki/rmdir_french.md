# [Linux] Bash rmdir : Supprimer des répertoires vides

## Overview
La commande `rmdir` est utilisée pour supprimer des répertoires vides dans un système de fichiers. Si le répertoire contient des fichiers ou d'autres répertoires, la commande échouera et ne supprimera rien.

## Usage
La syntaxe de base de la commande `rmdir` est la suivante :

```bash
rmdir [options] [arguments]
```

## Common Options
- `-p` : Supprime le répertoire spécifié ainsi que ses répertoires parents vides.
- `--ignore-fail-on-non-empty` : Ignore les erreurs si le répertoire n'est pas vide.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `rmdir` :

1. Supprimer un répertoire vide :
   ```bash
   rmdir mon_repertoire
   ```

2. Supprimer un répertoire et ses parents vides :
   ```bash
   rmdir -p mon_repertoire/parent/ancien_repertoire
   ```

3. Ignorer les erreurs si le répertoire n'est pas vide :
   ```bash
   rmdir --ignore-fail-on-non-empty mon_repertoire_non_vide
   ```

## Tips
- Assurez-vous que le répertoire est vide avant d'utiliser `rmdir`, sinon la commande échouera.
- Utilisez l'option `-p` pour nettoyer rapidement une hiérarchie de répertoires vides.
- Pour supprimer des répertoires non vides, envisagez d'utiliser la commande `rm -r` avec prudence, car cela supprimera également tous les fichiers et sous-répertoires.