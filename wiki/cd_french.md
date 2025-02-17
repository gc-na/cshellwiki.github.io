# [Linux] Bash cd utilisation : Changer de répertoire

## Overview
La commande `cd` (change directory) est utilisée dans Bash pour naviguer entre les répertoires du système de fichiers. Elle permet de se déplacer d'un répertoire à un autre, facilitant ainsi l'accès aux fichiers et aux dossiers.

## Usage
La syntaxe de base de la commande `cd` est la suivante :

```bash
cd [options] [arguments]
```

## Common Options
- `..` : Permet de remonter d'un niveau dans l'arborescence des répertoires.
- `-` : Permet de revenir au dernier répertoire visité.
- `~` : Représente le répertoire personnel de l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cd` :

1. Changer pour un répertoire spécifique :
   ```bash
   cd /chemin/vers/le/répertoire
   ```

2. Remonter d'un niveau dans l'arborescence :
   ```bash
   cd ..
   ```

3. Revenir au dernier répertoire visité :
   ```bash
   cd -
   ```

4. Accéder au répertoire personnel de l'utilisateur :
   ```bash
   cd ~
   ```

5. Accéder à un sous-répertoire :
   ```bash
   cd mon_dossier
   ```

## Tips
- Utilisez `cd -` pour naviguer rapidement entre deux répertoires.
- Tapez `cd` sans arguments pour retourner directement à votre répertoire personnel.
- Pour éviter les erreurs de chemin, utilisez la touche de tabulation pour l'auto-complétion des noms de répertoires.