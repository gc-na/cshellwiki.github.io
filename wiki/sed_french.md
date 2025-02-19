# [Linux] C Shell (csh) sed Utilisation : Outil de traitement de texte

## Overview
La commande `sed` (Stream Editor) est un éditeur de texte non interactif qui permet de manipuler et de transformer des flux de texte. Elle est souvent utilisée pour effectuer des substitutions, des suppressions ou des insertions dans des fichiers ou des entrées standard.

## Usage
La syntaxe de base de la commande `sed` est la suivante :

```bash
sed [options] [arguments]
```

## Common Options
Voici quelques options courantes de `sed` :

- `-e` : Permet d'ajouter une expression à exécuter.
- `-i` : Modifie le fichier en place (sans créer de fichier temporaire).
- `-n` : Supprime la sortie automatique, n'affiche que les lignes spécifiées.
- `s/pattern/replacement/` : Effectue une substitution de `pattern` par `replacement`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `sed` :

### Exemple 1 : Remplacer du texte dans un fichier
Pour remplacer toutes les occurrences de "chat" par "chien" dans un fichier `animaux.txt` :

```bash
sed -i 's/chat/chien/g' animaux.txt
```

### Exemple 2 : Afficher uniquement les lignes contenant un mot spécifique
Pour afficher les lignes contenant le mot "erreur" dans un fichier `log.txt` :

```bash
sed -n '/erreur/p' log.txt
```

### Exemple 3 : Supprimer les lignes vides d'un fichier
Pour supprimer toutes les lignes vides d'un fichier `texte.txt` :

```bash
sed -i '/^$/d' texte.txt
```

### Exemple 4 : Ajouter une ligne après une correspondance
Pour ajouter "Nouvelle ligne" après chaque ligne contenant "Important" dans `notes.txt` :

```bash
sed -i '/Important/a Nouvelle ligne' notes.txt
```

## Tips
- Toujours faire une sauvegarde de vos fichiers avant d'utiliser l'option `-i`, car elle modifie le fichier original.
- Utilisez des expressions régulières pour des substitutions plus complexes.
- Testez vos commandes `sed` sans l'option `-i` pour voir les résultats avant de les appliquer définitivement.