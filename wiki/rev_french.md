# [Linux] Bash rev : inverser les lignes de texte

## Overview
La commande `rev` est utilisée pour inverser les caractères de chaque ligne d'un fichier ou d'une entrée standard. Cela signifie que chaque ligne est retournée, avec les caractères dans l'ordre inverse.

## Usage
La syntaxe de base de la commande `rev` est la suivante :

```bash
rev [options] [arguments]
```

## Common Options
- `-o, --output=FILE` : Spécifie un fichier de sortie pour écrire les résultats inversés.
- `-h, --help` : Affiche un message d'aide et quitte.
- `-V, --version` : Affiche la version de la commande et quitte.

## Common Examples

### Exemple 1 : Inverser une chaîne de caractères
Pour inverser une chaîne de caractères entrée directement dans le terminal :

```bash
echo "Bonjour" | rev
```
**Sortie :**
```
ruojnoB
```

### Exemple 2 : Inverser le contenu d'un fichier
Pour inverser chaque ligne d'un fichier nommé `texte.txt` :

```bash
rev texte.txt
```

### Exemple 3 : Enregistrer le résultat dans un fichier
Pour inverser les lignes d'un fichier et enregistrer le résultat dans un nouveau fichier `inverse.txt` :

```bash
rev texte.txt > inverse.txt
```

### Exemple 4 : Utiliser rev avec d'autres commandes
Vous pouvez combiner `rev` avec d'autres commandes, par exemple, pour inverser les lignes d'une liste de fichiers :

```bash
ls | rev
```

## Tips
- Utilisez `rev` avec des fichiers de texte pour des résultats rapides et efficaces.
- Combinez `rev` avec d'autres commandes comme `sort` ou `grep` pour des manipulations de texte plus avancées.
- Pensez à rediriger la sortie vers un fichier si vous travaillez avec de grandes quantités de données pour éviter de perdre des informations.