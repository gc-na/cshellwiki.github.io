# [Linux] Bash minikube utilisation : Gérer des clusters Kubernetes localement

## Overview
La commande `minikube` permet de créer et de gérer des clusters Kubernetes localement sur votre machine. C'est un outil idéal pour les développeurs souhaitant tester des applications Kubernetes sans avoir besoin d'un environnement de production complet.

## Usage
La syntaxe de base de la commande `minikube` est la suivante :

```bash
minikube [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `minikube` :

- `start` : Démarre un nouveau cluster Minikube.
- `stop` : Arrête le cluster Minikube en cours d'exécution.
- `delete` : Supprime le cluster Minikube.
- `status` : Affiche l'état actuel du cluster Minikube.
- `kubectl` : Permet d'exécuter des commandes kubectl dans le cluster Minikube.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `minikube` :

### Démarrer un cluster Minikube
```bash
minikube start
```

### Arrêter le cluster Minikube
```bash
minikube stop
```

### Supprimer le cluster Minikube
```bash
minikube delete
```

### Vérifier l'état du cluster
```bash
minikube status
```

### Exécuter une commande kubectl
```bash
minikube kubectl -- get pods
```

## Tips
- Assurez-vous que votre machine dispose de suffisamment de ressources (CPU, RAM) pour exécuter Minikube efficacement.
- Utilisez `minikube addons` pour activer des fonctionnalités supplémentaires comme le tableau de bord Kubernetes.
- Pensez à utiliser des profils si vous souhaitez gérer plusieurs clusters Minikube en parallèle.