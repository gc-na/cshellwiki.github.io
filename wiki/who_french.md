# [Linux] C Shell (csh) who <Utilisation>: Afficher les utilisateurs connectés

## Overview
La commande `who` dans C Shell (csh) est utilisée pour afficher une liste des utilisateurs actuellement connectés au système. Elle fournit des informations telles que le nom d'utilisateur, le terminal, la date et l'heure de connexion.

## Usage
La syntaxe de base de la commande `who` est la suivante :

```
who [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `who` :

- `-b` : Affiche la date et l'heure du dernier démarrage du système.
- `-q` : Affiche uniquement les noms d'utilisateur et le nombre total d'utilisateurs connectés.
- `-H` : Affiche les en-têtes de colonnes pour les informations affichées.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `who` :

1. Afficher tous les utilisateurs connectés :
   ```csh
   who
   ```

2. Afficher le dernier démarrage du système :
   ```csh
   who -b
   ```

3. Afficher uniquement les noms d'utilisateur et le nombre total d'utilisateurs :
   ```csh
   who -q
   ```

4. Afficher les utilisateurs avec des en-têtes de colonnes :
   ```csh
   who -H
   ```

## Tips
- Utilisez `who` sans options pour obtenir rapidement une vue d'ensemble des utilisateurs connectés.
- Combinez `who` avec d'autres commandes comme `grep` pour filtrer les résultats selon des critères spécifiques.
- Pensez à utiliser `who -H` si vous souhaitez une sortie plus lisible avec des en-têtes.