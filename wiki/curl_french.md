# [Linux] C Shell (csh) curl Utilisation : Récupérer des données à partir d'URL

## Overview
La commande `curl` est un outil en ligne de commande utilisé pour transférer des données depuis ou vers un serveur à l'aide de divers protocoles, notamment HTTP, HTTPS, FTP, et plus encore. Elle est particulièrement utile pour interagir avec des API web et télécharger des fichiers.

## Usage
La syntaxe de base de la commande `curl` est la suivante :

```csh
curl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `curl` :

- `-O` : Télécharge le fichier et le sauvegarde avec le même nom que sur le serveur.
- `-L` : Suit les redirections si l'URL a changé.
- `-d` : Envoie des données dans une requête POST.
- `-H` : Ajoute un en-tête HTTP à la requête.
- `-u` : Fournit un nom d'utilisateur et un mot de passe pour l'authentification.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `curl` :

1. **Télécharger un fichier :**
   ```csh
   curl -O http://example.com/fichier.txt
   ```

2. **Suivre les redirections :**
   ```csh
   curl -L http://example.com
   ```

3. **Envoyer des données avec une requête POST :**
   ```csh
   curl -d "param1=valeur1&param2=valeur2" http://example.com/api
   ```

4. **Ajouter un en-tête HTTP :**
   ```csh
   curl -H "Authorization: Bearer token" http://example.com/api
   ```

5. **Télécharger un fichier en utilisant l'authentification :**
   ```csh
   curl -u nom_utilisateur:mot_de_passe -O http://example.com/fichier_protege.txt
   ```

## Tips
- Utilisez l'option `-v` pour activer le mode verbeux et obtenir plus d'informations sur la requête et la réponse.
- Pour tester des API, envisagez d'utiliser `curl` avec des options comme `-X` pour spécifier le type de requête (GET, POST, PUT, DELETE).
- N'oubliez pas de vérifier les permissions des fichiers téléchargés, surtout si vous les exécutez ou les utilisez dans des scripts.