# [Linux] Bash wget utilisation : Téléchargement de fichiers depuis le web

## Overview
La commande `wget` est un outil en ligne de commande qui permet de télécharger des fichiers à partir du web. Elle prend en charge divers protocoles tels que HTTP, HTTPS et FTP, et est particulièrement utile pour récupérer des fichiers de manière non interactive.

## Usage
La syntaxe de base de la commande `wget` est la suivante :

```bash
wget [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `wget` :

- `-O [nom_fichier]` : Spécifie le nom du fichier de sortie.
- `-c` : Reprend un téléchargement interrompu.
- `-r` : Télécharge de manière récursive, ce qui est utile pour télécharger des sites web entiers.
- `-q` : Mode silencieux, n'affiche pas les messages de progression.
- `--limit-rate=[vitesse]` : Limite la vitesse de téléchargement à la valeur spécifiée.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `wget` :

1. Télécharger un fichier simple :
   ```bash
   wget http://example.com/fichier.txt
   ```

2. Télécharger un fichier et le renommer :
   ```bash
   wget -O nouveau_nom.txt http://example.com/fichier.txt
   ```

3. Reprendre un téléchargement interrompu :
   ```bash
   wget -c http://example.com/fichier.zip
   ```

4. Télécharger un site web de manière récursive :
   ```bash
   wget -r http://example.com
   ```

5. Limiter la vitesse de téléchargement :
   ```bash
   wget --limit-rate=200k http://example.com/fichier.zip
   ```

## Tips
- Utilisez l'option `-q` pour éviter d'encombrer votre terminal avec des messages si vous téléchargez plusieurs fichiers.
- Pensez à utiliser `-r` avec précaution pour ne pas surcharger un serveur web.
- Vérifiez toujours les droits d'auteur et les conditions d'utilisation des fichiers que vous téléchargez.