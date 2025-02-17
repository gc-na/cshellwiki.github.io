# [Linux] Bash udevadm Utilisation : Gestion des périphériques sous Linux

## Overview
La commande `udevadm` est un outil utilisé pour interagir avec le système de gestion des périphériques `udev` sous Linux. Elle permet de gérer les événements liés aux périphériques, de surveiller les changements d'état des périphériques et de configurer les règles associées.

## Usage
La syntaxe de base de la commande `udevadm` est la suivante :

```bash
udevadm [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `udevadm` :

- `info` : Affiche des informations sur un périphérique spécifique.
- `monitor` : Surveille les événements `udev` en temps réel.
- `trigger` : Déclenche les événements `udev` pour les périphériques existants.
- `settle` : Attend que tous les événements `udev` en attente soient traités.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `udevadm` :

### Afficher des informations sur un périphérique
Pour obtenir des informations détaillées sur un périphérique, utilisez la commande suivante :

```bash
udevadm info --query=all --name=/dev/sda
```

### Surveiller les événements udev
Pour surveiller les événements en temps réel, exécutez :

```bash
udevadm monitor
```

### Déclencher des événements pour les périphériques existants
Pour déclencher les événements `udev` pour tous les périphériques, utilisez :

```bash
udevadm trigger
```

### Attendre que tous les événements soient traités
Pour s'assurer que tous les événements en attente sont traités, exécutez :

```bash
udevadm settle
```

## Tips
- Utilisez `udevadm monitor` pour diagnostiquer les problèmes de détection de périphériques en temps réel.
- Combinez `udevadm info` avec des scripts pour automatiser la gestion des périphériques.
- Soyez prudent lors de l'utilisation de `udevadm trigger`, car cela peut affecter le fonctionnement des périphériques en cours d'utilisation.