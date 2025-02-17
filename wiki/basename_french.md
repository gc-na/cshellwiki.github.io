# [Linux] Bash basename utilisation : Extraire le nom de fichier d'un chemin

## Overview
La commande `basename` est utilisée pour extraire le nom de fichier d'un chemin donné. Elle permet de simplifier le traitement des chemins en ne conservant que la partie finale, c'est-à-dire le nom du fichier ou du répertoire.

## Usage
La syntaxe de base de la commande `basename` est la suivante :

```bash
basename [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `basename` :

- `-a` : Traite plusieurs chemins en une seule commande.
- `-s` : Supprime une extension spécifique du nom de fichier.
- `--help` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `basename` :

1. Extraire le nom de fichier d'un chemin :

```bash
basename /chemin/vers/fichier.txt
```
*Sortie :* `fichier.txt`

2. Extraire le nom de fichier sans l'extension :

```bash
basename /chemin/vers/fichier.txt .txt
```
*Sortie :* `fichier`

3. Traiter plusieurs chemins :

```bash
basename -a /chemin/vers/fichier1.txt /chemin/vers/fichier2.txt
```
*Sortie :*
```
fichier1.txt
fichier2.txt
```

4. Supprimer une extension d'un fichier :

```bash
basename /chemin/vers/fichier.tar.gz .tar.gz
```
*Sortie :* `fichier`

## Tips
- Utilisez l'option `-a` pour traiter plusieurs fichiers à la fois, ce qui peut être très pratique dans des scripts.
- Pensez à spécifier l'extension à supprimer pour obtenir un nom de fichier propre sans suffixe.
- Combinez `basename` avec d'autres commandes comme `find` pour automatiser le traitement des fichiers dans des répertoires.