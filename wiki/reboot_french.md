# [Linux] Bash reboot usage : Redémarrer le système

## Overview
La commande `reboot` est utilisée pour redémarrer le système d'exploitation. Elle permet de fermer toutes les applications en cours et de redémarrer l'ordinateur, ce qui est souvent nécessaire après l'installation de mises à jour ou de nouveaux logiciels.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
reboot [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `reboot` :

- `-f` : Force le redémarrage sans passer par le processus d'arrêt normal.
- `-p` : Éteint l'ordinateur après le redémarrage.
- `--halt` : Arrête le système au lieu de le redémarrer.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `reboot` :

1. **Redémarrer le système normalement :**
   ```bash
   reboot
   ```

2. **Forcer le redémarrage sans attendre la fermeture des applications :**
   ```bash
   reboot -f
   ```

3. **Redémarrer et éteindre le système après le redémarrage :**
   ```bash
   reboot -p
   ```

4. **Utiliser la commande pour arrêter le système au lieu de redémarrer :**
   ```bash
   reboot --halt
   ```

## Tips
- Assurez-vous d'enregistrer votre travail avant d'utiliser la commande `reboot`, car elle fermera toutes les applications en cours.
- Utilisez l'option `-f` avec précaution, car cela peut entraîner la perte de données non sauvegardées.
- Pour un redémarrage programmé, envisagez d'utiliser la commande `shutdown` avec l'option `-r` pour un contrôle plus fin sur le processus de redémarrage.