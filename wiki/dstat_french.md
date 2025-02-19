# [Linux] C Shell (csh) dstat Utilisation : Surveillance des ressources système

## Overview
La commande `dstat` est un outil puissant qui permet de surveiller en temps réel les ressources système. Elle combine les fonctionnalités de plusieurs autres outils de surveillance, offrant une vue d'ensemble des performances du système, y compris l'utilisation du CPU, la mémoire, le réseau, et plus encore.

## Usage
La syntaxe de base de la commande `dstat` est la suivante :

```bash
dstat [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `dstat` :

- `-c` : Affiche l'utilisation du CPU.
- `-d` : Montre l'activité du disque.
- `-n` : Affiche l'activité réseau.
- `-m` : Montre l'utilisation de la mémoire.
- `-t` : Affiche l'horodatage pour chaque ligne de sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `dstat` :

1. Pour afficher l'utilisation du CPU et de la mémoire :
   ```bash
   dstat -c -m
   ```

2. Pour surveiller l'activité du disque et du réseau :
   ```bash
   dstat -d -n
   ```

3. Pour afficher toutes les statistiques disponibles avec un horodatage :
   ```bash
   dstat -tcdmn
   ```

4. Pour enregistrer la sortie dans un fichier pour une analyse ultérieure :
   ```bash
   dstat -tcdmn > dstat_output.txt
   ```

## Tips
- Utilisez `dstat` avec des options combinées pour obtenir une vue complète des performances de votre système.
- Pensez à rediriger la sortie vers un fichier si vous souhaitez analyser les données plus tard.
- Familiarisez-vous avec les différentes options pour adapter `dstat` à vos besoins spécifiques de surveillance.