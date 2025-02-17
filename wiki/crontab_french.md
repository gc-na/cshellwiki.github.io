# [Linux] Bash crontab utilisation : Planification des tâches

## Overview
La commande `crontab` permet de gérer les tâches planifiées sur un système Unix/Linux. Elle permet aux utilisateurs de spécifier des commandes qui seront exécutées automatiquement à des intervalles réguliers, ce qui est particulièrement utile pour l'automatisation des tâches répétitives.

## Usage
La syntaxe de base de la commande `crontab` est la suivante :

```bash
crontab [options] [arguments]
```

## Common Options
- `-e` : Édite le fichier crontab de l'utilisateur courant.
- `-l` : Affiche le contenu du fichier crontab de l'utilisateur courant.
- `-r` : Supprime le fichier crontab de l'utilisateur courant.
- `-i` : Demande une confirmation avant de supprimer le crontab.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `crontab` :

### 1. Éditer le crontab
Pour ouvrir le fichier crontab de l'utilisateur courant et y ajouter ou modifier des tâches :
```bash
crontab -e
```

### 2. Lister les tâches planifiées
Pour afficher toutes les tâches planifiées dans le crontab :
```bash
crontab -l
```

### 3. Supprimer le crontab
Pour supprimer toutes les tâches planifiées de l'utilisateur courant :
```bash
crontab -r
```

### 4. Planifier une tâche
Pour exécuter un script tous les jours à 2h du matin, ajoutez la ligne suivante dans le crontab :
```bash
0 2 * * * /chemin/vers/le/script.sh
```

### 5. Planifier une tâche chaque minute
Pour exécuter une commande chaque minute :
```bash
* * * * * /chemin/vers/la/commande
```

## Tips
- Utilisez `crontab -l > backup_crontab.txt` pour sauvegarder votre crontab avant de faire des modifications.
- Assurez-vous que les chemins des scripts ou des commandes soient absolus pour éviter des erreurs d'exécution.
- Vérifiez les logs de cron (généralement dans `/var/log/syslog` ou `/var/log/cron`) pour déboguer les tâches qui ne s'exécutent pas comme prévu.