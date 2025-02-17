# [Linux] Bash diff utilisation : Comparer des fichiers ligne par ligne

## Overview
La commande `diff` est utilisée pour comparer le contenu de deux fichiers ligne par ligne. Elle affiche les différences entre les fichiers, ce qui est particulièrement utile pour le développement de logiciels, la gestion de versions et la révision de documents.

## Usage
La syntaxe de base de la commande `diff` est la suivante :

```bash
diff [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `diff` :

- `-u` : Affiche les différences en format unifié, ce qui est plus lisible.
- `-c` : Affiche les différences en format contextuel, fournissant plus de contexte autour des changements.
- `-i` : Ignore la casse lors de la comparaison.
- `-w` : Ignore les espaces blancs lors de la comparaison.
- `-r` : Compare les répertoires de manière récursive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `diff` :

### Comparer deux fichiers texte
```bash
diff fichier1.txt fichier2.txt
```

### Comparer deux fichiers avec un format unifié
```bash
diff -u fichier1.txt fichier2.txt
```

### Comparer deux répertoires
```bash
diff -r dossier1/ dossier2/
```

### Ignorer les espaces blancs
```bash
diff -w fichier1.txt fichier2.txt
```

### Afficher les différences en format contextuel
```bash
diff -c fichier1.txt fichier2.txt
```

## Tips
- Utilisez l'option `-u` pour obtenir un affichage plus clair des différences, surtout lors de la révision de code.
- Lorsque vous travaillez avec des fichiers de code, envisagez d'utiliser `diff` avec des outils de contrôle de version comme Git pour une gestion plus efficace des modifications.
- Pour une comparaison visuelle, vous pouvez rediriger la sortie de `diff` vers un fichier et l'ouvrir avec un éditeur de texte.