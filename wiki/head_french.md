# [Linux] C Shell (csh) head : Afficher les premières lignes d'un fichier

## Overview
La commande `head` est utilisée pour afficher les premières lignes d'un fichier texte. Par défaut, elle montre les 10 premières lignes, mais cela peut être modifié en fonction des besoins de l'utilisateur.

## Usage
La syntaxe de base de la commande `head` est la suivante :

```
head [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `head` :

- `-n [nombre]` : Affiche le nombre spécifié de lignes à partir du début du fichier.
- `-c [nombre]` : Affiche le nombre spécifié de caractères à partir du début du fichier.
- `-q` : Ne pas afficher les noms des fichiers lorsque plusieurs fichiers sont fournis.
- `-v` : Affiche le nom du fichier avant son contenu.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `head` :

1. Afficher les 10 premières lignes d'un fichier :
   ```bash
   head fichier.txt
   ```

2. Afficher les 5 premières lignes d'un fichier :
   ```bash
   head -n 5 fichier.txt
   ```

3. Afficher les 20 premiers caractères d'un fichier :
   ```bash
   head -c 20 fichier.txt
   ```

4. Afficher les 10 premières lignes de plusieurs fichiers :
   ```bash
   head fichier1.txt fichier2.txt
   ```

5. Afficher le nom du fichier avant son contenu :
   ```bash
   head -v fichier.txt
   ```

## Tips
- Utilisez `head` en combinaison avec d'autres commandes, comme `grep`, pour filtrer les résultats avant d'afficher les premières lignes.
- Pour une visualisation rapide, `head` est très utile lors de l'examen de fichiers volumineux sans avoir à les ouvrir entièrement.
- Pensez à utiliser l'option `-n` pour ajuster le nombre de lignes affichées selon vos besoins spécifiques.