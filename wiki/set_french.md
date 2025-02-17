# [Linux] Bash set : Configurer les options de l'environnement de shell

## Overview
La commande `set` en Bash est utilisée pour définir ou modifier les options de l'environnement du shell. Elle permet de contrôler le comportement du shell et de gérer les variables d'environnement.

## Usage
La syntaxe de base de la commande `set` est la suivante :

```bash
set [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `set` :

- `-e` : Arrête l'exécution si une commande échoue.
- `-u` : Traite les variables non définies comme des erreurs.
- `-x` : Affiche chaque commande avant son exécution, utile pour le débogage.
- `-o` : Permet de définir des options spécifiques, comme `-o noclobber` pour empêcher l'écrasement des fichiers.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `set` :

1. **Arrêter l'exécution en cas d'erreur :**
   ```bash
   set -e
   ```
   Cela signifie que si une commande échoue, le script s'arrête immédiatement.

2. **Activer le débogage :**
   ```bash
   set -x
   ```
   Cela affichera chaque commande exécutée, ce qui est utile pour le débogage.

3. **Traiter les variables non définies comme erreurs :**
   ```bash
   set -u
   ```
   Cela renvoie une erreur si une variable non définie est utilisée.

4. **Combiner plusieurs options :**
   ```bash
   set -e -u -x
   ```
   Cela active les trois options simultanément pour un meilleur contrôle du script.

## Tips
- Utilisez `set -e` pour éviter que des erreurs passent inaperçues dans vos scripts.
- Activez `set -u` pour vous assurer que toutes les variables utilisées sont définies, ce qui peut aider à éviter des comportements inattendus.
- Pour le débogage, `set -x` est très utile, mais n'oubliez pas de le désactiver une fois que vous avez terminé le débogage pour éviter d'afficher des informations sensibles.