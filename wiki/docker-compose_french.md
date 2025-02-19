# [Linux] C Shell (csh) docker-compose : Gérer des applications multi-conteneurs

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
- `build` : Construit ou reconstruit les services définis.
- `logs` : Affiche les journaux des conteneurs en cours d'exécution.
- `ps` : Liste les conteneurs gérés par `docker-compose`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `docker-compose` :

1. **Démarrer les services définis** :
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

5. **Afficher les journaux des conteneurs** :
   ```bash
   docker-compose logs
   ```

## Tips
- Utilisez l'option `-d` avec `up` pour exécuter les conteneurs en arrière-plan, ce qui vous permet de continuer à utiliser le terminal.
- Assurez-vous que votre fichier `docker-compose.yml` est correctement configuré pour éviter des erreurs lors du démarrage des services.
- Utilisez `docker-compose ps` pour vérifier l'état de vos conteneurs et vous assurer qu'ils fonctionnent comme prévu.