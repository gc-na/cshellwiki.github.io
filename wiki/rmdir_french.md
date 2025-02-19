# [Linux] C Shell (csh) rmdir Utilisation : Supprimer des répertoires vides

## Overview
La commande `rmdir` est utilisée pour supprimer des répertoires vides dans le système de fichiers. Si le répertoire contient des fichiers ou d'autres répertoires, la commande échouera et ne supprimera pas le répertoire.

## Usage
La syntaxe de base de la commande `rmdir` est la suivante :

```csh
rmdir [options] [arguments]
```

## Common Options
- `-p` : Supprime le répertoire spécifié ainsi que ses parents vides.
- `--help` : Affiche l'aide et les options disponibles pour la commande.
- `--version` : Affiche la version de la commande `rmdir`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `rmdir` :

1. Supprimer un répertoire vide :
   ```csh
   rmdir mon_repertoire
   ```

2. Supprimer plusieurs répertoires vides à la fois :
   ```csh
   rmdir repertoire1 repertoire2
   ```

3. Supprimer un répertoire et ses parents vides :
   ```csh
   rmdir -p parent/enfant
   ```

4. Afficher l'aide pour la commande :
   ```csh
   rmdir --help
   ```

## Tips
- Assurez-vous que le répertoire est vide avant d'utiliser `rmdir`, sinon la commande échouera.
- Utilisez l'option `-p` pour nettoyer les répertoires parents vides en une seule commande.
- Vérifiez toujours les chemins des répertoires que vous souhaitez supprimer pour éviter des erreurs.