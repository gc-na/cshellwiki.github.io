# [Linux] C Shell (csh) crontab : Planifier des tâches automatisées

## Overview
La commande `crontab` permet de planifier des tâches automatisées dans le système d'exploitation Unix/Linux. Elle permet aux utilisateurs de spécifier des commandes à exécuter à des intervalles réguliers, facilitant ainsi l'automatisation de diverses tâches.

## Usage
La syntaxe de base de la commande `crontab` est la suivante :

```bash
crontab [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `crontab` :

- `-e` : Éditer le fichier crontab de l'utilisateur.
- `-l` : Lister les tâches planifiées de l'utilisateur.
- `-r` : Supprimer le fichier crontab de l'utilisateur.
- `-i` : Demander une confirmation avant de supprimer le crontab.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `crontab` :

1. **Éditer le crontab :**
   Pour ouvrir l'éditeur de texte et modifier le crontab :
   ```bash
   crontab -e
   ```

2. **Lister les tâches planifiées :**
   Pour afficher toutes les tâches cron de l'utilisateur :
   ```bash
   crontab -l
   ```

3. **Supprimer le crontab :**
   Pour supprimer toutes les tâches cron de l'utilisateur avec confirmation :
   ```bash
   crontab -r -i
   ```

4. **Planifier une tâche :**
   Pour exécuter un script tous les jours à 2h du matin, ajoutez la ligne suivante dans le crontab :
   ```bash
   0 2 * * * /chemin/vers/script.sh
   ```

5. **Planifier une tâche chaque lundi à 5h :**
   Pour exécuter une commande tous les lundis à 5h du matin :
   ```bash
   0 5 * * 1 /chemin/vers/commande
   ```

## Tips
- Assurez-vous que les chemins des scripts ou des commandes sont absolus pour éviter des erreurs d'exécution.
- Vérifiez régulièrement votre crontab pour vous assurer que les tâches sont toujours nécessaires et fonctionnent correctement.
- Utilisez des fichiers de log pour suivre l'exécution de vos tâches cron, ce qui peut aider à diagnostiquer des problèmes.