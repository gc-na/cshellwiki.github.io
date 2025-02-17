# [Linux] Bash vmstat Utilisation : Surveillance des ressources système

## Overview
La commande `vmstat` (Virtual Memory Statistics) est utilisée pour afficher des informations sur la mémoire virtuelle, les processus, l'entrée/sortie et l'utilisation du CPU. Elle permet aux utilisateurs de surveiller les performances du système en temps réel.

## Usage
La syntaxe de base de la commande `vmstat` est la suivante :

```bash
vmstat [options] [interval] [count]
```

- `options` : options supplémentaires pour personnaliser la sortie.
- `interval` : le temps en secondes entre chaque mise à jour.
- `count` : le nombre de mises à jour à afficher.

## Common Options
Voici quelques options courantes pour `vmstat` :

- `-s` : Affiche un résumé des statistiques de mémoire.
- `-m` : Affiche des informations sur la mémoire de page.
- `-d` : Affiche des statistiques sur les disques.
- `-a` : Affiche des informations sur la mémoire active et inactive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `vmstat` :

1. Afficher les statistiques par défaut :
   ```bash
   vmstat
   ```

2. Afficher les statistiques toutes les 2 secondes :
   ```bash
   vmstat 2
   ```

3. Afficher les statistiques toutes les 5 secondes, 10 fois :
   ```bash
   vmstat 5 10
   ```

4. Afficher un résumé des statistiques de mémoire :
   ```bash
   vmstat -s
   ```

5. Afficher les statistiques de disque :
   ```bash
   vmstat -d
   ```

## Tips
- Utilisez `vmstat` avec d'autres outils comme `top` ou `htop` pour une vue d'ensemble complète des performances du système.
- Surveillez régulièrement les valeurs de `si` et `so` (swap in et swap out) pour éviter des problèmes de performance liés à la mémoire.
- Combinez `vmstat` avec des scripts pour automatiser la surveillance des performances sur des périodes prolongées.