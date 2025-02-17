# [Linux] Bash socat : Outil de redirection de flux

## Overview
Le commandement `socat` (SOcket CAT) est un outil puissant pour la redirection de flux de données entre deux points, que ce soit des fichiers, des sockets réseau, ou des terminaux. Il permet de créer des connexions entre différents types de flux, facilitant ainsi la communication entre applications.

## Usage
La syntaxe de base de la commande `socat` est la suivante :

```bash
socat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `socat` :

- `-u` : Utiliser le mode non-bloquant.
- `-v` : Activer le mode verbeux pour afficher des informations supplémentaires sur l'exécution.
- `TCP:` : Spécifie une connexion TCP, par exemple, `TCP:hostname:port`.
- `UDP:` : Spécifie une connexion UDP, par exemple, `UDP:hostname:port`.
- `FILE:` : Utilise un fichier comme source ou destination.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `socat` :

1. **Rediriger un port TCP vers un autre port TCP :**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:localhost:5678
   ```

2. **Créer un serveur UDP :**
   ```bash
   socat UDP-LISTEN:1234,fork -
   ```

3. **Transférer des données entre un fichier et un socket :**
   ```bash
   socat FILE:/path/to/file,rdonly TCP:localhost:1234
   ```

4. **Établir une connexion SSH via un tunnel :**
   ```bash
   socat TCP-LISTEN:2222,fork EXEC:"ssh user@remote_host"
   ```

## Tips
- Utilisez l'option `-v` pour déboguer et voir les données qui transitent.
- Pensez à utiliser `fork` pour permettre plusieurs connexions simultanées.
- Soyez prudent avec les permissions des fichiers lorsque vous utilisez `socat` avec des fichiers, surtout en mode écriture.
- Testez vos configurations dans un environnement sécurisé avant de les déployer en production.