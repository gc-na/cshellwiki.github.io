# [Linux] C Shell (csh) lsblk Utilisation : Afficher les périphériques de bloc

## Overview
La commande `lsblk` permet d'afficher les périphériques de bloc disponibles sur le système, tels que les disques durs, les partitions et les périphériques de stockage amovibles. Elle fournit une vue hiérarchique des périphériques, facilitant ainsi la gestion des disques.

## Usage
La syntaxe de base de la commande `lsblk` est la suivante :

```csh
lsblk [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `lsblk` :

- `-a` : Affiche tous les périphériques, y compris ceux qui ne sont pas montés.
- `-f` : Affiche les informations sur le système de fichiers.
- `-l` : Affiche la sortie sous forme de liste au lieu de la forme arborescente.
- `-o` : Permet de spécifier les colonnes à afficher.
- `-p` : Affiche les chemins complets des périphériques.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `lsblk` :

1. Afficher tous les périphériques de bloc :
   ```csh
   lsblk
   ```

2. Afficher tous les périphériques, y compris ceux qui ne sont pas montés :
   ```csh
   lsblk -a
   ```

3. Afficher les informations sur le système de fichiers :
   ```csh
   lsblk -f
   ```

4. Afficher la sortie sous forme de liste :
   ```csh
   lsblk -l
   ```

5. Afficher des colonnes spécifiques, par exemple, le nom et la taille :
   ```csh
   lsblk -o NAME,SIZE
   ```

## Tips
- Utilisez l'option `-f` pour obtenir des informations détaillées sur les systèmes de fichiers, ce qui peut être utile pour le dépannage.
- Combinez plusieurs options pour obtenir une vue d'ensemble plus complète de vos périphériques de bloc.
- Pensez à exécuter `lsblk` avec des privilèges d'administrateur si vous ne voyez pas certains périphériques, car certains peuvent nécessiter des autorisations élevées pour être affichés.