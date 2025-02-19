# [Linux] C Shell (csh) à at : [planifier des tâches]

## Overview
La commande `at` permet de planifier l'exécution de commandes ou de scripts à un moment précis dans le futur. Elle est utile pour automatiser des tâches sans avoir besoin de rester connecté à la session.

## Usage
La syntaxe de base de la commande `at` est la suivante :

```
at [options] [arguments]
```

## Common Options
- `-f <file>` : Spécifie un fichier contenant les commandes à exécuter.
- `-m` : Envoie un e-mail à l'utilisateur lorsque la tâche est terminée.
- `-q <queue>` : Définit la file d'attente à utiliser pour la tâche.
- `-l` : Liste les tâches planifiées pour l'utilisateur courant.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `at` :

1. **Planifier une commande simple :**
   Pour exécuter la commande `echo "Hello World"` à 15h00 aujourd'hui :
   ```bash
   echo "echo 'Hello World'" | at 15:00
   ```

2. **Utiliser un fichier de commandes :**
   Si vous avez un fichier `script.sh` que vous souhaitez exécuter demain à 9h00 :
   ```bash
   at -f script.sh 09:00 tomorrow
   ```

3. **Envoyer un e-mail après l'exécution :**
   Pour exécuter une commande et recevoir un e-mail une fois terminée :
   ```bash
   echo "backup.sh" | at -m 02:00
   ```

4. **Lister les tâches planifiées :**
   Pour voir toutes les tâches que vous avez planifiées :
   ```bash
   at -l
   ```

## Tips
- Assurez-vous que le service `atd` est en cours d'exécution sur votre système pour que les tâches planifiées s'exécutent.
- Utilisez des horaires clairs et précis pour éviter toute confusion sur le moment où les tâches doivent s'exécuter.
- Pensez à vérifier régulièrement vos tâches planifiées avec `at -l` pour éviter d'avoir des tâches obsolètes.