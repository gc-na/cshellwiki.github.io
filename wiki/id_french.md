# [Linux] Bash id : Afficher les informations d'identification d'un utilisateur

## Overview
La commande `id` est utilisée pour afficher les informations d'identification d'un utilisateur, y compris son identifiant utilisateur (UID), son identifiant de groupe (GID) et les groupes auxquels il appartient. C'est un outil utile pour vérifier les permissions et les rôles d'un utilisateur dans le système.

## Usage
La syntaxe de base de la commande `id` est la suivante :

```bash
id [options] [arguments]
```

## Common Options
- `-u` : Affiche uniquement l'identifiant utilisateur (UID).
- `-g` : Affiche uniquement l'identifiant de groupe (GID).
- `-G` : Affiche tous les identifiants de groupe auxquels l'utilisateur appartient.
- `-n` : Affiche le nom au lieu de l'identifiant numérique.
- `-r` : Affiche l'identifiant de groupe réel au lieu de l'identifiant de groupe effectif.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `id` :

1. Afficher les informations d'identification de l'utilisateur actuel :
   ```bash
   id
   ```

2. Afficher uniquement l'identifiant utilisateur (UID) :
   ```bash
   id -u
   ```

3. Afficher uniquement l'identifiant de groupe (GID) :
   ```bash
   id -g
   ```

4. Afficher tous les groupes auxquels l'utilisateur appartient :
   ```bash
   id -G
   ```

5. Afficher le nom de l'utilisateur et de son groupe principal :
   ```bash
   id -n
   ```

## Tips
- Utilisez `id` sans options pour obtenir un aperçu complet de vos informations d'identification.
- Combinez les options pour obtenir des résultats spécifiques, par exemple, `id -u -n` pour obtenir le nom de l'utilisateur actuel.
- Vérifiez les permissions des fichiers en utilisant `id` pour comprendre les rôles des utilisateurs et des groupes dans le système.