# [Linux] C Shell (csh) groups : afficher les groupes d'utilisateurs

## Overview
La commande `groups` dans C Shell (csh) est utilisée pour afficher les groupes auxquels un utilisateur appartient. Cela permet de vérifier rapidement les permissions et les affiliations de groupe d'un utilisateur.

## Usage
La syntaxe de base de la commande `groups` est la suivante :

```csh
groups [options] [arguments]
```

## Common Options
- `-a` : Affiche tous les groupes, y compris les groupes secondaires.
- `-g` : Affiche uniquement les groupes principaux.
- `username` : Spécifie le nom d'utilisateur pour lequel afficher les groupes. Si aucun nom d'utilisateur n'est fourni, cela affiche les groupes de l'utilisateur courant.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `groups` :

1. Afficher les groupes de l'utilisateur courant :
   ```csh
   groups
   ```

2. Afficher les groupes d'un utilisateur spécifique (par exemple, `alice`) :
   ```csh
   groups alice
   ```

3. Afficher tous les groupes, y compris les groupes secondaires, pour l'utilisateur courant :
   ```csh
   groups -a
   ```

4. Afficher uniquement le groupe principal de l'utilisateur `bob` :
   ```csh
   groups -g bob
   ```

## Tips
- Utilisez la commande `groups` sans arguments pour rapidement vérifier vos propres groupes.
- Si vous êtes un administrateur système, vous pouvez utiliser cette commande pour vérifier les affiliations de groupe des utilisateurs lors de la gestion des permissions.
- Pensez à combiner `groups` avec d'autres commandes comme `id` pour obtenir des informations plus détaillées sur les utilisateurs et leurs groupes.