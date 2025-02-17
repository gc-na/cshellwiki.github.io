# [Linux] Utilisateurs Bash : Gérer les utilisateurs du système

## Overview
La commande `users` affiche les noms des utilisateurs actuellement connectés au système. C'est un outil simple mais utile pour obtenir rapidement des informations sur les sessions utilisateur actives.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
users [options] [arguments]
```

## Common Options
- `-a` : Affiche tous les utilisateurs connectés, y compris ceux qui sont connectés via des sessions non interactives.
- `-H` : Affiche les noms d'utilisateur sous forme de liste avec des en-têtes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `users` :

1. **Afficher les utilisateurs connectés :**
   ```bash
   users
   ```

2. **Afficher tous les utilisateurs connectés, y compris ceux en session non interactive :**
   ```bash
   users -a
   ```

3. **Afficher les utilisateurs avec des en-têtes :**
   ```bash
   users -H
   ```

## Tips
- Utilisez la commande `who` pour obtenir des informations plus détaillées sur les utilisateurs connectés, y compris leur terminal et l'heure de connexion.
- Pour surveiller l'activité des utilisateurs en temps réel, combinez `users` avec d'autres commandes comme `watch` :
  ```bash
  watch users
  ```
- Pensez à exécuter `users` dans un script pour automatiser la surveillance des connexions utilisateur.