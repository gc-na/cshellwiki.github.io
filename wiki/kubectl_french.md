# [Linux] C Shell (csh) kubectl utilisation : Gérer les ressources Kubernetes

## Overview
La commande `kubectl` est l'outil en ligne de commande principal pour interagir avec un cluster Kubernetes. Elle permet aux utilisateurs de déployer des applications, de gérer les ressources et d'obtenir des informations sur l'état du cluster.

## Usage
La syntaxe de base de la commande `kubectl` est la suivante :

```bash
kubectl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `kubectl` :

- `get` : Récupérer des informations sur les ressources.
- `apply` : Appliquer des modifications à des ressources à partir d'un fichier de configuration.
- `delete` : Supprimer des ressources du cluster.
- `describe` : Afficher des détails sur une ressource spécifique.
- `logs` : Afficher les journaux d'un pod.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `kubectl` :

- Pour obtenir la liste des pods dans le namespace par défaut :

```bash
kubectl get pods
```

- Pour appliquer un fichier de configuration YAML :

```bash
kubectl apply -f mon-deploiement.yaml
```

- Pour supprimer un pod spécifique :

```bash
kubectl delete pod nom-du-pod
```

- Pour afficher les détails d'un service :

```bash
kubectl describe service nom-du-service
```

- Pour voir les journaux d'un pod :

```bash
kubectl logs nom-du-pod
```

## Tips
- Utilisez `kubectl get all` pour obtenir un aperçu de toutes les ressources dans le namespace actuel.
- Ajoutez l'option `-n` pour spécifier un namespace particulier, par exemple `kubectl get pods -n mon-namespace`.
- Pensez à utiliser des fichiers de configuration pour gérer vos ressources de manière déclarative, ce qui facilite le suivi des modifications.