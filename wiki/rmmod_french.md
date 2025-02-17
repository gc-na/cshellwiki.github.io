# [Linux] Bash rmmod : Supprimer un module du noyau

## Overview
La commande `rmmod` est utilisée pour supprimer des modules du noyau Linux. Les modules du noyau sont des morceaux de code qui peuvent être chargés et déchargés dans le noyau à la volée, permettant ainsi d'ajouter ou de retirer des fonctionnalités au système d'exploitation sans avoir besoin de redémarrer.

## Usage
La syntaxe de base de la commande `rmmod` est la suivante :

```bash
rmmod [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `rmmod` :

- `-f` : Force la suppression du module, même s'il est en cours d'utilisation.
- `--wait` : Attendre que le module soit complètement déchargé avant de continuer.
- `--verbose` : Affiche des informations détaillées sur le processus de suppression.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `rmmod` :

1. Pour supprimer un module nommé `example_module` :

   ```bash
   rmmod example_module
   ```

2. Pour forcer la suppression d'un module même s'il est utilisé :

   ```bash
   rmmod -f example_module
   ```

3. Pour supprimer un module et afficher des informations détaillées :

   ```bash
   rmmod --verbose example_module
   ```

4. Pour attendre que le module soit complètement déchargé avant de continuer :

   ```bash
   rmmod --wait example_module
   ```

## Tips
- Avant de supprimer un module, assurez-vous qu'il n'est pas utilisé par d'autres processus pour éviter des erreurs.
- Utilisez l'option `--verbose` pour obtenir des informations supplémentaires qui peuvent vous aider à diagnostiquer des problèmes.
- Vérifiez toujours la liste des modules chargés avec `lsmod` avant de tenter de les supprimer.