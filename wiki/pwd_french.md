# [Linux] Bash pwd utilisation : Afficher le répertoire de travail actuel

## Overview
La commande `pwd` (print working directory) est utilisée dans Bash pour afficher le chemin absolu du répertoire de travail actuel. Cela permet aux utilisateurs de savoir où ils se trouvent dans la hiérarchie des fichiers.

## Usage
La syntaxe de base de la commande `pwd` est la suivante :

```bash
pwd [options]
```

## Common Options
Voici quelques options courantes pour la commande `pwd` :

- `-L` : Affiche le chemin logique du répertoire de travail actuel.
- `-P` : Affiche le chemin physique, en résolvant les liens symboliques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `pwd` :

1. Afficher le répertoire de travail actuel :
   ```bash
   pwd
   ```

2. Afficher le chemin logique du répertoire de travail :
   ```bash
   pwd -L
   ```

3. Afficher le chemin physique du répertoire de travail :
   ```bash
   pwd -P
   ```

## Tips
- Utilisez `pwd` régulièrement pour vérifier votre position dans le système de fichiers, surtout lorsque vous naviguez dans des répertoires complexes.
- Combinez `pwd` avec d'autres commandes comme `cd` pour une navigation efficace dans le terminal.
- Si vous utilisez des liens symboliques, n'oubliez pas de vérifier le chemin physique avec l'option `-P` pour éviter toute confusion.