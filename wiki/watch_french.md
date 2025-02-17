# [Linux] Bash watch utilisation : surveiller les commandes en temps réel

## Overview
La commande `watch` permet d'exécuter une commande à intervalles réguliers, affichant ainsi la sortie de cette commande en temps réel. Cela est particulièrement utile pour surveiller les changements dans les fichiers, les processus ou d'autres informations système.

## Usage
La syntaxe de base de la commande `watch` est la suivante :

```bash
watch [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `watch` :

- `-n, --interval` : Définit l'intervalle en secondes entre les exécutions de la commande. Par défaut, l'intervalle est de 2 secondes.
- `-d, --differences` : Met en surbrillance les différences entre les sorties successives.
- `-t, --no-title` : Supprime l'affichage de l'en-tête de la commande en cours d'exécution.
- `-x, --exec` : Exécute la commande spécifiée sans passer par un shell.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `watch` :

1. Surveiller l'utilisation de la mémoire :
   ```bash
   watch free -h
   ```

2. Observer les processus actifs :
   ```bash
   watch ps aux
   ```

3. Vérifier les modifications dans un répertoire :
   ```bash
   watch ls -l /chemin/vers/répertoire
   ```

4. Surveiller un fichier journal :
   ```bash
   watch tail -n 10 /var/log/syslog
   ```

5. Afficher les différences dans un fichier :
   ```bash
   watch -d cat fichier.txt
   ```

## Tips
- Utilisez l'option `-n` pour ajuster l'intervalle d'exécution selon vos besoins.
- Combinez `watch` avec d'autres commandes pour surveiller des informations spécifiques.
- Pensez à utiliser l'option `-d` pour mieux visualiser les changements importants dans les sorties.