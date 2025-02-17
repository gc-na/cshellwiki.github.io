# [Linux] Bash nice utilisation : Gérer la priorité des processus

## Overview
La commande `nice` permet de modifier la priorité d'exécution des processus sous Linux. En ajustant la priorité, vous pouvez influencer la manière dont le système alloue les ressources CPU aux différents processus, ce qui peut être utile pour optimiser les performances.

## Usage
La syntaxe de base de la commande `nice` est la suivante :

```bash
nice [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `nice` :

- `-n, --adjustment`: Définit la valeur d'ajustement de la priorité (entre -20 et 19).
- `-h, --help`: Affiche l'aide et les options disponibles.
- `--version`: Affiche la version de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `nice` :

1. Lancer un processus avec une priorité plus basse (valeur par défaut est 10) :
   ```bash
   nice -n 10 ./mon_script.sh
   ```

2. Lancer un processus avec une priorité plus élevée (valeur minimale est -20) :
   ```bash
   nice -n -5 ./mon_autre_script.sh
   ```

3. Vérifier la priorité d'un processus en cours :
   ```bash
   ps -o pid,nice,cmd
   ```

4. Lancer un processus en arrière-plan avec une priorité modifiée :
   ```bash
   nice -n 15 ./mon_processus_en_arriere_plan &
   ```

## Tips
- Utilisez `nice` pour les processus gourmands en ressources afin de ne pas ralentir le système.
- Pour vérifier la priorité d'un processus, utilisez la commande `ps` avec les options appropriées.
- Évitez de donner une priorité trop élevée à un processus critique pour le système, car cela pourrait affecter la stabilité globale.