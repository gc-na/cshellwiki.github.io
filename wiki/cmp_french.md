# [Linux] Bash cmp utilisation : Comparer des fichiers byte par byte

## Overview
La commande `cmp` est utilisée pour comparer deux fichiers byte par byte. Elle permet de déterminer si les fichiers sont identiques ou de localiser la première différence entre eux.

## Usage
La syntaxe de base de la commande `cmp` est la suivante :

```bash
cmp [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `cmp` :

- `-l` : Affiche les octets différents en format numérique.
- `-s` : Ne produit aucune sortie, mais renvoie un code de sortie indiquant si les fichiers sont identiques ou non.
- `-i OFFSET` : Ignore les premiers OFFSET octets de chaque fichier.
- `-n N` : Compare seulement les premiers N octets des fichiers.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cmp` :

1. Comparer deux fichiers et afficher la première différence :
   ```bash
   cmp fichier1.txt fichier2.txt
   ```

2. Comparer deux fichiers sans afficher de sortie, juste le code de sortie :
   ```bash
   cmp -s fichier1.txt fichier2.txt
   ```

3. Afficher les octets différents entre deux fichiers :
   ```bash
   cmp -l fichier1.txt fichier2.txt
   ```

4. Comparer seulement les 10 premiers octets de deux fichiers :
   ```bash
   cmp -n 10 fichier1.txt fichier2.txt
   ```

5. Ignorer les 5 premiers octets lors de la comparaison :
   ```bash
   cmp -i 5 fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez l'option `-s` pour des scripts automatisés où vous n'avez besoin que du code de sortie.
- Pour des fichiers binaires, l'option `-l` peut être très utile pour identifier les différences précises.
- Pensez à rediriger la sortie vers un fichier si vous comparez de grands fichiers et que vous souhaitez conserver un enregistrement des différences.