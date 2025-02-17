# [Linux] Bash psql : Exécuter des requêtes SQL dans PostgreSQL

## Overview
La commande `psql` est un client en ligne de commande pour interagir avec une base de données PostgreSQL. Elle permet d'exécuter des requêtes SQL, de gérer des bases de données et d'effectuer diverses tâches administratives.

## Usage
La syntaxe de base de la commande `psql` est la suivante :

```bash
psql [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `psql` :

- `-h` : Spécifie l'hôte de la base de données.
- `-p` : Définit le port de connexion.
- `-U` : Indique le nom d'utilisateur pour se connecter à la base de données.
- `-d` : Spécifie le nom de la base de données à laquelle se connecter.
- `-f` : Exécute les commandes SQL à partir d'un fichier.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `psql` :

1. **Se connecter à une base de données :**
   ```bash
   psql -U nom_utilisateur -d nom_base_de_données
   ```

2. **Exécuter une requête SQL directement depuis la ligne de commande :**
   ```bash
   psql -U nom_utilisateur -d nom_base_de_données -c "SELECT * FROM table;"
   ```

3. **Exécuter des commandes SQL à partir d'un fichier :**
   ```bash
   psql -U nom_utilisateur -d nom_base_de_données -f chemin/vers/fichier.sql
   ```

4. **Lister toutes les bases de données :**
   ```bash
   psql -U nom_utilisateur -c "\l"
   ```

## Tips
- Utilisez l'option `-W` pour demander un mot de passe lors de la connexion.
- Pour sortir de l'interface `psql`, tapez `\q`.
- Familiarisez-vous avec les commandes internes de `psql`, comme `\d` pour décrire les tables, afin de naviguer plus facilement dans vos bases de données.