# [Linux] Bash pidstat Utilisation : Suivi des statistiques des processus

## Overview
La commande `pidstat` est utilisée pour surveiller les statistiques des processus en cours d'exécution sur un système Linux. Elle permet d'afficher des informations détaillées sur l'utilisation du CPU, de la mémoire et d'autres ressources pour chaque processus.

## Usage
La syntaxe de base de la commande `pidstat` est la suivante :

```bash
pidstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `pidstat` :

- `-h` : Affiche l'aide et les options disponibles.
- `-r` : Affiche l'utilisation de la mémoire.
- `-u` : Affiche l'utilisation du CPU par processus.
- `-p <pid>` : Spécifie un ou plusieurs identifiants de processus à surveiller.
- `-t` : Affiche les statistiques des threads.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `pidstat` :

1. Afficher l'utilisation du CPU par tous les processus :
   ```bash
   pidstat -u
   ```

2. Afficher l'utilisation de la mémoire pour tous les processus :
   ```bash
   pidstat -r
   ```

3. Surveiller un processus spécifique par son PID (par exemple, PID 1234) :
   ```bash
   pidstat -p 1234
   ```

4. Afficher les statistiques des threads pour un processus spécifique :
   ```bash
   pidstat -t -p 1234
   ```

5. Afficher les statistiques toutes les 5 secondes :
   ```bash
   pidstat 5
   ```

## Tips
- Utilisez l'option `-h` pour obtenir une aide rapide sur les options disponibles.
- Combinez les options pour obtenir des informations plus détaillées, par exemple, `pidstat -u -r` pour voir à la fois l'utilisation du CPU et de la mémoire.
- Pensez à rediriger la sortie vers un fichier pour une analyse ultérieure, par exemple : `pidstat -u > statistiques.txt`.