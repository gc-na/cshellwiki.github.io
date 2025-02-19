# [Linux] C Shell (csh) xargs : Exécuter des commandes avec des arguments

## Overview
La commande `xargs` est utilisée pour construire et exécuter des commandes à partir de l'entrée standard. Elle prend des arguments d'une commande précédente et les passe à une autre commande, ce qui permet de traiter des listes d'arguments de manière efficace.

## Usage
La syntaxe de base de la commande `xargs` est la suivante :

```csh
xargs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `xargs` :

- `-n N` : Indique à `xargs` d'utiliser au maximum N arguments par commande.
- `-d DELIM` : Spécifie un délimiteur personnalisé pour séparer les arguments.
- `-p` : Demande une confirmation avant d'exécuter chaque commande.
- `-0` : Utilise un caractère nul (`\0`) comme délimiteur, ce qui est utile pour traiter les noms de fichiers contenant des espaces.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `xargs` :

1. **Supprimer des fichiers listés dans un fichier :**
   ```csh
   cat fichiers_a_supprimer.txt | xargs rm
   ```

2. **Compresser tous les fichiers `.txt` dans un répertoire :**
   ```csh
   ls *.txt | xargs gzip
   ```

3. **Trouver et supprimer des fichiers vides :**
   ```csh
   find . -type f -empty | xargs rm
   ```

4. **Compter le nombre de lignes dans plusieurs fichiers :**
   ```csh
   ls *.txt | xargs wc -l
   ```

## Tips
- Utilisez l'option `-n` pour contrôler le nombre d'arguments passés à chaque commande, ce qui peut être utile pour éviter des erreurs de dépassement de mémoire.
- Lorsque vous traitez des fichiers avec des espaces dans leurs noms, utilisez l'option `-0` avec `find` et `xargs` pour garantir que tous les noms de fichiers sont correctement interprétés.
- Pensez à utiliser l'option `-p` pour vérifier les commandes avant leur exécution, surtout lorsque vous effectuez des opérations destructrices comme `rm`.