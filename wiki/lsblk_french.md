# [Linux] Bash lsblk Utilisation : Afficher les informations sur les blocs de périphériques

## Overview
La commande `lsblk` est utilisée pour afficher des informations sur les périphériques de blocs disponibles sur le système. Elle fournit une vue d'ensemble des disques, partitions et autres périphériques de stockage, facilitant ainsi la gestion des ressources de stockage.

## Usage
La syntaxe de base de la commande `lsblk` est la suivante :

```bash
lsblk [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `lsblk` :

- `-a`, `--all` : Affiche tous les périphériques, y compris ceux qui ne sont pas montés.
- `-f`, `--fs` : Affiche des informations sur le système de fichiers, telles que le type de système de fichiers et l'étiquette.
- `-l`, `--list` : Affiche les informations sous forme de liste plutôt que sous forme d'arbre.
- `-o`, `--output` : Permet de spécifier les colonnes à afficher.
- `-p`, `--paths` : Affiche les chemins complets des périphériques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lsblk` :

1. **Afficher tous les périphériques de blocs :**

   ```bash
   lsblk
   ```

2. **Afficher tous les périphériques, y compris ceux non montés :**

   ```bash
   lsblk -a
   ```

3. **Afficher les informations sur le système de fichiers :**

   ```bash
   lsblk -f
   ```

4. **Afficher les périphériques sous forme de liste :**

   ```bash
   lsblk -l
   ```

5. **Afficher des colonnes spécifiques :**

   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tips
- Utilisez l'option `-f` pour obtenir rapidement des informations sur le type de système de fichiers, ce qui est utile lors de la gestion de plusieurs partitions.
- Combinez `lsblk` avec d'autres commandes comme `grep` pour filtrer les résultats, par exemple : 

   ```bash
   lsblk | grep sda
   ```

- Pensez à utiliser `man lsblk` pour consulter le manuel complet et découvrir d'autres options disponibles.