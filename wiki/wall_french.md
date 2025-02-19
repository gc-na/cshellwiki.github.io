# [Linux] C Shell (csh) wall : envoyer des messages à tous les utilisateurs connectés

## Overview
La commande `wall` (write all) permet d'envoyer un message à tous les utilisateurs actuellement connectés à un système. Cela peut être utile pour informer les utilisateurs de la maintenance prévue, des mises à jour ou d'autres annonces importantes.

## Usage
La syntaxe de base de la commande `wall` est la suivante :

```csh
wall [options] [arguments]
```

## Common Options
- `-n` : Ne pas afficher le nom de l'utilisateur qui envoie le message.
- `-s` : Envoyer le message en mode silencieux, sans afficher d'avertissement.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `wall` :

1. **Envoyer un message simple à tous les utilisateurs :**
   ```csh
   wall "Le système sera hors ligne pour maintenance à 22h00."
   ```

2. **Envoyer un message sans afficher le nom de l'utilisateur :**
   ```csh
   wall -n "Attention : le serveur sera redémarré dans 5 minutes."
   ```

3. **Utiliser un fichier pour envoyer un message :**
   ```csh
   wall < message.txt
   ```

4. **Envoyer un message silencieux :**
   ```csh
   wall -s "Mise à jour du système en cours."
   ```

## Tips
- Utilisez `wall` avec précaution, car les messages peuvent interrompre le travail des utilisateurs.
- Pour des messages importants, envisagez de les envoyer à l'avance pour donner aux utilisateurs le temps de se préparer.
- Vous pouvez rediriger le contenu d'un fichier vers `wall` pour envoyer des messages plus longs sans avoir à les taper manuellement.