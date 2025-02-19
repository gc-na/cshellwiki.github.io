# [Linux] C Shell (csh) userdel : Supprimer un utilisateur du système

## Overview
La commande `userdel` est utilisée pour supprimer un compte utilisateur du système. Elle permet de retirer les informations de l'utilisateur et, selon les options choisies, de supprimer également son répertoire personnel et ses fichiers.

## Usage
La syntaxe de base de la commande `userdel` est la suivante :

```csh
userdel [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `userdel` :

- `-r` : Supprime le répertoire personnel de l'utilisateur ainsi que son contenu.
- `-f` : Force la suppression de l'utilisateur même s'il est connecté.
- `-Z` : Supprime les informations de sécurité associées à l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `userdel` :

1. Supprimer un utilisateur sans supprimer son répertoire personnel :
   ```csh
   userdel nom_utilisateur
   ```

2. Supprimer un utilisateur et son répertoire personnel :
   ```csh
   userdel -r nom_utilisateur
   ```

3. Forcer la suppression d'un utilisateur qui est actuellement connecté :
   ```csh
   userdel -f nom_utilisateur
   ```

4. Supprimer un utilisateur tout en supprimant les informations de sécurité :
   ```csh
   userdel -Z nom_utilisateur
   ```

## Tips
- Assurez-vous de sauvegarder les données importantes de l'utilisateur avant de le supprimer, surtout si vous utilisez l'option `-r`.
- Vérifiez si l'utilisateur est connecté avant de le supprimer pour éviter des interruptions de service.
- Utilisez la commande `who` pour voir les utilisateurs actuellement connectés au système.