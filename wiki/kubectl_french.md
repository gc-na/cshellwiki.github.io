# [Linux] Bash kubectl Utilisation : Gérer les ressources Kubernetes

## Overview
Le commandement `kubectl` est l'outil en ligne de commande principal pour interagir avec un cluster Kubernetes. Il permet aux utilisateurs de déployer des applications, de gérer les ressources du cluster et d'obtenir des informations sur l'état des objets Kubernetes.

## Usage
La syntaxe de base pour utiliser `kubectl` est la suivante :

```bash
kubectl [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `kubectl` :

- `get` : Récupère des informations sur les ressources.
- `apply` : Applique des modifications à des ressources à partir de fichiers de configuration.
- `delete` : Supprime des ressources spécifiées.
- `describe` : Affiche des détails sur une ressource spécifique.
- `logs` : Affiche les journaux d'un pod.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `kubectl` :

1. **Lister tous les pods dans le namespace par défaut :**
   ```bash
   kubectl get pods
   ```

2. **Appliquer un fichier de configuration YAML :**
   ```bash
   kubectl apply -f mon-deploiement.yaml
   ```

3. **Supprimer un pod spécifique :**
   ```bash
   kubectl delete pod mon-pod
   ```

4. **Afficher les détails d'un service :**
   ```bash
   kubectl describe service mon-service
   ```

5. **Afficher les journaux d'un pod :**
   ```bash
   kubectl logs mon-pod
   ```

## Tips
- Utilisez l'option `-n` pour spécifier un namespace si vous ne travaillez pas dans le namespace par défaut, par exemple : `kubectl get pods -n mon-namespace`.
- Pour obtenir des résultats plus détaillés, ajoutez l'option `-o wide` à vos commandes, par exemple : `kubectl get pods -o wide`.
- Familiarisez-vous avec les fichiers de configuration YAML pour gérer vos ressources Kubernetes de manière efficace.