# [Linux] C Shell (csh) uniq Utilisation : Éliminer les doublons dans un fichier

## Overview
La commande `uniq` est utilisée pour filtrer les lignes répétées dans un fichier ou dans une entrée standard. Elle affiche uniquement les lignes uniques, ce qui est particulièrement utile pour traiter des listes ou des fichiers contenant des doublons.

## Usage
La syntaxe de base de la commande `uniq` est la suivante :

```csh
uniq [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `uniq` :

- `-c` : Compte le nombre d'occurrences de chaque ligne.
- `-d` : Affiche uniquement les lignes qui apparaissent plus d'une fois.
- `-u` : Affiche uniquement les lignes qui apparaissent une seule fois.
- `-i` : Ignore la casse lors de la comparaison des lignes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `uniq` :

1. **Éliminer les doublons d'un fichier :**
   ```csh
   uniq fichier.txt
   ```

2. **Compter les occurrences de chaque ligne :**
   ```csh
   uniq -c fichier.txt
   ```

3. **Afficher uniquement les lignes répétées :**
   ```csh
   uniq -d fichier.txt
   ```

4. **Afficher uniquement les lignes uniques :**
   ```csh
   uniq -u fichier.txt
   ```

5. **Utiliser uniq avec tri :**
   Pour s'assurer que les doublons sont adjacents, il est souvent utile de trier le fichier d'abord :
   ```csh
   sort fichier.txt | uniq
   ```

## Tips
- Assurez-vous que le fichier est trié si vous souhaitez utiliser `uniq` pour éliminer les doublons, car `uniq` ne supprime que les doublons adjacents.
- Utilisez l'option `-c` pour avoir une meilleure idée de la fréquence des lignes dans votre fichier.
- Combinez `uniq` avec d'autres commandes comme `sort` pour des résultats plus efficaces lors du traitement de grandes listes.