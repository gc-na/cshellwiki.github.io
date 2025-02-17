# [Linux] Bash paste utilisation : Combiner des fichiers ligne par ligne

## Overview
La commande `paste` est utilisée pour combiner plusieurs fichiers en les fusionnant ligne par ligne. Cela permet de créer un nouveau fichier où chaque ligne contient des données provenant de plusieurs fichiers, séparées par un caractère de tabulation par défaut.

## Usage
La syntaxe de base de la commande `paste` est la suivante :

```bash
paste [options] [arguments]
```

## Common Options
- `-d` : Spécifie un délimiteur personnalisé pour séparer les colonnes (par défaut, c'est une tabulation).
- `-s` : Combine les lignes de chaque fichier en une seule ligne, séparée par le délimiteur.
- `-z` : Traite les fichiers comme des flux de données, en utilisant un caractère nul comme délimiteur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `paste` :

### Exemple 1 : Combiner deux fichiers
Supposons que vous ayez deux fichiers, `file1.txt` et `file2.txt`, avec le contenu suivant :

**file1.txt**
```
A
B
C
```

**file2.txt**
```
1
2
3
```

Vous pouvez les combiner avec la commande suivante :

```bash
paste file1.txt file2.txt
```

**Sortie :**
```
A   1
B   2
C   3
```

### Exemple 2 : Utiliser un délimiteur personnalisé
Pour utiliser un délimiteur personnalisé, par exemple une virgule, vous pouvez faire comme suit :

```bash
paste -d, file1.txt file2.txt
```

**Sortie :**
```
A,1
B,2
C,3
```

### Exemple 3 : Combiner les lignes d'un fichier en une seule ligne
Si vous voulez combiner toutes les lignes de `file1.txt` en une seule ligne :

```bash
paste -s file1.txt
```

**Sortie :**
```
A   B   C
```

## Tips
- Utilisez l'option `-d` pour personnaliser le séparateur selon vos besoins, ce qui peut être utile pour des formats de données spécifiques.
- Pensez à utiliser `-s` lorsque vous souhaitez créer un résumé ou une vue d'ensemble des données d'un fichier.
- Vérifiez le nombre de lignes dans vos fichiers avant de les combiner pour éviter des résultats inattendus, surtout si les fichiers n'ont pas le même nombre de lignes.