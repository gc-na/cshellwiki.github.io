# [Linux] Bash iconv Utilisation : Convertir des fichiers entre différents encodages

## Overview
La commande `iconv` est utilisée pour convertir des fichiers texte d'un encodage à un autre. Cela est particulièrement utile lorsque vous travaillez avec des fichiers provenant de différentes sources qui peuvent utiliser des encodages variés.

## Usage
La syntaxe de base de la commande `iconv` est la suivante :

```bash
iconv [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `iconv` :

- `-f` : Spécifie l'encodage d'entrée (from encoding).
- `-t` : Spécifie l'encodage de sortie (to encoding).
- `-o` : Redirige la sortie vers un fichier au lieu de l'afficher dans le terminal.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `iconv` :

1. **Convertir un fichier de UTF-8 à ISO-8859-1** :
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 fichier_entree.txt -o fichier_sortie.txt
   ```

2. **Afficher le contenu converti dans le terminal** :
   ```bash
   iconv -f UTF-8 -t UTF-16 fichier_entree.txt
   ```

3. **Convertir un fichier et écraser le fichier d'origine** :
   ```bash
   iconv -f ISO-8859-1 -t UTF-8 fichier_entree.txt -o fichier_entree.txt
   ```

## Tips
- Toujours vérifier l'encodage d'origine et de destination pour éviter des pertes de données.
- Utilisez l'option `-o` pour éviter d'écraser accidentellement vos fichiers d'origine.
- Testez la conversion sur un petit fichier avant de l'appliquer à des fichiers plus volumineux.