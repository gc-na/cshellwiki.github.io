# [Linux] C Shell (csh) socat : [outil de transfert de données]

## Overview
Le commandement `socat` (SOcket CAT) est un outil polyvalent qui permet de créer des connexions entre des flux de données. Il peut relier des sockets, des fichiers, des tubes, et bien d'autres types de flux, facilitant ainsi le transfert de données entre différentes sources.

## Usage
La syntaxe de base de la commande `socat` est la suivante :

```bash
socat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `socat` :

- `-d` : Affiche des messages de débogage.
- `-v` : Affiche les données transférées.
- `TCP:<host>:<port>` : Se connecte à un hôte et un port spécifiés via TCP.
- `UDP:<host>:<port>` : Se connecte à un hôte et un port spécifiés via UDP.
- `FILE:<filename>` : Utilise un fichier comme source ou destination de données.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `socat` :

1. **Transférer des données entre deux ports TCP :**

```bash
socat TCP-LISTEN:1234,reuseaddr TCP:localhost:5678
```

2. **Écouter sur un port et écrire dans un fichier :**

```bash
socat TCP-LISTEN:1234,reuseaddr FILE:output.txt
```

3. **Transférer des données d'un fichier à un port TCP :**

```bash
socat FILE:input.txt TCP:localhost:1234
```

4. **Créer un tunnel UDP :**

```bash
socat UDP-LISTEN:1234,reuseaddr UDP:localhost:5678
```

## Tips
- Utilisez l'option `-d -v` pour le débogage lors de la configuration de nouveaux flux, cela vous aidera à identifier les problèmes.
- Pensez à utiliser `reuseaddr` pour éviter les erreurs de liaison lorsque vous redémarrez le service.
- Vérifiez toujours les permissions des fichiers lorsque vous utilisez `socat` avec des fichiers pour éviter des erreurs d'accès.