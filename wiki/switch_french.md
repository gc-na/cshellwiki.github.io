# [Linux] Bash switch usage : Changer de contexte d'exécution

## Overview
La commande `switch` en Bash permet de changer le contexte d'exécution d'un script ou d'une commande. Elle est souvent utilisée pour gérer des conditions et exécuter différentes sections de code en fonction des valeurs fournies.

## Usage
La syntaxe de base de la commande `switch` est la suivante :

```bash
switch [options] [arguments]
```

## Common Options
- `-c` : Permet de spécifier une condition.
- `-d` : Définit une valeur par défaut si aucune condition n'est remplie.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `switch` :

### Exemple 1 : Utilisation simple
```bash
switch -c "valeur" {
    case "option1":
        echo "Vous avez choisi l'option 1"
        break
    case "option2":
        echo "Vous avez choisi l'option 2"
        break
    default:
        echo "Option non reconnue"
}
```

### Exemple 2 : Valeur par défaut
```bash
switch -d {
    case "rouge":
        echo "Couleur rouge sélectionnée"
        break
    case "bleu":
        echo "Couleur bleue sélectionnée"
        break
    default:
        echo "Couleur non reconnue"
}
```

### Exemple 3 : Plusieurs conditions
```bash
switch -c "choix" {
    case "a":
        echo "Vous avez choisi A"
        break
    case "b":
        echo "Vous avez choisi B"
        break
    case "c":
        echo "Vous avez choisi C"
        break
    default:
        echo "Choix invalide"
}
```

## Tips
- Utilisez des commentaires dans votre code pour clarifier les différentes sections de votre `switch`.
- Assurez-vous de toujours inclure une option par défaut pour gérer les cas non prévus.
- Testez vos conditions avec des valeurs variées pour garantir que votre script fonctionne comme prévu.