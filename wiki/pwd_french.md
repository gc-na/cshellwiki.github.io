# [Linux] C Shell (csh) pwd : Afficher le répertoire de travail actuel

## Overview
La commande `pwd` (print working directory) est utilisée dans le C Shell pour afficher le chemin complet du répertoire de travail actuel. C'est un outil essentiel pour naviguer dans le système de fichiers et comprendre votre position actuelle dans l'arborescence des répertoires.

## Usage
La syntaxe de base de la commande `pwd` est la suivante :

```
pwd [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `pwd` :

- `-L` : Affiche le chemin logique du répertoire de travail actuel.
- `-P` : Affiche le chemin physique, en résolvant les liens symboliques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `pwd` :

1. Afficher le répertoire de travail actuel :
   ```csh
   pwd
   ```

2. Afficher le chemin logique du répertoire de travail :
   ```csh
   pwd -L
   ```

3. Afficher le chemin physique du répertoire de travail :
   ```csh
   pwd -P
   ```

## Tips
- Utilisez `pwd` régulièrement pour vérifier votre position dans le système de fichiers, surtout avant d'exécuter des commandes qui dépendent du répertoire courant.
- Combinez `pwd` avec d'autres commandes pour créer des scripts utiles qui nécessitent la connaissance du chemin actuel.
- Si vous travaillez avec des liens symboliques, utilisez l'option `-P` pour obtenir le chemin réel du répertoire.