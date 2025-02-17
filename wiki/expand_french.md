# [Linux] Bash expand utilisation : Convertir les tabulations en espaces

## Overview
La commande `expand` est utilisée pour convertir les tabulations en espaces dans un fichier texte. Cela permet d'uniformiser le formatage du texte, ce qui est particulièrement utile lors de la préparation de fichiers pour des affichages ou des traitements ultérieurs.

## Usage
La syntaxe de base de la commande `expand` est la suivante :

```bash
expand [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `expand` :

- `-t, --tabs=N` : Définit le nombre d'espaces pour chaque tabulation (par défaut, 8).
- `-i, --initial` : Convertit uniquement les tabulations qui apparaissent après le début de la ligne.
- `-n, --no-tabs` : Ne pas convertir les tabulations en espaces, mais afficher le texte tel quel.
- `-h, --help` : Affiche l'aide et les options disponibles pour la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `expand` :

1. **Convertir un fichier avec des tabulations en espaces :**

```bash
expand fichier.txt > fichier_converti.txt
```

2. **Définir un nombre différent d'espaces pour les tabulations :**

```bash
expand -t 4 fichier.txt > fichier_converti.txt
```

3. **Convertir uniquement les tabulations après le début de la ligne :**

```bash
expand -i fichier.txt > fichier_converti.txt
```

4. **Afficher le contenu sans conversion :**

```bash
expand -n fichier.txt
```

## Tips
- Utilisez l'option `-t` pour personnaliser le nombre d'espaces selon vos besoins spécifiques.
- Combinez `expand` avec d'autres commandes comme `cat` pour visualiser les résultats directement dans le terminal.
- Pensez à rediriger la sortie vers un nouveau fichier pour conserver l'original intact.