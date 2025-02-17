# [Linux] Bash find utilisation : trouver des fichiers

## Overview
La commande `find` est utilisée pour rechercher des fichiers et des répertoires dans un système de fichiers. Elle permet de localiser des fichiers en fonction de divers critères tels que le nom, la taille, la date de modification, et bien plus encore.

## Usage
La syntaxe de base de la commande `find` est la suivante :

```bash
find [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `find` :

- `-name [nom]` : recherche des fichiers par leur nom.
- `-type [type]` : recherche des fichiers d'un type spécifique (par exemple, `f` pour les fichiers, `d` pour les répertoires).
- `-size [taille]` : recherche des fichiers d'une taille spécifique.
- `-mtime [n]` : recherche des fichiers modifiés il y a `n` jours.
- `-exec [commande] {} \;` : exécute une commande sur chaque fichier trouvé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `find` :

1. **Trouver un fichier par nom :**
   ```bash
   find /chemin/vers/repertoire -name "fichier.txt"
   ```

2. **Trouver tous les fichiers de type répertoire :**
   ```bash
   find /chemin/vers/repertoire -type d
   ```

3. **Trouver des fichiers de plus de 1 Mo :**
   ```bash
   find /chemin/vers/repertoire -size +1M
   ```

4. **Trouver des fichiers modifiés dans les 7 derniers jours :**
   ```bash
   find /chemin/vers/repertoire -mtime -7
   ```

5. **Exécuter une commande sur chaque fichier trouvé :**
   ```bash
   find /chemin/vers/repertoire -name "*.log" -exec rm {} \;
   ```

## Tips
- Utilisez des chemins absolus pour éviter toute confusion sur le répertoire de recherche.
- Combinez plusieurs options pour affiner vos recherches.
- Testez d'abord votre commande `find` sans l'option `-exec` pour voir quels fichiers seront affectés.
- Pensez à utiliser `-print` pour afficher les résultats si vous ne spécifiez pas d'autres actions.