# [Linux] Bash htop Utilisation : Afficher et gérer les processus en temps réel

## Overview
La commande `htop` est un visualiseur de processus interactif pour Unix. Contrairement à la commande `top`, `htop` offre une interface utilisateur plus conviviale et permet de gérer les processus de manière plus intuitive.

## Usage
La syntaxe de base de la commande `htop` est la suivante :

```bash
htop [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `htop` :

- `-h`, `--help` : Affiche l'aide et les options disponibles.
- `-s`, `--sort` : Permet de trier les processus par différents critères (par exemple, par utilisation CPU ou mémoire).
- `-p`, `--pid` : Affiche uniquement les processus avec les identifiants spécifiés.
- `-C`, `--no-color` : Démarre `htop` sans couleur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `htop` :

1. Lancer `htop` sans options :
   ```bash
   htop
   ```

2. Trier les processus par utilisation de la mémoire :
   ```bash
   htop -s MEM%
   ```

3. Afficher uniquement un processus spécifique par son PID (par exemple, PID 1234) :
   ```bash
   htop -p 1234
   ```

4. Démarrer `htop` sans couleur :
   ```bash
   htop -C
   ```

## Tips
- Utilisez les touches fléchées pour naviguer dans la liste des processus et `F9` pour tuer un processus sélectionné.
- Vous pouvez filtrer les processus en appuyant sur `F3` et en entrant un critère de recherche.
- Pour changer la priorité d'un processus, sélectionnez-le et appuyez sur `F7` pour augmenter la priorité ou `F8` pour la diminuer.