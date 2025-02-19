# [Linux] C Shell (csh) diff : Comparer des fichiers ligne par ligne

## Overview
La commande `diff` est utilisée pour comparer le contenu de deux fichiers ligne par ligne. Elle affiche les différences entre les fichiers, ce qui est particulièrement utile pour les développeurs et les administrateurs système qui souhaitent voir les modifications apportées à un fichier.

## Usage
La syntaxe de base de la commande `diff` est la suivante :

```csh
diff [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `diff` :

- `-u` : Affiche les différences en mode unifié, ce qui rend la sortie plus lisible.
- `-c` : Affiche les différences en mode contextuel, montrant un contexte autour des lignes modifiées.
- `-i` : Ignore la casse lors de la comparaison.
- `-w` : Ignore les espaces blancs lors de la comparaison.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `diff` :

1. Comparer deux fichiers texte :
   ```csh
   diff fichier1.txt fichier2.txt
   ```

2. Afficher les différences en mode unifié :
   ```csh
   diff -u fichier1.txt fichier2.txt
   ```

3. Comparer deux répertoires :
   ```csh
   diff -r repertoire1/ repertoire2/
   ```

4. Ignorer les espaces blancs :
   ```csh
   diff -w fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez l'option `-u` pour obtenir une sortie plus lisible, surtout si vous partagez les résultats avec d'autres.
- Pour une comparaison de répertoires, l'option `-r` est très utile pour voir toutes les différences dans les fichiers contenus.
- Pensez à rediriger la sortie de `diff` vers un fichier si vous avez besoin de conserver un enregistrement des différences :
  ```csh
  diff fichier1.txt fichier2.txt > differences.txt
  ```