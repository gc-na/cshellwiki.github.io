# [Linux] Bash write usage : envoyer des messages à d'autres utilisateurs

## Overview
La commande `write` permet d'envoyer des messages en temps réel à d'autres utilisateurs connectés sur le même système. C'est un outil simple et efficace pour communiquer directement avec quelqu'un d'autre sur un terminal.

## Usage
La syntaxe de base de la commande `write` est la suivante :

```bash
write [options] [utilisateur] [terminal]
```

## Common Options
- `-n` : Ne pas afficher le nom de l'utilisateur qui envoie le message.
- `-s` : Mode silencieux, n'affiche pas les messages d'état.
- `-h` : Affiche l'aide sur la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `write` :

1. Envoyer un message à un utilisateur sur le même terminal :
   ```bash
   write alice
   Bonjour Alice, comment ça va ?
   ```

2. Envoyer un message à un utilisateur spécifique sur un terminal particulier :
   ```bash
   write bob pts/1
   Je suis en pause, reviens plus tard !
   ```

3. Utiliser l'option silencieuse pour envoyer un message sans afficher d'état :
   ```bash
   write -s charlie
   Je t'attends dans la salle de réunion.
   ```

## Tips
- Assurez-vous que l'utilisateur que vous essayez de contacter est connecté et que son terminal est disponible pour recevoir des messages.
- Pour interrompre l'envoi d'un message, utilisez `Ctrl + C`.
- Pensez à vérifier si l'utilisateur a désactivé la réception de messages avec la commande `mesg`, sinon votre message ne sera pas reçu.