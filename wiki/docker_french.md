# [Linux] Bash docker utilisation : Gérer des conteneurs et des images

## Overview
La commande `docker` est utilisée pour gérer des conteneurs et des images Docker. Elle permet de créer, exécuter et gérer des applications dans des environnements isolés, facilitant ainsi le développement et le déploiement d'applications.

## Usage
La syntaxe de base de la commande `docker` est la suivante :

```bash
docker [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `docker` :

- `run` : Crée et exécute un conteneur à partir d'une image spécifiée.
- `ps` : Affiche les conteneurs en cours d'exécution.
- `images` : Liste toutes les images Docker présentes sur le système.
- `rm` : Supprime un ou plusieurs conteneurs.
- `rmi` : Supprime une ou plusieurs images.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `docker` :

1. **Exécuter un conteneur Nginx :**
   ```bash
   docker run -d -p 80:80 nginx
   ```
   Cela exécute un conteneur Nginx en arrière-plan et le lie au port 80 de l'hôte.

2. **Lister les conteneurs en cours d'exécution :**
   ```bash
   docker ps
   ```
   Cette commande affiche tous les conteneurs qui sont actuellement en cours d'exécution.

3. **Lister toutes les images Docker :**
   ```bash
   docker images
   ```
   Cela montre toutes les images disponibles sur votre système.

4. **Supprimer un conteneur :**
   ```bash
   docker rm <container_id>
   ```
   Remplacez `<container_id>` par l'identifiant du conteneur que vous souhaitez supprimer.

5. **Supprimer une image Docker :**
   ```bash
   docker rmi <image_id>
   ```
   Remplacez `<image_id>` par l'identifiant de l'image que vous souhaitez supprimer.

## Tips
- Utilisez `docker-compose` pour gérer des applications multi-conteneurs plus facilement.
- Pensez à nommer vos conteneurs et images de manière descriptive pour faciliter leur identification.
- Vérifiez régulièrement les images et conteneurs inutilisés pour libérer de l'espace disque avec `docker system prune`.