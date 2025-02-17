# [Linux] Bash mysql utilisation : Exécuter des requêtes SQL

## Overview
La commande `mysql` est un client en ligne de commande pour interagir avec un serveur de bases de données MySQL. Elle permet d'exécuter des requêtes SQL, de gérer des bases de données et d'effectuer diverses opérations sur les données.

## Usage
La syntaxe de base de la commande `mysql` est la suivante :

```bash
mysql [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mysql` :

- `-u` : Spécifie le nom d'utilisateur pour se connecter à la base de données.
- `-p` : Demande un mot de passe pour l'utilisateur spécifié.
- `-h` : Indique l'hôte du serveur MySQL (par défaut, c'est `localhost`).
- `-D` : Sélectionne la base de données à utiliser après la connexion.
- `-e` : Permet d'exécuter une commande SQL directement depuis la ligne de commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mysql` :

1. **Se connecter à un serveur MySQL :**
   ```bash
   mysql -u nom_utilisateur -p
   ```
   Cela vous demandera de saisir le mot de passe pour l'utilisateur spécifié.

2. **Exécuter une requête SQL directement :**
   ```bash
   mysql -u nom_utilisateur -p -e "SHOW DATABASES;"
   ```
   Cette commande affichera toutes les bases de données disponibles sur le serveur.

3. **Se connecter à une base de données spécifique :**
   ```bash
   mysql -u nom_utilisateur -p -D nom_base_de_données
   ```

4. **Importer un fichier SQL :**
   ```bash
   mysql -u nom_utilisateur -p nom_base_de_données < fichier.sql
   ```

5. **Exporter une base de données :**
   ```bash
   mysqldump -u nom_utilisateur -p nom_base_de_données > sauvegarde.sql
   ```

## Tips
- Toujours utiliser des mots de passe forts pour vos utilisateurs MySQL afin de protéger vos données.
- Pensez à faire des sauvegardes régulières de vos bases de données avec `mysqldump`.
- Utilisez `-h` pour vous connecter à des serveurs distants et `-D` pour éviter de devoir sélectionner la base de données après la connexion.
- Pour des requêtes complexes, envisagez d'utiliser des fichiers `.sql` pour une meilleure lisibilité et maintenance.