# [Linux] Bash curl utilisation : Outil pour transférer des données

## Overview
Le commandement `curl` est un outil en ligne de commande utilisé pour transférer des données vers ou depuis un serveur. Il prend en charge divers protocoles, notamment HTTP, HTTPS, FTP et bien d'autres, ce qui en fait un outil polyvalent pour les développeurs et les administrateurs système.

## Usage
La syntaxe de base de la commande `curl` est la suivante :

```bash
curl [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `curl` :

- `-X` : Spécifie la méthode HTTP à utiliser (GET, POST, PUT, DELETE, etc.).
- `-d` : Envoie des données dans une requête POST.
- `-H` : Ajoute un en-tête HTTP à la requête.
- `-o` : Enregistre la sortie dans un fichier au lieu de l'afficher dans le terminal.
- `-I` : Récupère uniquement les en-têtes de la réponse.

## Common Examples

### 1. Faire une requête GET simple
Pour récupérer le contenu d'une page web :

```bash
curl http://example.com
```

### 2. Faire une requête POST avec des données
Pour envoyer des données à un serveur :

```bash
curl -X POST -d "param1=value1&param2=value2" http://example.com/api
```

### 3. Ajouter un en-tête à la requête
Pour inclure un en-tête personnalisé :

```bash
curl -H "Authorization: Bearer token" http://example.com/protected
```

### 4. Enregistrer la réponse dans un fichier
Pour sauvegarder le contenu d'une page dans un fichier :

```bash
curl -o page.html http://example.com
```

### 5. Récupérer uniquement les en-têtes
Pour obtenir les en-têtes de réponse d'une requête :

```bash
curl -I http://example.com
```

## Tips
- Utilisez l'option `-v` pour activer le mode verbeux, ce qui vous permettra de voir les détails de la requête et de la réponse.
- Pour des requêtes fréquentes, envisagez d'utiliser un fichier de configuration `.curlrc` pour stocker vos options par défaut.
- Soyez prudent avec les données sensibles lorsque vous utilisez `curl` dans des scripts, car elles peuvent être exposées dans l'historique des commandes.