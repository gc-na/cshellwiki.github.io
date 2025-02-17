# [Linux] Bash jobs Utilisation : Gérer les tâches en arrière-plan

## Overview
La commande `jobs` en Bash est utilisée pour afficher les tâches en cours d'exécution dans le shell actuel. Elle permet de visualiser les processus qui s'exécutent en arrière-plan ou qui sont suspendus, ce qui est particulièrement utile lors de la gestion de plusieurs tâches simultanément.

## Usage
La syntaxe de base de la commande `jobs` est la suivante :

```bash
jobs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `jobs` :

- `-l` : Affiche les numéros de processus (PID) avec la liste des tâches.
- `-n` : Affiche uniquement les tâches qui ont changé d'état depuis la dernière exécution de la commande.
- `-p` : Affiche uniquement les numéros de processus des tâches.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `jobs` :

1. **Afficher toutes les tâches en cours :**

   ```bash
   jobs
   ```

2. **Afficher les tâches avec les numéros de processus :**

   ```bash
   jobs -l
   ```

3. **Afficher uniquement les tâches qui ont changé d'état :**

   ```bash
   jobs -n
   ```

4. **Afficher uniquement les numéros de processus des tâches :**

   ```bash
   jobs -p
   ```

## Tips
- Utilisez `bg` pour reprendre une tâche suspendue en arrière-plan après avoir utilisé `Ctrl+Z` pour la suspendre.
- Utilisez `fg` pour ramener une tâche en arrière-plan au premier plan.
- Vérifiez régulièrement l'état de vos tâches avec `jobs` pour éviter d'avoir trop de processus en cours d'exécution.