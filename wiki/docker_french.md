# [Linux] C Shell (csh) docker utilisation : Gérer des conteneurs d'application

## Overview
La commande `docker` est utilisée pour gérer des conteneurs d'application. Elle permet de créer, exécuter et gérer des conteneurs, qui sont des environnements légers et portables pour exécuter des applications.

## Usage
La syntaxe de base de la commande `docker` est la suivante :

```csh
docker [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `docker` :

- `run` : Crée et exécute un conteneur à partir d'une image.
- `ps` : Liste les conteneurs en cours d'exécution.
- `images` : Affiche les images disponibles sur le système.
- `rm` : Supprime un ou plusieurs conteneurs.
- `rmi` : Supprime une ou plusieurs images.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `docker` :

1. **Exécuter un conteneur simple :**
   ```csh
   docker run hello-world
   ```

2. **Lister les conteneurs en cours d'exécution :**
   ```csh
   docker ps
   ```

3. **Lister toutes les images disponibles :**
   ```csh
   docker images
   ```

4. **Supprimer un conteneur spécifique :**
   ```csh
   docker rm <container_id>
   ```

5. **Supprimer une image spécifique :**
   ```csh
   docker rmi <image_id>
   ```

## Tips
- Toujours vérifier l'état des conteneurs avec `docker ps` avant de tenter de les supprimer.
- Utilisez des noms explicites pour vos conteneurs afin de faciliter leur gestion.
- Pensez à utiliser des volumes pour conserver les données même après la suppression des conteneurs.