# [Linux] C Shell (csh) lvm Utilisation : Gestion des volumes logiques

## Overview
La commande `lvm` (Logical Volume Manager) permet de gérer des volumes logiques sur un système Linux. Elle offre des fonctionnalités pour créer, supprimer, redimensionner et gérer des volumes logiques, facilitant ainsi la gestion de l'espace de stockage.

## Usage
Voici la syntaxe de base de la commande `lvm` :

```bash
lvm [options] [arguments]
```

## Common Options
- `create`: Crée un nouveau volume logique.
- `remove`: Supprime un volume logique existant.
- `extend`: Augmente la taille d'un volume logique.
- `reduce`: Réduit la taille d'un volume logique.
- `lvdisplay`: Affiche les informations sur les volumes logiques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lvm` :

### Créer un volume logique
```bash
lvm create -n mon_volume -L 10G mon_groupe
```

### Supprimer un volume logique
```bash
lvm remove mon_volume
```

### Étendre un volume logique
```bash
lvm extend -L +5G mon_volume
```

### Réduire un volume logique
```bash
lvm reduce -L -3G mon_volume
```

### Afficher les volumes logiques
```bash
lvm lvdisplay
```

## Tips
- Toujours sauvegarder vos données avant de modifier des volumes logiques.
- Utilisez `lvdisplay` pour vérifier l'état des volumes avant et après les modifications.
- Soyez prudent lors de l'utilisation des options `remove` et `reduce`, car elles peuvent entraîner une perte de données si elles sont mal utilisées.