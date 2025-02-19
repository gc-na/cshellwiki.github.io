# [Linux] C Shell (csh) wget Utilisation : Télécharger des fichiers depuis le web

## Overview
Le commandement `wget` est un outil en ligne de commande utilisé pour télécharger des fichiers à partir du web. Il supporte les protocoles HTTP, HTTPS et FTP, ce qui en fait un choix polyvalent pour récupérer des fichiers de manière simple et efficace.

## Usage
La syntaxe de base de la commande `wget` est la suivante :

```bash
wget [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `wget` :

- `-O <nom_fichier>` : Spécifie le nom du fichier de sortie.
- `-q` : Mode silencieux, ne montre pas les messages de progression.
- `-c` : Reprend un téléchargement interrompu.
- `--limit-rate=<vitesse>` : Limite la vitesse de téléchargement.
- `-r` : Télécharge récursivement des fichiers.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `wget` :

1. Télécharger un fichier simple :
   ```bash
   wget http://exemple.com/fichier.txt
   ```

2. Télécharger un fichier avec un nom de sortie spécifique :
   ```bash
   wget -O mon_fichier.txt http://exemple.com/fichier.txt
   ```

3. Reprendre un téléchargement interrompu :
   ```bash
   wget -c http://exemple.com/fichier_grand.zip
   ```

4. Télécharger un site web de manière récursive :
   ```bash
   wget -r http://exemple.com
   ```

5. Limiter la vitesse de téléchargement à 200kB/s :
   ```bash
   wget --limit-rate=200k http://exemple.com/fichier.zip
   ```

## Tips
- Utilisez l'option `-q` pour éviter d'encombrer votre terminal avec des messages si vous téléchargez plusieurs fichiers.
- Pensez à utiliser `-c` pour éviter de recommencer un téléchargement en cas d'interruption.
- Pour les téléchargements récursifs, assurez-vous de respecter les règles du site web pour éviter d'être bloqué pour un comportement abusif.