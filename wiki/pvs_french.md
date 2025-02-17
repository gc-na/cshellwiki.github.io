# [Linux] Bash pvs utilisation : Afficher les informations sur les volumes physiques

## Overview
La commande `pvs` est utilisée pour afficher des informations sur les volumes physiques dans un système de gestion de volumes logiques (LVM). Elle permet aux utilisateurs de visualiser les caractéristiques des volumes physiques, tels que leur taille, leur état et leur groupe de volumes associé.

## Usage
La syntaxe de base de la commande `pvs` est la suivante :

```bash
pvs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `pvs` :

- `-o, --options`: Spécifie les colonnes à afficher.
- `-n, --noheadings`: Supprime l'en-tête de la sortie.
- `-h, --units`: Affiche les tailles avec des unités lisibles (K, M, G, T).
- `-v, --verbose`: Affiche des informations détaillées sur les volumes physiques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `pvs` :

1. **Afficher les informations de base sur les volumes physiques :**

   ```bash
   pvs
   ```

2. **Afficher les informations avec des unités lisibles :**

   ```bash
   pvs -h
   ```

3. **Afficher des colonnes spécifiques, comme le nom et la taille :**

   ```bash
   pvs -o pv_name,pv_size
   ```

4. **Afficher les informations sans en-tête :**

   ```bash
   pvs -n
   ```

5. **Afficher des informations détaillées :**

   ```bash
   pvs -v
   ```

## Tips
- Utilisez l'option `-h` pour rendre la sortie plus lisible, surtout si vous travaillez avec de grandes tailles de volumes.
- Combinez `pvs` avec d'autres commandes LVM pour obtenir une vue d'ensemble complète de votre configuration de stockage.
- Pensez à utiliser `man pvs` pour consulter la page de manuel et découvrir d'autres options et fonctionnalités.