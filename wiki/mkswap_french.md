# [Linux] Bash mkswap : Créer un espace d'échange

## Overview
La commande `mkswap` est utilisée pour initialiser un fichier ou une partition pour être utilisé comme espace d'échange (swap) sur un système Linux. L'espace d'échange est essentiel pour la gestion de la mémoire, permettant au système d'utiliser de l'espace disque comme mémoire virtuelle lorsque la RAM est insuffisante.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
mkswap [options] [arguments]
```

## Common Options
- `-L, --label LABEL` : Définit une étiquette pour l'espace d'échange.
- `-f, --force` : Force l'initialisation même si le fichier ou la partition semble déjà être un espace d'échange.
- `-p, --pagesize SIZE` : Spécifie la taille des pages pour l'espace d'échange.

## Common Examples

### Initialiser un fichier d'échange
Pour créer un fichier d'échange de 1 Go et l'initialiser, vous pouvez utiliser les commandes suivantes :

```bash
sudo fallocate -l 1G /swapfile
sudo mkswap /swapfile
```

### Initialiser une partition d'échange
Pour initialiser une partition (par exemple, `/dev/sdX1`) comme espace d'échange :

```bash
sudo mkswap /dev/sdX1
```

### Ajouter une étiquette à l'espace d'échange
Pour créer un espace d'échange avec une étiquette :

```bash
sudo mkswap -L mon_swap /dev/sdX1
```

## Tips
- Assurez-vous que le fichier ou la partition que vous initialisez n'est pas monté avant d'exécuter `mkswap`.
- Utilisez `swapon` après `mkswap` pour activer l'espace d'échange que vous venez de créer.
- Vérifiez l'utilisation de l'espace d'échange avec la commande `swapon --show` pour vous assurer qu'il est actif.