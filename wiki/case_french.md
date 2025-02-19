# [Unix] C Shell (csh) case : Gérer les structures conditionnelles

## Overview
La commande `case` dans C Shell (csh) permet d'effectuer des comparaisons conditionnelles sur des variables. Elle est utilisée pour exécuter différentes sections de code en fonction de la valeur d'une variable, facilitant ainsi la gestion des choix multiples.

## Usage
La syntaxe de base de la commande `case` est la suivante :

```csh
case [variable] in
    [pattern1] ) [command1];;
    [pattern2] ) [command2];;
    ...
    * ) [default_command];;
esac
```

## Common Options
La commande `case` ne possède pas d'options spécifiques, mais elle utilise des motifs pour faire correspondre les valeurs. Voici quelques motifs courants :
- `*` : correspond à n'importe quelle chaîne.
- `?` : correspond à un seul caractère.
- `[abc]` : correspond à un caractère parmi ceux spécifiés (a, b ou c).

## Common Examples

### Exemple 1 : Vérifier un jour de la semaine
```csh
set day = "Lundi"
case $day in
    "Lundi" ) echo "C'est le début de la semaine";;
    "Samedi" | "Dimanche" ) echo "C'est le week-end";;
    * ) echo "C'est un jour de semaine";;
esac
```

### Exemple 2 : Identifier un type de fichier
```csh
set file = "document.txt"
case $file in
    *.txt ) echo "C'est un fichier texte";;
    *.jpg | *.png ) echo "C'est une image";;
    * ) echo "Type de fichier inconnu";;
esac
```

### Exemple 3 : Choisir une action selon une entrée utilisateur
```csh
set action = "sauvegarder"
case $action in
    "sauvegarder" ) echo "Sauvegarde en cours";;
    "restaurer" ) echo "Restauration en cours";;
    "quitter" ) echo "Fermeture du programme";;
    * ) echo "Action non reconnue";;
esac
```

## Tips
- Utilisez des motifs spécifiques pour éviter des correspondances inattendues.
- N'oubliez pas d'inclure une option par défaut (`*`) pour gérer les cas non prévus.
- Testez toujours vos conditions pour vous assurer qu'elles fonctionnent comme prévu.