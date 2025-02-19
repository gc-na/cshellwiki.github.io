# [Linux] C Shell (csh) udevadm Utilisation : Gérer les périphériques du système

## Overview
La commande `udevadm` est un outil utilisé pour interagir avec le gestionnaire de périphériques `udev` dans les systèmes Linux. Elle permet de gérer les événements liés aux périphériques, de surveiller les changements de matériel et de manipuler les règles de `udev`.

## Usage
La syntaxe de base de la commande `udevadm` est la suivante :

```shell
udevadm [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `udevadm` :

- `info` : Affiche des informations sur un périphérique spécifique.
- `trigger` : Déclenche des événements pour les périphériques.
- `settle` : Attend que tous les événements de périphériques soient traités.
- `control` : Gère le fonctionnement du démon `udevd`.
- `monitor` : Surveille les événements `udev` en temps réel.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `udevadm` :

### Afficher des informations sur un périphérique
Pour obtenir des informations sur un périphérique spécifique, utilisez :

```shell
udevadm info --query=all --name=/dev/sda
```

### Déclencher des événements pour tous les périphériques
Pour déclencher des événements pour tous les périphériques, exécutez :

```shell
udevadm trigger
```

### Attendre que tous les événements soient traités
Pour attendre que tous les événements de périphériques soient réglés, utilisez :

```shell
udevadm settle
```

### Surveiller les événements en temps réel
Pour surveiller les événements `udev` en temps réel, vous pouvez utiliser :

```shell
udevadm monitor
```

## Tips
- Utilisez `udevadm info` pour diagnostiquer les problèmes de périphériques en affichant des informations détaillées.
- Lors de la création ou de la modification de règles `udev`, n'oubliez pas de déclencher les événements avec `udevadm trigger` pour appliquer les changements.
- Pour une surveillance continue des événements, exécutez `udevadm monitor` dans un terminal séparé pendant que vous effectuez des modifications matérielles.