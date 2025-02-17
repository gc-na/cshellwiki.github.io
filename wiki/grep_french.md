# [Linux] Bash grep utilisation : rechercher des motifs dans des fichiers

## Overview
La commande `grep` est utilisée pour rechercher des motifs spécifiques dans des fichiers ou dans l'entrée standard. Elle est particulièrement utile pour filtrer des lignes de texte qui contiennent un certain motif, ce qui en fait un outil précieux pour l'analyse de fichiers et le traitement de texte.

## Usage
La syntaxe de base de la commande `grep` est la suivante :

```bash
grep [options] [arguments]
```

## Common Options
Voici quelques options courantes de `grep` avec de courtes explications :

- `-i` : Ignore la casse lors de la recherche.
- `-v` : Inverse la recherche, affichant les lignes qui ne correspondent pas au motif.
- `-r` : Recherche récursive dans tous les fichiers d'un répertoire.
- `-n` : Affiche les numéros de ligne avec les lignes correspondantes.
- `-l` : Affiche uniquement les noms de fichiers contenant le motif.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `grep` :

1. **Recherche d'un mot dans un fichier :**
   ```bash
   grep "mot" fichier.txt
   ```

2. **Recherche insensible à la casse :**
   ```bash
   grep -i "mot" fichier.txt
   ```

3. **Recherche récursive dans un répertoire :**
   ```bash
   grep -r "mot" /chemin/du/répertoire
   ```

4. **Afficher les numéros de ligne :**
   ```bash
   grep -n "mot" fichier.txt
   ```

5. **Afficher les fichiers contenant le motif :**
   ```bash
   grep -l "mot" *.txt
   ```

## Tips
- Utilisez `grep` avec d'autres commandes en utilisant des pipes pour filtrer les résultats. Par exemple :
  ```bash
  dmesg | grep "erreur"
  ```
- Combinez plusieurs options pour affiner votre recherche, comme `grep -rin "mot" /chemin/du/répertoire`.
- Pensez à utiliser des expressions régulières pour des recherches plus complexes.