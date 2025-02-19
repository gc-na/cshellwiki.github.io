# [Linux] C Shell (csh) tput : Contrôler les capacités du terminal

## Overview
La commande `tput` est utilisée pour initialiser et contrôler les capacités d'affichage d'un terminal. Elle permet d'envoyer des séquences d'échappement au terminal pour modifier son comportement, comme changer la couleur du texte ou déplacer le curseur.

## Usage
La syntaxe de base de la commande `tput` est la suivante :

```csh
tput [options] [arguments]
```

## Common Options
- `clear` : Efface l'écran du terminal.
- `setaf [n]` : Définit la couleur du texte (où `n` est le numéro de la couleur).
- `setab [n]` : Définit la couleur de fond (où `n` est le numéro de la couleur).
- `cup [x] [y]` : Déplace le curseur à la position spécifiée (ligne `x`, colonne `y`).
- `bold` : Active le texte en gras.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tput` :

1. **Effacer l'écran :**
   ```csh
   tput clear
   ```

2. **Changer la couleur du texte en rouge :**
   ```csh
   tput setaf 1
   echo "Ce texte est rouge"
   ```

3. **Changer la couleur de fond en bleu :**
   ```csh
   tput setab 4
   echo "Le fond est bleu"
   ```

4. **Déplacer le curseur :**
   ```csh
   tput cup 10 20
   echo "Je suis à la ligne 10, colonne 20"
   ```

5. **Activer le texte en gras :**
   ```csh
   tput bold
   echo "Ce texte est en gras"
   ```

## Tips
- Utilisez `tput reset` pour réinitialiser le terminal à ses paramètres par défaut.
- Combinez plusieurs commandes `tput` pour créer des affichages plus complexes.
- Testez les numéros de couleur disponibles sur votre terminal, car ils peuvent varier selon les configurations.