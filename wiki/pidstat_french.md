# [Linux] C Shell (csh) pidstat : [surveiller l'utilisation des ressources des processus]

## Overview
La commande `pidstat` est un outil puissant qui permet de surveiller l'utilisation des ressources des processus en cours d'exécution sur un système. Elle fournit des informations détaillées sur l'utilisation du CPU, de la mémoire et d'autres métriques essentielles pour chaque processus.

## Usage
La syntaxe de base de la commande `pidstat` est la suivante :

```bash
pidstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `pidstat` :

- `-h` : Affiche l'en-tête des colonnes.
- `-r` : Affiche l'utilisation de la mémoire.
- `-u` : Affiche l'utilisation du CPU.
- `-p <pid>` : Spécifie le PID du processus à surveiller.
- `-t` : Affiche les threads du processus.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `pidstat` :

1. **Surveiller l'utilisation du CPU de tous les processus :**
   ```bash
   pidstat -u
   ```

2. **Surveiller l'utilisation de la mémoire pour tous les processus :**
   ```bash
   pidstat -r
   ```

3. **Surveiller un processus spécifique par son PID :**
   ```bash
   pidstat -p 1234
   ```

4. **Surveiller les threads d'un processus :**
   ```bash
   pidstat -t -p 1234
   ```

5. **Afficher les statistiques toutes les 5 secondes :**
   ```bash
   pidstat 5
   ```

## Tips
- Utilisez l'option `-h` pour rendre la sortie plus lisible en affichant les en-têtes des colonnes.
- Combinez les options `-u` et `-r` pour obtenir une vue d'ensemble complète de l'utilisation des ressources.
- Pour une surveillance continue, envisagez d'utiliser `pidstat` avec un intervalle de temps pour observer les tendances d'utilisation des ressources.