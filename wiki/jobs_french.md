# [Linux] C Shell (csh) jobs : gérer les tâches en arrière-plan

## Overview
La commande `jobs` dans C Shell (csh) permet de lister les tâches en cours d'exécution dans le shell, qu'elles soient en arrière-plan ou suspendues. Cela aide les utilisateurs à gérer et à surveiller les processus qu'ils ont lancés.

## Usage
La syntaxe de base de la commande est la suivante :

```
jobs [options] [arguments]
```

## Common Options
- `-l` : Affiche les numéros de processus (PID) en plus des informations sur les tâches.
- `-n` : Affiche uniquement les tâches qui ont changé d'état depuis la dernière exécution de la commande.
- `-p` : Affiche uniquement les numéros de processus des tâches.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `jobs` :

1. **Lister toutes les tâches en cours :**
   ```csh
   jobs
   ```

2. **Lister les tâches avec les PID :**
   ```csh
   jobs -l
   ```

3. **Afficher uniquement les tâches qui ont changé d'état :**
   ```csh
   jobs -n
   ```

4. **Afficher uniquement les PID des tâches :**
   ```csh
   jobs -p
   ```

## Tips
- Utilisez `bg` pour reprendre une tâche suspendue en arrière-plan après avoir utilisé `Ctrl+Z`.
- Vous pouvez utiliser `fg %n` pour ramener une tâche en avant-plan, où `n` est le numéro de la tâche.
- Vérifiez régulièrement l'état de vos tâches avec `jobs` pour éviter d'avoir trop de processus en arrière-plan qui pourraient consommer des ressources.