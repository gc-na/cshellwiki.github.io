# [Linux] C Shell (csh) cp Utilisation : Copier des fichiers et des répertoires

## Overview
La commande `cp` dans le C Shell (csh) est utilisée pour copier des fichiers et des répertoires d'un emplacement à un autre. Elle permet de créer des duplicatas de fichiers tout en préservant leur contenu.

## Usage
La syntaxe de base de la commande `cp` est la suivante :

```csh
cp [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `cp` :

- `-i` : Demande une confirmation avant d'écraser un fichier existant.
- `-r` : Copie récursivement les répertoires et leur contenu.
- `-u` : Copie uniquement si le fichier source est plus récent que le fichier de destination ou si le fichier de destination n'existe pas.
- `-v` : Affiche les fichiers au fur et à mesure qu'ils sont copiés.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cp` :

1. Copier un fichier dans un autre emplacement :
   ```csh
   cp fichier.txt /chemin/vers/destination/
   ```

2. Copier un répertoire et son contenu :
   ```csh
   cp -r mon_repertoire /chemin/vers/destination/
   ```

3. Copier un fichier en demandant confirmation avant d'écraser :
   ```csh
   cp -i fichier.txt /chemin/vers/destination/
   ```

4. Copier un fichier uniquement s'il est plus récent :
   ```csh
   cp -u fichier.txt /chemin/vers/destination/
   ```

5. Copier un fichier tout en affichant les détails :
   ```csh
   cp -v fichier.txt /chemin/vers/destination/
   ```

## Tips
- Utilisez l'option `-i` pour éviter d'écraser accidentellement des fichiers importants.
- Pour copier plusieurs fichiers à la fois, vous pouvez spécifier plusieurs fichiers sources suivis du répertoire de destination.
- Pensez à vérifier les permissions des fichiers et répertoires, car cela peut affecter votre capacité à copier des fichiers.