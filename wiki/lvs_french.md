# [Linux] C Shell (csh) lvs : lister les volumes logiques

## Overview
La commande `lvs` dans le C Shell (csh) est utilisée pour afficher des informations sur les volumes logiques dans un système de gestion de volumes logiques (LVM). Elle permet aux utilisateurs de visualiser les volumes logiques existants, leurs tailles et d'autres attributs pertinents.

## Usage
La syntaxe de base de la commande `lvs` est la suivante :

```
lvs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `lvs` :

- `-a` : Affiche tous les volumes logiques, y compris ceux qui sont inactifs.
- `-o` : Permet de spécifier les colonnes à afficher.
- `--units` : Définit les unités d'affichage (par exemple, k, M, G).
- `-h` : Affiche l'aide sur l'utilisation de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lvs` :

1. **Afficher tous les volumes logiques :**
   ```bash
   lvs
   ```

2. **Afficher tous les volumes logiques, y compris ceux inactifs :**
   ```bash
   lvs -a
   ```

3. **Afficher les volumes logiques avec des unités spécifiques :**
   ```bash
   lvs --units g
   ```

4. **Afficher des colonnes spécifiques (par exemple, nom et taille) :**
   ```bash
   lvs -o lv_name,lv_size
   ```

## Tips
- Utilisez l'option `-h` pour obtenir de l'aide sur les différentes options disponibles avec la commande `lvs`.
- Combinez `lvs` avec d'autres commandes LVM pour une gestion plus efficace de vos volumes logiques.
- Pensez à vérifier régulièrement l'état de vos volumes logiques pour éviter des problèmes de stockage.