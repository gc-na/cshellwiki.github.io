# [Linux] Bash fold usage : Plier le texte à une largeur spécifiée

## Overview
La commande `fold` est utilisée pour plier le texte à une largeur spécifiée. Elle permet de formater le texte en ajoutant des retours à la ligne afin que chaque ligne ne dépasse pas un certain nombre de caractères, ce qui est particulièrement utile pour l'affichage sur des terminaux ou pour la préparation de fichiers texte.

## Usage
La syntaxe de base de la commande `fold` est la suivante :

```bash
fold [options] [arguments]
```

## Common Options
- `-w, --width=N` : Définit la largeur maximale des lignes à N caractères.
- `-s, --spaces` : Plie le texte en respectant les espaces, ce qui signifie qu'il ne coupera pas les mots à la fin d'une ligne.
- `-b, --bytes` : Compte la largeur en octets au lieu de caractères, ce qui peut être utile pour les fichiers contenant des caractères multibytes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fold` :

1. Plier un fichier texte à une largeur de 50 caractères :
   ```bash
   fold -w 50 mon_fichier.txt
   ```

2. Plier le texte d'une entrée standard (stdin) à 30 caractères, en respectant les espaces :
   ```bash
   echo "Ceci est un exemple de texte qui sera plié." | fold -s -w 30
   ```

3. Plier un fichier texte et rediriger la sortie vers un nouveau fichier :
   ```bash
   fold -w 60 mon_fichier.txt > fichier_plie.txt
   ```

4. Plier le texte tout en comptant les octets :
   ```bash
   fold -b -w 40 mon_fichier.txt
   ```

## Tips
- Utilisez l'option `-s` pour éviter de couper les mots à la fin des lignes, ce qui rend le texte plus lisible.
- Testez différentes largeurs pour voir ce qui fonctionne le mieux pour votre affichage ou votre formatage.
- Combinez `fold` avec d'autres commandes comme `cat` ou `less` pour un affichage amélioré de fichiers texte longs.