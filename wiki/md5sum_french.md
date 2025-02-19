# [Linux] C Shell (csh) md5sum : Calculer le hachage MD5 d'un fichier

## Overview
La commande `md5sum` est utilisée pour calculer et vérifier le hachage MD5 d'un fichier. Cela permet de s'assurer que le contenu d'un fichier n'a pas été modifié, en comparant le hachage calculé avec un hachage connu.

## Usage
La syntaxe de base de la commande `md5sum` est la suivante :

```csh
md5sum [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `md5sum` :

- `-b` : Traite les fichiers en mode binaire.
- `-c` : Vérifie les sommes de contrôle MD5 à partir d'un fichier.
- `-t` : Traite les fichiers en mode texte.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `md5sum` :

1. Calculer le hachage MD5 d'un fichier :

   ```csh
   md5sum fichier.txt
   ```

2. Vérifier un fichier à l'aide d'un fichier de sommes de contrôle :

   ```csh
   md5sum -c checksums.md5
   ```

3. Calculer le hachage MD5 d'un fichier binaire :

   ```csh
   md5sum -b image.png
   ```

4. Enregistrer le hachage MD5 d'un fichier dans un fichier texte :

   ```csh
   md5sum fichier.txt > hash.txt
   ```

## Tips
- Toujours vérifier les fichiers téléchargés en utilisant `md5sum` pour s'assurer qu'ils n'ont pas été corrompus.
- Utilisez l'option `-c` pour vérifier plusieurs fichiers à la fois en utilisant un fichier de sommes de contrôle.
- Gardez à l'esprit que le hachage MD5 n'est pas sécurisé contre les collisions, donc pour des applications critiques, envisagez d'utiliser un algorithme de hachage plus fort comme SHA-256.