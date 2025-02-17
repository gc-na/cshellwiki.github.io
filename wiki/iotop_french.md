# [Linux] Bash iotop : Surveiller l'utilisation des entrées/sorties

## Overview
La commande `iotop` est un outil de surveillance en temps réel qui affiche l'utilisation des entrées/sorties (I/O) par les processus en cours d'exécution sur un système Linux. Elle permet aux utilisateurs d'identifier quels processus consomment le plus de ressources I/O, ce qui est particulièrement utile pour le dépannage des performances du système.

## Usage
La syntaxe de base de la commande `iotop` est la suivante :

```bash
iotop [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `iotop` :

- `-o` : Affiche uniquement les processus qui effectuent des opérations I/O.
- `-b` : Exécute `iotop` en mode batch, utile pour les scripts ou la redirection de sortie.
- `-n NUM` : Définit le nombre d'itérations à afficher avant de quitter.
- `-d SEC` : Définit la durée d'attente entre les mises à jour en secondes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `iotop` :

1. **Afficher tous les processus I/O en temps réel** :
   ```bash
   iotop
   ```

2. **Afficher uniquement les processus effectuant des opérations I/O** :
   ```bash
   iotop -o
   ```

3. **Exécuter iotop en mode batch avec 5 itérations** :
   ```bash
   iotop -b -n 5
   ```

4. **Définir un délai de mise à jour de 2 secondes** :
   ```bash
   iotop -d 2
   ```

## Tips
- Utilisez `iotop` avec `sudo` pour obtenir des informations complètes sur tous les processus, car certains peuvent nécessiter des privilèges élevés.
- Combinez `iotop` avec d'autres outils de surveillance comme `htop` pour une vue d'ensemble des performances du système.
- Pensez à utiliser le mode batch pour enregistrer les données dans un fichier pour une analyse ultérieure.