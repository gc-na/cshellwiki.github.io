# [Linux] C Shell (csh) dnf : Gestionnaire de paquets pour les distributions basées sur RPM

## Overview
La commande `dnf` (Dandified YUM) est un gestionnaire de paquets utilisé pour installer, mettre à jour et supprimer des logiciels sur les distributions Linux basées sur RPM, comme Fedora et CentOS. Elle remplace l'ancienne commande `yum` et offre des fonctionnalités améliorées.

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

- Pour installer un paquet, par exemple `vim` :

```bash
dnf install vim
```

- Pour supprimer un paquet, par exemple `nano` :

```bash
dnf remove nano
```

- Pour mettre à jour tous les paquets installés :

```bash
dnf update
```

- Pour rechercher un paquet, par exemple `httpd` :

```bash
dnf search httpd
```

- Pour afficher des informations sur un paquet, par exemple `curl` :

```bash
dnf info curl
```

## Tips
- Toujours exécuter `dnf update` régulièrement pour s'assurer que tous les paquets sont à jour et sécurisés.
- Utilisez l'option `--assumeyes` pour automatiser les confirmations lors de l'installation ou de la mise à jour des paquets.
- Vérifiez les dépendances d'un paquet avant de l'installer pour éviter des problèmes de compatibilité.