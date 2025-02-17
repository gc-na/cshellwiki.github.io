# [Linux] Bash mpstat Utilisation : surveiller l'utilisation du processeur

## Overview
La commande `mpstat` est utilisée pour afficher les statistiques d'utilisation du processeur sur un système. Elle permet de surveiller la charge de travail des processeurs individuels et de l'ensemble du système, ce qui est essentiel pour l'optimisation des performances.

## Usage
La syntaxe de base de la commande `mpstat` est la suivante :

```bash
mpstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `mpstat` :

- `-P ALL` : Affiche les statistiques pour tous les processeurs.
- `-u` : Affiche l'utilisation du processeur en pourcentage.
- `-h` : Affiche les statistiques dans un format lisible par l'homme.
- `interval` : Spécifie l'intervalle de temps en secondes entre les rapports.
- `count` : Indique combien de fois les statistiques doivent être affichées.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `mpstat` :

1. Afficher les statistiques d'utilisation du processeur pour tous les processeurs :

    ```bash
    mpstat -P ALL
    ```

2. Afficher l'utilisation du processeur toutes les 5 secondes :

    ```bash
    mpstat 5
    ```

3. Afficher les statistiques d'utilisation du processeur avec un format lisible :

    ```bash
    mpstat -u -h
    ```

4. Afficher les statistiques pour un processeur spécifique (par exemple, le processeur 0) toutes les 2 secondes :

    ```bash
    mpstat -P 0 2
    ```

## Tips
- Utilisez `mpstat` avec l'option `-P ALL` pour obtenir une vue d'ensemble de tous les processeurs, ce qui est utile pour identifier les goulets d'étranglement.
- Combinez `mpstat` avec d'autres outils comme `top` ou `htop` pour une analyse plus approfondie des performances du système.
- Pensez à exécuter `mpstat` avec des privilèges d'administrateur si vous rencontrez des problèmes d'accès aux informations sur les processeurs.