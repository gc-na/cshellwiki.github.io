# [Linux] Bash dstat : surveiller les ressources système en temps réel

## Overview
La commande `dstat` est un outil puissant qui permet de surveiller les ressources système en temps réel. Elle combine les fonctionnalités de plusieurs autres outils de surveillance, comme `vmstat`, `iostat`, et `netstat`, en fournissant une vue d'ensemble des performances du système.

## Usage
La syntaxe de base de la commande `dstat` est la suivante :

```bash
dstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `dstat` :

- `-c` : Affiche l'utilisation du processeur.
- `-d` : Montre l'activité du disque.
- `-n` : Affiche les statistiques réseau.
- `-m` : Montre l'utilisation de la mémoire.
- `-t` : Affiche l'horodatage.
- `--help` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `dstat` :

1. Pour afficher l'utilisation du processeur et de la mémoire :

   ```bash
   dstat -c -m
   ```

2. Pour surveiller l'activité du disque et du réseau :

   ```bash
   dstat -d -n
   ```

3. Pour obtenir une vue complète avec horodatage :

   ```bash
   dstat -t -c -d -n -m
   ```

4. Pour enregistrer la sortie dans un fichier :

   ```bash
   dstat -t -c -d > output.txt
   ```

## Tips
- Utilisez `dstat` avec l'option `--help` pour explorer toutes les options disponibles et personnaliser votre surveillance.
- Combinez plusieurs options pour obtenir une vue d'ensemble complète des performances de votre système.
- Pensez à exécuter `dstat` avec des privilèges d'administrateur si vous souhaitez surveiller toutes les ressources système.