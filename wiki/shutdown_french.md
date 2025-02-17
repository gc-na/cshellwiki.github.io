# [Linux] Bash shutdown utilisation : Arrêter ou redémarrer le système

## Overview
La commande `shutdown` est utilisée pour arrêter ou redémarrer un système Linux. Elle permet de planifier l'arrêt ou le redémarrage de l'ordinateur à un moment précis ou après un certain délai.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
shutdown [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `shutdown` :

- `-h` : Arrête le système.
- `-r` : Redémarre le système.
- `-t [seconds]` : Définit un délai avant l'arrêt ou le redémarrage (en secondes).
- `now` : Indique que l'arrêt ou le redémarrage doit se faire immédiatement.
- `+m` : Planifie l'arrêt ou le redémarrage dans `m` minutes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `shutdown` :

1. **Arrêter le système immédiatement :**
   ```bash
   shutdown -h now
   ```

2. **Redémarrer le système dans 5 minutes :**
   ```bash
   shutdown -r +5
   ```

3. **Arrêter le système à une heure précise (par exemple, 22h00) :**
   ```bash
   shutdown -h 22:00
   ```

4. **Annuler un arrêt planifié :**
   ```bash
   shutdown -c
   ```

## Tips
- Toujours avertir les utilisateurs connectés avant d'arrêter ou de redémarrer le système pour éviter la perte de données.
- Utiliser `shutdown -h now` avec précaution, car cela arrête immédiatement le système sans délai.
- Pour des opérations régulières, envisagez d'utiliser des scripts pour automatiser l'arrêt ou le redémarrage à des moments spécifiques.