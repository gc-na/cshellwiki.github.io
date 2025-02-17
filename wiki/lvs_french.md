# [Linux] Bash lvs : Afficher les informations sur les volumes logiques

## Overview
La commande `lvs` est utilisée pour afficher des informations sur les volumes logiques dans un système utilisant LVM (Logical Volume Manager). Elle permet aux utilisateurs de visualiser les détails des volumes logiques, tels que leur taille, leur état et d'autres attributs pertinents.

## Usage
La syntaxe de base de la commande `lvs` est la suivante :

```bash
lvs [options] [arguments]
```

## Common Options
- `-o, --units`: Spécifie les unités à utiliser pour l'affichage des tailles.
- `-a, --all`: Affiche tous les volumes, y compris ceux qui sont inactifs.
- `-f, --full`: Affiche des informations détaillées sur les volumes logiques.
- `--noheadings`: Supprime les en-têtes de colonnes dans la sortie.
- `-S, --select`: Permet de filtrer les volumes logiques selon des critères spécifiques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lvs` :

1. **Afficher tous les volumes logiques** :
   ```bash
   lvs
   ```

2. **Afficher les volumes logiques avec des unités spécifiques** :
   ```bash
   lvs -o +devices
   ```

3. **Afficher tous les volumes, y compris ceux inactifs** :
   ```bash
   lvs -a
   ```

4. **Afficher les volumes logiques sans en-têtes** :
   ```bash
   lvs --noheadings
   ```

5. **Filtrer les volumes logiques selon un critère** :
   ```bash
   lvs -S 'lv_size > 10G'
   ```

## Tips
- Utilisez l'option `--units` pour rendre les tailles plus lisibles, surtout si vous travaillez avec de grands volumes.
- Combinez `lvs` avec d'autres commandes LVM pour une gestion efficace des volumes logiques.
- Pensez à utiliser des scripts pour automatiser la surveillance des volumes logiques, surtout dans des environnements de production.