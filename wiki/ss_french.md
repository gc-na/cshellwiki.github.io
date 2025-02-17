# [Linux] Bash ss Utilisation : Afficher les connexions réseau

## Overview
La commande `ss` est utilisée pour afficher des informations sur les connexions réseau, les sockets et les statistiques de réseau sur un système Linux. Elle est souvent considérée comme une alternative plus rapide et plus efficace à la commande `netstat`.

## Usage
La syntaxe de base de la commande `ss` est la suivante :

```bash
ss [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ss` :

- `-t` : Affiche uniquement les connexions TCP.
- `-u` : Affiche uniquement les connexions UDP.
- `-l` : Affiche uniquement les sockets à l'écoute.
- `-p` : Affiche les processus associés aux sockets.
- `-n` : Affiche les adresses et numéros de port sous forme numérique, sans résolution DNS.

## Common Examples

### Afficher toutes les connexions
Pour afficher toutes les connexions réseau actives, utilisez :

```bash
ss
```

### Afficher les connexions TCP
Pour afficher uniquement les connexions TCP, utilisez :

```bash
ss -t
```

### Afficher les sockets à l'écoute
Pour afficher les sockets qui sont à l'écoute, utilisez :

```bash
ss -l
```

### Afficher les connexions UDP
Pour afficher uniquement les connexions UDP, utilisez :

```bash
ss -u
```

### Afficher les processus associés
Pour voir les processus associés aux connexions, utilisez :

```bash
ss -p
```

### Afficher les connexions avec des adresses numériques
Pour afficher les connexions sans résolution DNS, utilisez :

```bash
ss -n
```

## Tips
- Utilisez `ss -t -l` pour voir les ports TCP à l'écoute, ce qui est utile pour le dépannage des services réseau.
- Combinez plusieurs options pour affiner vos résultats, par exemple `ss -tunlp` pour afficher les connexions TCP et UDP avec les processus associés.
- Pensez à exécuter `ss` avec des privilèges élevés (par exemple, en utilisant `sudo`) pour voir toutes les connexions, y compris celles des autres utilisateurs.