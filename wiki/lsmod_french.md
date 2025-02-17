# [Linux] Bash lsmod Utilisation : Afficher les modules du noyau chargés

## Overview
La commande `lsmod` est utilisée pour afficher les modules du noyau Linux qui sont actuellement chargés. Ces modules sont des morceaux de code qui peuvent être chargés et déchargés dans le noyau à la demande, permettant ainsi d'étendre les fonctionnalités du système d'exploitation sans avoir à le redémarrer.

## Usage
La syntaxe de base de la commande `lsmod` est la suivante :

```bash
lsmod [options] [arguments]
```

## Common Options
Bien que `lsmod` n'ait pas beaucoup d'options, voici quelques-unes des plus courantes :

- `-h`, `--help` : Affiche l'aide et les options disponibles pour la commande.
- `-v`, `--version` : Affiche la version de la commande `lsmod`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lsmod` :

1. **Afficher tous les modules chargés :**
   ```bash
   lsmod
   ```

2. **Afficher l'aide de la commande :**
   ```bash
   lsmod --help
   ```

3. **Afficher la version de la commande :**
   ```bash
   lsmod --version
   ```

## Tips
- Utilisez `lsmod` régulièrement pour vérifier quels modules sont chargés, surtout après l'installation de nouveaux matériels ou logiciels.
- Combinez `lsmod` avec d'autres commandes comme `modinfo` pour obtenir plus d'informations sur un module spécifique.
- Si vous souhaitez voir les dépendances des modules, vous pouvez utiliser la commande `modprobe -l` pour lister les modules disponibles.