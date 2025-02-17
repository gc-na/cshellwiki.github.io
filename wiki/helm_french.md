# [Linux] Bash helm utilisation : Gérer les applications Kubernetes

## Overview
La commande `helm` est un gestionnaire de paquets pour Kubernetes qui permet de déployer, gérer et configurer des applications sur un cluster Kubernetes. Elle facilite l'installation et la mise à jour des applications en utilisant des "charts", qui sont des ensembles de fichiers décrivant une application Kubernetes.

## Usage
La syntaxe de base de la commande `helm` est la suivante :

```bash
helm [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `helm` :

- `install` : Installe un nouveau chart.
- `upgrade` : Met à jour une release existante avec un nouveau chart.
- `uninstall` : Supprime une release.
- `list` : Affiche les releases installées.
- `repo` : Gère les dépôts de charts.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `helm` :

### Installer un chart
Pour installer un chart, utilisez la commande suivante :

```bash
helm install mon-application stable/mon-chart
```

### Mettre à jour une release
Pour mettre à jour une release existante, utilisez :

```bash
helm upgrade mon-application stable/mon-chart
```

### Lister les releases
Pour afficher toutes les releases installées, utilisez :

```bash
helm list
```

### Désinstaller une release
Pour supprimer une release, utilisez :

```bash
helm uninstall mon-application
```

## Tips
- Toujours vérifier la version du chart avant de l'installer ou de le mettre à jour pour éviter des incompatibilités.
- Utilisez des valeurs personnalisées avec l'option `-f` pour un déploiement plus adapté à vos besoins.
- Gardez vos dépôts de charts à jour avec la commande `helm repo update` pour accéder aux dernières versions des applications.