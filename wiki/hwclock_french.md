# [Linux] Bash hwclock : [gérer l'horloge matérielle]

## Overview
La commande `hwclock` est utilisée pour interagir avec l'horloge matérielle d'un système. Elle permet de lire, régler et synchroniser l'horloge du système avec l'horloge matérielle, ce qui est essentiel pour maintenir une heure précise, même lorsque le système est éteint.

## Usage
La syntaxe de base de la commande `hwclock` est la suivante :

```bash
hwclock [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `hwclock` :

- `--show` : Affiche la date et l'heure de l'horloge matérielle.
- `--set` : Définit la date et l'heure de l'horloge matérielle.
- `--hctosys` : Synchronise l'horloge système avec l'horloge matérielle.
- `--systohc` : Synchronise l'horloge matérielle avec l'horloge système.
- `--utc` : Indique que l'horloge matérielle est configurée pour l'heure UTC.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `hwclock` :

1. **Afficher l'heure de l'horloge matérielle :**

   ```bash
   hwclock --show
   ```

2. **Définir l'heure de l'horloge matérielle :**

   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. **Synchroniser l'horloge système avec l'horloge matérielle :**

   ```bash
   hwclock --hctosys
   ```

4. **Synchroniser l'horloge matérielle avec l'horloge système :**

   ```bash
   hwclock --systohc
   ```

5. **Afficher l'heure de l'horloge matérielle en UTC :**

   ```bash
   hwclock --show --utc
   ```

## Tips
- Assurez-vous d'exécuter `hwclock` avec des privilèges root si vous devez modifier l'horloge matérielle.
- Utilisez `hwclock --systohc` après avoir réglé l'heure de votre système pour vous assurer que l'horloge matérielle est à jour.
- Vérifiez régulièrement l'heure de l'horloge matérielle, surtout après un redémarrage, pour éviter des problèmes de synchronisation.