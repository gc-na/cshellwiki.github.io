# [Linux] Bash tput Utilisation : Contrôle des terminaux

## Overview
La commande `tput` est utilisée pour initialiser ou interroger les capacités d'un terminal. Elle permet de manipuler l'affichage dans le terminal en utilisant des séquences d'échappement, ce qui est particulièrement utile pour créer des interfaces utilisateur textuelles.

## Usage
La syntaxe de base de la commande `tput` est la suivante :

```bash
tput [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `tput` :

- `clear` : Efface l'écran du terminal.
- `setaf [n]` : Définit la couleur de premier plan (texte) à la couleur indexée `n`.
- `setab [n]` : Définit la couleur de fond à la couleur indexée `n`.
- `cup [x] [y]` : Déplace le curseur à la position (x, y) dans le terminal.
- `bold` : Définit le texte en gras.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tput` :

1. **Effacer l'écran :**
   ```bash
   tput clear
   ```

2. **Changer la couleur du texte :**
   ```bash
   tput setaf 1  # Définit le texte en rouge
   echo "Ceci est un texte rouge."
   tput sgr0     # Réinitialise les attributs du texte
   ```

3. **Déplacer le curseur :**
   ```bash
   tput cup 10 20  # Déplace le curseur à la ligne 10, colonne 20
   echo "Texte à une position spécifique."
   ```

4. **Texte en gras :**
   ```bash
   tput bold
   echo "Ceci est un texte en gras."
   tput sgr0
   ```

## Tips
- Utilisez `tput sgr0` après avoir appliqué des attributs pour réinitialiser les styles, afin d'éviter que les changements ne s'appliquent à d'autres textes.
- Vous pouvez combiner plusieurs commandes `tput` pour créer des affichages plus complexes et interactifs.
- Testez les différentes couleurs disponibles en utilisant `tput setaf` et `tput setab` avec des indices de couleur allant généralement de 0 à 7 pour les couleurs de base.