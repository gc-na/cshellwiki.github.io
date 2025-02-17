# [Linux] Bash head utilisation : afficher les premières lignes d'un fichier

## Overview
La commande `head` est utilisée pour afficher les premières lignes d'un fichier texte. Par défaut, elle montre les 10 premières lignes, mais cela peut être modifié selon les besoins de l'utilisateur.

## Usage
La syntaxe de base de la commande `head` est la suivante :

```bash
head [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `head` :

- `-n [nombre]` : Affiche le nombre spécifié de lignes au lieu des 10 par défaut.
- `-c [nombre]` : Affiche le nombre spécifié de caractères au lieu de lignes.
- `-q` : Ne pas afficher les noms de fichiers lorsque plusieurs fichiers sont fournis.
- `-v` : Toujours afficher les noms de fichiers, même s'il n'y a qu'un seul fichier.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `head` :

1. Afficher les 10 premières lignes d'un fichier :

   ```bash
   head mon_fichier.txt
   ```

2. Afficher les 5 premières lignes d'un fichier :

   ```bash
   head -n 5 mon_fichier.txt
   ```

3. Afficher les 20 premiers caractères d'un fichier :

   ```bash
   head -c 20 mon_fichier.txt
   ```

4. Afficher les 10 premières lignes de plusieurs fichiers :

   ```bash
   head fichier1.txt fichier2.txt
   ```

5. Toujours afficher le nom du fichier avant les lignes :

   ```bash
   head -v mon_fichier.txt
   ```

## Tips
- Utilisez `head` en combinaison avec d'autres commandes, comme `grep`, pour filtrer les résultats avant d'afficher les premières lignes.
- Pour visualiser rapidement le contenu d'un fichier, `head` est souvent plus rapide que d'ouvrir le fichier dans un éditeur de texte.
- Pensez à utiliser l'option `-n` pour ajuster le nombre de lignes affichées selon vos besoins spécifiques.