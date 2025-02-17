# [Linux] Bash timedatectl : Gérer la date et l'heure du système

## Overview
La commande `timedatectl` permet de gérer et de configurer la date et l'heure du système sous Linux. Elle fait partie du système de gestion de l'heure de systemd et offre une interface simple pour afficher et modifier les paramètres de temps.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
timedatectl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `timedatectl` :

- `status` : Affiche l'état actuel de la date et de l'heure.
- `set-time` : Définit la date et l'heure manuellement.
- `set-timezone` : Change le fuseau horaire du système.
- `set-ntp` : Active ou désactive la synchronisation NTP (Network Time Protocol).
- `list-timezones` : Affiche la liste des fuseaux horaires disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `timedatectl` :

1. **Afficher l'état actuel de la date et de l'heure :**

   ```bash
   timedatectl status
   ```

2. **Définir la date et l'heure manuellement :**

   ```bash
   timedatectl set-time '2023-10-01 12:00:00'
   ```

3. **Changer le fuseau horaire :**

   ```bash
   timedatectl set-timezone Europe/Paris
   ```

4. **Activer la synchronisation NTP :**

   ```bash
   timedatectl set-ntp true
   ```

5. **Lister tous les fuseaux horaires disponibles :**

   ```bash
   timedatectl list-timezones
   ```

## Tips
- Assurez-vous d'avoir les droits d'administrateur pour modifier la date et l'heure du système.
- Utilisez `timedatectl list-timezones` pour trouver le fuseau horaire correct avant de le définir.
- Vérifiez régulièrement l'état de la synchronisation NTP pour garantir que votre système reste à l'heure.