# [Linux] Bash clear Utilisation : Effacer l'écran du terminal

## Overview
La commande `clear` est utilisée pour effacer le contenu affiché dans le terminal, offrant ainsi un écran propre pour une meilleure lisibilité. Cela peut être particulièrement utile lorsque vous travaillez avec de nombreuses lignes de texte ou lorsque vous souhaitez réduire le désordre visuel.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
clear [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `clear` :

- `-x` : Efface l'écran et empêche le défilement de l'historique.
- `-V` : Affiche la version de la commande `clear`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `clear` :

1. **Effacer l'écran du terminal :**
   ```bash
   clear
   ```

2. **Effacer l'écran sans permettre le défilement :**
   ```bash
   clear -x
   ```

3. **Afficher la version de la commande :**
   ```bash
   clear -V
   ```

## Tips
- Utilisez `clear` régulièrement pour garder votre terminal organisé, surtout lors de l'exécution de longues commandes ou scripts.
- Vous pouvez créer un alias dans votre fichier `.bashrc` pour simplifier l'utilisation de la commande, par exemple : `alias cls='clear'`.
- Si vous utilisez souvent `clear`, envisagez d'ajouter un raccourci clavier dans votre terminal pour un accès rapide.