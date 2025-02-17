# [Linux] Bash dnf : Gestionnaire de paquets pour Fedora et dérivés

## Overview
La commande `dnf` (Dandified YUM) est un gestionnaire de paquets utilisé principalement sur les distributions basées sur Fedora. Elle permet d'installer, de mettre à jour et de supprimer des logiciels, tout en gérant les dépendances nécessaires.

## Usage
La syntaxe de base de la commande `dnf` est la suivante :

```bash
dnf [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `dnf` :

- `install` : Installe un ou plusieurs paquets.
- `remove` : Supprime un ou plusieurs paquets.
- `update` : Met à jour tous les paquets installés vers la dernière version disponible.
- `search` : Recherche un paquet dans les dépôts.
- `info` : Affiche des informations détaillées sur un paquet.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `dnf` :

1. **Installer un paquet :**
   ```bash
   dnf install nom_du_paquet
   ```

2. **Supprimer un paquet :**
   ```bash
   dnf remove nom_du_paquet
   ```

3. **Mettre à jour tous les paquets :**
   ```bash
   dnf update
   ```

4. **Rechercher un paquet :**
   ```bash
   dnf search nom_du_paquet
   ```

5. **Afficher des informations sur un paquet :**
   ```bash
   dnf info nom_du_paquet
   ```

## Tips
- Toujours vérifier les mises à jour régulièrement pour garder votre système sécurisé et à jour.
- Utilisez `dnf clean all` pour libérer de l'espace en supprimant les fichiers de cache inutiles.
- Pour éviter des conflits de dépendances, utilisez l'option `--best` lors de l'installation ou de la mise à jour des paquets.