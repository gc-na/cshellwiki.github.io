# [Linux] C Shell (csh) cmp : Comparer des fichiers binaires

## Overview
La commande `cmp` est utilisée pour comparer deux fichiers binaires ou texte. Elle permet de déterminer si les fichiers sont identiques ou de localiser la première différence entre eux.

## Usage
La syntaxe de base de la commande `cmp` est la suivante :

```csh
cmp [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `cmp` :

- `-l` : Affiche les octets différents en format numérique.
- `-s` : Ne produit aucune sortie, mais renvoie un code de sortie indiquant si les fichiers sont identiques ou non.
- `-i` : Ignore les premiers N octets lors de la comparaison.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cmp` :

1. Comparer deux fichiers et afficher la première différence :
   ```csh
   cmp fichier1.txt fichier2.txt
   ```

2. Comparer deux fichiers sans afficher de sortie, juste le code de retour :
   ```csh
   cmp -s fichier1.bin fichier2.bin
   ```

3. Comparer deux fichiers et afficher tous les octets différents :
   ```csh
   cmp -l fichier1.bin fichier2.bin
   ```

4. Comparer deux fichiers en ignorant les premiers 10 octets :
   ```csh
   cmp -i 10 fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez l'option `-s` pour des comparaisons silencieuses lorsque vous souhaitez simplement savoir si les fichiers sont identiques sans afficher les différences.
- Pour des fichiers très volumineux, `cmp` est plus efficace que d'autres commandes comme `diff`, car il s'arrête dès qu'il trouve une différence.
- Pensez à utiliser `cmp` pour vérifier l'intégrité des fichiers après un transfert ou une sauvegarde.