# [Linux] C Shell (csh) systemctl : Gérer les services système

## Overview
La commande `systemctl` est utilisée pour examiner et contrôler le système d'initialisation systemd et les services qui y sont associés. Elle permet de démarrer, arrêter, redémarrer et vérifier l'état des services sur un système Linux.

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

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `systemctl` :

- Pour démarrer un service, par exemple `nginx` :

```bash
systemctl start nginx
```

- Pour arrêter un service, par exemple `nginx` :

```bash
systemctl stop nginx
```

- Pour redémarrer un service, par exemple `nginx` :

```bash
systemctl restart nginx
```

- Pour vérifier l'état d'un service, par exemple `nginx` :

```bash
systemctl status nginx
```

- Pour activer un service au démarrage :

```bash
systemctl enable nginx
```

- Pour désactiver un service au démarrage :

```bash
systemctl disable nginx
```

## Tips
- Toujours vérifier l'état d'un service après l'avoir démarré ou arrêté pour s'assurer qu'il fonctionne comme prévu.
- Utilisez `systemctl list-units --type=service` pour voir tous les services actifs et leur état.
- Soyez prudent lors de l'activation ou de la désactivation des services, car cela peut affecter le fonctionnement de votre système.