# [Linux] C Shell (csh) vmstat : surveiller l'état du système

## Overview
La commande `vmstat` (Virtual Memory Statistics) fournit des informations sur la mémoire virtuelle, les processus, l'entrée/sortie et l'utilisation du CPU. Elle permet aux utilisateurs de surveiller les performances du système en temps réel.

## Usage
La syntaxe de base de la commande `vmstat` est la suivante :

```csh
vmstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `vmstat` :

- `-s` : Affiche les statistiques de mémoire.
- `-m` : Affiche les statistiques de la mémoire de la machine.
- `-d` : Affiche les statistiques de disque.
- `-t` : Affiche l'heure et la date avec les statistiques.
- `interval` : Définit l'intervalle de temps en secondes entre les mises à jour des statistiques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `vmstat` :

1. Afficher les statistiques par défaut :
   ```csh
   vmstat
   ```

2. Afficher les statistiques toutes les 5 secondes :
   ```csh
   vmstat 5
   ```

3. Afficher les statistiques de mémoire :
   ```csh
   vmstat -s
   ```

4. Afficher les statistiques de disque :
   ```csh
   vmstat -d
   ```

5. Afficher les statistiques avec l'heure et la date :
   ```csh
   vmstat -t 2
   ```

## Tips
- Utilisez `vmstat` avec un intervalle pour surveiller les performances du système en temps réel.
- Combinez `vmstat` avec d'autres outils comme `top` ou `iostat` pour une analyse plus approfondie.
- Vérifiez régulièrement les statistiques de mémoire pour éviter des problèmes de performance liés à une mémoire insuffisante.