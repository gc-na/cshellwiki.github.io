# [Linux] C Shell (csh) nice : Ajuster la priorité des processus

## Overview
La commande `nice` dans C Shell (csh) permet de modifier la priorité d'exécution d'un processus. En ajustant la priorité, vous pouvez influencer la quantité de ressources système allouées à un processus, ce qui peut être utile pour gérer les performances des applications en cours d'exécution.

## Usage
La syntaxe de base de la commande `nice` est la suivante :

```csh
nice [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `nice` :

- `-n` : Spécifie la valeur de "nice" à appliquer. Les valeurs vont de -20 (priorité la plus élevée) à 19 (priorité la plus basse).
- `-h` : Affiche l'aide et les options disponibles pour la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `nice` :

1. **Lancer un processus avec une priorité inférieure :**
   ```csh
   nice -n 10 ./mon_script.sh
   ```
   Cela exécute `mon_script.sh` avec une priorité de 10.

2. **Lancer un processus avec une priorité plus élevée :**
   ```csh
   nice -n -5 ./mon_programme
   ```
   Cela exécute `mon_programme` avec une priorité de -5.

3. **Vérifier la priorité d'un processus en cours :**
   ```csh
   ps -o pid,ni,cmd
   ```
   Cette commande affiche les PID, les valeurs de "nice" et les commandes des processus en cours.

## Tips
- Utilisez `nice` pour des processus non critiques afin de libérer des ressources pour d'autres tâches importantes.
- Évitez d'utiliser des valeurs de "nice" trop basses pour ne pas monopoliser le CPU.
- Combinez `nice` avec d'autres commandes comme `nohup` pour exécuter des processus en arrière-plan sans interruption.