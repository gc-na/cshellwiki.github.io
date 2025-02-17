# [Linux] Bash 7z Utilisation : Compresser et décompresser des fichiers

## Overview
La commande `7z` est un outil puissant pour la compression et la décompression de fichiers. Elle fait partie de l'archiveur 7-Zip, qui supporte plusieurs formats d'archive, y compris 7z, ZIP, RAR, et bien d'autres. Grâce à sa capacité à créer des archives hautement compressées, `7z` est souvent utilisé pour réduire la taille des fichiers et faciliter leur transfert.

## Usage
La syntaxe de base de la commande `7z` est la suivante :

```
7z [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `7z` :

- `a` : Ajouter des fichiers à une archive.
- `x` : Extraire des fichiers d'une archive.
- `l` : Lister le contenu d'une archive.
- `d` : Supprimer des fichiers d'une archive.
- `t` : Tester l'intégrité d'une archive.

## Common Examples

### 1. Créer une archive
Pour créer une archive nommée `archive.7z` contenant les fichiers `file1.txt` et `file2.txt`, utilisez la commande suivante :

```bash
7z a archive.7z file1.txt file2.txt
```

### 2. Extraire une archive
Pour extraire le contenu de `archive.7z` dans le répertoire courant, utilisez :

```bash
7z x archive.7z
```

### 3. Lister le contenu d'une archive
Pour afficher le contenu de `archive.7z`, utilisez :

```bash
7z l archive.7z
```

### 4. Supprimer un fichier d'une archive
Pour supprimer `file1.txt` de `archive.7z`, utilisez :

```bash
7z d archive.7z file1.txt
```

### 5. Tester l'intégrité d'une archive
Pour vérifier si `archive.7z` est corrompue, utilisez :

```bash
7z t archive.7z
```

## Tips
- **Utiliser des options de compression** : Vous pouvez spécifier le niveau de compression en ajoutant `-mx=N`, où N est un nombre de 0 à 9 (0 = aucune compression, 9 = compression maximale).
- **Créer des archives fractionnées** : Pour diviser une archive en plusieurs parties, utilisez l'option `-v` suivie de la taille souhaitée (par exemple, `-v10m` pour des fichiers de 10 Mo).
- **Automatiser avec des scripts** : Intégrez `7z` dans vos scripts Bash pour automatiser la gestion des fichiers compressés.

Avec ces informations, vous êtes prêt à utiliser la commande `7z` pour gérer vos fichiers efficacement.