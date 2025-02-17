# [Linux] Bash journalctl : Afficher les journaux système

## Overview
La commande `journalctl` est utilisée pour interroger et afficher les journaux du système gérés par `systemd`. Elle permet aux utilisateurs de consulter les messages de log générés par le système et les applications, facilitant ainsi le diagnostic et la surveillance des services.

## Usage
La syntaxe de base de la commande `journalctl` est la suivante :

```bash
journalctl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `journalctl` :

- `-b` : Affiche les journaux de la session de démarrage actuelle.
- `-f` : Suivre les nouveaux messages en temps réel (similaire à `tail -f`).
- `--since` : Affiche les journaux depuis une date ou une heure spécifiée.
- `--until` : Affiche les journaux jusqu'à une date ou une heure spécifiée.
- `-u <service>` : Affiche les journaux d'un service spécifique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `journalctl` :

1. **Afficher tous les journaux :**
   ```bash
   journalctl
   ```

2. **Afficher les journaux de la session de démarrage actuelle :**
   ```bash
   journalctl -b
   ```

3. **Suivre les nouveaux messages en temps réel :**
   ```bash
   journalctl -f
   ```

4. **Afficher les journaux depuis une date spécifique :**
   ```bash
   journalctl --since "2023-10-01 10:00:00"
   ```

5. **Afficher les journaux d'un service spécifique :**
   ```bash
   journalctl -u nginx.service
   ```

## Tips
- Utilisez `journalctl -b -1` pour afficher les journaux de la session de démarrage précédente.
- Combinez les options `--since` et `--until` pour affiner votre recherche de journaux.
- Pensez à rediriger la sortie vers un fichier pour une analyse ultérieure, par exemple : `journalctl > journaux.txt`.