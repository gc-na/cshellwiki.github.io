# [Linux] C Shell (csh) killall : Terminer tous les processus d'un nom donné

## Overview
La commande `killall` est utilisée pour terminer tous les processus qui correspondent à un nom spécifique. Cela permet de gérer facilement plusieurs instances d'un même programme sans avoir à les identifier individuellement.

## Usage
La syntaxe de base de la commande `killall` est la suivante :

```csh
killall [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `killall` :

- `-9` : Envoie un signal SIGKILL pour forcer l'arrêt immédiat des processus.
- `-v` : Affiche des informations détaillées sur les processus qui sont terminés.
- `-i` : Demande une confirmation avant de tuer chaque processus.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `killall` :

1. Terminer tous les processus nommés `firefox` :

   ```csh
   killall firefox
   ```

2. Forcer l'arrêt de tous les processus nommés `gedit` :

   ```csh
   killall -9 gedit
   ```

3. Afficher les processus qui seront terminés sans les arrêter :

   ```csh
   killall -v gnome-terminal
   ```

4. Demander une confirmation avant de terminer chaque processus nommé `ssh` :

   ```csh
   killall -i ssh
   ```

## Tips
- Utilisez l'option `-v` pour voir quels processus sont affectés, cela peut être utile pour le débogage.
- Soyez prudent avec l'option `-9`, car elle ne permet pas aux processus de se fermer proprement, ce qui peut entraîner une perte de données.
- Vérifiez toujours le nom exact du processus que vous souhaitez terminer pour éviter de fermer des applications non désirées.