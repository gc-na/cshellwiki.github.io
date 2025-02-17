# [Linux] Bash userdel : Supprimer un utilisateur du système

## Overview
La commande `userdel` est utilisée pour supprimer un compte utilisateur du système Linux. Elle permet de retirer les informations de l'utilisateur et, selon les options choisies, de supprimer également son répertoire personnel et ses fichiers.

## Usage
La syntaxe de base de la commande `userdel` est la suivante :

```bash
userdel [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `userdel` :

- `-r` : Supprime le répertoire personnel de l'utilisateur ainsi que son mail spool.
- `-f` : Force la suppression de l'utilisateur même s'il est connecté.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `userdel` :

1. Supprimer un utilisateur sans supprimer son répertoire personnel :

   ```bash
   userdel nom_utilisateur
   ```

2. Supprimer un utilisateur et son répertoire personnel :

   ```bash
   userdel -r nom_utilisateur
   ```

3. Forcer la suppression d'un utilisateur qui est actuellement connecté :

   ```bash
   userdel -f nom_utilisateur
   ```

## Tips
- Assurez-vous de sauvegarder les données importantes de l'utilisateur avant de le supprimer, surtout si vous utilisez l'option `-r`.
- Vérifiez les connexions actives des utilisateurs avec la commande `who` avant de forcer la suppression.
- Utilisez la commande `id nom_utilisateur` pour vérifier si l'utilisateur existe avant d'essayer de le supprimer.