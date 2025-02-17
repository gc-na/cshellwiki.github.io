# [Linux] Bash ulimit : Limiter les ressources des processus

## Overview
La commande `ulimit` est utilisée dans les systèmes Unix et Linux pour définir ou afficher les limites des ressources disponibles pour les processus en cours d'exécution. Cela permet de contrôler l'utilisation des ressources système, comme la mémoire ou le nombre de fichiers ouverts, afin de prévenir les abus et d'assurer la stabilité du système.

## Usage
La syntaxe de base de la commande `ulimit` est la suivante :

```bash
ulimit [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ulimit` :

- `-a` : Affiche toutes les limites actuelles.
- `-c` : Définit la taille maximale des fichiers de core dump.
- `-d` : Définit la taille maximale de la mémoire de données.
- `-f` : Définit la taille maximale des fichiers créés par le shell.
- `-n` : Définit le nombre maximal de fichiers ouverts par le processus.
- `-t` : Définit le temps maximal en secondes que le processus peut utiliser.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ulimit` :

1. **Afficher toutes les limites actuelles :**
   ```bash
   ulimit -a
   ```

2. **Définir la taille maximale d'un fichier à 100 Mo :**
   ```bash
   ulimit -f 102400
   ```

3. **Définir le nombre maximal de fichiers ouverts à 2048 :**
   ```bash
   ulimit -n 2048
   ```

4. **Limiter la taille des fichiers de core dump à 0 (désactiver les core dumps) :**
   ```bash
   ulimit -c 0
   ```

5. **Afficher la limite de la mémoire de données :**
   ```bash
   ulimit -d
   ```

## Tips
- **Vérifiez les limites avant d'exécuter des applications gourmandes en ressources** pour éviter les plantages.
- **Utilisez `ulimit -a` pour un aperçu rapide** de toutes les limites en place.
- **Modifiez les limites dans le fichier de configuration de votre shell** (comme `.bashrc`) pour qu'elles soient appliquées à chaque session.
- **Soyez prudent lorsque vous augmentez les limites**, car cela peut affecter la stabilité du système si trop de ressources sont consommées.