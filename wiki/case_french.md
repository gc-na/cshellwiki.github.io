# [Linux] Bash case : Gérer les choix conditionnels

## Overview
La commande `case` en Bash est utilisée pour effectuer des comparaisons multiples sur une variable. Elle permet de simplifier le code en remplaçant plusieurs instructions `if` par une structure plus lisible et organisée. Cela est particulièrement utile lorsque vous devez vérifier une variable contre plusieurs valeurs possibles.

## Usage
La syntaxe de base de la commande `case` est la suivante :

```bash
case [variable] in
    [pattern1])
        [commands1]
        ;;
    [pattern2])
        [commands2]
        ;;
    *)
        [default_commands]
        ;;
esac
```

## Common Options
La commande `case` ne possède pas d'options spécifiques, mais elle utilise des motifs (patterns) pour faire correspondre des valeurs. Voici quelques éléments à considérer :

- `*` : Correspond à n'importe quelle chaîne de caractères.
- `?` : Correspond à un seul caractère.
- `[...]` : Correspond à un ensemble de caractères.

## Common Examples

### Exemple 1 : Vérification d'un jour de la semaine
```bash
jour="lundi"

case $jour in
    lundi)
        echo "C'est le début de la semaine."
        ;;
    vendredi)
        echo "C'est presque le week-end."
        ;;
    samedi|dimanche)
        echo "C'est le week-end !"
        ;;
    *)
        echo "C'est un jour de semaine."
        ;;
esac
```

### Exemple 2 : Vérification d'une extension de fichier
```bash
fichier="document.txt"

case $fichier in
    *.txt)
        echo "C'est un fichier texte."
        ;;
    *.jpg|*.png)
        echo "C'est une image."
        ;;
    *.sh)
        echo "C'est un script Bash."
        ;;
    *)
        echo "Type de fichier inconnu."
        ;;
esac
```

### Exemple 3 : Choix d'une action en fonction d'une option
```bash
option="install"

case $option in
    install)
        echo "Installation en cours..."
        ;;
    remove)
        echo "Suppression en cours..."
        ;;
    update)
        echo "Mise à jour en cours..."
        ;;
    *)
        echo "Option non reconnue."
        ;;
esac
```

## Tips
- Utilisez des motifs globaux pour simplifier les correspondances, comme `*.txt` pour les fichiers texte.
- N'oubliez pas de terminer chaque bloc de commande par `;;` pour éviter des erreurs de syntaxe.
- Le motif `*` peut être utilisé comme un cas par défaut pour gérer les valeurs non spécifiées.