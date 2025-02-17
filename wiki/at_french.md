# [Linux] Bash à at : Planifier des tâches à exécuter

## Overview
La commande `at` permet de planifier l'exécution de commandes ou de scripts à un moment précis dans le futur. C'est un outil pratique pour automatiser des tâches sans avoir à rester connecté à la session.

## Usage
La syntaxe de base de la commande `at` est la suivante :

```bash
at [options] [arguments]
```

## Common Options
- `-f` : Spécifie un fichier contenant les commandes à exécuter.
- `-m` : Envoie un e-mail à l'utilisateur lorsque la tâche est terminée.
- `-q` : Définit la file d'attente pour la tâche.
- `-l` : Liste les tâches planifiées.
- `-d` : Supprime une tâche planifiée.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `at` :

1. **Planifier une commande pour exécution dans 5 minutes :**
   ```bash
   echo "echo 'Hello, World!'" | at now + 5 minutes
   ```

2. **Exécuter un script à une heure précise :**
   ```bash
   at 14:00 < /path/to/script.sh
   ```

3. **Planifier une tâche pour demain à 10h :**
   ```bash
   echo "backup.sh" | at 10:00 tomorrow
   ```

4. **Lister les tâches planifiées :**
   ```bash
   at -l
   ```

5. **Supprimer une tâche planifiée :**
   ```bash
   at -d 1
   ```

## Tips
- Assurez-vous que le service `atd` est en cours d'exécution pour que les tâches planifiées s'exécutent correctement.
- Utilisez l'option `-m` pour recevoir une notification par e-mail une fois la tâche terminée.
- Pour des tâches récurrentes, envisagez d'utiliser `cron`, qui est plus adapté pour les répétitions régulières.