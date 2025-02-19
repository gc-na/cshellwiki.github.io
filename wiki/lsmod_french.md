# [Linux] C Shell (csh) lsmod : Afficher les modules du noyau chargés

## Overview
La commande `lsmod` est utilisée pour afficher les modules du noyau Linux qui sont actuellement chargés dans le système. Elle fournit une liste des modules, ainsi que des informations sur les dépendances entre eux.

## Usage
La syntaxe de base de la commande `lsmod` est la suivante :

```csh
lsmod [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `lsmod` :

- `-h`, `--help` : Affiche l'aide et les options disponibles pour la commande.
- `-v`, `--verbose` : Affiche des informations détaillées sur les modules chargés.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lsmod` :

1. **Afficher tous les modules chargés :**

   ```csh
   lsmod
   ```

2. **Afficher l'aide de la commande :**

   ```csh
   lsmod --help
   ```

3. **Afficher les modules avec des informations détaillées :**

   ```csh
   lsmod --verbose
   ```

## Tips
- Utilisez `lsmod` régulièrement pour surveiller les modules chargés et détecter d'éventuels problèmes de compatibilité.
- Combinez `lsmod` avec d'autres commandes comme `modinfo` pour obtenir des informations supplémentaires sur un module spécifique.
- Pensez à vérifier les dépendances entre les modules pour mieux comprendre leur fonctionnement dans le noyau.