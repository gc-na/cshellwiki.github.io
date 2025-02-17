# [Linux] Bash exit usage : Terminer un script ou une session

## Overview
La commande `exit` dans Bash est utilisée pour terminer un script ou une session de terminal. Elle permet de quitter le shell en renvoyant un code de sortie, qui peut être utilisé pour indiquer si le script s'est exécuté correctement ou s'il y a eu une erreur.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
exit [options] [n]
```

Ici, `n` est un entier qui représente le code de sortie. Si aucun code n'est spécifié, le code de sortie par défaut est celui de la dernière commande exécutée.

## Common Options
- `n` : Un entier qui indique le code de sortie. Par convention, un code de sortie de `0` indique un succès, tandis qu'un code différent de `0` indique une erreur.

## Common Examples

### Exemple 1 : Quitter un script avec succès
```bash
#!/bin/bash
echo "Le script s'exécute correctement."
exit 0
```

### Exemple 2 : Quitter un script avec une erreur
```bash
#!/bin/bash
echo "Une erreur s'est produite."
exit 1
```

### Exemple 3 : Quitter une session de terminal
```bash
exit
```

### Exemple 4 : Utiliser le code de sortie d'une commande précédente
```bash
#!/bin/bash
ls /inexistant
exit $?  # Quitte avec le code de sortie de la commande ls
```

## Tips
- Utilisez `exit 0` pour indiquer que votre script s'est terminé avec succès.
- Utilisez des codes de sortie différents pour signaler différents types d'erreurs, ce qui peut aider au débogage.
- Dans les scripts, il est souvent utile d'utiliser `exit` à la fin pour s'assurer que le script se termine correctement.