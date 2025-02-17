# [Linux] Bash who usage : Affiche les utilisateurs connectés

## Overview
La commande `who` est utilisée pour afficher une liste des utilisateurs actuellement connectés au système. Elle fournit des informations telles que le nom d'utilisateur, le terminal utilisé, la date et l'heure de connexion, ainsi que d'autres détails pertinents.

## Usage
La syntaxe de base de la commande `who` est la suivante :

```bash
who [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `who` :

- `-a` : Affiche toutes les informations disponibles, y compris les utilisateurs connectés et les utilisateurs qui ont quitté.
- `-b` : Montre la dernière fois que le système a été redémarré.
- `-q` : Affiche uniquement les noms d'utilisateur et le nombre total d'utilisateurs connectés.
- `--help` : Affiche l'aide et les options disponibles pour la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `who` :

1. Afficher tous les utilisateurs connectés :
   ```bash
   who
   ```

2. Afficher toutes les informations, y compris les utilisateurs déconnectés :
   ```bash
   who -a
   ```

3. Afficher la dernière fois que le système a été redémarré :
   ```bash
   who -b
   ```

4. Afficher uniquement les noms d'utilisateur et le nombre total d'utilisateurs connectés :
   ```bash
   who -q
   ```

## Tips
- Utilisez `who -b` pour vérifier rapidement l'état de votre système et savoir quand il a été redémarré pour la dernière fois.
- Combinez `who` avec d'autres commandes comme `grep` pour filtrer les résultats. Par exemple, pour trouver un utilisateur spécifique :
  ```bash
  who | grep nom_utilisateur
  ```
- Pensez à utiliser `man who` pour consulter la page de manuel et découvrir d'autres options disponibles.