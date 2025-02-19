# [Linux] C Shell (csh) top : Afficher les processus en temps réel

## Overview
La commande `top` est utilisée pour afficher en temps réel les processus en cours d'exécution sur un système. Elle fournit des informations sur l'utilisation du CPU, de la mémoire et d'autres ressources système, permettant aux utilisateurs de surveiller l'activité de leur système.

## Usage
La syntaxe de base de la commande `top` est la suivante :

```
top [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `top` :

- `-d <seconds>` : Définit le délai entre les mises à jour de l'affichage.
- `-n <number>` : Spécifie le nombre de mises à jour à afficher avant de quitter.
- `-u <user>` : Affiche uniquement les processus appartenant à l'utilisateur spécifié.
- `-p <pid>` : Affiche uniquement les processus avec l'identifiant de processus spécifié.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `top` :

1. Lancer `top` avec les mises à jour par défaut :
   ```bash
   top
   ```

2. Afficher les processus avec une mise à jour toutes les 5 secondes :
   ```bash
   top -d 5
   ```

3. Afficher les processus d'un utilisateur spécifique :
   ```bash
   top -u username
   ```

4. Afficher les informations de processus pour un PID spécifique :
   ```bash
   top -p 1234
   ```

5. Limiter le nombre de mises à jour à 10 avant de quitter :
   ```bash
   top -n 10
   ```

## Tips
- Utilisez `q` pour quitter l'interface de `top`.
- Appuyez sur `h` pour afficher l'aide et les commandes interactives disponibles pendant l'exécution de `top`.
- Pour une vue plus concise, envisagez d'utiliser `htop`, qui est une version améliorée de `top` avec une interface utilisateur plus conviviale.