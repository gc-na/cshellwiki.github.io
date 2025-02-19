# [Linux] C Shell (csh) shutdown : Arrêter le système

## Overview
La commande `shutdown` est utilisée pour arrêter ou redémarrer un système Unix/Linux de manière contrôlée. Elle permet d'avertir les utilisateurs connectés et de fermer les processus en cours avant d'éteindre l'ordinateur.

## Usage
La syntaxe de base de la commande `shutdown` est la suivante :

```csh
shutdown [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `shutdown` :

- `-h` : Arrête le système.
- `-r` : Redémarre le système.
- `-k` : Envoie un message d'avertissement sans arrêter le système.
- `time` : Spécifie le délai avant l'arrêt (ex. `now`, `+5` pour 5 minutes).
- `message` : Un message à afficher aux utilisateurs avant l'arrêt.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `shutdown` :

1. Pour arrêter le système immédiatement :
   ```csh
   shutdown -h now
   ```

2. Pour redémarrer le système dans 10 minutes :
   ```csh
   shutdown -r +10
   ```

3. Pour envoyer un message d'avertissement sans arrêter le système :
   ```csh
   shutdown -k now "Le système sera arrêté bientôt."
   ```

4. Pour arrêter le système à une heure précise (par exemple, 22h00) :
   ```csh
   shutdown -h 22:00
   ```

## Tips
- Toujours informer les utilisateurs avant d'utiliser `shutdown` pour éviter toute perte de données.
- Utilisez l'option `-k` pour tester le message d'avertissement sans effectuer l'arrêt.
- Vérifiez les processus en cours et sauvegardez les travaux importants avant d'arrêter le système.