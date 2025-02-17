# [Linux] Bash systemctl utilisation : Gérer les services système

## Overview
La commande `systemctl` est un outil essentiel pour interagir avec le système d'initialisation `systemd`. Elle permet de démarrer, arrêter, redémarrer et gérer les services et les unités système sur les distributions Linux qui utilisent `systemd`.

## Usage
La syntaxe de base de la commande `systemctl` est la suivante :

```bash
systemctl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `systemctl` :

- `start` : Démarre un service.
- `stop` : Arrête un service.
- `restart` : Redémarre un service.
- `status` : Affiche l'état d'un service.
- `enable` : Active un service pour qu'il démarre au démarrage du système.
- `disable` : Désactive un service pour qu'il ne démarre pas au démarrage du système.
- `list-units` : Liste toutes les unités actives.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `systemctl` :

- Pour démarrer un service, par exemple `nginx` :

```bash
sudo systemctl start nginx
```

- Pour arrêter un service, par exemple `nginx` :

```bash
sudo systemctl stop nginx
```

- Pour redémarrer un service, par exemple `nginx` :

```bash
sudo systemctl restart nginx
```

- Pour vérifier l'état d'un service, par exemple `nginx` :

```bash
sudo systemctl status nginx
```

- Pour activer un service au démarrage :

```bash
sudo systemctl enable nginx
```

- Pour désactiver un service au démarrage :

```bash
sudo systemctl disable nginx
```

- Pour lister toutes les unités actives :

```bash
systemctl list-units
```

## Tips
- Utilisez `sudo` pour exécuter des commandes `systemctl` qui nécessitent des privilèges administratifs.
- Vérifiez régulièrement l'état de vos services pour vous assurer qu'ils fonctionnent comme prévu.
- N'oubliez pas de désactiver les services inutilisés pour améliorer la sécurité et les performances de votre système.