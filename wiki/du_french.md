# [Linux] Bash du : afficher l'utilisation de l'espace disque

## Overview
La commande `du` (disk usage) est utilisée pour estimer et afficher l'utilisation de l'espace disque par les fichiers et les répertoires dans un système de fichiers. Elle permet aux utilisateurs de comprendre combien d'espace est occupé par chaque élément, facilitant ainsi la gestion de l'espace disque.

## Usage
La syntaxe de base de la commande `du` est la suivante :

```bash
du [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `du` :

- `-h` : Affiche la taille dans un format lisible par l'homme (Ko, Mo, Go).
- `-s` : Affiche uniquement le total pour chaque argument.
- `-a` : Affiche la taille de chaque fichier, pas seulement des répertoires.
- `-c` : Affiche un total cumulatif à la fin.
- `--max-depth=N` : Limite la profondeur d'affichage des sous-répertoires à N niveaux.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `du` :

1. Afficher l'utilisation de l'espace disque pour le répertoire courant :
   ```bash
   du -h
   ```

2. Afficher la taille totale d'un répertoire spécifique :
   ```bash
   du -sh /chemin/vers/repertoire
   ```

3. Afficher l'utilisation de l'espace disque pour tous les fichiers et répertoires dans un répertoire :
   ```bash
   du -ah /chemin/vers/repertoire
   ```

4. Afficher l'utilisation de l'espace disque avec un total cumulatif :
   ```bash
   du -ch /chemin/vers/repertoire/*
   ```

5. Limiter l'affichage à une profondeur de 1 niveau :
   ```bash
   du -h --max-depth=1 /chemin/vers/repertoire
   ```

## Tips
- Utilisez l'option `-h` pour rendre les résultats plus lisibles, surtout lorsque vous travaillez avec de grandes quantités de données.
- Combinez `du` avec d'autres commandes comme `sort` pour trier les résultats par taille :
  ```bash
  du -h /chemin/vers/repertoire | sort -hr
  ```
- Pensez à utiliser `du` avec `grep` pour filtrer des résultats spécifiques :
  ```bash
  du -h | grep "pattern"
  ```