# [Linux] C Shell (csh) htop Utilisation : Afficher et gérer les processus système

## Overview
La commande `htop` est un visualiseur interactif de processus qui permet aux utilisateurs de surveiller les ressources système en temps réel. Contrairement à la commande `top`, `htop` offre une interface plus conviviale et des fonctionnalités avancées pour gérer les processus.

## Usage
La syntaxe de base de la commande `htop` est la suivante :

```csh
htop [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `htop` :

- `-h` : Affiche l'aide et les options disponibles.
- `-d <delay>` : Définit le délai entre les mises à jour de l'affichage (en secondes).
- `-p <pid>` : Affiche uniquement le processus avec l'identifiant spécifié (PID).
- `-s <sort>` : Définit le critère de tri, par exemple `pid`, `mem`, `cpu`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `htop` :

1. Lancer `htop` sans options :
   ```csh
   htop
   ```

2. Afficher l'aide :
   ```csh
   htop -h
   ```

3. Définir un délai de mise à jour de 2 secondes :
   ```csh
   htop -d 2
   ```

4. Afficher uniquement un processus spécifique avec son PID :
   ```csh
   htop -p 1234
   ```

5. Trier les processus par utilisation de la mémoire :
   ```csh
   htop -s mem
   ```

## Tips
- Utilisez les touches fléchées pour naviguer dans la liste des processus et `F9` pour tuer un processus sélectionné.
- Appuyez sur `F2` pour accéder aux paramètres et personnaliser l'affichage selon vos préférences.
- Pensez à utiliser `htop` avec des privilèges d'administrateur (par exemple, via `sudo`) pour voir tous les processus système.