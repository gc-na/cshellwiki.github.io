# [Linux] C Shell (csh) fmt <Utilisation équivalente>: Formater le texte

## Overview
La commande `fmt` est utilisée pour reformater le texte en ajustant la largeur des lignes. Elle est particulièrement utile pour rendre le texte plus lisible en évitant les lignes trop longues.

## Usage
La syntaxe de base de la commande `fmt` est la suivante :

```csh
fmt [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `fmt` :

- `-w <largeur>` : Définit la largeur maximale des lignes (par défaut, 72 caractères).
- `-s` : Supprime les lignes vides supplémentaires.
- `-u` : Utilise un formatage unifié, ce qui signifie que les lignes sont justifiées à gauche.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fmt` :

1. Reformater un fichier texte avec la largeur par défaut :

   ```csh
   fmt mon_fichier.txt
   ```

2. Spécifier une largeur de 50 caractères :

   ```csh
   fmt -w 50 mon_fichier.txt
   ```

3. Supprimer les lignes vides supplémentaires :

   ```csh
   fmt -s mon_fichier.txt
   ```

4. Justifier le texte à gauche :

   ```csh
   fmt -u mon_fichier.txt
   ```

## Tips
- Utilisez `fmt` en combinaison avec d'autres commandes comme `cat` ou `more` pour visualiser le texte formaté directement dans le terminal.
- Pour appliquer `fmt` à plusieurs fichiers, vous pouvez les lister tous dans la commande, par exemple : `fmt fichier1.txt fichier2.txt`.
- Si vous souhaitez sauvegarder le texte formaté dans un nouveau fichier, vous pouvez rediriger la sortie : `fmt mon_fichier.txt > fichier_formaté.txt`.