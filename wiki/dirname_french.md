# [Linux] Bash dirname Utilisation : Extraire le répertoire d'un chemin

## Overview
La commande `dirname` est utilisée pour extraire le chemin du répertoire d'un fichier ou d'un chemin donné. Elle renvoie la partie du chemin qui précède le dernier séparateur de répertoire.

## Usage
La syntaxe de base de la commande `dirname` est la suivante :

```bash
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero` : Traite les chemins d'accès séparés par des caractères null (NUL).
- `--help` : Affiche l'aide et quitte.
- `--version` : Affiche la version de la commande et quitte.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `dirname` :

1. Extraire le répertoire d'un chemin de fichier :

```bash
dirname /home/user/documents/file.txt
```
*Sortie :*
```
/home/user/documents
```

2. Utiliser `dirname` avec un chemin relatif :

```bash
dirname ./images/photo.jpg
```
*Sortie :*
```
./images
```

3. Extraire le répertoire d'un chemin avec des espaces :

```bash
dirname "/home/user/My Documents/file.txt"
```
*Sortie :*
```
/home/user/My Documents
```

4. Traiter plusieurs chemins en une seule commande :

```bash
dirname /var/log/syslog /usr/local/bin/script.sh
```
*Sortie :*
```
/var/log
/usr/local/bin
```

## Tips
- Utilisez des guillemets autour des chemins contenant des espaces pour éviter des erreurs.
- Combinez `dirname` avec d'autres commandes comme `find` ou `xargs` pour des opérations plus complexes sur les fichiers.
- Pensez à vérifier les permissions des répertoires lorsque vous utilisez `dirname` dans des scripts pour éviter des erreurs inattendues.