# [Linux] Bash renice : Modifier la priorité des processus

## Overview
La commande `renice` permet de modifier la priorité d'exécution des processus en cours sur un système Linux. En ajustant la priorité, vous pouvez influencer la quantité de ressources CPU allouées à un processus spécifique, ce qui peut être utile pour optimiser les performances du système.

## Usage
La syntaxe de base de la commande `renice` est la suivante :

```bash
renice [options] [arguments]
```

## Common Options
- `-n`, `--priority` : Définit la nouvelle priorité pour le processus. La valeur peut être un entier entre -20 (priorité la plus élevée) et 19 (priorité la plus basse).
- `-p`, `--pid` : Spécifie le ou les identifiants de processus (PID) dont la priorité doit être modifiée.
- `-g`, `--pgrp` : Modifie la priorité de tous les processus d'un groupe de processus.
- `-u`, `--user` : Modifie la priorité de tous les processus appartenant à un utilisateur spécifique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `renice` :

1. **Modifier la priorité d'un processus par son PID :**
   ```bash
   renice -n 10 -p 1234
   ```
   Cela change la priorité du processus avec le PID 1234 à 10.

2. **Modifier la priorité de tous les processus d'un utilisateur :**
   ```bash
   renice -n 5 -u username
   ```
   Cela ajuste la priorité de tous les processus appartenant à l'utilisateur `username` à 5.

3. **Modifier la priorité d'un groupe de processus :**
   ```bash
   renice -n -5 -g 5678
   ```
   Cela définit la priorité de tous les processus dans le groupe de processus avec l'identifiant 5678 à -5.

## Tips
- Utilisez `renice` avec précaution, car une priorité trop élevée pour un processus peut nuire aux performances globales du système.
- Vérifiez la priorité actuelle des processus avec la commande `ps -eo pid,ni,cmd` avant de faire des modifications.
- Pour des ajustements fréquents, envisagez d'automatiser le processus avec un script Bash.