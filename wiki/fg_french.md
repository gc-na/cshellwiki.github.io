# [Linux] Bash fg Utilisation : Ramener un processus au premier plan

## Overview
La commande `fg` est utilisée dans un environnement de terminal Bash pour ramener un processus qui s'exécute en arrière-plan au premier plan. Cela permet à l'utilisateur d'interagir directement avec le processus, par exemple, pour saisir des entrées ou pour voir les sorties en temps réel.

## Usage
La syntaxe de base de la commande `fg` est la suivante :

```bash
fg [options] [job_spec]
```

## Common Options
- `job_spec` : Spécifie le travail que vous souhaitez ramener au premier plan. Cela peut être un numéro de tâche ou un nom de processus.
- `%n` : Utilisé pour désigner un travail par son numéro (par exemple, `%1` pour le premier travail).
- `%string` : Utilisé pour désigner un travail par une chaîne de caractères qui correspond au nom du processus.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fg` :

1. **Ramener le dernier processus en arrière-plan au premier plan :**
   ```bash
   fg
   ```

2. **Ramener un processus spécifique au premier plan en utilisant son numéro de tâche :**
   ```bash
   fg %1
   ```

3. **Ramener un processus en utilisant une chaîne de caractères :**
   ```bash
   fg %mon_processus
   ```

4. **Si vous avez plusieurs processus en arrière-plan, vous pouvez les lister avec :**
   ```bash
   jobs
   ```
   Puis, utilisez `fg` avec le numéro de tâche approprié pour ramener le processus désiré.

## Tips
- Utilisez la commande `jobs` pour voir tous les processus en arrière-plan avant d'utiliser `fg`.
- Si vous souhaitez suspendre un processus en cours d'exécution au premier plan, utilisez `Ctrl + Z` pour le mettre en arrière-plan avant d'utiliser `fg`.
- Vous pouvez également utiliser `bg` pour continuer un processus en arrière-plan sans le ramener au premier plan.