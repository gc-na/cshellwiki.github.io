# [Linux] Bash fmt Utilisation : Reformater le texte

## Overview
La commande `fmt` est utilisée pour reformater le texte en ajustant la largeur des lignes. Elle est particulièrement utile pour rendre le texte plus lisible en s'assurant que les lignes ne dépassent pas une certaine longueur.

## Usage
La syntaxe de base de la commande `fmt` est la suivante :

```bash
fmt [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `fmt` :

- `-w [largeur]` : Définit la largeur maximale des lignes (par défaut, 75 caractères).
- `-s` : Supprime les lignes vides supplémentaires.
- `-u` : Supprime les espaces supplémentaires entre les mots.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fmt` :

1. Reformater un fichier texte avec la largeur par défaut :

   ```bash
   fmt mon_fichier.txt
   ```

2. Reformater un fichier texte avec une largeur de 50 caractères :

   ```bash
   fmt -w 50 mon_fichier.txt
   ```

3. Supprimer les lignes vides supplémentaires d'un fichier :

   ```bash
   fmt -s mon_fichier.txt
   ```

4. Reformater un texte en ligne de commande :

   ```bash
   echo "Ceci est un exemple de texte qui sera reformatté." | fmt
   ```

## Tips
- Utilisez l'option `-w` pour ajuster la largeur selon vos besoins spécifiques.
- Combinez `fmt` avec d'autres commandes comme `cat` ou `echo` pour traiter le texte en temps réel.
- Vérifiez le contenu de votre fichier avant et après le formatage pour vous assurer que le résultat est conforme à vos attentes.