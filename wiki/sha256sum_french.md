# [Linux] C Shell (csh) sha256sum : Calculer des sommes de contrôle SHA-256

## Overview
La commande `sha256sum` est utilisée pour calculer et vérifier les sommes de contrôle SHA-256 d'un fichier. Cela permet de garantir l'intégrité des données en s'assurant que le contenu d'un fichier n'a pas été modifié.

## Usage
La syntaxe de base de la commande `sha256sum` est la suivante :

```csh
sha256sum [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `sha256sum` :

- `-b` : Traite les fichiers en mode binaire.
- `-c` : Vérifie les sommes de contrôle à partir d'un fichier.
- `-o` : Écrit la sortie dans un fichier spécifié.
- `--quiet` : Ne produit aucune sortie sauf en cas d'erreur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `sha256sum` :

1. Calculer la somme de contrôle d'un fichier :
   ```csh
   sha256sum monfichier.txt
   ```

2. Vérifier la somme de contrôle à partir d'un fichier de sommes :
   ```csh
   sha256sum -c sommes.txt
   ```

3. Calculer la somme de contrôle d'un fichier et écrire la sortie dans un fichier :
   ```csh
   sha256sum monfichier.txt -o sortie.txt
   ```

4. Traiter un fichier en mode binaire :
   ```csh
   sha256sum -b monfichier.bin
   ```

## Tips
- Toujours vérifier les sommes de contrôle après le téléchargement de fichiers importants pour s'assurer qu'ils n'ont pas été corrompus.
- Utilisez l'option `-c` pour automatiser la vérification des fichiers en utilisant un fichier de sommes de contrôle.
- Gardez une copie des fichiers de sommes de contrôle pour une vérification future.