# [Linux] Bash sleep utilisation : Mettre en pause l'exécution

## Overview
La commande `sleep` est utilisée dans les scripts Bash pour suspendre l'exécution d'un script pendant une durée spécifiée. Cela peut être utile pour créer des délais entre les commandes ou pour attendre que certaines conditions soient remplies avant de continuer.

## Usage
La syntaxe de base de la commande `sleep` est la suivante :

```bash
sleep [options] [arguments]
```

## Common Options
- `-s`, `--seconds` : Spécifie la durée en secondes (c'est la valeur par défaut).
- `-m`, `--minutes` : Spécifie la durée en minutes.
- `-h`, `--hours` : Spécifie la durée en heures.
- `-d`, `--days` : Spécifie la durée en jours.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `sleep` :

1. **Mettre en pause pendant 5 secondes :**
   ```bash
   sleep 5
   ```

2. **Mettre en pause pendant 2 minutes :**
   ```bash
   sleep 2m
   ```

3. **Mettre en pause pendant 1 heure :**
   ```bash
   sleep 1h
   ```

4. **Utiliser sleep dans un script pour créer un délai entre les commandes :**
   ```bash
   echo "Début du processus..."
   sleep 10
   echo "Processus en cours..."
   sleep 5
   echo "Processus terminé."
   ```

5. **Combiner plusieurs durées :**
   ```bash
   sleep 1d 2h 30m
   ```

## Tips
- Utilisez `sleep` pour éviter de surcharger les ressources système en ajoutant des délais entre les tâches dans vos scripts.
- Soyez prudent avec des délais trop longs, car cela peut rendre vos scripts moins réactifs.
- Combinez `sleep` avec d'autres commandes dans des boucles pour créer des scripts d'attente efficaces.