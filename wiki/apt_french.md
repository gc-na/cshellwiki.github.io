# [Linux] Bash apt utilisation : Gestion des paquets

## Overview
La commande `apt` est un outil de gestion de paquets pour les systèmes basés sur Debian, comme Ubuntu. Elle permet d'installer, de mettre à jour et de supprimer des logiciels facilement à partir de la ligne de commande.

## Usage
La syntaxe de base de la commande `apt` est la suivante :

```bash
apt [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `apt` :

- `install` : Installe un ou plusieurs paquets.
- `remove` : Supprime un ou plusieurs paquets.
- `update` : Met à jour la liste des paquets disponibles.
- `upgrade` : Met à jour tous les paquets installés vers leur dernière version.
- `search` : Recherche un paquet dans les dépôts.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `apt` :

1. **Mettre à jour la liste des paquets :**
   ```bash
   sudo apt update
   ```

2. **Installer un paquet (par exemple, `curl`) :**
   ```bash
   sudo apt install curl
   ```

3. **Supprimer un paquet (par exemple, `curl`) :**
   ```bash
   sudo apt remove curl
   ```

4. **Mettre à jour tous les paquets installés :**
   ```bash
   sudo apt upgrade
   ```

5. **Rechercher un paquet (par exemple, `git`) :**
   ```bash
   apt search git
   ```

## Tips
- Utilisez `sudo` pour exécuter des commandes `apt` qui nécessitent des privilèges d'administrateur.
- Pensez à exécuter `apt update` avant d'installer ou de mettre à jour des paquets pour vous assurer que vous disposez des dernières informations sur les paquets disponibles.
- Pour une mise à jour complète du système, utilisez `sudo apt update && sudo apt upgrade` en une seule ligne.