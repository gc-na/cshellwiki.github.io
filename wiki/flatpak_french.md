# [Linux] Bash flatpak utilisation : Gestion des applications conteneurisées

## Overview
La commande `flatpak` est utilisée pour gérer des applications conteneurisées sur les systèmes Linux. Elle permet d'installer, de mettre à jour et de supprimer des applications, tout en garantissant qu'elles fonctionnent de manière isolée du reste du système.

## Usage
La syntaxe de base de la commande `flatpak` est la suivante :

```bash
flatpak [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `flatpak` :

- `install` : Installe une application à partir d'un dépôt.
- `uninstall` : Supprime une application installée.
- `update` : Met à jour les applications installées à leur dernière version.
- `list` : Affiche une liste des applications installées.
- `info` : Montre des informations détaillées sur une application spécifique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `flatpak` :

1. **Installer une application** :
   ```bash
   flatpak install flathub org.videolan.VLC
   ```

2. **Désinstaller une application** :
   ```bash
   flatpak uninstall org.videolan.VLC
   ```

3. **Mettre à jour toutes les applications installées** :
   ```bash
   flatpak update
   ```

4. **Lister les applications installées** :
   ```bash
   flatpak list
   ```

5. **Afficher des informations sur une application** :
   ```bash
   flatpak info org.videolan.VLC
   ```

## Tips
- Assurez-vous d'ajouter le dépôt `flathub` pour accéder à un large éventail d'applications :
  ```bash
  flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
  ```

- Utilisez `flatpak update` régulièrement pour garder vos applications à jour et sécurisées.

- Pour une meilleure gestion des applications, envisagez d'utiliser des outils graphiques comme GNOME Software ou Discover qui prennent en charge Flatpak.