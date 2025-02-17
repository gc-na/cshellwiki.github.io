# [Linux] Bash @ Utilisation : Exécuter des commandes en arrière-plan

## Overview
La commande `@` permet d'exécuter des commandes en arrière-plan dans un terminal Bash. Cela permet de libérer le terminal pour d'autres tâches tout en laissant une commande s'exécuter sans interruption.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
@ [options] [arguments]
```

## Common Options
- `&` : Exécute la commande en arrière-plan.
- `disown` : Supprime un travail de la liste des travaux, permettant à la commande de continuer à s'exécuter même après la fermeture du terminal.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `@` :

1. Exécuter un script en arrière-plan :
   ```bash
   ./mon_script.sh &
   ```

2. Lancer un serveur web en arrière-plan :
   ```bash
   python -m http.server 8000 &
   ```

3. Exécuter une commande longue et la détacher :
   ```bash
   long_running_command &
   disown
   ```

4. Exécuter plusieurs commandes en arrière-plan :
   ```bash
   command1 & command2 &
   ```

## Tips
- Utilisez `jobs` pour voir les tâches en cours d'exécution en arrière-plan.
- Pour ramener une tâche en arrière-plan au premier plan, utilisez `fg %n`, où `n` est le numéro de la tâche.
- Pensez à utiliser `nohup` pour éviter que la commande ne soit arrêtée lorsque vous fermez le terminal.