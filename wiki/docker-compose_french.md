# [Linux] Bash docker-compose utilisation : Gérer des applications multi-conteneurs

## Overview
La commande `docker-compose` permet de définir et de gérer des applications composées de plusieurs conteneurs Docker. Elle utilise un fichier de configuration, généralement nommé `docker-compose.yml`, pour spécifier les services, réseaux et volumes nécessaires à l'application.

## Usage
La syntaxe de base de la commande `docker-compose` est la suivante :

```bash
docker-compose [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `docker-compose` :

- `up` : Démarre les conteneurs définis dans le fichier `docker-compose.yml`.
- `down` : Arrête et supprime les conteneurs, réseaux et volumes créés par `up`.
- `build` : Construit ou reconstruit les services définis dans le fichier.
- `logs` : Affiche les journaux des conteneurs.
- `exec` : Exécute une commande dans un conteneur en cours d'exécution.

## Common Examples
Voici quelques exemples pratiques d'utilisation de `docker-compose` :

1. **Démarrer les services** :
   ```bash
   docker-compose up
   ```

2. **Démarrer les services en arrière-plan** :
   ```bash
   docker-compose up -d
   ```

3. **Arrêter et supprimer les conteneurs** :
   ```bash
   docker-compose down
   ```

4. **Construire les images des services** :
   ```bash
   docker-compose build
   ```

5. **Afficher les journaux des services** :
   ```bash
   docker-compose logs
   ```

6. **Exécuter une commande dans un conteneur** :
   ```bash
   docker-compose exec <service_name> <command>
   ```

## Tips
- Utilisez l'option `-d` pour exécuter les services en mode détaché, ce qui vous permet de continuer à utiliser le terminal.
- Vérifiez toujours le fichier `docker-compose.yml` pour vous assurer que tous les services sont correctement configurés avant de démarrer.
- Utilisez `docker-compose ps` pour voir l'état des conteneurs en cours d'exécution.
- Pensez à versionner votre fichier `docker-compose.yml` pour garder une trace des modifications apportées à votre configuration.