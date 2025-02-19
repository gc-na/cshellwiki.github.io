# [Linux] C Shell (csh) journalctl : Afficher les journaux système

## Overview
La commande `journalctl` est utilisée pour afficher les journaux du système gérés par le système de journalisation `systemd`. Elle permet aux utilisateurs de consulter les messages de log générés par le système et les services en cours d'exécution.

## Usage
La syntaxe de base de la commande `journalctl` est la suivante :

```csh
journalctl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `journalctl` :

- `-b` : Affiche les journaux depuis le dernier démarrage.
- `-f` : Suivre les journaux en temps réel (similaire à `tail -f`).
- `--since` : Affiche les journaux depuis une date ou une heure spécifiée.
- `--until` : Affiche les journaux jusqu'à une date ou une heure spécifiée.
- `-u` : Affiche les journaux pour une unité de service spécifique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `journalctl` :

1. Afficher tous les journaux :
   ```csh
   journalctl
   ```

2. Afficher les journaux depuis le dernier démarrage :
   ```csh
   journalctl -b
   ```

3. Suivre les journaux en temps réel :
   ```csh
   journalctl -f
   ```

4. Afficher les journaux d'un service spécifique (par exemple, `ssh.service`) :
   ```csh
   journalctl -u ssh.service
   ```

5. Afficher les journaux depuis une date spécifique :
   ```csh
   journalctl --since "2023-10-01 10:00:00"
   ```

## Tips
- Utilisez `journalctl -b -1` pour afficher les journaux du démarrage précédent.
- Combinez les options `--since` et `--until` pour filtrer les journaux sur une période spécifique.
- Pensez à rediriger la sortie vers un fichier si vous souhaitez conserver un enregistrement des journaux :
  ```csh
  journalctl > journaux.txt
  ```