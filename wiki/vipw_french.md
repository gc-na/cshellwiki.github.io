# [Linux] C Shell (csh) vipw : Édition sécurisée des fichiers de mots de passe

## Overview
La commande `vipw` permet d'éditer le fichier des mots de passe (`/etc/passwd`) de manière sécurisée. Elle verrouille le fichier pour éviter les modifications simultanées, ce qui prévient les corruptions de données.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
vipw [options]
```

## Common Options
- `-s` : Utilise un éditeur de texte sécurisé pour l'édition.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `vipw` :

### Édition du fichier de mots de passe
```csh
vipw
```
Cette commande ouvre le fichier `/etc/passwd` dans l'éditeur de texte par défaut.

### Utilisation d'un éditeur spécifique
```csh
vipw -s
```
Cette commande ouvre le fichier de manière sécurisée, en utilisant un éditeur spécifié par la variable d'environnement `EDITOR`.

## Tips
- Toujours utiliser `vipw` pour modifier le fichier des mots de passe afin d'éviter les conflits.
- Vérifiez les permissions du fichier `/etc/passwd` avant de l'éditer pour garantir que vous avez les droits nécessaires.
- Faites une sauvegarde du fichier avant de procéder à des modifications importantes.