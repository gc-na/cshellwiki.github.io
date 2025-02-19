# [Linux] C Shell (csh) utilisateurs : Afficher les utilisateurs connectés

## Overview
La commande `users` dans C Shell (csh) permet d'afficher les noms des utilisateurs actuellement connectés au système. C'est un outil simple mais utile pour obtenir rapidement une vue d'ensemble des sessions utilisateur actives.

## Usage
La syntaxe de base de la commande `users` est la suivante :

```
users [options] [arguments]
```

## Common Options
- `-n` : Affiche le nombre d'utilisateurs connectés au lieu de leurs noms.
- `-r` : Affiche uniquement les utilisateurs qui ont une session active.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `users` :

1. **Afficher les utilisateurs connectés :**
   ```csh
   users
   ```

2. **Afficher le nombre d'utilisateurs connectés :**
   ```csh
   users -n
   ```

3. **Afficher uniquement les utilisateurs avec une session active :**
   ```csh
   users -r
   ```

## Tips
- Utilisez `who` ou `w` pour obtenir des informations plus détaillées sur les utilisateurs connectés, comme leur adresse IP ou le temps de connexion.
- Combinez `users` avec d'autres commandes pour créer des scripts qui surveillent l'activité des utilisateurs sur le système.