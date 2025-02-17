# [Linux] Bash if : Évaluer des conditions

## Overview
La commande `if` en Bash est utilisée pour évaluer des conditions et exécuter des commandes en fonction du résultat de cette évaluation. Elle permet de contrôler le flux d'exécution des scripts en prenant des décisions basées sur des conditions booléennes.

## Usage
La syntaxe de base de la commande `if` est la suivante :

```bash
if [ condition ]; then
    # commandes à exécuter si la condition est vraie
fi
```

## Common Options
- `-e`: Vérifie si un fichier existe.
- `-d`: Vérifie si un répertoire existe.
- `-f`: Vérifie si un fichier est un fichier régulier.
- `-z`: Vérifie si une chaîne est vide.
- `-n`: Vérifie si une chaîne n'est pas vide.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `if` :

### Exemple 1 : Vérifier l'existence d'un fichier
```bash
if [ -e "mon_fichier.txt" ]; then
    echo "Le fichier existe."
else
    echo "Le fichier n'existe pas."
fi
```

### Exemple 2 : Vérifier si une variable est vide
```bash
ma_variable=""
if [ -z "$ma_variable" ]; then
    echo "La variable est vide."
else
    echo "La variable n'est pas vide."
fi
```

### Exemple 3 : Vérifier si un répertoire existe
```bash
if [ -d "/mon/répertoire" ]; then
    echo "Le répertoire existe."
else
    echo "Le répertoire n'existe pas."
fi
```

### Exemple 4 : Comparaison de nombres
```bash
nombre1=10
nombre2=20
if [ $nombre1 -lt $nombre2 ]; then
    echo "$nombre1 est inférieur à $nombre2."
fi
```

## Tips
- Toujours utiliser des espaces autour des crochets `[` et `]` pour éviter des erreurs de syntaxe.
- Utilisez des parenthèses doubles `[[ ]]` pour des comparaisons plus avancées, comme les expressions régulières.
- Pensez à utiliser `elif` pour tester plusieurs conditions dans une seule structure `if`.