# [Linux] Bash cp Utilisation : Copier des fichiers et des répertoires

## Overview
La commande `cp` est utilisée pour copier des fichiers et des répertoires dans un système Linux. Elle permet de créer une ou plusieurs copies d'un fichier ou d'un répertoire source vers une destination spécifiée.

## Usage
La syntaxe de base de la commande `cp` est la suivante :

```bash
cp [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `cp` :

- `-r` : Copie récursivement les répertoires et leur contenu.
- `-i` : Demande confirmation avant d'écraser un fichier existant.
- `-u` : Copie uniquement si le fichier source est plus récent que le fichier de destination ou si le fichier de destination n'existe pas.
- `-v` : Affiche les fichiers au fur et à mesure qu'ils sont copiés (mode verbeux).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cp` :

1. Copier un fichier :
   ```bash
   cp fichier.txt copie_fichier.txt
   ```

2. Copier un répertoire et son contenu :
   ```bash
   cp -r dossier_source/ dossier_destination/
   ```

3. Copier un fichier avec confirmation avant écrasement :
   ```bash
   cp -i fichier.txt copie_fichier.txt
   ```

4. Copier un fichier uniquement s'il est plus récent :
   ```bash
   cp -u fichier.txt copie_fichier.txt
   ```

5. Copier plusieurs fichiers dans un répertoire :
   ```bash
   cp fichier1.txt fichier2.txt dossier_destination/
   ```

## Tips
- Utilisez l'option `-v` pour suivre le processus de copie, surtout lorsque vous copiez plusieurs fichiers.
- Soyez prudent avec l'option `-r`, car elle peut écraser des fichiers sans avertissement si vous ne l'utilisez pas avec `-i`.
- Pour éviter des erreurs, vérifiez toujours le chemin de destination avant de lancer la commande, surtout lorsque vous copiez des fichiers importants.