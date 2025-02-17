# [Linux] Bash uptime : Affiche le temps de fonctionnement du système

## Overview
La commande `uptime` permet d'afficher depuis combien de temps le système est en fonctionnement, ainsi que le nombre d'utilisateurs connectés et la charge moyenne du système sur les 1, 5 et 15 dernières minutes. C'est un outil utile pour surveiller la performance et la disponibilité du système.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
uptime [options]
```

## Common Options
- `-p` : Affiche le temps de fonctionnement sous une forme lisible.
- `-s` : Affiche l'heure à laquelle le système a démarré.
- `-h` : Affiche l'aide sur la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `uptime` :

1. Afficher le temps de fonctionnement du système :
   ```bash
   uptime
   ```

2. Afficher le temps de fonctionnement dans un format lisible :
   ```bash
   uptime -p
   ```

3. Afficher l'heure de démarrage du système :
   ```bash
   uptime -s
   ```

4. Afficher l'aide pour la commande uptime :
   ```bash
   uptime -h
   ```

## Tips
- Utilisez `uptime` régulièrement pour surveiller la santé de votre serveur.
- Combinez `uptime` avec d'autres commandes comme `top` ou `htop` pour une analyse plus approfondie de la performance du système.
- Pensez à automatiser l'exécution de `uptime` dans des scripts de surveillance pour recevoir des alertes en cas de problèmes de performance.