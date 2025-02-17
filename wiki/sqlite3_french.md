# [Linux] Bash sqlite3 Utilisation : Interagir avec des bases de données SQLite

## Overview
La commande `sqlite3` permet d'interagir avec des bases de données SQLite. Elle offre une interface en ligne de commande pour créer, manipuler et interroger des bases de données, ce qui en fait un outil puissant pour les développeurs et les administrateurs de bases de données.

## Usage
La syntaxe de base de la commande `sqlite3` est la suivante :

```bash
sqlite3 [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `sqlite3` :

- `-help` : Affiche l'aide et les options disponibles.
- `-version` : Affiche la version de SQLite.
- `-init <file>` : Exécute les commandes SQL contenues dans le fichier spécifié au démarrage.
- `-batch` : Exécute les commandes en mode batch, sans interaction avec l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `sqlite3` :

### Créer une nouvelle base de données
```bash
sqlite3 ma_base_de_donnees.db
```

### Créer une table
```bash
sqlite3 ma_base_de_donnees.db "CREATE TABLE utilisateurs (id INTEGER PRIMARY KEY, nom TEXT, age INTEGER);"
```

### Insérer des données
```bash
sqlite3 ma_base_de_donnees.db "INSERT INTO utilisateurs (nom, age) VALUES ('Alice', 30);"
```

### Interroger des données
```bash
sqlite3 ma_base_de_donnees.db "SELECT * FROM utilisateurs;"
```

### Exporter des données vers un fichier
```bash
sqlite3 ma_base_de_donnees.db ".dump" > sauvegarde.sql
```

## Tips
- Utilisez l'option `-init` pour exécuter des scripts SQL au démarrage, ce qui peut faciliter la configuration initiale de votre base de données.
- Pensez à sauvegarder régulièrement votre base de données en utilisant la commande `.dump`.
- Familiarisez-vous avec les commandes SQL de base pour tirer le meilleur parti de `sqlite3`, comme `SELECT`, `INSERT`, `UPDATE`, et `DELETE`.