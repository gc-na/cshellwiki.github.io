# [Linux] Bash top : Afficher les processus en temps réel

## Overview
La commande `top` est un outil puissant qui permet de surveiller en temps réel les processus en cours d'exécution sur un système Linux. Elle fournit des informations détaillées sur l'utilisation du processeur, de la mémoire et d'autres ressources système, ce qui en fait un outil essentiel pour le diagnostic et l'optimisation des performances.

## Usage
La syntaxe de base de la commande `top` est la suivante :

```bash
top [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec la commande `top` :

- `-d <seconds>` : Définit l'intervalle de mise à jour en secondes.
- `-p <pid>` : Affiche uniquement le processus avec l'identifiant de processus spécifié.
- `-u <user>` : Affiche uniquement les processus appartenant à l'utilisateur spécifié.
- `-n <number>` : Exécute `top` pour un nombre spécifique de mises à jour avant de quitter.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `top` :

1. Lancer `top` avec les valeurs par défaut :
   ```bash
   top
   ```

2. Afficher les processus avec une mise à jour toutes les 5 secondes :
   ```bash
   top -d 5
   ```

3. Filtrer pour afficher uniquement les processus d'un utilisateur spécifique :
   ```bash
   top -u nom_utilisateur
   ```

4. Afficher un processus spécifique par son PID :
   ```bash
   top -p 1234
   ```

5. Exécuter `top` pour 10 mises à jour avant de quitter :
   ```bash
   top -n 10
   ```

## Tips
- Utilisez la touche `h` pendant que `top` est en cours d'exécution pour afficher l'aide intégrée et découvrir d'autres fonctionnalités.
- Vous pouvez trier les processus par différentes colonnes en appuyant sur les touches correspondantes (par exemple, `P` pour le tri par utilisation du processeur).
- Pour quitter `top`, appuyez simplement sur `q`.
- Pensez à utiliser `htop`, une alternative plus conviviale à `top`, qui offre une interface colorée et des fonctionnalités supplémentaires.