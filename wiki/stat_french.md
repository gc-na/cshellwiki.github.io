# [Linux] Bash stat : Afficher les informations sur les fichiers

## Overview
La commande `stat` est utilisée pour afficher des informations détaillées sur un fichier ou un système de fichiers. Elle fournit des données telles que la taille, les permissions, les dates de dernière modification, et d'autres attributs importants.

## Usage
La syntaxe de base de la commande `stat` est la suivante :

```bash
stat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `stat` :

- `-c` : Permet de spécifier un format de sortie personnalisé.
- `-f` : Affiche les informations sur le système de fichiers contenant le fichier.
- `--help` : Affiche l'aide et les options disponibles.
- `--version` : Affiche la version de la commande `stat`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `stat` :

1. Afficher les informations par défaut sur un fichier :
   ```bash
   stat mon_fichier.txt
   ```

2. Afficher les informations sur un répertoire :
   ```bash
   stat mon_dossier/
   ```

3. Utiliser un format de sortie personnalisé pour afficher uniquement la taille et les permissions :
   ```bash
   stat -c "Taille : %s, Permissions : %A" mon_fichier.txt
   ```

4. Afficher les informations sur le système de fichiers d'un fichier :
   ```bash
   stat -f mon_fichier.txt
   ```

## Tips
- Utilisez l'option `-c` pour personnaliser la sortie et obtenir uniquement les informations qui vous intéressent.
- Pensez à vérifier les permissions d'un fichier avec `stat` avant de tenter de le modifier.
- Pour une vue rapide des informations d'un fichier, utilisez simplement `stat` sans options pour obtenir un aperçu complet.