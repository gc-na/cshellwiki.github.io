# [Linux] Bash nohup Utilisation : Exécuter des commandes sans interruption

## Overview
La commande `nohup` (no hang up) permet d'exécuter des processus en arrière-plan, même si la session terminal est fermée. Cela est particulièrement utile pour les tâches longues qui ne doivent pas être interrompues par la déconnexion de l'utilisateur.

## Usage
La syntaxe de base de la commande `nohup` est la suivante :

```bash
nohup [options] [arguments]
```

## Common Options
- `&` : Exécute la commande en arrière-plan.
- `-o` : Spécifie un fichier de sortie pour les messages de la commande.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `nohup` :

1. Exécuter un script en arrière-plan :
   ```bash
   nohup ./mon_script.sh &
   ```

2. Exécuter une commande avec sortie redirigée vers un fichier :
   ```bash
   nohup ls -l > sortie.txt &
   ```

3. Exécuter un serveur web en arrière-plan :
   ```bash
   nohup python -m http.server 8000 &
   ```

4. Exécuter une tâche cron personnalisée sans interruption :
   ```bash
   nohup bash -c 'while true; do echo "Tâche en cours"; sleep 60; done' &
   ```

## Tips
- Utilisez `jobs` pour vérifier les processus en arrière-plan.
- Redirigez la sortie d'erreur en utilisant `2>` pour capturer les erreurs dans un fichier.
- Pensez à utiliser `disown` après avoir mis une tâche en arrière-plan pour éviter qu'elle ne soit tuée lors de la fermeture du terminal.