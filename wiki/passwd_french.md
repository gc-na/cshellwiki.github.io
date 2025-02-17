# [Linux] Bash passwd : Changer de mot de passe

## Overview
La commande `passwd` est utilisée pour changer le mot de passe d'un utilisateur dans un système Linux. Elle permet à un utilisateur de modifier son propre mot de passe ou à un administrateur de changer le mot de passe d'un autre utilisateur.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
passwd [options] [arguments]
```

## Common Options
- `-d` : Supprime le mot de passe de l'utilisateur, rendant son compte sans mot de passe.
- `-e` : Force l'utilisateur à changer son mot de passe lors de la prochaine connexion.
- `-l` : Verrouille le compte de l'utilisateur, empêchant ainsi toute connexion.
- `-u` : Déverrouille le compte de l'utilisateur.
- `-S` : Affiche l'état du mot de passe de l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `passwd` :

1. **Changer son propre mot de passe :**
   ```bash
   passwd
   ```

2. **Changer le mot de passe d'un autre utilisateur (nécessite des privilèges d'administrateur) :**
   ```bash
   sudo passwd nom_utilisateur
   ```

3. **Forcer un utilisateur à changer son mot de passe lors de la prochaine connexion :**
   ```bash
   sudo passwd -e nom_utilisateur
   ```

4. **Supprimer le mot de passe d'un utilisateur :**
   ```bash
   sudo passwd -d nom_utilisateur
   ```

5. **Vérifier l'état du mot de passe d'un utilisateur :**
   ```bash
   passwd -S nom_utilisateur
   ```

## Tips
- Assurez-vous de choisir un mot de passe fort pour sécuriser votre compte.
- Utilisez l'option `-e` régulièrement pour forcer les utilisateurs à mettre à jour leurs mots de passe.
- En tant qu'administrateur, soyez prudent lorsque vous modifiez les mots de passe des autres utilisateurs pour éviter tout accès non autorisé.