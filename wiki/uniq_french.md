# [Linux] Bash uniq Utilisation : Supprimer les doublons dans un fichier

## Overview
La commande `uniq` est utilisée pour filtrer les lignes répétées dans un fichier ou une entrée standard. Elle ne supprime que les doublons consécutifs, ce qui signifie que les lignes identiques doivent être adjacentes pour être considérées comme des doublons.

## Usage
La syntaxe de base de la commande `uniq` est la suivante :

```bash
uniq [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `uniq` :

- `-c` : Compte le nombre d'occurrences de chaque ligne.
- `-d` : Affiche uniquement les lignes qui apparaissent plus d'une fois.
- `-u` : Affiche uniquement les lignes qui sont uniques (n'apparaissent qu'une fois).
- `-i` : Ignore la casse lors de la comparaison des lignes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `uniq` :

1. **Supprimer les doublons d'un fichier :**

   ```bash
   uniq fichier.txt
   ```

2. **Compter les occurrences de chaque ligne :**

   ```bash
   uniq -c fichier.txt
   ```

3. **Afficher uniquement les lignes répétées :**

   ```bash
   uniq -d fichier.txt
   ```

4. **Afficher uniquement les lignes uniques :**

   ```bash
   uniq -u fichier.txt
   ```

5. **Ignorer la casse lors de la suppression des doublons :**

   ```bash
   uniq -i fichier.txt
   ```

## Tips
- Assurez-vous que le fichier est trié avant d'utiliser `uniq`, car cela ne supprime que les doublons consécutifs. Vous pouvez utiliser la commande `sort` pour trier le fichier.
- Combinez `sort` et `uniq` pour obtenir une liste de lignes uniques dans un fichier non trié :

  ```bash
  sort fichier.txt | uniq
  ```
  
- Utilisez `uniq -c` pour obtenir un aperçu rapide des lignes les plus fréquentes dans votre fichier.