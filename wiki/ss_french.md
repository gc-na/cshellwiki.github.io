# [Linux] C Shell (csh) ss Utilisation : Afficher les connexions réseau

## Overview
La commande `ss` est utilisée pour afficher les connexions réseau, les sockets et les statistiques de réseau sur un système. Elle est souvent considérée comme un outil plus rapide et plus efficace que la commande `netstat`.

## Usage
La syntaxe de base de la commande `ss` est la suivante :

```csh
ss [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ss` :

- `-t` : Affiche uniquement les connexions TCP.
- `-u` : Affiche uniquement les connexions UDP.
- `-l` : Montre les sockets en écoute.
- `-p` : Affiche les processus utilisant les sockets.
- `-n` : Affiche les adresses et numéros de port sous forme numérique, sans tenter de résoudre les noms.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ss` :

1. Afficher toutes les connexions TCP :
   ```csh
   ss -t
   ```

2. Afficher toutes les connexions UDP :
   ```csh
   ss -u
   ```

3. Afficher les sockets en écoute :
   ```csh
   ss -l
   ```

4. Afficher les connexions avec les processus associés :
   ```csh
   ss -p
   ```

5. Afficher les connexions avec des adresses numériques :
   ```csh
   ss -n
   ```

## Tips
- Utilisez `ss -t -l` pour voir les ports TCP en écoute, ce qui est utile pour le dépannage des serveurs.
- Combinez plusieurs options pour affiner vos résultats, par exemple `ss -tunlp` pour afficher les connexions TCP et UDP avec les processus.
- Pensez à exécuter `ss` avec des privilèges élevés (par exemple, en tant que super utilisateur) pour voir toutes les connexions, y compris celles des autres utilisateurs.