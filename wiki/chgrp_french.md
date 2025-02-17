# [Linux] Bash chgrp utilisation : Modifier le groupe d'un fichier ou d'un répertoire

## Overview
La commande `chgrp` permet de changer le groupe associé à un fichier ou à un répertoire. Cela est utile pour gérer les permissions d'accès et assurer que les utilisateurs d'un groupe spécifique peuvent accéder aux fichiers nécessaires.

## Usage
La syntaxe de base de la commande `chgrp` est la suivante :

```bash
chgrp [options] [arguments]
```

## Common Options
- `-R` : Applique le changement de groupe de manière récursive à tous les fichiers et sous-répertoires.
- `-v` : Affiche les fichiers dont le groupe a été modifié.
- `-c` : Affiche uniquement les fichiers dont le groupe a été changé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `chgrp` :

1. Changer le groupe d'un fichier :
   ```bash
   chgrp utilisateurs fichier.txt
   ```

2. Changer le groupe d'un répertoire :
   ```bash
   chgrp admin mon_repertoire
   ```

3. Changer le groupe de manière récursive :
   ```bash
   chgrp -R utilisateurs mon_repertoire
   ```

4. Afficher les fichiers dont le groupe a été modifié :
   ```bash
   chgrp -v utilisateurs fichier.txt
   ```

5. Changer le groupe et afficher uniquement les fichiers modifiés :
   ```bash
   chgrp -c utilisateurs fichier.txt
   ```

## Tips
- Assurez-vous d'avoir les permissions nécessaires pour changer le groupe d'un fichier ou d'un répertoire.
- Utilisez l'option `-R` avec précaution, car elle affecte tous les fichiers et sous-répertoires.
- Vérifiez les groupes disponibles sur votre système avec la commande `getent group` avant de modifier les groupes.