# [Linux] C Shell (csh) stat : Afficher les informations sur les fichiers

## Overview
La commande `stat` est utilisée pour afficher des informations détaillées sur un fichier ou un répertoire. Elle fournit des données telles que la taille, les permissions, les timestamps et d'autres attributs importants.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
stat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `stat` :

- `-c` : Permet de spécifier un format de sortie personnalisé.
- `-f` : Affiche les informations dans un format spécifique au système de fichiers.
- `--help` : Affiche l'aide et les options disponibles pour la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `stat` :

1. Afficher les informations par défaut sur un fichier :
   ```csh
   stat mon_fichier.txt
   ```

2. Afficher les informations d'un répertoire :
   ```csh
   stat mon_repertoire/
   ```

3. Utiliser un format de sortie personnalisé :
   ```csh
   stat -c '%n: %s octets' mon_fichier.txt
   ```

4. Afficher les informations d'un fichier avec un format spécifique au système de fichiers :
   ```csh
   stat -f '%N: %z octets' mon_fichier.txt
   ```

## Tips
- Utilisez l'option `-c` pour personnaliser la sortie et obtenir uniquement les informations dont vous avez besoin.
- Pensez à vérifier les permissions d'un fichier avec `stat` avant d'essayer de l'ouvrir ou de le modifier.
- Combinez `stat` avec d'autres commandes pour automatiser des tâches de gestion de fichiers.