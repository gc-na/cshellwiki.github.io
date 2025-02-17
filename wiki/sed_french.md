# [Linux] Bash sed utilisation : Modifier et transformer du texte

## Overview
La commande `sed`, qui signifie "stream editor", est un outil puissant utilisé pour manipuler et transformer du texte dans des fichiers ou des flux de données. Elle permet de réaliser des substitutions, des suppressions et d'autres modifications de manière non interactive.

## Usage
La syntaxe de base de la commande `sed` est la suivante :

```bash
sed [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `sed` :

- `-e` : Permet d'ajouter une expression à exécuter.
- `-i` : Modifie le fichier en place, sans créer de copie.
- `-n` : Supprime l'affichage automatique des lignes, utile avec l'option `p` pour afficher uniquement les lignes spécifiées.
- `s/pattern/replacement/` : Effectue une substitution de `pattern` par `replacement`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `sed` :

1. **Substituer un mot dans un fichier :**
   ```bash
   sed 's/ancien/nouveau/' fichier.txt
   ```

2. **Modifier un fichier en place :**
   ```bash
   sed -i 's/ancien/nouveau/g' fichier.txt
   ```

3. **Afficher uniquement les lignes contenant un mot spécifique :**
   ```bash
   sed -n '/mot/p' fichier.txt
   ```

4. **Supprimer les lignes vides d'un fichier :**
   ```bash
   sed '/^$/d' fichier.txt
   ```

5. **Remplacer un mot dans plusieurs fichiers :**
   ```bash
   sed -i 's/ancien/nouveau/g' *.txt
   ```

## Tips
- Toujours faire une sauvegarde de vos fichiers avant d'utiliser l'option `-i`, pour éviter toute perte de données.
- Utilisez des expressions régulières pour des substitutions plus complexes.
- Testez vos commandes `sed` sans l'option `-i` pour voir les résultats avant de les appliquer définitivement.